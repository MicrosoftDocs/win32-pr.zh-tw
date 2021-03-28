---
description: 如果您只將影像的左上角傳遞給 DrawImage 方法，Windows GDI + 可能會調整影像，這會降低效能。
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: 藉由避免自動調整來改善效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972876"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a><span data-ttu-id="91bb0-103">藉由避免自動調整來改善效能</span><span class="sxs-lookup"><span data-stu-id="91bb0-103">Improving Performance by Avoiding Automatic Scaling</span></span>

<span data-ttu-id="91bb0-104">如果您只將影像的左上角傳遞給 **DrawImage** 方法，WINDOWS gdi + 可能會調整影像，這會降低效能。</span><span class="sxs-lookup"><span data-stu-id="91bb0-104">If you pass only the upper-left corner of an image to the **DrawImage** method, Windows GDI+ might scale the image, which would decrease performance.</span></span>

<span data-ttu-id="91bb0-105">下列對 **DrawImage** 方法的呼叫會指定 (50 30) 的左上角，但不會指定目的地矩形：</span><span class="sxs-lookup"><span data-stu-id="91bb0-105">The following call to the **DrawImage** method specifies an upper-left corner of (50, 30) but does not specify a destination rectangle:</span></span>


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



<span data-ttu-id="91bb0-106">雖然這是最簡單的 **DrawImage** 方法版本（以所需的引數數目為限），但不一定是最有效率的。</span><span class="sxs-lookup"><span data-stu-id="91bb0-106">Although this is the easiest version of the **DrawImage** method in terms of the number of required arguments, it is not necessarily the most efficient.</span></span> <span data-ttu-id="91bb0-107">如果目前顯示裝置上的每英寸點數，與建立映射的裝置上的點數目不同，則 GDI + 會調整影像，讓其在目前顯示裝置上的實體大小盡可能靠近其在建立裝置上的實際大小。</span><span class="sxs-lookup"><span data-stu-id="91bb0-107">If the number of dots per inch on the current display device is different than the number of dots per inch on the device where the image was created, GDI+ scales the image so that its physical size on the current display device is as close as possible to its physical size on the device where it was created.</span></span>

<span data-ttu-id="91bb0-108">如果您想要避免這樣的調整，請將目的地矩形的寬度和高度傳遞給 **DrawImage** 方法。</span><span class="sxs-lookup"><span data-stu-id="91bb0-108">If you want to prevent such scaling, pass the width and height of a destination rectangle to the **DrawImage** method.</span></span> <span data-ttu-id="91bb0-109">下列範例會繪製相同的影像兩次。</span><span class="sxs-lookup"><span data-stu-id="91bb0-109">The following example draws the same image twice.</span></span> <span data-ttu-id="91bb0-110">在第一種情況下，不會指定目的矩形的寬度和高度，而且會自動調整影像。</span><span class="sxs-lookup"><span data-stu-id="91bb0-110">In the first case, the width and height of the destination rectangle are not specified, and the image is automatically scaled.</span></span> <span data-ttu-id="91bb0-111">在第二個案例中， (以圖元) 為單位測量的寬度和高度指定為與原始影像的寬度和高度相同。</span><span class="sxs-lookup"><span data-stu-id="91bb0-111">In the second case, the width and height (measured in pixels) of the destination rectangle are specified to be the same as the width and height of the original image.</span></span>


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



<span data-ttu-id="91bb0-112">下圖顯示呈現兩次的影像。</span><span class="sxs-lookup"><span data-stu-id="91bb0-112">The following illustration shows the image rendered twice.</span></span>

![視窗的螢幕擷取畫面，其中包含不同刻度的一個影像的兩個版本](images/scaledtexture1.png)

 

 



