+++
# Slider widget.
widget = "slider"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 20  # Order that this section will appear.

# Slide interval.
# Use `false` to disable animation or enter a time in ms, e.g. `5000` (5s).
interval = 5000

# Slide height (optional).
# E.g. `500px` for 500 pixels or `calc(100vh - 70px)` for full screen.
height = "320px"

# Slides.
# Duplicate an `[[item]]` block to add more slides.
[[item]]
  title = "SHUD模型源码"
  content = "SHUD的源代码由C++写成，已经共享在github，并且随时更新。另有若干案例数据供参考。"
  align = "center"  # Choose `center`, `left`, or `right`.

  # Overlay a color or image (optional).
  #   Deactivate an option by commenting out the line, prefixing it with `#`.
   overlay_color = "#666"  # An HTML color value.
   overlay_img = "github.png"  # Image path relative to your `static/media/` folder.
   overlay_filter = 0.80  # Darken the image. Value in range 0-1.

  # Call to action button (optional).
  #   Activate the button by specifying a URL and button label below.
  #   Deactivate by commenting out parameters, prefixing lines with `#`.
  cta_label = "源代码"
  cta_url = "https://github.com/SHUD-System/SHUD"
  cta_icon_pack = "fab"
  cta_icon = "github"
[[item]]
  title = "博士后招聘"
  content = "招聘2名全职博士后， 水文、气象、地理和计算机，或相关方向。基础年薪16-20万元，另有其他福利待遇。"
  align = "left"

  overlay_color = "#6594C1"  # An HTML color value.
  overlay_img = ""  # Image path relative to your `static/media/` folder.
  overlay_filter = 0.5  # Darken the image. Value in range 0-1.

  cta_label = "详情"
  cta_url = "/opp"
  cta_icon_pack = "fas"
  cta_icon = "link"
[[item]]
  title = "联培/客座研究生招聘"
  content = "招聘2-4名全日制研究生，以联合培养或客座形式加入本研究团队。"
  align = "left"

  overlay_color = "#2980B9"  # An HTML color value.
  overlay_img = ""  # Image path relative to your `static/media/` folder.
  overlay_filter = 0.5  # Darken the image. Value in range 0-1.

  cta_label = "详情"
  cta_url = "/opp"
  cta_icon_pack = "fas"
  cta_icon = "fa-link"
+++
