---
description: Microsoft Windows 圖形裝置介面 (GDI) 可讓應用程式在影片顯示器和印表機上使用圖形和格式化的文字。
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: Windows GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5fc6ba9f4eb99786b21daeff2e1c48b9ce09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973052"
---
# <a name="windows-gdi"></a><span data-ttu-id="adf50-103">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="adf50-103">Windows GDI</span></span>

## <a name="purpose"></a><span data-ttu-id="adf50-104">目的</span><span class="sxs-lookup"><span data-stu-id="adf50-104">Purpose</span></span>

<span data-ttu-id="adf50-105">Microsoft Windows 圖形裝置介面 (GDI) 可讓應用程式在影片顯示器和印表機上使用圖形和格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="adf50-105">The Microsoft Windows graphics device interface (GDI) enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="adf50-106">以 Windows 為基礎的應用程式不會直接存取圖形硬體。</span><span class="sxs-lookup"><span data-stu-id="adf50-106">Windows-based applications do not access the graphics hardware directly.</span></span> <span data-ttu-id="adf50-107">相反地，GDI 會代表應用程式與設備磁碟機互動。</span><span class="sxs-lookup"><span data-stu-id="adf50-107">Instead, GDI interacts with device drivers on behalf of applications.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="adf50-108">適用時</span><span class="sxs-lookup"><span data-stu-id="adf50-108">Where applicable</span></span>

<span data-ttu-id="adf50-109">GDI 可以在所有 Windows 應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="adf50-109">GDI can be used in all Windows-based applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="adf50-110">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="adf50-110">Developer audience</span></span>

<span data-ttu-id="adf50-111">此 API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="adf50-111">This API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="adf50-112">需要熟悉 Windows [訊息驅動架構](../learnwin32/window-messages.md) 。</span><span class="sxs-lookup"><span data-stu-id="adf50-112">Familiarity with the Windows [message-driven architecture](../learnwin32/window-messages.md) is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="adf50-113">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="adf50-113">Run-time requirements</span></span>

<span data-ttu-id="adf50-114">如需哪些作業系統需要哪些作業系統才能使用特定功能的相關資訊，請參閱函式檔集的需求一節。</span><span class="sxs-lookup"><span data-stu-id="adf50-114">For information on which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="adf50-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="adf50-115">In this section</span></span>

-   [<span data-ttu-id="adf50-116">點陣圖</span><span class="sxs-lookup"><span data-stu-id="adf50-116">Bitmaps</span></span>](bitmaps.md)
-   [<span data-ttu-id="adf50-117">筆刷</span><span class="sxs-lookup"><span data-stu-id="adf50-117">Brushes</span></span>](brushes.md)
-   [<span data-ttu-id="adf50-118">裁剪</span><span class="sxs-lookup"><span data-stu-id="adf50-118">Clipping</span></span>](clipping.md)
-   [<span data-ttu-id="adf50-119">色彩</span><span class="sxs-lookup"><span data-stu-id="adf50-119">Colors</span></span>](colors.md)
-   [<span data-ttu-id="adf50-120">座標空間和轉換</span><span class="sxs-lookup"><span data-stu-id="adf50-120">Coordinate Spaces and Transformations</span></span>](coordinate-spaces-and-transformations.md)
-   [<span data-ttu-id="adf50-121">裝置內容</span><span class="sxs-lookup"><span data-stu-id="adf50-121">Device Contexts</span></span>](device-contexts.md)
-   [<span data-ttu-id="adf50-122">填滿的圖案</span><span class="sxs-lookup"><span data-stu-id="adf50-122">Filled Shapes</span></span>](filled-shapes.md)
-   [<span data-ttu-id="adf50-123">字型和文字</span><span class="sxs-lookup"><span data-stu-id="adf50-123">Fonts and Text</span></span>](fonts-and-text.md)
-   [<span data-ttu-id="adf50-124">線條和曲線</span><span class="sxs-lookup"><span data-stu-id="adf50-124">Lines and Curves</span></span>](lines-and-curves.md)
-   [<span data-ttu-id="adf50-125">元</span><span class="sxs-lookup"><span data-stu-id="adf50-125">Metafiles</span></span>](metafiles.md)
-   [<span data-ttu-id="adf50-126">多顯示器監視</span><span class="sxs-lookup"><span data-stu-id="adf50-126">Multiple Display Monitors</span></span>](multiple-display-monitors.md)
-   [<span data-ttu-id="adf50-127">繪製和繪製</span><span class="sxs-lookup"><span data-stu-id="adf50-127">Painting and Drawing</span></span>](painting-and-drawing.md)
-   [<span data-ttu-id="adf50-128">路徑</span><span class="sxs-lookup"><span data-stu-id="adf50-128">Paths</span></span>](paths.md)
-   [<span data-ttu-id="adf50-129">手寫筆</span><span class="sxs-lookup"><span data-stu-id="adf50-129">Pens</span></span>](pens.md)
-   <span data-ttu-id="adf50-130">[列印和列印多工緩衝處理器](/previous-versions//dd162860(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="adf50-130">[Printing and Print Spooler](/previous-versions//dd162860(v=vs.85))</span></span>
-   [<span data-ttu-id="adf50-131">矩形</span><span class="sxs-lookup"><span data-stu-id="adf50-131">Rectangles</span></span>](rectangles.md)
-   [<span data-ttu-id="adf50-132">區域</span><span class="sxs-lookup"><span data-stu-id="adf50-132">Regions</span></span>](regions.md)

## <a name="related-topics"></a><span data-ttu-id="adf50-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="adf50-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf50-134">DirectX</span><span class="sxs-lookup"><span data-stu-id="adf50-134">DirectX</span></span>](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[<span data-ttu-id="adf50-135">GDI+</span><span class="sxs-lookup"><span data-stu-id="adf50-135">GDI+</span></span>](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[<span data-ttu-id="adf50-136">Opengl</span><span class="sxs-lookup"><span data-stu-id="adf50-136">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="adf50-137">Windows 映像取得</span><span class="sxs-lookup"><span data-stu-id="adf50-137">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> </dl>

 

 
