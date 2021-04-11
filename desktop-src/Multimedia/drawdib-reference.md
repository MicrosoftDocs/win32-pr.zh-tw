---
title: DrawDib 參考
description: DrawDib 參考
ms.assetid: 08489fa8-511d-4511-a158-f0cae2c6cef2
keywords:
- Windows 多媒體，DrawDib 參考
- 多媒體、DrawDib 參考
- Windows (VFW) 的影片，DrawDib 參考
- 適用于 Windows) 的 VFW (影片，DrawDib 參考
- DrawDib，參考
- DrawDib 參考，關於
- DrawDib 的參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be359e2d0af6de28d6a054e60e0c5cac1de55c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021937"
---
# <a name="drawdib-reference"></a><span data-ttu-id="e22d3-110">DrawDib 參考</span><span class="sxs-lookup"><span data-stu-id="e22d3-110">DrawDib Reference</span></span>

<span data-ttu-id="e22d3-111">本節描述 DrawDib 函式和相關聯的結構。</span><span class="sxs-lookup"><span data-stu-id="e22d3-111">This section describes the DrawDib functions and associated structures.</span></span> <span data-ttu-id="e22d3-112">這些元素的分組方式如下：</span><span class="sxs-lookup"><span data-stu-id="e22d3-112">These elements are grouped as follows:</span></span>

## <a name="drawdib-library-operations"></a><span data-ttu-id="e22d3-113">DrawDib 程式庫作業</span><span class="sxs-lookup"><span data-stu-id="e22d3-113">DrawDib Library Operations</span></span>

-   [<span data-ttu-id="e22d3-114">**DrawDibOpen**</span><span class="sxs-lookup"><span data-stu-id="e22d3-114">**DrawDibOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibopen)
-   [<span data-ttu-id="e22d3-115">**DrawDibClose**</span><span class="sxs-lookup"><span data-stu-id="e22d3-115">**DrawDibClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)
-   [<span data-ttu-id="e22d3-116">**DrawDibProfileDisplay**</span><span class="sxs-lookup"><span data-stu-id="e22d3-116">**DrawDibProfileDisplay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay)

## <a name="image-rendering"></a><span data-ttu-id="e22d3-117">影像轉譯</span><span class="sxs-lookup"><span data-stu-id="e22d3-117">Image Rendering</span></span>

-   [<span data-ttu-id="e22d3-118">**DrawDibDraw**</span><span class="sxs-lookup"><span data-stu-id="e22d3-118">**DrawDibDraw**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)
-   [<span data-ttu-id="e22d3-119">**DrawDibGetBuffer**</span><span class="sxs-lookup"><span data-stu-id="e22d3-119">**DrawDibGetBuffer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer)
-   [<span data-ttu-id="e22d3-120">**DrawDibUpdate**</span><span class="sxs-lookup"><span data-stu-id="e22d3-120">**DrawDibUpdate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate)
-   [<span data-ttu-id="e22d3-121">**StretchDIB**</span><span class="sxs-lookup"><span data-stu-id="e22d3-121">**StretchDIB**</span></span>](/windows/desktop/api/Vfw/nf-vfw-stretchdib)

## <a name="sequences-of-images"></a><span data-ttu-id="e22d3-122">影像的順序</span><span class="sxs-lookup"><span data-stu-id="e22d3-122">Sequences of Images</span></span>

-   [<span data-ttu-id="e22d3-123">**DrawDibBegin**</span><span class="sxs-lookup"><span data-stu-id="e22d3-123">**DrawDibBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)
-   [<span data-ttu-id="e22d3-124">**DrawDibEnd**</span><span class="sxs-lookup"><span data-stu-id="e22d3-124">**DrawDibEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibend)
-   [<span data-ttu-id="e22d3-125">**DrawDibStart**</span><span class="sxs-lookup"><span data-stu-id="e22d3-125">**DrawDibStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibstart)
-   [<span data-ttu-id="e22d3-126">**DrawDibStop**</span><span class="sxs-lookup"><span data-stu-id="e22d3-126">**DrawDibStop**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibstop)

## <a name="palettes"></a><span data-ttu-id="e22d3-127">調色板</span><span class="sxs-lookup"><span data-stu-id="e22d3-127">Palettes</span></span>

-   [<span data-ttu-id="e22d3-128">**DrawDibRealize**</span><span class="sxs-lookup"><span data-stu-id="e22d3-128">**DrawDibRealize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize)
-   [<span data-ttu-id="e22d3-129">**DrawDibSetPalette**</span><span class="sxs-lookup"><span data-stu-id="e22d3-129">**DrawDibSetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette)
-   [<span data-ttu-id="e22d3-130">**DrawDibGetPalette**</span><span class="sxs-lookup"><span data-stu-id="e22d3-130">**DrawDibGetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette)
-   [<span data-ttu-id="e22d3-131">**DrawDibChangePalette**</span><span class="sxs-lookup"><span data-stu-id="e22d3-131">**DrawDibChangePalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)

## <a name="timing-drawdib"></a><span data-ttu-id="e22d3-132">計時 DrawDib</span><span class="sxs-lookup"><span data-stu-id="e22d3-132">Timing DrawDib</span></span>

-   [<span data-ttu-id="e22d3-133">**DRAWDIBTIME**</span><span class="sxs-lookup"><span data-stu-id="e22d3-133">**DRAWDIBTIME**</span></span>](/windows/desktop/api/Vfw/ns-vfw-drawdibtime)

 

 




