---
title: Color
description: Color 是大部分使用者介面的重要視覺元素。
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ae58ddf232a3d8311a917ea0475c7aca1bae8949
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104116016"
---
# <a name="color"></a><span data-ttu-id="81257-103">Color</span><span class="sxs-lookup"><span data-stu-id="81257-103">Color</span></span>

> [!NOTE]
> <span data-ttu-id="81257-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="81257-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="81257-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="81257-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="81257-106">Color 是大部分使用者介面的重要視覺元素。</span><span class="sxs-lookup"><span data-stu-id="81257-106">Color is an important visual element of most user interfaces.</span></span> <span data-ttu-id="81257-107">除了純美學之外，color 具有相關聯的意義和 elicits 情緒回應。</span><span class="sxs-lookup"><span data-stu-id="81257-107">Beyond pure aesthetics, color has associated meanings and elicits emotional responses.</span></span> <span data-ttu-id="81257-108">為了避免混淆，必須一致地使用色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-108">To prevent confusion in meaning, color must be used consistently.</span></span> <span data-ttu-id="81257-109">若要取得所需的情緒回應，必須適當地使用色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-109">To obtain the desired emotional responses, color must be used appropriately.</span></span>

<span data-ttu-id="81257-110">色彩通常是以色彩空間的角度來思考，其中 RGB (紅色、綠色、藍色) 、HSL (色調、飽和度、亮度) 和 HSV (色調、飽和度、值) 是最常使用的色彩空間。</span><span class="sxs-lookup"><span data-stu-id="81257-110">Color is often thought of in terms of a color space, where RGB (red, green, blue), HSL (hue, saturation, luminosity), and HSV (hue, saturation, value) are the most commonly used color spaces.</span></span>

![<span data-ttu-id="81257-111">顯示色彩關聯性之 cube 的圖</span><span class="sxs-lookup"><span data-stu-id="81257-111">figure of a cube showing color relationships</span></span> ](images/vis-color-image1.png)

<span data-ttu-id="81257-112">RGB 色彩空間可哥視化為 cube。</span><span class="sxs-lookup"><span data-stu-id="81257-112">The RGB color space can be visualized as a cube.</span></span>

<span data-ttu-id="81257-113">雖然顯示器技術會使用 RGB 值，因此開發人員通常會在 RGB 方面考慮色彩，但 RGB 色彩空間不會對應到人們觀察色彩的方式。</span><span class="sxs-lookup"><span data-stu-id="81257-113">While display technology uses RGB values and consequently developers often think of colors in terms of RGB, the RGB color space doesn't correspond to how people perceive color.</span></span> <span data-ttu-id="81257-114">例如，如果您將紅色新增至深青，則結果不會被視為紅色但較淺的青色。</span><span class="sxs-lookup"><span data-stu-id="81257-114">For example, if you add red to dark cyan, the result isn't perceived as more red but as lighter cyan.</span></span>

![<span data-ttu-id="81257-115">深色和淺青方塊的圖例</span><span class="sxs-lookup"><span data-stu-id="81257-115">illustration of dark and light cyan squares</span></span> ](images/vis-color-image2.png)

<span data-ttu-id="81257-116">在此範例中，新增紅色到深青會讓它變得更淺，而不是紅色。</span><span class="sxs-lookup"><span data-stu-id="81257-116">In this example, adding red to dark cyan makes it lighter, not more red.</span></span> <span data-ttu-id="81257-117">RGB 色彩空間不會與人們觀察色彩的方式相對應。</span><span class="sxs-lookup"><span data-stu-id="81257-117">The RGB color space doesn't correspond to how people perceive color.</span></span>

<span data-ttu-id="81257-118">HSL/HSV 色彩空間是由三個元件所組成：色調、飽和度和亮度或值。</span><span class="sxs-lookup"><span data-stu-id="81257-118">The HSL/HSV color spaces consist of three components: hue, saturation, and luminosity or value.</span></span> <span data-ttu-id="81257-119">這些色彩空間通常是用來取代 RGB，因為它們比較符合人們觀察色彩的方式。</span><span class="sxs-lookup"><span data-stu-id="81257-119">These color spaces are often used instead of RGB because they better match how people perceive color.</span></span>

<span data-ttu-id="81257-120">HSL 色彩空間會形成一個雙錐形，也就是在頂端的白色、最底部的黑色，以及中間的中性：</span><span class="sxs-lookup"><span data-stu-id="81257-120">The HSL color space forms a double cone that is white on the top, black on the bottom, and neutral in the middle:</span></span>

-   <span data-ttu-id="81257-121">**色調：** 色輪中的基本色彩，範圍從0到360度，其中0和360度都是紅色。</span><span class="sxs-lookup"><span data-stu-id="81257-121">**Hue:** The basic color in the color wheel, ranging from 0 to 360 degrees where both 0 and 360 degrees are red.</span></span>

    ![<span data-ttu-id="81257-122">顯示色彩關聯性的圓形圖</span><span class="sxs-lookup"><span data-stu-id="81257-122">figure of a circle showing color relationships</span></span> ](images/vis-color-image3.png)

    <span data-ttu-id="81257-123">色彩滾輪（紅色為0度）、黃色為60度、綠色為120度、青色為180度、藍色為240度，而紅色為300度。</span><span class="sxs-lookup"><span data-stu-id="81257-123">The color wheel, where red is 0 degrees, yellow is 60 degrees, green is 120 degrees, cyan is 180 degrees, blue is 240 degrees, and magenta is 300 degrees.</span></span>

-   <span data-ttu-id="81257-124">**飽和度：** 純色的純 (與單調) 的色彩是，範圍從0到100，其中100是完全飽和，0是灰色。</span><span class="sxs-lookup"><span data-stu-id="81257-124">**Saturation:** How pure (vs. dull) the color is, ranging from 0 to 100, where 100 is fully saturated and 0 is gray.</span></span>
-   <span data-ttu-id="81257-125">**亮度：** 色彩的亮度（範圍從0到100），其中100的 (白色，不論色調和飽和度) ，0的亮度越深 (黑色) 。</span><span class="sxs-lookup"><span data-stu-id="81257-125">**Luminosity:** How light the color is, ranging from 0 to 100, where 100 is as light as possible (white, regardless of the hue and saturation) and 0 is as dark as possible (black).</span></span>

    ![<span data-ttu-id="81257-126">說明 hsl 色彩空間的圖表</span><span class="sxs-lookup"><span data-stu-id="81257-126">figure illustrating hsl color space</span></span> ](images/vis-color-image4.png)

    <span data-ttu-id="81257-127">HSL 色彩空間可哥視化為雙錐形。</span><span class="sxs-lookup"><span data-stu-id="81257-127">The HSL color space can be visualized as a double cone.</span></span>

<span data-ttu-id="81257-128">HSV 色彩空間很類似，不同之處在于其空間形成單一錐形：</span><span class="sxs-lookup"><span data-stu-id="81257-128">The HSV color space is similar, except that its space forms a single cone:</span></span>

-   <span data-ttu-id="81257-129">**色調：** 色輪中的基本色彩，範圍從0到360度，其中0和360度都是紅色。</span><span class="sxs-lookup"><span data-stu-id="81257-129">**Hue:** The basic color in the color wheel, ranging from 0 to 360 degrees where both 0 and 360 degrees are red.</span></span>
-   <span data-ttu-id="81257-130">**飽和度：** 純色的純 (與單調) 的色彩是，範圍從0到100，其中100是完全飽和，0是灰色。</span><span class="sxs-lookup"><span data-stu-id="81257-130">**Saturation:** How pure (vs. dull) the color is, ranging from 0 to 100, where 100 is fully saturated and 0 is gray.</span></span>
-   <span data-ttu-id="81257-131">**值：** 色彩的明暗程度（範圍從0到100），100越亮越好 (這在 HSL 空間中是半亮度) 而0越深 (黑色) 。</span><span class="sxs-lookup"><span data-stu-id="81257-131">**Value:** How bright the color is, ranging from 0 to 100, where 100 is as bright as possible (which is half luminosity in the HSL space) and 0 is as dark as possible (black).</span></span>

    ![<span data-ttu-id="81257-132">說明 hsv 色彩空間的圖表</span><span class="sxs-lookup"><span data-stu-id="81257-132">figure illustrating hsv color space</span></span> ](images/vis-color-image5.png)

    <span data-ttu-id="81257-133">HSV 色彩空間可哥視化為單一錐形。</span><span class="sxs-lookup"><span data-stu-id="81257-133">The HSV color space can be visualized as a single cone.</span></span>

<span data-ttu-id="81257-134">在 HSL 和 HSV 空間中，如果飽和度為0，則亮度會指定灰色的陰影。</span><span class="sxs-lookup"><span data-stu-id="81257-134">In both HSL and HSV spaces, if saturation is 0 then luminosity specifies a shade of gray.</span></span> <span data-ttu-id="81257-135">在 Windows 中，HSL 和 HSV 空間通常會重新對應到0到240之間的小數位數，讓色彩可以用32位值表示。</span><span class="sxs-lookup"><span data-stu-id="81257-135">In Windows, the HSL and HSV spaces are usually remapped to a scale between 0 to 240 so that colors can be represented with a 32-bit value.</span></span>

<span data-ttu-id="81257-136">**注意：**[與字型和](vis-fonts.md)[協助工具](inter-accessibility.md)相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="81257-136">**Note:** Guidelines related to [fonts](vis-fonts.md) and [accessibility](inter-accessibility.md) are presented in separate articles.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="81257-137">設計概念</span><span class="sxs-lookup"><span data-stu-id="81257-137">Design concepts</span></span>

<span data-ttu-id="81257-138">色彩的有效使用可讓您的程式使用者介面 (UI) 更有效率。</span><span class="sxs-lookup"><span data-stu-id="81257-138">Effective use of color can make your program's user interface (UI) more effective.</span></span> <span data-ttu-id="81257-139">色彩可協助使用者一眼就瞭解某些意義。</span><span class="sxs-lookup"><span data-stu-id="81257-139">Color can help users understand certain meanings at a glance.</span></span> <span data-ttu-id="81257-140">色彩也可以讓您的產品更容易以賞心悅目，而且更精簡。</span><span class="sxs-lookup"><span data-stu-id="81257-140">Color can also make your product appear more aesthetically pleasing and refined.</span></span>

<span data-ttu-id="81257-141">可惜的是，使用色彩無效很簡單，特別是當您未在視覺化設計中進行定型時。</span><span class="sxs-lookup"><span data-stu-id="81257-141">Unfortunately, it's all too easy to use color ineffectively, especially if you are not trained in visual design.</span></span> <span data-ttu-id="81257-142">使用色彩結果不佳的設計外觀不專業、日期、混淆或單純不美觀。</span><span class="sxs-lookup"><span data-stu-id="81257-142">Poor use of color results in designs that look unprofessional, dated, confusing, or just plain ugly.</span></span> <span data-ttu-id="81257-143">色彩不佳的用法可能會比完全不使用色彩更糟。</span><span class="sxs-lookup"><span data-stu-id="81257-143">A poor use of color can be worse than not using color at all.</span></span>

<span data-ttu-id="81257-144">本節說明有效使用色彩的須知事項。</span><span class="sxs-lookup"><span data-stu-id="81257-144">This section explains what you need to know to use color effectively.</span></span>

### <a name="how-color-is-used"></a><span data-ttu-id="81257-145">使用色彩的方式</span><span class="sxs-lookup"><span data-stu-id="81257-145">How color is used</span></span>

<span data-ttu-id="81257-146">色彩通常是在 UI 中用來進行通訊：</span><span class="sxs-lookup"><span data-stu-id="81257-146">Color is typically used in UI to communicate:</span></span>

-   <span data-ttu-id="81257-147">**意義。**</span><span class="sxs-lookup"><span data-stu-id="81257-147">**Meaning.**</span></span> <span data-ttu-id="81257-148">您可以透過色彩來摘要訊息的意義。</span><span class="sxs-lookup"><span data-stu-id="81257-148">The meaning of a message can be summarized through color.</span></span> <span data-ttu-id="81257-149">例如，色彩通常用來傳達紅色有問題或錯誤的狀態、黃色表示警告或警告，綠色表示良好。</span><span class="sxs-lookup"><span data-stu-id="81257-149">For example, color is often used to communicate status where red is a problem or error, yellow is caution or warning, and green is good.</span></span>
-   <span data-ttu-id="81257-150">**狀態。**</span><span class="sxs-lookup"><span data-stu-id="81257-150">**State.**</span></span> <span data-ttu-id="81257-151">物件的狀態可透過色彩表示。</span><span class="sxs-lookup"><span data-stu-id="81257-151">An object's state can be indicated through color.</span></span> <span data-ttu-id="81257-152">例如，Windows 使用 color 來表示選取範圍和暫留狀態。</span><span class="sxs-lookup"><span data-stu-id="81257-152">For example, Windows uses color to indicate selection and hover states.</span></span> <span data-ttu-id="81257-153">網頁中的連結會使用藍色進行未造訪，並使用紫色進行流覽。</span><span class="sxs-lookup"><span data-stu-id="81257-153">Links within Web pages use blue for unvisited and purple for visited.</span></span>
-   <span data-ttu-id="81257-154">**分化。**</span><span class="sxs-lookup"><span data-stu-id="81257-154">**Differentiation.**</span></span> <span data-ttu-id="81257-155">人們假設相同色彩的專案之間有關聯性，因此色彩編碼是區分物件的有效方式。</span><span class="sxs-lookup"><span data-stu-id="81257-155">People assume that there is a relationship between items of the same color, so color coding is an effective way to differentiate between objects.</span></span> <span data-ttu-id="81257-156">例如，在 [控制台] 專案中，工作窗格會使用綠色背景，以視覺方式將它們與主要內容分開。</span><span class="sxs-lookup"><span data-stu-id="81257-156">For example, in a control panel item, task panes use a green background to visually separate them from the main content.</span></span> <span data-ttu-id="81257-157">此外，Microsoft Outlook 還可讓使用者將不同的彩色旗標指派給訊息。</span><span class="sxs-lookup"><span data-stu-id="81257-157">Also, Microsoft Outlook allows users to assign different colored flags to messages.</span></span>
-   <span data-ttu-id="81257-158">**重點。**</span><span class="sxs-lookup"><span data-stu-id="81257-158">**Emphasis.**</span></span> <span data-ttu-id="81257-159">色彩可以用來繪製使用者的注意力。</span><span class="sxs-lookup"><span data-stu-id="81257-159">Color can be used to draw users' attention.</span></span> <span data-ttu-id="81257-160">例如，Windows 會使用藍色的 [主要指示](text-ui.md) 來協助它們從其他文字中脫穎而出。</span><span class="sxs-lookup"><span data-stu-id="81257-160">For example, Windows uses blue [main instructions](text-ui.md) to help them stand out from the other text.</span></span>

<span data-ttu-id="81257-161">當然，圖形中通常只會使用色彩來進行純粹的美觀原因。</span><span class="sxs-lookup"><span data-stu-id="81257-161">Of course, color is often used in graphics for purely aesthetic reasons.</span></span> <span data-ttu-id="81257-162">雖然美學很重要，但您應該根據它們所代表的意義來選擇 UI 元素的色彩，而不是它們的外觀。</span><span class="sxs-lookup"><span data-stu-id="81257-162">While aesthetics are important, you should choose the colors of UI elements primarily based on what they mean, not how they look.</span></span>

### <a name="color-interpretation"></a><span data-ttu-id="81257-163">色彩解讀</span><span class="sxs-lookup"><span data-stu-id="81257-163">Color interpretation</span></span>

<span data-ttu-id="81257-164">**使用者的色彩解釋通常會相依于文化特性。**</span><span class="sxs-lookup"><span data-stu-id="81257-164">**Users' interpretation of color is often culturally dependent.**</span></span> <span data-ttu-id="81257-165">例如，在美國，新娘的婚禮服裝主要與白色色彩相關聯，而黑色則與 funerals 相關聯。</span><span class="sxs-lookup"><span data-stu-id="81257-165">For example, in the United States, wedding attire for the bride is largely associated with the color white, while black is associated with funerals.</span></span> <span data-ttu-id="81257-166">不過，在日本，色彩符號正好相反：白色是在 funerals 的主要色彩，而黑色則被視為很幸運婚禮的色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-166">However, long ago in Japan the color symbolism was just the opposite: white was the predominant color at funerals, and black was considered a color that brings good luck for weddings.</span></span>

<span data-ttu-id="81257-167">話雖如此， **紅色、黃色和綠色對於狀態的解讀是全域一致的。**</span><span class="sxs-lookup"><span data-stu-id="81257-167">That said, **the interpretation of red, yellow, and green for status is consistent globally.**</span></span> <span data-ttu-id="81257-168">這是因為 [UNESCO 維也納慣例的道路正負號和信號](https://www.unece.org/trans/conventn/signalse.pdf)，會定義交通燈的全球慣例 (其中 red 表示 stop、綠表示繼續，而黃色表示繼續) 的警告。</span><span class="sxs-lookup"><span data-stu-id="81257-168">This is due to the [UNESCO Vienna Convention on Road Signs and Signals](https://www.unece.org/trans/conventn/signalse.pdf), which defines the worldwide convention for traffic lights (where red means stop, green means proceed, and yellow means proceed with caution).</span></span> <span data-ttu-id="81257-169">您可以使用這些狀態色彩，而不需要考慮與文化特性相關的解釋。</span><span class="sxs-lookup"><span data-stu-id="81257-169">You can use these status colors without concern for culturally dependent interpretations.</span></span>

<span data-ttu-id="81257-170">除了狀態色彩之外，Windows 也會根據慣例將意義指派給色彩，如本文的指導方針一節所示。</span><span class="sxs-lookup"><span data-stu-id="81257-170">Beyond the status colors, Windows assigns meanings to colors based on convention, as presented in the Guidelines section of this article.</span></span> <span data-ttu-id="81257-171">確定您的程式色彩使用方式與這些色彩慣例相容。</span><span class="sxs-lookup"><span data-stu-id="81257-171">Be sure that your program's color usage is compatible with these color conventions.</span></span>

### <a name="color-accessibility"></a><span data-ttu-id="81257-172">色彩存取範圍</span><span class="sxs-lookup"><span data-stu-id="81257-172">Color accessibility</span></span>

<span data-ttu-id="81257-173">色彩的使用會影響您的軟體對最廣泛的物件的存取性。</span><span class="sxs-lookup"><span data-stu-id="81257-173">Use of color affects the accessibility of your software to the widest possible audience.</span></span> <span data-ttu-id="81257-174">具有視力或弱視的使用者可能看不到這些色彩的效果。</span><span class="sxs-lookup"><span data-stu-id="81257-174">Users with blindness or low vision may not be able to see the colors well, if at all.</span></span> <span data-ttu-id="81257-175">有大約8% 的成人男性具有某種形式的色彩混淆 (通常不正確地稱為「色盲」 ) ，其中紅色綠色的色彩混淆是最常見的。</span><span class="sxs-lookup"><span data-stu-id="81257-175">Approximately 8 percent of adult males have some form of color confusion (often incorrectly referred to as "color blindness"), of which red-green color confusion is the most common.</span></span>

![<span data-ttu-id="81257-176">顯示如往常一樣的主要色彩圖表</span><span class="sxs-lookup"><span data-stu-id="81257-176">figure showing primary colors as normally seen</span></span> ](images/vis-color-image6.png)

<span data-ttu-id="81257-177">一般色彩視覺所見的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-177">The primary colors as seen with normal color vision.</span></span>

![<span data-ttu-id="81257-178">顯示與 protanopia 所見相同色彩的圖表</span><span class="sxs-lookup"><span data-stu-id="81257-178">figure showing same colors as seen with protanopia</span></span> ](images/vis-color-image7.png)

<span data-ttu-id="81257-179">Protanopia (1% 的男性擴展) 所看到的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-179">The primary colors as seen with Protanopia (1% of male population).</span></span>

![<span data-ttu-id="81257-180">顯示 deuteranopia 顯示相同色彩的圖</span><span class="sxs-lookup"><span data-stu-id="81257-180">figure showing same colors seen with deuteranopia</span></span> ](images/vis-color-image8.png)

<span data-ttu-id="81257-181">Deuteranopia (6% 的男性擴展) 看到的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-181">The primary colors as seen with Deuteranopia (6% of male population).</span></span>

![<span data-ttu-id="81257-182">顯示與 tritanopia 所見相同色彩的圖表</span><span class="sxs-lookup"><span data-stu-id="81257-182">figure showing same colors as seen with tritanopia</span></span> ](images/vis-color-image9.png)

<span data-ttu-id="81257-183">Tritanopia (1% 的男性擴展) 所看到的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-183">The primary colors as seen with Tritanopia (1% of male population).</span></span>

<span data-ttu-id="81257-184">如需詳細資訊，請參閱 [Color-Blind 使用者可以看到您的網站嗎？](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="81257-184">For more information, see [Can Color-Blind Users See Your Site?](/previous-versions/windows/internet-explorer/ie-developer/)</span></span>

### <a name="use-color-to-reinforce-visually"></a><span data-ttu-id="81257-185">使用色彩以視覺化方式強化</span><span class="sxs-lookup"><span data-stu-id="81257-185">Use color to reinforce visually</span></span>

<span data-ttu-id="81257-186">色彩解讀和協助工具問題的最佳解決方法是使用色彩，以視覺方式強調其中一個主要通訊方法的意義：</span><span class="sxs-lookup"><span data-stu-id="81257-186">The best solution to the color interpretation and accessibility problems is to use color to visually reinforce the meaning of one of these primary methods of communication:</span></span>

-   <span data-ttu-id="81257-187">**Text**。</span><span class="sxs-lookup"><span data-stu-id="81257-187">**Text.**</span></span> <span data-ttu-id="81257-188">簡潔的文字通常是直接在 UI 上或透過工具提示最有效的主要通訊。</span><span class="sxs-lookup"><span data-stu-id="81257-188">Concise text is usually the most effective primary communication either directly on the UI or through a tooltip.</span></span>

![<span data-ttu-id="81257-189">具有工具提示之小紅色圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="81257-189">screen shot of small red icon with tooltip</span></span> ](images/vis-color-image10.png)

<span data-ttu-id="81257-190">在此範例中，會使用工具提示文字來傳達圖示的意義。</span><span class="sxs-lookup"><span data-stu-id="81257-190">In this example, tooltip text is used to communicate an icon's meaning.</span></span>

-   <span data-ttu-id="81257-191">**設計。**</span><span class="sxs-lookup"><span data-stu-id="81257-191">**Design.**</span></span> <span data-ttu-id="81257-192">這些圖示很容易由設計來區分，尤其是其大綱圖形。</span><span class="sxs-lookup"><span data-stu-id="81257-192">Icons are easily distinguished by the designs, especially their outline shape.</span></span>

![<span data-ttu-id="81257-193">灰色陰影 (灰階) 的圖示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="81257-193">screen shot of icons in shades of gray (grayscale)</span></span> ](images/vis-color-image11.png)

<span data-ttu-id="81257-194">在此範例中，標準圖示可以根據其設計立即進行辨別。</span><span class="sxs-lookup"><span data-stu-id="81257-194">In this example, the standard icons are readily distinguishable based on their designs.</span></span>

-   <span data-ttu-id="81257-195">**位置。**</span><span class="sxs-lookup"><span data-stu-id="81257-195">**Location.**</span></span> <span data-ttu-id="81257-196">也可以使用相對位置，但這種方法比替代方案更弱。</span><span class="sxs-lookup"><span data-stu-id="81257-196">Relative location can also be used, but this approach is weaker than the alternatives.</span></span> <span data-ttu-id="81257-197">為了有效，此位置應該是標準且知名的，如同流量燈。</span><span class="sxs-lookup"><span data-stu-id="81257-197">To be effective, the location should be standard and well known, as with traffic lights.</span></span>

<span data-ttu-id="81257-198">雖然 color 是許多設計中最明顯的屬性，但它必須永遠是多餘的。</span><span class="sxs-lookup"><span data-stu-id="81257-198">While color is the most obvious attribute of many designs, it must always be redundant.</span></span>

### <a name="designing-with-color"></a><span data-ttu-id="81257-199">使用色彩設計</span><span class="sxs-lookup"><span data-stu-id="81257-199">Designing with color</span></span>

<span data-ttu-id="81257-200">諷刺是，設計色彩的最佳方式是從使用 [框線](glossary.md) 或單色設計沒有色彩的方式開始，然後稍後再加入色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-200">Ironically, the best way to design for color is to start by designing without color, using either [wireframes](glossary.md) or monochrome, and then add color later.</span></span> <span data-ttu-id="81257-201">這樣做有助於確保資訊不會單獨使用色彩進行通訊。</span><span class="sxs-lookup"><span data-stu-id="81257-201">Doing so helps ensure that information isn't being communicated using color alone.</span></span> <span data-ttu-id="81257-202">它也有助於確保您的列印功能在單色印表機上看起來很棒。</span><span class="sxs-lookup"><span data-stu-id="81257-202">It also helps ensure that your printouts look great on monochrome printers.</span></span>

### <a name="use-theme-or-system-colors"></a><span data-ttu-id="81257-203">使用主題或系統色彩</span><span class="sxs-lookup"><span data-stu-id="81257-203">Use theme or system colors</span></span>

<span data-ttu-id="81257-204">雖然在使用色彩方面有許多複雜的因素，但是在 Windows UI 中，選擇 [色彩] 通常是根據幾個簡單的規則來選擇適當的 [主題色彩](glossary.md) 或 [系統色彩](glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="81257-204">While there are many complex factors in using color effectively, in Windows UI choosing color often boils down to simply choosing the appropriate [theme color](glossary.md) or [system color](glossary.md) according to a few simple rules.</span></span> <span data-ttu-id="81257-205">然後，使用者可以選擇並自訂這些色彩配置。</span><span class="sxs-lookup"><span data-stu-id="81257-205">Users can then select and customize these color schemes as they choose.</span></span>

<span data-ttu-id="81257-206">如此一來，您不僅可以容納所有使用者的色彩喜好設定，還可以消除選擇一個適用于所有 tastes、樣式和文化特性之完美色彩配置的負擔 (當然，這種情況下無法) 。</span><span class="sxs-lookup"><span data-stu-id="81257-206">By doing so, not only do you accommodate the color preferences of all your users, but you eliminate the burden of choosing the one perfect color scheme that works for all tastes, styles, and cultures (which, of course, is otherwise impossible).</span></span>

<span data-ttu-id="81257-207">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="81257-207">**If you do only one thing...**</span></span>

<span data-ttu-id="81257-208">選取適當的主題色彩或系統色彩來選擇色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-208">Choose colors by selecting the appropriate theme color or system color.</span></span> <span data-ttu-id="81257-209">絕對不要使用色彩做為通訊的主要方法，而是以視覺化方式強調意義的次要方法。</span><span class="sxs-lookup"><span data-stu-id="81257-209">Never use color as a primary method of communication, but as a secondary method to reinforce meaning visually.</span></span> <span data-ttu-id="81257-210">使用框線或單色進行設計，以協助確保色彩為次要。</span><span class="sxs-lookup"><span data-stu-id="81257-210">Design using wireframes or monochrome to help ensure that color is secondary.</span></span>

### <a name="use-theme-or-system-colors-correctly"></a><span data-ttu-id="81257-211">使用正確的主題或系統色彩</span><span class="sxs-lookup"><span data-stu-id="81257-211">Use theme or system colors correctly</span></span>

<span data-ttu-id="81257-212">假設使用者根據自己的個人需求選擇主題或系統色彩，並適當地建造主題或系統色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-212">Assume that users choose theme or system colors based on their personal needs and that the theme or system colors are constructed appropriately.</span></span> <span data-ttu-id="81257-213">根據這項假設，如果您一律根據其預定用途和與其相關聯的背景來選擇 [主題] 或 [系統色彩]，則可保證在所有的影片模式中都能清楚地顯示色彩，並尊重使用者的願望，包括 [高對比模式](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="81257-213">Based on this assumption, if you always choose theme or system colors based on their intended purpose and pair foregrounds with their associated backgrounds, the colors are guaranteed to be legible and respect users' wishes in all video modes, including [high-contrast mode](glossary.md).</span></span> <span data-ttu-id="81257-214">例如，視窗文字系統色彩保證可以針對視窗背景系統色彩進行可讀性。</span><span class="sxs-lookup"><span data-stu-id="81257-214">For example, the window text system color is guaranteed to be legible against the window background system color.</span></span>

<span data-ttu-id="81257-215">具體而言，一律：</span><span class="sxs-lookup"><span data-stu-id="81257-215">Specifically, always:</span></span>

-   <span data-ttu-id="81257-216">**根據其用途來選擇色彩。**</span><span class="sxs-lookup"><span data-stu-id="81257-216">**Choose colors based on their purpose.**</span></span> <span data-ttu-id="81257-217">請勿根據其目前的外觀來選擇色彩，因為使用者或未來的 Windows 版本可以變更外觀。</span><span class="sxs-lookup"><span data-stu-id="81257-217">Don't choose colors based on their current appearance because that appearance can be changed by the user or future versions of Windows.</span></span>
-   <span data-ttu-id="81257-218">**比對前景色彩與其相關聯的背景色彩。**</span><span class="sxs-lookup"><span data-stu-id="81257-218">**Match foreground colors with their associated background colors.**</span></span> <span data-ttu-id="81257-219">前景色彩保證只能針對與其相關聯的背景色彩進行清楚的色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-219">Foreground colors are guaranteed to be legible only against their associated background colors.</span></span> <span data-ttu-id="81257-220">請勿混搭前景色彩，並將其與其他背景色彩比對，或其他前景色彩更糟。</span><span class="sxs-lookup"><span data-stu-id="81257-220">Don't mix and match foreground colors with other background colors, or worse yet, other foreground colors.</span></span>
-   <span data-ttu-id="81257-221">**不要混合色彩類型。**</span><span class="sxs-lookup"><span data-stu-id="81257-221">**Don't mix color types.**</span></span> <span data-ttu-id="81257-222">也就是說，一律比對主題色彩與其相關聯的主題色彩、系統色彩與其相關聯的系統色彩，以及使用其他寫死色彩寫死色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-222">That is, always match theme colors with their associated theme colors, system colors with their associated system colors, and hardwired colors with other hardwired colors.</span></span> <span data-ttu-id="81257-223">例如，不保證會針對寫死背景，提供主題文字色彩的可讀性。</span><span class="sxs-lookup"><span data-stu-id="81257-223">For example, a theme text color isn't guaranteed to be legible against a hardwired background.</span></span>
-   <span data-ttu-id="81257-224">**如果您必須 hardwire 色彩，請以特殊案例處理高對比模式。**</span><span class="sxs-lookup"><span data-stu-id="81257-224">**If you must hardwire colors, handle high-contrast mode as a special case.**</span></span>

<span data-ttu-id="81257-225">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="81257-225">**If you do only one thing...**</span></span>

<span data-ttu-id="81257-226">一律根據其預定用途選擇主題或系統色彩，並將 foregrounds 與其相關聯的背景配對。</span><span class="sxs-lookup"><span data-stu-id="81257-226">Always choose theme or system colors based on their intended purpose, and pair foregrounds with their associated backgrounds.</span></span>

### <a name="using-other-colors"></a><span data-ttu-id="81257-227">使用其他色彩</span><span class="sxs-lookup"><span data-stu-id="81257-227">Using other colors</span></span>

<span data-ttu-id="81257-228">雖然 Windows 主題會定義一組完整的主題元件，但您可能會發現您的程式需要在主題檔案中未定義的色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-228">While the Windows theme defines a comprehensive set of theme parts, you may find that your program needs colors that aren't defined in the theme file.</span></span> <span data-ttu-id="81257-229">雖然您可以 hardwire 這類色彩，但更好的方法是從主題或系統色彩衍生色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-229">While you could hardwire such colors, a better approach is to derive colors from the theme or system colors.</span></span> <span data-ttu-id="81257-230">策略性地使用這種方法，可提供您使用主題和系統色彩的所有優點，但有更大的彈性。</span><span class="sxs-lookup"><span data-stu-id="81257-230">Strategically using this approach gives you all the benefits of using theme and system colors, but with much more flexibility.</span></span>

<span data-ttu-id="81257-231">例如，假設您需要比主題視窗背景色彩更深色的視窗背景。</span><span class="sxs-lookup"><span data-stu-id="81257-231">For example, suppose you need a window background that is darker than the theme window background color.</span></span> <span data-ttu-id="81257-232">在 HSL 色彩空間中，具有較深的色彩表示亮度較低的色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-232">In the HSL color space, having a darker color means a color with a lower luminosity.</span></span> <span data-ttu-id="81257-233">因此，您可以使用下列步驟來衍生較深的視窗背景色彩：</span><span class="sxs-lookup"><span data-stu-id="81257-233">Thus, you can derive a darker window background color using the following steps:</span></span>

-   <span data-ttu-id="81257-234">取得視窗背景主題色彩 RGB。</span><span class="sxs-lookup"><span data-stu-id="81257-234">Obtain the window background theme color RGB.</span></span>
-   <span data-ttu-id="81257-235">將 RGB 轉換成其 HSL 值。</span><span class="sxs-lookup"><span data-stu-id="81257-235">Convert the RGB to its HSL value.</span></span>
-   <span data-ttu-id="81257-236"> (除以 20%) ，減少亮度值。</span><span class="sxs-lookup"><span data-stu-id="81257-236">Reduce the luminosity value (by, say, 20 percent).</span></span>
-   <span data-ttu-id="81257-237">轉換回 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="81257-237">Convert back to RGB values.</span></span>

<span data-ttu-id="81257-238">使用這種方法時，衍生的色彩一定會被視為原始色彩的較深陰影 (除非原始色彩的開頭非常深。 ) </span><span class="sxs-lookup"><span data-stu-id="81257-238">Using this approach, the derived color is guaranteed to be perceived as a darker shade of the original color (unless the original color was very dark to begin with.)</span></span>

![<span data-ttu-id="81257-239">顯示降低亮度之效果的圖例</span><span class="sxs-lookup"><span data-stu-id="81257-239">illustration showing effects of reduced luminosity</span></span> ](images/vis-color-image12.png)

<span data-ttu-id="81257-240">在此範例中，較深色的視窗背景色彩衍生自主題色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-240">In this example, a darker window background color is derived from the theme color.</span></span>

### <a name="testing-colors"></a><span data-ttu-id="81257-241">測試色彩</span><span class="sxs-lookup"><span data-stu-id="81257-241">Testing colors</span></span>

<span data-ttu-id="81257-242">若要判斷您的程式使用色彩是否可供存取，而不是用來做為主要的通訊方法，建議您使用 [Fujitsu ColorDoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) 或 [Vischeck](https://www.vischeck.com/) 公用程式來檢查：</span><span class="sxs-lookup"><span data-stu-id="81257-242">To determine if your program's use of color is accessible and not used as a primary method of communication, we recommend using the [Fujitsu ColorDoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) or the [Vischeck](https://www.vischeck.com/) utilities to check for:</span></span>

-   <span data-ttu-id="81257-243">使用灰色尺規篩選的整體色彩相依性。</span><span class="sxs-lookup"><span data-stu-id="81257-243">Overall dependency on color using the Gray scale filter.</span></span>
-   <span data-ttu-id="81257-244">使用 Protanopia、Deuteranopia 和 Tritanopia 篩選器的特定色彩混淆問題。</span><span class="sxs-lookup"><span data-stu-id="81257-244">Specific color confusion problems using the Protanopia, Deuteranopia, and Tritanopia filters.</span></span>

<span data-ttu-id="81257-245">若要判斷您的程式使用色彩是否正確地進行程式設計，請以下列模式測試您的程式：</span><span class="sxs-lookup"><span data-stu-id="81257-245">To determine if your program's use of color is programmed correctly, test your program in the following modes:</span></span>

-   <span data-ttu-id="81257-246">使用預設 Windows 主題來啟用主題。</span><span class="sxs-lookup"><span data-stu-id="81257-246">Theming enabled using the default Windows theme.</span></span>
-   <span data-ttu-id="81257-247">使用非預設主題來啟用主題。</span><span class="sxs-lookup"><span data-stu-id="81257-247">Theming enabled using a non-default theme.</span></span>
-   <span data-ttu-id="81257-248">在個人化主控台專案) 的主題設定中，已停用 ( 「Windows 傳統樣式」的主題。</span><span class="sxs-lookup"><span data-stu-id="81257-248">Theming disabled ("Windows Classic style" in the Theme Settings in the Personalization Control Panel item).</span></span>
-   <span data-ttu-id="81257-249">高對比黑色背景) 上的黑色 (白色文字。</span><span class="sxs-lookup"><span data-stu-id="81257-249">High Contrast Black (white text on a black background).</span></span>
-   <span data-ttu-id="81257-250">高對比白色背景) 的白色 (黑色文字。</span><span class="sxs-lookup"><span data-stu-id="81257-250">High Contrast White (black text on a white background).</span></span>

<span data-ttu-id="81257-251">所有的螢幕元素應該都能清晰清晰，並如預期般出現，即使在模式變更後立即顯示。</span><span class="sxs-lookup"><span data-stu-id="81257-251">All the screen elements should be legible and appear as expected, even immediately after mode changes.</span></span>

## <a name="guidelines"></a><span data-ttu-id="81257-252">指導方針</span><span class="sxs-lookup"><span data-stu-id="81257-252">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="81257-253">一般</span><span class="sxs-lookup"><span data-stu-id="81257-253">General</span></span>

-   <span data-ttu-id="81257-254">**絕對不要使用色彩做為通訊的主要方法，** 而是以視覺化方式強調意義的次要方法。</span><span class="sxs-lookup"><span data-stu-id="81257-254">**Never use color as a primary method of communication,** but as a secondary method to reinforce meaning visually.</span></span>

### <a name="using-theme-and-system-colors"></a><span data-ttu-id="81257-255">使用主題和系統色彩</span><span class="sxs-lookup"><span data-stu-id="81257-255">Using theme and system colors</span></span>

-   <span data-ttu-id="81257-256">可能的話，請 **選取適當的主題色彩或系統色彩來選擇色彩。**</span><span class="sxs-lookup"><span data-stu-id="81257-256">Whenever possible, **choose colors by selecting the appropriate theme color or system color.**</span></span> <span data-ttu-id="81257-257">如此一來，您一律可以尊重使用者的色彩喜好設定。</span><span class="sxs-lookup"><span data-stu-id="81257-257">By doing so, you can always respect users' color preference.</span></span>
-   <span data-ttu-id="81257-258">**根據其用途選擇主題和系統色彩。**</span><span class="sxs-lookup"><span data-stu-id="81257-258">**Choose theme and system colors based on their purpose.**</span></span> <span data-ttu-id="81257-259">請勿根據其目前的外觀來選擇色彩，因為使用者或未來的 Windows 版本可能會變更外觀。</span><span class="sxs-lookup"><span data-stu-id="81257-259">Don't choose colors based on their current appearance, as that appearance can be changed by the user or future versions of Windows.</span></span>
-   <span data-ttu-id="81257-260">**比對前景色彩與其相關聯的背景色彩。**</span><span class="sxs-lookup"><span data-stu-id="81257-260">**Match foreground colors with their associated background colors.**</span></span> <span data-ttu-id="81257-261">前景色彩保證只能針對與其相關聯的背景色彩進行清楚的色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-261">Foreground colors are guaranteed to be legible only against their associated background colors.</span></span> <span data-ttu-id="81257-262">請勿混搭前景色彩，並將其與其他背景色彩比對，或其他前景色彩更糟。</span><span class="sxs-lookup"><span data-stu-id="81257-262">Don't mix and match foreground colors with other background colors, or worse yet, other foreground colors.</span></span>
-   <span data-ttu-id="81257-263">**不要混合色彩類型。**</span><span class="sxs-lookup"><span data-stu-id="81257-263">**Don't mix color types.**</span></span> <span data-ttu-id="81257-264">也就是說，一律比對主題色彩與其相關聯的主題色彩、系統色彩與其相關聯的系統色彩，以及使用其他寫死色彩寫死色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-264">That is, always match theme colors with their associated theme colors, system colors with their associated system colors, and hardwired colors with other hardwired colors.</span></span> <span data-ttu-id="81257-265">例如，不保證會針對寫死背景，提供主題文字色彩的可讀性。</span><span class="sxs-lookup"><span data-stu-id="81257-265">For example, a theme text color isn't guaranteed to be legible against a hardwired background.</span></span>
-   <span data-ttu-id="81257-266">**如果您必須使用不是主題或系統色彩的色彩：**</span><span class="sxs-lookup"><span data-stu-id="81257-266">**If you must use a color that isn't a theme or system color:**</span></span>
    -   <span data-ttu-id="81257-267">**偏好從主題或系統色彩衍生色彩，而不是 hardwiring 其值。**</span><span class="sxs-lookup"><span data-stu-id="81257-267">**Prefer to derive the color from a theme or system color over hardwiring its value.**</span></span> <span data-ttu-id="81257-268">使用本文稍早所述的程式，以使用其他色彩。</span><span class="sxs-lookup"><span data-stu-id="81257-268">Use the process described earlier in this article, in Using other colors.</span></span>
    -   <span data-ttu-id="81257-269">**以特殊案例處理高對比模式。**</span><span class="sxs-lookup"><span data-stu-id="81257-269">**Handle high-contrast mode as a special case.**</span></span>
-   <span data-ttu-id="81257-270">**處理主題變更。**</span><span class="sxs-lookup"><span data-stu-id="81257-270">**Handle theme changes.**</span></span> <span data-ttu-id="81257-271">使用標準視窗框架和通用控制項的 windows 會自動處理主題變更。</span><span class="sxs-lookup"><span data-stu-id="81257-271">Theme changes are handled automatically by windows with standard window frames and common controls.</span></span> <span data-ttu-id="81257-272">具有自訂視窗框架、自訂或主控描繪控制項，以及色彩其他用法的視窗，必須明確地處理主題變更。</span><span class="sxs-lookup"><span data-stu-id="81257-272">Windows with custom window frames, custom or owner-draw controls, and other use of color must handle theme changes explicitly.</span></span>
    -   <span data-ttu-id="81257-273">**開發人員：** 您可以藉由處理 WM THEMECHANGED 訊息來回應主題變更事件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="81257-273">**Developers:** You can respond to theme change events by handling the WM\_THEMECHANGED message.</span></span>

### <a name="color-meaning"></a><span data-ttu-id="81257-274">色彩意義</span><span class="sxs-lookup"><span data-stu-id="81257-274">Color meaning</span></span>

-   <span data-ttu-id="81257-275">雖然您應該在每次可以時使用主題和系統色彩 (或衍生色彩) ，請確定色彩的任何其他用法都與 Windows 內色彩的下列使用方式相容。</span><span class="sxs-lookup"><span data-stu-id="81257-275">While you should use theme and system colors (or derived colors) whenever you can, make sure any other use of color is compatible with the following use of color within Windows.</span></span>



|                                      |                                                                               |                                                                                                                                                                 |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81257-276">**Hue**</span><span class="sxs-lookup"><span data-stu-id="81257-276">**Hue**</span></span><br/>                   | <span data-ttu-id="81257-277">**意義**</span><span class="sxs-lookup"><span data-stu-id="81257-277">**Meaning**</span></span><br/>                                                        | <span data-ttu-id="81257-278">**在 Windows 中使用**</span><span class="sxs-lookup"><span data-stu-id="81257-278">**Use in Windows**</span></span><br/>                                                                                                                                   |
| <span data-ttu-id="81257-279">藍色/綠色</span><span class="sxs-lookup"><span data-stu-id="81257-279">blue/green</span></span><br/>                | <span data-ttu-id="81257-280">Windows 品牌</span><span class="sxs-lookup"><span data-stu-id="81257-280">Windows brand</span></span><br/>                                                      | <span data-ttu-id="81257-281">背景： Windows 商標。</span><span class="sxs-lookup"><span data-stu-id="81257-281">Background: Windows branding.</span></span><br/>                                                                                                                        |
| <span data-ttu-id="81257-282">半透明、黑色、灰色、白色</span><span class="sxs-lookup"><span data-stu-id="81257-282">glass, black, gray, white</span></span><br/> | <span data-ttu-id="81257-283">neutral</span><span class="sxs-lookup"><span data-stu-id="81257-283">neutral</span></span><br/>                                                            | <span data-ttu-id="81257-284">背景：標準視窗框架、[開始] 功能表、工作列、提要欄位。</span><span class="sxs-lookup"><span data-stu-id="81257-284">Background: standard window frames, Start menu, taskbar, Sidebar.</span></span><br/> <span data-ttu-id="81257-285">前景：標準文字。</span><span class="sxs-lookup"><span data-stu-id="81257-285">Foreground: normal text.</span></span><br/>                                                |
| <span data-ttu-id="81257-286">藍色</span><span class="sxs-lookup"><span data-stu-id="81257-286">blue</span></span><br/>                      | <span data-ttu-id="81257-287">開始、認可</span><span class="sxs-lookup"><span data-stu-id="81257-287">start, commit</span></span><br/>                                                      | <span data-ttu-id="81257-288">背景：預設的命令按鈕、搜尋、登入。</span><span class="sxs-lookup"><span data-stu-id="81257-288">Background: default command buttons, search, log on.</span></span><br/> <span data-ttu-id="81257-289">圖示： information、Help。</span><span class="sxs-lookup"><span data-stu-id="81257-289">Icons: information, Help.</span></span><br/> <span data-ttu-id="81257-290">前景：主要指示、連結。</span><span class="sxs-lookup"><span data-stu-id="81257-290">Foreground: main instructions, links.</span></span><br/>           |
| <span data-ttu-id="81257-291">紅色</span><span class="sxs-lookup"><span data-stu-id="81257-291">red</span></span><br/>                       | <span data-ttu-id="81257-292">錯誤、停止、易受攻擊、重大、立即關注、受限</span><span class="sxs-lookup"><span data-stu-id="81257-292">error, stop, vulnerable, critical, immediate attention, restricted</span></span><br/> | <span data-ttu-id="81257-293">背景：狀態、已停止的進度 (進度列) 。</span><span class="sxs-lookup"><span data-stu-id="81257-293">Background: status, stopped progress (progress bars).</span></span><br/> <span data-ttu-id="81257-294">圖示：錯誤、停止、關閉視窗、刪除、必要輸入、遺失、無法使用。</span><span class="sxs-lookup"><span data-stu-id="81257-294">Icons: error, stop, close window, delete, required input, missing, unavailable.</span></span><br/>     |
| <span data-ttu-id="81257-295">黃色</span><span class="sxs-lookup"><span data-stu-id="81257-295">yellow</span></span><br/>                    | <span data-ttu-id="81257-296">警告，請注意，有疑問</span><span class="sxs-lookup"><span data-stu-id="81257-296">warning, caution, questionable</span></span><br/>                                     | <span data-ttu-id="81257-297">背景：狀態、暫停進度 (進度列) 。</span><span class="sxs-lookup"><span data-stu-id="81257-297">Background: status, paused progress (progress bars).</span></span><br/> <span data-ttu-id="81257-298">圖示：警告</span><span class="sxs-lookup"><span data-stu-id="81257-298">Icons: warning</span></span><br/>                                                                       |
| <span data-ttu-id="81257-299">綠色</span><span class="sxs-lookup"><span data-stu-id="81257-299">green</span></span><br/>                     | <span data-ttu-id="81257-300">go、繼續、進度、安全</span><span class="sxs-lookup"><span data-stu-id="81257-300">go, proceed, progress, safe</span></span><br/>                                        | <span data-ttu-id="81257-301">背景：狀態、正常進度 (進度列) 。</span><span class="sxs-lookup"><span data-stu-id="81257-301">Background: status, normal progress (progress bars).</span></span><br/> <span data-ttu-id="81257-302">圖示： go、完成、重新整理。</span><span class="sxs-lookup"><span data-stu-id="81257-302">Icons: go, done, refresh.</span></span><br/> <span data-ttu-id="81257-303">前景：搜尋結果中 (的路徑和 Url) 。</span><span class="sxs-lookup"><span data-stu-id="81257-303">Foreground: Paths and URLs (in search results).</span></span><br/> |
| <span data-ttu-id="81257-304">紫色</span><span class="sxs-lookup"><span data-stu-id="81257-304">purple</span></span><br/>                    | <span data-ttu-id="81257-305">訪問</span><span class="sxs-lookup"><span data-stu-id="81257-305">visited</span></span><br/>                                                            | <span data-ttu-id="81257-306">前景：已流覽的連結 (Windows Internet Explorer 和檔) 中的連結。</span><span class="sxs-lookup"><span data-stu-id="81257-306">Foreground: visited links (for links within Windows Internet Explorer and documents).</span></span><br/>                                                                |



 

-   <span data-ttu-id="81257-307">**若要避免傳達先前的意義，請選擇色彩的最高、低度和高或低亮度。**</span><span class="sxs-lookup"><span data-stu-id="81257-307">**To avoid communicating the previous meanings, choose colors have high mid to low saturation and high or low luminosity.**</span></span> <span data-ttu-id="81257-308">使用者將先前的意義與具有完整或高飽和度和中度亮度的色彩相關聯，因此您可以選擇不同的陰影來避免這些關聯。</span><span class="sxs-lookup"><span data-stu-id="81257-308">Users associate the previous meanings to colors that have full or high saturation and mid-level luminosity, so you can avoid these associations by choosing different shades.</span></span>

![<span data-ttu-id="81257-309">顯示亮度如何影響色彩的圖</span><span class="sxs-lookup"><span data-stu-id="81257-309">figure showing how luminosity affects color</span></span> ](images/vis-color-image13.png)

<span data-ttu-id="81257-310">在此範例中，有三種不同的黃色陰影，但只有高度飽和的中度亮度陰影會傳達警告。</span><span class="sxs-lookup"><span data-stu-id="81257-310">In this example, there are three different shades of yellow, but only the highly saturated, mid-level luminosity shade communicates warning.</span></span> <span data-ttu-id="81257-311">黃色資料夾圖示不會覺得警告。</span><span class="sxs-lookup"><span data-stu-id="81257-311">The yellow folder icon doesn't feel like a warning.</span></span>

### <a name="using-color-with-data"></a><span data-ttu-id="81257-312">使用色彩搭配資料</span><span class="sxs-lookup"><span data-stu-id="81257-312">Using color with data</span></span>

-   <span data-ttu-id="81257-313">當有説明時，請 **將色彩指派給資料，以協助使用者區分。**</span><span class="sxs-lookup"><span data-stu-id="81257-313">When helpful, **assign color to data to help users differentiate it.**</span></span> <span data-ttu-id="81257-314">請注意，使用者會假設具有類似色彩的資料具有類似的意義。</span><span class="sxs-lookup"><span data-stu-id="81257-314">Note that users will assume that data with similar colors have similar meanings.</span></span>
-   <span data-ttu-id="81257-315">**依預設，指派易於區別的色彩。**</span><span class="sxs-lookup"><span data-stu-id="81257-315">**Assign colors by default that are easy to distinguish.**</span></span> <span data-ttu-id="81257-316">一般來說，如果在 HSL/HSV 色彩空間中彼此不同，色彩很容易區分，同時維持高對比與其背景：</span><span class="sxs-lookup"><span data-stu-id="81257-316">Generally, colors are easy to distinguish if they are far apart from each other in the HSL/HSV color spaces, while maintaining high contrast with their background:</span></span>
    -   <span data-ttu-id="81257-317">選擇色彩時，偏好使用三角理論 harmonies 或互補色調，而不是連續的色調。</span><span class="sxs-lookup"><span data-stu-id="81257-317">When choosing colors, prefer triad harmonies or complementary hues, but not adjacent hues.</span></span>

        ![<span data-ttu-id="81257-318">顯示如何選擇對比色彩的圖</span><span class="sxs-lookup"><span data-stu-id="81257-318">figure showing how to choose contrasting colors</span></span> ](images/vis-color-image14.png)

        <span data-ttu-id="81257-319">在此範例中，如果第一個色彩指派為紅色，則下一個色彩應該是藍色、綠色或青色，但不能是洋紅、紫色、橙色或黃色。</span><span class="sxs-lookup"><span data-stu-id="81257-319">In this example, if the first color assignment is red, the next color should be blue, green, or cyan, but not magenta, purple, orange, or yellow.</span></span>

    -   <span data-ttu-id="81257-320">如果色調、飽和度或亮度有很大的差異，色彩會有高對比。</span><span class="sxs-lookup"><span data-stu-id="81257-320">Colors have high contrast if there is a large difference in their hue, saturation, or luminosity.</span></span>

        ![<span data-ttu-id="81257-321">顯示不同背景上的一種色彩的圖表</span><span class="sxs-lookup"><span data-stu-id="81257-321">figure showing one color on different backgrounds</span></span> ](images/vis-color-image15.png)

        <span data-ttu-id="81257-322">在此範例中，淺藍色基底色彩會與背景有很大的色調、飽和度或亮度有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="81257-322">In this example, the light blue base color contrasts with backgrounds with large differences in hue, saturation, or luminosity.</span></span>

    -   <span data-ttu-id="81257-323">使用白色或非常淺的背景，可讓對比前景色彩更容易區別。</span><span class="sxs-lookup"><span data-stu-id="81257-323">Using a white or very light background makes contrasting foreground colors easier to distinguish.</span></span>

        ![<span data-ttu-id="81257-324">說明良好且不良對比度的圖</span><span class="sxs-lookup"><span data-stu-id="81257-324">figure illustrating good and poor contrast</span></span> ](images/vis-color-image16.png)

        <span data-ttu-id="81257-325">在此範例中，白色和淺色背景色彩讓前景色彩更容易區分。</span><span class="sxs-lookup"><span data-stu-id="81257-325">In this example, white and light background colors make the foreground color easier to distinguish.</span></span>

-   <span data-ttu-id="81257-326">**允許使用者自訂這些色彩指派** ，因為色彩選擇是主觀和個人喜好設定。</span><span class="sxs-lookup"><span data-stu-id="81257-326">**Allow users to customize these color assignments** because color choice is subjective and a personal preference.</span></span> <span data-ttu-id="81257-327">如果有許多協調色彩，可讓使用者使用色彩配置將它們變更為群組。</span><span class="sxs-lookup"><span data-stu-id="81257-327">If there are many coordinated colors, allow users to change them as a group using color schemes.</span></span>
-   <span data-ttu-id="81257-328">**允許使用者標記這些色彩指派。**</span><span class="sxs-lookup"><span data-stu-id="81257-328">**Allow users to label these color assignments.**</span></span> <span data-ttu-id="81257-329">這麼做可讓您更輕鬆地識別和尋找。</span><span class="sxs-lookup"><span data-stu-id="81257-329">Doing so helps make them easier to identify and find.</span></span>
-   <span data-ttu-id="81257-330">**不同于 UI 色彩，當系統色彩變更時，資料不應該變更。**</span><span class="sxs-lookup"><span data-stu-id="81257-330">**Unlike UI colors, data should not change when the system colors change.**</span></span>

## <a name="documentation"></a><span data-ttu-id="81257-331">文件</span><span class="sxs-lookup"><span data-stu-id="81257-331">Documentation</span></span>

-   <span data-ttu-id="81257-332">**依名稱（而不是依其色彩）參考 UI 元素。**</span><span class="sxs-lookup"><span data-stu-id="81257-332">**Refer to UI elements by their names, not by their colors.**</span></span> <span data-ttu-id="81257-333">這類參考無法存取，而且系統色彩可能會變更。</span><span class="sxs-lookup"><span data-stu-id="81257-333">Such references aren't accessible and the system colors may change.</span></span> <span data-ttu-id="81257-334">如果 UI 元素的名稱不知名或沒有足夠的描述性，請顯示要說明的螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="81257-334">If a UI element's name isn't well known or not descriptive enough, show a screenshot to clarify.</span></span>

<span data-ttu-id="81257-335">**正確：**</span><span class="sxs-lookup"><span data-stu-id="81257-335">**Correct:**</span></span>

![<span data-ttu-id="81257-336">包含資訊列之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="81257-336">screen shot of message containing information bar</span></span> ](images/vis-color-image17.png)

<span data-ttu-id="81257-337">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="81257-337">**Incorrect:**</span></span>

![<span data-ttu-id="81257-338">包含「金色橫條圖」之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="81257-338">screen shot of message containing 'gold bar'</span></span> ](images/vis-color-image18.png)

<span data-ttu-id="81257-339">在不正確的範例中，訊息會依其色彩（而不是其名稱）參考 Windows Internet Explorer 資訊列。</span><span class="sxs-lookup"><span data-stu-id="81257-339">In the incorrect example, the message refers to the Windows Internet Explorer information bar by its color instead of its name.</span></span>

