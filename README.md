# Harati Ma Gaussian Splatting


# Abstract
Swayambhunath Stupa is a prevalent Buddhist temple located
in Nepal. It is a cultural heritage site that is central
to the practice of many Buddhists in the region. Dr. Lauren
Leve and Dr. Jim Mahaney partnered to create a 3D model
of the temple, utilizing photogrammetry, drone footage, and
LiDAR laser scans. Originally, the model had been put
through Reality Capture, Scene, and Blender to combine
all of the data to make a cohesive model; however, there
were anomalies within the model, such as holes in certain
sections of the stupa, flying objects that were accidentally
captured, and a general lack of detail. The goal of the project
was to create a model which preserved the details of the
stupa and created a better visual experience.

# Introduction 
located in Nepal. It is a cultural heritage site that is central
to the practice of many Buddhists in the region. Dr.
Lauren Leve and Dr. Jim Mahaney partnered to create a
3D model of the temple, utilizing photogrammetry, drone
footage, and LiDAR laser scans. Originally, the model had
been put through Reality Capture, Scene, and Blender to
combine all of the data to make a cohesive model; however,
there were anomalies within the model, such as holes in certain
sections of the stupa, flying objects that were accidentally
captured, and general lack of detail. The goal of the
project was to create a model which preserved the details of
the stupa and created a better visual experience.
In order to solve this issue, Dr. Praneeth Chakravarthula
suggested using Gaussian Splatting to render a better model.
Gaussian Splatting is an advanced rendering technique used
in computer graphics to represent 3D models with high fidelity
and detail. The approach involves approximating the
geometry and appearance of an object using Gaussian distributions
instead of traditional polygon meshes. Each Gaussian
acts as a soft 3D point, encoding attributes such as position,
color, and opacity in a probabilistic manner. By aggregating
and optimizing these Gaussian distributions, the
technique can effectively reconstruct complex scenes, fill in
gaps, and smooth anomalies, producing more accurate and
visually appealing results.
Gaussian Splatting is able to handle noisy data, such as
those derived from photogrammetry or laser scans. Unlike
conventional methods that may struggle with incomplete
or imperfect datasets, Gaussian Splatting integrates
spatial and color information in a unified framework, minimizing
visual anomalies like holes and floating elements.
This makes it particularly suited for cultural heritage preservation
projects, where maintaining authenticity and detail is
the priority. In this project, Gaussian Splatting was applied to address
the anomalies in the initial model of the Swayambhunath
Stupa, including gaps, flying objects, and lack of
detail. The technique allowed for a more immersive reconstruction,
preserving the details of the stupa while ensuring
a visually coherent representation.

# Inria Gaussian Splatting and Zidane Cluster 
To address the computational constraints of my local
hardware, I utilized the Zidane cluster at UNC Chapel
Hill, a computing resource equipped with robust GPUs.
This setup provided the necessary power to process the
abundance of photogrammetry data of the Swayambhunath
Stupa. Within the Zidane cluster, I worked with the
GraphDeco INRIA Gaussian Splatting repository, a tool designed
for reconstructing 3D models with exceptional detail
and accuracy. Focusing on specific sections of the model, I
began with Harati Ma, a smaller but architecturally intricate
part of the stupa, as a proof of concept for the Gaussian
Splatting technique.
By isolating Harati Ma, I was able to refine my approach
to Gaussian Splatting and optimize the pipeline for handling
the detailed photogrammetry data. The cluster’s computational
capabilities enabled iterative experimentation and
processing of the high-density data, ensuring a seamless
reconstruction. This laid the groundwork for scaling the
methodology to larger sections of the stupa. The results
from Harati Ma demonstrated the potential of Gaussian
Splatting to capture details while maintaining visual and
structural coherence.

# Future Plans 
The reconstruction of Harati Ma using Gaussian Splatting
represents a significant step forward in creating detailed
and visually coherent 3D models from photogrammetry
data. The resulting point cloud, stored as a ply file, was
successfully visualized using SuperSplat, an online viewer
to render point cloud and Gaussian splat data.
The reconstruction of Harati Ma using Gaussian Splatting
yielded a model with remarkable details, capturing
intricate features that were previously difficult to render.
However, the final output still included considerable visual
noise and anomalies, such as stray points and inconsistencies
in certain regions.
One potential avenue for improvement involves integrating
a method specifically designed to address these anomalies.
While Gaussian Splatting produces models with intricate
details, additional techniques, such as noise filtering or
outlier removal algorithms, could be applied to the existing
ply file. After processing this, the point cloud could be
run through the visual editor again, and observations can be
made about how much cleaner the model looks.

# Harati Ma Reconstructions and Resources 
Point Cloud File with Harati Ma construction:
https://drive.google.com/file/d/1XvKuqbozqkTSk6p1O--paWz1iU1gigts/view?usp=sharing

GraphDECO INRIA Gaussian Splatting Repository:
https://github.com/graphdeco-inria/
gaussian-splatting

SuperSplat: Online Viewer for Point Clouds: 
https://playcanvas.com/supersplat/editor/

Video of Harati Ma, courtesy of Benjamin Edwards:
https://drive.google.com/file/
d/1VKHqLzXPenFwTE7PXbr0J52EYnTYdR5T/
view?usp=sharing
