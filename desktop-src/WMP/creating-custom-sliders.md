---
title: 建立自訂滑杆
description: 建立自訂滑杆
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- 建立外觀、滑杆
- Windows Media Player 的外觀、滑杆
- 外觀、滑杆
- 外觀中的滑杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507332"
---
# <a name="creating-custom-sliders"></a><span data-ttu-id="119ce-107">建立自訂滑杆</span><span class="sxs-lookup"><span data-stu-id="119ce-107">Creating Custom Sliders</span></span>

<span data-ttu-id="119ce-108">您可以在任何想要的圖形中建立自訂滑杆。</span><span class="sxs-lookup"><span data-stu-id="119ce-108">You can create custom sliders in any shape you want.</span></span> <span data-ttu-id="119ce-109">在此範例中，選擇了簡單的帶，但實際的圖形可以是任何一種。</span><span class="sxs-lookup"><span data-stu-id="119ce-109">For this example, a simple strip is chosen, but the actual shape can be anything.</span></span> <span data-ttu-id="119ce-110">以下是 **CUSTOMSLIDER** 元素的程式碼：</span><span class="sxs-lookup"><span data-stu-id="119ce-110">Here is the code for the **CUSTOMSLIDER** element:</span></span>


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



<span data-ttu-id="119ce-111">這會設定滑杆的初始值。</span><span class="sxs-lookup"><span data-stu-id="119ce-111">This sets up an initial value for the slider.</span></span> <span data-ttu-id="119ce-112">引進兩個新的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="119ce-112">Two new bitmaps are introduced.</span></span> <span data-ttu-id="119ce-113">其中一個是灰階點陣圖 (slider.bmp) ，可定義按一下時將使用的值，另一個 (slider.bmp) 則會決定按一下灰階的特定部分時，會顯示哪個影像。</span><span class="sxs-lookup"><span data-stu-id="119ce-113">One is the grayscale bitmap (slider.bmp) that defines which values will be used when clicked on, and the other (slider.bmp) that determines which image will be shown when a particular portion of the grayscale is clicked on.</span></span>

<span data-ttu-id="119ce-114">初始值是藉由使用 wmpprop 接聽磁片區來決定，然後當使用者按一下會觸發值變更的滑杆部分時，就可以變更該磁片區。</span><span class="sxs-lookup"><span data-stu-id="119ce-114">The initial value is determined by listening to the volume with wmpprop and then the volume can be changed when the user clicks on a portion of the slider that triggers a change in value.</span></span>

<span data-ttu-id="119ce-115">您可以在 SDK 的 [範例] 區段中看到類似的工作滑杆外觀。</span><span class="sxs-lookup"><span data-stu-id="119ce-115">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="119ce-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="119ce-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="119ce-117">**外觀建立指南**</span><span class="sxs-lookup"><span data-stu-id="119ce-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




