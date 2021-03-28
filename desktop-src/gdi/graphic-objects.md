---
description: 與 DC 相關聯的畫筆、筆刷、點陣圖、調色板、區域和路徑稱為其繪圖物件。 下列屬性與每個物件相關聯。
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: 圖形物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991215"
---
# <a name="graphic-objects"></a><span data-ttu-id="80bd1-104">圖形物件</span><span class="sxs-lookup"><span data-stu-id="80bd1-104">Graphic Objects</span></span>

<span data-ttu-id="80bd1-105">與 DC 相關聯的畫筆、筆刷、點陣圖、調色板、區域和路徑稱為其繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="80bd1-105">The pen, brush, bitmap, palette, region, and path associated with a DC are referred to as its graphic objects.</span></span> <span data-ttu-id="80bd1-106">下列屬性與每個物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="80bd1-106">The following attributes are associated with each of these objects.</span></span>



| <span data-ttu-id="80bd1-107">繪圖物件</span><span class="sxs-lookup"><span data-stu-id="80bd1-107">Graphic object</span></span> | <span data-ttu-id="80bd1-108">相關聯的屬性</span><span class="sxs-lookup"><span data-stu-id="80bd1-108">Associated attributes</span></span>                                                               |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="80bd1-109">點陣圖</span><span class="sxs-lookup"><span data-stu-id="80bd1-109">Bitmap</span></span>         | <span data-ttu-id="80bd1-110">大小，以位元組為單位;維度（以圖元為單位）。色彩格式;壓縮配置;依此類推。</span><span class="sxs-lookup"><span data-stu-id="80bd1-110">Size, in bytes; dimensions, in pixels; color-format; compression scheme; and so on.</span></span> |
| <span data-ttu-id="80bd1-111">筆刷</span><span class="sxs-lookup"><span data-stu-id="80bd1-111">Brush</span></span>          | <span data-ttu-id="80bd1-112">樣式、色彩、模式和原點。</span><span class="sxs-lookup"><span data-stu-id="80bd1-112">Style, color, pattern, and origin.</span></span>                                                  |
| <span data-ttu-id="80bd1-113">調色盤</span><span class="sxs-lookup"><span data-stu-id="80bd1-113">Palette</span></span>        | <span data-ttu-id="80bd1-114">色彩和大小 (，或) 的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="80bd1-114">Colors and size (or number of colors).</span></span>                                              |
| <span data-ttu-id="80bd1-115">字型</span><span class="sxs-lookup"><span data-stu-id="80bd1-115">Font</span></span>           | <span data-ttu-id="80bd1-116">字型名稱、寬度、高度、權數、字元集等等。</span><span class="sxs-lookup"><span data-stu-id="80bd1-116">Typeface name, width, height, weight, character set, and so on.</span></span>                     |
| <span data-ttu-id="80bd1-117">路徑</span><span class="sxs-lookup"><span data-stu-id="80bd1-117">Path</span></span>           | <span data-ttu-id="80bd1-118">形狀。</span><span class="sxs-lookup"><span data-stu-id="80bd1-118">Shape.</span></span>                                                                              |
| <span data-ttu-id="80bd1-119">手寫筆</span><span class="sxs-lookup"><span data-stu-id="80bd1-119">Pen</span></span>            | <span data-ttu-id="80bd1-120">樣式、寬度和色彩。</span><span class="sxs-lookup"><span data-stu-id="80bd1-120">Style, width, and color.</span></span>                                                            |
| <span data-ttu-id="80bd1-121">區域</span><span class="sxs-lookup"><span data-stu-id="80bd1-121">Region</span></span>         | <span data-ttu-id="80bd1-122">位置和維度。</span><span class="sxs-lookup"><span data-stu-id="80bd1-122">Location and dimensions.</span></span>                                                            |



 

<span data-ttu-id="80bd1-123">當應用程式建立 DC 時，系統會自動將一組預設物件儲存 (沒有預設的點陣圖或路徑) 。</span><span class="sxs-lookup"><span data-stu-id="80bd1-123">When an application creates a DC, the system automatically stores a set of default objects in it (there is no default bitmap or path).</span></span> <span data-ttu-id="80bd1-124">應用程式可以藉由呼叫 [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) 和 [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) 函數來檢查預設物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="80bd1-124">An application can examine the attributes of the default objects by calling the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions.</span></span> <span data-ttu-id="80bd1-125">應用程式可以藉由建立新的物件並將其選取到 DC，來變更這些預設值。</span><span class="sxs-lookup"><span data-stu-id="80bd1-125">The application can change these defaults by creating a new object and selecting it into the DC.</span></span> <span data-ttu-id="80bd1-126">藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函數，將物件選取至 DC。</span><span class="sxs-lookup"><span data-stu-id="80bd1-126">An object is selected into a DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span>

<span data-ttu-id="80bd1-127">應用程式可以使用 [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)將目前的筆刷色彩設定為指定的色彩值。</span><span class="sxs-lookup"><span data-stu-id="80bd1-127">An application can set the current brush color to a specified color value with [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span></span>

<span data-ttu-id="80bd1-128">[**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)函式會傳回 DC 筆刷色彩。</span><span class="sxs-lookup"><span data-stu-id="80bd1-128">The [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) function returns the DC brush color.</span></span> <span data-ttu-id="80bd1-129">[**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)函式會將畫筆色彩設定為指定的色彩值。</span><span class="sxs-lookup"><span data-stu-id="80bd1-129">The [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) function sets the pen color to a specified color value.</span></span> <span data-ttu-id="80bd1-130">[**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)函式會傳回 DC 畫筆色彩。</span><span class="sxs-lookup"><span data-stu-id="80bd1-130">The [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) function returns the DC pen color.</span></span>

 

 



