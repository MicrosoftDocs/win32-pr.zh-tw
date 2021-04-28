---
title: 功能表函數
description: 功能表函數
ms.assetid: c40719aa-3735-4f46-88f7-6cc20b088ad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e55dec7532d30749d709f815b232ad3bcc6419
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087566"
---
# <a name="menu-functions"></a><span data-ttu-id="cf60c-103">功能表函數</span><span class="sxs-lookup"><span data-stu-id="cf60c-103">Menu Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cf60c-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="cf60c-104">In This Section</span></span>

-   [<span data-ttu-id="cf60c-105">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-105">**AppendMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
-   [<span data-ttu-id="cf60c-106">**CheckMenuItem**</span><span class="sxs-lookup"><span data-stu-id="cf60c-106">**CheckMenuItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)
-   [<span data-ttu-id="cf60c-107">**CheckMenuRadioItem**</span><span class="sxs-lookup"><span data-stu-id="cf60c-107">**CheckMenuRadioItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)
-   [<span data-ttu-id="cf60c-108">**CreateMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-108">**CreateMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createmenu)
-   [<span data-ttu-id="cf60c-109">**CreatePopupMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-109">**CreatePopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu)
-   [<span data-ttu-id="cf60c-110">**DeleteMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-110">**DeleteMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-deletemenu)
-   [<span data-ttu-id="cf60c-111">**DestroyMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-111">**DestroyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroymenu)
-   [<span data-ttu-id="cf60c-112">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="cf60c-112">**DrawMenuBar**</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawmenubar)
-   [<span data-ttu-id="cf60c-113">**EnableMenuItem**</span><span class="sxs-lookup"><span data-stu-id="cf60c-113">**EnableMenuItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem)
-   [<span data-ttu-id="cf60c-114">**EndMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-114">**EndMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endmenu)
-   [<span data-ttu-id="cf60c-115">**GetMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-115">**GetMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenu)
-   [<span data-ttu-id="cf60c-116">**GetMenuBarInfo**</span><span class="sxs-lookup"><span data-stu-id="cf60c-116">**GetMenuBarInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)
-   [<span data-ttu-id="cf60c-117">**GetMenuCheckMarkDimensions**</span><span class="sxs-lookup"><span data-stu-id="cf60c-117">**GetMenuCheckMarkDimensions**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions)
-   [<span data-ttu-id="cf60c-118">**GetMenuDefaultItem**</span><span class="sxs-lookup"><span data-stu-id="cf60c-118">**GetMenuDefaultItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem)
-   [<span data-ttu-id="cf60c-119">**GetMenuInfo**</span><span class="sxs-lookup"><span data-stu-id="cf60c-119">**GetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo)
-   [<span data-ttu-id="cf60c-120">**GetMenuItemCount**</span><span class="sxs-lookup"><span data-stu-id="cf60c-120">**GetMenuItemCount**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuitemcount)
-   [<span data-ttu-id="cf60c-121">**GetMenuItemID**</span><span class="sxs-lookup"><span data-stu-id="cf60c-121">**GetMenuItemID**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid)
-   [<span data-ttu-id="cf60c-122">**GetMenuItemInfo**</span><span class="sxs-lookup"><span data-stu-id="cf60c-122">**GetMenuItemInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)
-   [<span data-ttu-id="cf60c-123">**GetMenuItemRect**</span><span class="sxs-lookup"><span data-stu-id="cf60c-123">**GetMenuItemRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenuitemrect)
-   [<span data-ttu-id="cf60c-124">**GetMenuState**</span><span class="sxs-lookup"><span data-stu-id="cf60c-124">**GetMenuState**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenustate)
-   [<span data-ttu-id="cf60c-125">**GetMenuString**</span><span class="sxs-lookup"><span data-stu-id="cf60c-125">**GetMenuString**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmenustringa)
-   [<span data-ttu-id="cf60c-126">**GetSubMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-126">**GetSubMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
-   [<span data-ttu-id="cf60c-127">**GetSystemMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-127">**GetSystemMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
-   [<span data-ttu-id="cf60c-128">**HiliteMenuItem**</span><span class="sxs-lookup"><span data-stu-id="cf60c-128">**HiliteMenuItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem)
-   [<span data-ttu-id="cf60c-129">**InsertMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-129">**InsertMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
-   [<span data-ttu-id="cf60c-130">**InsertMenuItem**</span><span class="sxs-lookup"><span data-stu-id="cf60c-130">**InsertMenuItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)
-   [<span data-ttu-id="cf60c-131">**IsMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-131">**IsMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ismenu)
-   [<span data-ttu-id="cf60c-132">**LoadMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-132">**LoadMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenua)
-   [<span data-ttu-id="cf60c-133">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="cf60c-133">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
-   [<span data-ttu-id="cf60c-134">**MenuItemFromPoint**</span><span class="sxs-lookup"><span data-stu-id="cf60c-134">**MenuItemFromPoint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-menuitemfrompoint)
-   [<span data-ttu-id="cf60c-135">**ModifyMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-135">**ModifyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
-   [<span data-ttu-id="cf60c-136">**RemoveMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-136">**RemoveMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removemenu)
-   [<span data-ttu-id="cf60c-137">**SetMenu**</span><span class="sxs-lookup"><span data-stu-id="cf60c-137">**SetMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenu)
-   [<span data-ttu-id="cf60c-138">**SetMenuDefaultItem**</span><span class="sxs-lookup"><span data-stu-id="cf60c-138">**SetMenuDefaultItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)
-   [<span data-ttu-id="cf60c-139">**SetMenuInfo**</span><span class="sxs-lookup"><span data-stu-id="cf60c-139">**SetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
-   [<span data-ttu-id="cf60c-140">**SetMenuItemBitmaps**</span><span class="sxs-lookup"><span data-stu-id="cf60c-140">**SetMenuItemBitmaps**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)
-   [<span data-ttu-id="cf60c-141">**SetMenuItemInfo**</span><span class="sxs-lookup"><span data-stu-id="cf60c-141">**SetMenuItemInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)
-   [<span data-ttu-id="cf60c-142">**Trackpopupmenu 讓**</span><span class="sxs-lookup"><span data-stu-id="cf60c-142">**TrackPopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
-   [<span data-ttu-id="cf60c-143">**TrackPopupMenuEx**</span><span class="sxs-lookup"><span data-stu-id="cf60c-143">**TrackPopupMenuEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)

 

 




