---
title: 'EM_SETBKGNDCOLOR 訊息 (Richedit .h) '
description: EM \_ SETBKGNDCOLOR 訊息會設定 rich edit 控制項的背景色彩。
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173c2da9f3c04e49211224bd269d79c0634e1cb3f8ea959f6b58e354fdf0dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412652"
---
# <a name="em_setbkgndcolor-message"></a>EM \_ SETBKGNDCOLOR 訊息

**EM \_ SETBKGNDCOLOR** 訊息會設定 rich edit 控制項的背景色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定是否使用系統色彩。 如果此參數為非零值，則背景會設定為視窗背景系統色彩。 否則，背景會設定為指定的色彩。

</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref)結構，指定 *wParam* 為零時的色彩。 若要產生 **COLORREF**，請使用 [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) 宏。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回原始的背景色彩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**其他資源**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

