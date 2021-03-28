---
description: 有些應用程式會提供在工作區中繪製物件的扭曲功能。
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: 剪切
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193791"
---
# <a name="shear"></a><span data-ttu-id="2e520-103">剪切</span><span class="sxs-lookup"><span data-stu-id="2e520-103">Shear</span></span>

<span data-ttu-id="2e520-104">有些應用程式會提供在工作區中繪製物件的扭曲功能。</span><span class="sxs-lookup"><span data-stu-id="2e520-104">Some applications provide features that shear objects drawn in the client area.</span></span> <span data-ttu-id="2e520-105">使用切變功能的應用程式會使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，將世界空間中的適當值設定為頁面空間轉換。</span><span class="sxs-lookup"><span data-stu-id="2e520-105">Applications that use shear capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="2e520-106">此函式會接收 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，其中包含適當的值。</span><span class="sxs-lookup"><span data-stu-id="2e520-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="2e520-107">XFORM 的 eM12 和 eM21 成員分別指定水準和垂直 proportionality 常數。</span><span class="sxs-lookup"><span data-stu-id="2e520-107">The eM12 and eM21 members of XFORM specify the horizontal and vertical proportionality constants, respectively.</span></span>

<span data-ttu-id="2e520-108">*切變轉換* 有兩個元件。</span><span class="sxs-lookup"><span data-stu-id="2e520-108">There are two components of the *shear transformation*.</span></span> <span data-ttu-id="2e520-109">第一個改變物件中的垂直線;第二個改變水平線條。</span><span class="sxs-lookup"><span data-stu-id="2e520-109">The first alters the vertical lines in an object; the second alters the horizontal lines.</span></span> <span data-ttu-id="2e520-110">下圖顯示從世界空間複製到頁面空間時，水準切變的 20 x 單位矩形。</span><span class="sxs-lookup"><span data-stu-id="2e520-110">The following illustration shows a 20-by-20-unit rectangle sheared horizontally when copied from world space to page space.</span></span>

![圖例顯示世界空間中的矩形和頁面空間中的 trapeziod](images/cstrn-13.png)

<span data-ttu-id="2e520-112">水準切變可透過下列演算法來表示：</span><span class="sxs-lookup"><span data-stu-id="2e520-112">A horizontal shear can be represented by the following algorithm:</span></span>

``` syntax
x' = x + (Sx * y) 
```

<span data-ttu-id="2e520-113">其中 x 是原始 x 座標，Sx 是 proportionality 常數，而 x 是切變轉換的結果。</span><span class="sxs-lookup"><span data-stu-id="2e520-113">where x is the original x-coordinate, Sx is the proportionality constant, and x' is the result of the shear transformation.</span></span>

<span data-ttu-id="2e520-114">垂直切變可透過下列演算法來表示：</span><span class="sxs-lookup"><span data-stu-id="2e520-114">A vertical shear can be represented by the following algorithm:</span></span>

``` syntax
y' = y + (Sy * x) 
```

<span data-ttu-id="2e520-115">其中 y 是原始的 y 座標，Sy 是 proportionality 常數，y ' 是切變轉換的結果。</span><span class="sxs-lookup"><span data-stu-id="2e520-115">where y is the original y-coordinate, Sy is the proportionality constant, and y' is the result of the shear transformation.</span></span>

<span data-ttu-id="2e520-116">您可以使用2乘2矩陣，將水準切變和垂直切變轉換合併成單一作業。</span><span class="sxs-lookup"><span data-stu-id="2e520-116">The horizontal-shear and vertical-shear transformations can be combined into a single operation using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

<span data-ttu-id="2e520-117">產生切變的 2 x 2 矩陣包含下列值：</span><span class="sxs-lookup"><span data-stu-id="2e520-117">The 2-by-2 matrix that produced the shear contains the following values:</span></span>

``` syntax
|1    1| 
|0    1| 
```

 

 



