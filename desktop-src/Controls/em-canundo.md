---
title: 'EM_CANUNDO 訊息 (Winuser .h) '
description: 判斷是否在編輯控制項的復原佇列中有任何動作。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- EM_CANUNDO message Windows 控制項
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104502"
---
# <a name="em_canundo-message"></a>EM \_ CANUNDO 訊息

判斷是否在編輯控制項的復原佇列中有任何動作。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

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

如果控制項的復原佇列中有動作，傳回值為非零值。

如果恢復佇列是空的，則傳回值為零。

## <a name="remarks"></a>備註

如果復原佇列不是空的，您可以將 [**EM \_ 復原**](em-undo.md) 訊息傳送至控制項，以復原最近的作業。

**編輯控制項和 Rich edit 1.0：** 復原佇列只會包含最新的作業。

**Rich Edit 2.0 和更新版本：** 復原佇列可以包含多個作業。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ 復原**](em-undo.md)
</dt> </dl>

 

 





