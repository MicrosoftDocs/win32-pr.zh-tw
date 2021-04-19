---
description: NotifyOwnerMessage 方法會將特定訊息傳遞至影片視窗。
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: 'CBaseControlWindow. NotifyOwnerMessage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001221"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>CBaseControlWindow. NotifyOwnerMessage 方法

方法會將 `NotifyOwnerMessage` 特定訊息傳遞至影片視窗。

## <a name="syntax"></a>語法


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

影片視窗的控制碼。

</dd> <dt>

*uMsg* 
</dt> <dd>

訊息詳細資料。

</dd> <dt>

*wParam* 
</dt> <dd>

第一個訊息參數。

</dd> <dt>

*lParam* 
</dt> <dd>

第二個訊息參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

不傳回任何 \_ 錯誤。

## <a name="remarks"></a>備註

當影片視窗是另一個視窗的子系時，不會收到特定的最上層視窗訊息。 這些訊息可能對轉譯器很有價值，因為它們可能會影響其行為。 `NotifyOwnerMessage` 將下列任何訊息傳遞至影片視窗。

-   WM \_ ACTI加值稅EAPP
-   WM \_ DEVMODECHANGE
-   WM \_ DISPLAYCHANGE
-   WM \_ PALETTECHANGED
-   WM \_ PALETTEISCHANGING
-   WM \_ QUERYNEWPALETTE
-   WM \_ SYSCOLORCHANGE

您可以要求 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 外掛程式散發者 (PID) 讓視窗變成另一個視窗的子系。 發生這種情況時，PID 會尋找可能傳送至主控視窗的特定訊息。 然後，PID 會將這些訊息轉送到擁有的視窗。 訊息的預設處理方式是藉由呼叫 Win32 **SendMessage** 函式，以同步方式將訊息傳送到擁有的視窗程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




