---
title: WaveActiveMax 函式
description: 傳回目前 wave 中所有使用中通道的運算式的最大值，並將其複寫回所有使用中的通道。
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- WaveActiveMax 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c85936ca28aabe0365fd912b4d764739b0ab15765241a243ad67143dacd0d7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484198"
---
# <a name="waveactivemax-function"></a>WaveActiveMax 函式

傳回目前 wave 中所有使用中通道的運算式的最大值，並將其複寫回所有使用中的通道。

## <a name="syntax"></a>語法

``` syntax
<type> WaveActiveMax(
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

最大值。

## <a name="remarks"></a>備註

作業的順序未定義。

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="examples"></a>範例

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




