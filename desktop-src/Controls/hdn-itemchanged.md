---
title: 'HDN_ITEMCHANGED (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，標題專案的屬性已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- HDN_ITEMCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024668"
---
# <a name="hdn_itemchanged-notification-code"></a>HDN \_ ITEMCHANGED 通知碼

通知標題控制項的父視窗，標題專案的屬性已變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的相關資訊，包括已變更的屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDN \_ITEMCHANGEDW** (Unicode) 和 **HDN \_ ITEMCHANGEDA** (ANSI) <br/>           |



 

 





