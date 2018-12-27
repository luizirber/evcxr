# Evcxr image

Integration between [Evcxr
Jupyter](https://github.com/google/evcxr/blob/master/evcxr_jupyter/README.md)
and the image crate. Enables display of images in Evcxr Jupyter kernel.

Currently only supports:
* RgbImage
* GrayImage

Example usage:
```rust
extern crate evcxr_image;
extern crate image;

use evcxr_image::ImageDisplay;

image::ImageBuffer::from_fn(256, 256, |x, y| {
    if (x as i32 - y as i32).abs() < 3 {
        image::Rgb([0, 0, 255])
    } else {
        image::Rgb([0, 0, 0])
    }
})
```