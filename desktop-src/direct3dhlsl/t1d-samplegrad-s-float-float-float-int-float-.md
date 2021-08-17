---
title: Texture1D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float) 函數
description: 此函式會取樣材質、使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料層級 (」 LOD) 值為。
ms.assetid: 34A79CB6-0C45-40ED-845C-77C08F1DEC57
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
ms.openlocfilehash: 3c9f750f386ffb4fd3c13af717b173f752b7f515003cf16f9d2df4b37385dda9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724272"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1d"></a>Texture1D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float) 函數

使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。

## <a name="syntax"></a>語法


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
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

*位移* \[在\]
</dt> <dd>

類型： **int**

選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。 只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。 引數類型相依于材質物件類型。 如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。



| Texture-Object 類型           | 參數類型 |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D、Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | 不支援  |



 

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

[SampleGrad 方法](texture1d-samplegrad.md)
</dt> </dl>

 

 
