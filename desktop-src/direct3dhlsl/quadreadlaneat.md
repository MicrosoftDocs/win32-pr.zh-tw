---
title: QuadReadLaneAt 函式
description: 從目前四內的通道識別碼所識別的通道傳回指定的來源值。
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- QuadReadLaneAt 函式 HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463925"
---
# <a name="quadreadlaneat-function"></a>QuadReadLaneAt 函式

從目前四內的通道識別碼所識別的通道傳回指定的來源值。

## <a name="syntax"></a>語法


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sourceValue* 
</dt> <dd>

要求的類型。

</dd> <dt>

*quadLaneID* 
</dt> <dd>

通道識別碼;這會是從0到3的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

指定的來源值。 此函式的結果在四個之間是一致的。 如果來源通道為非使用中，則結果為未定義。

## <a name="remarks"></a>備註

如需四邊形的詳細資訊，請參閱 [著色器模型6的總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)。

只有在圖元和計算著色器中才支援來自著色器模型6.0 的函式。



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




