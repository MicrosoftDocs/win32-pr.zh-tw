---
title: 'EN_DROPFILES (Richedit 的通知碼) '
description: 通知 rich edit 控制項父視窗，使用者嘗試將檔案放入控制項。 Rich edit 控制項會在 \_ 收到 wm DROPFILES 訊息時，以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8813d3d62883ab607bb898f4aa34a664cbab47b2c8214fbd83fc8cc7913e26ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047778"
---
# <a name="en_dropfiles-notification-code"></a>EN \_ DROPFILES 通知碼

通知 rich edit 控制項父視窗，使用者嘗試將檔案放入控制項。 Rich edit 控制項會在收到 [**wm \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles)訊息時，以 [**WM \_ 通知**](wm-notify.md)訊息的形式傳送此通知碼。


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

接收已卸載檔案資訊的 [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回非零值以允許 drop 作業。

傳回零以忽略 drop 作業。

## <a name="remarks"></a>備註

若要讓 rich edit 控制項接收 [**WM \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) 訊息，父視窗必須使用 [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) 函數，將控制項註冊為放置目標。 控制項不會自行註冊。

若要接收 EN \_ DROPFILES 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

