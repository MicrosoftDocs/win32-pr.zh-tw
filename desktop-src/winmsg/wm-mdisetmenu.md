---
description: 應用程式會將 WM \_ MDISETMENU 訊息傳送至多重文件介面 (mdi) 用戶端視窗來取代 mdi 框架視窗的整個功能表、取代框架視窗的視窗功能表，或兩者都是。
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: 'WM_MDISETMENU 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974688"
---
# <a name="wm_mdisetmenu-message"></a>WM \_ MDISETMENU 訊息

應用程式會將 **WM \_ MDISETMENU** 訊息傳送至多重文件介面 (mdi) 用戶端視窗來取代 mdi 框架視窗的整個功能表、取代框架視窗的視窗功能表，或兩者都是。


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

新框架視窗功能表的控制碼。 如果此參數為 **Null**，則不會變更框架視窗功能表。

</dd> <dt>

*lParam* 
</dt> <dd>

新視窗功能表的控制碼。 如果此參數為 **Null**，則不會變更視窗功能表。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HMENU**

如果訊息成功，傳回值就是舊框架視窗功能表的控制碼。

如果訊息失敗，則傳回值為零。

## <a name="remarks"></a>備註

傳送此訊息之後，應用程式必須呼叫 [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) 函式來更新功能表列。

如果此訊息取代了 [視窗] 功能表，則會從上一個 [視窗] 功能表中移除 MDI 子視窗功能表項目，並將其加入至新的 [視窗] 功能表。

如果 MDI 子視窗最大化，而此訊息取代了 MDI 框架視窗功能表，則會從先前的框架視窗功能表中移除 [視窗] 功能表圖示和還原圖示，並將其加入至新的框架視窗功能表。

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

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**WM \_ MDIREFRESHMENU**](wm-mdirefreshmenu.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 
