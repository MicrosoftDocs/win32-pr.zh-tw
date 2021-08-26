---
title: Texture1D 的 SampleLevel：： SampleLevel (S、float、float、int、uint) 函數
description: 針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。 適用于 Texture1D。 |SampleLevel：： SampleLevel (S、float、float、int、uint) 函數
ms.assetid: B797C7F9-7436-4DD5-9CAB-EFF81D410174
keywords:
- SampleLevel 函式 HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15be5bc4c7e6607c53a051f9a750a72d16d9fdce09b4ec9c8d3d0be497a811d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023378"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture1d"></a>Texture1D 的 SampleLevel：： SampleLevel (S、float、float、int、uint) 函數

針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。

## <a name="syntax"></a>語法


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
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

*」 Lod* \[在\]
</dt> <dd>

類型： **float**

\[在 \] 指定 mipmap 層級的數位中。 如果值為≤0，則會使用 mipmap 層級 0 (最大的對應) 。 小數值 (如果提供的) 用來在兩個 mipmap 層級之間插補。

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

[SampleLevel 方法](texture1d-samplelevel.md)
</dt> </dl>

 

 
