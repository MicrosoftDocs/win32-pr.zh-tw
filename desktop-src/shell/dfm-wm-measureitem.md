---
description: 當控制項或功能表建立時，傳送至控制項或功能表項目的擁有者視窗。
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: 'DFM_WM_MEASUREITEM 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386113"
---
# <a name="dfm_wm_measureitem-message"></a>DFM \_ WM \_ MEASUREITEM 訊息

當控制項或功能表建立時，傳送至控制項或功能表項目的擁有者視窗。


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

*LpMeasureItem* 參數所指向之 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構的 **CtlID** 成員的值。 此值會識別傳送 **DFM \_ WM \_ MEASUREITEM** 訊息的控制項。

</dd> <dt>

*lpMeasureItem* \[擴展\]
</dt> <dd>

[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構的指標，其中包含主控描繪控制項或功能表項目的維度。

</dd> </dl>

## <a name="remarks"></a>備註

當擁有者視窗收到 **DFM 的 \_ WM \_ MEASUREITEM** 訊息時，擁有者會填入訊息的 *LpMeasureItem* 參數所指向的 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構並傳回; 這會通知系統有控制項的維度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
