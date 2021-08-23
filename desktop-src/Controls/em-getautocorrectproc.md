---
title: 'EM_GETAUTOCORRECTPROC 訊息 (Richedit .h) '
description: 取得應用程式定義之 AutoCorrectProc 函數的指標。
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- EM_GETAUTOCORRECTPROC 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc6b5068c1e72c05d7a1b85ee02e57b788cf417f732fe3c2bab8c66d0dcf383
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541088"
---
# <a name="em_getautocorrectproc-message"></a>EM \_ GETAUTOCORRECTPROC 訊息

取得應用程式定義之 [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) 函數的指標。

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

傳回應用程式定義 [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) 函式的指標。

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

[**EM \_ CALLAUTOCORRECTPROC**](em-callautocorrectproc.md)
</dt> <dt>

[**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)
</dt> </dl>

 

 





