---
title: 'TBN_SAVE (Commctrl 的通知碼) '
description: 通知工具列的父視窗，工具列正在儲存中。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f9d4fb40d0e5beafcd720b4de52a8cf09d17c3e4c6f7b4dcfa8da78e00e97ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876588"
---
# <a name="tbn_save-notification-code"></a>TBN \_ 儲存通知碼

通知工具列的父視窗，工具列正在儲存中。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

應用程式會在儲存程式開始時接收此通知碼一次，並在每個按鈕上接收一次。 此通知碼可讓您有機會將自己的資訊新增至 Shell 所儲存的資訊。 如果您不想要新增資訊，請忽略通知碼。 如需如何處理 TBN 儲存的詳細討論，請參閱 [工具列自訂](toolbar-controls-overview.md) \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[TBN \_ 還原](tbn-restore.md)
</dt> </dl>

 

 





