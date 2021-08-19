---
description: SendNotifyWindow 方法會通知影片視窗控制碼的上游篩選。
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: 'CBaseRenderer. SendNotifyWindow 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b4956ad2b20040b0d22903d2ffaa2c7b460af9250fe057d106db545173d53a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157495"
---
# <a name="cbaserenderersendnotifywindow-method"></a>CBaseRenderer. SendNotifyWindow 方法

`SendNotifyWindow`方法會通知影片視窗控制碼的上游篩選。

## <a name="syntax"></a>語法


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* 
</dt> <dd>

上游篩選器輸出釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。

</dd> <dt>

*hwnd* 
</dt> <dd>

影片視窗的控制碼，或 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果上游篩選的輸出釘選支援 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面，這個方法會將 [**EC \_ 通知 \_ 視窗**](ec-notify-window.md) 事件程式碼連同視窗控制碼一起傳送給它。

影片轉譯器可覆寫其 [**CBaseRenderer：： CompleteConnect**](cbaserenderer-completeconnect.md) 方法，以呼叫這個方法。 它會提供一種機制，以通知視窗控制碼的上游篩選。 如果您這樣做，請也覆寫 [**CBaseRenderer：： BreakConnect**](cbaserenderer-breakconnect.md) 方法，並 `SendNotifyWindow` 使用 **Null** 控制碼來呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




