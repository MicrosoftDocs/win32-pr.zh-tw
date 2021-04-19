---
title: 'WM_ENTERMENULOOP 訊息 (Winuser .h) '
description: 通知應用程式的主視窗程式，指出已進入功能表強制回應迴圈。
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996176"
---
# <a name="wm_entermenuloop-message"></a>WM \_ ENTERMENULOOP 訊息

通知應用程式的主視窗程式，指出已進入功能表強制回應迴圈。


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定是否使用 [**trackpopupmenu 讓**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) 函數輸入視窗功能表。 如果使用 **trackpopupmenu 讓** 輸入視窗功能表，此參數的值為 **TRUE** ，否則為 **FALSE** 。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函數會傳回零。

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

[**WM \_ EXITMENULOOP**](wm-exitmenuloop.md)
</dt> <dt>

**概念**
</dt> <dt>

[功能表](menus.md)
</dt> </dl>

 

