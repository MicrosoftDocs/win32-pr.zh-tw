---
title: 'EM_FILELINEINDEX 訊息 (CommCtrl .h) '
description: 取得多行編輯控制項中指定行第一個字元的字元索引，與螢幕上的線條顯示方式無關。
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c4bd1f21ee6bcdf7bec56828ea9c2996c837def614c0c537ef83ee053ebfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915608"
---
# <a name="em_filelineindex-message-commctrlh"></a>EM_FILELINEINDEX 訊息 (CommCtrl .h) 

取得多行編輯控制項中指定行第一個字元的字元索引，與螢幕上的線條顯示方式無關。 字元索引是編輯控制項開頭的字元之以零為起始的索引。

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

傳回值是 *wParam* 參數中指定之線條的字元索引，與螢幕上的線條顯示方式無關，或者，如果指定的行號大於編輯控制項中的行數，則為-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限 1809 desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2019 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ FILELINEFROMCHAR**](em-filelinefromchar.md)
</dt> </dl>

 

 





