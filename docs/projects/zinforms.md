# ZinForms
ZinForms makes designing user interfaces for MonoGame easy.

## Getting started
First import the DLL dependency and reference the namespace `Zintom.ZinForms`

Declare a `ZinFormsHost` in the main class of your game loop, usually in *Game.cs*, for the purpose of this tutorial I will name mine `formsHost`.

**Important:** Make sure you add `formsHost.Update(gameTime)` and `formsHost.Draw(gameTime, spriteBatch)` to your *Update()* and *Draw()* methods.

Now you're ready to start adding windows/controls to your application.

## Adding a window
Adding a window to the ZinFormsHost is as simple as creating a new `Window` object, specifying its parent `ZinFormsHost`, its size and location.
```
Window window1 = new Window(host: formsHost, size: new Point(200, 200), location: new Point(150, 150));

formsHost.WindowManager.Add(window1);
```
Boom, a window appears!

## Adding controls
Now lets add a control to our window, a simple label will do; we use the most basic constructor and will specify other parameters through the object initializer.
```
Label label1 = new Label(host: formsHost)
{
  Text = "I am a label.",
  Location = new Point(10, 10)
};
```
Adding it to the window is as easy as `window1.AddChild(label1)`.

Let's see what we've got so far!

![BasicWindow1](https://user-images.githubusercontent.com/18383281/99443377-a50a5500-2912-11eb-8b05-3876e83a6ebf.png)
