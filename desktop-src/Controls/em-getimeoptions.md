---
title: 'EM_GETIMEOPTIONS 訊息 (Richedit .h) '
description: 抓取目前的輸入方法編輯器 (IME) 選項。
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- EM_GETIMEOPTIONS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4513189014969dbfdf69a0ad257cbfde6a4ff99c2499f478c4865100a23c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049058"
---
# <a name="em_getimeoptions-message"></a>EM \_ GETIMEOPTIONS 訊息

抓取目前的輸入方法編輯器 (IME) 選項。

> [!Note]  
> 只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。 任何較新版本的 Rich Edit 都不支援此功能。

 

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

此訊息會傳回 [**EM \_ SETIMEOPTIONS**](em-setimeoptions.md) 訊息中所述的一或多個 IME 選項旗標值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETIMEOPTIONS**](em-setimeoptions.md)
</dt> </dl>

 

 





