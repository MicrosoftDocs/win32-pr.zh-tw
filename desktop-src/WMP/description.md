---
title: '描述 (Windows Media Player SDK) '
description: Description
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player 行動外觀、描述區段
- 外觀，描述區段
- 外觀的參考，描述區段
- 外觀中的描述區段
- 外觀定義檔，描述區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383678"
---
# <a name="description-windows-media-player-sdk"></a><span data-ttu-id="82b2b-108">描述 (Windows Media Player SDK) </span><span class="sxs-lookup"><span data-stu-id="82b2b-108">Description (Windows Media Player SDK)</span></span>

<span data-ttu-id="82b2b-109">當您建立適用于 Windows Mobile 2003 或更新版本的 Windows Media Player 9 系列面板時，必須包含描述區段。</span><span class="sxs-lookup"><span data-stu-id="82b2b-109">When you create a skin for Windows Media Player 9 Series for Windows Mobile 2003 or later, you must include a Description section.</span></span> <span data-ttu-id="82b2b-110">[描述] 區段可讓您指定顯示器的寬度和高度、顯示解析度，以及設計面板的顯示方向。</span><span class="sxs-lookup"><span data-stu-id="82b2b-110">The Description section enables you to specify the width and height of the display, the display resolution, and the display orientation for which the skin was designed.</span></span> <span data-ttu-id="82b2b-111">[描述] 區段必須出現在面板定義檔中的任何其他區段之前，以及在初始版本宣告之後。</span><span class="sxs-lookup"><span data-stu-id="82b2b-111">The Description section must appear in the skin definition file before any other section, and just after the initial version declaration.</span></span>

<span data-ttu-id="82b2b-112">面板定義檔的 [描述] 區段必須以下行開頭：</span><span class="sxs-lookup"><span data-stu-id="82b2b-112">The Description section of the skin definition file must begin with the following line:</span></span>


```C++
[ Description ]

```



<span data-ttu-id="82b2b-113">然後，您必須新增面板的維度和顯示解析度的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82b2b-113">You then must add information about the dimensions of the skin and the display resolution.</span></span> <span data-ttu-id="82b2b-114">下列範例顯示如何指定維度：</span><span class="sxs-lookup"><span data-stu-id="82b2b-114">The following example shows how to specify dimensions:</span></span>


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



<span data-ttu-id="82b2b-115">這會指定您將顯示的面板設計為240圖元寬、320圖元高，以及使用 96 DPI 顯示器解析度。</span><span class="sxs-lookup"><span data-stu-id="82b2b-115">This specifies that you designed the skin to be displayed 240 pixels wide, 320 pixels high, and using 96 DPI display resolution.</span></span> <span data-ttu-id="82b2b-116">請注意，這表示直向模式的方向。</span><span class="sxs-lookup"><span data-stu-id="82b2b-116">Note that this implies a portrait mode orientation.</span></span>

<span data-ttu-id="82b2b-117">您可以選擇性地指定您在 [描述] 區段中設計面板的方向模式。</span><span class="sxs-lookup"><span data-stu-id="82b2b-117">You may optionally specify the orientation mode for which you designed the skin in the description section.</span></span> <span data-ttu-id="82b2b-118">下列範例顯示如何指定方向：</span><span class="sxs-lookup"><span data-stu-id="82b2b-118">The following example shows how to specify orientation:</span></span>


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



<span data-ttu-id="82b2b-119">下表列出您可能用於方向的值。</span><span class="sxs-lookup"><span data-stu-id="82b2b-119">The following table lists the values you may use for Orientation.</span></span>



| <span data-ttu-id="82b2b-120">方向</span><span class="sxs-lookup"><span data-stu-id="82b2b-120">Orientation</span></span> | <span data-ttu-id="82b2b-121">描述</span><span class="sxs-lookup"><span data-stu-id="82b2b-121">Description</span></span>                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b2b-122">橫向</span><span class="sxs-lookup"><span data-stu-id="82b2b-122">Landscape</span></span>   | <span data-ttu-id="82b2b-123">外觀的寬度大於面板的高度。</span><span class="sxs-lookup"><span data-stu-id="82b2b-123">The width of the skin is greater than height of the skin.</span></span> <span data-ttu-id="82b2b-124">顯示是以水準方式導向。</span><span class="sxs-lookup"><span data-stu-id="82b2b-124">The display is oriented in a horizontal fashion.</span></span>   |
| <span data-ttu-id="82b2b-125">直向</span><span class="sxs-lookup"><span data-stu-id="82b2b-125">Portrait</span></span>    | <span data-ttu-id="82b2b-126">外觀的高度大於面板的寬度。</span><span class="sxs-lookup"><span data-stu-id="82b2b-126">The height of the skin is greater than the width of the skin.</span></span> <span data-ttu-id="82b2b-127">顯示器是以垂直方式導向。</span><span class="sxs-lookup"><span data-stu-id="82b2b-127">The display is oriented in a vertical fashion.</span></span> |
| <span data-ttu-id="82b2b-128">Square</span><span class="sxs-lookup"><span data-stu-id="82b2b-128">Square</span></span>      | <span data-ttu-id="82b2b-129">外觀的高度等於面板的寬度。</span><span class="sxs-lookup"><span data-stu-id="82b2b-129">The height of the skin is equal to the width of the skin.</span></span> <span data-ttu-id="82b2b-130">顯示器沒有方向。</span><span class="sxs-lookup"><span data-stu-id="82b2b-130">The display has no orientation.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="82b2b-131">當面板定義檔中指定的描述區段符合裝置目前的狀態時，Windows Mobile 2003 Windows Media Player 9 系列將只會顯示特定的外觀。</span><span class="sxs-lookup"><span data-stu-id="82b2b-131">Windows Media Player 9 Series for Windows Mobile 2003 will only display a particular skin when the description section specified in the skin definition file matches the current state of the device.</span></span>

 

<span data-ttu-id="82b2b-132">您應該小心指定您的面板所撰寫的正確維度、解析度和方向。</span><span class="sxs-lookup"><span data-stu-id="82b2b-132">You should be careful to always specify the correct dimensions, resolution, and orientation for which your skin was authored.</span></span> <span data-ttu-id="82b2b-133">例如，如果您的外觀所指定的維度描述了橫向的方向，則當裝置處於直向模式時，您的面板將無法使用，即使您在方向線中指定直向。</span><span class="sxs-lookup"><span data-stu-id="82b2b-133">For example, if the dimensions specified by your skin describe a landscape orientation, your skin will not be available when the device is in portrait mode, even if you specify Portrait in the orientation line.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82b2b-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="82b2b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82b2b-135">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="82b2b-135">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




