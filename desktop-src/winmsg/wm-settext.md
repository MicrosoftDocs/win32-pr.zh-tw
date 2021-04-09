---
description: 設定視窗的文字。
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: 'WM_SETTEXT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694971"
---
# <a name="wm_settext-message"></a>WM \_ SETTEXT 訊息

設定視窗的文字。


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

以 null 結束的字串指標，也就是視窗文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果已設定文字，則傳回值為 **TRUE** 。 這是 **FALSE** (針對編輯控制項) 、 **LB \_ ERRSPACE** (適用于清單方塊) ，或 **CB \_ ERRSPACE** (適用于下拉式方塊) 如果空間不足，無法設定編輯控制項中的文字。 如果此訊息傳送至沒有編輯控制項的下拉式方塊，則為 **CB \_ 錯誤** 。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會設定並顯示視窗文字。 若為編輯控制項，則文字是編輯控制項的內容。 如果是下拉式方塊，文字就是下拉式方塊編輯控制項部分的內容。 若為按鈕，文字就是按鈕名稱。 若為其他視窗，則文字為視窗標題。

此訊息不會變更下拉式方塊的清單方塊中目前的選取範圍。 應用程式應該使用 [**CB \_ SELECTSTRING**](../controls/cb-selectstring.md) 訊息，在清單方塊中選取符合編輯控制項中文字的專案。

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

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**CB \_ SELECTSTRING**](../controls/cb-selectstring.md)
</dt> </dl>

 

 
