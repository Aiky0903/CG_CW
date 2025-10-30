# Import Blender Model

## Import

## Model Fix

## Light Fix

# Fix Materials and Texture
Most of the texture and materials imported to Unreal Engine nicely with some requiring minor color changes to match the blender model. The only real problem was the floor surface for the station and platform (middle and bottom level) and the emissive materials.

## Emissive Materials
For the emissive materials, we added a scalar parameter for emissive strength for easy access. We then multiply with the base color to make and connected the node the the 'emission color' on the material node using blueprint. This was done to all emissive materials, with the only difference being the lamp post where that has a trancelucency to allow a light object to emit light from the position it.

## Floor Surface
The reason why the floor did not transfer from Blender to Unreal is because we used BlenderKit for those materials and the UV maps did not import with the model. With this, we decided to use Unreal Engines fab.com the floor materials and texture. For the station (middle floor) we added Seychelles Beige Marble Tiles (https://www.fab.com/listings/f96f2fbe-6935-4adb-820a-895c8968b0f5) and for the platform (lower level) we added Concrete Floor (https://www.fab.com/listings/7cd82969-789d-4d98-ad6c-b2e961df2fda) 

# Camera animation
First, we started off with the camera animation. This is achieved by creating an animation sequence along side with a camera object. The camera animation is relatively simple. We create keyframes that captures the transform variables of the camera object. As such, the camera will gradually move itself to the next keyframe based on its values. We then do this sequencially until it loops back to the point of origin.

# Object animations

## Coffee Shop
For the animation of the coffee shop, we added the emission material of the windows to the sequencer. Then, we added keyframes for the windows and changed its emission strength in the keyframes to simulate people turning individual lights off in the shop.

## Gate terminal
For the animation of the gates, we added the door objects to the sequencer and tracked their transform vrariables. We then rotated the gates in the keyframes to open them.

## Train
For the animation for the train, first we flicker the lights similar to how the coffee shop is done. We add keyframes for the window emission material and change the values in the keyframes to show the flickering effect. 

When the camera starts to exit the scene, we added keyframes for the train's transform properties and change its y-axis to make it start moving out of the station. When the train is outside of the camera's vision, the train's scale is set to 0 to make it disappear from the scene temporarily. As the camera pans away from the scene, we reset the scale of the train back to its original values and set its y-axis in the keyframes to make it start moving back into the station.