---
title: 'RBN_HEIGHTCHANGE (Commctrl 的通知碼) '
description: 當 Rebar 控制項的高度變更時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- RBN_HEIGHTCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934314"
---
# <a name="rbn_heightchange-notification-code"></a>RBN \_ HEIGHTCHANGE 通知碼

當 Rebar 控制項的高度變更時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此通知的傳回值。

## <a name="remarks"></a>備註

使用 [**CCS \_ 垂直**](common-control-styles.md) 樣式的 Rebar 控制項，會在其寬度變更時傳送此通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





