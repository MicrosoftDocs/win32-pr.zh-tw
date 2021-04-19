---
title: 'TVM_GETBKCOLOR 訊息 (Commctrl .h) '
description: 抓取控制項目前的背景色彩。 您可以使用 TreeView GetBkColor 宏明確地傳送此訊息 \_ 。
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR message Windows 控制項
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
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966140"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETBKCOLOR**](tvm-setbkcolor.md)
</dt> </dl>

 

