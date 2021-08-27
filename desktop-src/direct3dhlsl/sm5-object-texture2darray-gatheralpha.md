---
title: Texture2DArray：： GatherAlpha (S，float，int) 函數
description: 傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。 |Texture2DArray：： GatherAlpha (S，float，int) 函數
ms.assetid: d7270277-53c1-4034-bf66-9a95bc1b51e4
keywords:
- GatherAlpha 函式 HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e79805ff931c6fe2da880c3ae090b72b87713b1c0547e6bafcf5986f07b810f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118218"
---
# <a name="texture2darraygatheralphasfloatint-function"></a>Texture2DArray：： GatherAlpha (S，float，int) 函數

傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。

## <a name="syntax"></a>語法

``` syntax
TemplateType GatherAlpha(
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

[GatherAlpha 方法](texture2darray-gatheralpha.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




