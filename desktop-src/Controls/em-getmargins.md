---
title: 'EM_GETMARGINS 訊息 (Winuser .h) '
description: 取得編輯控制項左邊界和右邊界的寬度。
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- EM_GETMARGINS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33746bc44a7b1b0aadd11c573675fedd51e565a557da7601ebe35a4442ddc96c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541068"
---
# <a name="em_getmargins-message"></a>EM \_ GETMARGINS 訊息

取得編輯控制項左邊界和右邊界的寬度。

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

傳回 LOWORD 中左邊界的寬度，以及 HIWORD 中右邊界的寬度。

## <a name="remarks"></a>備註

**Rich Edit：** 不支援 **EM \_ GETMARGINS** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETMARGINS**](em-setmargins.md)
</dt> </dl>

 

 





