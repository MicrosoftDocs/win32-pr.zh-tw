---
title: '格式轉換函數 (HLSL 參考) '
description: 此區段包含計算和圖元著色器中所使用的格式轉換函數。
ms.assetid: 05575ee8-4428-437f-bfb6-e5c676405d65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1158a45ce2fc5df0bdc762a5d422492522886b8025c940e807c80707be173e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672918"
---
# <a name="format-conversion-functions-hlsl-reference"></a>格式轉換函數 (HLSL 參考) 

此區段包含計算和圖元著色器中所使用的格式轉換函數。

-   [轉換器函式](#converter-functions)
-   [相關主題](#related-topics)

> .Inl 標頭隨附于舊版 DirectX SDK，並依賴 XNAMath 來支援 c + + 支援。 D3DX_DXGIFormatConvert 它也包含在[DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中。 最新版本使用 DirectXMath 進行 c + + 支援，而所有函式都定義于 **DirectX** c + + 命名空間中。

## <a name="converter-functions"></a>轉換器函式

### <a name="dxgi_format_r10g10b10a2_unorm"></a>DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM

<dl>

[**\_ \_ \_ FLOAT4 的 D3DX R10G10B10A2 \_ UNORM**](d3dx-r10g10b10a2-unorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ 到 \_ R10G10B10A2 \_ UNORM**](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a>DXGI \_ 格式 \_ R10G10B10A2 \_ UINT

<dl>

[**D3DX \_ R10G10B10A2 \_ UINT \_ 至 \_ UINT4**](d3dx-r10g10b10a2-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ 到 \_ R10G10B10A2 \_ UINT**](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a>DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM：

<dl>

[**\_ \_ \_ FLOAT4 的 D3DX R8G8B8A8 \_ UNORM**](d3dx-r8g8b8a8-unorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM**](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a>DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB

<dl>

[**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4 不 \_ 精確**](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM \_ SRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a>DXGI \_ 格式 \_ R8G8B8A8 \_ UINT

<dl>

[**D3DX \_ R8G8B8A8 \_ UINT \_ 至 \_ UINT4**](d3dx-r8g8b8a8-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ 到 \_ R8G8B8A8 \_ UINT**](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a>DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM

<dl>

[**\_ \_ \_ FLOAT4 的 D3DX R8G8B8A8 \_ SNORM**](d3dx-r8g8b8a8-snorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ SNORM**](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a>DXGI \_ 格式 \_ R8G8B8A8 \_ 聖

<dl>

[**D3DX \_ R8G8B8A8 \_ 聖 \_ 至 \_ INT4**](d3dx-r8g8b8a8-sint-to-int4.md)  
[**D3DX \_ INT4 \_ 至 \_ R8G8B8A8 \_ 聖**](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a>DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM

<dl>

[**\_ \_ \_ FLOAT4 的 D3DX B8G8R8A8 \_ UNORM**](d3dx-b8g8r8a8-unorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ 到 \_ B8G8R8A8 \_ UNORM**](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a>DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB

<dl>

[**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4 不 \_ 精確**](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT4**](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM \_ SRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a>DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM

<dl>

[**\_ \_ \_ FLOAT3 的 D3DX B8G8R8X8 \_ UNORM**](d3dx-b8g8r8x8-unorm-to-float3.md)  
[**D3DX \_ FLOAT3 \_ 到 \_ B8G8R8X8 \_ UNORM**](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a>DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB

<dl>

[**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT3 不 \_ 精確**](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ 至 \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[**D3DX \_ FLOAT3 \_ 到 \_ B8G8R8X8 \_ UNORM \_ SRGB**](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a>DXGI \_ 格式 \_ R16G16 \_ FLOAT

<dl>

[**D3DX \_ R16G16 \_ FLOAT \_ 至 \_ FLOAT2**](d3dx-r16g16-float-to-float2.md)  
[**D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ FLOAT**](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a>DXGI \_ 格式 \_ R16G16 \_ UNORM

<dl>

[**\_ \_ \_ FLOAT2 的 D3DX R16G16 \_ UNORM**](d3dx-r16g16-unorm-to-float2.md)  
[**D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ UNORM**](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a>DXGI \_ 格式 \_ R16G16 \_ UINT

<dl>

[**D3DX \_ R16G16 \_ UINT \_ 至 \_ UINT2**](d3dx-r16g16-uint-to-uint2.md)  
[**D3DX \_ UINT2 \_ 到 \_ R16G16 \_ UINT**](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a>DXGI \_ 格式 \_ R16G16 \_ SNORM

<dl>

[**\_ \_ \_ FLOAT2 的 D3DX R16G16 \_ SNORM**](d3dx-r16g16-snorm-to-float2.md)  
[**D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ SNORM**](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a>DXGI \_ 格式 \_ R16G16 \_ 聖

<dl>

[**D3DX \_ R16G16 \_ 聖 \_ 至 \_ INT2**](d3dx-r16g16-sint-to-int2.md)  
[**D3DX \_ INT2 \_ 至 \_ R16G16 \_ 聖**](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[內嵌格式轉換參考](inline-format-conversion-reference.md)
</dt> <dt>

[\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
