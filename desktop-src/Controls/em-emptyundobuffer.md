---
title: 'EM_EMPTYUNDOBUFFER 訊息 (Winuser .h) '
description: 重設編輯控制項的復原旗標。 每當編輯控制項內的作業可以復原時，就會設定 [復原] 旗標。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER message Windows 控制項
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465900"
---
# <a name="em_emptyundobuffer-message"></a>EM \_ EMPTYUNDOBUFFER 訊息

重設編輯控制項的復原旗標。 每當編輯控制項內的作業可以復原時，就會設定 [復原] 旗標。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

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

此訊息不會傳回值。

## <a name="remarks"></a>備註

每當編輯控制項收到 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 或 [**EM \_ SETHANDLE**](em-sethandle.md) 訊息時，就會自動重設復原旗標。

**編輯控制項和 Rich edit 1.0：** 控制項只能復原或重做最新的作業。

**Rich Edit 2.0 和更新版本：****EM \_ EMPTYUNDOBUFFER** 訊息會清空所有的復原和重做緩衝區。 Rich edit 控制項可讓使用者復原或重做多項作業。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ SETHANDLE**](em-sethandle.md)
</dt> <dt>

[**EM \_ 復原**](em-undo.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

