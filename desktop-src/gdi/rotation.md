---
description: 許多 CAD 應用程式提供的功能可旋轉在工作區中繪製的物件。
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: 旋轉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973712"
---
# <a name="rotation"></a><span data-ttu-id="0fd75-103">旋轉</span><span class="sxs-lookup"><span data-stu-id="0fd75-103">Rotation</span></span>

<span data-ttu-id="0fd75-104">許多 CAD 應用程式提供的功能可旋轉在工作區中繪製的物件。</span><span class="sxs-lookup"><span data-stu-id="0fd75-104">Many CAD applications provide features that rotate objects drawn in the client area.</span></span> <span data-ttu-id="0fd75-105">包含旋轉功能的應用程式會使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，將適當的世界空間設定為頁面空間轉換。</span><span class="sxs-lookup"><span data-stu-id="0fd75-105">Applications that include rotation capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="0fd75-106">此函式會接收 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，其中包含適當的值。</span><span class="sxs-lookup"><span data-stu-id="0fd75-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="0fd75-107">XFORM 的 eM11、eM12、eM21 和 eM22 成員分別指定、余弦、正弦、負正弦值和旋轉角度的余弦值。</span><span class="sxs-lookup"><span data-stu-id="0fd75-107">The eM11, eM12, eM21, and eM22 members of XFORM specify respectively, the cosine, sine, negative sine, and cosine of the angle of rotation.</span></span>

<span data-ttu-id="0fd75-108">發生 *輪替* 時，構成物件的點會根據座標空間原點旋轉。</span><span class="sxs-lookup"><span data-stu-id="0fd75-108">When *rotation* occurs, the points that constitute an object are rotated with respect to the coordinate-space origin.</span></span> <span data-ttu-id="0fd75-109">下圖顯示從全局座標空間複製到頁面座標空間時，20 x 20 單位的矩形旋轉30度。</span><span class="sxs-lookup"><span data-stu-id="0fd75-109">The following illustration shows a 20-by-20-unit rectangle rotated 30 degrees when copied from world-coordinate space to page-coordinate space.</span></span>

![顯示兩個座標空間的圖例：每個都有不同位置的矩形，以及不同的旋轉](images/cstrn-11.png)

<span data-ttu-id="0fd75-111">在上圖中，矩形中的每個點都是相對於座標空間原點旋轉30度。</span><span class="sxs-lookup"><span data-stu-id="0fd75-111">In the preceding illustration, each point in the rectangle was rotated 30 degrees with respect to the coordinate-space origin.</span></span>

<span data-ttu-id="0fd75-112">下列演算法會針對以角度 A 旋轉的點 (x、y ) 計算新的 x 座標 (x ' ) （相對於座標空間原點）。</span><span class="sxs-lookup"><span data-stu-id="0fd75-112">The following algorithm computes the new x-coordinate (x ') for a point (x,y ) that is rotated by angle A with respect to the coordinate-space origin.</span></span>

``` syntax
x' = (x * cos A) - (y * sin A) 
```

<span data-ttu-id="0fd75-113">下列演算法會計算點 (x，y ) 的 y 座標 (y ' ) ，而該點是以相對於原點的角度 A 旋轉。</span><span class="sxs-lookup"><span data-stu-id="0fd75-113">The following algorithm computes the y-coordinate (y ') for a point (x,y ) that is rotated by the angle A with respect to the origin.</span></span>

``` syntax
y' = (x * sin A) + (y * cos A) 
```

<span data-ttu-id="0fd75-114">這兩個旋轉轉換可以合併成 2 x 2 個矩陣，如下所示。</span><span class="sxs-lookup"><span data-stu-id="0fd75-114">The two rotation transformations can be combined in a 2-by-2 matrix as follows.</span></span>

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

<span data-ttu-id="0fd75-115">產生旋轉的2到2個矩陣包含下列值。</span><span class="sxs-lookup"><span data-stu-id="0fd75-115">The 2-by-2 matrix that produced the rotation contains the following values.</span></span>

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a><span data-ttu-id="0fd75-116">輪替演算法衍生</span><span class="sxs-lookup"><span data-stu-id="0fd75-116">Rotation Algorithm Derivation</span></span>

<span data-ttu-id="0fd75-117">旋轉演算法以三角函數的加法定理為基礎，表示兩個角度的三角函式 (A1 和 A2 ) 可以用兩個角度的三角函數表示。</span><span class="sxs-lookup"><span data-stu-id="0fd75-117">Rotation algorithms are based on trigonometry's addition theorem stating that the trigonometric function of a sum of two angles (A1 and A2 ) can be expressed in terms of the trigonometric functions of the two angles.</span></span>

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

<span data-ttu-id="0fd75-118">下圖顯示以逆時針方向旋轉至新位置 p 的點 p。</span><span class="sxs-lookup"><span data-stu-id="0fd75-118">The following illustration shows a point p rotated counterclockwise to a new position p'.</span></span> <span data-ttu-id="0fd75-119">此外，它會顯示兩個三角形，以從座標空間原點繪製到每個點，以及從每個點到 X 軸繪製的線條來形成。</span><span class="sxs-lookup"><span data-stu-id="0fd75-119">In addition, it shows two triangles formed by a line drawn from the coordinate-space origin to each point and a line drawn from each point through the x-axis.</span></span>

![顯示原點、p 和 p 的圖表，以及兩個三角形](images/cstrn-12.png)

<span data-ttu-id="0fd75-121">使用三角函數，可以透過將斜邊 h 的長度乘以 A1 的余弦值來取得點 p 的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="0fd75-121">Using trigonometry, the x-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the cosine of A1.</span></span>

``` syntax
x = h * cos A1 
```

<span data-ttu-id="0fd75-122">您可以藉由將斜邊 h 的長度乘以 A1 的正弦來取得點 p 的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="0fd75-122">The y-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the sine of A1.</span></span>

``` syntax
y = h * sin A1 
```

<span data-ttu-id="0fd75-123">同樣地，您可以將斜邊 h 的長度乘以 (A1 + A2 ) 的余弦值，以取得點 p 的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="0fd75-123">Likewise, the x-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the cosine of (A1 +A2 ).</span></span>

``` syntax
x' = h * cos (A1 + A2) 
```

<span data-ttu-id="0fd75-124">最後，可以藉由將斜邊 h 的長度乘以 (A1 + A2 ) 的正弦值，來取得 point p 的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="0fd75-124">Finally, the y-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the sine of (A1 +A2 ).</span></span>

``` syntax
y' = h * sin (A1 + A2) 
```

<span data-ttu-id="0fd75-125">使用加法定理，上述的演算法會變成下列各項：</span><span class="sxs-lookup"><span data-stu-id="0fd75-125">Using the addition theorem, the preceding algorithms become the following:</span></span>

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

<span data-ttu-id="0fd75-126">以角度 A2 旋轉的指定點的旋轉演算法，可以藉由針對每個出現的 (h \* Cos a1 ) 來取代 x，以及針對每個出現的 (h \* sin a1 ) 替代 y 來取得。</span><span class="sxs-lookup"><span data-stu-id="0fd75-126">The rotation algorithms for a given point rotated by angle A2 can be obtained by substituting x for each occurrence of (h \* cos A1 ) and by substituting y for each occurrence of (h \* sin A1 ).</span></span>

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



