---
title: 'TVM_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定控制項的背景色彩。 您可以使用 TreeView SetBkColor 宏明確地傳送此訊息 \_ 。
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- TVM_SETBKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0609a15be2b8e05b1f8ca8f4f999cd4888ee946969c25f5bc1d86420b7529f2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060118"
---
# <a name="tvm_setbkcolor-message"></a>TVM \_ SETBKCOLOR 訊息

設定控制項的背景色彩。 您可以使用 [**TreeView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) 值，其中包含新的背景色彩。 如果這個值是-1，控制項將會還原為使用背景色彩的系統色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回表示先前背景色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。 如果這個值是-1，表示控制項使用的是背景色彩的系統色彩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ GETBKCOLOR**](tvm-getbkcolor.md)
</dt> </dl>

 

