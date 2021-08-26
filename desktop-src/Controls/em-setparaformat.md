---
title: 'EM_SETPARAFORMAT 訊息 (Richedit .h) '
description: 設定 rich edit 控制項中目前選取範圍的段落格式。
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- EM_SETPARAFORMAT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db0ba4e4bf505c5fb1b746b84cae71dcc621635a0a33b4a533ce8551486fe6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062908"
---
# <a name="em_setparaformat-message"></a>EM \_ SETPARAFORMAT 訊息

設定 rich edit 控制項中目前選取範圍的段落格式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)結構的指標，指定新段落格式化屬性。 只有 **dwMask** 成員所指定的屬性才會變更。

Microsoft Rich Edit 2.0 和更新版本：此參數可以是 [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) 結構的指標，也就是 [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) 結構的延伸。 傳送 **EM \_ SETPARAFORMAT** 訊息之前，請先設定結構的 **cbSize** 成員來指出結構的版本。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為非零值。

如果作業失敗，則傳回值為零。

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

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





