---
title: WaveActiveAnyTrue 函式
description: 如果目前 wave 的任何使用中通道中的運算式為 true，則傳回 true。
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- WaveActiveAnyTrue 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c49c9727461d316d7d2c9d8f048971384e568476d1ca693aeec49cdf14a4795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721728"
---
# <a name="waveactiveanytrue-function"></a>WaveActiveAnyTrue 函式

如果目前 wave 的任何使用中通道中的運算式為 true，則傳回 true。

## <a name="syntax"></a>語法

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*expr* 
</dt> <dd>

要評估的布林運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果任何通道中的運算式為 true，則為 true。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




