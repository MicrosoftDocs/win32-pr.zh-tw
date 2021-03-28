---
description: StretchBlt 函式會藉由在來源裝置內容中的矩形執行位區塊傳輸，來調整點陣圖，以轉換成目的地裝置內容中的矩形。
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: 點陣圖縮放比例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4011b06e6a7269be29e1834e90928c4f531b1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114732"
---
# <a name="bitmap-scaling"></a><span data-ttu-id="91a7e-103">點陣圖縮放比例</span><span class="sxs-lookup"><span data-stu-id="91a7e-103">Bitmap Scaling</span></span>

<span data-ttu-id="91a7e-104">[**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)函式會藉由在來源裝置內容中的矩形執行位區塊傳輸，來調整點陣圖，以轉換成目的地裝置內容中的矩形。</span><span class="sxs-lookup"><span data-stu-id="91a7e-104">The [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) function scales a bitmap by performing a bit-block transfer from a rectangle in a source device context into a rectangle in a destination device context.</span></span> <span data-ttu-id="91a7e-105">但是，與 [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) 函式不同的是，它會在目的矩形中複製來源矩形的維度，而 **StretchBlt** 可讓應用程式指定來源和目的地矩形的維度。</span><span class="sxs-lookup"><span data-stu-id="91a7e-105">However, unlike the [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) function, which duplicates the source rectangle dimensions in the destination rectangle, **StretchBlt** allows an application to specify the dimensions of both the source and the destination rectangles.</span></span> <span data-ttu-id="91a7e-106">當目的點陣圖小於來源點陣圖時，系統會將色彩資料的資料列或資料行 (或點陣圖中) 的資料行，然後在顯示裝置上呈現對應的影像。</span><span class="sxs-lookup"><span data-stu-id="91a7e-106">When the destination bitmap is smaller than the source bitmap, the system combines rows or columns of color data (or both) in the bitmap before rendering the corresponding image on the display device.</span></span> <span data-ttu-id="91a7e-107">系統會根據指定的延展模式（由應用程式透過呼叫 [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) 函式來定義）來合併色彩資料。</span><span class="sxs-lookup"><span data-stu-id="91a7e-107">The system combines the color data according to the specified stretch mode, which the application defines by calling the [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) function.</span></span> <span data-ttu-id="91a7e-108">當目的點陣圖大於來源點陣圖時，系統會據以調整或放大結果影像中的每個圖元。</span><span class="sxs-lookup"><span data-stu-id="91a7e-108">When the destination bitmap is larger than the source bitmap, the system scales or magnifies each pixel in the resultant image accordingly.</span></span>

 

 



