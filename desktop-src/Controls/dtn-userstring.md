---
title: 'DTN_USERSTRING (Commctrl 的通知碼) '
description: 當使用者完成編輯控制項中的字串時，日期和時間選擇器會傳送 (DTP) 控制項。
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6eabae4ed5a4fbe9ff0652b77fb7b6fbaf709b9030e3aa982af486ad6b7ed0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062918"
---
# <a name="dtn_userstring-notification-code"></a>DTN \_ USERSTRING 通知碼

當使用者完成編輯控制項中的字串時，日期和時間選擇器會傳送 (DTP) 控制項。 只有設定為 [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) 樣式的 DTP 控制項才會傳送此通知碼。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)結構的指標，其中包含通知碼實例的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項的擁有者必須傳回零。

## <a name="remarks"></a>備註

處理此通知碼可讓擁有者將自訂回應提供給使用者在控制項中輸入的字串。 擁有者必須準備好剖析輸入字串，並視需要採取動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DTN \_USERSTRINGW** (Unicode) 和 **DTN \_ USERSTRINGA** (ANSI) <br/>             |



 

 





