---
description: 應用程式會藉由呼叫 FillRgn 函式並提供識別特定筆刷的控制碼，填滿區域的內部。
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: 填滿區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026456"
---
# <a name="filling-regions"></a><span data-ttu-id="46b37-103">填滿區域</span><span class="sxs-lookup"><span data-stu-id="46b37-103">Filling Regions</span></span>

<span data-ttu-id="46b37-104">應用程式會藉由呼叫 [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) 函式並提供識別特定筆刷的控制碼，填滿區域的內部。</span><span class="sxs-lookup"><span data-stu-id="46b37-104">An application fills the interior of a region by calling the [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) function and supplying a handle that identifies a specific brush.</span></span> <span data-ttu-id="46b37-105">當應用程式呼叫 FillRgn 時，系統會使用指定之裝置內容的目前填滿模式，填滿該區域中的筆刷。</span><span class="sxs-lookup"><span data-stu-id="46b37-105">When an application calls FillRgn , the system fills the region with the brush by using the current fill mode for the specified device context.</span></span> <span data-ttu-id="46b37-106">填滿模式有兩種：替代和繞組。</span><span class="sxs-lookup"><span data-stu-id="46b37-106">There are two fill modes: alternate and winding.</span></span> <span data-ttu-id="46b37-107">應用程式可以藉由呼叫 [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) 函數來設定裝置內容的填滿模式。</span><span class="sxs-lookup"><span data-stu-id="46b37-107">The application can set the fill mode for a device context by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="46b37-108">應用程式可以藉由呼叫 [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) 函式，來取得裝置內容的目前填滿模式。</span><span class="sxs-lookup"><span data-stu-id="46b37-108">The application can retrieve the current fill mode for a device context by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function.</span></span>

<span data-ttu-id="46b37-109">下圖顯示兩個相同的區域：一個使用替代模式填滿，另一個則使用纏繞模式填滿。</span><span class="sxs-lookup"><span data-stu-id="46b37-109">The following illustration shows two identical regions: one filled using alternate mode and the other filled using winding mode.</span></span>

![顯示 2 5 點星星的圖例：一個只填滿在點中，另一個則完全填滿](images/csrgn-03.png)

## <a name="alternate-mode"></a><span data-ttu-id="46b37-111">替代模式</span><span class="sxs-lookup"><span data-stu-id="46b37-111">Alternate Mode</span></span>

<span data-ttu-id="46b37-112">若要判斷當指定替代模式時，系統要強調的圖元，請執行下列測試：</span><span class="sxs-lookup"><span data-stu-id="46b37-112">To determine which pixels the system highlights when alternate mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="46b37-113">選取區域內部的圖元。</span><span class="sxs-lookup"><span data-stu-id="46b37-113">Select a pixel within the region's interior.</span></span>
2.  <span data-ttu-id="46b37-114">以正 x 方向繪製虛光線，從該圖元到無限大。</span><span class="sxs-lookup"><span data-stu-id="46b37-114">Draw an imaginary ray, in the positive x-direction, from that pixel toward infinity.</span></span>
3.  <span data-ttu-id="46b37-115">每次光線相交界限線時，就會遞增計數值。</span><span class="sxs-lookup"><span data-stu-id="46b37-115">Each time the ray intersects a boundary line, increment a count value.</span></span>

<span data-ttu-id="46b37-116">如果 count 值是奇數，系統就會反白顯示圖元。</span><span class="sxs-lookup"><span data-stu-id="46b37-116">The system highlights the pixel if the count value is an odd number.</span></span>

## <a name="winding-mode"></a><span data-ttu-id="46b37-117">纏繞模式</span><span class="sxs-lookup"><span data-stu-id="46b37-117">Winding Mode</span></span>

<span data-ttu-id="46b37-118">若要判斷當指定了纏繞模式時，系統要強調的圖元，請執行下列測試：</span><span class="sxs-lookup"><span data-stu-id="46b37-118">To determine which pixels the system highlights when winding mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="46b37-119">決定繪製每個邊界線的方向。</span><span class="sxs-lookup"><span data-stu-id="46b37-119">Determine the direction in which each boundary line is drawn.</span></span>
2.  <span data-ttu-id="46b37-120">選取區域內部的圖元。</span><span class="sxs-lookup"><span data-stu-id="46b37-120">Select a pixel within the region's interior.</span></span>
3.  <span data-ttu-id="46b37-121">以正 x 方向繪製虛光線，從圖元朝無限大。</span><span class="sxs-lookup"><span data-stu-id="46b37-121">Draw an imaginary ray, in the positive x-direction, from the pixel toward infinity.</span></span>
4.  <span data-ttu-id="46b37-122">每次光線相交具有正面 y 元件的界限線時，就會遞增計數值。</span><span class="sxs-lookup"><span data-stu-id="46b37-122">Each time the ray intersects a boundary line with a positive y-component, increment a count value.</span></span> <span data-ttu-id="46b37-123">每次光線相交具有負 y 元件的界限線時，就會遞減計數值。</span><span class="sxs-lookup"><span data-stu-id="46b37-123">Each time the ray intersects a boundary line with a negative y-component, decrement the count value.</span></span>

<span data-ttu-id="46b37-124">如果 count 值為非零值，系統會反白顯示圖元。</span><span class="sxs-lookup"><span data-stu-id="46b37-124">The system highlights the pixel if the count value is nonzero.</span></span>

 

 



