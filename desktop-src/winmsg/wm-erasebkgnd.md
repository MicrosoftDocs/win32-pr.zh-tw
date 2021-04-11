---
description: 當視窗背景必須清除時傳送 (例如，當調整視窗大小時) 。 傳送訊息以準備視窗的無效部分進行繪製。
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: 'WM_ERASEBKGND 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193703"
---
# <a name="wm_erasebkgnd-message"></a>WM \_ ERASEBKGND 訊息

當視窗背景必須清除時傳送 (例如，當調整視窗大小時) 。 傳送訊息以準備視窗的無效部分進行繪製。


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

裝置內容的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式清除背景，則應該傳回非零值;否則，它應該會傳回零。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會使用 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **hbrBackground** 成員所指定的類別背景筆刷，來清除背景。 如果 **hbrBackground** 為 **Null**，則應用程式應該處理 **WM \_ ERASEBKGND** 訊息並清除背景。

如果應用程式處理訊息並清除背景，則應用程式應該傳回非零以回應 **WM \_ ERASEBKGND** ; 這表示不需要進一步清除。 如果應用程式傳回零，視窗將維持標記以進行清除。  (通常表示 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)結構的 **fErase** 成員將會是 **TRUE**。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

**概念**
</dt> <dt>

[圖示](../menurc/icons.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
