---
title: 'TVM_GETNEXTITEM 訊息 (Commctrl .h) '
description: 抓取具有指定專案之指定關聯性的樹狀檢視專案。 您可以使用 TreeView GetNextItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- TVM_GETNEXTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099af5e9abcd3e9c144cfc615a12dd2acb0332b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094160"
---
# <a name="tvm_getnextitem-message"></a><span data-ttu-id="c6699-105">TVM \_ GETNEXTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="c6699-105">TVM\_GETNEXTITEM message</span></span>

<span data-ttu-id="c6699-106">抓取具有指定專案之指定關聯性的樹狀檢視專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-106">Retrieves the tree-view item that bears the specified relationship to a specified item.</span></span> <span data-ttu-id="c6699-107">您可以使用 [**TreeView \_ GetNextItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-107">You can send this message explicitly, by using the [**TreeView\_GetNextItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6699-108">參數</span><span class="sxs-lookup"><span data-stu-id="c6699-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6699-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6699-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6699-110">指定要取出之專案的旗標。</span><span class="sxs-lookup"><span data-stu-id="c6699-110">Flag specifying the item to retrieve.</span></span> <span data-ttu-id="c6699-111">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="c6699-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="c6699-112">值</span><span class="sxs-lookup"><span data-stu-id="c6699-112">Value</span></span>                                                                                                                                                                              | <span data-ttu-id="c6699-113">意義</span><span class="sxs-lookup"><span data-stu-id="c6699-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <span data-ttu-id="c6699-114"><dt>**TVGN \_ 插入號**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-114"><dt>**TVGN\_CARET**</dt></span></span> </dl>                               | <span data-ttu-id="c6699-115">抓取目前選取的專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-115">Retrieves the currently selected item.</span></span> <span data-ttu-id="c6699-116">您可以使用 [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-116">You can use the [**TreeView\_GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) macro to send this message.</span></span><br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <span data-ttu-id="c6699-117"><dt>**TVGN \_ 子系**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-117"><dt>**TVGN\_CHILD**</dt></span></span> </dl>                               | <span data-ttu-id="c6699-118">抓取 *hitem* 參數所指定之專案的第一個子專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-118">Retrieves the first child item of the item specified by the *hitem* parameter.</span></span> <span data-ttu-id="c6699-119">您可以使用 [**TreeView \_ system.windows.media.visualtreehelper.getchild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-119">You can use the [**TreeView\_GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) macro to send this message.</span></span><br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <span data-ttu-id="c6699-120"><dt>**TVGN \_ DROPHILITE**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-120"><dt>**TVGN\_DROPHILITE**</dt></span></span> </dl>                | <span data-ttu-id="c6699-121">抓取做為拖放作業之目標的專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-121">Retrieves the item that is the target of a drag-and-drop operation.</span></span> <span data-ttu-id="c6699-122">您可以使用 [**TreeView \_ GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-122">You can use the [**TreeView\_GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) macro to send this message.</span></span><br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <span data-ttu-id="c6699-123"><dt>**TVGN \_ FIRSTVISIBLE**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-123"><dt>**TVGN\_FIRSTVISIBLE**</dt></span></span> </dl>          | <span data-ttu-id="c6699-124">抓取樹狀檢視視窗中可見的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-124">Retrieves the first item that is visible in the tree-view window.</span></span> <span data-ttu-id="c6699-125">您可以使用 [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-125">You can use the [**TreeView\_GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) macro to send this message.</span></span><br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <span data-ttu-id="c6699-126"><dt>**TVGN \_ LASTVISIBLE**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-126"><dt>**TVGN\_LASTVISIBLE**</dt></span></span> </dl>             | <span data-ttu-id="c6699-127">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="c6699-127">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="c6699-128">抓取樹狀結構中最後展開的專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-128">Retrieves the last expanded item in the tree.</span></span> <span data-ttu-id="c6699-129">這不會取出樹狀檢視視窗中顯示的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-129">This does not retrieve the last item visible in the tree-view window.</span></span> <span data-ttu-id="c6699-130">您可以使用 [**TreeView \_ GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-130">You can use the [**TreeView\_GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) macro to send this message.</span></span><br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <span data-ttu-id="c6699-131"><dt>**TVGN \_ 下一步**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-131"><dt>**TVGN\_NEXT**</dt></span></span> </dl>                                  | <span data-ttu-id="c6699-132">抓取下一個同級專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-132">Retrieves the next sibling item.</span></span> <span data-ttu-id="c6699-133">您可以使用 [**TreeView \_ GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-133">You can use the [**TreeView\_GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) macro to send this message.</span></span><br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <span data-ttu-id="c6699-134"><dt>**TVGN \_ NEXTSELECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-134"><dt>**TVGN\_NEXTSELECTED**</dt></span></span> </dl>          | <span data-ttu-id="c6699-135">**Windows Vista （含）以後版本。**</span><span class="sxs-lookup"><span data-stu-id="c6699-135">**Windows Vista and later.**</span></span> <span data-ttu-id="c6699-136">抓取下一個選取的專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-136">Retrieves the next selected item.</span></span> <span data-ttu-id="c6699-137">您可以使用 [**TreeView \_ GetNextSelected**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-137">You can use the [**TreeView\_GetNextSelected**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) macro to send this message.</span></span><br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <span data-ttu-id="c6699-138"><dt>**TVGN \_ NEXTVISIBLE**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-138"><dt>**TVGN\_NEXTVISIBLE**</dt></span></span> </dl>             | <span data-ttu-id="c6699-139">抓取位於指定專案後面的下一個可見專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-139">Retrieves the next visible item that follows the specified item.</span></span> <span data-ttu-id="c6699-140">指定的專案必須是可見的。</span><span class="sxs-lookup"><span data-stu-id="c6699-140">The specified item must be visible.</span></span> <span data-ttu-id="c6699-141">使用 [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) 訊息來判斷是否可以看到專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-141">Use the [**TVM\_GETITEMRECT**](tvm-getitemrect.md) message to determine whether an item is visible.</span></span> <span data-ttu-id="c6699-142">您可以使用 [**TreeView \_ GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-142">You can use the [**TreeView\_GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) macro to send this message.</span></span><br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <span data-ttu-id="c6699-143"><dt>**TVGN \_ 父系**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-143"><dt>**TVGN\_PARENT**</dt></span></span> </dl>                            | <span data-ttu-id="c6699-144">抓取指定之專案的父系。</span><span class="sxs-lookup"><span data-stu-id="c6699-144">Retrieves the parent of the specified item.</span></span> <span data-ttu-id="c6699-145">您可以使用 [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-145">You can use the [**TreeView\_GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) macro to send this message.</span></span><br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <span data-ttu-id="c6699-146"><dt>**TVGN \_ 上一步**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-146"><dt>**TVGN\_PREVIOUS**</dt></span></span> </dl>                      | <span data-ttu-id="c6699-147">抓取上一個同級專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-147">Retrieves the previous sibling item.</span></span> <span data-ttu-id="c6699-148">您可以使用 [**TreeView \_ GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-148">You can use the [**TreeView\_GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) macro to send this message.</span></span><br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <span data-ttu-id="c6699-149"><dt>**TVGN \_ PREVIOUSVISIBLE**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-149"><dt>**TVGN\_PREVIOUSVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="c6699-150">抓取指定專案之前的第一個可見專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-150">Retrieves the first visible item that precedes the specified item.</span></span> <span data-ttu-id="c6699-151">指定的專案必須是可見的。</span><span class="sxs-lookup"><span data-stu-id="c6699-151">The specified item must be visible.</span></span> <span data-ttu-id="c6699-152">使用 [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) 訊息來判斷是否可以看到專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-152">Use the [**TVM\_GETITEMRECT**](tvm-getitemrect.md) message to determine whether an item is visible.</span></span> <span data-ttu-id="c6699-153">您可以使用 [**TreeView \_ GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-153">You can use the [**TreeView\_GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) macro to send this message.</span></span><br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <span data-ttu-id="c6699-154"><dt>**TVGN \_ 根目錄**</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-154"><dt>**TVGN\_ROOT**</dt></span></span> </dl>                                  | <span data-ttu-id="c6699-155">抓取樹狀檢視控制項的最上層或第一個專案。</span><span class="sxs-lookup"><span data-stu-id="c6699-155">Retrieves the topmost or very first item of the tree-view control.</span></span> <span data-ttu-id="c6699-156">您可以使用 [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c6699-156">You can use the [**TreeView\_GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) macro to send this message.</span></span> <br/>                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="c6699-157">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6699-157">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6699-158">專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6699-158">Handle to an item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6699-159">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6699-159">Return value</span></span>

<span data-ttu-id="c6699-160">如果成功，則傳回專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6699-160">Returns the handle to the item if successful.</span></span> <span data-ttu-id="c6699-161">在大部分的情況下，訊息會傳回 **Null** 值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6699-161">For most cases, the message returns a **NULL** value to indicate an error.</span></span> <span data-ttu-id="c6699-162">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="c6699-162">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6699-163">備註</span><span class="sxs-lookup"><span data-stu-id="c6699-163">Remarks</span></span>

<span data-ttu-id="c6699-164">如果要抓取的專案是樹狀結構的根節點，此訊息將會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c6699-164">This message will return **NULL** if the item being retrieved is the root node of the tree.</span></span> <span data-ttu-id="c6699-165">例如，如果您在 \_ 樹狀檢視根節點的第一個層級子系上，使用此訊息搭配 TVGN 父旗標，訊息將會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c6699-165">For example, if you use this message with the TVGN\_PARENT flag on a first-level child of the tree view's root node, the message will return **NULL**.</span></span>

<span data-ttu-id="c6699-166">您也可以使用下列其中一個相關宏：</span><span class="sxs-lookup"><span data-stu-id="c6699-166">You can also use one of these related macros:</span></span>



|                                                               |
|---------------------------------------------------------------|
| [<span data-ttu-id="c6699-167">**TreeView \_ system.windows.media.visualtreehelper.getchild**</span><span class="sxs-lookup"><span data-stu-id="c6699-167">**TreeView\_GetChild**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [<span data-ttu-id="c6699-168">**TreeView \_ GetDropHilight**</span><span class="sxs-lookup"><span data-stu-id="c6699-168">**TreeView\_GetDropHilight**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [<span data-ttu-id="c6699-169">**TreeView \_ GetFirstVisible**</span><span class="sxs-lookup"><span data-stu-id="c6699-169">**TreeView\_GetFirstVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [<span data-ttu-id="c6699-170">**TreeView \_ GetLastVisible**</span><span class="sxs-lookup"><span data-stu-id="c6699-170">**TreeView\_GetLastVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [<span data-ttu-id="c6699-171">**TreeView \_ GetNextSibling**</span><span class="sxs-lookup"><span data-stu-id="c6699-171">**TreeView\_GetNextSibling**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [<span data-ttu-id="c6699-172">**TreeView \_ GetNextVisible**</span><span class="sxs-lookup"><span data-stu-id="c6699-172">**TreeView\_GetNextVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [<span data-ttu-id="c6699-173">**TreeView \_ GetParent**</span><span class="sxs-lookup"><span data-stu-id="c6699-173">**TreeView\_GetParent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [<span data-ttu-id="c6699-174">**TreeView \_ GetPrevSibling**</span><span class="sxs-lookup"><span data-stu-id="c6699-174">**TreeView\_GetPrevSibling**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [<span data-ttu-id="c6699-175">**TreeView \_ GetPrevVisible**</span><span class="sxs-lookup"><span data-stu-id="c6699-175">**TreeView\_GetPrevVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [<span data-ttu-id="c6699-176">**TreeView \_ GetRoot**</span><span class="sxs-lookup"><span data-stu-id="c6699-176">**TreeView\_GetRoot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [<span data-ttu-id="c6699-177">**TreeView \_ GetSelection**</span><span class="sxs-lookup"><span data-stu-id="c6699-177">**TreeView\_GetSelection**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a><span data-ttu-id="c6699-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6699-178">Requirements</span></span>



| <span data-ttu-id="c6699-179">需求</span><span class="sxs-lookup"><span data-stu-id="c6699-179">Requirement</span></span> | <span data-ttu-id="c6699-180">值</span><span class="sxs-lookup"><span data-stu-id="c6699-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6699-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6699-181">Minimum supported client</span></span><br/> | <span data-ttu-id="c6699-182">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6699-182">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6699-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6699-183">Minimum supported server</span></span><br/> | <span data-ttu-id="c6699-184">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6699-184">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6699-185">標頭</span><span class="sxs-lookup"><span data-stu-id="c6699-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6699-186"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6699-186"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





