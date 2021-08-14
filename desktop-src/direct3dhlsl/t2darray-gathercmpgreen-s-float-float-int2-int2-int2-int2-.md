---
title: Texture2DArray：： GatherCmpGreen (S、float、float、int2、int2、int2、int2) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。 |Texture2DArray：： GatherCmpGreen (S、float、float、int2、int2、int2、int2) 函數
ms.assetid: 5A4B8AEB-B278-4456-893A-CAE61BFD6CA5
keywords:
- GatherCmpGreen 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e45997d3238038d3260594b5e568ca628f170af73dbabf7e382dddb2587dbb4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507361"
---
# <a name="texture2darraygathercmpgreensfloatfloatint2int2int2int2-function"></a>Texture2DArray：： GatherCmpGreen (S、float、float、int2、int2、int2、int2) 函數

針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。

## <a name="syntax"></a>語法


``` syntax
TemplateType GatherCmpGreen(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的 S\]
</dt> <dd>

類型： **SamplerState**

以零為基底的取樣器索引。

</dd> <dt>

*位置* \[在\]
</dt> <dd>

類型： **float**

此範例會協調 (u，v) 。

</dd> <dt>

*CompareValue* \[在\]
</dt> <dd>

類型： **float**

要針對每個取樣值進行比較的值。

</dd> <dt>

*Offset1* \[在\]
</dt> <dd>

類型： **int2**

第一個位移元件會在取樣之前套用至材質座標。

</dd> <dt>

*Offset2* \[在\]
</dt> <dd>

類型： **int2**

第二個位移元件會在取樣之前套用至材質座標。

</dd> <dt>

*Offset3* \[在\]
</dt> <dd>

類型： **int2**

第三個位移元件會在取樣之前套用至材質座標。

</dd> <dt>

*Offset4* \[在\]
</dt> <dd>

類型： **int2**

第四個位移元件會在取樣之前套用至材質座標。

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

[GatherCmpGreen 方法](texture2darray-gathercmpgreen.md)
</dt> </dl>

 

 




