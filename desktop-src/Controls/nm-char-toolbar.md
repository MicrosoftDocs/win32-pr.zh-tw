---
title: 'NM_CHAR (工具列) 通知碼 (Commctrl) '
description: 當工具列收到 WM \_ 字元訊息時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- NM_CHAR (工具列) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a318c7385e9d7205ad0fa159e1f987c5d650d27414eefeed4d915c5544cb4564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018936"
---
# <a name="nm_char-toolbar-notification-code"></a>NM \_ 字元 (工具列) 通知碼

當工具列收到 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar)結構的指標，其中包含造成通知碼之字元的其他相關資訊。 此結構的 **dwItemPrev** 成員包含目前作用中之專案的命令識別碼，如果沒有任何專案在作用中，則為-1。 此結構的 **dwItemNext** 成員包含將變成經常性存取之專案的命令識別碼，如果索引鍵不符合任何專案的快速鍵，則為-1。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** ，表示工具列不應處理字元和 **FALSE** ，讓工具列處理該字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

