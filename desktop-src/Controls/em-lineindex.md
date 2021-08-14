---
title: 'EM_LINEINDEX 訊息 (Winuser .h) '
description: 取得多行編輯控制項中指定行第一個字元的字元索引。
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_LINEINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 223208b2f9a31dcc1d81d6811aab32210adedbeb807eb0cdbef8c53ec853ab04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171397"
---
# <a name="em_lineindex-message-winuserh"></a>EM_LINEINDEX 訊息 (Winuser .h) 

取得多行編輯控制項中指定行第一個字元的字元索引。 字元索引是編輯控制項開頭的字元之以零為起始的索引。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的行號。 值-1 會指定包含插入號)  (行的目前行號。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 *wParam* 參數中指定之行的字元索引，如果指定的行號大於編輯控制項中的行數，則為-1。

## <a name="remarks"></a>備註

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ LINEFROMCHAR**](em-linefromchar.md)
</dt> </dl>

 

 





