---
title: 'EM_GETPASSWORDCHAR 訊息 (Winuser .h) '
description: 取得當使用者輸入文字時，編輯控制項所顯示的密碼字元。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844135"
---
# <a name="em_getpasswordchar-message"></a>EM \_ GETPASSWORDCHAR 訊息

取得當使用者輸入文字時，編輯控制項所顯示的密碼字元。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

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

傳回值會指定要顯示的字元，以取代使用者輸入的任何字元。 如果傳回值為 **Null**，則不會有密碼字元，而且控制項會顯示使用者輸入的字元。

## <a name="remarks"></a>備註

如果以 [**ES \_ 密碼**](edit-control-styles.md) 樣式建立編輯控制項，則預設密碼字元會設定為星號 (\*) 。 如果建立不含 **ES \_ 密碼** 樣式的編輯控制項，則不會有密碼字元。 若要變更密碼字元，請傳送 [**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md) 訊息。

**編輯控制項：** 多行編輯控制項不支援密碼樣式或訊息。

**Rich edit：** Microsoft Rich Edit 2.0 和更新版本支援。 單行和多行編輯控制項都支援密碼樣式和訊息。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md)
</dt> </dl>

 

 





