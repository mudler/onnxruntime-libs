# onnxruntime-libs

Prebuilt ONNX Runtime 1.28.2 release archives used by the LocalAI backends
(silero-vad, sherpa-onnx, supertonic).

## Why this repository exists

The upstream `microsoft/onnxruntime` GitHub repository is unavailable (its
release URLs return 404). LocalAI needs prebuilt runtimes at build time, so
this repository hosts a copy of them under a stable URL.

## Provenance

The files are byte-identical copies of the release assets published at
<https://github.com/csukuangfj/onnxruntime-libs/releases/tag/v1.28.2>.
That third-party mirror is also what `k2-fsa/sherpa-onnx` downloads. The file
names are the same as in the mirror, so only the base URL changes:

    https://github.com/mudler/onnxruntime-libs/releases/download/v1.28.2/<file>

The files are not modified here. The `-patched` CUDA archives are the mirror's
own patched builds. Each SHA256 below equals the digest GitHub shows for the
mirror asset. For the CPU and macOS archives, and for the CUDA 12 archive, it
also equals the hash pinned in the `k2-fsa/sherpa-onnx` cmake files.

## Assets (release v1.28.2)

| File | Size (bytes) | SHA256 |
|---|---|---|
| onnxruntime-linux-aarch64-glibc2_17-Release-1.28.2.zip | 11658719 | 28083273643f40fa6477ef9d53986fe216304710c4b1c743b217a4effd016339 |
| onnxruntime-linux-x64-glibc2_17-Release-1.28.2.zip | 8781463 | c4f8994d56191d9d2c92a961b39fe790459f2c5d155f912b239506ea31359534 |
| onnxruntime-linux-x64-gpu_cuda12-1.28.2-patched.zip | 423749731 | 3417d0d4bf608e2532928eb1e8d6c9383b28ba449f0d02f0493e21501ab0bc74 |
| onnxruntime-linux-x64-gpu_cuda13-1.28.2-patched.zip | 240884030 | da0c23641091fdeef7d7f78551008e188741051e936ed0495011202f0268ab8b |
| onnxruntime-osx-arm64-1.28.2.zip | 8041795 | d9e5c0c79929e201f5b8eb095e6809a91ce78be9866a1bca0dfab7e20b40ae40 |
| onnxruntime-osx-x86_64-1.28.2.zip | 9207322 | cef42f2a4fca3b23dd16914ead36229adc7d5c119d563aaa12cc5d1e9177f93d |

`SHA256SUMS` lists the same hashes. Check a download with
`sha256sum -c SHA256SUMS --ignore-missing`.

## License

ONNX Runtime is copyright Microsoft Corporation and is licensed under the MIT
License. Every archive contains the license text and third-party notices. The
license text is also in the `LICENSE` file of this repository:

    MIT License
    
    Copyright (c) Microsoft Corporation
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
