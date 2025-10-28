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
