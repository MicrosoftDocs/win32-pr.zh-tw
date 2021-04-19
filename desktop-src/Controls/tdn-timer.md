---
title: 'TDN_TIMER (Commctrl 的通知碼) '
description: 工作對話方塊大約每隔200毫秒傳送一次。
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966354"
---
# <a name="tdn_timer-notification-code"></a>TDN \_ 計時器通知碼

工作對話方塊大約每隔200毫秒傳送一次。 當已 \_ \_ 在傳遞給 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)函式的 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構的 **dwFlags** 成員中設定 .tdf 回呼計時器旗標時，就會傳送此通知碼。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 **TaskDialogIndirect** 方法來註冊。


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD** ，指定自建立對話方塊之後的毫秒數，或此通知碼傳回 **\_ FALSE**。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

若要重設 tickcount，應用程式必須 **傳回 \_ FALSE**，否則 tickcount 會繼續遞增。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





