---
title: Texture2DArray：： GatherGreen (S，float，int) 函數
description: 傳回雙線性篩選作業中所使用之四個材質值的綠色元件。 |Texture2DArray：： GatherGreen (S，float，int) 函數
ms.assetid: bfe9ab9f-64f7-4a50-aa46-2ec6effebce2
keywords:
- GatherGreen 函式 HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fab908d7c8b0ed97a99aa04b8557e1008235cb91597ab00bdc90912e83e9627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724579"
---
# <a name="texture2darraygathergreensfloatint-function"></a>Texture2DArray：： GatherGreen (S，float，int) 函數

傳回雙線性篩選作業中所使用之四個材質值的綠色元件。

## <a name="syntax"></a>語法

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的 s\]
</dt> <dd>

類型：**取樣** 器

以零為基底的取樣器索引。

</dd> <dt>

*位置* \[在\]
</dt> <dd>

類型： **float3**

此範例會協調 (u，v) 。

</dd> <dt>

*位移* \[在\]
</dt> <dd>

類型： **int2**

取樣之前套用至材質座標的位移。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **TemplateType**

四個元件的值，其類型與範本類型相同。

## <a name="remarks"></a>備註

紋理範例可用於雙線性插補。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[GatherGreen 方法](texture2darray-gathergreen.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




