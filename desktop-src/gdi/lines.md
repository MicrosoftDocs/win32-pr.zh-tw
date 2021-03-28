---
description: 線條是點陣顯示器上的反白顯示圖元 (或列印頁面上的一組點，) 由兩個點來識別：起點和結束點。
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: 線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cd678f782567e98d32ab7f8786d5b87aab1918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191937"
---
# <a name="lines"></a><span data-ttu-id="1c98c-103">線條</span><span class="sxs-lookup"><span data-stu-id="1c98c-103">Lines</span></span>

<span data-ttu-id="1c98c-104">線條是點陣顯示器上的反白顯示圖元 (或列印頁面上的一組點，) 由兩個點來識別：起點和結束點。</span><span class="sxs-lookup"><span data-stu-id="1c98c-104">A line is a set of highlighted pixels on a raster display (or a set of dots on a printed page) identified by two points: a starting point and an ending point.</span></span> <span data-ttu-id="1c98c-105">位於起點的圖元一律會包含在行中，而且一律會排除位於結束點的圖元。</span><span class="sxs-lookup"><span data-stu-id="1c98c-105">The pixel located at the starting point is always included in the line, and the pixel located at the ending point is always excluded.</span></span> <span data-ttu-id="1c98c-106">這種類型的 (有時稱為內含專屬。 ) </span><span class="sxs-lookup"><span data-stu-id="1c98c-106">(This kind of line is sometimes called inclusive-exclusive.)</span></span>

<span data-ttu-id="1c98c-107">當應用程式呼叫其中一個線條繪圖函式、圖形裝置介面 (GDI) ，或在某些情況下，設備磁碟機會判斷應該反白顯示的圖元。</span><span class="sxs-lookup"><span data-stu-id="1c98c-107">When an application calls one of the line-drawing functions, graphics device interface (GDI), or in some cases a device driver, determines which pixels should be highlighted.</span></span> <span data-ttu-id="1c98c-108">GDI 是動態連結程式庫 (DLL) ，可處理來自應用程式的圖形函式呼叫，並將這些呼叫傳遞給設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="1c98c-108">GDI is a dynamic-link library (DLL) that processes graphics function calls from an application and passes those calls to a device driver.</span></span> <span data-ttu-id="1c98c-109">設備磁碟機是接收來自 GDI 之輸入的 DLL、將輸入轉換成裝置命令，然後將這些命令傳遞給適當的裝置。</span><span class="sxs-lookup"><span data-stu-id="1c98c-109">A device driver is a DLL that receives input from GDI, converts the input to device commands, and passes those commands to the appropriate device.</span></span> <span data-ttu-id="1c98c-110">GDI 會使用數位差異分析器 (DDA) 來判斷可定義線條的一組圖元。</span><span class="sxs-lookup"><span data-stu-id="1c98c-110">GDI uses a digital differential analyzer (DDA) to determine the set of pixels that define a line.</span></span> <span data-ttu-id="1c98c-111">DDA 藉由檢查線條上的每個點，並在顯示介面上識別這些圖元， (或列印) 頁面上對應到點的點，來決定一組圖元。</span><span class="sxs-lookup"><span data-stu-id="1c98c-111">A DDA determines the set of pixels by examining each point on the line and identifying those pixels on the display surface (or dots on a printed page) that correspond to the points.</span></span> <span data-ttu-id="1c98c-112">下圖顯示的是線條、其起點、其結束點，以及使用簡單的 DDA 強調顯示的圖元。</span><span class="sxs-lookup"><span data-stu-id="1c98c-112">The following illustration shows a line, its starting point, its ending point, and the pixels highlighted by using a simple DDA.</span></span>

![圖例顯示圖元的方格、開始和結束點、線條，以及沿著直線的圖元陰影](images/cslcv-01.png)

<span data-ttu-id="1c98c-114">最簡單且最常見的 DDA 是 Bresenham 或增量，DDA。</span><span class="sxs-lookup"><span data-stu-id="1c98c-114">The simplest and most common DDA is the Bresenham, or incremental, DDA.</span></span> <span data-ttu-id="1c98c-115">此演算法的修改版本會在 Windows 中繪製線條。</span><span class="sxs-lookup"><span data-stu-id="1c98c-115">A modified version of this algorithm draws lines in Windows.</span></span> <span data-ttu-id="1c98c-116">為了簡單起見，會記下遞增的 DDA，但其誤差也會注明。</span><span class="sxs-lookup"><span data-stu-id="1c98c-116">The incremental DDA is noted for its simplicity, but it is also noted for its inaccuracy.</span></span> <span data-ttu-id="1c98c-117">因為它會四捨五入到最接近的整數值，所以有時無法表示應用程式所要求的原始程式列。</span><span class="sxs-lookup"><span data-stu-id="1c98c-117">Because it rounds off to the nearest integer value, it sometimes fails to represent the original line requested by the application.</span></span> <span data-ttu-id="1c98c-118">GDI 使用的 DDA 不會四捨五入到最接近的整數。</span><span class="sxs-lookup"><span data-stu-id="1c98c-118">The DDA used by GDI does not round off to the nearest integer.</span></span> <span data-ttu-id="1c98c-119">如此一來，這個新的 DDA 會產生輸出，有時會比應用程式所要求的原始程式列更接近外觀。</span><span class="sxs-lookup"><span data-stu-id="1c98c-119">As a result, this new DDA produces output that is sometimes much closer in appearance to the original line requested by the application.</span></span>

> [!Note]  
> <span data-ttu-id="1c98c-120">如果應用程式需要無法使用新的 DDA 達成的行輸出，它可以藉由呼叫 [**LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) 函式，並提供私用的 Dda ([**LineDDAProc**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)) 來繪製自己的行。</span><span class="sxs-lookup"><span data-stu-id="1c98c-120">If an application requires line output that cannot be achieved with the new DDA, it can draw its own lines by calling the [**LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) function and supplying a private DDA ([**LineDDAProc**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)).</span></span> <span data-ttu-id="1c98c-121">不過， **LineDDA** 函式繪製的線條速度會比線條繪圖函式慢許多。</span><span class="sxs-lookup"><span data-stu-id="1c98c-121">However, the **LineDDA** function draws lines much slower than the line-drawing functions.</span></span> <span data-ttu-id="1c98c-122">如果速度是主要考慮，請勿在應用程式中使用此函數。</span><span class="sxs-lookup"><span data-stu-id="1c98c-122">Do not use this function within an application if speed is a primary concern.</span></span>

 

<span data-ttu-id="1c98c-123">應用程式可以使用新的 DDA 來繪製單一線條和多個連接的線段。</span><span class="sxs-lookup"><span data-stu-id="1c98c-123">An application can use the new DDA to draw single lines and multiple, connected line segments.</span></span> <span data-ttu-id="1c98c-124">應用程式可以藉由呼叫 [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) 函數來繪製單一行。</span><span class="sxs-lookup"><span data-stu-id="1c98c-124">An application can draw a single line by calling the [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) function.</span></span> <span data-ttu-id="1c98c-125">此函式會從目前的位置（但不包括指定的結束點）繪製線條。</span><span class="sxs-lookup"><span data-stu-id="1c98c-125">This function draws a line from the current position up to, but not including, a specified ending point.</span></span> <span data-ttu-id="1c98c-126">應用程式可以藉由呼叫 [**彙總函式來**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) 繪製一連串的連接直線線段，提供指定每個線條區段之結束點的點陣列。</span><span class="sxs-lookup"><span data-stu-id="1c98c-126">An application can draw a series of connected line segments by calling the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function, supplying an array of points that specify the ending point of each line segment.</span></span> <span data-ttu-id="1c98c-127">應用程式可以藉由呼叫 [**PolyPolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) 函式，並提供必要的結束點，來繪製多個脫離的連接線區段。</span><span class="sxs-lookup"><span data-stu-id="1c98c-127">An application can draw multiple, disjointed series of connected line segments by calling the [**PolyPolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) function, supplying the required ending points.</span></span>

<span data-ttu-id="1c98c-128">下圖顯示藉由呼叫 [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)、彙總函式和 [**PolyPolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)函式所 [**建立的行**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)輸出。</span><span class="sxs-lookup"><span data-stu-id="1c98c-128">The following illustration shows line output created by calling the [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline), and [**PolyPolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) functions.</span></span>

![圖例顯示直線、"l" 形方塊，以及兩個顯示3d 的圖形](images/cslcv-02.png)

 

 



