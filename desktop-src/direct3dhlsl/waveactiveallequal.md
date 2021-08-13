---
title: WaveActiveAllEqual 函式
description: 如果目前 wave (中的每個使用中通道的運算式相同，則會傳回 true，因此) 之間保持一致。
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- WaveActiveAllEqual 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f62493a1bf08b85e95acad319bac2d022c30a53d43c28a87d0f5f603e78d300f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786108"
---
# <a name="waveactiveallequal-function"></a>WaveActiveAllEqual 函式

如果目前 wave (中的每個使用中通道的運算式相同，則會傳回 true，因此) 之間保持一致。

## <a name="syntax"></a>語法


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*expr* 
</dt> <dd>

要評估的運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果目前 wave 中的每個使用中通道的運算式相同，則為 True。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




