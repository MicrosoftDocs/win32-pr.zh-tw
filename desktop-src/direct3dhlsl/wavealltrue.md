---
title: WaveActiveAllTrue 函式
description: 如果目前 wave 的所有作用中通道中的運算式為 true，則傳回 true。
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- WaveActiveAllTrue 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f80c9af3bb9a1be47a3d64f31f0b3c3c610022d3a017a13053c0e4fc7db3a82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504868"
---
# <a name="waveactivealltrue-function"></a>WaveActiveAllTrue 函式

如果目前 wave 的所有作用中通道中的運算式為 true，則傳回 true。

## <a name="syntax"></a>語法

``` syntax
bool WaveActiveAllTrue(
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

如果運算式在所有泳道中為 true，則為 true。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




