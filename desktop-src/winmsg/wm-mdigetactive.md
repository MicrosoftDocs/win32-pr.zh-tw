---
description: 應用程式會將 WM \_ MDIGETACTIVE 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以抓取作用中 MDI 子視窗的控制碼。
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: 'WM_MDIGETACTIVE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979923"
---
# <a name="wm_mdigetactive-message"></a>WM \_ MDIGETACTIVE 訊息

應用程式會將 **WM \_ MDIGETACTIVE** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以抓取作用中 MDI 子視窗的控制碼。


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

最大化的狀態。 如果這個參數不是 **Null**，它就是值的指標，指出 MDI 子視窗最大化的狀態。 如果值為 **TRUE**，則會將視窗最大化; **FALSE** 值表示它不是。 如果此參數為 **Null**，則會忽略參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HWND**

傳回值是現用 MDI 子視窗的控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[多重文件介面總覽](multiple-document-interface.md)
</dt> </dl>

 

 




