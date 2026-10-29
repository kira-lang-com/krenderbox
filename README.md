# RenderBox

A Kira port of Apple's RenderBox, the GPU 2D renderer under SwiftUI and
IconRendering: a display list of shapes, fills, layers, clips and styles,
drawn on Ember.

The API is RenderBox's own. Types drop the `RB` prefix (`RBDisplayList` is
`DisplayList`), selectors keep their names and argument order, and codes such
as blend modes and layer flags keep RenderBox's values, read from its
`RB::XML` writer and its `_RBDrawingState` functions.

- `app/Types`: blend modes, clip modes, colour spaces, layer flags.
- `app/Shape`: `Shape`, the analytic primitives (`RB::Coverage::Primitive`)
  and paths.
- `app/Fill`: `Fill`: colours, gradients, images and shaders.
- `app/Shader`: `Shader` and `ShaderLibrary`, RenderBox's stitchable functions.
- `app/DisplayList`: `DisplayList`, its state stack, layers and items.

Tests: `kira test tests/renderbox_kik`.
