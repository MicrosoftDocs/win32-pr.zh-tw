---
title: Texture2DArray：： GatherCmpAlpha (S、float、float、int) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較。 |Texture2DArray：： GatherCmpAlpha (S、float、float、int) 函數
ms.assetid: d5fc78eb-2378-4e63-a712-c6f4ef9fc729
keywords:
- GatherCmpAlpha 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42f11131ebf377ddc64be5309c3edf77214ddd4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322480"
---
# <a name="texture2darraygathercmpalphasfloatfloatint-function"></a>Texture2DArray：： GatherCmpAlpha (S、float、float、int) 函數

針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較。

## <a name="syntax"></a>語法

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **SamplerComparisonState**

以零為基底的取樣器索引。

</dd> <dt>

*位置* \[在\]
</dt> <dd>

類型： **float3**

此範例會協調 (u，v) 。

</dd> <dt>

*比較 \_ 值* \[\]
</dt> <dd>

類型： **float**

要針對每個取樣值進行比較的值。

</dd> <dt>

*位移* \[在\]
</dt> <dd>

類型： **int2**

取樣之前套用至材質座標的位移。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **float4**

四個元件的值，每個元件都是每個元件的比較結果。

## <a name="remarks"></a>備註

紋理範例可用於雙線性插補。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[GatherCmpAlpha 方法](texture2darray-gathercmpalpha.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




