---
title: 按鈕類型
description: 按鈕類型
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Windows Media Player 行動外觀、按鈕類型
- 外觀，按鈕類型
- 外觀、按鈕的參考
- 外觀中的按鈕，類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839567"
---
# <a name="button-type"></a><span data-ttu-id="3e778-107">按鈕類型</span><span class="sxs-lookup"><span data-stu-id="3e778-107">Button Type</span></span>

<span data-ttu-id="3e778-108">按鈕分為兩種一般類型：位置和區域。</span><span class="sxs-lookup"><span data-stu-id="3e778-108">Buttons come in two general types: location and region.</span></span> <span data-ttu-id="3e778-109">每個一般類型都有三個特定的類型，全部都有六個按鈕類型。</span><span class="sxs-lookup"><span data-stu-id="3e778-109">Each general type has three specific types, making six button types in all.</span></span>

> [!Note]  
> <span data-ttu-id="3e778-110">在 Windows Media Player 10 行動裝置版或更新版本的面板中，按鈕類型已被取代。</span><span class="sxs-lookup"><span data-stu-id="3e778-110">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="3e778-111">位置按鈕類型</span><span class="sxs-lookup"><span data-stu-id="3e778-111">Location Button Types</span></span>

<span data-ttu-id="3e778-112">位置按鈕使用座標來定義其相對於背景的位置。</span><span class="sxs-lookup"><span data-stu-id="3e778-112">Location buttons use coordinates to define their locations relative to the background.</span></span> <span data-ttu-id="3e778-113">下表顯示對位置按鈕類型有效的值。</span><span class="sxs-lookup"><span data-stu-id="3e778-113">The following table shows the values that are valid for location button types.</span></span> <span data-ttu-id="3e778-114">您不需要為您將不會在面板中使用的類型定義值。</span><span class="sxs-lookup"><span data-stu-id="3e778-114">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="3e778-115">值</span><span class="sxs-lookup"><span data-stu-id="3e778-115">Value</span></span>  | <span data-ttu-id="3e778-116">描述</span><span class="sxs-lookup"><span data-stu-id="3e778-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e778-117">發送</span><span class="sxs-lookup"><span data-stu-id="3e778-117">Push</span></span>   | <span data-ttu-id="3e778-118">定義觸發一次事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e778-118">Defines a button that triggers an event once.</span></span> <span data-ttu-id="3e778-119">每次都必須推送按鈕，以觸發進一步的事件。</span><span class="sxs-lookup"><span data-stu-id="3e778-119">The button must be pushed each time to trigger further events.</span></span> <span data-ttu-id="3e778-120">例如，移至播放清單中下一個專案的按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e778-120">An example would be a button that moves to the next item in the playlist.</span></span> <span data-ttu-id="3e778-121">按鈕的位置是由其座標定義。</span><span class="sxs-lookup"><span data-stu-id="3e778-121">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3e778-122">切換</span><span class="sxs-lookup"><span data-stu-id="3e778-122">Toggle</span></span> | <span data-ttu-id="3e778-123">定義觸發變更狀態之事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e778-123">Defines a button that triggers an event that changes a state.</span></span> <span data-ttu-id="3e778-124">狀態會一直留在按鈕再次推送為止。</span><span class="sxs-lookup"><span data-stu-id="3e778-124">The state remains until the button is pushed again.</span></span> <span data-ttu-id="3e778-125">其中一個範例是洗牌播放清單的按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e778-125">An example is a button that shuffles the playlist.</span></span> <span data-ttu-id="3e778-126">當播放清單處於未進入狀態時，它會保持隨機運作，直到按鈕再次推送為止。</span><span class="sxs-lookup"><span data-stu-id="3e778-126">Once the playlist is in a shuffled state, it will remain shuffled until the button is pushed again.</span></span> <span data-ttu-id="3e778-127">按鈕的位置是由其座標定義。</span><span class="sxs-lookup"><span data-stu-id="3e778-127">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3e778-128">2Push</span><span class="sxs-lookup"><span data-stu-id="3e778-128">2Push</span></span>  | <span data-ttu-id="3e778-129">定義觸發事件的按鈕，然後變更為已準備好觸發不同事件的狀態。</span><span class="sxs-lookup"><span data-stu-id="3e778-129">Defines a button that triggers an event, and then changes to a state that is ready to trigger a different event.</span></span> <span data-ttu-id="3e778-130">這兩個狀態會在每次推送按鈕時切換。</span><span class="sxs-lookup"><span data-stu-id="3e778-130">The two states are toggled every time the button is pushed.</span></span> <span data-ttu-id="3e778-131">例如，使用 **PlayPause** 函式來切換播放和暫停目前媒體專案的按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e778-131">An example is a button that uses the **PlayPause** function to toggle between playing and pausing the current media item.</span></span> <span data-ttu-id="3e778-132">第一次推送按鈕時，會觸發主要播放狀態，並顯示次要影像以表示可以觸發 **暫停** 事件。</span><span class="sxs-lookup"><span data-stu-id="3e778-132">When the button is pushed the first time, the primary Play state is triggered and a secondary image is displayed to indicate that a **Pause** event can be triggered.</span></span> <span data-ttu-id="3e778-133">再次推送按鈕時，會觸發暫停狀態，並顯示原始影像以表示可以觸發 **播放** 事件。</span><span class="sxs-lookup"><span data-stu-id="3e778-133">When the button is pushed again, the Pause state is triggered and the original image is displayed to indicate that a **Play** event can be triggered.</span></span> <span data-ttu-id="3e778-134">按鈕的位置是由其座標定義。</span><span class="sxs-lookup"><span data-stu-id="3e778-134">The location of the button is defined by its coordinates.</span></span> |



 

<span data-ttu-id="3e778-135">區域按鈕類型</span><span class="sxs-lookup"><span data-stu-id="3e778-135">Region Button Types</span></span>

<span data-ttu-id="3e778-136">區域按鈕會使用區域影像中的色彩區域，來定義特定按鈕要處理的位置。</span><span class="sxs-lookup"><span data-stu-id="3e778-136">Region buttons use color areas in the Region image to define where taps will be processed for a particular button.</span></span> <span data-ttu-id="3e778-137">下表顯示對區域按鈕類型有效的值。</span><span class="sxs-lookup"><span data-stu-id="3e778-137">The following table shows the values that are valid for region button types.</span></span> <span data-ttu-id="3e778-138">您不需要為您將不會在面板中使用的類型定義值。</span><span class="sxs-lookup"><span data-stu-id="3e778-138">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="3e778-139">值</span><span class="sxs-lookup"><span data-stu-id="3e778-139">Value</span></span>     | <span data-ttu-id="3e778-140">描述</span><span class="sxs-lookup"><span data-stu-id="3e778-140">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e778-141">PushHit</span><span class="sxs-lookup"><span data-stu-id="3e778-141">PushHit</span></span>   | <span data-ttu-id="3e778-142">類似于推播按鈕值，不同之處在于按鈕的點擊區域是以區域影像中的色彩值來定義。</span><span class="sxs-lookup"><span data-stu-id="3e778-142">Similar to the Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>   |
| <span data-ttu-id="3e778-143">ToggleHit</span><span class="sxs-lookup"><span data-stu-id="3e778-143">ToggleHit</span></span> | <span data-ttu-id="3e778-144">類似于切換按鈕值，不同之處在于按鈕的點擊區域是以區域影像中的色彩值來定義。</span><span class="sxs-lookup"><span data-stu-id="3e778-144">Similar to the Toggle button value except that the hit area of the button is defined by the color value in the Region image.</span></span> |
| <span data-ttu-id="3e778-145">2PushHit</span><span class="sxs-lookup"><span data-stu-id="3e778-145">2PushHit</span></span>  | <span data-ttu-id="3e778-146">類似于2Push 按鈕值，不同之處在于按鈕的點擊區域是以區域影像中的色彩值來定義。</span><span class="sxs-lookup"><span data-stu-id="3e778-146">Similar to the 2Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="3e778-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e778-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e778-148">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="3e778-148">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




