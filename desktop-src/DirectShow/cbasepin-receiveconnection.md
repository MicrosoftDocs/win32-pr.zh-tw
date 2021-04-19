---
description: ReceiveConnection 方法會接受來自另一個 pin 的連接。 這個方法會實 IPin：： ReceiveConnection 方法。
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: 'CBasePin. ReceiveConnection 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995375"
---
# <a name="cbasepinreceiveconnection-method"></a>CBasePin. ReceiveConnection 方法

`ReceiveConnection`方法會接受來自另一個 pin 的連接。 這個方法會實 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pConnector* 
</dt> <dd>

連接釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                                | Description                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                                                                |
| <dl> <dt>**E \_ 指標**</dt> </dl>                  | **Null** 指標引數。<br/>                                              |
| <dl> <dt>**VFW \_ E \_ 已 \_ 連線**</dt> </dl>  | Pin 已連線。<br/>                                           |
| <dl> <dt>**VFW \_ E \_ 未 \_ 停止**</dt> </dl>        | 篩選準則為使用中，且 pin 不支援動態重新連接。<br/> |
| <dl> <dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt> </dl> | 無法接受指定的媒體類型。<br/>                             |



 

## <a name="remarks"></a>備註

輸出圖釘會在輸入 pin 上呼叫這個方法。 如果輸入 pin 傳回錯誤碼，連接將會失敗。

在基類中，這個方法會執行下列步驟：

-   檢查 pin 是否已連接。
-   檢查篩選是否已停止。
-   呼叫 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) 方法以測試連接的 pin 是否適合。
-   呼叫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法，測試是否可接受媒體類型。

如果上述所有步驟都成功，則此方法會呼叫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 和 [**SetMediaType**](cbasepin-setmediatype.md) 方法來完成連接。 這些方法會將媒體類型和指標儲存在輸出圖釘的上方。

如果 **CheckConnect** 或 **CheckMediaType** 失敗，基類會呼叫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法來中斷連接，然後從傳回錯誤碼 `ReceiveConnection` 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




