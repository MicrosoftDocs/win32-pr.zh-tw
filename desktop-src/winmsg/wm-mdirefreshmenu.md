---
description: 應用程式會將 WM \_ MDIREFRESHMENU 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以重新整理 mdi 框架視窗的 [視窗] 功能表。
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: 'WM_MDIREFRESHMENU 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 707059d3cc51703819968f929f9692dbb2422ee3f9fa77e2edb697f12257faf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200064"
---
# <a name="wm_mdirefreshmenu-message"></a>WM \_ MDIREFRESHMENU 訊息

應用程式會將 **WM \_ MDIREFRESHMENU** 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以重新整理 mdi 框架視窗的 [視窗] 功能表。


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HMENU**

如果訊息成功，則傳回值是框架視窗功能表的控制碼。

如果訊息失敗，則傳回值為 **Null**。

## <a name="remarks"></a>備註

傳送此訊息之後，應用程式必須呼叫 [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) 函式來更新功能表列。

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

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**WM \_ MDISETMENU**](wm-mdisetmenu.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 
