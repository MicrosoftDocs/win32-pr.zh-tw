---
title: 'TVM_EXPAND 訊息 (Commctrl .h) '
description: TVM \_ 展開訊息會展開或折迭與指定的父專案相關聯的子專案清單（如果有的話）。 您可以明確地傳送此訊息，或使用 TreeView \_ Expand 宏來傳送。
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- TVM_EXPAND message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466488"
---
# <a name="tvm_expand-message"></a>TVM \_ 展開訊息

**TVM \_ 展開** 訊息會展開或折迭與指定的父專案相關聯的子專案清單（如果有的話）。 您可以明確地傳送此訊息，或使用 [**TreeView \_ Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

動作旗標。 這個參數可以是下列其中一個或多個值：



| 值                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <dt>**TVE \_ 折迭**</dt> </dl>                | 折迭清單。 <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <dt>**TVE \_ COLLAPSERESET**</dt> </dl> | 折迭清單並移除子專案。 已重設 [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) 狀態旗標。 此旗標必須與 TVE 折迭旗標搭配使用 \_ 。<br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <dt>**TVE \_ 展開**</dt> </dl>                      | 展開清單。<br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <dt>**TVE \_ EXPANDPARTIAL**</dt> </dl> | [版本 4.70](common-control-versions.md)。 部分展開清單。 在此狀態下，子專案會顯示出來，且父專案的加號 (+) （表示可以展開）會隨即顯示。 此旗標必須與 TVE 展開旗標搭配使用 \_ 。<br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <dt>**TVE \_ 切換**</dt> </dl>                      | 如果已展開，則會折迭清單或展開清單。<br/>                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

要展開或折迭之父專案的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

展開已展開的節點會被視為成功的作業，而 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 會傳回非零值。 如果節點已折迭，則折迭節點會傳回零;否則，它會傳回非零值。 嘗試展開或折迭沒有子系的節點會被視為失敗，而 **SendMessage** 會傳回零。

當專案第一次由 **TVM \_ 展開** 訊息展開時，此動作會產生 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 和 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md) 通知碼，並設定專案的 [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) 狀態旗標。 只要保持設定此狀態旗標，後續 **TVM \_ 展開** 訊息不會產生 IZDEBSKI \_ ITEMEXPANDING 或 izdebski \_ ITEMEXPANDED 通知。 若要重設 **TVIS \_ EXPANDEDONCE** state 旗標，您必須傳送具有 TVE COLLAPSE 和 TVE COLLAPSERESET 旗標集的 **TVM \_ EXPAND** 訊息 \_ \_ 。 嘗試明確設定 **TVIS \_ EXPANDEDONCE** 將會導致無法預期的行為。

如果 treeview 控制項的擁有者拒絕回應 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 通知的作業，則展開作業可能會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

