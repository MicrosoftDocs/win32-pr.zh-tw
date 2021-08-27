---
description: Unadvise 方法會移除建議的要求。
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: 'CAMSchedule. Unadvise 方法 (Dsschedule .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bc9b1c964d698e1c1323846c7a25a29f60c0cd71009fbb60f1a09a6757b50b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057598"
---
# <a name="camscheduleunadvise-method"></a>CAMSchedule. Unadvise 方法

`Unadvise`方法會移除建議的要求。

## <a name="syntax"></a>語法


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

[**CAMSchedule：： AddAdvisePacket**](camschedule-addadvisepacket.md)方法所傳回之建議要求的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | 描述          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 找不到<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | Success<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dsschedule (包含： .h) </dt> </dl>                                                                                |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMSchedule 類別**](camschedule.md)
</dt> </dl>

 

 




