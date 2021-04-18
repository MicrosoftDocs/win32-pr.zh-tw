---
title: 'TVM_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項所使用之子工具提示控制項的控制碼。 您可以使用 TreeView GetToolTips 宏明確地傳送此訊息 \_ 。
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- TVM_GETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464761"
---
# <a name="tvm_gettooltips-message"></a>TVM \_ GETTOOLTIPS 訊息

抓取樹狀檢視控制項所使用之子工具提示控制項的控制碼。 您可以使用 [**TreeView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回子工具提示控制項的控制碼，如果控制項不使用工具提示，則為 **Null** 。

## <a name="remarks"></a>備註

建立時，樹狀檢視控制項會自動建立子工具提示控制項。 若要讓樹狀檢視控制項不使用工具提示，請使用 [**tv \_ NOTOOLTIPS**](tree-view-control-window-styles.md) 樣式建立控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETTOOLTIPS**](tvm-settooltips.md)
</dt> </dl>

 

 





