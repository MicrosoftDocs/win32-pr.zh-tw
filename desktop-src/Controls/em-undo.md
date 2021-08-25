---
title: 'EM_UNDO 訊息 (Winuser .h) '
description: 此訊息會復原控制項復原佇列中的最後一個編輯控制項作業。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- EM_UNDO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 452d82e6d0685314a79f1f95cff487ee3f52e2d1b70925c3e6e72f9263f442e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047918"
---
# <a name="em_undo-message"></a>EM \_ 復原訊息

此訊息會復原控制項復原佇列中的最後一個編輯控制項作業。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

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

針對單行編輯控制項，傳回值一律為 **TRUE**。

若為多行編輯控制項，如果復原作業成功，傳回值為 **TRUE** ; 如果復原作業失敗，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

**編輯控制項和 Rich edit 1.0：** 復原操作也可以復原。 例如，您可以使用第一次 **em \_ 復原** 訊息來還原已刪除的文字，並使用第二個 **em \_ 復原** 訊息再次移除文字，只要沒有任何中間的編輯作業。

**Rich Edit 2.0 和更新版本：** 復原功能是多層的，因此傳送兩個 **EM \_ 復原** 訊息將會復原復原佇列中的最後兩個作業。 若要重做作業，請傳送 [**EM \_ 重做**](em-redo.md) 訊息。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> </dl>

 

 





