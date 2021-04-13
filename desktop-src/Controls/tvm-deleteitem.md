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
# <a name="tvm_deleteitem-message"></a><span data-ttu-id="18f9a-105">TVM \_ DELETEITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="18f9a-105">TVM\_DELETEITEM message</span></span>

<span data-ttu-id="18f9a-106">從樹狀檢視控制項中移除專案及其所有子系。</span><span class="sxs-lookup"><span data-stu-id="18f9a-106">Removes an item and all its children from a tree-view control.</span></span> <span data-ttu-id="18f9a-107">您可以使用 [**TreeView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="18f9a-107">You can send this message explicitly or by using the [**TreeView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="18f9a-108">參數</span><span class="sxs-lookup"><span data-stu-id="18f9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18f9a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18f9a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="18f9a-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="18f9a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="18f9a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18f9a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18f9a-112">要刪除之專案的 **HTREEITEM** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="18f9a-112">**HTREEITEM** handle to the item to delete.</span></span> <span data-ttu-id="18f9a-113">如果 *lParam* 設定為 TVI \_ ROOT 或 **Null**，則會刪除所有專案。</span><span class="sxs-lookup"><span data-stu-id="18f9a-113">If *lParam* is set to TVI\_ROOT or to **NULL**, all items are deleted.</span></span> <span data-ttu-id="18f9a-114">您也可以使用 [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) 宏來刪除所有專案。</span><span class="sxs-lookup"><span data-stu-id="18f9a-114">You can also use the [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) macro to delete all items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18f9a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="18f9a-115">Return value</span></span>

<span data-ttu-id="18f9a-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="18f9a-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="18f9a-117">備註</span><span class="sxs-lookup"><span data-stu-id="18f9a-117">Remarks</span></span>

<span data-ttu-id="18f9a-118">您無法安全地刪除專案以回應通知，例如 [izdebski \_ SELCHANGING](tvn-selchanging.md)。</span><span class="sxs-lookup"><span data-stu-id="18f9a-118">It is not safe to delete items in response to a notification such as [TVN\_SELCHANGING](tvn-selchanging.md).</span></span>

<span data-ttu-id="18f9a-119">刪除專案之後，其控制碼無效且無法使用。</span><span class="sxs-lookup"><span data-stu-id="18f9a-119">Once an item is deleted, its handle is invalid and cannot be used.</span></span>

<span data-ttu-id="18f9a-120">移除每個專案時，父視窗會收到 [izdebski \_ DELETEITEM](tvn-deleteitem.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="18f9a-120">The parent window receives a [TVN\_DELETEITEM](tvn-deleteitem.md) notification code when each item is removed.</span></span>

<span data-ttu-id="18f9a-121">如果正在編輯專案標籤，則會取消編輯作業，而且父視窗會收到 [izdebski \_ ENDLABELEDIT](tvn-endlabeledit.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="18f9a-121">If the item label is being edited, the edit operation is canceled and the parent window receives the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

<span data-ttu-id="18f9a-122">如果您刪除具有 [**電視 \_ NOSCROLL**](tree-view-control-window-styles.md) 樣式之樹狀檢視控制項中的所有專案，則後續新增的專案可能無法正確顯示。</span><span class="sxs-lookup"><span data-stu-id="18f9a-122">If you delete all items in a tree-view control that has the [**TVS\_NOSCROLL**](tree-view-control-window-styles.md) style, items subsequently added may not display properly.</span></span> <span data-ttu-id="18f9a-123">如需詳細資訊，請參閱 [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems)。</span><span class="sxs-lookup"><span data-stu-id="18f9a-123">For more information, see [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span></span>

## <a name="requirements"></a><span data-ttu-id="18f9a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="18f9a-124">Requirements</span></span>



| <span data-ttu-id="18f9a-125">需求</span><span class="sxs-lookup"><span data-stu-id="18f9a-125">Requirement</span></span> | <span data-ttu-id="18f9a-126">值</span><span class="sxs-lookup"><span data-stu-id="18f9a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18f9a-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18f9a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="18f9a-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18f9a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18f9a-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18f9a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="18f9a-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18f9a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18f9a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="18f9a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="18f9a-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="18f9a-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





