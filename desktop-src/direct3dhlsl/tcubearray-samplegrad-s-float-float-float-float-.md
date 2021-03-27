---
title: SampleGrad：： SampleGrad (S，float，float，float，float) function for TextureCubeArray
description: 瞭解此函式如何使用漸層來取樣材質，以影響範例位置的計算方式。 適用于 TextureCubeArray。
ms.assetid: 0C7DC9AA-3F0A-47E4-852F-7AE25CF67EA3
keywords:
- SampleGrad 函式 HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5320f47a5ae4db5bd96232dfa0a1d55b54f29c25
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103696879"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecubearray"></a>SampleGrad：： SampleGrad (S，float，float，float，float) function for TextureCubeArray

使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。

## <a name="syntax"></a>語法


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的 S\]
</dt> <dd>

類型： **SamplerState**

[取樣器狀態](dx-graphics-hlsl-sampler.md)。 這是在包含狀態指派的效果檔案中宣告的物件。

</dd> <dt>

*位置* \[在\]
</dt> <dd>

類型： **float**

材質座標。 引數類型相依于材質物件類型。



| Texture-Object 類型                    | 參數類型 |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray、Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

 \[ 中的 DDX\]
</dt> <dd>

類型： **float**

以 x 方向呈現的表面幾何變化率。 引數類型相依于材質物件類型。



| Texture-Object 類型                      | 參數類型 |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D、Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | 不支援  |



 

</dd> <dt>

*DDY* \[在\]
</dt> <dd>

類型： **float**

介面幾何在 y 方向的變化率。 引數類型相依于材質物件類型。



| Texture-Object 類型                      | 參數類型 |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D、Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | 不支援  |



 

</dd> <dt>

*夾具* \[在\]
</dt> <dd>

類型： **float**

用來將範例」 LOD 值設為的選擇性值。 例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[SampleGrad 方法](texturecubearray-samplegrad.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
