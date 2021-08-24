---
title: 'EM_LINEFROMCHAR 訊息 (Winuser .h) '
description: 取得在多行編輯控制項中包含指定之字元索引的行索引。
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_LINEFROMCHAR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcbffff68ecafec2202c78f0707556508ed34d173647cccacc4b90f1658f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006283"
---
# <a name="em_linefromchar-message"></a>EM \_ LINEFROMCHAR 訊息

取得在多行編輯控制項中包含指定之字元索引的行索引。 字元索引是編輯控制項開頭的字元之以零為起始的索引。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出其數位的行中所含字元的字元索引。 如果此參數為-1， **EM \_ LINEFROMCHAR** 會抓取目前行的行號， (包含插入號) 的行號，或者，如果有選取範圍，則為包含選取範圍開頭之行的行號。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是行的以零為起始的行號，包含 *wParam* 所指定的字元索引。

## <a name="remarks"></a>備註

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如果字元索引大於64000，請使用 [**EM \_ EXLINEFROMCHAR**](em-exlinefromchar.md) 訊息。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ EXLINEFROMCHAR**](em-exlinefromchar.md)
</dt> <dt>

[**EM \_ LINEINDEX**](em-lineindex.md)
</dt> </dl>

 

 





