---
title: QuadReadAcrossDiagonal 函式
description: 傳回指定的區域值，此值是從這個四個對角線中的相反通道讀取的。
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- QuadReadAcrossDiagonal 函式 HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53066864ec87528406b20d5503f4e47497cb3aa80e44f01e279845fdc2674339
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981928"
---
# <a name="quadreadacrossdiagonal-function"></a>QuadReadAcrossDiagonal 函式

傳回指定的區域值，此值是從這個四個對角線中的相反通道讀取的。

## <a name="syntax"></a>語法


``` syntax
<type> QuadReadAcrossDiagonal(
   <type> localValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*localValue* 
</dt> <dd>

要求的類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

指定的區域值，此值會從這個四項的對角線方向進行讀取。

## <a name="remarks"></a>備註

如需四邊形的詳細資訊，請參閱 [著色器模型6的總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)。

只有在圖元和計算著色器中才支援來自著色器模型6.0 的函式。



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




