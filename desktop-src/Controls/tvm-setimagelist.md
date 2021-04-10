---
title: 'TVM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項的 [一般] 或 [狀態] 影像清單，然後使用新的影像來重新繪製控制項。 您可以使用 TreeView SetImageList 宏明確地傳送此訊息 \_ 。
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- TVM_SETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685921"
---
# <a name="tvm_setimagelist-message"></a><span data-ttu-id="b52d3-105">TVM \_ SETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="b52d3-105">TVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="b52d3-106">設定樹狀檢視控制項的 [一般] 或 [狀態] 影像清單，然後使用新的影像來重新繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="b52d3-106">Sets the normal or state image list for a tree-view control and redraws the control using the new images.</span></span> <span data-ttu-id="b52d3-107">您可以使用 [**TreeView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b52d3-107">You can send this message explicitly or by using the [**TreeView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b52d3-108">參數</span><span class="sxs-lookup"><span data-stu-id="b52d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b52d3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b52d3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b52d3-110">要設定之影像清單的類型。</span><span class="sxs-lookup"><span data-stu-id="b52d3-110">Type of image list to set.</span></span> <span data-ttu-id="b52d3-111">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="b52d3-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="b52d3-112">值</span><span class="sxs-lookup"><span data-stu-id="b52d3-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="b52d3-113">意義</span><span class="sxs-lookup"><span data-stu-id="b52d3-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="b52d3-114"><dt>**TVSIL \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="b52d3-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="b52d3-115">指出一般影像清單，其中包含樹狀檢視控制項專案的已選取、nonselected 和重迭影像。</span><span class="sxs-lookup"><span data-stu-id="b52d3-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="b52d3-116"><dt>**TVSIL \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="b52d3-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="b52d3-117">表示狀態影像清單。</span><span class="sxs-lookup"><span data-stu-id="b52d3-117">Indicates the state image list.</span></span> <span data-ttu-id="b52d3-118">您可以使用狀態影像來表示應用程式定義的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="b52d3-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="b52d3-119">狀態影像會顯示在專案的選取專案或 nonselected 影像的左邊。</span><span class="sxs-lookup"><span data-stu-id="b52d3-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b52d3-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b52d3-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b52d3-121">影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b52d3-121">Handle to the image list.</span></span> <span data-ttu-id="b52d3-122">如果 *lParam* 為 **Null**，則訊息會從樹狀檢視控制項中移除指定的影像清單。</span><span class="sxs-lookup"><span data-stu-id="b52d3-122">If *lParam* is **NULL**, the message removes the specified image list from the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b52d3-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="b52d3-123">Return value</span></span>

<span data-ttu-id="b52d3-124">傳回上一個影像清單的控制碼（如果有的話），否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b52d3-124">Returns the handle to the previous image list, if any, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b52d3-125">備註</span><span class="sxs-lookup"><span data-stu-id="b52d3-125">Remarks</span></span>

<span data-ttu-id="b52d3-126">樹狀檢視控制項將不會損毀以此訊息指定的影像清單。</span><span class="sxs-lookup"><span data-stu-id="b52d3-126">The tree-view control will not destroy the image list specified with this message.</span></span> <span data-ttu-id="b52d3-127">當您的應用程式不再需要時，您的應用程式必須損毀映射清單。</span><span class="sxs-lookup"><span data-stu-id="b52d3-127">Your application must destroy the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b52d3-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b52d3-128">Requirements</span></span>



| <span data-ttu-id="b52d3-129">需求</span><span class="sxs-lookup"><span data-stu-id="b52d3-129">Requirement</span></span> | <span data-ttu-id="b52d3-130">值</span><span class="sxs-lookup"><span data-stu-id="b52d3-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b52d3-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b52d3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b52d3-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b52d3-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b52d3-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b52d3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b52d3-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b52d3-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b52d3-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b52d3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b52d3-136"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b52d3-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b52d3-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b52d3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52d3-138">**TVM \_ GETIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="b52d3-138">**TVM\_GETIMAGELIST**</span></span>](tvm-getimagelist.md)
</dt> </dl>

 

 





