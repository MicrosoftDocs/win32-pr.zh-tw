---
title: Texture2DArray：： GatherAlpha (S、float、int2、int2、int2、int2) 函數
description: 傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。 |Texture2DArray：： GatherAlpha (S、float、int2、int2、int2、int2) 函數
ms.assetid: A7F96B45-A097-437B-A0D0-18555FF76544
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
ms.openlocfilehash: ff6910152c9ac133c819456b9ec7aaeb2406b791
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945828"
---
# <a name="texture2darraygatheralphasfloatint2int2int2int2-function"></a>Texture2DArray：： GatherAlpha (S、float、int2、int2、int2、int2) 函數

傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。

## <a name="syntax"></a>語法


``` syntax
TemplateType GatherAlpha(
  in SamplerState S,
  in float        Location,
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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[GatherAlpha 方法](texture2darray-gatheralpha.md)
</dt> </dl>

 

 




