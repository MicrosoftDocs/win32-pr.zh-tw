---
title: 'EM_REDO 訊息 (Richedit .h) '
description: 將 EM \_ 重做訊息傳送至 rich edit 控制項，以重做控制項的重做佇列中的下一個動作。
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39b679e8bf7e78cf7ce028d0bb440438770d0d0123516313fb418b2136ebc11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437858"
---
# <a name="em_redo-message"></a>EM \_ 重做訊息

將 **EM \_ 重做** 訊息傳送至 rich edit 控制項，以重做控制項的重做佇列中的下一個動作。

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

如果 **重做** 作業成功，則傳回值為非零值。

如果 **重做** 作業失敗，則傳回值為零。

## <a name="remarks"></a>備註

若要判斷控制項的重做佇列中是否有任何動作，請傳送 [**EM \_ CANREDO**](em-canredo.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ 復原**](em-undo.md)
</dt> </dl>

 

 





