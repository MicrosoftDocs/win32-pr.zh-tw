---
title: 重迭、基礎和主要平面
description: 您可以在應用程式中使用硬體層平面 (重迭和基礎平面) 。
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- Windows 上的 OpenGL，硬體層平面
- 硬體層平面 OpenGL
- 覆蓋平面 OpenGL
- 基礎平面 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969656"
---
# <a name="overlay-underlay-and-main-planes"></a><span data-ttu-id="e3a8c-107">重迭、基礎和主要平面</span><span class="sxs-lookup"><span data-stu-id="e3a8c-107">Overlay, Underlay, and Main Planes</span></span>

<span data-ttu-id="e3a8c-108">您可以在應用程式中使用硬體層平面 (重迭和基礎平面) 。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-108">You can use hardware layer planes (overlay and underlay planes) in your applications.</span></span> <span data-ttu-id="e3a8c-109">使用 Windows，像素格式會描述圖形裝置的圖元設定。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-109">With Windows, pixel formats describe the pixel configurations of a graphics device.</span></span> <span data-ttu-id="e3a8c-110">每個像素格式都會描述主要色彩緩衝區的深度和其他特性，並描述其他緩衝區 (例如主要平面使用的深度、累積、樣板和輔助) 。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-110">Each pixel format describes the depth and other characteristics of the main color buffers and describes additional buffers (such as depth, accumulation, stencil, and auxiliary) that the main plane uses.</span></span> <span data-ttu-id="e3a8c-111">像素格式現在已擴充，以包含重迭和基礎緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-111">Pixel formats are now extended to include overlay and underlay buffers.</span></span>

<span data-ttu-id="e3a8c-112">圖層平面一律具有 front 左邊的色彩緩衝區，也可以包含 front 和上一頁色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-112">Layer planes always have a front-left color buffer and also can include front-right and back color buffers.</span></span> <span data-ttu-id="e3a8c-113">每個圖層平面都有特定的轉譯內容，可轉譯成圖層緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-113">Each layer plane has a specific rendering context to render into the layer buffers.</span></span> <span data-ttu-id="e3a8c-114">您無法在圖層平面中使用 GDI 繪圖函數。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-114">You cannot use GDI drawing functions in layer planes.</span></span>

<span data-ttu-id="e3a8c-115">視窗會管理圖層平面的色彩緩衝區，與管理主平面色彩緩衝區的方式相似。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-115">A window manages the color buffers of layer planes similarly to the way it manages main-plane color buffers.</span></span> <span data-ttu-id="e3a8c-116">您可以同時顯示多個具有重迭及/或基礎平面的視窗。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-116">You can display multiple windows with overlay and/or underlay planes at the same time.</span></span> <span data-ttu-id="e3a8c-117">您無法擁有可在主要繪圖平面中的任何視窗上移動的自由浮動重迭視窗。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-117">You cannot have free-floating overlay windows that can move over any window in the main drawing plane.</span></span> <span data-ttu-id="e3a8c-118">此外，因為它會在視窗中隨時遮蔽基礎平面，所以您無法使用沒有透明色彩的硬體快顯平面。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-118">In addition, because it would obscure underlying planes in a window at all times, you cannot use hardware pop-up planes that have no transparent color.</span></span>

<span data-ttu-id="e3a8c-119">視窗中的每個圖層平面都有相關聯的調色板。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-119">Each layer plane in a window has an associated palette.</span></span> <span data-ttu-id="e3a8c-120">您可以設定 [色彩索引圖層] 平面的 [調色板]，但您可以修正 RGBA 色彩平面的調色板。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-120">You can set the palette of a color-index layer plane, but the palette of an RGBA color plane is fixed.</span></span> <span data-ttu-id="e3a8c-121">當視窗在前景時，您必須實現適當的調色板。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-121">You must realize the appropriate palette when a window is in the foreground.</span></span> <span data-ttu-id="e3a8c-122">圖層平面具有透明的圖元色彩或索引，可讓任何基礎圖層平面顯示。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-122">Layer planes have a transparent pixel color or index that enables any underlying layer planes to show through.</span></span>

<span data-ttu-id="e3a8c-123">您可以在不同的分層平面中，將轉譯內容的狀態複製到另一個呈現內容。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-123">You can copy the state of a rendering context to another rendering context in a separate layer plane.</span></span> <span data-ttu-id="e3a8c-124">您也可以在不同的分層平面中，共用轉譯內容之間的顯示清單。</span><span class="sxs-lookup"><span data-stu-id="e3a8c-124">You can also share display lists among rendering contexts in different layer planes.</span></span>

<span data-ttu-id="e3a8c-125">下列函式適用于圖層平面：</span><span class="sxs-lookup"><span data-stu-id="e3a8c-125">The following functions are used with layer planes:</span></span>

-   [<span data-ttu-id="e3a8c-126">**wglCopyCoNtext**</span><span class="sxs-lookup"><span data-stu-id="e3a8c-126">**wglCopyContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [<span data-ttu-id="e3a8c-127">**wglCreateLayerCoNtext**</span><span class="sxs-lookup"><span data-stu-id="e3a8c-127">**wglCreateLayerContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [<span data-ttu-id="e3a8c-128">**wglDescribeLayerPlane**</span><span class="sxs-lookup"><span data-stu-id="e3a8c-128">**wglDescribeLayerPlane**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [<span data-ttu-id="e3a8c-129">**wglGetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="e3a8c-129">**wglGetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [<span data-ttu-id="e3a8c-130">**wglRealizeLayerPalette**</span><span class="sxs-lookup"><span data-stu-id="e3a8c-130">**wglRealizeLayerPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [<span data-ttu-id="e3a8c-131">**wglSetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="e3a8c-131">**wglSetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [<span data-ttu-id="e3a8c-132">**wglSwapLayerBuffers**</span><span class="sxs-lookup"><span data-stu-id="e3a8c-132">**wglSwapLayerBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




