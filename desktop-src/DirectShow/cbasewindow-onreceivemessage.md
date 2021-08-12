---
description: OnReceiveMessage 方法會處理視窗訊息。
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: 'CBaseWindow. OnReceiveMessage 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a5dbfb84edef1f5257cfda8cae08d27b219909f47a7d88fd29580ae12e48b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657961"
---
# <a name="cbasewindowonreceivemessage-method"></a>CBaseWindow. OnReceiveMessage 方法

`OnReceiveMessage`方法會處理視窗訊息。

## <a name="syntax"></a>語法


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> <dt>

*uMsg* 
</dt> <dd>

訊息識別碼。

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

如果已處理訊息，則傳回 0; 如果未處理訊息，則傳回1。

## <a name="remarks"></a>備註

基底類別會處理下列訊息：

-   WM \_ 關閉
-   WM \_ 移動
-   WM \_ PALETTECHANGED
-   WM \_ QUERYNEWPALETTE
-   WM \_ 大小
-   WM \_ SYSCOLORCHANGE

衍生類別可以覆寫這個方法來處理其他訊息。 衍生類別應該呼叫基類方法，以處理衍生類別忽略的任何訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




