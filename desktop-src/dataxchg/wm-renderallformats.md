---
title: 'WM_RENDERALLFORMATS 訊息 (Winuser .h) '
description: 如果剪貼簿擁有者有延遲轉譯一或多個剪貼簿格式，則會在終結之前傳送給剪貼簿擁有者。
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS 訊息資料交換
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509092"
---
# <a name="wm_renderallformats-message"></a>WM \_ RENDERALLFORMATS 訊息

如果剪貼簿擁有者有延遲轉譯一或多個剪貼簿格式，則會在終結之前傳送給剪貼簿擁有者。 若要讓剪貼簿的內容仍然可供其他應用程式使用，剪貼簿擁有者必須以它能夠產生的所有格式轉譯資料，並藉由呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) 函式將資料放在剪貼簿上。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

回應 **WM \_ RENDERALLFORMATS** 訊息時，應用程式必須呼叫 [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) 函式，然後藉由呼叫 [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) 函式來檢查它是否仍是剪貼簿擁有者，然後再呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)。

在開啟剪貼簿之後，應用程式必須檢查它是否仍是剪貼簿擁有者，因為它會在收到 **WM \_ RENDERALLFORMATS** 訊息之後，但在開啟剪貼簿之前，另一個應用程式可能已開啟並取得剪貼簿的擁有權，而且不應該覆寫該應用程式的資料。

在大部分的情況下，應用程式不應該在呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)之前呼叫 [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard)函式，因為這樣做會清除應用程式已經轉譯的剪貼簿格式。

當應用程式傳回時，系統會從可用的剪貼簿格式清單中移除任何 unrendered 格式。 如需延遲呈現的詳細資訊，請參閱 [延遲](clipboard-operations.md#delayed-rendering)轉譯。

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

[**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERFORMAT**](wm-renderformat.md)
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> </dl>

 

