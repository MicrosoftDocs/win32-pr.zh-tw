---
description: AddAdvisePacket 方法會將建議要求新增至暫止的要求清單。
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: 'CAMSchedule. AddAdvisePacket 方法 (Dsschedule .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999272"
---
# <a name="camscheduleaddadvisepacket-method"></a>CAMSchedule. AddAdvisePacket 方法

`AddAdvisePacket`方法會將建議要求新增至暫止的要求清單。

## <a name="syntax"></a>語法


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*time1* \[裁判\]
</dt> <dd>

建議的要求時間。

</dd> <dt>

*time2* \[裁判\]
</dt> <dd>

針對週期性建議要求，這是通知之間的時間。 如果 *bPeriodic* 為 **FALSE**，則會忽略此參數。

</dd> <dt>

*hNotify* 
</dt> <dd>

如果 *bPeriodic* 為 **TRUE**，則為信號的控制碼，如果 *bPeriodic* 為 **FALSE**，則處理事件的控制碼。

</dd> <dt>

*bPeriodic* 
</dt> <dd>

指定是否要新增定期通知或單次通知的布林值。 若 **為 TRUE**，則會定期通知; *time2* 參數會指定通知之間的時間。 若 **為 FALSE**，則只會出現一次通知。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回「cookie」 )  (「建議」要求的識別碼。 如果方法失敗，則傳回值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dsschedule (包含： .h) </dt> </dl>                                                                                |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMSchedule 類別**](camschedule.md)
</dt> </dl>

 

 




