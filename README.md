# Inpainting
The final project for the discipline SCC0251-Image Processing.

## Basic information
 - **Title:** Inpainting using search of texture information

 - **Developer:** Bruno Manias Trazzi

 - **Objective:** Image reconstruction using inpainting techniques

 - **Application:** The reconstruction of an image that has missing pixels or informations that should be removed, such as objects that are unwanted on the scene, or effects that interfered in the image acquisition, etc.

## Methodology
The damaged image and the area to be inpainted will be provided to the program. The area to be inpainted  will be taken as a mask where white pixels mark the ones that should be inpainted in the damaged image.
#### Algorithm
The the program will select a pixel to inpaint and define a neighbourhood around it, then it will extract texture information from it, this will be the reference neighbourhood. So it will slide a window, of same size as the one used in the reference neighbourhood, trough the image and extract texture information from it, then compare it with the reference one. The pixel at the center of the neighbourhood that has the higher similarity with the reference one will be copied to the pixel we selected for inpaint. The program will repeat these steps until all there are no pixels left to inpaint.
