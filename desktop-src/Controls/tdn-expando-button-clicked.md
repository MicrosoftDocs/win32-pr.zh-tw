---
title: 'TDN_EXPANDO_BUTTON_CLICKED (Commctrl 的通知碼) '
description: 當使用者按一下對話方塊的 expando 按鈕時，由工作對話方塊傳送。 只有透過工作對話方塊回呼函式（可使用 TaskDialogIndirect 方法來註冊）才會收到此通知。
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- TDN_EXPANDO_BUTTON_CLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968998"
---
# <a name="tdn_expando_button_clicked-notification-code"></a>TDN \_ EXPANDO \_ 按鈕已 \_ 按一下通知碼

當使用者按一下對話方塊的 expando 按鈕時，由工作對話方塊傳送。 只有透過工作對話方塊回呼函式（可使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊）才會收到此通知。


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

如果展開對話方塊，則 **布林****值為 TRUE** ，否則為 **FALSE** 。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

語法區段中的範例會顯示在傳送通知之前轉換成 wParam。 **LPARAM** 不會使用，且必須為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





