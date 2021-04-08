---
title: 功能表函數
description: .
ms.assetid: c40719aa-3735-4f46-88f7-6cc20b088ad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea264d2c0bf34176da47d4948e9201cb157690af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840120"
---
# <a name="menu-functions"></a><span data-ttu-id="f8ad5-103">功能表函數</span><span class="sxs-lookup"><span data-stu-id="f8ad5-103">Menu Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f8ad5-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="f8ad5-104">In This Section</span></span>

-   [<span data-ttu-id="f8ad5-105">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-105">**AppendMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
-   [<span data-ttu-id="f8ad5-106">**CheckMenuItem**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-106">**CheckMenuItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)
-   [<span data-ttu-id="f8ad5-107">**CheckMenuRadioItem**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-107">**CheckMenuRadioItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)
-   [<span data-ttu-id="f8ad5-108">**CreateMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-108">**CreateMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createmenu)
-   [<span data-ttu-id="f8ad5-109">**CreatePopupMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-109">**CreatePopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu)
-   [<span data-ttu-id="f8ad5-110">**DeleteMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-110">**DeleteMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-deletemenu)
-   [<span data-ttu-id="f8ad5-111">**DestroyMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-111">**DestroyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroymenu)
-   [<span data-ttu-id="f8ad5-112">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-112">**DrawMenuBar**</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawmenubar)
-   [<span data-ttu-id="f8ad5-113">**EnableMenuItem**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-113">**EnableMenuItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem)
-   [<span data-ttu-id="f8ad5-114">**EndMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-114">**EndMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endmenu)
-   [<span data-ttu-id="f8ad5-115">**GetMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-115">**GetMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenu)
-   [<span data-ttu-id="f8ad5-116">**GetMenuBarInfo**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-116">**GetMenuBarInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)
-   [<span data-ttu-id="f8ad5-117">**GetMenuCheckMarkDimensions**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-117">**GetMenuCheckMarkDimensions**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions)
-   [<span data-ttu-id="f8ad5-118">**GetMenuDefaultItem**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-118">**GetMenuDefaultItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem)
-   [<span data-ttu-id="f8ad5-119">**GetMenuInfo**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-119">**GetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo)
-   [<span data-ttu-id="f8ad5-120">**GetMenuItemCount**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-120">**GetMenuItemCount**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuitemcount)
-   [<span data-ttu-id="f8ad5-121">**GetMenuItemID**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-121">**GetMenuItemID**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid)
-   [<span data-ttu-id="f8ad5-122">**GetMenuItemInfo**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-122">**GetMenuItemInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)
-   [<span data-ttu-id="f8ad5-123">**GetMenuItemRect**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-123">**GetMenuItemRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuitemrect)
-   [<span data-ttu-id="f8ad5-124">**GetMenuState**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-124">**GetMenuState**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenustate)
-   [<span data-ttu-id="f8ad5-125">**GetMenuString**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-125">**GetMenuString**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenustringa)
-   [<span data-ttu-id="f8ad5-126">**GetSubMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-126">**GetSubMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
-   [<span data-ttu-id="f8ad5-127">**GetSystemMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-127">**GetSystemMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
-   [<span data-ttu-id="f8ad5-128">**HiliteMenuItem**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-128">**HiliteMenuItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem)
-   [<span data-ttu-id="f8ad5-129">**InsertMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-129">**InsertMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
-   [<span data-ttu-id="f8ad5-130">**InsertMenuItem**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-130">**InsertMenuItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)
-   [<span data-ttu-id="f8ad5-131">**IsMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-131">**IsMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ismenu)
-   [<span data-ttu-id="f8ad5-132">**LoadMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-132">**LoadMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenua)
-   [<span data-ttu-id="f8ad5-133">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-133">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
-   [<span data-ttu-id="f8ad5-134">**MenuItemFromPoint**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-134">**MenuItemFromPoint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-menuitemfrompoint)
-   [<span data-ttu-id="f8ad5-135">**ModifyMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-135">**ModifyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
-   [<span data-ttu-id="f8ad5-136">**RemoveMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-136">**RemoveMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removemenu)
-   [<span data-ttu-id="f8ad5-137">**SetMenu**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-137">**SetMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenu)
-   [<span data-ttu-id="f8ad5-138">**SetMenuDefaultItem**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-138">**SetMenuDefaultItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)
-   [<span data-ttu-id="f8ad5-139">**SetMenuInfo**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-139">**SetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
-   [<span data-ttu-id="f8ad5-140">**SetMenuItemBitmaps**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-140">**SetMenuItemBitmaps**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)
-   [<span data-ttu-id="f8ad5-141">**SetMenuItemInfo**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-141">**SetMenuItemInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)
-   [<span data-ttu-id="f8ad5-142">**Trackpopupmenu 讓**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-142">**TrackPopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
-   [<span data-ttu-id="f8ad5-143">**TrackPopupMenuEx**</span><span class="sxs-lookup"><span data-stu-id="f8ad5-143">**TrackPopupMenuEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)

 

 




