---
title: 建立主要藝術檔
description: 建立主要藝術檔
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- 建立外觀、主要藝術檔案
- Windows Media Player 的外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 面板的美工圖案、主要影像
- Windows Media Player 的外觀、主要映射
- 外觀，主要影像
- 外觀中的主要影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104553901"
---
# <a name="creating-the-primary-art-file"></a><span data-ttu-id="dc0be-111">建立主要藝術檔</span><span class="sxs-lookup"><span data-stu-id="dc0be-111">Creating the Primary Art File</span></span>

<span data-ttu-id="dc0be-112">主要藝術檔案將包含您的面板使用者先看到的藝術。</span><span class="sxs-lookup"><span data-stu-id="dc0be-112">The primary art file will contain the art that the user of your skin first sees.</span></span> <span data-ttu-id="dc0be-113">在此情況下，您將會在藝術節目的不同層次中建立影像。</span><span class="sxs-lookup"><span data-stu-id="dc0be-113">In this case, you will be creating images in different layers of your art program.</span></span> <span data-ttu-id="dc0be-114">使用圖層的原因是您稍後將複製特定的圖層，以建立對應檔案和替代的美工檔案。</span><span class="sxs-lookup"><span data-stu-id="dc0be-114">The reason for using layers is that you will copy specific layers later to create map files and alternate art files.</span></span>

<span data-ttu-id="dc0be-115">若要建立主要藝術檔案，您將以下列順序建立下列圖層：</span><span class="sxs-lookup"><span data-stu-id="dc0be-115">To create the primary art file, you will create the following layers in the following order:</span></span>

<span data-ttu-id="dc0be-116">外觀背景圖層</span><span class="sxs-lookup"><span data-stu-id="dc0be-116">Skin background layer</span></span>

<span data-ttu-id="dc0be-117">這是顯示面板時，會變成透明的色彩。</span><span class="sxs-lookup"><span data-stu-id="dc0be-117">This is the color that will be transparent when the skin is displayed.</span></span> <span data-ttu-id="dc0be-118">先為此圖層建立圖層，但在您選擇面板容器圖層的色彩之後，請選擇此圖層的最終色彩。</span><span class="sxs-lookup"><span data-stu-id="dc0be-118">Create a layer for this first, but choose the final color of this layer after you chose a color for the skin container layer.</span></span> <span data-ttu-id="dc0be-119">此色彩應該類似于面板容器圖層，但不能隱藏任何消除鋸齒效果。</span><span class="sxs-lookup"><span data-stu-id="dc0be-119">This color should be similar to, but not the same as, the skin container layer, to hide any anti-aliasing effects.</span></span>

<span data-ttu-id="dc0be-120">外觀容器圖層</span><span class="sxs-lookup"><span data-stu-id="dc0be-120">Skin container layer</span></span>

<span data-ttu-id="dc0be-121">這是將構成您面板大綱的影像，而且將會是使用者看到的內容。</span><span class="sxs-lookup"><span data-stu-id="dc0be-121">This is the image that will form the outline of your skin and will be what the user sees.</span></span> <span data-ttu-id="dc0be-122">它也會是此範例中兩個按鈕的容器。</span><span class="sxs-lookup"><span data-stu-id="dc0be-122">It also will be the container for the two buttons in this example.</span></span> <span data-ttu-id="dc0be-123">請將您的外觀視為使用者介面控制項的容器，例如按鈕、滑杆等等。</span><span class="sxs-lookup"><span data-stu-id="dc0be-123">Think of your skin as a container for user interface controls such as buttons, sliders, and so on.</span></span> <span data-ttu-id="dc0be-124">在此範例中，容器是黃色橢圓。</span><span class="sxs-lookup"><span data-stu-id="dc0be-124">In this example, the container is a yellow oval.</span></span>

<span data-ttu-id="dc0be-125">播放和關閉按鈕圖層</span><span class="sxs-lookup"><span data-stu-id="dc0be-125">Play and Close button layers</span></span>

<span data-ttu-id="dc0be-126">以下是此範例所使用的兩個使用者介面控制項。</span><span class="sxs-lookup"><span data-stu-id="dc0be-126">These are the two user interface controls that this example uses.</span></span> <span data-ttu-id="dc0be-127">您會將它們放在不同的層級，以便您可以輕鬆地加以調整或稍後複製。</span><span class="sxs-lookup"><span data-stu-id="dc0be-127">You will put them in separate layers so that you can easily adjust them or copy them later.</span></span>

<span data-ttu-id="dc0be-128">建立圖層之前，您必須先建立將會保存您的圖層的檔案。</span><span class="sxs-lookup"><span data-stu-id="dc0be-128">Before you create your layers, you must create the file that will hold your layers.</span></span> <span data-ttu-id="dc0be-129">啟動 Photoshop 並建立100圖元高和200圖元寬的新檔案。</span><span class="sxs-lookup"><span data-stu-id="dc0be-129">Start up Photoshop and create a new file that is 100 pixels high and 200 pixels wide.</span></span> <span data-ttu-id="dc0be-130">用來建立此範例之藝術的檔案稱為 tiny.psd，並且隨附于 SDK。</span><span class="sxs-lookup"><span data-stu-id="dc0be-130">The file used to create the art for this sample is called tiny.psd and is included with the SDK.</span></span>

<span data-ttu-id="dc0be-131">所有指示都是以 Photoshop 為依據，但只要您可以儲存至 Windows Media Player (BMP、GIF、JPG 和 PNG) 所支援的其中一種檔案格式，就可以使用任何其他藝術程式來建立外觀。</span><span class="sxs-lookup"><span data-stu-id="dc0be-131">All instructions are given in terms of Photoshop, but any other art program can be used to create skins as long as you can save to one of the file formats supported by the Windows Media Player (BMP, GIF, JPG, and PNG).</span></span> <span data-ttu-id="dc0be-132">如果您使用具有圖層（例如 Adobe Photoshop、Jasc 油漆店專業版或 Jedor Viscosity）的藝術節目，就可以更輕鬆地建立外觀。</span><span class="sxs-lookup"><span data-stu-id="dc0be-132">You will find skin creation easier if you use an art program that has layers, such as Adobe Photoshop, Jasc Paint Shop Pro, or Jedor Viscosity.</span></span> <span data-ttu-id="dc0be-133">圖層非常有説明，因為影像對應和替代影像的顯示必須適當地對齊影像。</span><span class="sxs-lookup"><span data-stu-id="dc0be-133">Layers are extremely useful because images must be properly aligned for image mapping and display of alternative images.</span></span>

## <a name="skin-background-layer"></a><span data-ttu-id="dc0be-134">外觀背景圖層</span><span class="sxs-lookup"><span data-stu-id="dc0be-134">Skin Background Layer</span></span>

<span data-ttu-id="dc0be-135">建立新的圖層，並將其命名為「外觀背景」。</span><span class="sxs-lookup"><span data-stu-id="dc0be-135">Create a new layer and name it "Skin background".</span></span> <span data-ttu-id="dc0be-136">這會成為您將在外觀定義檔中定義的透明度色彩。</span><span class="sxs-lookup"><span data-stu-id="dc0be-136">This will become the transparency color you will define in the skin definition file.</span></span> <span data-ttu-id="dc0be-137">等到選取了面板容器的色彩之後，再以特定色彩填滿面板背景圖層。</span><span class="sxs-lookup"><span data-stu-id="dc0be-137">Wait until the color for the skin container is chosen before filling the skin background layer with a specific color.</span></span>

## <a name="skin-container-layer"></a><span data-ttu-id="dc0be-138">外觀容器圖層</span><span class="sxs-lookup"><span data-stu-id="dc0be-138">Skin Container Layer</span></span>

<span data-ttu-id="dc0be-139">接著，建立新的圖層，並將其命名為「外觀容器」。</span><span class="sxs-lookup"><span data-stu-id="dc0be-139">Next create a new layer and call it "Skin container".</span></span> <span data-ttu-id="dc0be-140">這將會定義您面板的邊緣，並將是按鈕的容器。</span><span class="sxs-lookup"><span data-stu-id="dc0be-140">This will define the edges of your skin and will be the container for the buttons.</span></span>

<span data-ttu-id="dc0be-141">使用 Web 色彩滑杆，選擇圖形的前景色彩。</span><span class="sxs-lookup"><span data-stu-id="dc0be-141">Choose a foreground color for the shape, using the Web color sliders.</span></span> <span data-ttu-id="dc0be-142">在此範例中， \# 已選擇 "DBDD11" 色彩。</span><span class="sxs-lookup"><span data-stu-id="dc0be-142">In this example, the color "\#DBDD11" was chosen.</span></span>

<span data-ttu-id="dc0be-143">接下來建立 oval 圖形。</span><span class="sxs-lookup"><span data-stu-id="dc0be-143">Next create an oval shape.</span></span> <span data-ttu-id="dc0be-144">最簡單的方式是使用 Eliptical 天棚工具，並建立 oval 選取專案。</span><span class="sxs-lookup"><span data-stu-id="dc0be-144">The easiest way is to use the Eliptical Marquee tool and create an oval selection.</span></span> <span data-ttu-id="dc0be-145">當您建立了您想要的大小和形狀的 oval 選取專案時，請以前景色彩填滿選取範圍，然後取消選取專案。</span><span class="sxs-lookup"><span data-stu-id="dc0be-145">When you have created an oval selection that is the size and shape you want, fill the selection with the foreground color and cancel the selection.</span></span>

<span data-ttu-id="dc0be-146">最後，為了讓這看起來更有趣，請以預設值套用斜面和浮凸的圖層效果。</span><span class="sxs-lookup"><span data-stu-id="dc0be-146">Finally, to make this look a bit more interesting, apply the layer effect of Bevel and Emboss with the default values.</span></span>

<span data-ttu-id="dc0be-147">您的面板容器圖層看起來應該如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="dc0be-147">Your skin container layer should look like the following illustration.</span></span>

![外觀容器圖層](images/g01cont.png)

## <a name="background-skin-color"></a><span data-ttu-id="dc0be-149">背景外觀色彩</span><span class="sxs-lookup"><span data-stu-id="dc0be-149">Background Skin Color</span></span>

<span data-ttu-id="dc0be-150">現在您已為面板容器圖形選擇前景色彩，您可以為面板背景圖選擇類似的色彩。</span><span class="sxs-lookup"><span data-stu-id="dc0be-150">Now that you have chosen a foreground color for your skin container shape, you can choose a similar color for your skin background layer.</span></span> <span data-ttu-id="dc0be-151">您不想要完全相同的色彩，或您的面板容器也會是透明的。</span><span class="sxs-lookup"><span data-stu-id="dc0be-151">You do not want the exact same color, or your skin container will be transparent also.</span></span> <span data-ttu-id="dc0be-152">事實上，請確定您不會在面板中的任何其他位置（甚至是在相片中）使用此確切色彩，因為在此色彩出現時，桌面影像會改為顯示。</span><span class="sxs-lookup"><span data-stu-id="dc0be-152">In fact, be sure you do not use this exact color anywhere else in your skin, even in photographs, because wherever this color appears, the desktop image will appear instead.</span></span>

<span data-ttu-id="dc0be-153">您想要一個接近外觀容器色彩的色彩，以避免消除鋸齒效果。</span><span class="sxs-lookup"><span data-stu-id="dc0be-153">You want a color close to the skin container color to avoid anti-aliasing effects.</span></span> <span data-ttu-id="dc0be-154">例如，如果您有黑色背景，部分的黑色可能會顯示在您的外觀邊緣周圍。</span><span class="sxs-lookup"><span data-stu-id="dc0be-154">For example, if you have a black background, some bits of black may show up around the edge of your skin.</span></span> <span data-ttu-id="dc0be-155">藉由選擇接近外觀容器色彩的色彩，將不會察覺在消除鋸齒程式中顯示的任何偏離圖元。</span><span class="sxs-lookup"><span data-stu-id="dc0be-155">By choosing a color close to the color of the skin container, any stray pixels that show up in the anti-aliasing process will be unnoticed.</span></span>

<span data-ttu-id="dc0be-156">消除鋸齒是平滑傾斜或曲線圖形邊緣的流程。</span><span class="sxs-lookup"><span data-stu-id="dc0be-156">Anti-aliasing is the process of smoothing the edges of slanted or curved shapes.</span></span> <span data-ttu-id="dc0be-157">消除鋸齒會以圖形邊緣的圖元為單位來建立新的色彩，也就是前景色彩與背景色彩的 blend。</span><span class="sxs-lookup"><span data-stu-id="dc0be-157">Anti-aliasing creates new colors, for pixels along the edges of a shape, that are a blend of the foreground color and the background color.</span></span> <span data-ttu-id="dc0be-158">在背景色彩變成透明的情況時，其中某些色彩可能會遺失圖元。</span><span class="sxs-lookup"><span data-stu-id="dc0be-158">Some of these in-between colors can cause pixels to be missed when the background color is made transparent.</span></span>

<span data-ttu-id="dc0be-159">您的面板背景圖層看起來應該如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="dc0be-159">Your skin background layer should look like the following illustration.</span></span>

![背景外觀圖層](images/g01backg.png)

## <a name="play-and-close-button-layers"></a><span data-ttu-id="dc0be-161">播放和關閉按鈕圖層</span><span class="sxs-lookup"><span data-stu-id="dc0be-161">Play and Close Button Layers</span></span>

<span data-ttu-id="dc0be-162">建立新的圖層，並將其命名為「關閉按鈕」。</span><span class="sxs-lookup"><span data-stu-id="dc0be-162">Create a new layer and name it "Close button".</span></span> <span data-ttu-id="dc0be-163">再次使用 [Eliptical 天棚選取] 工具，建立圓形並將其置於整體影像的左邊。</span><span class="sxs-lookup"><span data-stu-id="dc0be-163">Using the Eliptical Marquee selection tool again, create a circle and position it on the left side of the overall image.</span></span> <span data-ttu-id="dc0be-164">開啟外觀容器檔案的可見度，以協助放置選取專案。</span><span class="sxs-lookup"><span data-stu-id="dc0be-164">Turn on the visibility of the skin container file to help place the selection.</span></span>

<span data-ttu-id="dc0be-165">當您滿意放置時，請使用任何色彩來填滿選取範圍 (除了面板容器的色彩或面板背景) 之外。</span><span class="sxs-lookup"><span data-stu-id="dc0be-165">When you are satisfied with the placement, fill the selection with any color (except the color of the skin container or the skin background).</span></span> <span data-ttu-id="dc0be-166">在此範例中，選擇紫色的色彩。</span><span class="sxs-lookup"><span data-stu-id="dc0be-166">In this example, a purple color was chosen.</span></span> <span data-ttu-id="dc0be-167">您不需要記住色彩的數目。</span><span class="sxs-lookup"><span data-stu-id="dc0be-167">You do not need to remember the number of the color.</span></span> <span data-ttu-id="dc0be-168">然後取消選取專案，並套用另一個預設斜面和浮凸圖層效果。</span><span class="sxs-lookup"><span data-stu-id="dc0be-168">Then cancel the selection and apply another default Bevel and Emboss layer effect.</span></span> <span data-ttu-id="dc0be-169">如果您想要將非圖層效果套用至按鈕，請建立原始的複本以供稍後用於對應。</span><span class="sxs-lookup"><span data-stu-id="dc0be-169">If you want to apply non-layer effects to your button, make a copy of the original for later use in mapping.</span></span>

<span data-ttu-id="dc0be-170">您的 [關閉] 按鈕看起來應該如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="dc0be-170">Your Close button should look like the following illustration.</span></span>

![關閉按鈕](images/g01qbut.png)

<span data-ttu-id="dc0be-172">建立新的圖層，並將其命名為「播放按鈕」。</span><span class="sxs-lookup"><span data-stu-id="dc0be-172">Create a new layer and name it "Play button".</span></span> <span data-ttu-id="dc0be-173">使用您針對 [關閉] 按鈕所做的相同技術，但提供不同的色彩。</span><span class="sxs-lookup"><span data-stu-id="dc0be-173">Use the same techniques you did for the Close button, but give it a different color.</span></span> <span data-ttu-id="dc0be-174">在此情況下，選擇粉紅色按鈕色彩，但只要色彩與面板容器 (的色彩不同，就可以使用任何色彩，因為它會 blend 至容器) 或面板背景色彩 (，因為它會變成透明) 。</span><span class="sxs-lookup"><span data-stu-id="dc0be-174">In this case, a pink button color was chosen, but any color can be used as long as it is not the same color as the skin container (because it would blend into the container) or the skin background color (because it would become transparent).</span></span>

<span data-ttu-id="dc0be-175">您的 [播放] 按鈕看起來應該如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="dc0be-175">Your Play button should look like the following illustration.</span></span>

![[播放] 按鈕](images/g01pbut.png)

## <a name="combine-layers-and-save"></a><span data-ttu-id="dc0be-177">合併圖層並儲存</span><span class="sxs-lookup"><span data-stu-id="dc0be-177">Combine Layers and Save</span></span>

<span data-ttu-id="dc0be-178">您現在已準備好建立主要藝術檔。</span><span class="sxs-lookup"><span data-stu-id="dc0be-178">You are now ready to create the primary art file.</span></span> <span data-ttu-id="dc0be-179">隱藏所有圖層，然後依序顯示下列層級 (從上到下) ：</span><span class="sxs-lookup"><span data-stu-id="dc0be-179">Hide all layers and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="dc0be-180">[播放] 按鈕</span><span class="sxs-lookup"><span data-stu-id="dc0be-180">Play button</span></span>

<span data-ttu-id="dc0be-181">[關閉] 按鈕</span><span class="sxs-lookup"><span data-stu-id="dc0be-181">Close button</span></span>

<span data-ttu-id="dc0be-182">外觀容器</span><span class="sxs-lookup"><span data-stu-id="dc0be-182">Skin container</span></span>

<span data-ttu-id="dc0be-183">外觀背景</span><span class="sxs-lookup"><span data-stu-id="dc0be-183">Skin background</span></span>

<span data-ttu-id="dc0be-184">使用 [檔案] 功能表中的 [儲存複製] 命令，儲存至新的檔案。</span><span class="sxs-lookup"><span data-stu-id="dc0be-184">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="dc0be-185">在 [儲存複本] 對話方塊的 [另存新檔] 對話方塊中，選取 [BMP] 選項，然後輸入您稍後會在面板定義檔中參考的檔案名。</span><span class="sxs-lookup"><span data-stu-id="dc0be-185">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="dc0be-186">在理想的情況下，您應該將它儲存在與面板定義檔案相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="dc0be-186">Ideally you should save this in the same directory as your skin definition file.</span></span> <span data-ttu-id="dc0be-187">例如，您可以呼叫此 background.bmp。</span><span class="sxs-lookup"><span data-stu-id="dc0be-187">For example, you could call this background.bmp.</span></span> <span data-ttu-id="dc0be-188">選擇預設設定，然後儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="dc0be-188">Choose the default settings and save the file.</span></span>

<span data-ttu-id="dc0be-189">您的主要藝術檔案看起來應該像這樣：</span><span class="sxs-lookup"><span data-stu-id="dc0be-189">Your primary art file should look like this:</span></span>

![主要藝術檔](images/g01prime.png)

<span data-ttu-id="dc0be-191">您將使用此檔案名作為面板定義檔中 **VIEW** 元素的 **backgroundImage** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="dc0be-191">You will use this file name as the value for the **backgroundImage** attribute of the **VIEW** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc0be-192">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc0be-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc0be-193">**建立您的第一個外觀**</span><span class="sxs-lookup"><span data-stu-id="dc0be-193">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




