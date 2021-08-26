---
title: 'EM_CALLAUTOCORRECTPROC 訊息 (Richedit .h) '
description: 呼叫由 EM SETAUTOCORRECTPROC 訊息儲存的自動校正回呼函式 \_ （假設插入點前面的文字是自動校正的候選項）。
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad76ec66018b4e673913c433ce16a1294944f69c9d33a5dbaedb85ba21f985a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916078"
---
# <a name="em_callautocorrectproc-message"></a>EM \_ CALLAUTOCORRECTPROC 訊息

呼叫由 [**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md) 訊息儲存的自動校正回呼函式（假設插入點前面的文字是自動校正的候選項）。


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**WCHAR** 類型的字元。 如果此字元是 (U + 0009) 的索引標籤，而插入點前面的字元不是索引標籤，則插入點前面的字元會被視為自動校正候選字串的一部分，而不是字串分隔符號;否則， *wParam* 不會有任何作用。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值為零，如果發生錯誤則傳回非零值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ GETAUTOCORRECTPROC**](em-getautocorrectproc.md)
</dt> <dt>

[**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)
</dt> </dl>

 

 





