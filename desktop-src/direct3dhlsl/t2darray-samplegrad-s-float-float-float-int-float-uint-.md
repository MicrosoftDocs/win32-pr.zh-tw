---
title: Texture2DArray 的 SampleGrad：： SampleGrad (S、float、float、float、int、float、uint) 函數
description: 瞭解此函式如何使用漸層來取樣材質，以影響範例位置的計算方式。 適用于 Texture2DArray。
ms.assetid: 71CC8747-8684-4ABD-8B7A-E02889048261
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
ms.openlocfilehash: 3d6c46deb14c3a2c3554052ecc3e6625b13b2848
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992422"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture2darray"></a>Texture2DArray 的 SampleGrad：： SampleGrad (S、float、float、float、int、float、uint) 函數

使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。 傳回操作的相關狀態。

## <a name="syntax"></a>語法


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
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

</dd> <dt>

*狀態* \[擴展\]
</dt> <dd>

類型： **uint**

作業的狀態。 您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。 如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。 如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[SampleGrad 方法](texture2darray-samplegrad.md)
</dt> <dt>

[**Texture2DArray**](sm5-object-texture2darray.md)
</dt> </dl>

 

 
