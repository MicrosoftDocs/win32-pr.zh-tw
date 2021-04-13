---
title: 'DTN_FORMAT (Commctrl 的通知碼) '
description: 由日期和時間選擇器所傳送 (DTP) 控制項，要求在回呼欄位中顯示文字。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- DTN_FORMAT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465920"
---
# <a name="dtn_format-notification-code"></a>DTN \_ 格式通知碼

由日期和時間選擇器所傳送 (DTP) 控制項，要求在回呼欄位中顯示文字。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)結構的指標，其中包含此通知碼實例的相關資訊。 結構包含定義回呼欄位的子字串，並接收控制項將顯示的格式化字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項的擁有者必須傳回零。

## <a name="remarks"></a>備註

處理此通知碼可讓控制項的擁有者提供控制項將顯示的自訂字串。  (如需回呼欄位的其他資訊，請參閱 [回呼欄位](date-and-time-picker-controls.md)。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DTN \_FORMATW** (Unicode) 和 **DTN \_ FORMATA** (ANSI) <br/>                     |



 

 





