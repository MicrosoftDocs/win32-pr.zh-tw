---
title: 'TDN_RADIO_BUTTON_CLICKED (Commctrl 的通知碼) '
description: 當使用者在工作對話方塊中選取選項按鈕或命令連結時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 TaskDialogIndirect 方法來註冊。
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- TDN_RADIO_BUTTON_CLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea1917a1523cdc3a106398d07912d3fff5295f7da18a59055f059a13007f98b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875758"
---
# <a name="tdn_radio_button_clicked-notification-code"></a>TDN \_ 選項按鈕已按下 \_ \_ 通知碼

當使用者在工作對話方塊中選取選項按鈕或命令連結時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**Int** ，指定對應至已按一下之選項按鈕的識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





