---
title: 'WM_EXITMENULOOP 訊息 (Winuser .h) '
description: 通知應用程式的主視窗程式，表示已結束功能表強制回應迴圈。
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec6d2cfb8457a748b7bb7bbdda481a0a1f73e5331891d45bd1bf1cabdfe0c5c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886378"
---
# <a name="wm_exitmenuloop-message"></a>WM \_ EXITMENULOOP 訊息

通知應用程式的主視窗程式，表示已結束功能表強制回應迴圈。


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定功能表是否為快捷方式功能表。 如果這個參數是快捷方式功能表，則此參數的值為 **TRUE** ，否則為 **FALSE** 。

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
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ENTERMENULOOP**](wm-entermenuloop.md)
</dt> <dt>

**概念**
</dt> <dt>

[功能表](menus.md)
</dt> </dl>

 

