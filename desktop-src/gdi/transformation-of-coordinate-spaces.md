---
description: 座標空間是以笛卡兒座標系統為基礎的平面空間。
ms.assetid: 1a232030-8561-4b57-b274-dca0a8b3e3a1
title: 座標空間的轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1bca3d7190c4566ea7548166134ff745cc5e2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853007"
---
# <a name="transformation-of-coordinate-spaces"></a><span data-ttu-id="6fb7d-103">座標空間的轉換</span><span class="sxs-lookup"><span data-stu-id="6fb7d-103">Transformation of Coordinate Spaces</span></span>

<span data-ttu-id="6fb7d-104">*座標空間* 是以笛卡兒座標系統為基礎的平面空間。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-104">A *coordinate space* is a planar space based on the Cartesian coordinate system.</span></span> <span data-ttu-id="6fb7d-105">這個系統會提供一種方法來指定平面上每個點的位置。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-105">This system provides a means of specifying the location of each point on a plane.</span></span> <span data-ttu-id="6fb7d-106">它需要兩個垂直和相等長度的座標軸。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-106">It requires two axes that are perpendicular and equal in length.</span></span> <span data-ttu-id="6fb7d-107">下圖顯示座標空間。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-107">The following illustration shows a coordinate space.</span></span>

![座標空間的圖例，顯示來源、兩個軸，以及每個軸的最大值和最小值](images/cstrn-07.png)

<span data-ttu-id="6fb7d-109">系統支援四個座標空間，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-109">The system supports four coordinate spaces, as described in the following table.</span></span>



| <span data-ttu-id="6fb7d-110">座標空間</span><span class="sxs-lookup"><span data-stu-id="6fb7d-110">Coordinate space</span></span> | <span data-ttu-id="6fb7d-111">Description</span><span class="sxs-lookup"><span data-stu-id="6fb7d-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb7d-112">world</span><span class="sxs-lookup"><span data-stu-id="6fb7d-112">world</span></span>            | <span data-ttu-id="6fb7d-113">選擇性地當做圖形轉換的起始座標空間使用。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-113">Used optionally as the starting coordinate space for graphics transformations.</span></span> <span data-ttu-id="6fb7d-114">它允許縮放、轉譯、旋轉、剪下和反映。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-114">It allows scaling, translation, rotation, shearing, and reflection.</span></span> <span data-ttu-id="6fb7d-115">全球空間測量 2 ^ 32 個單位，高達 2 ^ 32 個單位寬。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-115">World space measures 2^32 units high by 2^32 units wide.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="6fb7d-116">頁面</span><span class="sxs-lookup"><span data-stu-id="6fb7d-116">page</span></span>             | <span data-ttu-id="6fb7d-117">用來作為全球空間之後的下一個空格，或做為圖形轉換的開始空間。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-117">Used either as the next space after world space or as the starting space for graphics transformations.</span></span> <span data-ttu-id="6fb7d-118">它會設定對應模式。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-118">It sets the mapping mode.</span></span> <span data-ttu-id="6fb7d-119">頁面空間也會測量 2 ^ 32 個單位，高達 2 ^ 32 個單位寬。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-119">Page space also measures 2^32 units high by 2^32 units wide.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6fb7d-120">裝置</span><span class="sxs-lookup"><span data-stu-id="6fb7d-120">device</span></span>           | <span data-ttu-id="6fb7d-121">用來做為頁面空間之後的下一個空格。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-121">Used as the next space after page space.</span></span> <span data-ttu-id="6fb7d-122">它只允許轉譯，可確保裝置空間的來源會對應到實體裝置空間中的適當位置。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-122">It only allows translation, which ensures the origin of the device space maps to the proper location in physical device space.</span></span> <span data-ttu-id="6fb7d-123">裝置空間測量 2 ^ 27 個單位，高達 2 ^ 27 個單位寬。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-123">Device space measures 2^27 units high by 2^27 units wide.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="6fb7d-124">實體裝置</span><span class="sxs-lookup"><span data-stu-id="6fb7d-124">physical device</span></span>  | <span data-ttu-id="6fb7d-125">最後 (輸出) 空間以進行圖形轉換。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-125">The final (output) space for graphics transformations.</span></span> <span data-ttu-id="6fb7d-126">它通常是指應用程式視窗的工作區。不過，它也可以包含整個桌面、完整的視窗 (包括框架、標題列和功能表列) ，或是印表機或繪圖器紙的頁面，視取得裝置內容控制碼的函式而定。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-126">It usually refers to the client area of the application window; however, it can also include the entire desktop, a complete window (including the frame, title bar, and menu bar), or a page of printer or plotter paper, depending on the function that obtained the handle to the device context.</span></span> <span data-ttu-id="6fb7d-127">實體裝置維度會根據顯示器、印表機或繪圖器技術所設定的維度而有所不同。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-127">Physical device dimensions vary according to the dimensions set by the display, printer, or plotter technology.</span></span> |



 

<span data-ttu-id="6fb7d-128">頁面空間可與裝置空間搭配使用，為應用程式提供與裝置無關的單位，例如毫米和英寸。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-128">Page space works with device space to provide applications with device-independent units, such as millimeters and inches.</span></span> <span data-ttu-id="6fb7d-129">本總覽是指世界空間和頁面空間的邏輯空間。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-129">This overview refers to both world space and page space as logical space.</span></span>

<span data-ttu-id="6fb7d-130">為了描述實體裝置上的輸出，系統會使用轉換將矩形區域中的 (或地圖) 一個座標空間複製到下一個座標空間，直到輸出在實體裝置上全部出現為止。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-130">To depict output on a physical device, the system copies (or maps) a rectangular region from one coordinate space into the next using a transformation until the output appears in its entirety on the physical device.</span></span> <span data-ttu-id="6fb7d-131">如果應用程式已呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，則對應會在應用程式的世界空間中開始進行：否則，對應會出現在頁面空間中。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-131">Mapping begins in the application's world space if the application has called the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function; otherwise, mapping occurs in page space.</span></span> <span data-ttu-id="6fb7d-132">當系統將矩形區域內的每個點從某個空間複製到另一個空間時，它會套用稱為轉換的演算法。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-132">As the system copies each point within the rectangular region from one space into another, it applies an algorithm called a transformation.</span></span> <span data-ttu-id="6fb7d-133">*轉換* 會改變 (或轉換) 從某個座標空間複製到另一個座標空間的物件大小、方向和圖形。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-133">A *transformation* alters (or transforms) the size, orientation, and shape of objects that are copied from one coordinate space into another.</span></span> <span data-ttu-id="6fb7d-134">雖然轉換會影響整個物件，但它會套用至物件中的每個點或每一行。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-134">Although a transformation affects an object as a whole, it is applied to each point, or to each line, in the object.</span></span>

<span data-ttu-id="6fb7d-135">下圖顯示使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函數執行的一般轉換。</span><span class="sxs-lookup"><span data-stu-id="6fb7d-135">The following illustration shows a typical transformation performed by using the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function.</span></span>

![圖例顯示在世界空間、頁面空間、裝置空間和裝置中，變更大小和位置的矩形](images/cstrn-08.png)

 

 



