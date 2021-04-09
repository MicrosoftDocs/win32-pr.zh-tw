---
title: 新增滑杆
description: 新增滑杆
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- 建立外觀、滑杆
- Windows Media Player 的外觀、滑杆
- 外觀、滑杆
- 外觀中的滑杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021702"
---
# <a name="adding-a-slider"></a><span data-ttu-id="364a3-107">新增滑杆</span><span class="sxs-lookup"><span data-stu-id="364a3-107">Adding a Slider</span></span>

<span data-ttu-id="364a3-108">您可以新增滑杆來顯示媒體目前的位置，也可以讓使用者變更目前媒體檔案中的位置。</span><span class="sxs-lookup"><span data-stu-id="364a3-108">You can add a slider to show the current position of the media, and also enable the user to change the position in the current media file.</span></span>

<span data-ttu-id="364a3-109">首先，您必須加入 **滑杆** 元素：</span><span class="sxs-lookup"><span data-stu-id="364a3-109">First you must add the **SLIDER** element:</span></span>


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



<span data-ttu-id="364a3-110">這會根據目前媒體檔案的持續時間來設定最大值。</span><span class="sxs-lookup"><span data-stu-id="364a3-110">This sets a maximum value based on the duration of the current media file.</span></span> <span data-ttu-id="364a3-111">這會使用小型 thumb 影像點陣圖，而這只是10圖元 x 綠色正方形的10圖元。</span><span class="sxs-lookup"><span data-stu-id="364a3-111">This uses a tiny thumb image bitmap that is just a 10 pixel by 10 pixel green square.</span></span> <span data-ttu-id="364a3-112">滑杆的背景會是紅色，前景則會是藍色。</span><span class="sxs-lookup"><span data-stu-id="364a3-112">The background of the slider will be red and the foreground will be blue.</span></span> <span data-ttu-id="364a3-113">當使用者將 thumb 影像拖曳至新位置，並讓滑鼠移至滑鼠按鍵時，媒體將會變更至該位置。</span><span class="sxs-lookup"><span data-stu-id="364a3-113">When the user drags the thumb image to a new position and lets go of the mouse button, the media will change to that position.</span></span>

<span data-ttu-id="364a3-114">但是，除非您使用 **控制項** 專案的 **currentPosition \_ onchange** 屬性來測量目前的位置，它會內嵌在 **PLAYER** 元素中，否則滑杆不會自行移動。</span><span class="sxs-lookup"><span data-stu-id="364a3-114">But the slider will not move by itself unless you measure the current position with the **currentPosition\_onchange** attribute of the **CONTROLS** element, which is embedded in the **PLAYER** element.</span></span>


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



<span data-ttu-id="364a3-115">當媒體的位置變更時，就會引發事件，然後執行程式程式碼，將滑杆的值變更為媒體的目前位置。</span><span class="sxs-lookup"><span data-stu-id="364a3-115">When the position of the media changes, this fires an event which then runs the line of code that changes the value of the slider to the current position of the media.</span></span>

<span data-ttu-id="364a3-116">您可以在 SDK 的 [範例] 區段中看到類似的工作滑杆外觀。</span><span class="sxs-lookup"><span data-stu-id="364a3-116">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="364a3-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="364a3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="364a3-118">**外觀建立指南**</span><span class="sxs-lookup"><span data-stu-id="364a3-118">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




