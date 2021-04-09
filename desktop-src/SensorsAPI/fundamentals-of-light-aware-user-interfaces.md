---
description: Light-Aware 的使用者介面基礎
ms.assetid: 7ea391cb-f72b-4ac1-99be-c957d4ccc8af
title: Light-Aware 的使用者介面基礎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce71ab67e11684d14b188fef7ae73500edb7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694476"
---
# <a name="fundamentals-of-light-aware-user-interfaces"></a><span data-ttu-id="ce193-103">Light-Aware 的使用者介面基礎</span><span class="sxs-lookup"><span data-stu-id="ce193-103">Fundamentals of Light-Aware User Interfaces</span></span>

<span data-ttu-id="ce193-104">輕量 *感知 UI* 指的是一個程式，它會使用光線感應器資料來優化其內容、控制項和其他圖形，以獲得許多光源的最佳使用者體驗，範圍從暗度到 direct。</span><span class="sxs-lookup"><span data-stu-id="ce193-104">The term *light-aware UI* refers to a program that uses light sensor data to optimize its content, controls, and other graphics for an optimum user experience in many lighting conditions, ranging from darkness to direct sunlight.</span></span> <span data-ttu-id="ce193-105">可能是最重要的優化，因為在這些情況下，螢幕通常不會有很好的可讀性、可讀性和互動。</span><span class="sxs-lookup"><span data-stu-id="ce193-105">Perhaps the most important optimizations are legibility, readability, and interactions in direct sunlight, because screens do not typically perform well in these conditions.</span></span> <span data-ttu-id="ce193-106">在本節中，我們將焦點放在三個 UI 屬性：縮放、對比和色彩。</span><span class="sxs-lookup"><span data-stu-id="ce193-106">In this section, we focus on three UI properties: scale, contrast, and color.</span></span> <span data-ttu-id="ce193-107">這些屬性可以變更，以優化視覺使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="ce193-107">These properties can be changed to optimize the visual user experience.</span></span>

## <a name="scale-and-brightness"></a><span data-ttu-id="ce193-108">調整規模和亮度</span><span class="sxs-lookup"><span data-stu-id="ce193-108">Scale and Brightness</span></span>

<span data-ttu-id="ce193-109">一般而言，較大的物件會更容易看見。</span><span class="sxs-lookup"><span data-stu-id="ce193-109">In general, larger objects are easier to see.</span></span> <span data-ttu-id="ce193-110">當電腦處於不良照明條件時 (例如在直接的照明) 讓內容更大時，可協助改善該內容的可讀性和 interactiveness。</span><span class="sxs-lookup"><span data-stu-id="ce193-110">When the computer is in adverse lighting conditions (such as in direct sunlight) making content larger can help to improve the legibility and interactiveness of that content.</span></span>

<span data-ttu-id="ce193-111">下列相片將一般螢幕亮度和縮放層級的膝上型電腦，與具有淺感知 UI 的相同照明條件中的膝上型電腦進行比較。</span><span class="sxs-lookup"><span data-stu-id="ce193-111">The following photographs compare a laptop in direct sunlight with typical screen brightness and zoom levels to a laptop in the same lighting conditions with light-aware UI.</span></span> <span data-ttu-id="ce193-112">第一張相片顯示使用一般縮放層級，將顯示器設為40% 的亮度。</span><span class="sxs-lookup"><span data-stu-id="ce193-112">The first photograph shows the display set to 40% brightness with normal zoom levels.</span></span> <span data-ttu-id="ce193-113">第二張相片顯示將顯示設定為100% 的亮度（具有增加的縮放層級）。</span><span class="sxs-lookup"><span data-stu-id="ce193-113">The second photograph shows the display set to 100% brightness with increased zoom levels.</span></span>

![使用一般縮放層級的膝上型電腦以40% 的亮度顯示](images/laptop-40.png)![膝上型電腦以100% 的亮度顯示，縮放層級增加](images/laptop-100.png)

### <a name="varying-font-size"></a><span data-ttu-id="ce193-116">不同的字型大小</span><span class="sxs-lookup"><span data-stu-id="ce193-116">Varying Font Size</span></span>

<span data-ttu-id="ce193-117">如果您增加用來顯示文字的字型大小，則文字在不良光源條件中會更清晰。</span><span class="sxs-lookup"><span data-stu-id="ce193-117">If you increase the size of the font that is used to display text, the text is more legible in adverse lighting conditions.</span></span> <span data-ttu-id="ce193-118">字型樣式、字型和其他特性也可以不同，以優化可讀性和可讀性。</span><span class="sxs-lookup"><span data-stu-id="ce193-118">Font style, font face, and other characteristics can also be varied to optimize legibility and readability.</span></span> <span data-ttu-id="ce193-119">例如，「sans serif」字型通常比 serif 字型更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="ce193-119">For example, sans serif fonts are typically easier to read than serif fonts.</span></span>

![相較于 serif 字型的 sans serif 字型](images/fonts.png)

### <a name="zooming-content"></a><span data-ttu-id="ce193-121">縮放內容</span><span class="sxs-lookup"><span data-stu-id="ce193-121">Zooming Content</span></span>

<span data-ttu-id="ce193-122">如果您的程式會執行縮放，則可以使用它來調整內容。</span><span class="sxs-lookup"><span data-stu-id="ce193-122">If your program implements zooming, it can be used to scale the content.</span></span> <span data-ttu-id="ce193-123">放大可提高可讀性，而放大可讓程式顯示更多內容。</span><span class="sxs-lookup"><span data-stu-id="ce193-123">Zooming in enhances legibility while zooming out enables the program to display more content.</span></span>

### <a name="altering-vector-graphic-rendering-properties"></a><span data-ttu-id="ce193-124">改變向量圖形轉譯屬性</span><span class="sxs-lookup"><span data-stu-id="ce193-124">Altering Vector Graphic Rendering Properties</span></span>

<span data-ttu-id="ce193-125">如果您的程式會呈現向量圖形基本專案 (例如線條、圓形等) ，則可以改變轉譯的特性以優化可讀性。</span><span class="sxs-lookup"><span data-stu-id="ce193-125">If your program renders vector graphic primitives (such as lines, circles, and so on), the characteristics of the rendering can be altered to optimize legibility.</span></span> <span data-ttu-id="ce193-126">例如，如果您的程式會呈現矩形，則用來呈現矩形的線條寬度可以調整 (更寬的室外，並讓室內) 更窄，以優化向量圖形內容的外觀和可讀性。</span><span class="sxs-lookup"><span data-stu-id="ce193-126">For example, if your program renders rectangles, the width of the lines that are used to render the rectangles could be scaled (wider for outdoors and narrower for indoors) to optimize the appearance and legibility of the vector graphic content.</span></span>

## <a name="contrast"></a><span data-ttu-id="ce193-127">這個</span><span class="sxs-lookup"><span data-stu-id="ce193-127">Contrast</span></span>

<span data-ttu-id="ce193-128">在明亮的照明條件中使用 LCD 螢幕時，螢幕的整體對比會減少。</span><span class="sxs-lookup"><span data-stu-id="ce193-128">When LCD screens are used in bright lighting conditions, the overall contrast of the screen is reduced.</span></span> <span data-ttu-id="ce193-129">當螢幕上的光線 (過了，例如) ，使用者對螢幕上的暗區的認知將會降低。</span><span class="sxs-lookup"><span data-stu-id="ce193-129">When the screen is flooded with light (from the sun, for example), the user's perception of dark areas on the screen is reduced.</span></span> <span data-ttu-id="ce193-130">一般來說，當環境燈亮亮時，請務必增加內容和 UI 的對比。</span><span class="sxs-lookup"><span data-stu-id="ce193-130">In general, this makes it important to increase the contrast of content and UI when the ambient light is bright.</span></span> <span data-ttu-id="ce193-131">您可能想要使用單色色彩配置來最大化這些光源條件的對比。</span><span class="sxs-lookup"><span data-stu-id="ce193-131">It may be desirable to use a monochrome color scheme to maximize contrast in these lighting conditions.</span></span> <span data-ttu-id="ce193-132">另一種提高對比的方法是以高對比的元素來取代低對比度的內容 (例如，) 具有高對比元素 (例如黑色白色街道向量圖形模式) 。</span><span class="sxs-lookup"><span data-stu-id="ce193-132">Another way to increase contrast is to replace low-contrast content (such as an aerial photo mode in a mapping program) with high-contrast elements (such as black-on-white street vector graphics mode).</span></span>

## <a name="color"></a><span data-ttu-id="ce193-133">Color</span><span class="sxs-lookup"><span data-stu-id="ce193-133">Color</span></span>

<span data-ttu-id="ce193-134">程式用來顯示其內容的色彩，可能會對整體使用者體驗和轉譯內容的可讀性造成嚴重的影響。</span><span class="sxs-lookup"><span data-stu-id="ce193-134">The colors that a program uses to display its content can have a drastic effect on the overall user experience and legibility of rendered content.</span></span> <span data-ttu-id="ce193-135">藉由根據環境光源來變更色彩對比，您可以讓內容更容易閱讀，例如亮鮮燈亮或深亮燈。</span><span class="sxs-lookup"><span data-stu-id="ce193-135">By changing color contrast based on ambient light, you can make content more readable in adverse lighting conditions, such as bright outdoor light or dark interior light.</span></span>

<span data-ttu-id="ce193-136">提高色彩對比度的其中一種方式是透過色彩飽和度。</span><span class="sxs-lookup"><span data-stu-id="ce193-136">One way to increase color contrast is through color saturation.</span></span> <span data-ttu-id="ce193-137">另一種方式是使用互補色彩，而不是連續的色彩，以提升可讀性。</span><span class="sxs-lookup"><span data-stu-id="ce193-137">Another way is by using complementary colors instead of adjacent colors for better readability.</span></span> <span data-ttu-id="ce193-138">互補色彩是一組相反色調的色彩，例如藍色和黃色。</span><span class="sxs-lookup"><span data-stu-id="ce193-138">Complementary colors are pairs of colors that are of opposite hue, such as blue and yellow.</span></span> <span data-ttu-id="ce193-139">下列並存範例顯示如何使用互補色彩來協助改善色彩對比。</span><span class="sxs-lookup"><span data-stu-id="ce193-139">The following side-by-side example shows how using complementary colors can help improve color contrast.</span></span>

![文字色彩在可讀性上的效果範例。](images/color.png)

 

 



