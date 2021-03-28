---
title: TextureCube 的 SampleLevel：： SampleLevel (S、float、float、uint) 函數
description: 針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。 |SampleLevel：： SampleLevel (S，float，float，uint) 函數
ms.assetid: DB27D8B9-11AB-4F0C-947A-9469BA565F41
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
ms.openlocfilehash: a31eaa2351b4758c29327aaa08ccee5ed0c3056c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104386539"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function-for-texturecube"></a>TextureCube 的 SampleLevel：： SampleLevel (S、float、float、uint) 函數

針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。

## <a name="syntax"></a>語法


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
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

[SampleLevel 方法](texturecube-samplelevel.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
