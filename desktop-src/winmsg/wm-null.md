---
description: 不執行任何操作。 如果應用程式 \_ 想要張貼收件者視窗將忽略的訊息，則會傳送 WM Null 訊息。
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: 'WM_Null 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192787"
---
# <a name="wm_null-message"></a>WM \_ Null 訊息

不執行任何操作。 如果應用程式想要張貼收件者視窗將忽略的訊息，則會傳送 **WM \_ Null** 訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則會傳回零。

## <a name="remarks"></a>備註

例如，如果應用程式已安裝 **WH \_ GETMESSAGE** 勾點，而且想要防止處理訊息，則 [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) 回呼函式可以將訊息編號變更為 **WM \_ Null** ，讓收件者略過它。

另一個範例是，應用程式可以使用 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)函數傳送 **WM \_ Null** 訊息，以檢查視窗是否回應訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows 總覽](windows.md)
</dt> </dl>

 

 
