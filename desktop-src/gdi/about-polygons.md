---
description: 多邊形是具有直邊的填滿形狀。
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: 關於多邊形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026469"
---
# <a name="about-polygons"></a><span data-ttu-id="ebb15-103">關於多邊形</span><span class="sxs-lookup"><span data-stu-id="ebb15-103">About Polygons</span></span>

<span data-ttu-id="ebb15-104">*多邊形* 是具有直邊的填滿形狀。</span><span class="sxs-lookup"><span data-stu-id="ebb15-104">A *polygon* is a filled shape with straight sides.</span></span> <span data-ttu-id="ebb15-105">多邊形的側邊使用目前的畫筆繪製。</span><span class="sxs-lookup"><span data-stu-id="ebb15-105">The sides of a polygon are drawn by using the current pen.</span></span> <span data-ttu-id="ebb15-106">當系統填滿多邊形時，它會使用目前的筆刷和目前的多邊形填滿模式。</span><span class="sxs-lookup"><span data-stu-id="ebb15-106">When the system fills a polygon, it uses the current brush and the current polygon fill mode.</span></span> <span data-ttu-id="ebb15-107">這兩種填滿模式（替代 (預設) 和繞組）會決定是否要填滿或省略複雜多邊形內的區域。</span><span class="sxs-lookup"><span data-stu-id="ebb15-107">The two fill modes, alternate (the default) and winding, determine whether regions within a complex polygon are filled or left unpainted.</span></span> <span data-ttu-id="ebb15-108">應用程式可以藉由呼叫 [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) 函式來選取其中一個模式。</span><span class="sxs-lookup"><span data-stu-id="ebb15-108">An application can select either mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="ebb15-109">如需多邊形填滿模式的詳細資訊，請參閱 [區域](regions.md)。</span><span class="sxs-lookup"><span data-stu-id="ebb15-109">For more information about polygon fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="ebb15-110">下圖顯示使用 [**多邊形**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)繪製的多邊形。</span><span class="sxs-lookup"><span data-stu-id="ebb15-110">The following illustration shows a polygon drawn by using [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span></span>

![以五向星形為圖形的多邊形圖例](images/csfsh-04.png)

<span data-ttu-id="ebb15-112">除了使用 [**多邊形**](/windows/win32/api/wingdi/nf-wingdi-polygon)繪製單一多邊形，應用程式可以使用 [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) 函數來繪製多個多邊形。</span><span class="sxs-lookup"><span data-stu-id="ebb15-112">In addition to drawing a single polygon by using [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), an application can draw multiple polygons by using the [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) function.</span></span>

 

 
