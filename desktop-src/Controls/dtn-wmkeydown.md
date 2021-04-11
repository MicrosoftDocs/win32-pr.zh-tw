---
title: 'DTN_WMKEYDOWN (Commctrl 的通知碼) '
description: 當使用者在回呼欄位中輸入時，日期和時間選擇器會傳送 (DTP) 控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094011"
---
# <a name="dtn_wmkeydown-notification-code"></a>DTN \_ WMKEYDOWN 通知碼

當使用者在回呼欄位中輸入時，日期和時間選擇器會傳送 (DTP) 控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)結構的指標，其中包含此通知碼實例的相關資訊。 結構包含使用者所輸入之金鑰的相關資訊、定義回呼欄位的子字串，以及目前的系統日期和時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項的擁有者必須傳回零。

## <a name="remarks"></a>備註

處理此通知程式碼可讓控制項的擁有者在控制項的回呼欄位內提供對按鍵的特定回應。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DTN \_WMKEYDOWNW** (Unicode) 和 **DTN \_ WMKEYDOWNA** (ANSI) <br/>               |



 

 





