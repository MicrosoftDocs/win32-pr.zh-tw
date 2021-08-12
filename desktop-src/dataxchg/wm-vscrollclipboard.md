---
title: 'WM_VSCROLLCLIPBOARD 訊息 (Winuser .h) '
description: 當剪貼簿包含 CF \_ OWNERDISPLAY 格式的資料，並在剪貼簿檢視器的垂直捲動條中發生事件時，將剪貼簿檢視器視窗傳送給剪貼簿擁有者。
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD 訊息資料 Exchange
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcf634870ce232543cd20ccd42c9e8ca255705810e81af39cc6e81f8e41658d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544873"
---
# <a name="wm_vscrollclipboard-message"></a>WM \_ VSCROLLCLIPBOARD 訊息

當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，並在剪貼簿檢視器的垂直捲動條中發生事件時，將剪貼簿檢視器視窗傳送給剪貼簿擁有者。 擁有者應該滾動剪貼簿影像，並更新捲軸值。


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

剪貼簿檢視器視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

*LParam* 的低序位字指定捲軸事件。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                         | 意義                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_底部**</dt> <dt>7</dt> </dl>                      | 向右下方。<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ENDSCROLL**</dt> <dt>8</dt> </dl>             | 結束捲軸。<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_LINEDOWN**</dt> <dt>1</dt> </dl>                | 向下移動一行。<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_系列系列**</dt> <dt>0</dt> </dl>                      | 向上移動一行。<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_PAGEDOWN**</dt> <dt>3</dt> </dl>                | 向下移動一頁。<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_PAGEUP**</dt> <dt>2</dt> </dl>                      | 向上滾動一頁。<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_THUMBPOSITION**</dt> <dt>4</dt> </dl> | 滾動至絕對位置。 目前的位置是由高序位字指定。<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_前**</dt> <dt>6</dt>名 </dl>                               | 滾動至左上方。<br/>                                                                  |



 

如果 *lParam* 的低序位字是 **SB \_ THUMBPOSITION**，則 *lParam* 的高序位字組會指定捲動方塊的目前位置; 否則，將不會使用 *lParam* 的高序位字。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

剪貼簿擁有者可以使用 [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) 函式，在 [剪貼簿檢視器] 視窗中滾動影像，並讓適當的區域失效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

