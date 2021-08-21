---
title: 'DTN_FORMATQUERY (Commctrl 的通知碼) '
description: 由日期和時間選擇器所傳送 (DTP) 控制項，以取得將顯示在回呼欄位中之字串的允許大小上限。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14bd1a9efe22251aba71f157dfb2a68e2b0a70385c30564bb7f08e420e0c0cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019986"
---
# <a name="dtn_formatquery-notification-code"></a>DTN \_ FORMATQUERY 通知碼

由日期和時間選擇器所傳送 (DTP) 控制項，以取得將顯示在回呼欄位中之字串的允許大小上限。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya)結構的指標，其中包含回呼欄位的相關資訊。 結構包含定義回呼欄位的子字串，並接收將在回呼欄位中顯示之字串的最大允許大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項的擁有者必須計算將顯示在回呼欄位中之文字的最大可能寬度、設定 [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya)結構的 **szMax** 成員，然後傳回零。

## <a name="remarks"></a>備註

處理此通知程式碼可讓控制項進行調整，以調整將顯示在特定回呼欄位中的字串大小上限。 這樣可讓控制項隨時適當地顯示輸出，減少控制項顯示內的閃爍。  (如需回呼欄位的其他資訊，請參閱 [回呼欄位](date-and-time-picker-controls.md)。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DTN \_FORMATQUERYW** (Unicode) 和 **DTN \_ FORMATQUERYA** (ANSI) <br/>           |



 

 





