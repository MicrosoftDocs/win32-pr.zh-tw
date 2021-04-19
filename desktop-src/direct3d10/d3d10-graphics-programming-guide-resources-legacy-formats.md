---
description: 下表列出可對應至 Direct3D 10 格式的 Direct3D 9 格式。
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 舊版格式：將 Direct3D 9 格式對應至 Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230b8ed17984d47a3b57ce287aa9b434a2b92aae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973773"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>舊版格式：將 Direct3D 9 格式對應至 Direct3D 10

下表列出可對應至 Direct3D 10 格式的 Direct3D 9 格式。 Direct3D 10 格式的分歧來自 Direct3D 9 格式，因此可以合併頂點和材質格式，以啟用跨序的應用程式。



| Direct3D 9 材質/頂點/索引格式 | 相等的 Direct3D 10 格式                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ 不明                        | DXGI \_ 格式 \_ 未知                                                |
| D3DFMT \_ R8G8B8                         | 無法使用                                                        |
| D3DFMT \_ A8R8G8B8                       | DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM (DXGI 1.1)                              |
| D3DFMT \_ X8R8G8B8                       | DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM (DXGI 1.1)                              |
| D3DFMT \_ R5G6B5                         | DXGI \_ 格式 \_ B5G6R5 \_ UNORM (DXGI 1.2)                                |
| D3DFMT \_ X1R5G5B5                       | 無法使用                                                        |
| D3DFMT \_ A1R5G5B5                       | DXGI \_ 格式 \_ B5G5R5A1 \_ UNORM (DXGI 1.2)                              |
| D3DFMT \_ A4R4G4B4                       | DXGI \_ 格式 \_ B4G4R4A4 \_ UNORM (DXGI 1.2)                              |
| D3DFMT \_ R3G3B2                         | 無法使用                                                        |
| D3DFMT \_ A8                             | DXGI \_ 格式 \_ A8 \_ UNORM                                              |
| D3DFMT \_ A8R3G3B2                       | 無法使用                                                        |
| D3DFMT \_ X4R4G4B4                       | 無法使用                                                        |
| D3DFMT \_ A2B10G10R10                    | DXGI \_ 格式 \_ R10G10B10A2                                            |
| D3DFMT \_ A8B8G8R8                       | DXGI \_ format \_ R8G8B8A8 \_ UNORM 或 dxgi \_ format \_ R8G8B8A8 \_ UNORM \_ SRGB |
| D3DFMT \_ X8B8G8R8                       | 無法使用                                                        |
| D3DFMT \_ G16R16                         | DXGI \_ 格式 \_ R16G16 \_ UNORM                                          |
| D3DFMT \_ A2R10G10B10                    | 無法使用                                                        |
| D3DFMT \_ A16B16G16R16                   | DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM                                    |
| D3DFMT \_ A8P8                           | 無法使用                                                        |
| D3DFMT \_ P8                             | 無法使用                                                        |
| D3DFMT 的 \_ L8                             | DXGI \_ 格式 \_ R8 \_ UNORM ¹                                            |
| D3DFMT \_ A8L8                           | 無法使用                                                        |
| D3DFMT \_ A4L4                           | 無法使用                                                        |
| D3DFMT \_ V8U8                           | DXGI \_ 格式 \_ R8G8 \_ SNORM                                            |
| D3DFMT \_ L6V5U5                         | 無法使用                                                        |
| D3DFMT \_ X8L8V8U8                       | 無法使用                                                        |
| D3DFMT \_ Q8W8V8U8                       | DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM                                        |
| D3DFMT \_ V16U16                         | DXGI \_ 格式 \_ R16G16 \_ SNORM                                          |
| D3DFMT \_ W11V11U10                      | 無法使用                                                        |
| D3DFMT \_ A2W10V10U10                    | 無法使用                                                        |
| D3DFMT \_ UYVY                           | 無法使用                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | DXGI \_ 格式 \_ G8R8 \_ G8B8 \_ UNORM ²                                    |
| D3DFMT \_ YUY2                           | 無法使用                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | DXGI \_ 格式 \_ R8G8 \_ B8G8 \_ UNORM ²                                    |
| D3DFMT \_ DXT1                           | DXGI \_ format \_ BC1 \_ UNORM 或 dxgi \_ format \_ BC1 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT2                           | DXGI \_ format \_ BC2 \_ UNORM 或 DXGI \_ format \_ BC2 \_ UNORM \_ SRGB ³         |
| D3DFMT \_ DXT3                           | DXGI \_ format \_ BC2 \_ UNORM 或 dxgi \_ format \_ BC2 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT4                           | DXGI \_ format \_ BC3 \_ UNORM 或 DXGI \_ format \_ BC3 \_ UNORM \_ SRGB ³         |
| D3DFMT \_ DXT5                           | DXGI \_ format \_ BC3 \_ UNORM 或 dxgi \_ format \_ BC3 \_ UNORM \_ SRGB           |
| D3DFMT \_ D16 和 D3DFMT \_ D16 的 \_ 鎖定  | DXGI \_ 格式 \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32                            | 無法使用                                                        |
| D3DFMT \_ D15S1                          | 無法使用                                                        |
| D3DFMT \_ D24S8                          | 無法使用                                                        |
| D3DFMT \_ D24X8                          | 無法使用                                                        |
| D3DFMT \_ D24X4S4                        | 無法使用                                                        |
| D3DFMT \_ D16                            | DXGI \_ 格式 \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F 的 \_ 鎖定                 | DXGI \_ 格式 \_ D32 \_ FLOAT                                             |
| D3DFMT \_ D24FS8                         | 無法使用                                                        |
| D3DFMT \_ S1D15                          | 無法使用                                                        |
| D3DFMT \_ S8D24                          | DXGI \_ 格式 \_ D24 \_ UNORM \_ S8 \_ UINT                                   |
| D3DFMT \_ X8D24                          | 無法使用                                                        |
| D3DFMT \_ X4S4D24                        | 無法使用                                                        |
| D3DFMT \_ l16 也                            | DXGI \_ 格式 \_ R16 \_ UNORM ¹                                           |
| D3DFMT \_ INDEX16                        | DXGI \_ 格式 \_ R16 \_ UINT                                              |
| D3DFMT \_ INDEX32                        | DXGI \_ 格式 \_ R32 \_ UINT                                              |
| D3DFMT \_ Q16W16V16U16                   | DXGI \_ 格式 \_ R16G16B16A16 \_ SNORM                                    |
| D3DFMT \_ MULTI2 \_ ARGB8                  | 無法使用                                                        |
| D3DFMT \_ R16F                           | DXGI \_ 格式 \_ R16 \_ FLOAT                                             |
| D3DFMT \_ G16R16F                        | DXGI \_ 格式 \_ R16G16 \_ FLOAT                                          |
| D3DFMT \_ A16B16G16R16F                  | DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT                                    |
| D3DFMT \_ R32F                           | DXGI \_ 格式 \_ R32 \_ FLOAT                                             |
| D3DFMT \_ G32R32F                        | DXGI \_ 格式 \_ R32G32 \_ FLOAT                                          |
| D3DFMT \_ A32B32G32R32F                  | DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT                                    |
| D3DFMT \_ CxV8U8                         | 無法使用                                                        |
| D3DDECLTYPE \_ FLOAT1                    | DXGI \_ 格式 \_ R32 \_ FLOAT                                             |
| D3DDECLTYPE \_ FLOAT2                    | DXGI \_ 格式 \_ R32G32 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT3                    | DXGI \_ 格式 \_ R32G32B32 \_ FLOAT                                       |
| D3DDECLTYPE \_ FLOAT4                    | DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT                                    |
| D3DDECLTYPED3DCOLOR                    | 無法使用                                                        |
| D3DDECLTYPE \_ UBYTE4                    | DXGI \_ 格式 \_ R8G8B8A8 \_ UINT ⁴                                       |
| D3DDECLTYPE \_ SHORT2                    | DXGI \_ 格式 \_ R16G16 \_ 聖                                           |
| D3DDECLTYPE \_ SHORT4                    | DXGI \_ 格式 \_ R16G16B16A16 \_ 聖                                     |
| D3DDECLTYPE \_ UBYTE4N                   | DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM                                        |
| D3DDECLTYPE \_ SHORT2N                   | DXGI \_ 格式 \_ R16G16 \_ SNORM                                          |
| D3DDECLTYPE \_ SHORT4N                   | DXGI \_ 格式 \_ R16G16B16A16 \_ SNORM                                    |
| D3DDECLTYPE \_ USHORT2N                  | DXGI \_ 格式 \_ R16G16 \_ UNORM                                          |
| D3DDECLTYPE \_ USHORT4N                  | DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM                                    |
| D3DDECLTYPE \_ UDEC3                     | 無法使用                                                        |
| D3DDECLTYPE \_ DEC3N                     | 無法使用                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | DXGI \_ 格式 \_ R16G16 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT                                    |



 

1.  在著色器中使用 r swizzle，以將紅色複製到其他元件，以取得 Direct3D 9 行為。
2.  在 Direct3D 9 中，資料是由 255.0 f （可改為著色器程式碼）進行擴充。
3.  DXT2 和 DXT3 與 API 的觀點相同;DXT4 和 DXT5 與 API 的觀點相同。 唯一的差異在於預乘 Alpha，可由應用程式追蹤，而且不需要個別的格式。
4.  著色器會取得 UINT 值，但如果 Direct3D 9 樣式整數浮點數 (0.0 f、1.0 f .。。需要有255個) ，UINT 可以轉換成著色器中的 float32。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



