# Floor Plan Segmentation with Boundary-Aware Context Fusion  
**Efficient Deep Learning Architecture for Automated Floor Plan Analysis**  

This repository contains the implementation of a novel deep learning model designed to enhance semantic segmentation of architectural floor plans. Our approach builds on a dual-branch encoder-decoder architecture, integrating advanced attention mechanisms to address the challenge of capturing both local and global spatial dependencies inherent in complex architectural layouts.  

## Key Features:  

- **Global Context (GC) Module**: Positioned at the encoder bottleneck, this module captures long-range spatial relationships using cross-attention with learnable global tokens. This enhances the model's ability to interpret spatial context across the entire floor plan.  

- **Efficient Multi-Head Self-Attention (EMHSA)**: Applied in the decoder stages, this optimized variant of multi-head self-attention employs spatial reduction techniques to maintain computational feasibility without compromising on capturing critical contextual information.  

- **Feature Fusion Attention (FFA) Modules**: Incorporated within the dual-decoder structure, these modules refine room segmentation by leveraging boundary information through efficient multi-head self-attention. This fusion strategy improves the integration of room boundary features for accurate room type predictions.  

- **Room Boundary Aware Context Fusion Module (RBACFM)**: Combines the GC and FFA modules, creating a synergy that integrates global spatial relationships and boundary-aware feature fusion. This results in improved segmentation of both room types and structural boundaries.  

- **Performance Gain**: Achieves significant improvements over the baseline model on the R3D dataset:  
  - **Mean Intersection over Union (mIoU)**: Increased by 8.6% (from 53.5% to 62.1%)  
  - **Overall Pixel Accuracy**: Increased by 4.4% (from 85.0% to 89.4%)  
  - **Per-Class Improvements**: Notable gains in segmentation accuracy, particularly for complex room categories such as Bedrooms (+16.0%), Living/Kitchen/Dining rooms (+15.0%), and Hallways (+10.4%).  

## Applications:  
- Automated building analysis  
- 3D reconstruction and floor plan modeling  
- Design automation and architectural CAD tools  
- Smart home and indoor navigation systems  

## Experimental Results:  
The model has been evaluated on the **R3D floor plan dataset**, demonstrating improved accuracy across diverse architectural layouts. Our qualitative analysis shows that the model effectively handles complex spatial relationships, long-range dependencies, and boundary-affected room classifications.

