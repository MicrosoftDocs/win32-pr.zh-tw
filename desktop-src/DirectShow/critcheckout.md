---
description: 如果目前的執行緒是指定之重要區段的擁有者，則傳回 FALSE。
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: 'CritCheckOut 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995278"
---
# <a name="critcheckout-function"></a>CritCheckOut 函式

如果目前的執行緒是指定之重要區段的擁有者，則傳回 **FALSE** 。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcCrit* 
</dt> <dd>

[**CCritSec**](ccritsec.md)重要區段的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

在偵錯工具組建中，如果目前的執行緒是此重要區段的擁有者，則傳回 **FALSE** ，否則傳回 **TRUE** 。 在零售組建中，一律會傳回 **TRUE**。

## <a name="remarks"></a>備註

此函數是 [**CritCheckIn**](critcheckin.md) 函數的反向。 如果 **CritCheckIn** 傳回 **TRUE，則** **CritCheckOut** 會傳回 **FALSE**，反之亦然。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[重要區段調試函數](critical-section-debugging-functions.md)
</dt> </dl>

 

 




