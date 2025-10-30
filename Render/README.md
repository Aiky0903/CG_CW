# Level 2 Stall:
The general design of the stall is referenced from Ray Studio's tutorial video at https://youtu.be/iE6mZIICHxM with some detail changes. First, the outer split partition design is made using loop cuts on a cube to separate the regions and applying solidify to give it some volume.
 
Another block is added within it to finish the base.
 
Next, a pillar of the stall is added on one corner of the block.
 
Next, we applied a mirror modifier to easily copy the pillars on the other corners of the stall.
  
Next, we add a roof to the stall.
 
## The materials used for the model are as follows:
-	Roof uses principled BSDF with minor modifications.
-	Pillars use a wood material made by Ksenia Starkova on https://starkosha.gumroad.com/l/vtfsb
-	The partitions also use a wood material by Ksenia Starkova on https://starkosha.gumroad.com/l/vtfsb
-	The internal block uses principled BSDF



# Level 2 Gate terminal:
No references were made for this model. First, a cube object is rounded using the bevel tool.
 
Then, a scanner for train tickets or pass is added to the top of the terminal on both sides using mirror tool.
 
Then similarly, the direction panel (indicating direction of gate opening and closure) is added to the terminal on both sides using the mirror tool.
 
Then, the hinges of the door are added to both sides of the terminal using the mirror tool.
 
Then, the gate is attached to both sides of the hinges.
 
## The materials used are as follows:
-	Terminal uses principled BSDF with metallic properties.
-	Scanner uses a modified stainless-steel material imported from BlenderKit
-	The hinges and gates uses principled BSDF


# Level 2 Ticket Counter:
There are no references used for this model.
First, a cube is created and its faces on the z-axis are removed. Then, a solidify modifier is added to give volume to the faces. The back face is then extended and subdivided into parts to model the door and doorframe on both sides.
 
Then, the faces on the left and right are also extended.
 
Then, some cuboids are attached to the sides of the counter as a serving table.
 
The roof is then attached to the top of the model.
 
Then, a cuboid is attached to the top of the model to serve as the light board.
 
Some texts are then added to the board.
 
Lastly, the window is created.
 
## The materials used for this model are as follows:
-	Window uses transparent plastic material from BlenderKit
-	The board uses metallic BSDF
-	Text uses the emission material
-	All other materials used are principled BSDF

# Level 2 Barrier:
The barriers are added to the scene at the end.
First, a plane is folded and placed on the floor as a scaffold for the barrier.
 
A wireframe modifier is added to the barrier along side with a skin modifier.
The model is then loop cutted to add more vertices to act as vertical beams.
 
## Materials used for this model are as follows:
-	Light iron material from BlenderKit

# Level 2 Imports:
-	Potted plant from BlenderKit
-	Stool from BlenderKit
-	Bananas, grapes, mangos from BlenderKit
-	Bowl from BlenderKit
-	Escalator by Alex1402 at  https://www.turbosquid.com/3d-models/escalator-2264462

# Level 3 Train:
The design was from a tutorial made from Imphenzia (https://www.youtube.com/watch?v=ar2ZOPddjTM). First was to cut the cube in half and mirror so that only one side is edited. Then the front top corners are dragged back to make a streamline front. Windows, doors, and headlights were modeled with inset and extrusions. For the wheels and the base, cylinders and squares were added and aligned so that four pairs of wheels are on the front and the back of the train. After modelling one train, it was the duplicated to make a double sided train.
 
## The materials used for the model are as follows:
-	Endesga 32 Palette used for the main body (https://lospec.com/palette-list/endesga-32)
-	Own principled BSDF used for headlights and windows for emission and color. 



# Level 3 Benches:
No references were made for this model. First one of the legs was modelled by cutting a cube and moving the faces. the it was duplicated to make a pair of legs with the desired length. Then another cube was made long and thin to mimic the wooden part of the bench, to which then was duplicated to fill in the bench position.
 
## The materials used are as follows:
-	Endesga 32 Palette used for the main body (https://lospec.com/palette-list/endesga-32)


# Level 3 Platform:
The platform was the blender file that attaches everything together. First get the desired width and length (x and y) to match the other levels. then the train was and put into the position to make cuts so that there can be an indent where the train can be. After adding indents, the face was pulled down to make the indent then 2 more cubes were added to make the joint bars for the rails and aligned to the train wheel. Then another object was made using a cube that is narrowed and elongated to make rails. It is a separate object from the platform so that the array modifier can make multiple rails. Then after positioning the train to the rails, benches were added to fill in the blank positions.
 
## Materials used for this model are as follows:
-	Concrete floor from BlenderKit
-	Endesga 32 Palette used for the wood portion of the rails (https://lospec.com/palette-list/endesga-32)


# Level 3 Sign:
There are no references used for this model. This was added after the platform to fill in the space. The it was made from a single cube that was narrowed and elongated to act as the frame. Then inset and extruded to make a the inner portion where the sign would be.
 
## The materials used for this model are as follows:
-	Endesga 32 Palette used for the frame (https://lospec.com/palette-list/endesga-32)
-	The inner portion uses principled BSDF to added an emissive element. 
