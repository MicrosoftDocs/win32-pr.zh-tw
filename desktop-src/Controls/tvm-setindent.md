---
title: 'TVM_SETINDENT 訊息 (Commctrl .h) '
description: 為樹狀檢視控制項設定縮排的寬度，並重新繪製控制項以反映新的寬度。 您可以使用 TreeView SetIndent 宏明確地傳送此訊息 \_ 。
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538a89439909afe346ae8776d31a2104c7f6014664a33bdd3864bf43b0387e80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669663"
---
# <a name="tvm_setindent-message"></a>TVM \_ SETINDENT 訊息

為樹狀檢視控制項設定縮排的寬度，並重新繪製控制項以反映新的寬度。 您可以使用 [**TreeView \_ SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

縮排的寬度（以圖元為單位）。 如果這個參數小於系統定義的最小寬度，則新寬度會設定為系統定義的最小值。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

系統定義的最小縮排值通常是五個圖元，但不是固定的。 若要在特定系統上取得最小縮排的確切值，請傳送 **TVM \_ SETINDENT** 訊息，其中 *wParam* 設定為零。 然後傳送 [**TVM \_ setindent**](tvm-getindent.md) 訊息來取得最小縮排值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TreeView \_ SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





