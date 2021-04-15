---
title: 'EM_GETTEXTMODE 訊息 (Richedit .h) '
description: 取得 rich edit 控制項的目前文字模式和復原層級。
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- EM_GETTEXTMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466240"
---
# <a name="em_gettextmode-message"></a>EM \_ GETTEXTMODE 訊息

取得 rich edit 控制項的目前文字模式和復原層級。

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

傳回值是 [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) 列舉型別中的一或多個值。 這些值表示控制項目前的文字模式和復原層級。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ SETTEXTMODE**](em-settextmode.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





