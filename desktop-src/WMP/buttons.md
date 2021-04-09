---
title: Windows Media Player SDK) 的按鈕 (
description: 按鈕
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Windows Media Player 行動外觀面板，按鈕總覽
- 外觀，按鈕總覽
- 外觀、按鈕的參考
- 面板中的按鈕，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093708"
---
# <a name="buttons-windows-media-player-sdk"></a><span data-ttu-id="def65-107">Windows Media Player SDK) 的按鈕 (</span><span class="sxs-lookup"><span data-stu-id="def65-107">Buttons (Windows Media Player SDK)</span></span>

<span data-ttu-id="def65-108">您會想要在面板中使用一或多個按鈕，而且每個按鈕都必須定義于面板定義檔中。</span><span class="sxs-lookup"><span data-stu-id="def65-108">You will want to use one or more buttons in your skin, and each button must be defined in the skin definition file.</span></span> <span data-ttu-id="def65-109">如果您未在此區段中定義按鈕，您的面板將無法使用它。</span><span class="sxs-lookup"><span data-stu-id="def65-109">If you do not define a button in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="def65-110">面板定義檔的 [按鈕] 區段開頭為以下這一行：</span><span class="sxs-lookup"><span data-stu-id="def65-110">The buttons section of the skin definition file begins with this line:</span></span>


```C++
[ Buttons ]

```



<span data-ttu-id="def65-111">然後，您必須新增一或多行，其中包含面板中每個按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="def65-111">You then must add one or more lines that contain information about each of the buttons in your skin.</span></span> <span data-ttu-id="def65-112">一般的行可能是：</span><span class="sxs-lookup"><span data-stu-id="def65-112">A typical line might be:</span></span>


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



<span data-ttu-id="def65-113">請注意，此程式碼的類型應該是以 "PlayPause" 為開頭的一行，並以 "推送 @ 160，98" 結尾。</span><span class="sxs-lookup"><span data-stu-id="def65-113">Note that this code should be typed as one line starting with "PlayPause" and ending with "Pushed @ 160,98".</span></span>

<span data-ttu-id="def65-114">您可以針對面板定義檔的按鈕區段使用下列範本：</span><span class="sxs-lookup"><span data-stu-id="def65-114">You can use the following template for the Button section of your skin definition file:</span></span>


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



<span data-ttu-id="def65-115">同樣地，請注意，這些應輸入為單一行，第一個開頭為 "// <Function> " 且結尾為 " &lt; Push 2 Image Src &gt; "。</span><span class="sxs-lookup"><span data-stu-id="def65-115">Again, note that these should be typed as single lines, the first starting with "// <Function>" and ending with "&lt;Push 2 Image Src&gt;".</span></span> <span data-ttu-id="def65-116">第二行的開頭為 "//----------"，結尾為 "------------------."</span><span class="sxs-lookup"><span data-stu-id="def65-116">The second line starts with "// ----------" and ends with "------------------."</span></span>

<span data-ttu-id="def65-117">按鈕區段中每一行的按鈕資訊必須以下列順序顯示。</span><span class="sxs-lookup"><span data-stu-id="def65-117">Button information for each line in the Button section must appear in the following order.</span></span> <span data-ttu-id="def65-118">只有行的前六個部分是必要的。</span><span class="sxs-lookup"><span data-stu-id="def65-118">Only the first six parts of the line are required.</span></span> <span data-ttu-id="def65-119">除非必要，否則不會包含次要映射。</span><span class="sxs-lookup"><span data-stu-id="def65-119">Secondary images are not included unless they are needed.</span></span>

1.  [<span data-ttu-id="def65-120">Button 函數</span><span class="sxs-lookup"><span data-stu-id="def65-120">Button Function</span></span>](button-function.md)
2.  [<span data-ttu-id="def65-121">按鈕類型</span><span class="sxs-lookup"><span data-stu-id="def65-121">Button Type</span></span>](button-type.md)
3.  [<span data-ttu-id="def65-122">按鈕位置</span><span class="sxs-lookup"><span data-stu-id="def65-122">Button Location</span></span>](button-location.md)
4.  [<span data-ttu-id="def65-123">推送的影像來源</span><span class="sxs-lookup"><span data-stu-id="def65-123">Pushed Image Source</span></span>](pushed-image-source.md)
5.  [<span data-ttu-id="def65-124">已停用按鈕的影像來源</span><span class="sxs-lookup"><span data-stu-id="def65-124">Image Source for Disabled Button</span></span>](image-source-for-disabled-button.md)
6.  [<span data-ttu-id="def65-125">點擊 RGB 色彩</span><span class="sxs-lookup"><span data-stu-id="def65-125">Hit RGB Color</span></span>](hit-rgb-color.md)
7.  [<span data-ttu-id="def65-126">一般次要影像來源</span><span class="sxs-lookup"><span data-stu-id="def65-126">Normal Secondary Image Source</span></span>](normal-secondary-image-source.md)
8.  [<span data-ttu-id="def65-127">一般的三映射來源</span><span class="sxs-lookup"><span data-stu-id="def65-127">Normal Tertiary Image Source</span></span>](normal-tertiary-image-source.md)
9.  [<span data-ttu-id="def65-128">推送的次要影像來源</span><span class="sxs-lookup"><span data-stu-id="def65-128">Pushed Secondary Image Source</span></span>](pushed-secondary-image-source.md)
10. [<span data-ttu-id="def65-129">推送的第三個映射來源</span><span class="sxs-lookup"><span data-stu-id="def65-129">Pushed Tertiary Image Source</span></span>](pushed-tertiary-image-source.md)

<span data-ttu-id="def65-130">如需按鈕程式碼的範例，請參閱 [範例按鈕一節](sample-button-section.md)。</span><span class="sxs-lookup"><span data-stu-id="def65-130">For an example of button code, see [Sample Button Section](sample-button-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="def65-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="def65-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="def65-132">**外觀參考**</span><span class="sxs-lookup"><span data-stu-id="def65-132">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




