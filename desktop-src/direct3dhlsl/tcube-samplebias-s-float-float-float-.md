---
title: SampleBias：： SampleBias (S，float，float，float) function for TextureCube
description: 將偏差值套用至 mipmap 層級之後，TextureCube 範例的 SampleBias：： SampleBias (S、float、float、float) 函數會進行紋理取樣。
ms.assetid: BCDDADD9-D8B0-47C9-A312-5E6AF9C3C07B
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
ms.openlocfilehash: 55404f2e32f45e5b19e7b0cd4c109a6d5a8bcc13
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106993702"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecube"></a>SampleBias：： SampleBias (S，float，float，float) function for TextureCube

將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。

## <a name="syntax"></a>語法


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
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

*偏差* \[在\]
</dt> <dd>

類型： **float**

偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。

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

[SampleBias 方法](texturecube-samplebias.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
