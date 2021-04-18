---
title: 新增影片
description: 新增影片
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- 建立外觀、影片
- Windows Media Player 的外觀、影片
- 外觀、影片
- 外觀中的影片，新增
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964970"
---
# <a name="adding-video"></a><span data-ttu-id="2577d-107">新增影片</span><span class="sxs-lookup"><span data-stu-id="2577d-107">Adding Video</span></span>

<span data-ttu-id="2577d-108">只要使用 **video** 元素，並定義要放置影片視窗的位置，您就可以將影片新增到檔案中。</span><span class="sxs-lookup"><span data-stu-id="2577d-108">You can add a video to your file by simply using the **VIDEO** element and defining where you want the video window to be placed.</span></span>

<span data-ttu-id="2577d-109">使用與 [選擇檔案] 區段中相同的程式碼;您只需要新增具有頂端、左方、寬度和高度屬性的 **影片** 元素即可。</span><span class="sxs-lookup"><span data-stu-id="2577d-109">Use the same code as you did in the Choosing Files section; all you need to do is add the **VIDEO** element with the top, left, width, and height attributes.</span></span>


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



<span data-ttu-id="2577d-110">然後當您播放影片時，它就會顯示在視窗中。</span><span class="sxs-lookup"><span data-stu-id="2577d-110">Then when you play a video, it will be displayed in the window.</span></span> <span data-ttu-id="2577d-111">影片範例的藝術已修改成稍微放大一個外觀。</span><span class="sxs-lookup"><span data-stu-id="2577d-111">The art for the video sample was modified to make a slightly larger skin.</span></span> <span data-ttu-id="2577d-112">由於圖層是在 Photoshop 中使用，因此這些按鈕很容易四處移動，而且會非常快速地建立新的集合。</span><span class="sxs-lookup"><span data-stu-id="2577d-112">Because layers were used in Photoshop, the buttons were easily moved around and a new set was created very quickly.</span></span> <span data-ttu-id="2577d-113">只有背景影像已變更。</span><span class="sxs-lookup"><span data-stu-id="2577d-113">Only the background image was changed.</span></span> <span data-ttu-id="2577d-114">空白圖層中使用填滿，且已新增斜面和浮凸效果。</span><span class="sxs-lookup"><span data-stu-id="2577d-114">A fill was used in a blank layer and a bevel and emboss effect was added.</span></span>

<span data-ttu-id="2577d-115">您可以在 SDK 的 [範例] 區段中看到類似的工作影片外觀。</span><span class="sxs-lookup"><span data-stu-id="2577d-115">You can see a similar working video skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2577d-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="2577d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2577d-117">**外觀建立指南**</span><span class="sxs-lookup"><span data-stu-id="2577d-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




