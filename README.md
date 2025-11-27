# Canny-Edge-Detection

## INTRODUCTION:
The Canny Edge Detector is a highly effective and widely used computer vision algorithm designed to find optimal edges in images. It's often referred to as the optimal detector because it satisfies three main criteria:
- Low Error Rate: It minimizes the chances of finding edges where none exist (false positives) and missing real edges (false negatives).
- Good Localization: The detected edge points are accurately positioned close to the true edges.
- Single Response: It provides a single, thin edge response for a single actual edge.

## PROCECURE:
1. Smooth Image (Gaussian Filter): The image is filtered using a Gaussian blur to suppress noise and minor texture variations that could otherwise be mistaken for edges.
2. Find Gradients (Sobel Operator): The strength (magnitude) and direction of intensity changes are calculated across the image, highlighting all potential edge locations.
3. Thin Edges (Non-Maximum Suppression): Only the local maximum gradient values are preserved along the gradient direction, which results in the detected edges being reduced to a single-pixel width.Determine Edge 4. Categories (Double Thresholding): Two threshold values ($\text{High}$ and $\text{Low}$) are used to categorize potential edges as Strong (definite) or Weak (uncertain).
5. Finalize Outlines (Hysteresis Tracking): Weak Edges are kept only if they are directly connected to a Strong Edge, ensuring the final output consists of continuous, noise-free object outlines.
