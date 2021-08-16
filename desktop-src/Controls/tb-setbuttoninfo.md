---
title: 'TB_SETBUTTONINFO 訊息 (Commctrl .h) '
description: 設定工具列中現有按鈕的資訊。
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- TB_SETBUTTONINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e9fa1da0f9556c025b83ac2b3345680fe11dac0dd15e202ed7336cacfe511e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829622"
---
# <a name="tb_setbuttoninfo-message"></a>TB \_ SETBUTTONINFO 訊息

設定工具列中現有按鈕的資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

按鈕識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa)結構的指標，其中包含新的按鈕資訊。 在傳送此訊息之前，必須先填入此結構的 **cbSize** 和 **dwMask** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

將文字新增至工具列時，通常會將文字指派給按鈕，方法是在工具列的字串集區中指定字串的索引。 如果您使用 **TB \_ SETBUTTONINFO** 將新文字指派給按鈕，則會從字串集區永久覆寫文字。 您可以再次呼叫 **TB \_ SETBUTTONINFO** 來變更文字，但無法從字串集區重新指派字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_SETBUTTONINFOW** (Unicode) 和 **TB \_ SETBUTTONINFOA** (ANSI) <br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TB \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> <dt>

[**TB \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

 





