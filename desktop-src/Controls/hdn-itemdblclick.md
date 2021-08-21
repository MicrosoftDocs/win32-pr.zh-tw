---
title: 'HDN_ITEMDBLCLICK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，使用者按兩下控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。 只有設定為 HDS 按鈕樣式的標題控制項才會 \_ 傳送此通知碼。
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7117ceb8d17447eed8003f7da3dab70a17252c750bfb3885cd3f235a70b7bb53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544609"
---
# <a name="hdn_itemdblclick-notification-code"></a>HDN \_ ITEMDBLCLICK 通知碼

通知標題控制項的父視窗，使用者按兩下控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 只有設定為 [**HDS \_ 按鈕**](header-control-styles.md) 樣式的標題控制項才會傳送此通知碼。


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含此通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDN \_ITEMDBLCLICKW** (Unicode) 和 **HDN \_ ITEMDBLCLICKA** (ANSI) <br/>         |



 

 





