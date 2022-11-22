+++
# About widget.
widget = "blank"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = false  # Activate this widget? true/false
weight = 20  # Order that this section will appear in.
title = "SHUD system"

author = "admin"
+++

The Simulator for Hydrologic Unstructured Domains (SHUD - pronounced “SHOULD”) is a multiprocess, multiscale, and multitemporal model that integrates major hydrologic processes and solves the physical equations with the finite volume method. The governing equations are solved within an unstructured mesh domain consisting of triangular cells. The variables used for the surface, vadose layer, groundwater, and river routing are fully coupled together with a fine time step. The SHUD uses the 1D unsaturated flow and 2D groundwater flow. River channels connect with hillslope via overland flow and baseflow. The model, while using distributed terrestrial characteristics (from climate, land use, soil, and geology) and preserving their heterogeneity, supports efficient performance through parallel computation.
