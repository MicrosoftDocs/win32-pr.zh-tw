---
title: 'EM_SETHYPHENATEINFO 訊息 (Richedit .h) '
description: 設定 rich edit 控制項進行斷字的方式。
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844128"
---
# <a name="em_sethyphenateinfo-message"></a>EM \_ SETHYPHENATEINFO 訊息

設定 rich edit 控制項進行斷字的方式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo)結構的指標。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用，必須為零。

</dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> 若要啟用斷字功能，用戶端必須呼叫 [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)，並指定 \_ ADVANCEDTYPOGRAPHY。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETHYPHENATEINFO**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





