---
title: 'EM_GETCTFMODEBIAS 訊息 (Richedit .h) '
description: 取得 Microsoft Rich Edit 控制項的文字服務架構模式偏差值。
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- EM_GETCTFMODEBIAS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d6e030e3080ec9bf3d801583b9ade182483ba8560b3eccb2fb9813be7d39cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019746"
---
# <a name="em_getctfmodebias-message"></a>EM \_ GETCTFMODEBIAS 訊息

取得 Microsoft Rich Edit 控制項的文字服務架構模式偏差值。

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

目前的文字服務架構模式偏差值。

## <a name="remarks"></a>備註

若要取得 IME 模式偏差，請呼叫 [**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> <dt>

[**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md)
</dt> </dl>

 

 





