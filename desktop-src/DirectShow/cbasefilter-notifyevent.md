---
description: NotifyEvent 方法會將事件通知傳送至篩選圖形管理員。
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: 'CBaseFilter. NotifyEvent 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983185"
---
# <a name="cbasefilternotifyevent-method"></a>CBaseFilter. NotifyEvent 方法

`NotifyEvent`方法會將事件通知傳送至篩選圖形管理員。

## <a name="syntax"></a>語法


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*EventCode* 
</dt> <dd>

事件通知碼。

</dd> <dt>

*EventParam1* 
</dt> <dd>

事件的第一個參數。

</dd> <dt>

*EventParam2* 
</dt> <dd>

事件的第二個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                               | Description                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | 篩選圖形管理員不接受事件通知。<br/>                              |
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 成功。<br/>                                                                                    |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl> | 篩選沒有指向 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面的指標。<br/> |



 

## <a name="remarks"></a>備註

如需通知碼和參數值的清單，請參閱 [事件通知碼](event-notification-codes.md)。

在基類中，如果事件程式碼為 EC \_ 完成，方法會將 *EventParam2* 參數設定為篩選的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




