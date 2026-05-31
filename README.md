# AI Image Detector

A free, private, browser-based tool that analyzes images and estimates the probability they were AI-generated — with per-signal reasoning.

**No account required. No data uploaded. No cost. Ever.**

---

## How it works

When you upload an image, the tool reads the raw pixel data directly in your browser using the Canvas API. It runs six heuristic signal analyses on that data and returns a weighted probability score with explanations.

No image is ever sent to a server. Everything runs on your device.

## The six signals

| Signal | What it detects |
|---|---|
| Noise uniformity | AI models synthesize texture procedurally, creating unnaturally uniform noise patterns |
| Color gradient smoothness | Diffusion models interpolate color too cleanly compared to real optical lenses |
| High-frequency detail bias | AI struggles with fine repetitive texture — hair, fabric, foliage |
| Edge coherence | AI edges are mathematically too clean; real lenses produce natural blur and falloff |
| Saturation clustering | AI tends to hyper-saturate dominant hues while compressing mid-tone variation |
| Output dimension pattern | Most AI generators output at fixed sizes (512, 768, 1024, 1536px) — cameras don't |

## Accuracy disclaimer

This tool uses pixel-level heuristics, not a trained neural network. It will catch obvious cases and miss sophisticated ones. Heavily edited real photos may score high. Treat the result as a first filter, not a verdict.

For production-grade accuracy a trained model is required — which means API costs. This tool is intentionally free and private, which comes with that tradeoff.

## Usage

1. Open `index.html` in any modern browser
2. Drop or upload an image (JPEG, PNG, WebP)
3. Read the signal breakdown and probability score

Or use the live version at: https://phychef.github.io/ai-image-detector

## License

Copyright (C) 2025 Roberto Cimmino

This project is licensed under the GNU General Public License v3.0.
See the [LICENSE](LICENSE) file for details.

Any use, modification, or distribution of this code must remain open source under the same license and must retain the original copyright notice.

## Author

Built by Roberto Cimmino — github.com/phychef
