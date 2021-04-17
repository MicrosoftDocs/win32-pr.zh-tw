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
# <a name="tvm_expand-message"></a><span data-ttu-id="99be0-105">TVM \_ 展開訊息</span><span class="sxs-lookup"><span data-stu-id="99be0-105">TVM\_EXPAND message</span></span>

<span data-ttu-id="99be0-106">**TVM \_ 展開** 訊息會展開或折迭與指定的父專案相關聯的子專案清單（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="99be0-106">The **TVM\_EXPAND** message expands or collapses the list of child items associated with the specified parent item, if any.</span></span> <span data-ttu-id="99be0-107">您可以明確地傳送此訊息，或使用 [**TreeView \_ Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="99be0-107">You can send this message explicitly or by using the [**TreeView\_Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="99be0-108">參數</span><span class="sxs-lookup"><span data-stu-id="99be0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99be0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99be0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99be0-110">動作旗標。</span><span class="sxs-lookup"><span data-stu-id="99be0-110">Action flag.</span></span> <span data-ttu-id="99be0-111">這個參數可以是下列其中一個或多個值：</span><span class="sxs-lookup"><span data-stu-id="99be0-111">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="99be0-112">值</span><span class="sxs-lookup"><span data-stu-id="99be0-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="99be0-113">意義</span><span class="sxs-lookup"><span data-stu-id="99be0-113">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <span data-ttu-id="99be0-114"><dt>**TVE \_ 折迭**</dt></span><span class="sxs-lookup"><span data-stu-id="99be0-114"><dt>**TVE\_COLLAPSE**</dt></span></span> </dl>                | <span data-ttu-id="99be0-115">折迭清單。</span><span class="sxs-lookup"><span data-stu-id="99be0-115">Collapses the list.</span></span> <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <span data-ttu-id="99be0-116"><dt>**TVE \_ COLLAPSERESET**</dt></span><span class="sxs-lookup"><span data-stu-id="99be0-116"><dt>**TVE\_COLLAPSERESET**</dt></span></span> </dl> | <span data-ttu-id="99be0-117">折迭清單並移除子專案。</span><span class="sxs-lookup"><span data-stu-id="99be0-117">Collapses the list and removes the child items.</span></span> <span data-ttu-id="99be0-118">已重設 [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) 狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="99be0-118">The [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is reset.</span></span> <span data-ttu-id="99be0-119">此旗標必須與 TVE 折迭旗標搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="99be0-119">This flag must be used with the TVE\_COLLAPSE flag.</span></span><br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <span data-ttu-id="99be0-120"><dt>**TVE \_ 展開**</dt></span><span class="sxs-lookup"><span data-stu-id="99be0-120"><dt>**TVE\_EXPAND**</dt></span></span> </dl>                      | <span data-ttu-id="99be0-121">展開清單。</span><span class="sxs-lookup"><span data-stu-id="99be0-121">Expands the list.</span></span><br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <span data-ttu-id="99be0-122"><dt>**TVE \_ EXPANDPARTIAL**</dt></span><span class="sxs-lookup"><span data-stu-id="99be0-122"><dt>**TVE\_EXPANDPARTIAL**</dt></span></span> </dl> | <span data-ttu-id="99be0-123">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="99be0-123">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="99be0-124">部分展開清單。</span><span class="sxs-lookup"><span data-stu-id="99be0-124">Partially expands the list.</span></span> <span data-ttu-id="99be0-125">在此狀態下，子專案會顯示出來，且父專案的加號 (+) （表示可以展開）會隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="99be0-125">In this state the child items are visible and the parent item's plus sign (+), indicating that it can be expanded, is displayed.</span></span> <span data-ttu-id="99be0-126">此旗標必須與 TVE 展開旗標搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="99be0-126">This flag must be used in combination with the TVE\_EXPAND flag.</span></span><br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <span data-ttu-id="99be0-127"><dt>**TVE \_ 切換**</dt></span><span class="sxs-lookup"><span data-stu-id="99be0-127"><dt>**TVE\_TOGGLE**</dt></span></span> </dl>                      | <span data-ttu-id="99be0-128">如果已展開，則會折迭清單或展開清單。</span><span class="sxs-lookup"><span data-stu-id="99be0-128">Collapses the list if it is expanded or expands it if it is collapsed.</span></span><br/>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="99be0-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99be0-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99be0-130">要展開或折迭之父專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="99be0-130">Handle to the parent item to expand or collapse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99be0-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="99be0-131">Return value</span></span>

<span data-ttu-id="99be0-132">如果作業成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="99be0-132">Returns nonzero if the operation was successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="99be0-133">備註</span><span class="sxs-lookup"><span data-stu-id="99be0-133">Remarks</span></span>

<span data-ttu-id="99be0-134">展開已展開的節點會被視為成功的作業，而 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="99be0-134">Expanding a node that is already expanded is considered a successful operation and [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns a nonzero value.</span></span> <span data-ttu-id="99be0-135">如果節點已折迭，則折迭節點會傳回零;否則，它會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="99be0-135">Collapsing a node returns zero if the node is already collapsed; otherwise it returns nonzero.</span></span> <span data-ttu-id="99be0-136">嘗試展開或折迭沒有子系的節點會被視為失敗，而 **SendMessage** 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="99be0-136">Attempting to expand or collapse a node that has no children is considered a failure and **SendMessage** returns zero.</span></span>

<span data-ttu-id="99be0-137">當專案第一次由 **TVM \_ 展開** 訊息展開時，此動作會產生 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 和 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md) 通知碼，並設定專案的 [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) 狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="99be0-137">When an item is first expanded by a **TVM\_EXPAND** message, the action generates [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes and the item's [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is set.</span></span> <span data-ttu-id="99be0-138">只要保持設定此狀態旗標，後續 **TVM \_ 展開** 訊息不會產生 IZDEBSKI \_ ITEMEXPANDING 或 izdebski \_ ITEMEXPANDED 通知。</span><span class="sxs-lookup"><span data-stu-id="99be0-138">As long as this state flag remains set, subsequent **TVM\_EXPAND** messages do not generate TVN\_ITEMEXPANDING or TVN\_ITEMEXPANDED notifications.</span></span> <span data-ttu-id="99be0-139">若要重設 **TVIS \_ EXPANDEDONCE** state 旗標，您必須傳送具有 TVE COLLAPSE 和 TVE COLLAPSERESET 旗標集的 **TVM \_ EXPAND** 訊息 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="99be0-139">To reset the **TVIS\_EXPANDEDONCE** state flag, you must send a **TVM\_EXPAND** message with the TVE\_COLLAPSE and TVE\_COLLAPSERESET flags set.</span></span> <span data-ttu-id="99be0-140">嘗試明確設定 **TVIS \_ EXPANDEDONCE** 將會導致無法預期的行為。</span><span class="sxs-lookup"><span data-stu-id="99be0-140">Attempting to explicitly set **TVIS\_EXPANDEDONCE** will result in unpredictable behavior.</span></span>

<span data-ttu-id="99be0-141">如果 treeview 控制項的擁有者拒絕回應 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 通知的作業，則展開作業可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="99be0-141">The expand operation may fail if the owner of the treeview control denies the operation in response to a [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="99be0-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="99be0-142">Requirements</span></span>



| <span data-ttu-id="99be0-143">需求</span><span class="sxs-lookup"><span data-stu-id="99be0-143">Requirement</span></span> | <span data-ttu-id="99be0-144">值</span><span class="sxs-lookup"><span data-stu-id="99be0-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99be0-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99be0-145">Minimum supported client</span></span><br/> | <span data-ttu-id="99be0-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99be0-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99be0-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99be0-147">Minimum supported server</span></span><br/> | <span data-ttu-id="99be0-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99be0-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99be0-149">標頭</span><span class="sxs-lookup"><span data-stu-id="99be0-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="99be0-150"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="99be0-150"><dt>Commctrl.h</dt></span></span> </dl> |



 

