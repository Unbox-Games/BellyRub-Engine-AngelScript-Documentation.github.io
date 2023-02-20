# **AngelScript Documentation**

## **Getting Started**

When you create a new script it should look a little something like this.

```AngelScript
class Example : NativeScriptController
{
	Entity@ entity;
	Example(Entity@ obj)
	{
		@entity = obj;
	}

    void Start()
    {

    }

    void Update()
    {

    }
}
```
The top of this file does look a little scary but let's run through what this actually does.

This here is the Entity that this script is attached to. This way you can get the script to easily
interact with the Entity you have assigned this script to and provide it with behaviour and other
cool things.

```AngelScript
Entity@ entity;
```
This here is the Script Constructor. Basically the first thing that is called when we run the game, even before
Start(). What this does is set a reference to the Entity that the script is attached to. This constructor **must**
stay the same.
> If you do understand how constructors work, feel free to change it up how you like. Remeber if you still want
> access to the entity you have assigned the script to, it is strongly recommended that you leave the default setup
> inside the constructor as well.

```AngelScript
Example(Entity@ obj)
{
	@entity = obj;
}
```

## **Interacting with the world!**
