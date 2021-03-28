---
title: Texture2DArray：： GatherBlue (S，float，int) 函數
description: 傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。 |Texture2DArray：： GatherBlue (S，float，int) 函數
ms.assetid: f81596b5-afd1-4baf-b6c0-ca4661a3ef22
keywords:
- GatherBlue 函式 HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1844b898deca767b04aba438f4784a54a5afa112
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991927"
---
# <a name="texture2darraygatherbluesfloatint-function"></a>Texture2DArray：： GatherBlue (S，float，int) 函數

傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。

## <a name="syntax"></a>語法

``` syntax
TemplateType GatherBlue(
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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[GatherBlue 方法](texture2darray-gatherblue.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




