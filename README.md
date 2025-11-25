# FastDnnBenchmarks

Compare DNN inference speed in Python, C#, and C++

## Overview
A straight-up repo for checking how fast different languages run DNN using OpenCV’s module. SSD models used for the test. No fancy wrappers, just runtime benchmarks and code for exact numbers.

## Tested setups

- **Python**
  - Python 3.6.3
  - OpenCV 3.3.0.10 (`opencv-python`)

- **C#**
  - .NET Framework 4.7
  - EmguCV 3.3.0.2824
  - OpenCvSharp 3.3.1.20171117

- **C++**
  - VC14
  - OpenCV 3.3.1

### System Specs
- Windows 10 Pro 64bit
- Intel Core i7-7820HQ @ 2.90GHz
- GPU not used—OpenCV DNN had no GPU support for these tests

### Model
- SSD / PASCAL VOC — based on VOC 07++12+COCO
- SSD512, downloaded from original source

## Results

| Language           | DNN Runtime (ms) |
|--------------------|-----------------|
| Python + OpenCV    | 1510            |
| C# + OpenCvSharp   | 1917            |
| C# + EmguCV        | 4041            |
| C++ + OpenCV       | 9306            |

## How to run
- Find code samples for each setup:
  - Python: `OpenCvSSD.py`
  - C++: `OpenCvSsdCplus.cpp`
  - C# (EmguCV): `emguCvSsd.cs`
  - C# (OpenCvSharp): `OpenCvSharpDnn/`

## Extra info
For a technical breakdown, hardware/OS setups, or more performance details, see the blog post: “OpenCV DNN speed compare in Python, C#, C++.”
Contributions and alternate configs welcome, send a PR or open an issue if you’ve got suggestions or new benchmark results.
