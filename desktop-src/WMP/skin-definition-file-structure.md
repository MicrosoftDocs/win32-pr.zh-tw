---
title: 外觀定義檔案結構
description: 外觀定義檔案結構
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- 面板定義檔 Windows Media Player 的外觀
- 外觀、面板定義檔
- 面板的檔案、外觀定義
- 外觀定義檔，結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021715"
---
# <a name="skin-definition-file-structure"></a><span data-ttu-id="72cb7-107">外觀定義檔案結構</span><span class="sxs-lookup"><span data-stu-id="72cb7-107">Skin Definition File Structure</span></span>

<span data-ttu-id="72cb7-108">外觀定義檔必須遵循特定的結構。</span><span class="sxs-lookup"><span data-stu-id="72cb7-108">The skin definition file must follow a specific structure.</span></span> <span data-ttu-id="72cb7-109">您可以從 **主題** 專案開始，建立一個或多個 **view** 元素，然後使用適合您要使用之檢視類型的使用者介面元素，來定義每個 **view** 元素。</span><span class="sxs-lookup"><span data-stu-id="72cb7-109">You start with a **THEME** element, create one or more **VIEW** elements, and then define each **VIEW** element with the user interface elements appropriate for the type of view you want to use.</span></span>

## <a name="theme-elements"></a><span data-ttu-id="72cb7-110">主題元素</span><span class="sxs-lookup"><span data-stu-id="72cb7-110">THEME Elements</span></span>

<span data-ttu-id="72cb7-111">在最上層，您必須以 **主題** 元素啟動面板定義檔，並將其關閉。</span><span class="sxs-lookup"><span data-stu-id="72cb7-111">At the top level, you must start the skin definition file with the **THEME** element and close with it.</span></span>


```C++
<THEME>
    ...
</THEME>

```



<span data-ttu-id="72cb7-112">**主題** 元素是面板的根項目。</span><span class="sxs-lookup"><span data-stu-id="72cb7-112">The **THEME** element is the root element for your skin.</span></span> <span data-ttu-id="72cb7-113">面板定義檔中只能有一個 **主題** 元素，而且它必須位於最上層。</span><span class="sxs-lookup"><span data-stu-id="72cb7-113">There can be only one **THEME** element in a skin definition file, and it must be at the top level.</span></span> <span data-ttu-id="72cb7-114">**主題** 元素有特定和環境屬性，不過大部分的情況下，您不需要使用它們。</span><span class="sxs-lookup"><span data-stu-id="72cb7-114">**THEME** elements have specific and ambient attributes, though most of the time you will not need to use them.</span></span> <span data-ttu-id="72cb7-115">如需這些屬性的詳細資訊，請參閱 [外觀程式設計參考](skin-programming-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="72cb7-115">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="view-elements"></a><span data-ttu-id="72cb7-116">VIEW 元素</span><span class="sxs-lookup"><span data-stu-id="72cb7-116">VIEW Elements</span></span>

<span data-ttu-id="72cb7-117">每個 **主題** 都必須至少有一個 **VIEW** 元素。</span><span class="sxs-lookup"><span data-stu-id="72cb7-117">Each **THEME** must have at least one **VIEW** element.</span></span> <span data-ttu-id="72cb7-118">**VIEW** 元素會控制您在螢幕上看到的特定影像。</span><span class="sxs-lookup"><span data-stu-id="72cb7-118">The **VIEW** element governs the particular image you see on the screen.</span></span> <span data-ttu-id="72cb7-119">您可能會想要有一個以上的視圖，讓您可以來回切換。</span><span class="sxs-lookup"><span data-stu-id="72cb7-119">You may want to have more than one view, so you can switch back and forth.</span></span> <span data-ttu-id="72cb7-120">例如，您可能想要有很大的觀點來使用播放清單、觀看視覺效果的中型視圖，以及適合螢幕角落的小視野。</span><span class="sxs-lookup"><span data-stu-id="72cb7-120">For example, you might want to have a large view for working with playlists, a medium view for watching visualizations, and a tiny view that fits in a corner of the screen.</span></span>

<span data-ttu-id="72cb7-121">如果您要建立多個視圖，您會想要確定每個視圖都具有唯一的 **識別碼** 屬性值，以用來識別此視圖。</span><span class="sxs-lookup"><span data-stu-id="72cb7-121">If you are creating multiple views, you will want to make sure that each view has a unique **ID** attribute value that will be used to identify the view.</span></span> <span data-ttu-id="72cb7-122">您必須定義 **backgroundImage** 屬性，否則您的視圖將不會有起始影像。</span><span class="sxs-lookup"><span data-stu-id="72cb7-122">You must define the **backgroundImage** attribute or your view will have no starting image.</span></span> <span data-ttu-id="72cb7-123">如果您不想要顯示矩形影像，您可能會想要使用 **clippingColor** 屬性來定義不會顯示的面板區域，而且您可能會想要設定 **VIEW** 元素的 **標題列** 屬性。</span><span class="sxs-lookup"><span data-stu-id="72cb7-123">If you do not want to display a rectangular image, you will probably want to use the **clippingColor** attribute to define the areas of your skin that will not display, and you will probably want to set the **titleBar** attribute of the **VIEW** element.</span></span>

<span data-ttu-id="72cb7-124">每一個 **VIEW** 專案也可以有一或 **多個子視圖元素** 。</span><span class="sxs-lookup"><span data-stu-id="72cb7-124">Each **VIEW** element can also have one or more **SUBVIEW** elements.</span></span> <span data-ttu-id="72cb7-125">子 **視圖元素類似** 于 **視圖** ，可用於您想要四處移動、隱藏或顯示的部分面板。</span><span class="sxs-lookup"><span data-stu-id="72cb7-125">A **SUBVIEW** element is similar to a **VIEW** and can be used for parts of your skin that you want to move around, hide, or show.</span></span> <span data-ttu-id="72cb7-126">例如，子 **視圖** 元素可用來建立滑出面板的滑動紙匣，以顯示圖形等化器。</span><span class="sxs-lookup"><span data-stu-id="72cb7-126">For example, a **SUBVIEW** element might be used to create a sliding tray that pops out of your skin to display a graphic equalizer.</span></span> <span data-ttu-id="72cb7-127">子 **視圖專案** 可以與 **視圖** 對齊，並與該 **視圖** 具有其他特殊關聯性。</span><span class="sxs-lookup"><span data-stu-id="72cb7-127">**SUBVIEW** elements can be aligned with the **VIEW** and have other special relationships to the **VIEW**.</span></span>

## <a name="initializing-windows-media-player"></a><span data-ttu-id="72cb7-128">正在初始化 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="72cb7-128">Initializing Windows Media Player</span></span>

<span data-ttu-id="72cb7-129">您可以使用 [ **播放** 程式]、[ **設定**] 和 [ **控制項** ] 元素，設定 Windows Media Player 的特定初始屬性。</span><span class="sxs-lookup"><span data-stu-id="72cb7-129">You can set certain initial properties of Windows Media Player by using the **PLAYER**, **SETTINGS**, and **CONTROLS** elements.</span></span> <span data-ttu-id="72cb7-130">例如，您可以將磁片區設定為初始層級，或指定檔案名的預設值。</span><span class="sxs-lookup"><span data-stu-id="72cb7-130">For example, you could set the volume to an initial level or give a default value for a file name.</span></span>

<span data-ttu-id="72cb7-131">下列程式碼顯示如何在面板中設定 **URL** 值：</span><span class="sxs-lookup"><span data-stu-id="72cb7-131">The following code shows how to set the **URL** value in a skin:</span></span>


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



<span data-ttu-id="72cb7-132">如果您想要將 [**設定**] 的 [**自動啟動**] 屬性設定為 False，您可以使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="72cb7-132">If you wanted to set the **autoStart** attribute of **SETTINGS** to False, you would use the following code:</span></span>


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



<span data-ttu-id="72cb7-133">請注意， **SETTINGS** 元素是在 **PLAYER** 專案內進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="72cb7-133">Note that the **SETTINGS** element is nested inside the **PLAYER** element.</span></span>

<span data-ttu-id="72cb7-134">您可以使用這些元素，在設計階段指定下列屬性和事件：</span><span class="sxs-lookup"><span data-stu-id="72cb7-134">Using these elements, the following attributes and events can be specified at design time:</span></span>

<span data-ttu-id="72cb7-135">**PLAYER 元素屬性**</span><span class="sxs-lookup"><span data-stu-id="72cb7-135">**PLAYER Element Attributes**</span></span>

-   <span data-ttu-id="72cb7-136">**url**</span><span class="sxs-lookup"><span data-stu-id="72cb7-136">**url**</span></span>
-   <span data-ttu-id="72cb7-137">**緩衝處理**</span><span class="sxs-lookup"><span data-stu-id="72cb7-137">**Buffering**</span></span>
-   <span data-ttu-id="72cb7-138">**Currentitemchange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-138">**Currentitemchange**</span></span>
-   <span data-ttu-id="72cb7-139">**Currentplaylistchange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-139">**Currentplaylistchange**</span></span>
-   <span data-ttu-id="72cb7-140">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="72cb7-140">**Error**</span></span>
-   <span data-ttu-id="72cb7-141">**Markerhit**</span><span class="sxs-lookup"><span data-stu-id="72cb7-141">**Markerhit**</span></span>
-   <span data-ttu-id="72cb7-142">**Mediachange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-142">**Mediachange**</span></span>
-   <span data-ttu-id="72cb7-143">**Mediacollectionchange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-143">**Mediacollectionchange**</span></span>
-   <span data-ttu-id="72cb7-144">**Modechange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-144">**Modechange**</span></span>
-   <span data-ttu-id="72cb7-145">**Mpenstatechange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-145">**Mpenstatechange**</span></span>
-   <span data-ttu-id="72cb7-146">**Mlaylistchange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-146">**Mlaylistchange**</span></span>
-   <span data-ttu-id="72cb7-147">**Mlaystatechange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-147">**Mlaystatechange**</span></span>
-   <span data-ttu-id="72cb7-148">**Mositionchange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-148">**Mositionchange**</span></span>
-   <span data-ttu-id="72cb7-149">**Mcriptcommand**</span><span class="sxs-lookup"><span data-stu-id="72cb7-149">**Mcriptcommand**</span></span>
-   <span data-ttu-id="72cb7-150">**Mtatuschange**</span><span class="sxs-lookup"><span data-stu-id="72cb7-150">**Mtatuschange**</span></span>

<span data-ttu-id="72cb7-151">**SETTINGS 元素屬性**</span><span class="sxs-lookup"><span data-stu-id="72cb7-151">**SETTINGS Element Attributes**</span></span>

-   <span data-ttu-id="72cb7-152">**啟動**</span><span class="sxs-lookup"><span data-stu-id="72cb7-152">**autoStart**</span></span>
-   <span data-ttu-id="72cb7-153">**平衡**</span><span class="sxs-lookup"><span data-stu-id="72cb7-153">**balance**</span></span>
-   <span data-ttu-id="72cb7-154">**baseURL**</span><span class="sxs-lookup"><span data-stu-id="72cb7-154">**baseURL**</span></span>
-   <span data-ttu-id="72cb7-155">**defaultFrame**</span><span class="sxs-lookup"><span data-stu-id="72cb7-155">**defaultFrame**</span></span>
-   <span data-ttu-id="72cb7-156">**enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="72cb7-156">**enableErrorDialogs**</span></span>
-   <span data-ttu-id="72cb7-157">**invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="72cb7-157">**invokeURLs**</span></span>
-   <span data-ttu-id="72cb7-158">**靜音**</span><span class="sxs-lookup"><span data-stu-id="72cb7-158">**mute**</span></span>
-   <span data-ttu-id="72cb7-159">**playCount**</span><span class="sxs-lookup"><span data-stu-id="72cb7-159">**playCount**</span></span>
-   <span data-ttu-id="72cb7-160">**率**</span><span class="sxs-lookup"><span data-stu-id="72cb7-160">**rate**</span></span>
-   <span data-ttu-id="72cb7-161">**體積**</span><span class="sxs-lookup"><span data-stu-id="72cb7-161">**volume**</span></span>

## <a name="controls-element-attributes"></a><span data-ttu-id="72cb7-162">CONTROLS 元素屬性</span><span class="sxs-lookup"><span data-stu-id="72cb7-162">CONTROLS Element Attributes</span></span>

-   <span data-ttu-id="72cb7-163">**currentMarker**</span><span class="sxs-lookup"><span data-stu-id="72cb7-163">**currentMarker**</span></span>
-   <span data-ttu-id="72cb7-164">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="72cb7-164">**currentPosition**</span></span>

## <a name="other-user-interface-elements"></a><span data-ttu-id="72cb7-165">其他消費者介面元素</span><span class="sxs-lookup"><span data-stu-id="72cb7-165">Other User Interface Elements</span></span>

<span data-ttu-id="72cb7-166">一旦定義您的 **主題** 和 **VIEW** 專案之後，您必須使用特定的使用者介面元素來填入您的 **視圖** 。</span><span class="sxs-lookup"><span data-stu-id="72cb7-166">Once you have defined your **THEME** and **VIEW** elements, you must populate your **VIEW** with specific user interface elements.</span></span> <span data-ttu-id="72cb7-167">您不需要在面板中使用所有可用的專案，只是您需要的專案。</span><span class="sxs-lookup"><span data-stu-id="72cb7-167">You do not have to use all the available elements in a skin, just the ones you need.</span></span>

<span data-ttu-id="72cb7-168">如果使用者可以看到某個元素，則會呼叫控制項。</span><span class="sxs-lookup"><span data-stu-id="72cb7-168">If an element can be seen by the user, it is called a control.</span></span> <span data-ttu-id="72cb7-169">下列控制項適用于下列的外觀：</span><span class="sxs-lookup"><span data-stu-id="72cb7-169">The following controls are available for skins:</span></span>

-   <span data-ttu-id="72cb7-170">按鈕</span><span class="sxs-lookup"><span data-stu-id="72cb7-170">Buttons</span></span>
-   <span data-ttu-id="72cb7-171">滑杆、自訂滑杆和進度列</span><span class="sxs-lookup"><span data-stu-id="72cb7-171">Sliders, custom sliders, and progress bars</span></span>
-   <span data-ttu-id="72cb7-172">文字方塊</span><span class="sxs-lookup"><span data-stu-id="72cb7-172">Text boxes</span></span>
-   <span data-ttu-id="72cb7-173">影片視窗</span><span class="sxs-lookup"><span data-stu-id="72cb7-173">Video windows</span></span>
-   <span data-ttu-id="72cb7-174">視覺效果視窗</span><span class="sxs-lookup"><span data-stu-id="72cb7-174">Visualization windows</span></span>
-   <span data-ttu-id="72cb7-175">播放清單視窗</span><span class="sxs-lookup"><span data-stu-id="72cb7-175">Playlist windows</span></span>
-   <span data-ttu-id="72cb7-176">子視圖視窗</span><span class="sxs-lookup"><span data-stu-id="72cb7-176">Subview windows</span></span>

<span data-ttu-id="72cb7-177">此外，您還可以使用數個元素來進一步定義 Windows Media Player 動作，但它們需要視覺元素，例如按鈕或滑杆：</span><span class="sxs-lookup"><span data-stu-id="72cb7-177">In addition, several elements can be used to further define Windows Media Player actions, but they require visual elements such as buttons or sliders:</span></span>

-   <span data-ttu-id="72cb7-178">影片設定</span><span class="sxs-lookup"><span data-stu-id="72cb7-178">Video settings</span></span>
-   <span data-ttu-id="72cb7-179">等化器設定</span><span class="sxs-lookup"><span data-stu-id="72cb7-179">Equalizer Settings</span></span>
-   <span data-ttu-id="72cb7-180">視覺效果設定</span><span class="sxs-lookup"><span data-stu-id="72cb7-180">Visualization settings</span></span>

## <a name="buttons"></a><span data-ttu-id="72cb7-181">按鈕</span><span class="sxs-lookup"><span data-stu-id="72cb7-181">Buttons</span></span>

<span data-ttu-id="72cb7-182">按鈕是外觀最受歡迎的部分。</span><span class="sxs-lookup"><span data-stu-id="72cb7-182">Buttons are the most popular part of a skin.</span></span> <span data-ttu-id="72cb7-183">您可以使用按鈕來觸發動作，例如播放、停止、結束、最小化，以及切換至不同的視圖。</span><span class="sxs-lookup"><span data-stu-id="72cb7-183">You can use buttons to trigger actions such as play, stop, quit, minimize, and switch to different view.</span></span> <span data-ttu-id="72cb7-184">Windows Media Player 提供具有兩種按鈕元素的外觀建立者： **button** 元素和 **BUTTONGROUP** 元素。</span><span class="sxs-lookup"><span data-stu-id="72cb7-184">Windows Media Player provides the skin creator with two types of button elements: the **BUTTON** element and the **BUTTONGROUP** element.</span></span> <span data-ttu-id="72cb7-185">此外，還有數個預先定義的按鈕類型。</span><span class="sxs-lookup"><span data-stu-id="72cb7-185">In addition, there are several predefined types of buttons.</span></span>

-   <span data-ttu-id="72cb7-186">**BUTTON 元素。**</span><span class="sxs-lookup"><span data-stu-id="72cb7-186">**BUTTON element.**</span></span> <span data-ttu-id="72cb7-187">**按鈕** 元素用於個別按鈕。</span><span class="sxs-lookup"><span data-stu-id="72cb7-187">The **BUTTON** element is used for individual buttons.</span></span> <span data-ttu-id="72cb7-188">如果您使用 **button** 元素，您必須為每個按鈕提供影像，並定義您希望按鈕顯示在相對於背景影像的確切位置。</span><span class="sxs-lookup"><span data-stu-id="72cb7-188">If you use the **BUTTON** element, you must supply an image for each button and define the exact location where you want the button to appear relative to the background image.</span></span> <span data-ttu-id="72cb7-189">**按鈕** 元素的優點之一，就是您可以動態變更按鈕影像。</span><span class="sxs-lookup"><span data-stu-id="72cb7-189">One of the advantages of the **BUTTON** element is that you can change the button image dynamically.</span></span>
-   <span data-ttu-id="72cb7-190">**BUTTONGROUP 元素。**</span><span class="sxs-lookup"><span data-stu-id="72cb7-190">**BUTTONGROUP element.**</span></span> <span data-ttu-id="72cb7-191">**BUTTONGROUP** 元素用於按鈕群組。</span><span class="sxs-lookup"><span data-stu-id="72cb7-191">The **BUTTONGROUP** element is used for groups of buttons.</span></span> <span data-ttu-id="72cb7-192">事實上，您必須將每個 **BUTTONGROUP** 元素與一對 **BUTTONGROUP** 標記括住。</span><span class="sxs-lookup"><span data-stu-id="72cb7-192">In fact, you must enclose each **BUTTONGROUP** element with a pair of **BUTTONGROUP** tags.</span></span> <span data-ttu-id="72cb7-193">使用按鈕群組比使用個別按鈕更簡單，因為您不需要為每個按鈕指定確切的位置。</span><span class="sxs-lookup"><span data-stu-id="72cb7-193">Using button groups is easier than using individual buttons because you do not have to specify the exact location for each button.</span></span> <span data-ttu-id="72cb7-194">相反地，您會提供個別的影像地圖，以定義當滑鼠停留在背景上或按一下某個區域時將會發生的動作。</span><span class="sxs-lookup"><span data-stu-id="72cb7-194">Instead, you supply a separate image map that defines the actions that will take place when the mouse hovers over or clicks an area on your background.</span></span> <span data-ttu-id="72cb7-195">使用影像地圖很容易，因為您可以將所建立的圖案帶到您的背景，並將其複製到圖形編輯程式中的地圖圖層。</span><span class="sxs-lookup"><span data-stu-id="72cb7-195">Using image maps is easy because you can take the art you created for your background and copy it to a mapping layer in your graphics editing program.</span></span> <span data-ttu-id="72cb7-196">使用您的圖形編輯程式比起嘗試明確定義應在背景上放置個別按鈕的位置更快且更精確。</span><span class="sxs-lookup"><span data-stu-id="72cb7-196">Using your graphics editing program is faster and more precise than trying to define exactly where an individual button should be placed on your background.</span></span>
-   <span data-ttu-id="72cb7-197">**預先定義的按鈕。**</span><span class="sxs-lookup"><span data-stu-id="72cb7-197">**Predefined buttons.**</span></span> <span data-ttu-id="72cb7-198">有幾個預先定義的按鈕。</span><span class="sxs-lookup"><span data-stu-id="72cb7-198">There are several predefined buttons.</span></span> <span data-ttu-id="72cb7-199">例如，您可以使用 [PLAYELEMENT] 按鈕來播放數位媒體檔案，以及使用 STOPELEMENT 來停止播放。</span><span class="sxs-lookup"><span data-stu-id="72cb7-199">For example, you can use a PLAYELEMENT button to play digital media files, and a STOPELEMENT to stop playback.</span></span> <span data-ttu-id="72cb7-200">請參閱面板程式設計參考中的 [BUTTONGROUP](buttongroup-element.md) 元素和 [按鈕](button-element.md) 專案。</span><span class="sxs-lookup"><span data-stu-id="72cb7-200">See [BUTTONGROUP](buttongroup-element.md) Element and [BUTTON Element](button-element.md) in the Skin Programming Reference.</span></span> <span data-ttu-id="72cb7-201">[IMAGEBUTTON](imagebutton.md)可以用來顯示可變更以回應特定事件的影像。</span><span class="sxs-lookup"><span data-stu-id="72cb7-201">The [IMAGEBUTTON](imagebutton.md) can be used to display images that can change in response to specific events.</span></span>

## <a name="sliders"></a><span data-ttu-id="72cb7-202">滑桿</span><span class="sxs-lookup"><span data-stu-id="72cb7-202">Sliders</span></span>

<span data-ttu-id="72cb7-203">滑杆適用于使用隨時間變化的資訊。</span><span class="sxs-lookup"><span data-stu-id="72cb7-203">Sliders are useful for working with information that changes over time.</span></span> <span data-ttu-id="72cb7-204">例如，您可以使用滑杆來指出已針對特定媒體檔案播放的音樂數量。</span><span class="sxs-lookup"><span data-stu-id="72cb7-204">For example, you might use a slider to indicate the amount of music that has already played for a particular media file.</span></span> <span data-ttu-id="72cb7-205">滑杆可以是水準或垂直、線性或圓形，或是您可以想像的任何圖形。</span><span class="sxs-lookup"><span data-stu-id="72cb7-205">Sliders can be horizontal or vertical, linear or circular, or any shape you can think of.</span></span> <span data-ttu-id="72cb7-206">滑杆分為三種：滑杆、進度列和自訂滑杆。</span><span class="sxs-lookup"><span data-stu-id="72cb7-206">Sliders come in three varieties: sliders, progress bars, and custom sliders.</span></span>

-   <span data-ttu-id="72cb7-207">**滑 塊。**</span><span class="sxs-lookup"><span data-stu-id="72cb7-207">**Sliders.**</span></span> <span data-ttu-id="72cb7-208">您可以使用 **滑杆** 元素進行音量控制項，或讓使用者移至媒體內容的不同部分。</span><span class="sxs-lookup"><span data-stu-id="72cb7-208">You can use the **SLIDER** element for volume controls or to allow the user to move to a different part of the media content.</span></span>
-   <span data-ttu-id="72cb7-209">**進度列。**</span><span class="sxs-lookup"><span data-stu-id="72cb7-209">**Progress bars.**</span></span> <span data-ttu-id="72cb7-210">進度列類似滑杆。</span><span class="sxs-lookup"><span data-stu-id="72cb7-210">Progress bars are similar to sliders.</span></span> <span data-ttu-id="72cb7-211">進度列的設計目的是要以圖形方式顯示已完成之特定進程的百分比，而不是使用者會想要與之互動的進程。</span><span class="sxs-lookup"><span data-stu-id="72cb7-211">Progress bars are designed for graphically displaying the percentage of a particular process that has been completed, but not for a process that the user will want to interact with.</span></span> <span data-ttu-id="72cb7-212">例如，您可能想要使用進度列來指出緩衝進度。</span><span class="sxs-lookup"><span data-stu-id="72cb7-212">For example, you might want to use a progress bar to indicate buffering progress.</span></span>
-   <span data-ttu-id="72cb7-213">**自訂滑杆。**</span><span class="sxs-lookup"><span data-stu-id="72cb7-213">**Custom sliders.**</span></span> <span data-ttu-id="72cb7-214">提供自訂滑杆功能，因此您可以建立旋鈕之類的控制項，或進行不尋常的控制機制。</span><span class="sxs-lookup"><span data-stu-id="72cb7-214">Custom slider functionality is provided so you can create controls such as knobs, or make unusual control mechanisms.</span></span> <span data-ttu-id="72cb7-215">例如，如果您想要建立在您的面板周圍換行的音量控制項，可以使用自訂滑杆來進行。</span><span class="sxs-lookup"><span data-stu-id="72cb7-215">For example, if you want to create a volume control that wraps around your skin, you can do it with a custom slider.</span></span> <span data-ttu-id="72cb7-216">若要設定自訂滑杆，您必須建立包含灰階影像的影像地圖，以定義滑杆上值的位置。</span><span class="sxs-lookup"><span data-stu-id="72cb7-216">To set up the custom slider, you must create an image map that contains grayscale images to define the locations of the values on the slider.</span></span> <span data-ttu-id="72cb7-217">這與支援圖層的圖形編輯程式相當簡單。</span><span class="sxs-lookup"><span data-stu-id="72cb7-217">This is relatively easy to do with a graphics editing program that supports layers.</span></span>

## <a name="text"></a><span data-ttu-id="72cb7-218">Text</span><span class="sxs-lookup"><span data-stu-id="72cb7-218">Text</span></span>

<span data-ttu-id="72cb7-219">您可以使用 **文字** 專案在面板上顯示文字，例如歌曲標題。</span><span class="sxs-lookup"><span data-stu-id="72cb7-219">You can use the **TEXT** element to display text on your skin, such as song titles.</span></span>

## <a name="video"></a><span data-ttu-id="72cb7-220">影片</span><span class="sxs-lookup"><span data-stu-id="72cb7-220">Video</span></span>

<span data-ttu-id="72cb7-221">您可以在面板中顯示影片。</span><span class="sxs-lookup"><span data-stu-id="72cb7-221">You can display video in your skin.</span></span> <span data-ttu-id="72cb7-222">**影片** 元素可讓您設定影片視窗的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="72cb7-222">The **VIDEO** element allows you to set the size and position of the video window.</span></span>

<span data-ttu-id="72cb7-223">您也可以允許使用者使用 **VIDEOSETTINGS** 元素來變更影片設定。</span><span class="sxs-lookup"><span data-stu-id="72cb7-223">You can also allow the user to change the video settings with the **VIDEOSETTINGS** element.</span></span> <span data-ttu-id="72cb7-224">例如，您可以建立控制項來調整影片的亮度。</span><span class="sxs-lookup"><span data-stu-id="72cb7-224">For example, you can create controls to adjust the brightness of the video.</span></span>

<span data-ttu-id="72cb7-225">如果您未提供影片元素，且內容包含影片，Windows Media Player 將會回到 [完整] 模式，且不會顯示您的面板。</span><span class="sxs-lookup"><span data-stu-id="72cb7-225">If you do not supply a video element and the content contains video, Windows Media Player will return to full mode and your skin will not be displayed.</span></span>

## <a name="equalizer-settings"></a><span data-ttu-id="72cb7-226">等化器設定</span><span class="sxs-lookup"><span data-stu-id="72cb7-226">Equalizer Settings</span></span>

<span data-ttu-id="72cb7-227">您可以使用 **EQUALIZERSETTINGS** 元素來設定特定音訊頻率群組的篩選。</span><span class="sxs-lookup"><span data-stu-id="72cb7-227">You can set the filtering for specific audio frequency bands by using the **EQUALIZERSETTINGS** element.</span></span> <span data-ttu-id="72cb7-228">您可以提高低音、調整高音，以及設定音效以符合您的耳或客廳。</span><span class="sxs-lookup"><span data-stu-id="72cb7-228">You can boost the bass, tweak the treble, and set up your sounds to match your ears or your living room.</span></span>

## <a name="visualizations"></a><span data-ttu-id="72cb7-229">視覺效果</span><span class="sxs-lookup"><span data-stu-id="72cb7-229">Visualizations</span></span>

<span data-ttu-id="72cb7-230">您可以在面板中顯示視覺效果。</span><span class="sxs-lookup"><span data-stu-id="72cb7-230">You can display visualizations in your skin.</span></span> <span data-ttu-id="72cb7-231">視覺效果是一段時間的視覺效果，會隨著音訊透過 Windows Media Player 播放。</span><span class="sxs-lookup"><span data-stu-id="72cb7-231">Visualizations are visual effects that change over time as audio is playing through Windows Media Player.</span></span> <span data-ttu-id="72cb7-232">**效果** 元素會決定視覺效果的播放位置、視窗的大小，以及要播放的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="72cb7-232">The **EFFECTS** element determines where the visualizations will play, what size the window will be, and which visualizations will be played.</span></span>

## <a name="playlists"></a><span data-ttu-id="72cb7-233">播放清單</span><span class="sxs-lookup"><span data-stu-id="72cb7-233">Playlists</span></span>

<span data-ttu-id="72cb7-234">您可以使用 **播放清單** 元素，讓使用者從特定的播放清單中選取專案。</span><span class="sxs-lookup"><span data-stu-id="72cb7-234">You can use the **PLAYLIST** element to let the user select an item from a specific playlist.</span></span>

## <a name="subviews"></a><span data-ttu-id="72cb7-235">子檢視</span><span class="sxs-lookup"><span data-stu-id="72cb7-235">Subviews</span></span>

<span data-ttu-id="72cb7-236">您可以使用 [子 **視圖** ] 元素來顯示介面控制項的次要集合，例如播放清單或影片控制項。</span><span class="sxs-lookup"><span data-stu-id="72cb7-236">You can use the **SUBVIEW** element to display secondary sets of interface controls, such as a playlist or video controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72cb7-237">相關主題</span><span class="sxs-lookup"><span data-stu-id="72cb7-237">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72cb7-238">**面板檔案**</span><span class="sxs-lookup"><span data-stu-id="72cb7-238">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




