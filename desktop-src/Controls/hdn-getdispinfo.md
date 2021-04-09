---
title: 'HDN_GETDISPINFO (Commctrl 的通知碼) '
description: 當控制項需要回呼標頭專案的相關資訊時，傳送至標題控制項的擁有者。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024669"
---
# <a name="hdn_getdispinfo-notification-code"></a>HDN \_ GETDISPINFO 通知碼

當控制項需要回呼標頭專案的相關資訊時，傳送至標題控制項的擁有者。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa)結構的指標。 在輸入時，結構的欄位會指定所需的資訊，以及感興趣的專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 LRESULT。

## <a name="remarks"></a>備註

填入適當的結構成員，以將要求的資訊傳回至標題控制項。 如果您的訊息處理常式將 [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa)結構的 **遮罩** 成員設定為 HDI \_ DI \_ SETITEM，則標頭控制項會儲存資訊，而不會再次要求它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDN \_GETDISPINFOW** (Unicode) 和 **HDN \_ GETDISPINFOA** (ANSI) <br/>           |



 

 





