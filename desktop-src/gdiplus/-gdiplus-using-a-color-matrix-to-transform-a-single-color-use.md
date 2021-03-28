---
description: Windows GDI + 提供用來儲存和操作影像的影像和點陣圖類別。
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: 使用色彩矩陣轉換單一色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560435"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a><span data-ttu-id="4dc57-103">使用色彩矩陣轉換單一色彩</span><span class="sxs-lookup"><span data-stu-id="4dc57-103">Using a Color Matrix to Transform a Single Color</span></span>

<span data-ttu-id="4dc57-104">Windows GDI + 提供用來儲存和操作影像的 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 和 [**點陣圖**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 類別。</span><span class="sxs-lookup"><span data-stu-id="4dc57-104">Windows GDI+ provides the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) classes for storing and manipulating images.</span></span> <span data-ttu-id="4dc57-105">**影像** 和 **點陣圖** 物件會將每個圖元的色彩儲存為32位數位：紅色、綠色、藍色和 Alpha 各有8位。</span><span class="sxs-lookup"><span data-stu-id="4dc57-105">**Image** and **Bitmap** objects store the color of each pixel as a 32-bit number: 8 bits each for red, green, blue, and alpha.</span></span> <span data-ttu-id="4dc57-106">四個元件的每一個都是從0到255的數位，0代表沒有濃度，而255代表完整強度。</span><span class="sxs-lookup"><span data-stu-id="4dc57-106">Each of the four components is a number from 0 through 255, with 0 representing no intensity and 255 representing full intensity.</span></span> <span data-ttu-id="4dc57-107">Alpha 元件會指定色彩的透明度：0是完全透明的，而255則完全不透明。</span><span class="sxs-lookup"><span data-stu-id="4dc57-107">The alpha component specifies the transparency of the color: 0 is fully transparent, and 255 is fully opaque.</span></span>

<span data-ttu-id="4dc57-108">色彩向量是表單的4個元組， (紅色、綠色、藍色、Alpha) 。</span><span class="sxs-lookup"><span data-stu-id="4dc57-108">A color vector is a 4-tuple of the form (red, green, blue, alpha).</span></span> <span data-ttu-id="4dc57-109">例如，色彩向量 (0、255、0、255) 代表沒有紅色或藍色的不透明色彩，但具有全強度的綠色。</span><span class="sxs-lookup"><span data-stu-id="4dc57-109">For example, the color vector (0, 255, 0, 255) represents an opaque color that has no red or blue, but has green at full intensity.</span></span>

<span data-ttu-id="4dc57-110">表示色彩的另一個慣例會使用數位1來表示最大強度，並使用數位0表示最小強度。</span><span class="sxs-lookup"><span data-stu-id="4dc57-110">Another convention for representing colors uses the number 1 for maximum intensity and the number 0 for minimum intensity.</span></span> <span data-ttu-id="4dc57-111">使用該慣例時，上一段所述的色彩會以向量 (0、1、0、1) 表示。</span><span class="sxs-lookup"><span data-stu-id="4dc57-111">Using that convention, the color described in the preceding paragraph would be represented by the vector (0, 1, 0, 1).</span></span> <span data-ttu-id="4dc57-112">GDI + 在執行色彩轉換時，會使用1的慣例作為完整強度。</span><span class="sxs-lookup"><span data-stu-id="4dc57-112">GDI+ uses the convention of 1 as full intensity when it performs color transformations.</span></span>

<span data-ttu-id="4dc57-113">您可以將線性轉換 (旋轉、縮放和類似的) ，藉由使用4×4矩陣來乘以色彩向量。</span><span class="sxs-lookup"><span data-stu-id="4dc57-113">You can apply linear transformations (rotation, scaling, and the like) to color vectors by multiplying by a 4 ×4 matrix.</span></span> <span data-ttu-id="4dc57-114">不過，您無法使用4×4矩陣來執行 (非線性) 的轉譯。</span><span class="sxs-lookup"><span data-stu-id="4dc57-114">However, you cannot use a 4 ×4 matrix to perform a translation (nonlinear).</span></span> <span data-ttu-id="4dc57-115">如果您新增了虛擬的第五座標 (例如，數位 1) 至每個色彩向量，則可以使用5×5矩陣來套用線性轉換和翻譯的任何組合。</span><span class="sxs-lookup"><span data-stu-id="4dc57-115">If you add a dummy fifth coordinate (for example, the number 1) to each of the color vectors, you can use a 5 ×5 matrix to apply any combination of linear transformations and translations.</span></span> <span data-ttu-id="4dc57-116">由線性轉換所組成的轉換，後面接著平移，稱為仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="4dc57-116">A transformation consisting of a linear transformation followed by a translation is called an affine transformation.</span></span> <span data-ttu-id="4dc57-117">代表仿射轉換的5×5矩陣稱為4個空間轉換的同質矩陣。</span><span class="sxs-lookup"><span data-stu-id="4dc57-117">A 5 ×5 matrix that represents an affine transformation is called a homogeneous matrix for a 4-space transformation.</span></span> <span data-ttu-id="4dc57-118">5×5同質矩陣的第五個數據列和第五個數據行中的元素必須是1，而第五個數據行中的所有其他專案都必須是0。</span><span class="sxs-lookup"><span data-stu-id="4dc57-118">The element in the fifth row and fifth column of a 5 ×5 homogeneous matrix must be 1, and all of the other entries in the fifth column must be 0.</span></span>

<span data-ttu-id="4dc57-119">例如，假設您想要從色彩 (0.2、0.0、0.4、1.0) 開始，並套用下列轉換：</span><span class="sxs-lookup"><span data-stu-id="4dc57-119">For example, suppose you want to start with the color (0.2, 0.0, 0.4, 1.0) and apply the following transformations:</span></span>

1.  <span data-ttu-id="4dc57-120">兩倍的紅色元件</span><span class="sxs-lookup"><span data-stu-id="4dc57-120">Double the red component</span></span>
2.  <span data-ttu-id="4dc57-121">將0.2 新增至紅色、綠色和藍色的元件</span><span class="sxs-lookup"><span data-stu-id="4dc57-121">Add 0.2 to the red, green, and blue components</span></span>

<span data-ttu-id="4dc57-122">下列矩陣乘法將依列出的循序執行一組轉換。</span><span class="sxs-lookup"><span data-stu-id="4dc57-122">The following matrix multiplication will perform the pair of transformations in the order listed.</span></span>

![圖例顯示數位的5x1 矩陣乘以5x5 矩陣，以建立新的5x1 矩陣](images/recoloring01.png)

<span data-ttu-id="4dc57-124">色彩矩陣的元素會根據 (以零為基礎的) 依資料列和資料行來編制索引。</span><span class="sxs-lookup"><span data-stu-id="4dc57-124">The elements of a color matrix are indexed (zero-based) by row and then column.</span></span> <span data-ttu-id="4dc57-125">例如，第五個數據列和第三個數據行中的專案會以 M \[ 4 \] \[ 2 表示 \] 。</span><span class="sxs-lookup"><span data-stu-id="4dc57-125">For example, the entry in the fifth row and third column of matrix M is denoted by M\[4\]\[2\].</span></span>

<span data-ttu-id="4dc57-126">下圖中所示的5×5識別矩陣 (，) 在對角線上具有1s，其他地方則為0。</span><span class="sxs-lookup"><span data-stu-id="4dc57-126">The 5 ×5 identity matrix (shown in the following illustration) has 1s on the diagonal and 0s everywhere else.</span></span> <span data-ttu-id="4dc57-127">如果您將色彩向量乘以標識矩陣，色彩向量不會變更。</span><span class="sxs-lookup"><span data-stu-id="4dc57-127">If you multiply a color vector by the identity matrix, the color vector does not change.</span></span> <span data-ttu-id="4dc57-128">形成色彩轉換矩陣的方便方式，就是從標識矩陣開始著手，然後再進行一項小變更來產生所需的轉換。</span><span class="sxs-lookup"><span data-stu-id="4dc57-128">A convenient way to form the matrix of a color transformation is to start with the identity matrix and make a small change that produces the desired transformation.</span></span>

![顯示5x5 身分識別矩陣的圖例;從左上角到右下角的 1-10，其他地方則為0](images/recoloring02.png)

<span data-ttu-id="4dc57-130">如需矩陣和轉換的詳細討論，請參閱 [座標系統和轉換](-gdiplus-coordinate-systems-and-transformations-about.md)。</span><span class="sxs-lookup"><span data-stu-id="4dc57-130">For a more detailed discussion of matrices and transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="4dc57-131">下列範例會取得全為一種色彩 (0.2、0.0、0.4、1.0) 的影像，並套用先前段落中所述的轉換。</span><span class="sxs-lookup"><span data-stu-id="4dc57-131">The following example takes an image that is all one color (0.2, 0.0, 0.4, 1.0) and applies the transformation described in the preceding paragraphs.</span></span>


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="4dc57-132">下圖顯示左邊的原始影像，以及右邊的已轉換影像。</span><span class="sxs-lookup"><span data-stu-id="4dc57-132">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![<span data-ttu-id="4dc57-133">圖例顯示以深色純色填滿的矩形，然後以較淺的純色填滿一個</span><span class="sxs-lookup"><span data-stu-id="4dc57-133">illustration showing a rectangle filled by a dark solid color and then one filled by a lighter solid color</span></span> ](images/colortrans1.png)

<span data-ttu-id="4dc57-134">上述範例中的程式碼會使用下列步驟來執行重新著色：</span><span class="sxs-lookup"><span data-stu-id="4dc57-134">The code in the preceding example uses the following steps to perform the recoloring:</span></span>

1.  <span data-ttu-id="4dc57-135">初始化 [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) 結構。</span><span class="sxs-lookup"><span data-stu-id="4dc57-135">Initialize a [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>
2.  <span data-ttu-id="4dc57-136">建立 [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes)物件，並將 [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix)結構的位址傳遞至 **ImageAttributes** 物件的 [**ImageAttributes：： SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix)方法。</span><span class="sxs-lookup"><span data-stu-id="4dc57-136">Create an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object and pass the address of the [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object.</span></span>
3.  <span data-ttu-id="4dc57-137">將 [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes)物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 [DrawImage 方法](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))方法。</span><span class="sxs-lookup"><span data-stu-id="4dc57-137">Pass the address of the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

 

 



