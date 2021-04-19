---
description: 模式 (或自訂) 筆刷是從應用程式定義的點陣圖或與裝置無關的點陣圖 (DIB) 所建立。 下列矩形使用不同的模式筆刷繪製。
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: 模式筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988081"
---
# <a name="pattern-brush"></a><span data-ttu-id="882e3-104">模式筆刷</span><span class="sxs-lookup"><span data-stu-id="882e3-104">Pattern Brush</span></span>

<span data-ttu-id="882e3-105">模式 (或自訂) 筆刷是從應用程式定義的點陣圖或與裝置無關的點陣圖 (DIB) 所建立。</span><span class="sxs-lookup"><span data-stu-id="882e3-105">A pattern (or custom) brush is created from an application-defined bitmap or device-independent bitmap (DIB).</span></span> <span data-ttu-id="882e3-106">下列矩形使用不同的模式筆刷繪製。</span><span class="sxs-lookup"><span data-stu-id="882e3-106">The following rectangles were painted by using different pattern brushes.</span></span>

![顯示三個方塊的圖例，每個方塊都以不同的模式填滿](images/csbru-05.png)

<span data-ttu-id="882e3-108">若要建立邏輯模式筆刷，應用程式必須先建立點陣圖。</span><span class="sxs-lookup"><span data-stu-id="882e3-108">To create a logical pattern brush, an application must first create a bitmap.</span></span> <span data-ttu-id="882e3-109">建立點陣圖之後，應用程式可以藉由呼叫 [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) 或 [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) 函式，提供識別點陣圖 (或 DIB) 的控制碼，建立邏輯模式筆刷。</span><span class="sxs-lookup"><span data-stu-id="882e3-109">After creating the bitmap, the application can create the logical pattern brush by calling the [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) or [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) function, supplying a handle that identifies the bitmap (or DIB).</span></span> <span data-ttu-id="882e3-110">上圖中顯示的筆刷是從單色點陣圖建立。</span><span class="sxs-lookup"><span data-stu-id="882e3-110">The brushes that appear in the preceding illustration were created from monochrome bitmaps.</span></span> <span data-ttu-id="882e3-111">如需點陣圖、Dib 和建立它們的函式的說明，請參閱 [點陣圖](bitmaps.md)。</span><span class="sxs-lookup"><span data-stu-id="882e3-111">For a description of bitmaps, DIBs, and the functions that create them, see [Bitmaps](bitmaps.md).</span></span>

 

 



