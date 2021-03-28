---
description: 應用程式會藉由呼叫 InvertRgn 函式來反轉區域內出現的色彩。
ms.assetid: bcd9fe61-0f92-41bc-b953-a66e01e43a75
title: 反轉區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e3c4b4d01f9ed8f09e819d59bf3268a1ccae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991199"
---
# <a name="inverting-regions"></a><span data-ttu-id="2e501-103">反轉區域</span><span class="sxs-lookup"><span data-stu-id="2e501-103">Inverting Regions</span></span>

<span data-ttu-id="2e501-104">應用程式會藉由呼叫 [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) 函式來反轉區域內出現的色彩。</span><span class="sxs-lookup"><span data-stu-id="2e501-104">An application inverts the colors that appear within a region by calling the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function.</span></span> <span data-ttu-id="2e501-105">在單色顯示器上， **InvertRgn** 會將白色圖元的黑色和黑色圖元白色。</span><span class="sxs-lookup"><span data-stu-id="2e501-105">On monochrome displays, **InvertRgn** makes white pixels black and black pixels white.</span></span> <span data-ttu-id="2e501-106">在色彩畫面上，這項反轉取決於用來產生螢幕色彩的技術類型。</span><span class="sxs-lookup"><span data-stu-id="2e501-106">On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.</span></span>

 

 



