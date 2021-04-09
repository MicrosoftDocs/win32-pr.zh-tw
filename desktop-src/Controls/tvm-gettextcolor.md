---
title: 'TVM_GETTEXTCOLOR 訊息 (Commctrl .h) '
description: 抓取控制項目前的文字色彩。 您可以使用 TreeView GetTextColor 宏明確地傳送此訊息 \_ 。
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- TVM_GETTEXTCOLOR message Windows 控制項
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
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024839"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md)
</dt> </dl>

 

