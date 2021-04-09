---
title: 'TVM_SETTEXTCOLOR 訊息 (Commctrl .h) '
description: 設定控制項的文字色彩。 您可以使用 TreeView SetTextColor 宏明確地傳送此訊息 \_ 。
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- TVM_SETTEXTCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686032"
---
# <a name="tvm_settextcolor-message"></a>TVM \_ SETTEXTCOLOR 訊息

設定控制項的文字色彩。 您可以使用 [**TreeView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) 值，其中包含新的文字色彩。 如果這個引數是-1，則控制項會還原為使用文字色彩的系統色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回表示先前文字色彩的 **COLORREF** 值。 如果這個值是-1，表示控制項使用的是文字色彩的系統色彩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md)
</dt> </dl>

 

