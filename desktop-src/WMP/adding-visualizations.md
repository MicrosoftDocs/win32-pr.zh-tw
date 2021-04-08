---
title: 新增視覺效果
description: 新增視覺效果
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- 建立外觀、視覺效果
- Windows Media Player 的外觀、視覺效果
- 外觀、視覺效果
- 視覺效果，外觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673391"
---
# <a name="adding-visualizations"></a><span data-ttu-id="e01df-107">新增視覺效果</span><span class="sxs-lookup"><span data-stu-id="e01df-107">Adding Visualizations</span></span>

<span data-ttu-id="e01df-108">您可以使用新增影片視窗的相同方式來新增視覺效果視窗。</span><span class="sxs-lookup"><span data-stu-id="e01df-108">You can add a visualization window the same way you added a video window.</span></span> <span data-ttu-id="e01df-109">您可以使用相同的面板，但會使用 **效果** 元素。</span><span class="sxs-lookup"><span data-stu-id="e01df-109">The same skin can be used, but an **EFFECTS** element is used.</span></span>

<span data-ttu-id="e01df-110">首先，您必須新增 **效果** 元素，並為其指定識別碼和大小：</span><span class="sxs-lookup"><span data-stu-id="e01df-110">First you must add the **EFFECTS** element and give it an ID and size:</span></span>


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



<span data-ttu-id="e01df-111">然後，您可以為先前和下一個視覺效果程式碼字串指派兩個按鈕：</span><span class="sxs-lookup"><span data-stu-id="e01df-111">Then you can assign the two buttons a previous and next visualization code string:</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



<span data-ttu-id="e01df-112">圖層和點陣圖與影片範例中所用的圖層和點陣圖相同，不同之處在于會以水準方式複製和翻轉播放箭號。</span><span class="sxs-lookup"><span data-stu-id="e01df-112">The layers and bitmaps were the same ones used in the video example, except that the play arrow was copied and flipped horizontally.</span></span>

<span data-ttu-id="e01df-113">最後，新增了具有 **URL** 屬性的簡單 **播放機** 元素，以選擇要播放的歌曲。</span><span class="sxs-lookup"><span data-stu-id="e01df-113">Finally, a simple **PLAYER** element with the **URL** attribute was added to choose a song to play.</span></span>


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



<span data-ttu-id="e01df-114">您可以在 SDK 的範例區段中看到類似的工作視覺效果外觀。</span><span class="sxs-lookup"><span data-stu-id="e01df-114">You can see a similar working visualization skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e01df-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e01df-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e01df-116">**外觀建立指南**</span><span class="sxs-lookup"><span data-stu-id="e01df-116">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




