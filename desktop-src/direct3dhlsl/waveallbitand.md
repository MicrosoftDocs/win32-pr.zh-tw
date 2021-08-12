---
title: WaveActiveBitAnd 函式
description: 傳回目前 wave 中所有使用中通道的所有運算式值的位 AND，然後將它複製回所有使用中的通道。
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- WaveActiveBitAnd 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96d09d91df4ff9226a8fb86203be0bd79bc3c11d1882553607358c3c84d3814c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282996"
---
# <a name="waveactivebitand-function"></a>WaveActiveBitAnd 函式

傳回目前 wave 中所有使用中通道的所有運算式值的位 AND，然後將它複製回所有使用中的通道。

## <a name="syntax"></a>語法


``` syntax
<int_type> WaveActiveBitAnd(
   <int_type> expr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*expr* 
</dt> <dd>

要評估的運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

位 AND 值。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




