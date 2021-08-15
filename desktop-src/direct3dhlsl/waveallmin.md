---
title: WaveActiveMin 函式
description: 傳回在目前 wave 的所有作用中通道上，運算式的最小值，將它複製回所有使用中的通道。
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- WaveActiveMin 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b97f2e58449e8b33270318f305a6fee87662a6aac4643b35152024366bf8b08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721785"
---
# <a name="waveactivemin-function"></a>WaveActiveMin 函式

傳回在目前 wave 的所有作用中通道上，運算式的最小值，將它複製回所有使用中的通道。

## <a name="syntax"></a>語法

``` syntax
<type> WaveActiveMin(
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

最小值。

## <a name="remarks"></a>備註

作業的順序未定義。

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="examples"></a>範例

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




