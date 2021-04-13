---
title: 'WM_HSCROLLCLIPBOARD 訊息 (Winuser .h) '
description: 由剪貼簿檢視器視窗傳送給剪貼簿擁有者。
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- WM_HSCROLLCLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466365"
---
# <a name="wm_hscrollclipboard-message"></a>WM \_ HSCROLLCLIPBOARD 訊息

由剪貼簿檢視器視窗傳送給剪貼簿擁有者。 當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，而且在剪貼簿檢視器的水準捲軸中發生事件時，就會發生這種情況。 擁有者應該滾動剪貼簿影像，並更新捲軸值。


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

剪貼簿檢視器視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

*LParam* 的低序位字指定捲軸事件。 此參數可以是下列其中一個值。 如果 *lParam* 的低序位字是 **SB \_ THUMBPOSITION**，則 *lParam* 的高序位字組會指定捲動方塊的目前位置; 否則，就不會使用高序位字。



| 值                                                                                                                                                                                                                         | 意義                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ENDSCROLL**</dt> <dt>8</dt> </dl>             | 結束捲軸。<br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_左方**</dt> <dt>6</dt> </dl>                            | 滾動至左上方。<br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_右**</dt> <dt>7</dt> </dl>                         | 向右下方。<br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_LINELEFT**</dt> <dt>0</dt> </dl>                | 向左滾動一個單位。<br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_LINERIGHT**</dt> <dt>1</dt> </dl>             | 向右滾動一個單位。<br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_PAGELEFT**</dt> <dt>2</dt> </dl>                | 以視窗的寬度向左滾動。<br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_PAGERIGHT**</dt> <dt>3</dt> </dl>             | 向右滾動視窗的寬度。<br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_THUMBPOSITION**</dt> <dt>4</dt> </dl> | 滾動至絕對位置。 目前的位置是由高序位字指定。<br/> |



 

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
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



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

 

