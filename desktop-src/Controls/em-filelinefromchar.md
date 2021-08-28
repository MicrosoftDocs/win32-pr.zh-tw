---
title: 'EM_FILELINEFROMCHAR 訊息 (CommCtrl .h) '
description: 取得在多行編輯控制項中包含指定字元索引的行索引，與螢幕上的線條顯示方式無關。
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_FILELINEFROMCHAR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d238117a9f2ba18ae838eec32d7dc2fa12ba0833f9cdee54ce2d1a2c998944
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915628"
---
# <a name="em_filelinefromchar-message"></a>EM \_ FILELINEFROMCHAR 訊息

取得在多行編輯控制項中包含指定字元索引的行索引，與螢幕上的線條顯示方式無關。 字元索引是編輯控制項開頭的字元之以零為起始的索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出其數位的行中所含字元的字元索引。 如果此參數為-1， **EM \_ FILELINEFROMCHAR** 會抓取目前行的行號， (包含插入號) 的行號，或者，如果有選取範圍，則為包含選取範圍開頭之行的行號。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是行的以零為起始的行號，其中包含 *wParam* 指定的字元索引，與螢幕上的線條顯示方式無關。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限 1809 desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2019 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





