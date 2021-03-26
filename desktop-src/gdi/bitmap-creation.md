---
description: 若要建立點陣圖，請使用 CreateBitmap、CreateBitmapIndirect 或 CreateCompatibleBitmap 函數、CreateDIBitmap 和 CreateDiscardableBitmap。
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: 點陣圖建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191963"
---
# <a name="bitmap-creation"></a><span data-ttu-id="e910e-103">點陣圖建立</span><span class="sxs-lookup"><span data-stu-id="e910e-103">Bitmap Creation</span></span>

<span data-ttu-id="e910e-104">若要建立點陣圖，請使用 [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)、 [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)或 [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) 函數、 [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)和 [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)。</span><span class="sxs-lookup"><span data-stu-id="e910e-104">To create a bitmap, use the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap), and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span></span>

<span data-ttu-id="e910e-105">這些函數可讓您指定點陣圖的寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="e910e-105">These functions allow you to specify the width and height, in pixels, of the bitmap.</span></span> <span data-ttu-id="e910e-106">[**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)和 [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)函式也可讓您指定色彩平面的數目，以及用來識別色彩所需的位數。</span><span class="sxs-lookup"><span data-stu-id="e910e-106">The [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) and [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) function also allow you to specify the number of color planes and the number of bits required to identify the color.</span></span> <span data-ttu-id="e910e-107">另一方面， [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) 和 [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) 函式會使用指定的裝置內容，來取得色彩平面的數目和識別色彩所需的位數。</span><span class="sxs-lookup"><span data-stu-id="e910e-107">On the other hand, the [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) functions use a specified device context to obtain the number of color planes and the number of bits required to identify the color.</span></span>

<span data-ttu-id="e910e-108">[**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)函式會從與裝置無關的點陣圖建立裝置相依點陣圖。</span><span class="sxs-lookup"><span data-stu-id="e910e-108">The [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) function creates a device-dependent bitmap from a device-independent bitmap.</span></span> <span data-ttu-id="e910e-109">它包含描述圖元值如何對應至 RGB 色彩值的色彩表。</span><span class="sxs-lookup"><span data-stu-id="e910e-109">It contains a color table that describes how pixel values correspond to RGB color values.</span></span> <span data-ttu-id="e910e-110">如需詳細資訊，請參閱 [裝置相關點陣圖](device-dependent-bitmaps.md) 和與 [裝置無關的點陣圖](device-independent-bitmaps.md)。</span><span class="sxs-lookup"><span data-stu-id="e910e-110">For more information, see [Device-Dependent Bitmaps](device-dependent-bitmaps.md) and [Device-Independent Bitmaps](device-independent-bitmaps.md).</span></span>

<span data-ttu-id="e910e-111">建立點陣圖之後，您就無法變更其大小、色彩平面的數目或識別色彩所需的位數。</span><span class="sxs-lookup"><span data-stu-id="e910e-111">After the bitmap has been created, you cannot change its size, number of color planes, or number of bits required to identify the color.</span></span>

<span data-ttu-id="e910e-112">當您不再需要點陣圖時，請呼叫 [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) 函數來刪除它。</span><span class="sxs-lookup"><span data-stu-id="e910e-112">When you no longer need a bitmap, call the [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) function to delete it.</span></span>

 

 



