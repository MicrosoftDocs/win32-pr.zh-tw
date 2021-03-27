---
description: 您可以藉由指定原始影像左上角、右上角和左下角的目的地點，來旋轉、反映及扭曲影像。
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: 旋轉、反映及扭曲影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943942"
---
# <a name="rotating-reflecting-and-skewing-images"></a><span data-ttu-id="13ee1-103">旋轉、反映及扭曲影像</span><span class="sxs-lookup"><span data-stu-id="13ee1-103">Rotating, Reflecting, and Skewing Images</span></span>

<span data-ttu-id="13ee1-104">您可以藉由指定原始影像左上角、右上角和左下角的目的地點，來旋轉、反映及扭曲影像。</span><span class="sxs-lookup"><span data-stu-id="13ee1-104">You can rotate, reflect, and skew an image by specifying destination points for the upper-left, upper-right, and lower-left corners of the original image.</span></span> <span data-ttu-id="13ee1-105">三個目的地點決定將原始矩形影像對應至平行四邊形的仿射轉換。</span><span class="sxs-lookup"><span data-stu-id="13ee1-105">The three destination points determine an affine transformation that maps the original rectangular image to a parallelogram.</span></span> <span data-ttu-id="13ee1-106"> (原始影像的右下角會對應到平行四邊形的第四個角落，這是從三個指定的目的點計算而來。 ) </span><span class="sxs-lookup"><span data-stu-id="13ee1-106">(The lower-right corner of the original image is mapped to the fourth corner of the parallelogram, which is calculated from the three specified destination points.)</span></span>

<span data-ttu-id="13ee1-107">例如，假設原始影像是左上角的矩形，位於 (0、0) 、右上角 (100、0) 和左下角，位於 (0，50) 。</span><span class="sxs-lookup"><span data-stu-id="13ee1-107">For example, suppose the original image is a rectangle with upper-left corner at (0, 0), upper-right corner at (100, 0), and lower-left corner at (0, 50).</span></span> <span data-ttu-id="13ee1-108">現在假設我們將這三個點對應到目的地點，如下所示。</span><span class="sxs-lookup"><span data-stu-id="13ee1-108">Now suppose we map those three points to destination points as follows.</span></span>



| <span data-ttu-id="13ee1-109">原始點</span><span class="sxs-lookup"><span data-stu-id="13ee1-109">Original point</span></span>       | <span data-ttu-id="13ee1-110">目的地點</span><span class="sxs-lookup"><span data-stu-id="13ee1-110">Destination point</span></span> |
|----------------------|-------------------|
| <span data-ttu-id="13ee1-111">左上 (0、0) </span><span class="sxs-lookup"><span data-stu-id="13ee1-111">Upper-left (0, 0)</span></span>    | <span data-ttu-id="13ee1-112">(200, 20)</span><span class="sxs-lookup"><span data-stu-id="13ee1-112">(200, 20)</span></span>         |
| <span data-ttu-id="13ee1-113">右上角的 (100，0) </span><span class="sxs-lookup"><span data-stu-id="13ee1-113">Upper-right (100, 0)</span></span> | <span data-ttu-id="13ee1-114">(110, 100)</span><span class="sxs-lookup"><span data-stu-id="13ee1-114">(110, 100)</span></span>        |
| <span data-ttu-id="13ee1-115">左下 (0、50) </span><span class="sxs-lookup"><span data-stu-id="13ee1-115">Lower-left (0, 50)</span></span>   | <span data-ttu-id="13ee1-116">(250, 30)</span><span class="sxs-lookup"><span data-stu-id="13ee1-116">(250, 30)</span></span>         |



 

<span data-ttu-id="13ee1-117">下圖顯示原始影像和對應至平行四邊形的影像。</span><span class="sxs-lookup"><span data-stu-id="13ee1-117">The following illustration shows the original image and the image mapped to the parallelogram.</span></span> <span data-ttu-id="13ee1-118">原始影像已扭曲、反映、旋轉和轉譯。</span><span class="sxs-lookup"><span data-stu-id="13ee1-118">The original image has been skewed, reflected, rotated, and translated.</span></span> <span data-ttu-id="13ee1-119">沿著原始影像上邊緣的 X 軸會對應到 (200、20) 和 (110，100) 執行的行。</span><span class="sxs-lookup"><span data-stu-id="13ee1-119">The x-axis along the top edge of the original image is mapped to the line that runs through (200, 20) and (110, 100).</span></span> <span data-ttu-id="13ee1-120">沿著原始影像左邊緣的 y 軸，會對應至透過 (200、20) 和 (250，30) 執行的線條。</span><span class="sxs-lookup"><span data-stu-id="13ee1-120">The y-axis along the left edge of the original image is mapped to the line that runs through (200, 20) and (250, 30).</span></span>

![圖例顯示座標軸原點的彩色條紋，以及扭曲和不同位置、旋轉和大小的相同條紋](images/stripes1.png)

<span data-ttu-id="13ee1-122">下列範例會產生上圖所示的影像。</span><span class="sxs-lookup"><span data-stu-id="13ee1-122">The following example produces the images shown in the preceding illustration.</span></span>


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



<span data-ttu-id="13ee1-123">下圖顯示套用至照片影像的類似轉換。</span><span class="sxs-lookup"><span data-stu-id="13ee1-123">The following illustration shows a similar transformation applied to a photographic image.</span></span>

![顯示相同相片兩次的圖例;第二個是反轉、扭曲，而且有不同的大小、旋轉和位置](images/transformedclimber.png)

<span data-ttu-id="13ee1-125">下圖顯示套用至中繼檔的類似轉換。</span><span class="sxs-lookup"><span data-stu-id="13ee1-125">The following illustration shows a similar transformation applied to a metafile.</span></span>

![顯示圖形和文字的圖例，然後以不同的位置、旋轉和大小進行反轉、扭曲及調整大小](images/transformedmetafile.png)

 

 



