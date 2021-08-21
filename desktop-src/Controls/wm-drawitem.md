---
title: 'WM_DRAWITEM 訊息 (Winuser .h) '
description: 當按鈕、下拉式方塊、清單方塊或功能表的視覺外觀已變更時，傳送至主控描繪按鈕、下拉式方塊、清單方塊或功能表的父視窗。
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- WM_DRAWITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f5d4b2addfa2de5f8c76ded636ca29a96fb3af7e0ab4157d25ac26a78c462c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957517"
---
# <a name="wm_drawitem-message"></a>WM \_ DRAWITEM 訊息

當按鈕、下拉式方塊、清單方塊或功能表的視覺外觀已變更時，傳送至主控描繪按鈕、下拉式方塊、清單方塊或功能表的父視窗。

視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定傳送 **WM \_ DRAWITEM** 訊息之控制項的識別碼。 如果訊息是由功能表傳送，此參數為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的指標，其中包含要繪製之專案的相關資訊，以及所需的繪圖類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE**。

## <a name="remarks"></a>備註

根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會繪製主控描繪清單方塊專案的焦點矩形。

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 *itemAction* 成員會指定應用程式應該執行的繪圖作業。

從處理此訊息傳回之前，應用程式應該確定 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 *hDC* 成員所識別的裝置內容為預設狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

**其他資源**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

