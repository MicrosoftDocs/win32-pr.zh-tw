---
title: EvaluateAttributeAtSample 函式
description: 在索引範例位置評估。
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- EvaluateAttributeAtSample 函式 HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29191a3790afee2d37fee3d2ee8fb58673ff487af178bd8b1e2b33f26f1ec44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982478"
---
# <a name="evaluateattributeatsample-function"></a>EvaluateAttributeAtSample 函式

在索引範例位置評估。

## <a name="syntax"></a>語法

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **attrib 數值**

輸入值。

</dd> <dt>

*sampleindex* \[在\]
</dt> <dd>

類型： **uint**

範例位置。

</dd> </dl>

## <a name="remarks"></a>備註

插補模式可以是 **線性** 或線性，而不是在變數上的 **\_ \_ 觀點** 。 會忽略 **距心** 或 **sample** 的使用。 也允許具有常數插補的屬性，在此情況下，會忽略範例索引。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




