---
description: 色彩會以三種主要色彩的組合來定義：紅色、綠色和藍色。
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: 色彩值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114693"
---
# <a name="color-values"></a><span data-ttu-id="4c79c-103">色彩值</span><span class="sxs-lookup"><span data-stu-id="4c79c-103">Color Values</span></span>

<span data-ttu-id="4c79c-104">色彩會以三種主要色彩的組合來定義：紅色、綠色和藍色。</span><span class="sxs-lookup"><span data-stu-id="4c79c-104">Color is defined as a combination of three primary colors red, green, and blue.</span></span> <span data-ttu-id="4c79c-105">系統會藉由提供色彩值 (（有時稱為 RGB 三) ，其中包含指定其色彩元件亮度的 3 8 位值）來識別色彩。</span><span class="sxs-lookup"><span data-stu-id="4c79c-105">the system identifies a color by giving it a color value (sometimes called an RGB triplet), which consists of three 8-bit values specifying the intensities of its color components.</span></span> <span data-ttu-id="4c79c-106">黑色具有紅色、綠色和藍色的最小濃度，因此黑色的色彩值是 (0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="4c79c-106">Black has the minimum intensity for red, green, and blue, so the color value for black is (0, 0, 0).</span></span> <span data-ttu-id="4c79c-107">白色具有紅色、綠色和藍色的最大濃度，因此其色彩值為 (255、255、255) 。</span><span class="sxs-lookup"><span data-stu-id="4c79c-107">White has the maximum intensity for red, green, and blue, so its color value is (255, 255, 255).</span></span>

> [!Note]  
> <span data-ttu-id="4c79c-108">如果啟用影像色彩比對，色彩的定義和色彩值的意義取決於目前針對裝置內容設定的色彩空間類型。</span><span class="sxs-lookup"><span data-stu-id="4c79c-108">If image color matching is enabled, the definition of color and the meaning of a color value depends on the type of color space that is currently set for the device context.</span></span>

 

<span data-ttu-id="4c79c-109">系統和應用程式會使用具有 [COLORREF](colorref.md) 類型的參數和變數來傳遞和儲存色彩值。</span><span class="sxs-lookup"><span data-stu-id="4c79c-109">The system and applications use parameters and variables having the [COLORREF](colorref.md) type to pass and store color values.</span></span> <span data-ttu-id="4c79c-110">例如， [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)函式會藉由將 [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen)結構中的 **lopnColor** 成員設定為色彩值，來識別每個畫筆的色彩。</span><span class="sxs-lookup"><span data-stu-id="4c79c-110">For example, the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function identifies the color of each pen by setting the **lopnColor** member in a [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) structure to a color value.</span></span> <span data-ttu-id="4c79c-111">應用程式可以分別使用 [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)、 [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)和 [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) 宏，從色彩值解壓縮紅色、綠色和藍色元件的個別值。</span><span class="sxs-lookup"><span data-stu-id="4c79c-111">Applications can extract the individual values of the red, green, and blue components from a color value by using the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span> <span data-ttu-id="4c79c-112">應用程式可以使用 [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 宏來建立個別元件值的色彩值。</span><span class="sxs-lookup"><span data-stu-id="4c79c-112">Applications can create a color value from individual component values by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="4c79c-113">建立或檢查邏輯元件時，應用程式會使用 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構來定義色彩值，以及檢查個別的元件值。</span><span class="sxs-lookup"><span data-stu-id="4c79c-113">When creating or examining a logical palette, an application uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure to define color values and to examine individual component values.</span></span>

 

 



