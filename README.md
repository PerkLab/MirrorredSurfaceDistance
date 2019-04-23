# MirrorredSurfaceDistance
This is a 3D Slicer Module which is used to compute the surface-to-surface between either:
* The input surface and the mirror surface of the input surface
* Between two different surfaces 

## Prerequisite
* The slicer module **Model to Model Distance** from the Extension Manger must be downloaded 

## User Information 
* The Input Fiducial Selector is used to crop the model within the fiduicals and only display surface-to-surface distance within the formed loop (This is normally the breast boundary fiducials) 
* If only one input model is passed as input a mirorr model of the original model will be created
* Registration automatically occurs between the two models using ICP
  * If the inital regstration fails (ie. Original model and mirrored Registered Input or two input models do not align correctly) create a rough manual registration in the transforms model using the MirrorInput (**not registered**) or the second input 
  * Pass the manual registration tranform as the input for the initial transform and rerun
* Once the output model is created go to the Models module and select the output model 
  * Under display select Scalars 
  * Ensure Signed is selected for Active Scalar
  * Choose Either the Cold to Hot or Hot to Cold Rainbow for the colour Table
  * To create a stanadrd scale ensure the display range is equal on both sides of 0, this is done by setting the scalar Range model to Manual 
