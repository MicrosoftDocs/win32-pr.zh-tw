---
title: 'NM_CLICK (工具列) 通知碼 (Commctrl) '
description: 當使用者按一下具有滑鼠左鍵的專案時，由工具列控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- NM_CLICK (工具列) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844463"
---
# <a name="nm_click-toolbar-notification-code"></a>NM \_ 按一下 (工具列) 通知碼

當使用者按一下具有滑鼠左鍵的專案時，由工具列控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知的其他相關資訊。 **DwItemSpec** 成員包含已按下之區段的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 表示滑鼠按一下已處理，並隱藏系統的預設處理。 傳回 **FALSE** 以允許按一下的預設處理。

## <a name="remarks"></a>備註

按一下具有滑鼠左鍵的專案，會導致工具列將 [BN \_ 按一下](bn-clicked.md)通知程式碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息傳送至父視窗。 NM \_ CLICK 通知會在 **WM \_ 命令** 訊息之後傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

