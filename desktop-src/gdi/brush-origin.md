---
description: 當應用程式呼叫繪圖函式來繪製圖形時，系統會將筆刷放置於繪製作業的開頭，然後將筆刷點陣圖中的圖元對應至視窗原點的工作區，也就是視窗的左上角。
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: 筆刷來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568002"
---
# <a name="brush-origin"></a><span data-ttu-id="b4964-103">筆刷來源</span><span class="sxs-lookup"><span data-stu-id="b4964-103">Brush Origin</span></span>

<span data-ttu-id="b4964-104">當應用程式呼叫繪圖函式來繪製圖形時，系統會將筆刷放置於繪製作業的開頭，然後將筆刷點陣圖中的圖元對應至 *視窗原點* 的工作區，也就是視窗的左上角。</span><span class="sxs-lookup"><span data-stu-id="b4964-104">When an application calls a drawing function to paint a shape, the system positions a brush at the start of the paint operation and maps a pixel in the brush bitmap to the client area at the *window origin*, which is the upper-left corner of the window.</span></span> <span data-ttu-id="b4964-105">系統對應的圖元座標稱為 *筆刷原點*。</span><span class="sxs-lookup"><span data-stu-id="b4964-105">The coordinates of the pixel that the system maps are called the *brush origin*.</span></span> <span data-ttu-id="b4964-106">預設筆刷原點位於筆刷點陣圖的左上角，位於座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="b4964-106">The default brush origin is located in the upper-left corner of the brush bitmap, at the coordinates (0,0).</span></span> <span data-ttu-id="b4964-107">然後系統會將筆刷複製到工作區，形成與點陣圖高度一樣的模式。</span><span class="sxs-lookup"><span data-stu-id="b4964-107">The system then copies the brush across the client area, forming a pattern that is as tall as the bitmap.</span></span> <span data-ttu-id="b4964-108">複製作業會繼續（逐列），直到填滿整個工作區為止。</span><span class="sxs-lookup"><span data-stu-id="b4964-108">The copy operation continues, row by row, until the entire client area is filled.</span></span> <span data-ttu-id="b4964-109">不過，筆刷模式只會顯示在指定圖形的界限內。</span><span class="sxs-lookup"><span data-stu-id="b4964-109">However, the brush pattern is visible only within the boundaries of the specified shape.</span></span>

<span data-ttu-id="b4964-110">在某些情況下，不應使用預設筆刷來源。</span><span class="sxs-lookup"><span data-stu-id="b4964-110">There are instances when the default brush origin should not be used.</span></span> <span data-ttu-id="b4964-111">例如，應用程式可能需要使用相同的筆刷來繪製其父視窗和子視窗的背景，並將子視窗的背景與父視窗的背景混合。</span><span class="sxs-lookup"><span data-stu-id="b4964-111">For example, it may be necessary for an application to use the same brush to paint the backgrounds of its parent and child windows and blend a child window's background with that of the parent window.</span></span> <span data-ttu-id="b4964-112">若要這樣做，應用程式應該呼叫 [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) 函式，並將原點移至所需的圖元數目，以重設筆刷原點。</span><span class="sxs-lookup"><span data-stu-id="b4964-112">To do this, the application should reset the brush origin by calling the [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) function and shifting the origin the required number of pixels.</span></span> <span data-ttu-id="b4964-113"> (應用程式可以藉由呼叫 [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) 函式來取得目前的筆刷原點。 ) </span><span class="sxs-lookup"><span data-stu-id="b4964-113">(An application can retrieve the current brush origin by calling the [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) function.)</span></span>

<span data-ttu-id="b4964-114">下圖顯示使用應用程式定義的筆刷填滿的五方星形。</span><span class="sxs-lookup"><span data-stu-id="b4964-114">The following illustration shows a five-pointed star filled by using an application-defined brush.</span></span> <span data-ttu-id="b4964-115">下圖顯示筆刷的放大影像，以及繪製作業開始時所對應的位置。</span><span class="sxs-lookup"><span data-stu-id="b4964-115">The illustration shows a zoomed image of the brush, as well as the location to which it was mapped at the beginning of the paint operation.</span></span>

![圖例顯示筆刷原點對應至視窗來源](images/csbru-01.png)

 

 



