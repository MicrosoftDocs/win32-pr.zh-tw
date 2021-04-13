---
title: 'WM_UNDO 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 復原訊息傳送至編輯控制項，以復原最後一個作業。 將此訊息傳送至編輯控制項時，會還原先前刪除的文字，或刪除先前加入的文字。
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- WM_UNDO message Windows 控制項
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465848"
---
# <a name="wm_undo-message"></a>WM \_ 復原訊息

應用程式會將 **WM \_ 復原** 訊息傳送至編輯控制項，以復原最後一個作業。 將此訊息傳送至編輯控制項時，會還原先前刪除的文字，或刪除先前加入的文字。

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

如果訊息成功，則傳回值為 **TRUE**。

如果訊息失敗，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

**Rich Edit：** 建議使用 [**EM \_ 復原**](em-undo.md) ，而不是使用 **WM \_ 復原**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**其他資源**
</dt> <dt>

[**WM \_ 清除**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**WM \_ 複製**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**WM \_ 剪下**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**WM \_ 貼上**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

