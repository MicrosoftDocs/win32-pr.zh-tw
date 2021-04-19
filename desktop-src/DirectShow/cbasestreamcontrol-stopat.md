---
description: StopAt 方法會通知 pin 何時停止傳遞資料。 這個方法會實 IAMStreamControl：： StopAt 方法。
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: 'CBaseStreamControl. StopAt 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985931"
---
# <a name="cbasestreamcontrolstopat-method"></a>CBaseStreamControl. StopAt 方法

`StopAt`方法會在停止傳遞資料時通知 pin。 這個方法會實 [**IAMStreamControl：： StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ptStop* 
</dt> <dd>

[**參考 \_ 時間**](reference-time.md)值的指標，此值會指定 pin 應停止傳遞資料的時間。

</dd> <dt>

*bSendExtra* 
</dt> <dd>

指定布林值，指出是否要在排定的停止時間之後傳送額外的範例。 若 **為 TRUE**，則會傳送一個額外的範例給 pin。

</dd> <dt>

*dwCookie* 
</dt> <dd>

指定要連同開始通知一起傳送的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Strmctl (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseStreamControl 類別**](cbasestreamcontrol.md)
</dt> </dl>

 

 




