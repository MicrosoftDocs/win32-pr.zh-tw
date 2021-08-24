---
title: EvaluateAttributeAtCentroid 函式
description: 在圖元距心進行評估。
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- EvaluateAttributeAtCentroid 函式 HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 867f7dadc2ccf7d86eed602dd9e65d07be7558f0a8a00426e3a45bc1c2c97a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744038"
---
# <a name="evaluateattributeatcentroid-function"></a>EvaluateAttributeAtCentroid 函式

在圖元距心進行評估。

## <a name="syntax"></a>語法

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **attrib 數值**

輸入值。

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

 

 




