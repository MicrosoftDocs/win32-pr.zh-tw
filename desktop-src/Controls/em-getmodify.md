---
title: 'EM_GETMODIFY 訊息 (Winuser .h) '
description: 取得編輯控制項之修改旗標的狀態。 旗標會指出編輯控制項的內容是否已修改。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34156e363824e975af68449b40ed639eeeb7e3ab76bd680b9837f3d3dd907537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048898"
---
# <a name="em_getmodify-message"></a>EM \_ GETMODIFY 訊息

取得編輯控制項之修改旗標的狀態。 旗標會指出編輯控制項的內容是否已修改。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

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

如果編輯控制項的內容已修改，則傳回值為非零。否則，它是零。

## <a name="remarks"></a>備註

建立控制項時，系統會自動將修改旗標清除為零。 如果使用者變更控制項的文字，系統會將旗標設定為非零。 您可以將 [**EM \_ SETMODIFY**](em-setmodify.md) 訊息傳送至編輯控制項，以設定或清除旗標。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETMODIFY**](em-setmodify.md)
</dt> </dl>

 

 





