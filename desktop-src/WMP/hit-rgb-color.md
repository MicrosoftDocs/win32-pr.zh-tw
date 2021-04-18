---
title: 點擊 RGB 色彩
description: 點擊 RGB 色彩
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Windows Media Player 行動外觀、按鈕色彩
- 外觀，按鈕色彩
- 外觀、按鈕的參考
- 外觀、色彩中的按鈕
- 外觀的色彩參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965184"
---
# <a name="hit-rgb-color"></a><span data-ttu-id="8bacd-108">點擊 RGB 色彩</span><span class="sxs-lookup"><span data-stu-id="8bacd-108">Hit RGB Color</span></span>

<span data-ttu-id="8bacd-109">如果您使用的是 [PushHit]、[ToggleHit] 和 [2PushHit])  (的 [區域] 按鈕，您必須定義 Windows Media Player 將用來決定按鈕點擊區域的色彩。</span><span class="sxs-lookup"><span data-stu-id="8bacd-109">If you are using region buttons (PushHit, ToggleHit, and 2PushHit), you must define the color that Windows Media Player will use to determine the hit area of your button.</span></span> <span data-ttu-id="8bacd-110">這個值必須使用以逗號分隔的三個正整數來指定。</span><span class="sxs-lookup"><span data-stu-id="8bacd-110">This value must be specified using three positive integers separated by commas.</span></span> <span data-ttu-id="8bacd-111">這些整數代表點陣圖色彩的紅色、綠色和藍色量，範圍從0到255。</span><span class="sxs-lookup"><span data-stu-id="8bacd-111">These integers represent the amount of red, green, and blue for a bitmap color, and range from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="8bacd-112">在 Windows Media Player 10 行動裝置版或更新版本的面板中，按鈕類型已被取代。</span><span class="sxs-lookup"><span data-stu-id="8bacd-112">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="8bacd-113">您可以針對這些值使用任何色彩，但請確定您定義的每個區域按鈕在區域影像檔中都有唯一的色彩，而您在這裡定義的色彩值，會符合區域影像中使用的實際色彩。</span><span class="sxs-lookup"><span data-stu-id="8bacd-113">You can use any colors for the values, but be sure that each region button you define has a unique color in the Region image file and that the color value you define here as a number matches the actual color used in the Region image.</span></span>

<span data-ttu-id="8bacd-114">下表顯示您可能想要使用的一些典型色彩。</span><span class="sxs-lookup"><span data-stu-id="8bacd-114">The following table shows some typical colors you might want to use.</span></span>



| <span data-ttu-id="8bacd-115">值</span><span class="sxs-lookup"><span data-stu-id="8bacd-115">Value</span></span>       | <span data-ttu-id="8bacd-116">描述</span><span class="sxs-lookup"><span data-stu-id="8bacd-116">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="8bacd-117">0、0、0</span><span class="sxs-lookup"><span data-stu-id="8bacd-117">0,0,0</span></span>       | <span data-ttu-id="8bacd-118">黑色</span><span class="sxs-lookup"><span data-stu-id="8bacd-118">Black</span></span>       |
| <span data-ttu-id="8bacd-119">255255255</span><span class="sxs-lookup"><span data-stu-id="8bacd-119">255,255,255</span></span> | <span data-ttu-id="8bacd-120">白色</span><span class="sxs-lookup"><span data-stu-id="8bacd-120">White</span></span>       |
| <span data-ttu-id="8bacd-121">255、0、0</span><span class="sxs-lookup"><span data-stu-id="8bacd-121">255,0,0</span></span>     | <span data-ttu-id="8bacd-122">紅色</span><span class="sxs-lookup"><span data-stu-id="8bacd-122">Red</span></span>         |
| <span data-ttu-id="8bacd-123">0255，0</span><span class="sxs-lookup"><span data-stu-id="8bacd-123">0,255,0</span></span>     | <span data-ttu-id="8bacd-124">綠色</span><span class="sxs-lookup"><span data-stu-id="8bacd-124">Green</span></span>       |
| <span data-ttu-id="8bacd-125">0、0255</span><span class="sxs-lookup"><span data-stu-id="8bacd-125">0,0,255</span></span>     | <span data-ttu-id="8bacd-126">藍色</span><span class="sxs-lookup"><span data-stu-id="8bacd-126">Blue</span></span>        |



 

<span data-ttu-id="8bacd-127">如果您未使用區域按鈕，則必須輸入下列內容：</span><span class="sxs-lookup"><span data-stu-id="8bacd-127">If you do not use region buttons, you must enter the following:</span></span>


```C++
0,0,0

```



## <a name="related-topics"></a><span data-ttu-id="8bacd-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="8bacd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bacd-129">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="8bacd-129">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




