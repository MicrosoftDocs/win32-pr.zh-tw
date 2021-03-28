---
description: 大部分的 CAD 和繪圖應用程式都會提供可調整使用者所建立之輸出的功能。
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: 調整大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973524"
---
# <a name="scaling"></a><span data-ttu-id="2ae2c-103">調整大小</span><span class="sxs-lookup"><span data-stu-id="2ae2c-103">Scaling</span></span>

<span data-ttu-id="2ae2c-104">大部分的 CAD 和繪圖應用程式都會提供可調整使用者所建立之輸出的功能。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-104">Most CAD and drawing applications provide features that scale output created by the user.</span></span> <span data-ttu-id="2ae2c-105">包含調整 (或縮放) 功能的應用程式會呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，將適當的世界空間設定為頁面空間轉換。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-105">Applications that include scaling (or zoom) capabilities call the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="2ae2c-106">此函式會接收 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，其中包含適當的值。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="2ae2c-107">XFORM 的 eM11 和 eM22 成員分別指定水準和垂直縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical scaling components, respectively.</span></span>

<span data-ttu-id="2ae2c-108">進行 *調整* 時，會根據 X 軸或 y 軸來延展或壓縮組成物件的垂直和水平線條 (或向量) 。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-108">When *scaling* occurs, the vertical and horizontal lines (or vectors), that constitute an object, are stretched or compressed with respect to the x- or y-axis.</span></span> <span data-ttu-id="2ae2c-109">下圖顯示從全局座標空間複製到頁面座標空間時，垂直縮放至其原始高度的兩倍的 20 x 20 單位矩形。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-109">The following illustration shows a 20-by-20-unit rectangle scaled vertically to twice its original height when copied from world-coordinate space to page-coordinate space.</span></span>

![圖例顯示世界空間中的小矩形，以及頁面空間中的高度](images/cstrn-10.png)

<span data-ttu-id="2ae2c-111">在上圖中，定義原始矩形的側邊量值20個單位的垂直線，而定義縮放矩形側邊量值40單位的垂直線則是垂直線條。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-111">In the preceding illustration, the vertical lines that define the original rectangle's side measure 20 units, while the vertical lines that define the scaled rectangle's sides measure 40 units.</span></span>

<span data-ttu-id="2ae2c-112">垂直調整可透過下列演算法來表示。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-112">Vertical scaling can be represented by the following algorithm.</span></span>

``` syntax
y' = y * Dy 
```

<span data-ttu-id="2ae2c-113">其中 y ' 是新的長度，y 是原始長度，而 Dy 是垂直縮放比例。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-113">Where y' is the new length, y is the original length, and Dy is the vertical scaling factor.</span></span>

<span data-ttu-id="2ae2c-114">水準調整可透過下列演算法來表示。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-114">Horizontal scaling can be represented by the following algorithm.</span></span>

``` syntax
x' = x * Dx 
```

<span data-ttu-id="2ae2c-115">其中 x 是新的長度，x 是原始長度，而 Dx 是水準縮放因數。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-115">Where x' is the new length, x is the original length, and Dx is the horizontal scaling factor.</span></span>

<span data-ttu-id="2ae2c-116">垂直和水準縮放轉換可以使用2乘2矩陣合併為單一作業。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-116">The vertical and horizontal scaling transformations can be combined into a single operation by using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

<span data-ttu-id="2ae2c-117">產生縮放轉換的2到2個矩陣包含下列值。</span><span class="sxs-lookup"><span data-stu-id="2ae2c-117">The 2-by-2 matrix that produced the scaling transformation contains the following values.</span></span>

``` syntax
|1    0| 
|0    2| 
```

 

 



