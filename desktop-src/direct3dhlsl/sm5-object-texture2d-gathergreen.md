---
title: Texture2D：： GatherGreen (S，float，int) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。 |Texture2D：： GatherGreen (S，float，int) 函數
ms.assetid: 97e1fb52-75f4-4e73-93f1-98b7a5925efc
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
ms.openlocfilehash: 722d7a3ac90fa3083b8f42f7704f5c9e0aeb1829
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992002"
---
# <a name="texture2dgathergreensfloatint-function"></a>Texture2D：： GatherGreen (S，float，int) 函數

針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。

## <a name="syntax"></a>語法

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float2 location,
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

類型： **float2**

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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[GatherGreen 方法](texture2d-gathergreen.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




