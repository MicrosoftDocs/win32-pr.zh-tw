---
description: 下列函數用來建立、改變或繪製路徑。
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: '路徑函式 (Windows GDI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab85e52392b3e600877f8f5adac08d5de77e873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972596"
---
# <a name="path-functions-windows-gdi"></a><span data-ttu-id="9f52e-103">路徑函式 (Windows GDI) </span><span class="sxs-lookup"><span data-stu-id="9f52e-103">Path Functions (Windows GDI)</span></span>

<span data-ttu-id="9f52e-104">下列函數用來建立、改變或繪製路徑。</span><span class="sxs-lookup"><span data-stu-id="9f52e-104">The following functions are used to create, alter, or draw paths.</span></span>



| <span data-ttu-id="9f52e-105">函式</span><span class="sxs-lookup"><span data-stu-id="9f52e-105">Function</span></span>                                       | <span data-ttu-id="9f52e-106">描述</span><span class="sxs-lookup"><span data-stu-id="9f52e-106">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f52e-107">**AbortPath**</span><span class="sxs-lookup"><span data-stu-id="9f52e-107">**AbortPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | <span data-ttu-id="9f52e-108">關閉並捨棄指定之裝置內容中的任何路徑。</span><span class="sxs-lookup"><span data-stu-id="9f52e-108">Closes and discards any paths in the specified device context.</span></span>                                                                                                   |
| [<span data-ttu-id="9f52e-109">**BeginPath**</span><span class="sxs-lookup"><span data-stu-id="9f52e-109">**BeginPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | <span data-ttu-id="9f52e-110">在指定的裝置內容中開啟路徑括弧。</span><span class="sxs-lookup"><span data-stu-id="9f52e-110">Opens a path bracket in the specified device context.</span></span>                                                                                                            |
| [<span data-ttu-id="9f52e-111">**CloseFigure**</span><span class="sxs-lookup"><span data-stu-id="9f52e-111">**CloseFigure**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | <span data-ttu-id="9f52e-112">在路徑中關閉已開啟的圖表。</span><span class="sxs-lookup"><span data-stu-id="9f52e-112">Closes an open figure in a path.</span></span>                                                                                                                                 |
| [<span data-ttu-id="9f52e-113">**EndPath**</span><span class="sxs-lookup"><span data-stu-id="9f52e-113">**EndPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | <span data-ttu-id="9f52e-114">關閉路徑括弧，並在指定的裝置內容中選取由括弧定義的路徑。</span><span class="sxs-lookup"><span data-stu-id="9f52e-114">Closes a path bracket and selects the path defined by the bracket into the specified device context.</span></span>                                                             |
| [<span data-ttu-id="9f52e-115">**FillPath**</span><span class="sxs-lookup"><span data-stu-id="9f52e-115">**FillPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | <span data-ttu-id="9f52e-116">關閉目前路徑中的所有開啟的圖表，並使用目前的筆刷和多邊形填滿模式來填滿路徑的內部。</span><span class="sxs-lookup"><span data-stu-id="9f52e-116">Closes any open figures in the current path and fills the path's interior by using the current brush and polygon-filling mode.</span></span>                                   |
| [<span data-ttu-id="9f52e-117">**FlattenPath**</span><span class="sxs-lookup"><span data-stu-id="9f52e-117">**FlattenPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | <span data-ttu-id="9f52e-118">將選取的路徑中的任何曲線轉換為目前的裝置內容 (DC) ，將每個曲線轉換成一連串的線條。</span><span class="sxs-lookup"><span data-stu-id="9f52e-118">Transforms any curves in the path that is selected into the current device context (DC), turning each curve into a sequence of lines.</span></span>                            |
| [<span data-ttu-id="9f52e-119">**GetMiterLimit**</span><span class="sxs-lookup"><span data-stu-id="9f52e-119">**GetMiterLimit**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | <span data-ttu-id="9f52e-120">抓取指定之裝置內容的斜接限制。</span><span class="sxs-lookup"><span data-stu-id="9f52e-120">Retrieves the miter limit for the specified device context.</span></span>                                                                                                      |
| [<span data-ttu-id="9f52e-121">**GetPath**</span><span class="sxs-lookup"><span data-stu-id="9f52e-121">**GetPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | <span data-ttu-id="9f52e-122">抓取定義線條端點的座標，以及在指定的裝置內容中選取的路徑中找到的曲線控制點。</span><span class="sxs-lookup"><span data-stu-id="9f52e-122">Retrieves the coordinates defining the endpoints of lines and the control points of curves found in the path that is selected into the specified device context.</span></span> |
| [<span data-ttu-id="9f52e-123">**PathToRegion**</span><span class="sxs-lookup"><span data-stu-id="9f52e-123">**PathToRegion**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | <span data-ttu-id="9f52e-124">從選取到指定之裝置內容的路徑建立區域。</span><span class="sxs-lookup"><span data-stu-id="9f52e-124">Creates a region from the path that is selected into the specified device context.</span></span>                                                                               |
| [<span data-ttu-id="9f52e-125">**SetMiterLimit**</span><span class="sxs-lookup"><span data-stu-id="9f52e-125">**SetMiterLimit**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | <span data-ttu-id="9f52e-126">設定指定之裝置內容的斜接聯結長度限制。</span><span class="sxs-lookup"><span data-stu-id="9f52e-126">Sets the limit for the length of miter joins for the specified device context.</span></span>                                                                                   |
| [<span data-ttu-id="9f52e-127">**StrokeAndFillPath**</span><span class="sxs-lookup"><span data-stu-id="9f52e-127">**StrokeAndFillPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | <span data-ttu-id="9f52e-128">關閉路徑中的所有開啟的圖表，使用目前的畫筆來筆劃路徑的外框，並使用目前的筆刷來填滿其內部。</span><span class="sxs-lookup"><span data-stu-id="9f52e-128">Closes any open figures in a path, strokes the outline of the path by using the current pen, and fills its interior by using the current brush.</span></span>                  |
| [<span data-ttu-id="9f52e-129">**StrokePath**</span><span class="sxs-lookup"><span data-stu-id="9f52e-129">**StrokePath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | <span data-ttu-id="9f52e-130">使用目前的畫筆呈現指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="9f52e-130">Renders the specified path by using the current pen.</span></span>                                                                                                             |
| [<span data-ttu-id="9f52e-131">**WidenPath**</span><span class="sxs-lookup"><span data-stu-id="9f52e-131">**WidenPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | <span data-ttu-id="9f52e-132">將目前的路徑重新定義為如果路徑是使用目前選取的畫筆，在指定的裝置內容中繪製的區域。</span><span class="sxs-lookup"><span data-stu-id="9f52e-132">Redefines the current path as the area that would be painted if the path were stroked using the pen currently selected into the given device context.</span></span>            |



 

 

 



