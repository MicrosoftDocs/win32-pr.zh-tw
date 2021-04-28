---
title: 'NM_KEYDOWN (工具列) 通知碼 (Commctrl) '
description: 當控制項有鍵盤焦點且使用者按下按鍵時，NM_KEYDOWN (工具列) 通知碼-由控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- NM_KEYDOWN (工具列) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d53818cf417e1efac686e94d3b4ef5919f819ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112356"
---
# <a name="nm_keydown-toolbar-notification-code"></a>NM \_ KEYDOWN (工具列) 通知碼

當控制項具有鍵盤焦點，且使用者按下按鍵時，由控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey)結構的指標，其中包含造成通知碼之索引鍵的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回非零以防止控制項處理索引鍵，否則傳回零。

## <a name="remarks"></a>備註

目前，只有 toolbar 控制項會傳送此通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





