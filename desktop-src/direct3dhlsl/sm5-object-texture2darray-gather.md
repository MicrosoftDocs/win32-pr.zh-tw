---
title: Texture2DArray：：搜集 (S、float、int) 函數
description: 傳回要在雙線性篩選作業中使用的四個材質值。 |Texture2DArray：：搜集 (S、float、int) 函數
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- 收集函數 HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f684efa4cb597a640b78a2cdd08074d47fec3b4ec2f8a4a6fe6bcf993fd53ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367798"
---
# <a name="texture2darraygathersfloatint-function"></a>Texture2DArray：：搜集 (S、float、int) 函數

傳回要在雙線性篩選作業中使用的四個材質值。

## <a name="syntax"></a>語法

``` syntax
TemplateType Gather(
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

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[收集方法](texture2darray-gather.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




