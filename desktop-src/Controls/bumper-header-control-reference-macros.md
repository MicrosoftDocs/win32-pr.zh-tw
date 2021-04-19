---
title: 標題控制項宏
description: 標題控制項宏
ms.assetid: 5ef52add-f796-48e5-83a8-e7d2c07e202d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ddf0f735950fd014edc9a68493e131ff6ed1e0a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106982844"
---
# <a name="header-control-macros"></a><span data-ttu-id="0c35b-103">標題控制項宏</span><span class="sxs-lookup"><span data-stu-id="0c35b-103">Header Control Macros</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0c35b-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="0c35b-104">In This Section</span></span>

-   [<span data-ttu-id="0c35b-105">**標頭 \_ ClearAllFilters**</span><span class="sxs-lookup"><span data-stu-id="0c35b-105">**Header\_ClearAllFilters**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
-   [<span data-ttu-id="0c35b-106">**標頭 \_ ClearFilter**</span><span class="sxs-lookup"><span data-stu-id="0c35b-106">**Header\_ClearFilter**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter)
-   [<span data-ttu-id="0c35b-107">**標頭 \_ CreateDragImage**</span><span class="sxs-lookup"><span data-stu-id="0c35b-107">**Header\_CreateDragImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage)
-   [<span data-ttu-id="0c35b-108">**標頭 \_ DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="0c35b-108">**Header\_DeleteItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem)
-   [<span data-ttu-id="0c35b-109">**標頭 \_ EditFilter**</span><span class="sxs-lookup"><span data-stu-id="0c35b-109">**Header\_EditFilter**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_editfilter)
-   [<span data-ttu-id="0c35b-110">**標頭 \_ GetBitmapMargin**</span><span class="sxs-lookup"><span data-stu-id="0c35b-110">**Header\_GetBitmapMargin**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin)
-   [<span data-ttu-id="0c35b-111">**標頭 \_ GetFocusedItem**</span><span class="sxs-lookup"><span data-stu-id="0c35b-111">**Header\_GetFocusedItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem)
-   [<span data-ttu-id="0c35b-112">**標頭 \_ GetImageList**</span><span class="sxs-lookup"><span data-stu-id="0c35b-112">**Header\_GetImageList**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist)
-   [<span data-ttu-id="0c35b-113">**標頭 \_ GetItem**</span><span class="sxs-lookup"><span data-stu-id="0c35b-113">**Header\_GetItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem)
-   [<span data-ttu-id="0c35b-114">**標頭 \_ GetItemCount**</span><span class="sxs-lookup"><span data-stu-id="0c35b-114">**Header\_GetItemCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount)
-   [<span data-ttu-id="0c35b-115">**標頭 \_ GetItemDropDownRect**</span><span class="sxs-lookup"><span data-stu-id="0c35b-115">**Header\_GetItemDropDownRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect)
-   [<span data-ttu-id="0c35b-116">**標頭 \_ GetItemRect**</span><span class="sxs-lookup"><span data-stu-id="0c35b-116">**Header\_GetItemRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect)
-   [<span data-ttu-id="0c35b-117">**標頭 \_ GetOrderArray**</span><span class="sxs-lookup"><span data-stu-id="0c35b-117">**Header\_GetOrderArray**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray)
-   [<span data-ttu-id="0c35b-118">**標頭 \_ GetOverflowRect**</span><span class="sxs-lookup"><span data-stu-id="0c35b-118">**Header\_GetOverflowRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect)
-   [<span data-ttu-id="0c35b-119">**標頭 \_ GetStateImageList**</span><span class="sxs-lookup"><span data-stu-id="0c35b-119">**Header\_GetStateImageList**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist)
-   [<span data-ttu-id="0c35b-120">**標頭 \_ GetUnicodeFormat**</span><span class="sxs-lookup"><span data-stu-id="0c35b-120">**Header\_GetUnicodeFormat**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat)
-   [<span data-ttu-id="0c35b-121">**標頭 \_ InsertItem**</span><span class="sxs-lookup"><span data-stu-id="0c35b-121">**Header\_InsertItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem)
-   [<span data-ttu-id="0c35b-122">**標頭 \_ 版面配置**</span><span class="sxs-lookup"><span data-stu-id="0c35b-122">**Header\_Layout**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_layout)
-   [<span data-ttu-id="0c35b-123">**標頭 \_ OrderToIndex**</span><span class="sxs-lookup"><span data-stu-id="0c35b-123">**Header\_OrderToIndex**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex)
-   [<span data-ttu-id="0c35b-124">**標頭 \_ SetBitmapMargin**</span><span class="sxs-lookup"><span data-stu-id="0c35b-124">**Header\_SetBitmapMargin**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin)
-   [<span data-ttu-id="0c35b-125">**標頭 \_ SetFilterChangeTimeout**</span><span class="sxs-lookup"><span data-stu-id="0c35b-125">**Header\_SetFilterChangeTimeout**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout)
-   [<span data-ttu-id="0c35b-126">**標頭 \_ SetFocusedItem**</span><span class="sxs-lookup"><span data-stu-id="0c35b-126">**Header\_SetFocusedItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem)
-   [<span data-ttu-id="0c35b-127">**標頭 \_ SetHotDivider**</span><span class="sxs-lookup"><span data-stu-id="0c35b-127">**Header\_SetHotDivider**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider)
-   [<span data-ttu-id="0c35b-128">**標頭 \_ SetImageList**</span><span class="sxs-lookup"><span data-stu-id="0c35b-128">**Header\_SetImageList**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist)
-   [<span data-ttu-id="0c35b-129">**標頭 \_ SetItem**</span><span class="sxs-lookup"><span data-stu-id="0c35b-129">**Header\_SetItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem)
-   [<span data-ttu-id="0c35b-130">**標頭 \_ SetOrderArray**</span><span class="sxs-lookup"><span data-stu-id="0c35b-130">**Header\_SetOrderArray**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray)
-   [<span data-ttu-id="0c35b-131">**標頭 \_ SetStateImageList**</span><span class="sxs-lookup"><span data-stu-id="0c35b-131">**Header\_SetStateImageList**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist)
-   [<span data-ttu-id="0c35b-132">**標頭 \_ SetUnicodeFormat**</span><span class="sxs-lookup"><span data-stu-id="0c35b-132">**Header\_SetUnicodeFormat**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat)

 

 




