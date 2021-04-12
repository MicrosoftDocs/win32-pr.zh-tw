---
title: 子視圖元素
description: 子視圖元素
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Windows Media Player 的外觀、子視圖元素
- 外觀，子視圖元素
- 子視圖元素
- 外觀的參考、子視圖元素
- 元素、子視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301808"
---
# <a name="subview-element"></a><span data-ttu-id="ca81a-108">子視圖元素</span><span class="sxs-lookup"><span data-stu-id="ca81a-108">SUBVIEW Element</span></span>

<span data-ttu-id="ca81a-109">[子 **視圖** ] 元素提供操作面板部分的方式，例如，提供在未使用時可以隱藏的 [控制台]。</span><span class="sxs-lookup"><span data-stu-id="ca81a-109">The **SUBVIEW** element provides a way to manipulate a portion of a skin, for example, to provide a control panel that can be hidden when it is not being used.</span></span> <span data-ttu-id="ca81a-110">子視圖 **元素一律** 是父 **VIEW** 專案的子系，而且可以包含其他面板元素，但 **VIEW**、**主題** 和 **其他子視圖專案** 除外。</span><span class="sxs-lookup"><span data-stu-id="ca81a-110">**SUBVIEW** elements are always children of parent **VIEW** elements, and can contain other skin element except for **VIEW**, **THEME**, and other **SUBVIEW** elements.</span></span>

<span data-ttu-id="ca81a-111">子 **視圖元素支援** 下列屬性，這些屬性定義于 **VIEW** 元素之下。</span><span class="sxs-lookup"><span data-stu-id="ca81a-111">The **SUBVIEW** element supports the following attributes, which are defined under the **VIEW** element.</span></span>



| <span data-ttu-id="ca81a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ca81a-112">Attribute</span></span>                                                       | <span data-ttu-id="ca81a-113">描述</span><span class="sxs-lookup"><span data-stu-id="ca81a-113">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca81a-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ca81a-114">backgroundColor</span></span>](view-backgroundcolor.md)                     | <span data-ttu-id="ca81a-115">指定或抓取子 **視圖** 控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="ca81a-115">Specifies or retrieves the background color of the **SUBVIEW** control.</span></span> <span data-ttu-id="ca81a-116">預設值為 "none"。</span><span class="sxs-lookup"><span data-stu-id="ca81a-116">The default value is "none".</span></span>        |
| [<span data-ttu-id="ca81a-117">backgroundImage</span><span class="sxs-lookup"><span data-stu-id="ca81a-117">backgroundImage</span></span>](view-backgroundimage.md)                     | <span data-ttu-id="ca81a-118">指定或抓取子 **視圖** 控制項的背景影像。</span><span class="sxs-lookup"><span data-stu-id="ca81a-118">Specifies or retrieves the background image of the **SUBVIEW** control.</span></span>                                     |
| [<span data-ttu-id="ca81a-119">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="ca81a-119">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="ca81a-120">指定或抓取背景影像色調的位移量。</span><span class="sxs-lookup"><span data-stu-id="ca81a-120">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                      |
| [<span data-ttu-id="ca81a-121">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="ca81a-121">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="ca81a-122">指定或抓取背景影像的飽和度值。</span><span class="sxs-lookup"><span data-stu-id="ca81a-122">Specifies or retrieves the saturation value of the background image.</span></span>                                        |
| [<span data-ttu-id="ca81a-123">backgroundTiled</span><span class="sxs-lookup"><span data-stu-id="ca81a-123">backgroundTiled</span></span>](view-backgroundtiled.md)                     | <span data-ttu-id="ca81a-124">指定或抓取值，指出是否將子 **視圖** 控制項的背景影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="ca81a-124">Specifies or retrieves a value indicating whether the background image of the **SUBVIEW** control is tiled.</span></span> |
| [<span data-ttu-id="ca81a-125">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="ca81a-125">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="ca81a-126">指定或抓取值，指出背景影像是否可以調整大小。</span><span class="sxs-lookup"><span data-stu-id="ca81a-126">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                      |
| [<span data-ttu-id="ca81a-127">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="ca81a-127">transparencyColor</span></span>](view-transparencycolor.md)                 | <span data-ttu-id="ca81a-128">指定或抓取背景影像的透明色彩。</span><span class="sxs-lookup"><span data-stu-id="ca81a-128">Specifies or retrieves the transparency color of the background image.</span></span>                                      |



 

<span data-ttu-id="ca81a-129">除非有注明，否則 [子 **視圖** ] 元素支援環境屬性。</span><span class="sxs-lookup"><span data-stu-id="ca81a-129">The **SUBVIEW** element supports the ambient attributes, except where noted.</span></span> <span data-ttu-id="ca81a-130">如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="ca81a-130">For more information, see [Ambient Attributes](ambient-attributes.md).</span></span>

<span data-ttu-id="ca81a-131">子 **視圖** 專案可以執行下列環境事件處理常式： [onendmove](onendmove.md) 和 [onresize](onresize.md)。</span><span class="sxs-lookup"><span data-stu-id="ca81a-131">The **SUBVIEW** element can implement the following ambient event handlers: [onendmove](onendmove.md) and [onresize](onresize.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca81a-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca81a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca81a-133">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="ca81a-133">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="ca81a-134">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="ca81a-134">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 




