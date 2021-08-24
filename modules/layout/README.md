These are the actual layout files.  Adding a new layout requires that you implement a few #aliases:
* layout_init - do splits, draw lines, panels, etc.
* update_top_panel - if you have a top panel, update the content here
* update_bottom_panel - If you have a bottom panel, update them here
* display_right_tiles, display_left_tiles - if you have side panels, update them here
* layout_comms_update - if you have a comms display on screen, fire the update

You also need to update the valid_layouts list in layout module.

This will change over time, and I think maybe we should have a file extension on the layout files (.layout?).
For now, they're loaded into class layout-selection and updated by the layout command.
