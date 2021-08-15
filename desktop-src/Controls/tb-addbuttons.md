---
title: 'TB_ADDBUTTONS 訊息 (Commctrl .h) '
description: 將一或多個按鈕加入至工具列。
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd3a5a15ac1983d93ca161dae20876159e5f633cf580d485686d67889276747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168521"
---
# <a name="tb_addbuttons-message"></a>TB \_ ADDBUTTONS 訊息

將一或多個按鈕加入至工具列。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要加入的按鈕數目。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構陣列的指標，其中包含要加入之按鈕的相關資訊。 陣列中的元素數目必須與 *wParam* 所指定的按鈕相同。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果工具列是使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式所建立，您必須先將 [**tb \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) 訊息傳送至工具列，然後再傳送 **tb \_ ADDBUTTONS**。

如需如何將點陣圖指派給一或多個影像清單中的工具列按鈕的討論，請參閱 [**TB \_ SETIMAGELIST**](tb-setimagelist.md) 。

## <a name="examples"></a>範例

下列範例程式碼會使用 [視圖] 按鈕的標準系統點陣圖，將三個按鈕加入至工具列。 [**TB \_ ADDBITMAP**](tb-addbitmap.md)訊息會傳回影像清單中第一個按鈕影像的索引。 個別的影像是以該值的位移來識別。


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_ADDBUTTONSW** (Unicode) 和 **TB \_ ADDBUTTONSA** (ANSI) <br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**工具列標準按鈕影像索引值**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

