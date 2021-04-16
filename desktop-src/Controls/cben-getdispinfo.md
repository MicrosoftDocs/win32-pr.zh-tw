---
title: 'CBEN_GETDISPINFO (Commctrl 的通知碼) '
description: 傳送以取得回呼專案的顯示資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508312"
---
# <a name="cben_getdispinfo-notification-code"></a>CBEN \_ GETDISPINFO 通知碼

傳送以取得回呼專案的顯示資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)結構的指標，其中包含通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

處理此通知程式碼的應用程式必須傳回零。

## <a name="remarks"></a>備註

[**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)結構包含 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構。 **遮罩** 成員會指定控制項所要求的資訊。

填入適當的結構成員，以將要求的資訊傳回給控制項。 如果您的訊息處理常式將 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **遮罩** 成員設定為 CBEIF \_ DI \_ SETITEM，則該控制項會儲存資訊，而且不會再次要求它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **CBEN \_GETDISPINFOW** (Unicode) 和 **CBEN \_ GETDISPINFOA** (ANSI) <br/>         |



 

 





