---
title: Texture2DArray：： GatherCmpRed (S、float、float、int) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。 |Texture2DArray：： GatherCmpRed (S、float、float、int) 函數
ms.assetid: aa7fadf8-fe96-406a-9c93-9ae0c59ef087
keywords:
- GatherCmpRed 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cf0f7094c7e535a84e6d8fd6ba7e87bb702dbfd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991979"
---
# <a name="texture2darraygathercmpredsfloatfloatint-function"></a>Texture2DArray：： GatherCmpRed (S、float、float、int) 函數

針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。

## <a name="syntax"></a>語法

``` syntax
float4 GatherCmpRed(
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

[GatherCmpRed 方法](texture2darray-gathercmpred.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




