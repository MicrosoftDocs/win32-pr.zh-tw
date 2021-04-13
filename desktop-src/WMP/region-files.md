---
title: 區域檔案
description: 區域檔案
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Windows Media Player 行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 適用于外觀、區域檔案的美工檔案
- Windows Media Player 行動外觀、區域檔案
- 外觀，區域檔案
- 外觀中的區域檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311114"
---
# <a name="region-files"></a><span data-ttu-id="a50ee-110">區域檔案</span><span class="sxs-lookup"><span data-stu-id="a50ee-110">Region Files</span></span>

<span data-ttu-id="a50ee-111">如果您使用任何類型的點擊按鈕 (2PushHit、PushHit 或 ToggleHit) ，就需要區域檔案。</span><span class="sxs-lookup"><span data-stu-id="a50ee-111">Region files are required if you use any type of hit button (2PushHit, PushHit, or ToggleHit).</span></span>

<span data-ttu-id="a50ee-112">區域檔案是用來定義區域，這些區域會在特定按鈕上回應點一下，也稱為點擊。</span><span class="sxs-lookup"><span data-stu-id="a50ee-112">Region files are used to define areas that will respond to a tap, also known as a hit, on a specific button.</span></span> <span data-ttu-id="a50ee-113">針對每個點擊按鈕，區域點陣圖中的區域會獲得特定的 Web 色彩 (例如 \# FF0000，這是純紅色) 的值。</span><span class="sxs-lookup"><span data-stu-id="a50ee-113">For each hit button, an area in the Region bitmap is given a specific Web color (such as \#FF0000, which is the value for solid red).</span></span> <span data-ttu-id="a50ee-114">顏色編號是在區域按鈕定義中指定的。</span><span class="sxs-lookup"><span data-stu-id="a50ee-114">The color number is specified in the region button definition.</span></span> <span data-ttu-id="a50ee-115">當使用者顯示面板時，按鈕影像會使用區域點陣圖中區域的座標來重迭到背景。</span><span class="sxs-lookup"><span data-stu-id="a50ee-115">When the user displays the skin, the button image is superimposed onto the background using the coordinates of the area in the Region bitmap.</span></span>

<span data-ttu-id="a50ee-116">例如，您可以在對應至 [下一步] 按鈕位置的位置繪製紅色圓圈，並將其設為純紅色 (\# FF0000) 。</span><span class="sxs-lookup"><span data-stu-id="a50ee-116">For example, you could draw a red circle in a location corresponding to the location of the Next button and color it solid red (\#FF0000).</span></span> <span data-ttu-id="a50ee-117">然後，在按鈕定義中，您可以指派255、0、0 (的點擊 RGB 值，這是 FF0000) 的 RGB 對等專案 \# 。</span><span class="sxs-lookup"><span data-stu-id="a50ee-117">Then in the button definition, you could assign a hit RGB value of 255,0,0 (which is the RGB equivalent of \#FF0000).</span></span> <span data-ttu-id="a50ee-118">在此情況下，[下一步] 按鈕只會回應在紅色圓圈內) 的點擊 (叫用。</span><span class="sxs-lookup"><span data-stu-id="a50ee-118">In this case, the Next button would only respond to taps (hits) inside the red circle.</span></span>

<span data-ttu-id="a50ee-119">當您想要定義矩形以外的圖形時，就會使用點擊按鈕。</span><span class="sxs-lookup"><span data-stu-id="a50ee-119">Hit buttons are used when you want to define shapes other than rectangles.</span></span> <span data-ttu-id="a50ee-120">您仍然必須定義每個按鈕的座標，才能正確地找出已推送和已停用的次要影像。</span><span class="sxs-lookup"><span data-stu-id="a50ee-120">You must still define the coordinates for each button so that secondary images such as Pushed and Disabled can be located correctly.</span></span> <span data-ttu-id="a50ee-121">在實務上，每個按鈕都會以矩形來系結，而這些虛數界限矩形不得重迭。</span><span class="sxs-lookup"><span data-stu-id="a50ee-121">In practice, each button is bounded by a rectangle, and these imaginary boundary rectangles must not overlap.</span></span>

> [!Note]  
> <span data-ttu-id="a50ee-122">Windows Media Player 10 行動面板中不需要區域藝術檔案，因為 Windows Media Player 10 行動裝置版或更新版本不支援按鈕類型。</span><span class="sxs-lookup"><span data-stu-id="a50ee-122">Region art files are not needed in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="a50ee-123">下圖是一般的區域檔案。</span><span class="sxs-lookup"><span data-stu-id="a50ee-123">The following image is a typical Region file.</span></span>

![區域檔案](images/cesdkreg.png)

<span data-ttu-id="a50ee-125">此檔案會定義每個點擊類型按鈕的面板部分。</span><span class="sxs-lookup"><span data-stu-id="a50ee-125">This file defines the parts of the skin for each hit-type button.</span></span> <span data-ttu-id="a50ee-126">每個色彩都會依面板定義檔之按鈕區段中的色彩數位來識別。</span><span class="sxs-lookup"><span data-stu-id="a50ee-126">Each color will be identified by its color number in the Buttons section of the skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a50ee-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="a50ee-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a50ee-128">**美工檔案**</span><span class="sxs-lookup"><span data-stu-id="a50ee-128">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




