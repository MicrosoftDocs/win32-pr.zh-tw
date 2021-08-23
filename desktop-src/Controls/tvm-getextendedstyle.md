---
title: 'TVM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項的延伸樣式。 明確地傳送此訊息，或使用 TreeView \_ GetExtendedStyle 宏。
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- TVM_GETEXTENDEDSTYLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93eb22b3dfdbe05365d28a7c93bfa9df3619796f9b4ae9ec603c74da252c5a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834198"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a>TVM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) 

抓取樹狀檢視控制項的延伸樣式。 明確地傳送此訊息，或使用 [**TreeView \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回擴充樣式的值。如需樣式的詳細資訊，請參閱 [樹狀檢視控制項擴充樣式](tree-view-control-window-extended-styles.md)。

## <a name="remarks"></a>備註

樹狀檢視控制項的擴充樣式與函數 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 或函數 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)所使用的擴充樣式沒有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

