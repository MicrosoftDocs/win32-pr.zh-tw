---
description: Windows 支援五種圖形模式，可讓應用程式指定色彩的混合方式、顯示輸出的方式、如何調整輸出等等。 下表說明這些儲存在 DC 中的模式。
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: 圖形模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512889"
---
# <a name="graphic-modes"></a><span data-ttu-id="a5b93-104">圖形模式</span><span class="sxs-lookup"><span data-stu-id="a5b93-104">Graphic Modes</span></span>

<span data-ttu-id="a5b93-105">Windows 支援五種圖形模式，可讓應用程式指定色彩的混合方式、顯示輸出的方式、如何調整輸出等等。</span><span class="sxs-lookup"><span data-stu-id="a5b93-105">Windows supports five graphic modes that allow an application to specify how colors are mixed, where output appears, how the output is scaled, and so on.</span></span> <span data-ttu-id="a5b93-106">下表說明這些儲存在 DC 中的模式。</span><span class="sxs-lookup"><span data-stu-id="a5b93-106">These modes, which are stored in a DC, are described in the following table.</span></span>



| <span data-ttu-id="a5b93-107">圖形模式</span><span class="sxs-lookup"><span data-stu-id="a5b93-107">Graphics mode</span></span> | <span data-ttu-id="a5b93-108">Description</span><span class="sxs-lookup"><span data-stu-id="a5b93-108">Description</span></span>                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b93-109">背景</span><span class="sxs-lookup"><span data-stu-id="a5b93-109">Background</span></span>    | <span data-ttu-id="a5b93-110">定義背景色彩如何與點陣圖和文字作業的現有視窗或螢幕色彩混合。</span><span class="sxs-lookup"><span data-stu-id="a5b93-110">Defines how background colors are mixed with existing window or screen colors for bitmap and text operations.</span></span>              |
| <span data-ttu-id="a5b93-111">繪圖</span><span class="sxs-lookup"><span data-stu-id="a5b93-111">Drawing</span></span>       | <span data-ttu-id="a5b93-112">定義如何使用畫筆、筆刷、點陣圖和文字作業的現有視窗或螢幕色彩來混合前景色彩。</span><span class="sxs-lookup"><span data-stu-id="a5b93-112">Defines how foreground colors are mixed with existing window or screen colors for pen, brush, bitmap, and text operations.</span></span> |
| <span data-ttu-id="a5b93-113">對應</span><span class="sxs-lookup"><span data-stu-id="a5b93-113">Mapping</span></span>       | <span data-ttu-id="a5b93-114">定義圖形輸出如何從邏輯 (或世界) 空間對應至視窗、螢幕或印表機紙張。</span><span class="sxs-lookup"><span data-stu-id="a5b93-114">Defines how graphics output is mapped from logical (or world) space onto the window, screen, or printer paper.</span></span>             |
| <span data-ttu-id="a5b93-115">多邊形填滿</span><span class="sxs-lookup"><span data-stu-id="a5b93-115">Polygon-fill</span></span>  | <span data-ttu-id="a5b93-116">定義如何使用筆刷模式來填滿複雜區域的內部。</span><span class="sxs-lookup"><span data-stu-id="a5b93-116">Defines how the brush pattern is used to fill the interior of complex regions.</span></span>                                             |
| <span data-ttu-id="a5b93-117">伸展</span><span class="sxs-lookup"><span data-stu-id="a5b93-117">Stretching</span></span>    | <span data-ttu-id="a5b93-118">定義點陣圖壓縮 (或縮小) 時，如何使用現有的視窗或螢幕色彩來混合點陣圖色彩。</span><span class="sxs-lookup"><span data-stu-id="a5b93-118">Defines how bitmap colors are mixed with existing window or screen colors when the bitmap is compressed (or scaled down).</span></span>  |



 

<span data-ttu-id="a5b93-119">和繪圖物件一樣，系統會使用預設的圖形模式來初始化 DC。</span><span class="sxs-lookup"><span data-stu-id="a5b93-119">As it does with graphic objects, the system initializes a DC with default graphic modes.</span></span> <span data-ttu-id="a5b93-120">應用程式可以藉由呼叫下列函式來取得和檢查這些預設模式。</span><span class="sxs-lookup"><span data-stu-id="a5b93-120">An application can retrieve and examine these default modes by calling the following functions.</span></span>



| <span data-ttu-id="a5b93-121">圖形模式</span><span class="sxs-lookup"><span data-stu-id="a5b93-121">Graphics mode</span></span> | <span data-ttu-id="a5b93-122">函式</span><span class="sxs-lookup"><span data-stu-id="a5b93-122">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="a5b93-123">背景</span><span class="sxs-lookup"><span data-stu-id="a5b93-123">Background</span></span>    | [<span data-ttu-id="a5b93-124">**GetBkMode**</span><span class="sxs-lookup"><span data-stu-id="a5b93-124">**GetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| <span data-ttu-id="a5b93-125">繪圖</span><span class="sxs-lookup"><span data-stu-id="a5b93-125">Drawing</span></span>       | [<span data-ttu-id="a5b93-126">**GetROP2**</span><span class="sxs-lookup"><span data-stu-id="a5b93-126">**GetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| <span data-ttu-id="a5b93-127">對應</span><span class="sxs-lookup"><span data-stu-id="a5b93-127">Mapping</span></span>       | [<span data-ttu-id="a5b93-128">**GetMapMode**</span><span class="sxs-lookup"><span data-stu-id="a5b93-128">**GetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| <span data-ttu-id="a5b93-129">多邊形填滿</span><span class="sxs-lookup"><span data-stu-id="a5b93-129">Polygon-fill</span></span>  | [<span data-ttu-id="a5b93-130">**GetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="a5b93-130">**GetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| <span data-ttu-id="a5b93-131">伸展</span><span class="sxs-lookup"><span data-stu-id="a5b93-131">Stretching</span></span>    | [<span data-ttu-id="a5b93-132">**GetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="a5b93-132">**GetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

<span data-ttu-id="a5b93-133">應用程式可以藉由呼叫下列其中一項功能來變更預設模式。</span><span class="sxs-lookup"><span data-stu-id="a5b93-133">An application can change the default modes by calling one of the following functions.</span></span>



| <span data-ttu-id="a5b93-134">圖形模式</span><span class="sxs-lookup"><span data-stu-id="a5b93-134">Graphics mode</span></span> | <span data-ttu-id="a5b93-135">函式</span><span class="sxs-lookup"><span data-stu-id="a5b93-135">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="a5b93-136">背景</span><span class="sxs-lookup"><span data-stu-id="a5b93-136">Background</span></span>    | [<span data-ttu-id="a5b93-137">**SetBkMode**</span><span class="sxs-lookup"><span data-stu-id="a5b93-137">**SetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| <span data-ttu-id="a5b93-138">繪圖</span><span class="sxs-lookup"><span data-stu-id="a5b93-138">Drawing</span></span>       | [<span data-ttu-id="a5b93-139">**SetROP2**</span><span class="sxs-lookup"><span data-stu-id="a5b93-139">**SetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| <span data-ttu-id="a5b93-140">對應</span><span class="sxs-lookup"><span data-stu-id="a5b93-140">Mapping</span></span>       | [<span data-ttu-id="a5b93-141">**SetMapMode**</span><span class="sxs-lookup"><span data-stu-id="a5b93-141">**SetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| <span data-ttu-id="a5b93-142">多邊形填滿</span><span class="sxs-lookup"><span data-stu-id="a5b93-142">Polygon-fill</span></span>  | [<span data-ttu-id="a5b93-143">**SetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="a5b93-143">**SetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| <span data-ttu-id="a5b93-144">伸展</span><span class="sxs-lookup"><span data-stu-id="a5b93-144">Stretching</span></span>    | [<span data-ttu-id="a5b93-145">**SetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="a5b93-145">**SetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



