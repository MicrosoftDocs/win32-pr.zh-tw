---
title: 按鈕區段
description: 按鈕區段
ms.assetid: fa413bb4-e04a-4e3d-9754-cd4c2d82de6e
keywords:
- Windows Media Player 行動外觀、按鈕區段
- 外觀、按鈕區段
- 建立外觀、按鈕區段
- 撰寫面板的程式碼，按鈕區段
- 外觀、按鈕區段中的按鈕
- 外觀定義檔，按鈕區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f994225154e3f4cc55070351c32c654d5ad616c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021668"
---
# <a name="buttons-section"></a><span data-ttu-id="43345-109">按鈕區段</span><span class="sxs-lookup"><span data-stu-id="43345-109">Buttons Section</span></span>

<span data-ttu-id="43345-110">接下來，您必須定義您將使用的按鈕：</span><span class="sxs-lookup"><span data-stu-id="43345-110">Next, you must define the buttons you will be using:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   100,20,110,100 Pushed @ 100,20   Disabled @ 100,20    0,255,255  Pushed @ 270,20     Pushed @ 270,130
    Stop       PushHit    20,20,45,45    Pushed @ 20,20    Disabled @ 20,20   255,255,  0
    Next       PushHit    20,80,45,45    Pushed @ 20,80    Disabled @ 20,80   255,  0,  0
    Prev       PushHit    20,140,45,45   Pushed @ 20,140   Disabled @ 20,130    0,  0,255

```



<span data-ttu-id="43345-111">此區段中定義了四個按鈕。</span><span class="sxs-lookup"><span data-stu-id="43345-111">There are four buttons defined in this section.</span></span> <span data-ttu-id="43345-112">您正在觀賞的頁面可能會包裝這些行，但是當您輸入程式碼時，不能換行;也就是說，每一行都必須完成，並以段落標記結尾。</span><span class="sxs-lookup"><span data-stu-id="43345-112">The page you are viewing may wrap these lines, but when you type in the code, you must not wrap lines; that is, each line must be complete and end with a paragraph mark.</span></span>

> [!Note]  
> <span data-ttu-id="43345-113">按鈕類型在 Windows Media Player 10 行動裝置版或更新版本的外觀中已被取代。</span><span class="sxs-lookup"><span data-stu-id="43345-113">Buttons types are deprecated in Windows Media Player 10 Mobile or later skins.</span></span> <span data-ttu-id="43345-114">請為每個類型輸入 "NA"，而不是在您的面板檔案中宣告的按鈕類型。</span><span class="sxs-lookup"><span data-stu-id="43345-114">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

<span data-ttu-id="43345-115">針對每個按鈕，您必須針對) 的點擊類型按鈕，定義函式、類型、位置、推播影像來源、停用的來源和色彩 (。</span><span class="sxs-lookup"><span data-stu-id="43345-115">For each button you must define the function, type, location, pushed image source, disabled source, and color (for hit-type buttons).</span></span> <span data-ttu-id="43345-116">此外，針對 [PlayPause] 按鈕，您必須針對 [暫停] 狀態定義正常和推送的影像來源。</span><span class="sxs-lookup"><span data-stu-id="43345-116">In addition, for the PlayPause button, you must define the normal and pushed image sources for the paused state.</span></span>

<span data-ttu-id="43345-117">如需有關面板定義檔之按鈕區段的詳細資訊，請參閱面板參考中的 [按鈕](buttons.md) 。</span><span class="sxs-lookup"><span data-stu-id="43345-117">For more about the Buttons section of the skin definition file, see [Buttons](buttons.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43345-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="43345-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43345-119">**撰寫程式碼**</span><span class="sxs-lookup"><span data-stu-id="43345-119">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




