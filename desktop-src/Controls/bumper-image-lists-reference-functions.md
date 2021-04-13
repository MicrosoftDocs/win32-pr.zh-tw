---
title: 影像清單函式
description: 影像清單函式
ms.assetid: b5754633-f673-414e-9e0b-3f6f211ecd2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3e877e4f264aa9c0440b183a2c528592b6ccee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321927"
---
# <a name="image-list-functions"></a><span data-ttu-id="3c034-103">影像清單函式</span><span class="sxs-lookup"><span data-stu-id="3c034-103">Image List Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3c034-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="3c034-104">In This Section</span></span>

-   [<span data-ttu-id="3c034-105">**HIMAGELIST \_ QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="3c034-105">**HIMAGELIST\_QueryInterface**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-himagelist_queryinterface)
-   [<span data-ttu-id="3c034-106">**ImageList \_ 新增**</span><span class="sxs-lookup"><span data-stu-id="3c034-106">**ImageList\_Add**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add)
-   [<span data-ttu-id="3c034-107">**ImageList \_ AddMasked**</span><span class="sxs-lookup"><span data-stu-id="3c034-107">**ImageList\_AddMasked**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)
-   [<span data-ttu-id="3c034-108">**ImageList \_ BeginDrag**</span><span class="sxs-lookup"><span data-stu-id="3c034-108">**ImageList\_BeginDrag**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)
-   [<span data-ttu-id="3c034-109">**ImageList \_ CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="3c034-109">**ImageList\_CoCreateInstance**</span></span>](/windows/desktop/api/CommonControls/nf-commoncontrols-imagelist_cocreateinstance)
-   [<span data-ttu-id="3c034-110">**ImageList \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="3c034-110">**ImageList\_Copy**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_copy)
-   [<span data-ttu-id="3c034-111">**ImageList \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="3c034-111">**ImageList\_Create**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)
-   [<span data-ttu-id="3c034-112">**ImageList 損 \_ 毀**</span><span class="sxs-lookup"><span data-stu-id="3c034-112">**ImageList\_Destroy**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy)
-   [<span data-ttu-id="3c034-113">**ImageList \_ system.windows.dragdrop.dragenter>**</span><span class="sxs-lookup"><span data-stu-id="3c034-113">**ImageList\_DragEnter**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter)
-   [<span data-ttu-id="3c034-114">**ImageList \_ DragLeave**</span><span class="sxs-lookup"><span data-stu-id="3c034-114">**ImageList\_DragLeave**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave)
-   [<span data-ttu-id="3c034-115">**ImageList \_ DragMove**</span><span class="sxs-lookup"><span data-stu-id="3c034-115">**ImageList\_DragMove**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove)
-   [<span data-ttu-id="3c034-116">**ImageList \_ DragShowNolock**</span><span class="sxs-lookup"><span data-stu-id="3c034-116">**ImageList\_DragShowNolock**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragshownolock)
-   [<span data-ttu-id="3c034-117">**ImageList \_ 繪圖**</span><span class="sxs-lookup"><span data-stu-id="3c034-117">**ImageList\_Draw**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw)
-   [<span data-ttu-id="3c034-118">**ImageList \_ DrawEx**</span><span class="sxs-lookup"><span data-stu-id="3c034-118">**ImageList\_DrawEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex)
-   [<span data-ttu-id="3c034-119">**ImageList \_ DrawIndirect**</span><span class="sxs-lookup"><span data-stu-id="3c034-119">**ImageList\_DrawIndirect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawindirect)
-   [<span data-ttu-id="3c034-120">**ImageList \_ 重複**</span><span class="sxs-lookup"><span data-stu-id="3c034-120">**ImageList\_Duplicate**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_duplicate)
-   [<span data-ttu-id="3c034-121">**ImageList \_ EndDrag**</span><span class="sxs-lookup"><span data-stu-id="3c034-121">**ImageList\_EndDrag**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag)
-   [<span data-ttu-id="3c034-122">**ImageList \_ GetBkColor**</span><span class="sxs-lookup"><span data-stu-id="3c034-122">**ImageList\_GetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor)
-   [<span data-ttu-id="3c034-123">**ImageList \_ GetDragImage**</span><span class="sxs-lookup"><span data-stu-id="3c034-123">**ImageList\_GetDragImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage)
-   [<span data-ttu-id="3c034-124">**ImageList \_ GetIcon**</span><span class="sxs-lookup"><span data-stu-id="3c034-124">**ImageList\_GetIcon**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon)
-   [<span data-ttu-id="3c034-125">**ImageList \_ GetIconSize**</span><span class="sxs-lookup"><span data-stu-id="3c034-125">**ImageList\_GetIconSize**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticonsize)
-   [<span data-ttu-id="3c034-126">**ImageList \_ GetImageCount**</span><span class="sxs-lookup"><span data-stu-id="3c034-126">**ImageList\_GetImageCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount)
-   [<span data-ttu-id="3c034-127">**ImageList \_ GetImageInfo**</span><span class="sxs-lookup"><span data-stu-id="3c034-127">**ImageList\_GetImageInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo)
-   [<span data-ttu-id="3c034-128">**ImageList \_ LoadImage**</span><span class="sxs-lookup"><span data-stu-id="3c034-128">**ImageList\_LoadImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_loadimagea)
-   [<span data-ttu-id="3c034-129">**ImageList \_ 合併**</span><span class="sxs-lookup"><span data-stu-id="3c034-129">**ImageList\_Merge**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge)
-   [<span data-ttu-id="3c034-130">**ImageList \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="3c034-130">**ImageList\_Read**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_read)
-   [<span data-ttu-id="3c034-131">**ImageList \_ ReadEx**</span><span class="sxs-lookup"><span data-stu-id="3c034-131">**ImageList\_ReadEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_readex)
-   [<span data-ttu-id="3c034-132">**ImageList \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="3c034-132">**ImageList\_Remove**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove)
-   [<span data-ttu-id="3c034-133">**ImageList \_ 取代**</span><span class="sxs-lookup"><span data-stu-id="3c034-133">**ImageList\_Replace**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace)
-   [<span data-ttu-id="3c034-134">**ImageList \_ ReplaceIcon**</span><span class="sxs-lookup"><span data-stu-id="3c034-134">**ImageList\_ReplaceIcon**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon)
-   [<span data-ttu-id="3c034-135">**ImageList \_ SetBkColor**</span><span class="sxs-lookup"><span data-stu-id="3c034-135">**ImageList\_SetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor)
-   [<span data-ttu-id="3c034-136">**ImageList \_ SetColorTable**</span><span class="sxs-lookup"><span data-stu-id="3c034-136">**ImageList\_SetColorTable**</span></span>](imagelist-setcolortable.md)
-   [<span data-ttu-id="3c034-137">**ImageList \_ SetDragCursorImage**</span><span class="sxs-lookup"><span data-stu-id="3c034-137">**ImageList\_SetDragCursorImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage)
-   [<span data-ttu-id="3c034-138">**ImageList \_ SetIconSize**</span><span class="sxs-lookup"><span data-stu-id="3c034-138">**ImageList\_SetIconSize**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_seticonsize)
-   [<span data-ttu-id="3c034-139">**ImageList \_ SetImageCount**</span><span class="sxs-lookup"><span data-stu-id="3c034-139">**ImageList\_SetImageCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setimagecount)
-   [<span data-ttu-id="3c034-140">**ImageList \_ SetOverlayImage**</span><span class="sxs-lookup"><span data-stu-id="3c034-140">**ImageList\_SetOverlayImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage)
-   [<span data-ttu-id="3c034-141">**ImageList \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="3c034-141">**ImageList\_Write**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_write)
-   [<span data-ttu-id="3c034-142">**ImageList \_ WriteEx**</span><span class="sxs-lookup"><span data-stu-id="3c034-142">**ImageList\_WriteEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_writeex)

 

 




