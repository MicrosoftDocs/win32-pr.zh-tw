---
title: 'EM_PASTESPECIAL 訊息 (Richedit .h) '
description: 在 rich edit 控制項中貼上特定的剪貼簿格式。
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- EM_PASTESPECIAL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc1af4dd0566cdf8e256b34f87fcc52ea855bc521c87cbe390e02b8b1cf7b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412799"
---
# <a name="em_pastespecial-message"></a>EM \_ PASTESPECIAL 訊息

在 rich edit 控制項中貼上特定的剪貼簿格式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定 [剪貼簿格式](/windows/desktop/dataxchg/clipboard-formats)。

</dd> <dt>

*lParam* 
</dt> <dd>

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)結構的指標或 **Null**。 如果要貼上物件，則會以所需的顯示外觀填入 **REPASTESPECIAL** 結構。 如果 *lParam* 為 **Null** 或 **dwAspect** 成員為零，則使用的顯示外觀將會是物件描述項的內容。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

