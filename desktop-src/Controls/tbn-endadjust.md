---
title: 'TBN_ENDADJUST (Commctrl 的通知碼) '
description: 通知工具列的父視窗，指出使用者已停止自訂工具列。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 9a7496ec-787d-4571-8eca-50d60383519b
keywords:
- TBN_ENDADJUST 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_ENDADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec420c535a207f02d12e17901efab1c18a11bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024986"
---
# <a name="tbn_endadjust-notification-code"></a>TBN \_ ENDADJUST 通知碼

通知工具列的父視窗，指出使用者已停止自訂工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_ENDADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





