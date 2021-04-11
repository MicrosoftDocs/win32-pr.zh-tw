---
title: 'TVM_SELECTITEM 訊息 (Commctrl .h) '
description: 選取指定的樹狀檢視專案、將專案滾動到視圖，或是以用來表示拖放作業目標的樣式來重繪專案。
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- TVM_SELECTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843244"
---
# <a name="tvm_selectitem-message"></a><span data-ttu-id="92988-104">TVM \_ SELECTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="92988-104">TVM\_SELECTITEM message</span></span>

<span data-ttu-id="92988-105">選取指定的樹狀檢視專案、將專案滾動到視圖，或是以用來表示拖放作業目標的樣式來重繪專案。</span><span class="sxs-lookup"><span data-stu-id="92988-105">Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation.</span></span> <span data-ttu-id="92988-106">您可以明確地傳送此訊息，或使用 [**treeview \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select)、 [**treeview \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)或 [**treeview \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="92988-106">You can send this message explicitly or by using the [**TreeView\_Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem), or [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="92988-107">參數</span><span class="sxs-lookup"><span data-stu-id="92988-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92988-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92988-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92988-109">動作旗標。</span><span class="sxs-lookup"><span data-stu-id="92988-109">Action flag.</span></span> <span data-ttu-id="92988-110">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="92988-110">This parameter can be one of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="92988-111">值</span><span class="sxs-lookup"><span data-stu-id="92988-111">Value</span></span></th>
<th><span data-ttu-id="92988-112">意義</span><span class="sxs-lookup"><span data-stu-id="92988-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <span data-ttu-id="92988-113"><dt><strong>TVGN_CARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="92988-113"><dt><strong>TVGN_CARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="92988-114">將選取範圍設定為指定的專案。</span><span class="sxs-lookup"><span data-stu-id="92988-114">Sets the selection to the specified item.</span></span> <span data-ttu-id="92988-115">樹狀檢視控制項的父視窗會接收 <a href="tvn-selchanging.md">TVN_SELCHANGING</a> 並 <a href="tvn-selchanged.md">TVN_SELCHANGED</a> 通知碼。</span><span class="sxs-lookup"><span data-stu-id="92988-115">The tree-view control's parent window receives the <a href="tvn-selchanging.md">TVN_SELCHANGING</a> and <a href="tvn-selchanged.md">TVN_SELCHANGED</a> notification codes.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <span data-ttu-id="92988-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="92988-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="92988-117">以用來表示拖放作業目標的樣式來重繪指定的專案。</span><span class="sxs-lookup"><span data-stu-id="92988-117">Redraws the specified item in the style used to indicate the target of a drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <span data-ttu-id="92988-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="92988-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="92988-119">確定指定的專案是可見的，如果可能的話，會將它顯示在控制項視窗的頂端。</span><span class="sxs-lookup"><span data-stu-id="92988-119">Ensures that the specified item is visible, and, if possible, displays it at the top of the control's window.</span></span> <span data-ttu-id="92988-120">樹狀檢視控制項會在視窗中顯示任意數量的專案。</span><span class="sxs-lookup"><span data-stu-id="92988-120">Tree-view controls display as many items as will fit in the window.</span></span> <span data-ttu-id="92988-121">如果指定的專案位於控制項階層專案的底部附近，它可能不會成為第一個可見的專案，視視窗中容納的專案數目而定。</span><span class="sxs-lookup"><span data-stu-id="92988-121">If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <span data-ttu-id="92988-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="92988-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="92988-123">選取單一專案時，會確保 treeview 不會展開該專案的子系。</span><span class="sxs-lookup"><span data-stu-id="92988-123">When a single item is selected, ensures that the treeview does not expand the children of that item.</span></span> <span data-ttu-id="92988-124">只有搭配 TVGN_CARET 旗標使用時才有效。</span><span class="sxs-lookup"><span data-stu-id="92988-124">This is valid only if used with the TVGN_CARET flag.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="92988-125">若要使用此旗標，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="92988-125">To use this flag, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="92988-126">如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。</span><span class="sxs-lookup"><span data-stu-id="92988-126">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="92988-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92988-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92988-128">專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="92988-128">Handle to an item.</span></span> <span data-ttu-id="92988-129">如果 *lParam* 為 **Null**，則控制項設定為沒有選取的專案。</span><span class="sxs-lookup"><span data-stu-id="92988-129">If *lParam* is **NULL**, the control is set to have no selected item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92988-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="92988-130">Return value</span></span>

<span data-ttu-id="92988-131">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="92988-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="92988-132">備註</span><span class="sxs-lookup"><span data-stu-id="92988-132">Remarks</span></span>

<span data-ttu-id="92988-133">如果指定的專案是折迭父項目的子系，則會展開父代的子專案清單，以顯示指定的專案。</span><span class="sxs-lookup"><span data-stu-id="92988-133">If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item.</span></span> <span data-ttu-id="92988-134">在此情況下，控制項的父視窗會收到 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 和 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="92988-134">In this case, the control's parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

<span data-ttu-id="92988-135">使用 [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)宏相當於將 *wParam* 設定為 TVGN 插入號值的 **TVM \_ SelectItem** 訊息傳送 \_ 。</span><span class="sxs-lookup"><span data-stu-id="92988-135">Using the [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_CARET value.</span></span> <span data-ttu-id="92988-136">使用 [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget)宏相當於將 *wParam* 設定為 TVGN DROPHILITE 值的 **TVM \_ SELECTITEM** 訊息傳送 \_ 。</span><span class="sxs-lookup"><span data-stu-id="92988-136">Using the [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_DROPHILITE value.</span></span> <span data-ttu-id="92988-137">使用 [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible)相當於將 *wParam* 設定為 TVGN FIRSTVISIBLE 值的 **TVM \_ SELECTITEM** 訊息傳送 \_ 。</span><span class="sxs-lookup"><span data-stu-id="92988-137">Using [**TreeView\_SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_FIRSTVISIBLE value.</span></span>

## <a name="requirements"></a><span data-ttu-id="92988-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="92988-138">Requirements</span></span>



| <span data-ttu-id="92988-139">需求</span><span class="sxs-lookup"><span data-stu-id="92988-139">Requirement</span></span> | <span data-ttu-id="92988-140">值</span><span class="sxs-lookup"><span data-stu-id="92988-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92988-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92988-141">Minimum supported client</span></span><br/> | <span data-ttu-id="92988-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92988-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92988-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92988-143">Minimum supported server</span></span><br/> | <span data-ttu-id="92988-144">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92988-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92988-145">標頭</span><span class="sxs-lookup"><span data-stu-id="92988-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="92988-146"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="92988-146"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





