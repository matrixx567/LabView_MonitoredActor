Any actor-based system can get complicated quickly. The MGI Monitored Actor provides a quick and easy way to visualize what actors are currently running in the system and provides tools to help debug those running actors.

# Important Note!

This package just contains the core framework for the monitored actor tool. It **does not** contain an implementation of the Actor Monitor. Be sure to install another package that actually contains a Actor Monitor (such as MGI's ) or implement your own Actor Monitor.

## The Question

Actor based systems are dynamic. The number and types of actors running is constantly changing and reacting to user input, measured data, or any number of other factors. This is great news when developing complex and efficient software, this is bad news when it comes to debugging. What actors are running right now? How do I highlight execution on one instance of a running actor? How do I stop a runaway actor?!?!?

These are frustrating things to deal when developing an actor based application.

## The Solution

The MGI Monitored Actor toolkit provides an easy way to monitor your dynamically spawned actor application. It provides a nice user interface that allows you visualize the actors currently running in the system. From this interface you can easily open the running `Actor core.vi`. This allows you prob/set breakpoints/highlight execution as needed to properly debug your code. Additionally from the user interface you can stop running actors.

## How to use it

### Setup your Actor

The only difference between a monitored actor and a plain-old actor is a monitored actor inherits from `Monitored Actor.lvclass`. Thats it! That means any existing actors you have can be trivially converted to monitored actors, and any new actors just need to inherit from a slightly different parent.

Once your inheritance has been changed, just launch your actor like normal. The Actor Monitor will automatically pop up and show the list of running actors.

### Debugging a running Actor

Once your monitored actor is launched, the Actor Monitor will launch. This window (although it doesn't have to be a window...) contains a tree showing the running actors. Double click on any of these actors to open it's `Actor core.vi` currently running clone. This means that you have access to the specific instance of the actor that's running. You can use all of your normal debugging tools like highlight execution, probes, etc.

Additionally, from the Actor Monitor you can send stop messages and perform a few other debug tasks.

## The Actor Monitor

The Actor Monitor is the main entry point for debugging a Monitored Actor. This is an abstract interface. As actors in the system are launched, the Actor Monitor will receive messages and build the `Monitor Data.lvclass` structure. This data structure can be used to find information about all of the actors in the system. This data can then be used to build a nice user interface for the system.

Since monitoring actors is a debugging tool by default the actor monitor is NOT launched when the application is launched in the run time engine.

### Selecting the right Actor Monitor

When your first actor is launched, the monitored actor framework tries to find the correct Actor Monitor, by default, it uses the first child of `Actor Monitor.lvclass` that it finds in memory. If this guess isn't right, it's possible to tell the framework what type of actor monitor to use by calling the `Set Actor Monitor.vi` method and wiring in the specific Actor Monitor type. This same method can be used to get the Actor Monitor to be launched in the run time environment.

## Contributing

See [Contributing.md](CONTRIBUTING.md) for information on how to submit pull requests. Bugs can be reported using the repositories issue tracker.

#### _This package is implemented with LabVIEW 2017_
