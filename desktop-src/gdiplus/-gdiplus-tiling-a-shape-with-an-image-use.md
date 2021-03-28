---
description: 就像磚可以放在彼此旁以涵蓋樓層一樣，可以將矩形影像放在彼此旁，以填滿圖形) 的 (圖格。
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: 使用影像將圖形平平圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112945"
---
# <a name="tiling-a-shape-with-an-image"></a><span data-ttu-id="8c8cd-103">使用影像將圖形平平圖</span><span class="sxs-lookup"><span data-stu-id="8c8cd-103">Tiling a Shape with an Image</span></span>

<span data-ttu-id="8c8cd-104">就像磚可以放在彼此旁以涵蓋樓層一樣，可以將矩形影像放在彼此旁，以填滿圖形) 的 (圖格。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-104">Just as tiles can be placed next to each other to cover a floor, rectangular images can be placed next to each other to fill (tile) a shape.</span></span> <span data-ttu-id="8c8cd-105">若要並排顯示圖形的內部，請使用材質筆刷。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-105">To tile the interior of a shape, use a texture brush.</span></span> <span data-ttu-id="8c8cd-106">當您建立 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 物件時，您傳遞給函式的其中一個引數就是 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-106">When you construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, one of the arguments you pass to the constructor is the address of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="8c8cd-107">當您使用紋理筆刷繪製圖形的內部時，圖形會填入此影像的重複複本。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-107">When you use the texture brush to paint the interior of a shape, the shape is filled with repeated copies of this image.</span></span>

<span data-ttu-id="8c8cd-108">[**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)物件的 wrap 模式屬性會決定影像的導向方式，因為它會在矩形方格中重複。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-108">The wrap mode property of the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object determines how the image is oriented as it is repeated in a rectangular grid.</span></span> <span data-ttu-id="8c8cd-109">您可以讓格線中的所有圖格都有相同的方向，也可以讓影像從一個格線位置切換至下一個。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-109">You can make all the tiles in the grid have the same orientation, or you can make the image flip from one grid position to the next.</span></span> <span data-ttu-id="8c8cd-110">翻轉可以是水準、垂直或兩者。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-110">The flipping can be horizontal, vertical, or both.</span></span> <span data-ttu-id="8c8cd-111">下列範例示範如何使用不同類型的翻轉進行平鋪。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-111">The following examples demonstrate tiling with different types of flipping.</span></span>

## <a name="tiling-an-image"></a><span data-ttu-id="8c8cd-112">平鋪影像</span><span class="sxs-lookup"><span data-stu-id="8c8cd-112">Tiling an Image</span></span>

<span data-ttu-id="8c8cd-113">此範例使用下列75×75影像來磚出200×200矩形：</span><span class="sxs-lookup"><span data-stu-id="8c8cd-113">This example uses the following 75 ×75 image to tile a 200 ×200 rectangle:</span></span>

![此主題中做為其他圖例基底的圖例：在背景上的房屋和樹狀結構，並以矩形為中心](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="8c8cd-115">下圖顯示矩形如何與影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-115">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="8c8cd-116">請注意，所有圖格都有相同的方向;沒有任何翻轉。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-116">Note that all tiles have the same orientation; there is no flipping.</span></span>

![顯示在大型矩形中以水準和垂直方式重複的基底影像圖例](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a><span data-ttu-id="8c8cd-118">在並排平邊時水準翻轉影像</span><span class="sxs-lookup"><span data-stu-id="8c8cd-118">Flipping an Image Horizontally While Tiling</span></span>

<span data-ttu-id="8c8cd-119">此範例使用75×75影像來填滿200×200的矩形。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-119">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="8c8cd-120">Wrap 模式設定為水準翻轉影像。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-120">The wrap mode is set to flip the image horizontally.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="8c8cd-121">下圖顯示矩形如何與影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-121">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="8c8cd-122">請注意，當您在指定的資料列中，從一個圖格移至下一個磚時，影像會水準翻轉。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-122">Note that as you move from one tile to the next in a given row, the image is flipped horizontally.</span></span>

![此圖顯示水準重複的基底影像，但以水準方式反轉偶數的實例](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a><span data-ttu-id="8c8cd-124">在並排平邊時垂直翻轉影像</span><span class="sxs-lookup"><span data-stu-id="8c8cd-124">Flipping an Image Vertically While Tiling</span></span>

<span data-ttu-id="8c8cd-125">此範例使用75×75影像來填滿200×200的矩形。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-125">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="8c8cd-126">自動換行模式會設定為垂直翻轉影像。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-126">The wrap mode is set to flip the image vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="8c8cd-127">下圖顯示矩形如何與影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-127">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="8c8cd-128">請注意，當您在指定的資料行中，從一個圖格移至下一個磚時，影像會垂直翻轉。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-128">Note that as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![圖例顯示以水準和垂直方式重複的基底影像，但偶數的資料列會垂直反轉](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a><span data-ttu-id="8c8cd-130">在圖格時水準和垂直翻轉影像</span><span class="sxs-lookup"><span data-stu-id="8c8cd-130">Flipping an Image Horizontally and Vertically While Tiling</span></span>

<span data-ttu-id="8c8cd-131">此範例使用75×75影像來建立200×200矩形的磚。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-131">This example uses a 75 ×75 image to tile a 200 ×200 rectangle.</span></span> <span data-ttu-id="8c8cd-132">Wrap 模式設定為水準和垂直翻轉影像。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-132">The wrap mode is set to flip the image both horizontally and vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="8c8cd-133">下圖顯示矩形如何以影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-133">The following illustration shows how the rectangle is tiled by the image.</span></span> <span data-ttu-id="8c8cd-134">請注意，當您在指定的資料列中，從一個圖格移至下一個磚時，影像會水準翻轉，當您從某個圖格移至特定資料行中的下一個圖格時，影像會垂直翻轉。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-134">Note that as you move from one tile to the next in a given row, the image is flipped horizontally, and as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![顯示每個資料列中基底影像之替代實例水準翻轉的圖例，以及垂直翻轉的替換資料列](images/tile5.png)

 

 



