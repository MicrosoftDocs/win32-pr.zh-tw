---
title: 'TVN_KEYDOWN (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，讓使用者按下按鍵，並讓樹狀檢視控制項擁有輸入焦點。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464245"
---
# <a name="tvn_keydown-notification-code"></a>IZDEBSKI \_ KEYDOWN 通知碼

通知樹狀檢視控制項的父視窗，讓使用者按下按鍵，並讓樹狀檢視控制項擁有輸入焦點。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown)結構的指標。 **WVKey** 成員會指定虛擬金鑰碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *lParam* 的 **wVKey** 成員是字元按鍵碼，則會使用該字元作為增量搜尋的一部分。 傳回非零值以排除增量搜尋中的字元，或零以包含搜尋中的字元。 若為所有其他索引鍵，則會忽略傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





