A workflow that create sensor fusion data from rgb and thermal camera.

1. Get field layouts from BETYdb, by function: terra_common.CoordinateConverter().bety_query()
2. Generate a list of rois that look at the center of plots, you can specify the field of view for the ROI(0.5 meter now), by function: generate_roi_list_all_plots_center_plant()
3. Crop initial sensor fusion data from both sensor, inputs from pre-cropped-to-plot data(generated by GWUvision/OPEN/crop/stereo.py(thermal.py)), and the roi list, by function: crop_from_both_sensors()
4. Resize,rename and redirect initial data to a standard form that easy for deep learning, by function: reorganize_main(), init_joint_main() and split_val_test_main() 
