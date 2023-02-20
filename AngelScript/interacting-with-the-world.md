# **AngelScript Documentation**

Now to look at how we can use AngelScript to interact with the game environment.

## **Lighting Example**

Let's say you have an idea to cut power to every light in the scene or you want to flicker a light due to sparks.
Whatever it may be. this little example should be able to show you how to get a light to work inside of your scene.

Let's first of all create the script. Name it whatever you like, and let's create a variable to hold onto a `LightComponent` Pointer.
> Private variables won't show in the **Inspector**. 

```ml
private LightComponent@ m_LightComponent = null;
```

Now as you can see the variable is `null`. Meaning it isn't usable just yet.
We now need to find the light entity. In this case we need to set it.

In your `Start` function we need to search the assigned entity if it has a light component.

```ml
void Start()
{
    @m_LightComponent = entity.GetLightComponent();
}
```

Let's say there isn't a light on this entity. We need a way of telling us if we cannot find one. A way we can do this is by logging to the **Console**.

```ml
if(m_LightComponent == null) { Console.Log("Light Component not found!"); }
```
