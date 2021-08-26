---
title: 'EM_LINESCROLL 訊息 (Winuser .h) '
description: 滾動多行編輯控制項中的文字。
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- EM_LINESCROLL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6da4adbd789a8d9ae3344a1a49d39c7f5fbe22b7ec1ca51fcc6cead98ea7780
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048638"
---
# <a name="em_linescroll-message"></a>EM \_ LINESCROLL 訊息

滾動多行編輯控制項中的文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**編輯控制項：** 要水準滾動的字元數。

**Rich edit 控制項：** 未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

垂直捲動的行數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息傳送至多行編輯控制項，則傳回值為 **TRUE**。

如果訊息傳送至單行編輯控制項，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

控制項不會在編輯控制項中的最後一行文字之前垂直捲動。 如果目前的行加上 *lParam* 參數所指定的行數超過編輯控制項中的行總數，則會調整此值，以便將編輯控制項的最後一行滾動至編輯控制項視窗的頂端。

**編輯控制項：****EM \_ LINESCROLL** 訊息會在多行編輯控制項中，以垂直或水準方式滾動文字。 **EM \_ LINESCROLL** 訊息可以用來將任何一行的最後一個字元水準滾動。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 **EM \_ LINESCROLL** 訊息會在多行編輯控制項中垂直捲動文字。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



 

 





