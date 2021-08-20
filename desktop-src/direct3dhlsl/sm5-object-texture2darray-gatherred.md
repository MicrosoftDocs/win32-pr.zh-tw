---
title: Texture2DArray：： GatherRed (S，float，int) 函數
description: 傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。 |Texture2DArray：： GatherRed (S，float，int) 函數
ms.assetid: cb9c21ef-87f4-4c32-b41a-9fc7478713a6
keywords:
- GatherRed 函式 HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c5bd278605217b723035e53091d22b8b6f69dd0457b6cf5c12f2ad895699d1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905255"
---
# <a name="texture2darraygatherredsfloatint-function"></a>Texture2DArray：： GatherRed (S，float，int) 函數

傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。

## <a name="syntax"></a>語法

``` syntax
TemplateType GatherRed(
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

[GatherRed 方法](texture2darray-gatherred.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




