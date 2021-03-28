---
description: 裁剪區域是應用程式可在裝置內容 (DC) 中選取的其中一個繪圖物件。
ms.assetid: d9238ee5-3305-4e85-aef3-2c5c8b74aacd
title: 裁剪區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a830e05b2a9ce709183f23fad66f937c8c512acd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114713"
---
# <a name="clipping-regions"></a><span data-ttu-id="77ece-103">裁剪區域</span><span class="sxs-lookup"><span data-stu-id="77ece-103">Clipping Regions</span></span>

<span data-ttu-id="77ece-104">裁剪區域是應用程式可在裝置內容 (DC) 中選取的其中一個繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="77ece-104">A clipping region is one of the graphic objects that an application can select into a device context (DC).</span></span> <span data-ttu-id="77ece-105">它通常是矩形。</span><span class="sxs-lookup"><span data-stu-id="77ece-105">It is typically rectangular.</span></span> <span data-ttu-id="77ece-106">某些裝置內容提供預先定義或預設的裁剪區域，其他則否。</span><span class="sxs-lookup"><span data-stu-id="77ece-106">Some device contexts provide a predefined or default clipping region while others do not.</span></span> <span data-ttu-id="77ece-107">例如，如果您從 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 函式取得裝置內容控制碼，DC 就會包含預先定義的矩形裁剪區域，該區域會對應至需要重新繪製的無效矩形。</span><span class="sxs-lookup"><span data-stu-id="77ece-107">For example, if you obtain a device context handle from the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) function, the DC contains a predefined rectangular clipping region that corresponds to the invalid rectangle that requires repainting.</span></span> <span data-ttu-id="77ece-108">但是，當您藉由呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式（使用 **Null**_HWnd_ 參數）或呼叫 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 函式來取得裝置內容控制碼時，DC 不會包含預設的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="77ece-108">However, when you obtain a device context handle by calling the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function with a **NULL**_hWnd_ parameter, or by calling the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function, the DC does not contain a default clipping region.</span></span> <span data-ttu-id="77ece-109">如需 **BeginPaint** 函式所傳回之裝置內容的詳細資訊，請參閱 [繪製和繪製](painting-and-drawing.md) 。</span><span class="sxs-lookup"><span data-stu-id="77ece-109">For more information about device contexts returned by the **BeginPaint** function, see [Painting and Drawing](painting-and-drawing.md) .</span></span> <span data-ttu-id="77ece-110">如需 **CreateDC** 和 **GetDC** 函數所傳回之裝置內容的詳細資訊，請參閱 [裝置](device-contexts.md)內容。</span><span class="sxs-lookup"><span data-stu-id="77ece-110">For more information about device contexts returned by the **CreateDC** and **GetDC** functions, see [Device Contexts](device-contexts.md).</span></span>

<span data-ttu-id="77ece-111">應用程式可以在裁剪區域上執行各種作業。</span><span class="sxs-lookup"><span data-stu-id="77ece-111">Applications can perform a variety of operations on clipping regions.</span></span> <span data-ttu-id="77ece-112">其中有些作業需要識別區域的控制碼，有些則否。</span><span class="sxs-lookup"><span data-stu-id="77ece-112">Some of these operations require a handle identifying the region and some do not.</span></span> <span data-ttu-id="77ece-113">例如，應用程式可以直接在裝置內容的裁剪區域上執行下列作業。</span><span class="sxs-lookup"><span data-stu-id="77ece-113">For example, an application can perform the following operations directly on a device context's clipping region.</span></span>

-   <span data-ttu-id="77ece-114">藉由將對應的線條、弧線、點陣圖、文字或填滿圖形的座標傳遞給 [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible) 函式，來判斷圖形輸出是否出現在區域的框線內。</span><span class="sxs-lookup"><span data-stu-id="77ece-114">Determine whether graphics output appears within the region's borders by passing coordinates of the corresponding line, arc, bitmap, text, or filled shape to the [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible) function.</span></span>
-   <span data-ttu-id="77ece-115">藉由呼叫 [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) 函數，判斷用戶端區域的一部分是否與區域相交。</span><span class="sxs-lookup"><span data-stu-id="77ece-115">Determine whether part of the client area intersects a region by calling the [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) function.</span></span>
-   <span data-ttu-id="77ece-116">藉由呼叫 [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn) 函數，以指定的位移來移動現有的區域。</span><span class="sxs-lookup"><span data-stu-id="77ece-116">Move the existing region by a specified offset by calling the [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn) function.</span></span>
-   <span data-ttu-id="77ece-117">藉由呼叫 [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect) 函式，從目前的裁剪區域中排除工作區的矩形部分。</span><span class="sxs-lookup"><span data-stu-id="77ece-117">Exclude a rectangular part of the client area from the current clipping region by calling the [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect) function.</span></span>
-   <span data-ttu-id="77ece-118">藉由呼叫 [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) 函式，將工作區的矩形部分與目前的裁剪區域結合在一起。</span><span class="sxs-lookup"><span data-stu-id="77ece-118">Combine a rectangular part of the client area with the current clipping region by calling the [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) function.</span></span>

<span data-ttu-id="77ece-119">取得識別裁剪區域的控制碼之後，應用程式就可以執行與區域共通的任何作業，例如：</span><span class="sxs-lookup"><span data-stu-id="77ece-119">After obtaining a handle identifying the clipping region, an application can perform any operation that is common with regions, such as:</span></span>

-   <span data-ttu-id="77ece-120">藉由呼叫 [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) 函數，結合目前裁剪區域的複本與第二個區域。</span><span class="sxs-lookup"><span data-stu-id="77ece-120">Combining a copy of the current clipping region with a second region by calling the [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) function.</span></span>
-   <span data-ttu-id="77ece-121">藉由呼叫 [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn) 函數，比較目前裁剪區域的複本與第二個區域。</span><span class="sxs-lookup"><span data-stu-id="77ece-121">Compare a copy of the current clipping region to a second region by calling the [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn) function.</span></span>
-   <span data-ttu-id="77ece-122">藉由呼叫 [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) 函式，判斷某個點是否位在目前裁剪區域的複本內部。</span><span class="sxs-lookup"><span data-stu-id="77ece-122">Determine whether a point lies within the interior of a copy of the current clipping region by calling the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function.</span></span>

 

 



