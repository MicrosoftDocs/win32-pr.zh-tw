---
title: 'EM_GETLIMITTEXT 訊息 (Winuser .h) '
description: 取得編輯控制項的目前文字限制。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- EM_GETLIMITTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2066bf03fd8ea05851a9cef58f4e308db49f82bdee94c2d503cadf1c20a2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831679"
---
# <a name="em_getlimittext-message"></a>EM \_ GETLIMITTEXT 訊息

取得編輯控制項的目前文字限制。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是文字限制。

## <a name="remarks"></a>備註

**編輯控制項、Rich Edit 2.0 和更新版本：** 文字限制是控制項可以包含的最大文字數量（以 **TCHAR** s 為限）。 若為 ANSI 文字，此為位元組數;若為 Unicode 文字，此為字元數。 兩份具有相同字元限制的檔將會產生相同的文字限制，即使其中一個是 ANSI，另一個則是 Unicode。

**Rich Edit 1.0：** 文字限制是 rich edit 控制項可以包含的最大文字數量（以位元組為單位）。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 





