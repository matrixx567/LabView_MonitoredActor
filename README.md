# Monitored Actor

Any actor-based system can get complicated quickly. The MGI Monitored Actor provides a quick and easy way to visualize what actors are currently running in the system and provides tools to help debug those running actors.

## The Question

Actor based systems are dynamic. The number and types of actors running is constantly changing and reacting to user input, measured data, or any number of other factors. This is great news when developing complex and efficient software, this is bad news when it comes to debugging. What actors are running right now? How do I highlight execution on one instance of a running actor? How do I stop a runaway actor?!?!?

These are frustrating things to deal when developing an actor based application.

## The Solution

The MGI Monitored Actor toolkit provides an easy way to monitor your dynamically spawned actor application. It provides a nice user interface that allows you visualize the actors currently running in the system. From this interface you can easily open the running `Actor core.vi`. This allows you prob/set breakpoints/highlight execution as needed to properly debug your code. Additionally from the user interface you can stop running actors.

## How to use it

### Setup your Actor

The only difference between a monitored actor and a plain-old actor is a monitored actor inherits from `Monitored Actor.lvclass`. Thats it! That means any existing actors you have can be trivially converted to monitored actors, and any new actors just need to inherit from a slightly different parent.

Once your inheritance has been changed, just launch your actor like normal. The Monitored Actor Window will automatically pop up and show the list of running actors.

### Debugging a running Actor

Once your monitored actor is launched, the monitored actor window will launch. This window contains a tree showing the running actors. Double click on any of these actors to open it's `Actor core.vi` currently running clone. This means that you have access to the specific instance of the actor that's running. You can use all of your normal debugging tools like highlight execution, probes, etc.

Additionally, from the monitored actor window you can send stop messages and perform a few other debug tasks.

---

MGI currently works with the GPM Package Manager and decided to stop the support for VIPM. This package is based on the GPM packages of the MGI Monitored Actor. It also add the support of the previously published examples and tool Monitored Actors Switcher.

This VIPM package is based on the following GPM packages:

https://gpackage.io/packages/@mgi/monitored-actor  
https://gitlab.com/mgi/gpm-packages/monitored-actor  

https://gpackage.io/packages/@mgi/monitored-actor-core  
https://gitlab.com/mgi/gpm-packages/monitored-actor-core  

## Installation notes
The original MGI Monitored Actor package isn't set as incompatible package. But considered to remove the original MGI Monitored Actor package before installing this package.

## Legacy Software:
Be sure to change the inheritance of your actors to the provides Monitored Actor of this package.