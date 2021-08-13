---
title: 'TVM_GETTEXTCOLOR 訊息 (Commctrl .h) '
description: 抓取控制項目前的文字色彩。 您可以使用 TreeView GetTextColor 宏明確地傳送此訊息 \_ 。
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- TVM_GETTEXTCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a578753b6f86d2ceaa6a664fe6e6e0ff88475dccfb953ae6c6f652bc2dffbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669709"
---
# <a name="tvm_gettextcolor-message"></a>TVM \_ GETTEXTCOLOR 訊息

抓取控制項目前的文字色彩。 您可以使用 [**TreeView \_ GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回代表目前文字色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。 如果這個值是-1，表示控制項使用的是文字色彩的系統色彩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md)
</dt> </dl>

 

