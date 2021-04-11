---
description: 在 Direct3D 和視窗程式設計中，畫面上的物件是以周框矩形為參考。
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: " (Direct3D 9) 的矩形"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108457"
---
# <a name="rectangles-direct3d-9"></a><span data-ttu-id="a9b3a-103"> (Direct3D 9) 的矩形</span><span class="sxs-lookup"><span data-stu-id="a9b3a-103">Rectangles (Direct3D 9)</span></span>

<span data-ttu-id="a9b3a-104">在 Direct3D 和視窗程式設計中，畫面上的物件是以周框矩形為參考。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-104">Throughout Direct3D and Window programming, objects on the screen are referred to in terms of bounding rectangles.</span></span> <span data-ttu-id="a9b3a-105">週框的側邊永遠和螢幕的側邊平行，以讓矩形可由兩個點描述，這兩點為左上角和右下角。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-105">The sides of a bounding rectangle are always parallel to the sides of the screen, so the rectangle can be described by two points, the upper-left corner and lower-right corner.</span></span> <span data-ttu-id="a9b3a-106">大部分的應用程式會使用 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構，來攜帶在 blitting 至螢幕或執行點擊偵測時，所要使用的周框的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-106">Most applications use the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to carry information about a bounding rectangle to use when blitting to the screen or performing hit detection.</span></span>

<span data-ttu-id="a9b3a-107">在 c + + 中， [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構具有下列定義。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-107">In C++, the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure has the following definition.</span></span>


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



<span data-ttu-id="a9b3a-108">在先前的範例中，左上成員是繫結矩形的左上角的 x 座標和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-108">In the preceding example, the left and top members are the x- and y-coordinates of a bounding rectangle's upper-left corner.</span></span> <span data-ttu-id="a9b3a-109">同樣地，右下成員組成右下角的座標。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-109">Similarly, the right and bottom members make up the coordinates of the lower-right corner.</span></span> <span data-ttu-id="a9b3a-110">下圖顯示您可以視覺化這些值的方式。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-110">The following illustration shows how you can visualize these values.</span></span>

![左、上、右和下方值所繫結矩形的圖例](images/rect.png)

<span data-ttu-id="a9b3a-112">右緣的像素資料行和下緣的像素資料列不包含在 RECT 中。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-112">The column of pixels at the right edge and the row of pixels at the bottom edge are not included in the RECT.</span></span> <span data-ttu-id="a9b3a-113">例如，鎖定成員 {10, 10, 138, 138} 的 RECT 產生矩形寬度與高度為 128 像素的物件。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-113">For example, locking a RECT with members {10, 10, 138, 138} results in an object 128 pixels in width and height.</span></span>

<span data-ttu-id="a9b3a-114">在效率、一致性和易用性方面，所有的 Direct3D 展示函式都可搭配矩形使用。</span><span class="sxs-lookup"><span data-stu-id="a9b3a-114">In the interest of efficiency, consistency, and ease of use, all Direct3D presentation functions work with rectangles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9b3a-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9b3a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9b3a-116">座標系統和幾何</span><span class="sxs-lookup"><span data-stu-id="a9b3a-116">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
