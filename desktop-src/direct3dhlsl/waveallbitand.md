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
ms.openlocfilehash: 2b6a3b0b097ea8737e07a91fcfc6553f22b828f1
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024333"
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

 

 




