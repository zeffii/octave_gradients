# octave_gradients
gradients for Cycles color ramps

installation, use Install from File and make sure it's enabled:
![image1](https://cloud.githubusercontent.com/assets/619340/10429386/66712cc4-70f8-11e5-833d-6432f3f51a14.png)

### What is it
____

This adds a panel called Octave Gradient Demo to the Cycles node view. From here you can choose the gradient by name, it will display the colors in the same panel. These are a group of 14 commonly used gradients you might be familiar with from Octave or Matlab. You could easily add extra palettes by augmenting the `hexviz` dict in `__init__.py`, I might extend this feature at a later stage.

![image2](http://i.stack.imgur.com/9TpRj.png)

### Usage
____

1. enable addon
2. make sure renderer is set to cycles 
3. create a new node based material
4. get a view open to see the nodes for the material
5. in the right side panel (use N to show the shelf) you'll see the _Octave Gradient Demo_ panel.
6. initially this will show all black ramp slots until you change the palette from the dropdown.
7. If you haven't already added a ColorRamp node to the current Material, that's OK the _set gradient_ button adds a ramp for you.
  If you don't already have a ColorRamp in the nodeview
   - If you use _set gradient_  it will place one at (0,0) of the nodeview canvas.
   - If you use the operator called `Octave Cradient Operator` from the spacebar search feature in the nodeview, then it will add a new ColorRamp roughly where you mouse cursor is.

The addon kind of expects that you won't be using more than one ColorRamp node per material. It's the way I use it, but I can imagine that a node-picker would be handier so you can choose freely -- but this is not implemented, and if i'm the only one using it that's the way it will stay until I need more functionality.
