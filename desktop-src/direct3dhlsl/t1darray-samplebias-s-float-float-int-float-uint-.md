---
title: Texture1DArray 的 SampleBias：： SampleBias (S、float、float、int、float、uint) 函數
description: 將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。 |Texture1DArray 的 SampleBias：： SampleBias (S、float、float、int、float、uint) 函數
ms.assetid: 6136674B-38F4-4081-82D6-0731604EB1A3
keywords:
- SampleBias 函式 HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c8c189b38abba3d127118fcb9cc6a5efa0ead651e4f81156057b7234ab418af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904645"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture1darray"></a>Texture1DArray 的 SampleBias：： SampleBias (S、float、float、int、float、uint) 函數

將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。 傳回操作的相關狀態。

## <a name="syntax"></a>語法


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
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

*偏差* \[在\]
</dt> <dd>

類型： **float**

偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。

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

[SampleBias 方法](texture1darray-samplebias.md)
</dt> </dl>

 

 
