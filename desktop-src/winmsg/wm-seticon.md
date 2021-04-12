---
description: 將新的大型或小型圖示與視窗產生關聯。 系統會在 ALT + TAB 對話方塊中顯示大型圖示，並在視窗標題中顯示小圖示。
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: 'WM_SETICON 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192784"
---
# <a name="wm_seticon-message"></a>WM \_ SETICON 訊息

將新的大型或小型圖示與視窗產生關聯。 系統會在 ALT + TAB 對話方塊中顯示大型圖示，並在視窗標題中顯示小圖示。


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要設定的圖示類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                       | 意義                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**圖示 \_BIG**</dt> <dt>1</dt> </dl>       | 設定視窗的大型圖示。<br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**圖示 \_小**</dt> <dt>0</dt> </dl> | 設定視窗的小圖示。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

新大或小圖示的控制碼。 如果此參數為 **Null**，則會移除 *wParam* 所指出的圖示。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

傳回值是先前大型或小型圖示的控制碼，取決於 *wParam* 的值。 如果視窗之前沒有 *wParam* 所指定之類型的圖示，則為 **Null** 。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會根據 *wParam* 的值，傳回與視窗相關聯的先前大型或小型圖示控制碼。

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

[**WM \_ GETICON**](wm-geticon.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
