---
description: 只要裝置內容的延展模式設定為 [半色調]，就可以使用半色調調色板。
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: 半色調調色板和色彩調整
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512888"
---
# <a name="halftone-palette-and-color-adjustment"></a><span data-ttu-id="ac7b3-103">半色調調色板和色彩調整</span><span class="sxs-lookup"><span data-stu-id="ac7b3-103">Halftone Palette and Color Adjustment</span></span>

<span data-ttu-id="ac7b3-104">只要裝置內容的延展模式設定為 [半色調]，就可以使用半色調調色板。</span><span class="sxs-lookup"><span data-stu-id="ac7b3-104">Halftone palettes are intended to be used whenever the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="ac7b3-105">應用程式會使用 [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) 函式來建立半色調調色板。</span><span class="sxs-lookup"><span data-stu-id="ac7b3-105">An application creates a halftone palette by using the [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) function.</span></span> <span data-ttu-id="ac7b3-106">在呼叫 [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) 或 [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) 函式之前，應用程式必須在裝置內容中選取並實現這個調色板。</span><span class="sxs-lookup"><span data-stu-id="ac7b3-106">The application must select and realize this palette into the device context before calling the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) or [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) function.</span></span>

<span data-ttu-id="ac7b3-107">每當應用程式呼叫 [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) 和 [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) 函式，且裝置內容的延展模式設定為 [半色調] 時，系統就會自動調整來源點陣圖的輸入色彩。</span><span class="sxs-lookup"><span data-stu-id="ac7b3-107">The system automatically adjusts the input color of source bitmaps whenever applications call the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) and [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) functions and the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="ac7b3-108">這些色彩調整會影響影像的某些屬性，例如對比和亮度。</span><span class="sxs-lookup"><span data-stu-id="ac7b3-108">These color adjustments affect certain attributes of the image, such as contrast and brightness.</span></span> <span data-ttu-id="ac7b3-109">應用程式可以使用 [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) 函數來設定色彩調整值。</span><span class="sxs-lookup"><span data-stu-id="ac7b3-109">An application can set the color adjustment values by using the [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) function.</span></span> <span data-ttu-id="ac7b3-110">應用程式可以使用 [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) 函式，來取得指定之裝置內容的色彩調整值。</span><span class="sxs-lookup"><span data-stu-id="ac7b3-110">The application can retrieve the color adjustment values for the specified device context by using the [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) function.</span></span>

 

 



