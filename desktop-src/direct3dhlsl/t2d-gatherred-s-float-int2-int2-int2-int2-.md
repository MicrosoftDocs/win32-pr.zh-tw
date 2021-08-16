---
title: Texture2D：： GatherRed (S、float、int2、int2、int2、int2) 函數
description: 傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。 |Texture2D：： GatherRed (S、float、int2、int2、int2、int2) 函數
ms.assetid: 85C321CB-B77C-430B-921D-D56E5597B24A
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
ms.openlocfilehash: 7ccd6d9c42ebcd447d6ef266b199f5d706c439fd0aa83b33ac923ec8692be65f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043596"
---
# <a name="texture2dgatherredsfloatint2int2int2int2-function"></a>Texture2D：： GatherRed (S、float、int2、int2、int2、int2) 函數

傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。

## <a name="syntax"></a>語法


``` syntax
TemplateType GatherRed(
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



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[GatherRed 方法](texture2d-gatherred.md)
</dt> </dl>

 

 




