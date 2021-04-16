---
title: 執行轉譯範例
description: 執行轉譯範例
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- 視覺效果、光暈範例
- 自訂視覺效果，發光範例
- 程式設計指南，視覺效果
- 範例，發光視覺效果
- 發光視覺效果範例
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 轉譯函數，發光範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508276"
---
# <a name="implementing-render-sample"></a><span data-ttu-id="f071d-111">執行轉譯範例</span><span class="sxs-lookup"><span data-stu-id="f071d-111">Implementing Render Sample</span></span>

<span data-ttu-id="f071d-112">下列程式碼會用來執行轉譯 **函數：**</span><span class="sxs-lookup"><span data-stu-id="f071d-112">The following code is used to implement the **Render** function:</span></span>


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



<span data-ttu-id="f071d-113">以下是程式碼的說明：</span><span class="sxs-lookup"><span data-stu-id="f071d-113">Here is an explanation of the code:</span></span>

<span data-ttu-id="f071d-114">名為 *mycolor* 的變數會用於發光的色彩，並使用 **COLORREF** 來宣告。</span><span class="sxs-lookup"><span data-stu-id="f071d-114">A variable named *mycolor* is used for the color of the glow and is declared with **COLORREF**.</span></span> <span data-ttu-id="f071d-115">所有色彩都應該使用 **COLORREF** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f071d-115">All colors should use the **COLORREF** data type.</span></span>

<span data-ttu-id="f071d-116">名為 *mylevel* 的變數會用於音訊波形層級快照集。</span><span class="sxs-lookup"><span data-stu-id="f071d-116">A variable named *mylevel* is used for the audio waveform level snapshot.</span></span> <span data-ttu-id="f071d-117">此值將取決於快照集當時的實際電源等級。</span><span class="sxs-lookup"><span data-stu-id="f071d-117">This value will depend on the actual power level at the moment of the snapshot.</span></span>

<span data-ttu-id="f071d-118">**Switch** 語句是由使用者在 Windows Media Player 上選擇的預設值所設定。</span><span class="sxs-lookup"><span data-stu-id="f071d-118">The **switch** statement is set by the preset that the user has chosen on Windows Media Player.</span></span> <span data-ttu-id="f071d-119">選擇會將 *mycolor* 設定為所需的色彩 (red、綠或 blue) 。</span><span class="sxs-lookup"><span data-stu-id="f071d-119">The choice will set *mycolor* to the desired color (red, green, or blue).</span></span> <span data-ttu-id="f071d-120">不過，確切的色彩會由音訊電源等級決定。</span><span class="sxs-lookup"><span data-stu-id="f071d-120">However, the exact color will be determined by the audio power level.</span></span> <span data-ttu-id="f071d-121">例如，如果選擇紅色的預設值，色彩會是紅色的紅色，但會根據快照集當時的音訊波形而變得較淺或較暗。</span><span class="sxs-lookup"><span data-stu-id="f071d-121">For example, if the red preset is chosen, the color will be a solid red, but it will be lighter or darker depending on the audio waveform at the moment of the snapshot.</span></span> <span data-ttu-id="f071d-122">請務必使用 **RBG** 宏來建立您的色彩。</span><span class="sxs-lookup"><span data-stu-id="f071d-122">Be sure to use the **RBG** macro to create your color.</span></span>

<span data-ttu-id="f071d-123">建立的筆刷稱為 *hNewBrush*，它是用來填滿 Windows Media Player 所提供的 *prc* 矩形。</span><span class="sxs-lookup"><span data-stu-id="f071d-123">A brush is created called *hNewBrush*, and it is used to fill the *prc* rectangle provided by Windows Media Player.</span></span> <span data-ttu-id="f071d-124">繪圖介面是 Windows Media Player 所提供的 *hdc* 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="f071d-124">The drawing surface is the *hdc* device context provided by Windows Media Player.</span></span>

<span data-ttu-id="f071d-125">**DeleteObject** 會刪除筆刷。</span><span class="sxs-lookup"><span data-stu-id="f071d-125">The brush is deleted by **DeleteObject**.</span></span> <span data-ttu-id="f071d-126">務必刪除您所建立的任何畫筆或筆刷。</span><span class="sxs-lookup"><span data-stu-id="f071d-126">Always be sure to delete any pens or brushes you create.</span></span>

<span data-ttu-id="f071d-127">轉譯程式 **代碼完成** 後，Windows Media Player 將會在所使用的面板所決定的視窗中顯示 *hdc* 圖形。</span><span class="sxs-lookup"><span data-stu-id="f071d-127">Once the **Render** code is finished, Windows Media Player will display the *hdc* graphics in a window determined by the skin being used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f071d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="f071d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f071d-129">**發光範例**</span><span class="sxs-lookup"><span data-stu-id="f071d-129">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




