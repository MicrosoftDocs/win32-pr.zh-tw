---
title: 'NM_NCHITTEST (Rebar) 通知碼 (Commctrl) '
description: NM_NCHITTEST (Rebar) 通知碼-當控制項收到 WM NCHITTEST 訊息時，由 Rebar 控制項傳送 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST (Rebar) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5831ca9dbeda35c7757613cae1d31db921aa80f4b749d4c9407339a2531abcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410699"
---
# <a name="nm_nchittest-rebar-notification-code"></a>NM \_ NCHITTEST (Rebar) 通知碼

當控制項收到 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 訊息時，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含通知碼的相關資訊。 **DwItemSpec** 成員包含發生點擊測試訊息的頻外索引，而 **pt** 成員則包含點擊測試訊息的滑鼠座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以允許 Rebar 執行點擊測試訊息的預設處理，或傳回 \* 在 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 下記載的其中一個 HT 值以覆寫預設點擊測試處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

