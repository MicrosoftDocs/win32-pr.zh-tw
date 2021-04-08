---
title: 如何執行氣球工具提示
description: 氣球工具提示類似于標準工具提示，但會顯示在卡通樣式 \ 0034; balloon \ 0034;以指向工具的主幹。
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671979"
---
# <a name="how-to-implement-balloon-tooltips"></a><span data-ttu-id="b0336-103">如何執行氣球工具提示</span><span class="sxs-lookup"><span data-stu-id="b0336-103">How to Implement Balloon Tooltips</span></span>

<span data-ttu-id="b0336-104">氣球工具提示類似于標準工具提示，但會顯示在卡通樣式的「球標」中，並以主幹指向工具。</span><span class="sxs-lookup"><span data-stu-id="b0336-104">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="b0336-105">氣球工具提示可以是單行或多行。</span><span class="sxs-lookup"><span data-stu-id="b0336-105">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="b0336-106">它們的建立和處理方式與標準工具提示的方式大致相同。</span><span class="sxs-lookup"><span data-stu-id="b0336-106">They are created and handled in much the same way as standard tooltips.</span></span>

<span data-ttu-id="b0336-107">下圖顯示詞幹和矩形的預設位置。</span><span class="sxs-lookup"><span data-stu-id="b0336-107">The default position of the stem and rectangle is shown in the following illustration.</span></span> <span data-ttu-id="b0336-108">如果工具太接近畫面頂端，工具提示會出現在工具矩形的下方和右邊。</span><span class="sxs-lookup"><span data-stu-id="b0336-108">If the tool is too close to the top of the screen, the tooltip appears below and to the right of the tool's rectangle.</span></span> <span data-ttu-id="b0336-109">如果工具太接近畫面右側，則適用類似的原則，但工具提示會出現在工具矩形的左邊。</span><span class="sxs-lookup"><span data-stu-id="b0336-109">If the tool is too close to the right side of the screen, similar principles apply, but the tooltip appears to the left of the tool's rectangle.</span></span>

![對話方塊的螢幕擷取畫面;具有一行文字的氣球工具提示會出現在目標的上方和右邊](images/tt-balloon.png)

<span data-ttu-id="b0336-111">您可以藉由在工具提示 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uFlags** 成員中設定 **TTF \_ CENTERTIP** 旗標，來變更預設位置。</span><span class="sxs-lookup"><span data-stu-id="b0336-111">You can change the default positioning by setting the **TTF\_CENTERTIP** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="b0336-112">在這種情況下，詞幹通常會指向工具矩形的下邊緣中央，而文字矩形則會直接顯示在工具的正下方。</span><span class="sxs-lookup"><span data-stu-id="b0336-112">In that case, the stem normally points to the center of the lower edge of the tool's rectangle, and the text rectangle is displayed directly below the tool.</span></span> <span data-ttu-id="b0336-113">此詞幹會附加至上方邊緣的文字矩形。</span><span class="sxs-lookup"><span data-stu-id="b0336-113">The stem attaches to the text rectangle at the center of the upper edge.</span></span> <span data-ttu-id="b0336-114">如果工具太接近畫面底部，則文字矩形的中心會在工具的上方，而莖會附加至下邊緣的中央。</span><span class="sxs-lookup"><span data-stu-id="b0336-114">If the tool is too close to the bottom of the screen, the text rectangle is centered above the tool, and the stem attaches to the center of the lower edge.</span></span>

<span data-ttu-id="b0336-115">下圖顯示以工具為中心的工具提示。</span><span class="sxs-lookup"><span data-stu-id="b0336-115">The following illustration shows a tooltip that is centered on the tool.</span></span>

![對話方塊的螢幕擷取畫面;具有一行文字的氣球工具提示會出現在目標底下的中央](images/tt-ballooncenter.png)

<span data-ttu-id="b0336-117">如果您想要指定莖的位置，請在工具提示 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uFlags** 成員中設定 **TTF \_ TRACK** 旗標。</span><span class="sxs-lookup"><span data-stu-id="b0336-117">If you want to specify where the stem points, set the **TTF\_TRACK** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="b0336-118">然後，您可以使用 *lParam* 值中的 x 和 y 座標來傳送 [**TTM \_ TRACKPOSITION**](ttm-trackposition.md)訊息，以指定座標。</span><span class="sxs-lookup"><span data-stu-id="b0336-118">You then specify the coordinate by sending a [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message, with the x- and y-coordinates in the *lParam* value.</span></span> <span data-ttu-id="b0336-119">如果同時設定了 **TTF \_ CENTERTIP** ，則詞幹仍會指向 **TTM \_ TRACKPOSITION** 訊息所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="b0336-119">If **TTF\_CENTERTIP** is also set, the stem still points to the position specified by the **TTM\_TRACKPOSITION** message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b0336-120">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="b0336-120">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b0336-121">技術</span><span class="sxs-lookup"><span data-stu-id="b0336-121">Technologies</span></span>

-   [<span data-ttu-id="b0336-122">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="b0336-122">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b0336-123">必要條件</span><span class="sxs-lookup"><span data-stu-id="b0336-123">Prerequisites</span></span>

-   <span data-ttu-id="b0336-124">C/C++</span><span class="sxs-lookup"><span data-stu-id="b0336-124">C/C++</span></span>
-   <span data-ttu-id="b0336-125">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="b0336-125">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b0336-126">指示</span><span class="sxs-lookup"><span data-stu-id="b0336-126">Instructions</span></span>

### <a name="implement-balloon-tooltips"></a><span data-ttu-id="b0336-127">執行氣球工具提示</span><span class="sxs-lookup"><span data-stu-id="b0336-127">Implement Balloon Tooltips</span></span>

<span data-ttu-id="b0336-128">下列範例程式碼示範如何使用 **TTS \_ 氣球** 工具提示控制項樣式來執行置中的氣球工具提示。</span><span class="sxs-lookup"><span data-stu-id="b0336-128">The following example code shows how to implement a centered balloon tooltip by using the **TTS\_BALLOON** tooltip control style.</span></span>


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a><span data-ttu-id="b0336-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0336-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0336-130">使用工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="b0336-130">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> <dt>

[<span data-ttu-id="b0336-131">**工具提示樣式**</span><span class="sxs-lookup"><span data-stu-id="b0336-131">**Tooltip Styles**</span></span>](tooltip-styles.md)
</dt> </dl>

 

 




