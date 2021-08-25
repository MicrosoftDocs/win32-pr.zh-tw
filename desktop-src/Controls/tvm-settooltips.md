---
title: 'TVM_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項的子工具提示控制項。 您可以使用 TreeView SetToolTips 宏明確地傳送此訊息 \_ 。
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- TVM_SETTOOLTIPS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd18a5217db0d105841722d208904c1b65199504750576acf1ff8035f31bd585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913958"
---
# <a name="tvm_settooltips-message"></a>TVM \_ SETTOOLTIPS 訊息

設定樹狀檢視控制項的子工具提示控制項。 您可以使用 [**TreeView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

工具提示控制項的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前針對樹狀檢視控制項設定之工具提示控制項的控制碼，如果先前未使用工具提示，則為 **Null** 。

## <a name="remarks"></a>備註

建立時，樹狀檢視控制項會自動建立子工具提示控制項。 若要防止樹狀檢視控制項使用工具提示，請使用 [**tv \_ NOTOOLTIPS**](tree-view-control-window-styles.md) 樣式建立控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ GETTOOLTIPS**](tvm-gettooltips.md)
</dt> </dl>

 

 





