---
title: WaveActiveBitOr 函式
description: 傳回目前 wave 中所有使用中通道的所有運算式值位 OR，然後將其複寫回所有使用中的通道。
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- WaveActiveBitOr 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7efe678093fca38940e0a98a31d4c39065bcf172d04aa5eb0932467fc716457b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504888"
---
# <a name="waveactivebitor-function"></a>WaveActiveBitOr 函式

傳回目前 wave 中所有使用中通道的所有運算式值位 OR，然後將其複寫回所有使用中的通道。

## <a name="syntax"></a>語法

``` syntax
<int_type> WaveActiveBitOr(
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

位 OR 值。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




