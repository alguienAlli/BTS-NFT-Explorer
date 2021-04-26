What is an OBJT fIle?

OBJT is a custom format/Convention proposed by 'AlguienAlli', being the main motivation, incorporating separated 3D model files into a single and easy to parse container. It consists of a packager for one OBJ and one png file.

OBJ has been for long time a very useful format for 3D models, it specially shines when used for static models with very simple properties, as in today climate, other container formats easily ramp up the final size of the model. If you do not need animations, vertex colors, fancy materials or the such, OBJ is the way to to. The other side of the problem, is that OBJ does not self-contain the texture of the model. OBJT will be evaluated soon to optionally incorporate the highly efficient compression algorith Zstd for fast loading times and even lower file sizes.

An OBJT file is formated in the following way:

First byte = unused, in the future will be used to indicate Zstd compression.  
Next 4 bytes: uint32 (.obj file byte array length)  
Next n bytes = .obj bytes.  
Next 4 bytes: uint32 (.png file array length)  
Next n bytes = .png bytes.  
  
