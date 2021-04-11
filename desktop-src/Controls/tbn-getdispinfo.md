---
title: 'TBN_GETDISPINFO (Commctrl 的通知碼) '
description: 抓取工具列專案的顯示資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- TBN_GETDISPINFO 通知碼 Windows 控制項
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105029"
---
# <a name="tbn_getdispinfo-notification-code"></a>TBN \_ GETDISPINFO 通知碼

抓取工具列專案的顯示資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa)結構的指標。 **IdCommand** 成員會指定專案的命令識別碼、 **lParam** 成員包含專案的應用程式定義資料，而 **dwMask** 成員會指定所要求的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項會忽略傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TBN \_GETDISPINFOW** (Unicode) 和 **TBN \_ GETDISPINFOA** (ANSI) <br/>           |



 

 





