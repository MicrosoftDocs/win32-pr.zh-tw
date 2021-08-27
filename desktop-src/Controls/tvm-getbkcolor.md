---
title: 'TVM_GETBKCOLOR 訊息 (Commctrl .h) '
description: 抓取控制項目前的背景色彩。 您可以使用 TreeView GetBkColor 宏明確地傳送此訊息 \_ 。
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a5a6530b1aada1fab06c0b353d7ead666e61f0f796b890d1f5c56fe0be094b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088448"
---
# <a name="tvm_getbkcolor-message"></a>TVM \_ GETBKCOLOR 訊息

抓取控制項目前的背景色彩。 您可以使用 [**TreeView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回代表目前背景色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。 如果這個值是-1，表示控制項使用背景色彩的系統色彩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETBKCOLOR**](tvm-setbkcolor.md)
</dt> </dl>

 

