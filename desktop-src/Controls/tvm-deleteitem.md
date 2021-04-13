---
title: 'TVM_DELETEITEM 訊息 (Commctrl .h) '
description: 從樹狀檢視控制項中移除專案及其所有子系。 您可以使用 TreeView DeleteItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- TVM_DELETEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465465"
---
# <a name="tvm_deleteitem-message"></a>TVM \_ DELETEITEM 訊息

從樹狀檢視控制項中移除專案及其所有子系。 您可以使用 [**TreeView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

要刪除之專案的 **HTREEITEM** 控制碼。 如果 *lParam* 設定為 TVI \_ ROOT 或 **Null**，則會刪除所有專案。 您也可以使用 [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) 宏來刪除所有專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

您無法安全地刪除專案以回應通知，例如 [izdebski \_ SELCHANGING](tvn-selchanging.md)。

刪除專案之後，其控制碼無效且無法使用。

移除每個專案時，父視窗會收到 [izdebski \_ DELETEITEM](tvn-deleteitem.md) 通知碼。

如果正在編輯專案標籤，則會取消編輯作業，而且父視窗會收到 [izdebski \_ ENDLABELEDIT](tvn-endlabeledit.md) 通知碼。

如果您刪除具有 [**電視 \_ NOSCROLL**](tree-view-control-window-styles.md) 樣式之樹狀檢視控制項中的所有專案，則後續新增的專案可能無法正確顯示。 如需詳細資訊，請參閱 [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





