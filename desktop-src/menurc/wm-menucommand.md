---
title: 'WM_MENUCOMMAND 訊息 (Winuser .h) '
description: 當使用者從功能表進行選取時傳送。
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385278"
---
# <a name="wm_menucommand-message"></a>WM \_ MENUCOMMAND 訊息

當使用者從功能表進行選取時傳送。


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

所選取專案之以零為起始的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

已選取專案之功能表的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

**WM \_ MENUCOMMAND** 訊息會提供您功能表的控制碼，讓您可以存取 [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo)結構中的功能表資料，也會提供所選取專案的索引，這通常是應用程式所需的專案。 相反地， [**WM \_ 命令**](wm-command.md) 訊息會提供您功能表項目識別碼。

只有在 [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo)結構的 **dwStyle** 成員中設定的 **MNS \_ NOTIFYBYPOS** 旗標所定義的功能表上，才會傳送 **WM \_ MENUCOMMAND** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[功能表總覽](menus.md)
</dt> </dl>

 

 





