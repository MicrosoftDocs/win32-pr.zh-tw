---
title: 簡易藝術範例
description: 簡易藝術範例
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Windows Media Player 的外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 面板的美工圖案，範例
- Windows Media Player 的外觀範例
- 外觀，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672872"
---
# <a name="simple-art-example"></a><span data-ttu-id="d74d1-109">簡易藝術範例</span><span class="sxs-lookup"><span data-stu-id="d74d1-109">Simple Art Example</span></span>

<span data-ttu-id="d74d1-110">建立具有兩個按鈕的簡單面板時需要三個藝術檔案。</span><span class="sxs-lookup"><span data-stu-id="d74d1-110">Three art files are needed to create a simple skin with two buttons.</span></span> <span data-ttu-id="d74d1-111">需要主要映射和對應影像，而替代映射則提供視覺提示給使用者，讓使用者可以按一下按鈕。</span><span class="sxs-lookup"><span data-stu-id="d74d1-111">A primary image and a mapping image are required, and an alternate image provides a visual cue to the user that a button is clickable.</span></span>

<span data-ttu-id="d74d1-112">這些美工檔案是在使用圖層的尖端程式中所建立。</span><span class="sxs-lookup"><span data-stu-id="d74d1-112">These art files were created in an art program that uses layers.</span></span> <span data-ttu-id="d74d1-113">使用圖層可讓您更輕鬆地確保主要、對應和替代影像的大小都相同，並且彼此對齊。</span><span class="sxs-lookup"><span data-stu-id="d74d1-113">Using layers makes it easier to make sure that your primary, mapping, and alternate images are all the same size and line up with each other.</span></span>

<span data-ttu-id="d74d1-114">有關建立藝術的詳細指示，請見面板 [建立指南](skin-creation-guide.md)。</span><span class="sxs-lookup"><span data-stu-id="d74d1-114">The detailed instructions on creating the art are in the [Skin Creation Guide](skin-creation-guide.md).</span></span>

## <a name="primary-image"></a><span data-ttu-id="d74d1-115">主要映像</span><span class="sxs-lookup"><span data-stu-id="d74d1-115">Primary Image</span></span>

<span data-ttu-id="d74d1-116">主要影像是具有兩個按鈕的簡單黃色橢圓，Windows Media Player 的粉紅色和紫色按鈕來停止。</span><span class="sxs-lookup"><span data-stu-id="d74d1-116">The primary image is a simple yellow oval with two buttons, a pink one to start Windows Media Player and purple button to stop it.</span></span> <span data-ttu-id="d74d1-117">背景是稍微比橢圓稍微深一點的黃色。</span><span class="sxs-lookup"><span data-stu-id="d74d1-117">The background is a slightly darker yellow than the oval.</span></span> <span data-ttu-id="d74d1-118">下圖顯示此影像。</span><span class="sxs-lookup"><span data-stu-id="d74d1-118">This image is shown in the following illustration.</span></span>

![主要映射](images/absam01b.png)

<span data-ttu-id="d74d1-120">主要映射來自下列映射，每個映射位於不同的圖層。</span><span class="sxs-lookup"><span data-stu-id="d74d1-120">The primary image was from the following images, each in a separate layer.</span></span> <span data-ttu-id="d74d1-121">第一個橢圓形是使用圖層斜面和浮凸效果所建立。</span><span class="sxs-lookup"><span data-stu-id="d74d1-121">First an oval was created with a layer bevel and emboss effect.</span></span> <span data-ttu-id="d74d1-122">下圖顯示此影像。</span><span class="sxs-lookup"><span data-stu-id="d74d1-122">This image is shown in the following illustration.</span></span>

![oval 影像](images/absam01s.png)

<span data-ttu-id="d74d1-124">接著會建立兩個按鈕，以及圖層斜面和浮凸效果。</span><span class="sxs-lookup"><span data-stu-id="d74d1-124">Then the two buttons were created, also with layer bevel and emboss effects.</span></span> <span data-ttu-id="d74d1-125">這會顯示在下圖中。</span><span class="sxs-lookup"><span data-stu-id="d74d1-125">This is shown in the following illustration.</span></span>

![兩個按鈕](images/absam01p.png)

<span data-ttu-id="d74d1-127">接下來會建立影像背景。</span><span class="sxs-lookup"><span data-stu-id="d74d1-127">Next the image background was created.</span></span> <span data-ttu-id="d74d1-128">選擇稍微較深的黃色，如此就不會注意到橢圓和背景之間的任何消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="d74d1-128">A slightly darker yellow was chosen so that any anti-aliasing between the oval and the background will not be noticed.</span></span> <span data-ttu-id="d74d1-129">色彩值為 \# CCCC00。</span><span class="sxs-lookup"><span data-stu-id="d74d1-129">The color value is \#CCCC00.</span></span> <span data-ttu-id="d74d1-130">下圖顯示此影像。</span><span class="sxs-lookup"><span data-stu-id="d74d1-130">This image is shown in the following illustration.</span></span>

![背景影像](images/absam01y.png)

<span data-ttu-id="d74d1-132">包含這些影像的圖層會顯示出來，並儲存為點陣圖格式的複本，以建立主要映射。</span><span class="sxs-lookup"><span data-stu-id="d74d1-132">The layers that contained these images were made visible and saved as a copy in bitmap format, creating the primary image.</span></span> <span data-ttu-id="d74d1-133">**VIEW** 元素的 **backgroundImage** 屬性將使用主要複合影像。</span><span class="sxs-lookup"><span data-stu-id="d74d1-133">The primary composite image will be used by the **backgroundImage** attribute of the **VIEW** element.</span></span>

## <a name="mapping-image"></a><span data-ttu-id="d74d1-134">對應影像</span><span class="sxs-lookup"><span data-stu-id="d74d1-134">Mapping Image</span></span>

<span data-ttu-id="d74d1-135">需要有對應影像，以指定按一下面板的時機和位置。</span><span class="sxs-lookup"><span data-stu-id="d74d1-135">A mapping image is needed to specify when and where a skin is clicked.</span></span> <span data-ttu-id="d74d1-136">使用紅色區域和綠色區域建立地圖影像。</span><span class="sxs-lookup"><span data-stu-id="d74d1-136">A mapping image was created with a red area and a green area.</span></span> <span data-ttu-id="d74d1-137">下圖顯示此影像。</span><span class="sxs-lookup"><span data-stu-id="d74d1-137">This image is shown in the following illustration.</span></span>

![對應影像](images/absam01m.png)

<span data-ttu-id="d74d1-139">綠色區域將用來識別面板上將開始 Windows Media Player 的區域，而紅色區域將用來停止。</span><span class="sxs-lookup"><span data-stu-id="d74d1-139">The green area will be used to identify the area on the skin that will start Windows Media Player and the red area will be used to stop it.</span></span> <span data-ttu-id="d74d1-140">對應影像的大小與主要映射相同。</span><span class="sxs-lookup"><span data-stu-id="d74d1-140">The mapping image is the same size as the primary image.</span></span>

<span data-ttu-id="d74d1-141">地圖影像的建立方式是將按鈕圖層複製到新圖層，並關閉斜面和浮凸效果。</span><span class="sxs-lookup"><span data-stu-id="d74d1-141">The mapping image was created by copying the button layer to a new layer and turning off the bevel and emboss effect.</span></span> <span data-ttu-id="d74d1-142">對應需要平面影像，因為 Windows Media Player 會在每個區域中尋找單一色彩值。</span><span class="sxs-lookup"><span data-stu-id="d74d1-142">Flat images are needed for mapping because Windows Media Player will be looking for single color values in each area.</span></span> <span data-ttu-id="d74d1-143">它只能搜尋您所定義的色彩，例如 (\# FF0000) 的紅色。</span><span class="sxs-lookup"><span data-stu-id="d74d1-143">It can only search for a color you define, such as red (\#FF0000).</span></span> <span data-ttu-id="d74d1-144">如果您的影像具有斜面或其他效果，則並非全部都是您所需的完全紅色。</span><span class="sxs-lookup"><span data-stu-id="d74d1-144">If your image has a bevel or other effect, not all of it will be the exact red you need.</span></span>

<span data-ttu-id="d74d1-145">為了讓對應按鈕具有簡單的色彩，影像以純紅色和純綠填滿，但可以使用任何色彩。</span><span class="sxs-lookup"><span data-stu-id="d74d1-145">To make the mapping buttons an easy color to remember, the images were filled with pure red and pure green, but any color can be used.</span></span> <span data-ttu-id="d74d1-146">您必須記住地圖中的色彩，以便可以在 XML 面板定義檔中輸入這些數位。</span><span class="sxs-lookup"><span data-stu-id="d74d1-146">You will need to remember the color numbers in your map so that they can be entered in the XML skin definition file.</span></span> <span data-ttu-id="d74d1-147">在此情況下，紅色為 \# FF0000，綠色為 \# 00FF00。</span><span class="sxs-lookup"><span data-stu-id="d74d1-147">In this case, red is \#FF0000 and green is \#00FF00.</span></span>

<span data-ttu-id="d74d1-148">然後，只要顯示新的圖層，影像就會儲存為 BMP 檔案的副本。</span><span class="sxs-lookup"><span data-stu-id="d74d1-148">Then, with only the new layer visible, the image was saved as a copy to a BMP file.</span></span> <span data-ttu-id="d74d1-149">它會由 **BUTTONGROUP** 元素的 **mappingImage** 屬性呼叫。</span><span class="sxs-lookup"><span data-stu-id="d74d1-149">It will be called by the **mappingImage** attribute of the **BUTTONGROUP** element.</span></span>

## <a name="alternate-image"></a><span data-ttu-id="d74d1-150">替代映射</span><span class="sxs-lookup"><span data-stu-id="d74d1-150">Alternate Image</span></span>

<span data-ttu-id="d74d1-151">不需要替代的映射，但對使用者提供視覺提示非常有用。</span><span class="sxs-lookup"><span data-stu-id="d74d1-151">Alternate images are not required but are very useful to give visual cues to the user.</span></span> <span data-ttu-id="d74d1-152">在此情況下，建議使用暫留影像，讓使用者知道可以按一下的區域。</span><span class="sxs-lookup"><span data-stu-id="d74d1-152">In this case, a hover image is recommended so that the user knows what areas can be clicked on.</span></span>

<span data-ttu-id="d74d1-153">以兩個黃色按鈕建立替代映射。</span><span class="sxs-lookup"><span data-stu-id="d74d1-153">An alternate image was created with two yellow buttons.</span></span> <span data-ttu-id="d74d1-154">這會顯示在下圖中。</span><span class="sxs-lookup"><span data-stu-id="d74d1-154">This is shown in the following illustration.</span></span>

![停留影像](images/absam01h.png)

<span data-ttu-id="d74d1-156">建立替代影像的方式是將原始按鈕圖層複製到新圖層，然後將填滿色彩變更為黃色。</span><span class="sxs-lookup"><span data-stu-id="d74d1-156">The alternate image was created by copying the original button layer to a new layer and then changing the fill color to yellow.</span></span> <span data-ttu-id="d74d1-157">已保留斜面和浮凸效果。</span><span class="sxs-lookup"><span data-stu-id="d74d1-157">The bevel and emboss effect was kept.</span></span> <span data-ttu-id="d74d1-158">接著會建立新的圖層並新增影像：箭號表示「播放」，而正方形表示「停止」。</span><span class="sxs-lookup"><span data-stu-id="d74d1-158">Then a new layer was created and images were added: the arrow indicates "play" and the square indicates "stop".</span></span> <span data-ttu-id="d74d1-159">然後，只要顯示新的黃色按鈕並輸入圖層，影像就會儲存為點陣圖檔案的副本。</span><span class="sxs-lookup"><span data-stu-id="d74d1-159">Then, with only the new yellow button and type layers visible, the image was saved as a copy to a bitmap file.</span></span>

<span data-ttu-id="d74d1-160">結果就是當滑鼠停留在地圖影像所定義的區域上方時，將會顯示暫留影像，並在讀者按一下該位置時發出警示，提醒讀者，他們可以播放或停止 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="d74d1-160">The result is that when the mouse hovers over an area defined by the mapping image, the hover image will be displayed, alerting the reader that if they click on that spot, they can play or stop Windows Media Player.</span></span>

## <a name="final-image"></a><span data-ttu-id="d74d1-161">最終影像</span><span class="sxs-lookup"><span data-stu-id="d74d1-161">Final Image</span></span>

<span data-ttu-id="d74d1-162">以下是外觀的最終影像。</span><span class="sxs-lookup"><span data-stu-id="d74d1-162">Here is the final image of the skin.</span></span>

![最終影像](images/absam01f.png)

<span data-ttu-id="d74d1-164">如果您將滑鼠停留在右邊的粉紅色按鈕上方，就會看到這種影像。</span><span class="sxs-lookup"><span data-stu-id="d74d1-164">And this is the image you will see if you hover over the pink button on the right.</span></span>

![將滑鼠停留在右方按鈕上](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a><span data-ttu-id="d74d1-166">藝術範例的 XML 程式碼</span><span class="sxs-lookup"><span data-stu-id="d74d1-166">XML Code for the Art Example</span></span>

<span data-ttu-id="d74d1-167">如需如何撰寫 XML 程式碼的詳細資料，請參閱面板 [建立指南](skin-creation-guide.md)，但為了顯示建立工作面板所需的程式碼，以下是此範例中的插圖程式碼。</span><span class="sxs-lookup"><span data-stu-id="d74d1-167">The details of how to write XML code are given in the [Skin Creation Guide](skin-creation-guide.md), but to show how little code is needed to create a working skin, here is the code for the artwork in this example.</span></span>

<span data-ttu-id="d74d1-168">預先定義的按鈕用於播放和停止功能。</span><span class="sxs-lookup"><span data-stu-id="d74d1-168">Predefined buttons are used for the play and stop functions.</span></span> <span data-ttu-id="d74d1-169">您必須從 Windows Media 錨點載入檔案或播放清單。</span><span class="sxs-lookup"><span data-stu-id="d74d1-169">You must load a file or playlist from the Windows Media anchor.</span></span> <span data-ttu-id="d74d1-170">當 Windows Media Player 變更為面板模式時，螢幕右下角會出現一個小方塊。</span><span class="sxs-lookup"><span data-stu-id="d74d1-170">When Windows Media Player changes to skin mode, a small box appears in the lower-right corner of the screen.</span></span> <span data-ttu-id="d74d1-171">此方塊稱為「錨點」。</span><span class="sxs-lookup"><span data-stu-id="d74d1-171">This box is called the "anchor".</span></span> <span data-ttu-id="d74d1-172">按一下錨點可提供您所需的最小功能，以防面板無法返回 Windows Media Player 的完整模式。</span><span class="sxs-lookup"><span data-stu-id="d74d1-172">Clicking the anchor gives you the minimum functionality needed, in case a skin does not provide a way to return to the full mode of Windows Media Player.</span></span> <span data-ttu-id="d74d1-173">使用者可以使用 [ **View** ] 功能表（如果處於完整模式），或是在面板模式下按一下錨點來切換模式。</span><span class="sxs-lookup"><span data-stu-id="d74d1-173">The user can switch between modes by using the **View** menu if in full mode, or by clicking the anchor if in skin mode.</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a><span data-ttu-id="d74d1-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="d74d1-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d74d1-175">**美工檔案**</span><span class="sxs-lookup"><span data-stu-id="d74d1-175">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




