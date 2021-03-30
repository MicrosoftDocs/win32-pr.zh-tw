---
description: '\_只要使用者變更裝置模式設定，就會將 WM DEVMODECHANGE 訊息傳送至所有最上層視窗。'
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: 'WM_DEVMODECHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973517"
---
# <a name="wm_devmodechange-message"></a>WM \_ DEVMODECHANGE 訊息

只要使用者變更裝置模式設定，就會將 **WM \_ DEVMODECHANGE** 訊息傳送至所有最上層視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控點。

</dd> <dt>

*uMsg* 
</dt> <dd>

WM \_ DEVMODECHANGE

</dd> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

指定裝置名稱之字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

此訊息無法直接傳送至視窗。 若要將 **WM \_ DEVMODECHANGE** 訊息傳送至所有最上層視窗，請使用 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) 函式並將 *hwnd* 參數設定為 hwnd \_ 廣播。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[裝置內容總覽](device-contexts.md)
</dt> <dt>

[裝置內容訊息](device-context-messages.md)
</dt> </dl>

 

 
