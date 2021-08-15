---
title: WaveActiveProduct 函式
description: 將運算式的值與目前 wave 中所有使用中的車道相乘，並將其複寫回所有使用中的通道。
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- WaveActiveProduct 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95bef050d335ba261e08852a7d4b9a1acbcda271b91778b7241d5de9f4a6d9ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119369398"
---
# <a name="waveactiveproduct-function"></a>WaveActiveProduct 函式

將運算式的值與目前 wave 中所有使用中的車道相乘，並將其複寫回所有使用中的通道。

## <a name="syntax"></a>語法

``` syntax
<type> WaveActiveProduct(
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

產品值。

## <a name="remarks"></a>備註

作業的順序未定義。

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




