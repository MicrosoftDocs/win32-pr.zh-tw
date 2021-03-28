---
description: 許多函式會使用目前選取的筆刷至裝置內容，以執行點陣圖作業。
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: 點陣圖作為筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191959"
---
# <a name="bitmaps-as-brushes"></a><span data-ttu-id="fc8b1-103">點陣圖作為筆刷</span><span class="sxs-lookup"><span data-stu-id="fc8b1-103">Bitmaps as Brushes</span></span>

<span data-ttu-id="fc8b1-104">許多函式會使用目前選取的筆刷至裝置內容，以執行點陣圖作業。</span><span class="sxs-lookup"><span data-stu-id="fc8b1-104">A number of functions use the brush currently selected into a device context to perform bitmap operations.</span></span> <span data-ttu-id="fc8b1-105">例如， [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) 函式會在視窗內的矩形區域中複寫筆刷，而 [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) 函式會將筆刷複寫到指定色彩所系結之視窗內的某個區域內， (不同于 **PatBlt**， **FloodFill** 會填滿非矩形圖形) 。</span><span class="sxs-lookup"><span data-stu-id="fc8b1-105">For example, the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function replicates the brush in a rectangular region within a window, and the [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush inside an area in a window bounded by the specified color (unlike **PatBlt**, **FloodFill** does fill nonrectangular shapes).</span></span>

<span data-ttu-id="fc8b1-106">[**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)函式會在以指定的色彩所系結的區域內複寫筆刷。</span><span class="sxs-lookup"><span data-stu-id="fc8b1-106">The [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush within a region bounded by a specified color.</span></span> <span data-ttu-id="fc8b1-107">但是，與 [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) 函式不同的是， **FloodFill** 不會將筆刷的色彩資料與顯示器上的圖元色彩資料結合在一起。它只會將顯示區域內的所有圖元色彩，設定為目前在裝置內容中選取之筆刷的色彩。</span><span class="sxs-lookup"><span data-stu-id="fc8b1-107">However, unlike the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function, **FloodFill** does not combine the color data for the brush with the color data for the pixels on the display; it simply sets the color of all pixels within the enclosed region on the display to the color of the brush that is currently selected into the device context.</span></span>

 

 



