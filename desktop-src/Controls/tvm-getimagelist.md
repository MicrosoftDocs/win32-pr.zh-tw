---
title: 'TVM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 抓取與樹狀檢視控制項相關聯之一般或狀態影像清單的控制碼。 您可以使用 TreeView GetImageList 宏明確地傳送此訊息 \_ 。
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- TVM_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686380"
---
# <a name="tvm_getimagelist-message"></a><span data-ttu-id="cdb39-105">TVM \_ GETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="cdb39-105">TVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="cdb39-106">抓取與樹狀檢視控制項相關聯之一般或狀態影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cdb39-106">Retrieves the handle to the normal or state image list associated with a tree-view control.</span></span> <span data-ttu-id="cdb39-107">您可以使用 [**TreeView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="cdb39-107">You can send this message explicitly or by using the [**TreeView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdb39-108">參數</span><span class="sxs-lookup"><span data-stu-id="cdb39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdb39-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cdb39-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdb39-110">要取出的影像清單類型。</span><span class="sxs-lookup"><span data-stu-id="cdb39-110">Type of image list to retrieve.</span></span> <span data-ttu-id="cdb39-111">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="cdb39-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="cdb39-112">值</span><span class="sxs-lookup"><span data-stu-id="cdb39-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="cdb39-113">意義</span><span class="sxs-lookup"><span data-stu-id="cdb39-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="cdb39-114"><dt>**TVSIL \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="cdb39-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="cdb39-115">指出一般影像清單，其中包含樹狀檢視控制項專案的已選取、nonselected 和重迭影像。</span><span class="sxs-lookup"><span data-stu-id="cdb39-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="cdb39-116"><dt>**TVSIL \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="cdb39-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="cdb39-117">表示狀態影像清單。</span><span class="sxs-lookup"><span data-stu-id="cdb39-117">Indicates the state image list.</span></span> <span data-ttu-id="cdb39-118">您可以使用狀態影像來表示應用程式定義的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="cdb39-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="cdb39-119">狀態影像會顯示在專案的選取專案或 nonselected 影像的左邊。</span><span class="sxs-lookup"><span data-stu-id="cdb39-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cdb39-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cdb39-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cdb39-121">必須為零。</span><span class="sxs-lookup"><span data-stu-id="cdb39-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdb39-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdb39-122">Return value</span></span>

<span data-ttu-id="cdb39-123">傳回指定之影像清單的 HIMAGELIST 控制碼。</span><span class="sxs-lookup"><span data-stu-id="cdb39-123">Returns an HIMAGELIST handle to the specified image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb39-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdb39-124">Requirements</span></span>



| <span data-ttu-id="cdb39-125">需求</span><span class="sxs-lookup"><span data-stu-id="cdb39-125">Requirement</span></span> | <span data-ttu-id="cdb39-126">值</span><span class="sxs-lookup"><span data-stu-id="cdb39-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb39-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdb39-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb39-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdb39-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cdb39-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdb39-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb39-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdb39-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cdb39-131">標頭</span><span class="sxs-lookup"><span data-stu-id="cdb39-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdb39-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cdb39-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdb39-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdb39-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb39-134">**TVM \_ SETIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="cdb39-134">**TVM\_SETIMAGELIST**</span></span>](tvm-setimagelist.md)
</dt> </dl>

 

 





