---
title: 點陣圖類型
description: 點陣圖類型
ms.assetid: 208df4b9-d1be-49ff-bc0b-2e000608e9c7
keywords:
- Windows Media Player 行動外觀、點陣圖
- 外觀，點陣圖
- 外觀、點陣圖的參考
- 外觀中的點陣圖，類型
- 外觀中的點陣圖、值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602a436b5f4428b897672607265098104a9c1b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839995"
---
# <a name="bitmap-type"></a><span data-ttu-id="f9155-108">點陣圖類型</span><span class="sxs-lookup"><span data-stu-id="f9155-108">Bitmap Type</span></span>

<span data-ttu-id="f9155-109">下表顯示對點陣圖類型有效的值。</span><span class="sxs-lookup"><span data-stu-id="f9155-109">The following table shows the values that are valid for the bitmap type.</span></span> <span data-ttu-id="f9155-110">只需要背景類型;其他則是選擇性的，且與影像的不同可能用途相關。</span><span class="sxs-lookup"><span data-stu-id="f9155-110">Only the Background type is required; others are optional and relate to different possible uses of images.</span></span>



| <span data-ttu-id="f9155-111">值</span><span class="sxs-lookup"><span data-stu-id="f9155-111">Value</span></span>       | <span data-ttu-id="f9155-112">描述</span><span class="sxs-lookup"><span data-stu-id="f9155-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9155-113">背景</span><span class="sxs-lookup"><span data-stu-id="f9155-113">Background</span></span>  | <span data-ttu-id="f9155-114">必要。</span><span class="sxs-lookup"><span data-stu-id="f9155-114">Required.</span></span> <span data-ttu-id="f9155-115">所有按鈕影像的疊加影像。</span><span class="sxs-lookup"><span data-stu-id="f9155-115">The image upon which all button images are superimposed.</span></span> <span data-ttu-id="f9155-116">基底背景影像維度包含螢幕的完整寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="f9155-116">The base background image dimensions include the full width and height of the screen.</span></span> <span data-ttu-id="f9155-117">這也是顯示按鈕和 trackbars 自然狀態影像的檔案。</span><span class="sxs-lookup"><span data-stu-id="f9155-117">This is also the file where images for the natural states of buttons and trackbars are displayed.</span></span> <span data-ttu-id="f9155-118"> (推送和停用的按鈕不是此影像的一部分。 ) </span><span class="sxs-lookup"><span data-stu-id="f9155-118">(Pushed and disabled buttons are not part of this image.)</span></span>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f9155-119">Disabled</span><span class="sxs-lookup"><span data-stu-id="f9155-119">Disabled</span></span>    | <span data-ttu-id="f9155-120">必要。</span><span class="sxs-lookup"><span data-stu-id="f9155-120">Required.</span></span> <span data-ttu-id="f9155-121">表示推送按鈕不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="f9155-121">Indicates that pushing the button will have no effect.</span></span> <span data-ttu-id="f9155-122">定義當使用者無法使用特定的播放程式功能時，所顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="f9155-122">Defines an image that is displayed when specific player functionality is unavailable to the user.</span></span> <span data-ttu-id="f9155-123">您必須提供座標值，以指出此影像相對於背景影像的左上角位置。</span><span class="sxs-lookup"><span data-stu-id="f9155-123">You must supply a Coordinates value to indicate the top-left corner position of this image relative to the Background image.</span></span>                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f9155-124">推</span><span class="sxs-lookup"><span data-stu-id="f9155-124">Pushed</span></span>      | <span data-ttu-id="f9155-125">必要。</span><span class="sxs-lookup"><span data-stu-id="f9155-125">Required.</span></span> <span data-ttu-id="f9155-126">定義當使用者推送按鈕時所顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="f9155-126">Defines an image that is displayed when the user pushes a button.</span></span> <span data-ttu-id="f9155-127">當使用者按下按鈕時，使用 [已推播] 將視覺效果意見反應提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="f9155-127">Use Pushed to give visual feedback to the user when he taps on a button.</span></span> <span data-ttu-id="f9155-128">您必須提供座標值，以指出此影像相對於背景影像的左上角位置。</span><span class="sxs-lookup"><span data-stu-id="f9155-128">You must supply a Coordinates value to indicate the top-left corner position of this image relative to the Background image.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f9155-129">區域</span><span class="sxs-lookup"><span data-stu-id="f9155-129">Region</span></span>      | <span data-ttu-id="f9155-130">定義影像，使用彩色區域表示點擊類型按鈕的點-回應區域： PushHit、ToggleHit、2PushHit。</span><span class="sxs-lookup"><span data-stu-id="f9155-130">Defines images that use colored regions to represent the tap-response area for the hit-type buttons: PushHit, ToggleHit, 2PushHit.</span></span> <span data-ttu-id="f9155-131">如果您使用的是 [點擊類型] 按鈕，則必須提供區域影像。</span><span class="sxs-lookup"><span data-stu-id="f9155-131">If you are using the hit-type buttons, you must supply a Region image.</span></span> <span data-ttu-id="f9155-132">這個影像檔使用每個控制項的特定 Windows 元件色彩。</span><span class="sxs-lookup"><span data-stu-id="f9155-132">This image file uses specific Windows Palette colors for each control.</span></span> <span data-ttu-id="f9155-133">色彩是以代表區域紅色、綠色和藍色值的數位來定義。</span><span class="sxs-lookup"><span data-stu-id="f9155-133">The colors are defined by numbers representing the value of red, green, and blue for the region.</span></span> <span data-ttu-id="f9155-134">使用者永遠看不到此映射。</span><span class="sxs-lookup"><span data-stu-id="f9155-134">This image is never seen by the user.</span></span> <span data-ttu-id="f9155-135">您也必須提供座標值，以指出此影像相對於背景影像的左上角位置。</span><span class="sxs-lookup"><span data-stu-id="f9155-135">You must also supply a Coordinates value to indicate the top-left corner position of this image relative to the Background image.</span></span>                                                      |
| <span data-ttu-id="f9155-136">SeekThumb</span><span class="sxs-lookup"><span data-stu-id="f9155-136">SeekThumb</span></span>   | <span data-ttu-id="f9155-137">定義您將搭配使用中的影像，以表示媒體專案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="f9155-137">Defines an image that you will use in conjunction with a trackbar to indicate the current position in the media item.</span></span> <span data-ttu-id="f9155-138">例如，如果歌曲已完成一半的播放，則 SeekThumb 影像會顯示在顯示區的中間。</span><span class="sxs-lookup"><span data-stu-id="f9155-138">For example, if a song is half finished playing, the SeekThumb image is displayed in the middle of the trackbar.</span></span> <span data-ttu-id="f9155-139">藉由點擊和拖曳 SeekThumb 影像，使用者可以在任何位置（稱為 *搜尋*）重新開機媒體專案。</span><span class="sxs-lookup"><span data-stu-id="f9155-139">By tapping and dragging the SeekThumb image, the user can restart the media item at any position, which is called *seeking*.</span></span> <span data-ttu-id="f9155-140">在背景影像中定義了 [自動程式] 本身的影像。</span><span class="sxs-lookup"><span data-stu-id="f9155-140">The image of the trackbar itself is defined in the Background image.</span></span> <span data-ttu-id="f9155-141">SeekThumb 映射不會包含在面板定義檔的點陣圖區段中，但會指定為 TrackBars 區段中的 [區段] 定義的一部分。</span><span class="sxs-lookup"><span data-stu-id="f9155-141">The SeekThumb image is not included in the Bitmaps section of the skin definition file, but is specified as part of the trackbar definition in the TrackBars section.</span></span> |
| <span data-ttu-id="f9155-142">Super</span><span class="sxs-lookup"><span data-stu-id="f9155-142">Super</span></span>       | <span data-ttu-id="f9155-143">定義已停用的程式的影像。</span><span class="sxs-lookup"><span data-stu-id="f9155-143">Defines the Disabled image for a trackbar.</span></span> <span data-ttu-id="f9155-144">它也可以包含 [靜音] 按鈕的替代影像。</span><span class="sxs-lookup"><span data-stu-id="f9155-144">It can also contain alternate images for the mute button.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f9155-145">VolumeThumb</span><span class="sxs-lookup"><span data-stu-id="f9155-145">VolumeThumb</span></span> | <span data-ttu-id="f9155-146">定義要與處理常式搭配使用以表示音量位置的影像。</span><span class="sxs-lookup"><span data-stu-id="f9155-146">Defines an image to use in conjunction with a trackbar to indicate the volume position.</span></span> <span data-ttu-id="f9155-147">藉由點擊和拖曳 VolumeThumb 影像，使用者就可以變更音量層級。</span><span class="sxs-lookup"><span data-stu-id="f9155-147">By tapping and dragging the VolumeThumb image, the user can change the volume level.</span></span> <span data-ttu-id="f9155-148">在背景影像中定義了 [自動程式] 本身的影像。</span><span class="sxs-lookup"><span data-stu-id="f9155-148">The image of the trackbar itself is defined in the Background image.</span></span> <span data-ttu-id="f9155-149">VolumeThumb 映射不會包含在面板定義檔的點陣圖區段中，但會指定為 TrackBars 區段中的 [區段] 定義的一部分。</span><span class="sxs-lookup"><span data-stu-id="f9155-149">The VolumeThumb image is not included in the Bitmaps section of the skin definition file, but is specified as part of the trackbar definition in the TrackBars section.</span></span>                                                                                                                                                                                      |



 

> [!Note]  
> <span data-ttu-id="f9155-150">區域和 Super 點陣圖類型在 Windows Media Player 10 行動版或更新版本的外觀中已被取代。</span><span class="sxs-lookup"><span data-stu-id="f9155-150">Region and Super bitmap types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="f9155-151">請注意，檔案名和檔案類型的名稱不一定相同。</span><span class="sxs-lookup"><span data-stu-id="f9155-151">Note that the file name and the file type are not necessarily the same.</span></span> <span data-ttu-id="f9155-152">您可以呼叫所需的推播檔案，但在其他地方仍稱為推送。</span><span class="sxs-lookup"><span data-stu-id="f9155-152">You can call the Pushed file anything you like, but it is still referred to in other places as Pushed.</span></span> <span data-ttu-id="f9155-153">例如，在 [按鈕] 區段中，您將會有一個專案，例如：</span><span class="sxs-lookup"><span data-stu-id="f9155-153">For example, in the Buttons section, you will have an item such as:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="f9155-154">這是指檔案的類型，而不是檔案名。</span><span class="sxs-lookup"><span data-stu-id="f9155-154">This refers to the type of the file, not the file name.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9155-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9155-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9155-156">**點陣圖**</span><span class="sxs-lookup"><span data-stu-id="f9155-156">**Bitmaps**</span></span>](bitmaps.md)
</dt> </dl>

 

 




