---
title: 'TVM_GETITEMRECT 訊息 (Commctrl .h) '
description: 抓取樹狀檢視專案的周框，並指出專案是否可見。 您可以使用 TreeView GetItemRect 宏明確地傳送此訊息 \_ 。
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094411"
---
# <a name="tvm_getitemrect-message"></a><span data-ttu-id="e4b6e-105">TVM \_ GETITEMRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="e4b6e-105">TVM\_GETITEMRECT message</span></span>

<span data-ttu-id="e4b6e-106">抓取樹狀檢視專案的周框，並指出專案是否可見。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-106">Retrieves the bounding rectangle for a tree-view item and indicates whether the item is visible.</span></span> <span data-ttu-id="e4b6e-107">您可以使用 [**TreeView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-107">You can send this message explicitly or by using the [**TreeView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4b6e-108">參數</span><span class="sxs-lookup"><span data-stu-id="e4b6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b6e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4b6e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b6e-110">值，指定要對其取得周框矩形的專案部分。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-110">Value specifying the portion of the item for which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="e4b6e-111">如果此參數為 **TRUE**，周框矩形只會包含專案的文字。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-111">If this parameter is **TRUE**, the bounding rectangle includes only the text of the item.</span></span> <span data-ttu-id="e4b6e-112">否則，它會包含專案在樹狀檢視控制項中所占的整個行。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-112">Otherwise, it includes the entire line that the item occupies in the tree-view control.</span></span>

</dd> <dt>

<span data-ttu-id="e4b6e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4b6e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b6e-114">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，在傳送訊息時，會包含要取得其矩形之專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that, when sending the message, contains the handle of the item to retrieve the rectangle for.</span></span> <span data-ttu-id="e4b6e-115">請參閱下列範例，以取得如何將專案控制碼放置在此參數中的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-115">See the example below for more information on how to place the item handle in this parameter.</span></span> <span data-ttu-id="e4b6e-116">從訊息傳回之後，這個參數會包含周框。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-116">After returning from the message, this parameter contains the bounding rectangle.</span></span> <span data-ttu-id="e4b6e-117">座標相對於樹狀檢視控制項的左上角。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-117">The coordinates are relative to the upper-left corner of the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b6e-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4b6e-118">Return value</span></span>

<span data-ttu-id="e4b6e-119">如果專案是可見的，且已成功取出周框，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-119">If the item is visible and the bounding rectangle was successfully retrieved, the return value is **TRUE**.</span></span> <span data-ttu-id="e4b6e-120">否則，訊息會傳回 **FALSE** ，且不會取出周框。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-120">Otherwise, the message returns **FALSE** and does not retrieve the bounding rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b6e-121">備註</span><span class="sxs-lookup"><span data-stu-id="e4b6e-121">Remarks</span></span>

<span data-ttu-id="e4b6e-122">傳送此訊息時， *lParam* 參數包含要為其抓取矩形之專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e4b6e-122">When sending this message, the *lParam* parameter contains the handle of the item that the rectangle is being retrieved for.</span></span> <span data-ttu-id="e4b6e-123">控制碼會放置在 *lParam* 中，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="e4b6e-123">The handle is placed in *lParam* as shown in the following example:</span></span>


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a><span data-ttu-id="e4b6e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4b6e-124">Requirements</span></span>



| <span data-ttu-id="e4b6e-125">需求</span><span class="sxs-lookup"><span data-stu-id="e4b6e-125">Requirement</span></span> | <span data-ttu-id="e4b6e-126">值</span><span class="sxs-lookup"><span data-stu-id="e4b6e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b6e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4b6e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b6e-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4b6e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4b6e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4b6e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b6e-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4b6e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4b6e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="e4b6e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b6e-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b6e-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

