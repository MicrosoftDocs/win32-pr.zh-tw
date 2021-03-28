---
description: 筆刷中的範例會使用區域來模擬 &\# 0034; 縮放&\# 0034; 查看 8 x 8 圖元的單色點陣圖。
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: 使用區域來執行點擊測試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192391"
---
# <a name="using-regions-to-perform-hit-testing"></a><span data-ttu-id="0f4e5-103">使用區域來執行點擊測試</span><span class="sxs-lookup"><span data-stu-id="0f4e5-103">Using Regions to Perform Hit Testing</span></span>

<span data-ttu-id="0f4e5-104">[筆刷](brushes.md)中的範例會使用區域來模擬 8 x 8 圖元單色點陣圖的「縮放」視圖。</span><span class="sxs-lookup"><span data-stu-id="0f4e5-104">The example in [Brushes](brushes.md) uses regions to simulate a "zoomed" view of an 8- by 8-pixel monochrome bitmap.</span></span> <span data-ttu-id="0f4e5-105">藉由按一下此點陣圖中的圖元，使用者會建立適合繪圖作業的自訂筆刷。</span><span class="sxs-lookup"><span data-stu-id="0f4e5-105">By clicking on the pixels in this bitmap, the user creates a custom brush suitable for drawing operations.</span></span> <span data-ttu-id="0f4e5-106">此範例示範如何使用 [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) 函式來執行點擊測試，並使用 [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) 函數來反轉區域中的色彩。</span><span class="sxs-lookup"><span data-stu-id="0f4e5-106">The example shows how to use the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function to perform hit testing and the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function to invert the colors in a region.</span></span>

 

 



