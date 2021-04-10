---
title: 新增 Close BUTTONELEMENT
description: 新增 Close BUTTONELEMENT
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- 建立外觀，BUTTONELEMENT 元素
- Windows Media Player 的 BUTTONELEMENT 元素
- 外觀，BUTTONELEMENT 元素
- 外觀定義檔，BUTTONELEMENT 元素
- BUTTONELEMENT 元素
- 元素，BUTTONELEMENT
- 建立外觀、關閉按鈕
- Windows Media Player 的外觀、關閉按鈕
- 外觀、關閉按鈕
- 外觀定義檔，關閉按鈕
- 關閉按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183600"
---
# <a name="adding-the-close-buttonelement"></a><span data-ttu-id="a4608-114">新增 Close BUTTONELEMENT</span><span class="sxs-lookup"><span data-stu-id="a4608-114">Adding the Close BUTTONELEMENT</span></span>

<span data-ttu-id="a4608-115">[關閉] 按鈕與 [播放] 按鈕的概念類似，但有不同的代碼和色彩。</span><span class="sxs-lookup"><span data-stu-id="a4608-115">The Close button is similar in concept to the Play button, but has different codes and colors.</span></span>

<span data-ttu-id="a4608-116">將接近 **BUTTONELEMENT** 的程式碼放在播放 **BUTTONELEMENT** 的右角括弧之後。</span><span class="sxs-lookup"><span data-stu-id="a4608-116">Put the Close **BUTTONELEMENT** code after the closing angle bracket of the Play **BUTTONELEMENT**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



<span data-ttu-id="a4608-117">下列屬性是用來定義 [關閉] 按鈕的 **BUTTONELEMENT** ：</span><span class="sxs-lookup"><span data-stu-id="a4608-117">The following attributes are used to define the **BUTTONELEMENT** for the Close button:</span></span>

<span data-ttu-id="a4608-118">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="a4608-118">**mappingColor**</span></span>

<span data-ttu-id="a4608-119">這是您先前建立之地圖藝術檔案中區域的色彩值。</span><span class="sxs-lookup"><span data-stu-id="a4608-119">This is the color value of the region in the mapping art file you created before.</span></span> <span data-ttu-id="a4608-120">在此情況下，它是紅色的紅色色彩。</span><span class="sxs-lookup"><span data-stu-id="a4608-120">In this case it is the solid red color.</span></span> <span data-ttu-id="a4608-121">任何 **BUTTONELEMENT** 都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a4608-121">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="a4608-122">藉由定義此色彩，您會告訴 Windows Media Player 將此色彩區域與此按鈕的 XML 程式碼產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a4608-122">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="a4608-123">**upToolTip**</span><span class="sxs-lookup"><span data-stu-id="a4608-123">**upToolTip**</span></span>

<span data-ttu-id="a4608-124">這會定義當使用者將滑鼠停留在按鈕上時，將顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="a4608-124">This defines the text that will be displayed when the user hovers the mouse over the button.</span></span> <span data-ttu-id="a4608-125">這與 [播放] 按鈕相同，不同之處在于它標示為「關閉」。</span><span class="sxs-lookup"><span data-stu-id="a4608-125">This is the same as the Play button except that it is labeled "Close".</span></span>

<span data-ttu-id="a4608-126">**onClick**</span><span class="sxs-lookup"><span data-stu-id="a4608-126">**onClick**</span></span>

<span data-ttu-id="a4608-127">這會定義滑鼠按一下按鈕時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="a4608-127">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="a4608-128">這個事件屬性的值稱為「事件處理常式」（event handler），它會是 Microsoft JScript 程式碼的行，或是由 **視圖** 的 **loadScript** 屬性所載入之外部文字檔中的 jscript 函數。</span><span class="sxs-lookup"><span data-stu-id="a4608-128">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="a4608-129">在此情況下，JScript 程式碼會使用全域屬性（attribute）**視圖** 來呼叫 **view** 專案的 **close** 方法，這會關閉視圖並關閉 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="a4608-129">In this case, the JScript code calls the **close** method of the **VIEW** element using the global attribute **view**, which closes the view and shuts down Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4608-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4608-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4608-131">**建立外觀定義檔**</span><span class="sxs-lookup"><span data-stu-id="a4608-131">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




