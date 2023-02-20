# **AngelScript Documentation**

This section will cover some of the basics on how to use AngelScript inside of the engine.
If you haven't used AngelScript before or need a bit of a refresher on how to use it. We 
suggest you read through AngelScript documentation to grasp the basics of the language
syntax.
Link: [https://www.angelcode.com/angelscript/sdk/docs/manual/doc_script.html](https://www.angelcode.com/angelscript/sdk/docs/manual/doc_script.html)

## **Getting Started**

When you create a new script it should look a little something like this.

```ml
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

```ml
Entity@ entity;
```
This here is the Script Constructor. Basically the first thing that is called when we run the game, even before
Start(). What this does is set a reference to the Entity that the script is attached to. This constructor **must**
stay the same.
> If you do understand how constructors work, feel free to change it up how you like. Remeber if you still want
> access to the entity you have assigned the script to, it is strongly recommended that you leave the default setup
> inside the constructor as well.

```ml
Example(Entity@ obj)
{
    @entity = obj;
}
```

Now that we have sorted out what the top of our script does, let's look at the two functions that come with our script.

This is the `Start` function, essentially called at the start of the game or when the entity is about to begin the main loop.
> This will only be called once!
```ml
void Start()
{

}
```

This is the `Update` fucntion, this will be called every frame.
> Execution times may vary due to the performance of the game. Make sure to be cautious of that.
```ml
void Update()
{

}
```
