---
widget: hero
headless: true
weight: 10
title: SHUD Modeling System
hero_media: hero.png
cta:
  label: 3D Model
  url: https://www.shud.xyz/gallery/shud3d
cta_alt:
  label: 'User Guide'
  url: https://www.shud.xyz/Book_EN/

<!-- cta_note:
  label: <a class="js-github-release" href="https://github.com/SHUD-System/SHUD" data-repo="SHUD-System/SHUD">SHUD Source Code<!-- V --></a>
  url: https://www.shud.xyz/Book_EN/ -->

design:
    background:
        # Name of image in `assets/media/`.
      image: bg.png
        # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.
      image_darken: 1
        #  Options are `cover` (default), `contain`, or `actual` size.
      image_size: cover
        # Options include `left`, `center` (default), or `right`.
      image_position: center
        # Use a fun parallax-like fixed background effect on desktop? true/false
      image_parallax: true
        # Text color (true=light, false=dark, or remove for the dynamic theme color).
      text_color_light: false
      css_class: fullscreen
#    gradient_end: 'LightBlue'
#    gradient_start: 'DeepSkyBlue'
#    text_color_light: true
advanced:
  css_class:
---


The Simulator for Hydrologic Unstructured Domains (**SHUD** - pronounced **“SHOULD”**) is a multi-process, multi-scale integrated hydrological model using the semi-discrete Finite Volume Method.


**Spatial structure**: Unstructured mesh domain --- irregulated triangular network. Three vertical layers: land surface, unstructured and saturated layers.

**Time-step**: Adaptive time-step based on the spatial resolution and slow-fast hydrological processes. The normal time-step ranges from 1 ~ 60 seconds.

The SHUD modeling system is of quick, reproducible and automatic hydrological modeling.


SHUD encapsulates the strategy for synthesizing multi-state distributed hydrological models using the integral representation of the underlying physical process equations and state variables. As a heritage of Penn State Integrated Hydrologic Model (PIHM), the SHUD model is a continuation of 16 years of PIHM modeling in hydrology and related fields since the release of its first PIHM version (Qu, 2004).

Source code of SHUD model is accessible via https://github.com/SHUD-System/SHUD.
