---
title: 內部事件
description: 內部事件
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Windows Media Player 的外觀、內部事件
- 外觀，內部事件
- 事件，內部
- 撰寫適用于面板、內部事件的程式碼
- 內部事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931998"
---
# <a name="internal-events"></a><span data-ttu-id="5b85d-108">內部事件</span><span class="sxs-lookup"><span data-stu-id="5b85d-108">Internal Events</span></span>

<span data-ttu-id="5b85d-109">您可以偵測 Windows Media Player 中發生的變更或您自己面板中的變更。</span><span class="sxs-lookup"><span data-stu-id="5b85d-109">You can detect changes that occur in Windows Media Player or changes in your own skin.</span></span> <span data-ttu-id="5b85d-110">這些可以是 Windows Media Player 物件屬性或方法中的變更、面板屬性的變更等等。</span><span class="sxs-lookup"><span data-stu-id="5b85d-110">These can be changes in Windows Media Player object properties or methods, changes in skin attributes, and so on.</span></span>

## <a name="windows-media-player-property-changes"></a><span data-ttu-id="5b85d-111">Windows Media Player 屬性變更</span><span class="sxs-lookup"><span data-stu-id="5b85d-111">Windows Media Player Property Changes</span></span>

<span data-ttu-id="5b85d-112">您可以使用 wmpprop 接聽程式來處理 Windows Media Player 中的變更。</span><span class="sxs-lookup"><span data-stu-id="5b85d-112">You can process changes in Windows Media Player by using the wmpprop listener.</span></span> <span data-ttu-id="5b85d-113">您必須將接聽程式設定為屬性的值。</span><span class="sxs-lookup"><span data-stu-id="5b85d-113">You must set up the listener as a value of an attribute.</span></span> <span data-ttu-id="5b85d-114">以雙引號括住值，並以 "wmpprop" 一字開頭，後面接著冒號。</span><span class="sxs-lookup"><span data-stu-id="5b85d-114">Put the value in double quotes, and start with the word "wmpprop" followed by a colon.</span></span> <span data-ttu-id="5b85d-115">然後，您會包含想要接聽的屬性。</span><span class="sxs-lookup"><span data-stu-id="5b85d-115">Then you include the property you want to listen to.</span></span> <span data-ttu-id="5b85d-116">當屬性變更時，屬性的值也會變更。</span><span class="sxs-lookup"><span data-stu-id="5b85d-116">When the property changes, the value of the attribute will change also.</span></span> <span data-ttu-id="5b85d-117">例如，每當 **currentPosition** 屬性的值變更時，若要讓滑杆元素值變更，請輸入下列內容：</span><span class="sxs-lookup"><span data-stu-id="5b85d-117">For example, to have a slider element value change whenever the value of the **currentPosition** attribute changes, type the following:</span></span>


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   <span data-ttu-id="5b85d-118">**重要** 請勿在 Windows Media Player 方法上使用 wmpprop。</span><span class="sxs-lookup"><span data-stu-id="5b85d-118">**Important** Do not use wmpprop on Windows Media Player methods.</span></span> <span data-ttu-id="5b85d-119">可能會發生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="5b85d-119">Unexpected results may occur.</span></span>

## <a name="windows-media-player-method-changes"></a><span data-ttu-id="5b85d-120">Windows Media Player 方法變更</span><span class="sxs-lookup"><span data-stu-id="5b85d-120">Windows Media Player Method Changes</span></span>

<span data-ttu-id="5b85d-121">您可以使用 wmpenabled 和 wmpdisabled，讓您的面板回應 Windows Media Player 上的方法可用性。</span><span class="sxs-lookup"><span data-stu-id="5b85d-121">You can make your skin respond to the availability of methods on Windows Media Player using wmpenabled and wmpdisabled.</span></span> <span data-ttu-id="5b85d-122">這些使用方式與 wmpprop 接聽程式類似，不同之處在于您只能在 **isAvailable** 方法所支援的 **控制項** 物件方法上使用這些方法。</span><span class="sxs-lookup"><span data-stu-id="5b85d-122">These are used similarly to the wmpprop listener except that you can only use these on methods of the **Control** object that are supported by the **isAvailable** method.</span></span>

<span data-ttu-id="5b85d-123">例如，您可以只在啟用 **Play** 方法時啟用按鈕，使用如下的程式碼：</span><span class="sxs-lookup"><span data-stu-id="5b85d-123">For example, you could enable a button only when the **Play** method is enabled, using code like this:</span></span>


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   <span data-ttu-id="5b85d-124">**重要** 請勿在 Windows Media Player 屬性上使用 wmpenabled 或 wmpdisabled。</span><span class="sxs-lookup"><span data-stu-id="5b85d-124">**Important** Do not use wmpenabled or wmpdisabled on Windows Media Player properties.</span></span> <span data-ttu-id="5b85d-125">可能會發生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="5b85d-125">Unexpected results may occur.</span></span>

## <a name="skin-attribute-changes"></a><span data-ttu-id="5b85d-126">外觀屬性變更</span><span class="sxs-lookup"><span data-stu-id="5b85d-126">Skin Attribute Changes</span></span>

<span data-ttu-id="5b85d-127">您可以使用 wmpprop 或 **\_ onchange** 事件，以兩種方式的其中一種來回應面板屬性中的變更。</span><span class="sxs-lookup"><span data-stu-id="5b85d-127">You can respond to changes in your skin attributes in one of two ways, by using wmpprop or the **\_onchange** event.</span></span>

<span data-ttu-id="5b85d-128">您可以使用 wmpprop 來接聽您自己面板中的變更。</span><span class="sxs-lookup"><span data-stu-id="5b85d-128">You can use wmpprop to listen for changes in your own skin.</span></span> <span data-ttu-id="5b85d-129">例如，若要在文字方塊中顯示滑杆值，您可以輸入下列內容：</span><span class="sxs-lookup"><span data-stu-id="5b85d-129">For example, to show the Slider value in a text box, you could type the following:</span></span>


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



<span data-ttu-id="5b85d-130">您可以使用 **\_ onchange** 事件來處理元素內的事件。</span><span class="sxs-lookup"><span data-stu-id="5b85d-130">You can use the **\_onchange** event to process events inside an element.</span></span> <span data-ttu-id="5b85d-131">您必須將您要追蹤的屬性名稱附加至 **\_ onchange**。</span><span class="sxs-lookup"><span data-stu-id="5b85d-131">You must attach the name of the attribute you want to track to **\_onchange**.</span></span> <span data-ttu-id="5b85d-132">例如，如果您想要追蹤文字方塊的值，請輸入：</span><span class="sxs-lookup"><span data-stu-id="5b85d-132">For example, if you want to track the value of a text box, you would type:</span></span>


```C++
value_onchange

```



<span data-ttu-id="5b85d-133">然後，您將指派值變更時要執行的 JScript 字串。</span><span class="sxs-lookup"><span data-stu-id="5b85d-133">You would then assign a JScript string that you want to run when the value changes.</span></span> <span data-ttu-id="5b85d-134">例如，若要回應可用來調整 Windows Media Player 音量之文字方塊值的變更，請在您的 **text** 元素內部輸入下列內容做為屬性：</span><span class="sxs-lookup"><span data-stu-id="5b85d-134">For example, to respond to a change in the value of a text box that can be used to adjust the volume of Windows Media Player, type the following inside your **TEXT** element as an attribute:</span></span>


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a><span data-ttu-id="5b85d-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b85d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b85d-136">**處理事件**</span><span class="sxs-lookup"><span data-stu-id="5b85d-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




