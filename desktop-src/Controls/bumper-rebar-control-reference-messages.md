---
title: Rebar 控制項訊息
description: Rebar 控制項訊息
ms.assetid: 5fa1df55-0883-4b3b-bcde-7c40d574c792
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc43d8091b1a3808b98091b62ed8b7965f13bb9b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035294"
---
# <a name="rebar-control-messages"></a><span data-ttu-id="19486-103">Rebar 控制項訊息</span><span class="sxs-lookup"><span data-stu-id="19486-103">Rebar Control Messages</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19486-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="19486-104">In This Section</span></span>

-   [<span data-ttu-id="19486-105">**RB \_ BEGINDRAG**</span><span class="sxs-lookup"><span data-stu-id="19486-105">**RB\_BEGINDRAG**</span></span>](rb-begindrag.md)
-   [<span data-ttu-id="19486-106">**RB \_ DELETEBAND**</span><span class="sxs-lookup"><span data-stu-id="19486-106">**RB\_DELETEBAND**</span></span>](rb-deleteband.md)
-   [<span data-ttu-id="19486-107">**RB \_ DRAGMOVE**</span><span class="sxs-lookup"><span data-stu-id="19486-107">**RB\_DRAGMOVE**</span></span>](rb-dragmove.md)
-   [<span data-ttu-id="19486-108">**RB \_ ENDDRAG**</span><span class="sxs-lookup"><span data-stu-id="19486-108">**RB\_ENDDRAG**</span></span>](rb-enddrag.md)
-   [<span data-ttu-id="19486-109">**RB \_ GETBANDBORDERS**</span><span class="sxs-lookup"><span data-stu-id="19486-109">**RB\_GETBANDBORDERS**</span></span>](rb-getbandborders.md)
-   [<span data-ttu-id="19486-110">**RB \_ GETBANDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="19486-110">**RB\_GETBANDCOUNT**</span></span>](rb-getbandcount.md)
-   [<span data-ttu-id="19486-111">**RB \_ GETBANDINFO**</span><span class="sxs-lookup"><span data-stu-id="19486-111">**RB\_GETBANDINFO**</span></span>](rb-getbandinfo.md)
-   [<span data-ttu-id="19486-112">**RB \_ GETBANDMARGINS**</span><span class="sxs-lookup"><span data-stu-id="19486-112">**RB\_GETBANDMARGINS**</span></span>](rb-getbandmargins.md)
-   [<span data-ttu-id="19486-113">**RB \_ GETBARHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="19486-113">**RB\_GETBARHEIGHT**</span></span>](rb-getbarheight.md)
-   [<span data-ttu-id="19486-114">**RB \_ GETBARINFO**</span><span class="sxs-lookup"><span data-stu-id="19486-114">**RB\_GETBARINFO**</span></span>](rb-getbarinfo.md)
-   [<span data-ttu-id="19486-115">**RB \_ GETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="19486-115">**RB\_GETBKCOLOR**</span></span>](rb-getbkcolor.md)
-   [<span data-ttu-id="19486-116">**RB \_ GETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="19486-116">**RB\_GETCOLORSCHEME**</span></span>](rb-getcolorscheme.md)
-   [<span data-ttu-id="19486-117">**RB \_ GETDROPTARGET**</span><span class="sxs-lookup"><span data-stu-id="19486-117">**RB\_GETDROPTARGET**</span></span>](rb-getdroptarget.md)
-   [<span data-ttu-id="19486-118">**RB \_ GETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="19486-118">**RB\_GETEXTENDEDSTYLE**</span></span>](rb-getextendedstyle.md)
-   [<span data-ttu-id="19486-119">**RB \_ GETPALETTE**</span><span class="sxs-lookup"><span data-stu-id="19486-119">**RB\_GETPALETTE**</span></span>](rb-getpalette.md)
-   [<span data-ttu-id="19486-120">**RB \_ GETRECT**</span><span class="sxs-lookup"><span data-stu-id="19486-120">**RB\_GETRECT**</span></span>](rb-getrect.md)
-   [<span data-ttu-id="19486-121">**RB \_ GETROWCOUNT**</span><span class="sxs-lookup"><span data-stu-id="19486-121">**RB\_GETROWCOUNT**</span></span>](rb-getrowcount.md)
-   [<span data-ttu-id="19486-122">**RB \_ GETROWHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="19486-122">**RB\_GETROWHEIGHT**</span></span>](rb-getrowheight.md)
-   [<span data-ttu-id="19486-123">**RB \_ GETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="19486-123">**RB\_GETTEXTCOLOR**</span></span>](rb-gettextcolor.md)
-   [<span data-ttu-id="19486-124">**RB \_ GETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="19486-124">**RB\_GETTOOLTIPS**</span></span>](rb-gettooltips.md)
-   [<span data-ttu-id="19486-125">**RB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="19486-125">**RB\_GETUNICODEFORMAT**</span></span>](rb-getunicodeformat.md)
-   [<span data-ttu-id="19486-126">**RB \_ SYSTEM.WINDOWS.MEDIA.VISUALTREEHELPER.HITTEST**</span><span class="sxs-lookup"><span data-stu-id="19486-126">**RB\_HITTEST**</span></span>](rb-hittest.md)
-   [<span data-ttu-id="19486-127">**RB \_ IDTOINDEX**</span><span class="sxs-lookup"><span data-stu-id="19486-127">**RB\_IDTOINDEX**</span></span>](rb-idtoindex.md)
-   [<span data-ttu-id="19486-128">**RB \_ INSERTBAND**</span><span class="sxs-lookup"><span data-stu-id="19486-128">**RB\_INSERTBAND**</span></span>](rb-insertband.md)
-   [<span data-ttu-id="19486-129">**RB \_ MAXIMIZEBAND**</span><span class="sxs-lookup"><span data-stu-id="19486-129">**RB\_MAXIMIZEBAND**</span></span>](rb-maximizeband.md)
-   [<span data-ttu-id="19486-130">**RB \_ MINIMIZEBAND**</span><span class="sxs-lookup"><span data-stu-id="19486-130">**RB\_MINIMIZEBAND**</span></span>](rb-minimizeband.md)
-   [<span data-ttu-id="19486-131">**RB \_ MOVEBAND**</span><span class="sxs-lookup"><span data-stu-id="19486-131">**RB\_MOVEBAND**</span></span>](rb-moveband.md)
-   [<span data-ttu-id="19486-132">**RB \_ PUSHCHEVRON**</span><span class="sxs-lookup"><span data-stu-id="19486-132">**RB\_PUSHCHEVRON**</span></span>](rb-pushchevron.md)
-   [<span data-ttu-id="19486-133">**RB \_ SETBANDINFO**</span><span class="sxs-lookup"><span data-stu-id="19486-133">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
-   [<span data-ttu-id="19486-134">**RB \_ SETBANDWIDTH**</span><span class="sxs-lookup"><span data-stu-id="19486-134">**RB\_SETBANDWIDTH**</span></span>](rb-setbandwidth.md)
-   [<span data-ttu-id="19486-135">**RB \_ SETBARINFO**</span><span class="sxs-lookup"><span data-stu-id="19486-135">**RB\_SETBARINFO**</span></span>](rb-setbarinfo.md)
-   [<span data-ttu-id="19486-136">**RB \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="19486-136">**RB\_SETBKCOLOR**</span></span>](rb-setbkcolor.md)
-   [<span data-ttu-id="19486-137">**RB \_ SETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="19486-137">**RB\_SETCOLORSCHEME**</span></span>](rb-setcolorscheme.md)
-   [<span data-ttu-id="19486-138">**RB \_ SETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="19486-138">**RB\_SETEXTENDEDSTYLE**</span></span>](rb-setextendedstyle.md)
-   [<span data-ttu-id="19486-139">**RB \_ SETPALETTE**</span><span class="sxs-lookup"><span data-stu-id="19486-139">**RB\_SETPALETTE**</span></span>](rb-setpalette.md)
-   [<span data-ttu-id="19486-140">**RB \_ SETPARENT**</span><span class="sxs-lookup"><span data-stu-id="19486-140">**RB\_SETPARENT**</span></span>](rb-setparent.md)
-   [<span data-ttu-id="19486-141">**RB \_ SETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="19486-141">**RB\_SETTEXTCOLOR**</span></span>](rb-settextcolor.md)
-   [<span data-ttu-id="19486-142">**RB \_ SETTOOLTIPS**</span><span class="sxs-lookup"><span data-stu-id="19486-142">**RB\_SETTOOLTIPS**</span></span>](rb-settooltips.md)
-   [<span data-ttu-id="19486-143">**RB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="19486-143">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
-   [<span data-ttu-id="19486-144">**RB \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="19486-144">**RB\_SETWINDOWTHEME**</span></span>](rb-setwindowtheme.md)
-   [<span data-ttu-id="19486-145">**RB \_ SHOWBAND**</span><span class="sxs-lookup"><span data-stu-id="19486-145">**RB\_SHOWBAND**</span></span>](rb-showband.md)
-   [<span data-ttu-id="19486-146">**RB \_ SIZETORECT**</span><span class="sxs-lookup"><span data-stu-id="19486-146">**RB\_SIZETORECT**</span></span>](rb-sizetorect.md)

 

 




