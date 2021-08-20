---
title: 'EM_SCROLL 訊息 (Winuser .h) '
description: 在多行編輯控制項中垂直捲動文字。 這則訊息相當於將 WM \_ VSCROLL 訊息傳送至編輯控制項。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- EM_SCROLL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c619a50d14185289776e891373dcc7fc9e7cae607a899517a4bf5bc9289a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006205"
---
# <a name="em_scroll-message"></a>EM \_ 捲軸訊息

在多行編輯控制項中垂直捲動文字。 這則訊息相當於將 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送至編輯控制項。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

捲軸所要採取的動作。 此參數可以是下列其中一個值。



| 值                                                                                                                                                   | 意義                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl> | 向下捲動一行。<br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ 系列**</dt> </dl>       | 向上捲動一行。<br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> </dl> | 向下捲動一頁。<br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> </dl>       | 向上捲動一頁。<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 為 **TRUE**，而 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 是命令所滾動的行數。 如果捲軸移至文字的開頭或結尾，則傳回的數位可能與滾動的實際行數不同。 如果 *wParam* 參數指定的值無效，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

若要滾動至特定的行或字元位置，請使用 [**EM \_ LINESCROLL**](em-linescroll.md) 訊息。 若要將插入號滾動至視圖，請使用 [**EM \_ SCROLLCARET**](em-scrollcaret.md) 訊息。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

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

[**EM \_ LINESCROLL**](em-linescroll.md)
</dt> <dt>

[**EM \_ SCROLLCARET**](em-scrollcaret.md)
</dt> <dt>

[**WM \_ VSCROLL**](wm-vscroll.md)
</dt> </dl>

 

