---
description: 「建議」方法會分派排程于指定時間或更早時間的所有要求。
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: 'CAMSchedule，建議方法 (Dsschedule) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0943479aaa7fe2e6d699bba147977a73f48fc31186fb64ea26a211e2ea31d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757788"
---
# <a name="camscheduleadvise-method"></a>CAMSchedule，建議方法

`Advise`方法會分派排程于指定時間或更早時間的所有要求。

## <a name="syntax"></a>語法


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rtTime* \[裁判\]
</dt> <dd>

指定目前參考時間的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下一個排定的建議要求的參考時間，或如果沒有任何剩餘的時間，則為最大 \_ 時間。

## <a name="remarks"></a>備註

當時鐘呼叫這個方法時，它會指定目前的參考時間。 排程器會判斷哪些告知要求已過期（如果有的話），並分派這些要求。 如果單次要求過期，排程器就會將它刪除。 如果定期要求過期，排程器會在下一個建議時間重新排程它。 方法會傳回下一個暫止要求的時間。

為了分派提出建議的要求，排程器會向 [**CAMSchedule：： AddAdvisePacket**](camschedule-addadvisepacket.md)方法的 *hNotify* 參數中指定的事件或信號發出信號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dsschedule (包含： .h) </dt> </dl>                                                                                |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMSchedule 類別**](camschedule.md)
</dt> </dl>

 

 




