---
title: 新增播放 BUTTONELEMENT
description: 新增播放 BUTTONELEMENT
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- 建立外觀，BUTTONELEMENT 元素
- Windows Media Player 的 BUTTONELEMENT 元素
- 外觀，BUTTONELEMENT 元素
- 外觀定義檔，BUTTONELEMENT 元素
- BUTTONELEMENT 元素
- 元素，BUTTONELEMENT
- 建立外觀、播放按鈕
- Windows Media Player 的外觀、播放按鈕
- 外觀、播放按鈕
- 外觀定義檔，播放按鈕
- 播放按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507248"
---
# <a name="adding-the-play-buttonelement"></a><span data-ttu-id="4bbfd-114">新增播放 BUTTONELEMENT</span><span class="sxs-lookup"><span data-stu-id="4bbfd-114">Adding the Play BUTTONELEMENT</span></span>

<span data-ttu-id="4bbfd-115">最後，您可以加入 **BUTTONELEMENT** 元素，以連接螢幕上的視覺效果按鈕來 Windows Media Player 動作。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-115">Finally, you can add the **BUTTONELEMENT** elements that connect the visual buttons on the screen to Windows Media Player actions.</span></span> <span data-ttu-id="4bbfd-116">這是您面板的核心，而您可以將其視為將面板表面連接到 Windows Media Player 的內部機械。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-116">This is the core of your skin and you can think of it as wiring the surface of the skin to the inner machinery of Windows Media Player.</span></span>

<span data-ttu-id="4bbfd-117">**BUTTONELEMENT** 會包含在 **BUTTONGROUP** 中。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-117">**BUTTONELEMENT** s are contained within a **BUTTONGROUP**.</span></span> <span data-ttu-id="4bbfd-118">每個 **BUTTONGROUP** 內都必須至少有一個 **BUTTONELEMENT** 。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-118">You must always have at least one **BUTTONELEMENT** inside each **BUTTONGROUP**.</span></span>

<span data-ttu-id="4bbfd-119">將 Play **BUTTONELEMENT** 程式碼放在 **BUTTONGROUP** 的右角括弧之後。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-119">Put the Play **BUTTONELEMENT** code after the closing angle bracket of **BUTTONGROUP**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



<span data-ttu-id="4bbfd-120">下列屬性是用來定義 [播放] 按鈕的 **BUTTONELEMENT** ：</span><span class="sxs-lookup"><span data-stu-id="4bbfd-120">The following attributes are used to define the **BUTTONELEMENT** for the Play button:</span></span>

<span data-ttu-id="4bbfd-121">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="4bbfd-121">**mappingColor**</span></span>

<span data-ttu-id="4bbfd-122">這是您先前建立之地圖藝術檔案中區域的色彩值。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-122">This is the color value of a region in the mapping art file you created before.</span></span> <span data-ttu-id="4bbfd-123">在這種情況下，它是純色的綠色色彩。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-123">In this case it is the solid green color.</span></span> <span data-ttu-id="4bbfd-124">任何 **BUTTONELEMENT** 都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-124">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="4bbfd-125">藉由定義此色彩，您會告訴 Windows Media Player 將此色彩區域與此按鈕的 XML 程式碼產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-125">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="4bbfd-126">**upToolTip**</span><span class="sxs-lookup"><span data-stu-id="4bbfd-126">**upToolTip**</span></span>

<span data-ttu-id="4bbfd-127">這會定義當使用者將滑鼠停留在按鈕上時所要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-127">This defines the text that will be displayed if the user hovers the mouse over the button.</span></span> <span data-ttu-id="4bbfd-128">請勿將它與將會顯示的暫留圖片混淆。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-128">Do not confuse this with the hover art that will be displayed.</span></span> <span data-ttu-id="4bbfd-129">工具提示是很小的氣球標題，需要一些時間才會出現。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-129">A ToolTip is a small balloon caption that takes a moment to appear.</span></span> <span data-ttu-id="4bbfd-130">不過，「暫止」圖片會以您選擇的任何色彩和圖形立即出現。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-130">The hover art image, however, will appear instantly in whatever color and shape you choose.</span></span>

<span data-ttu-id="4bbfd-131">**onClick**</span><span class="sxs-lookup"><span data-stu-id="4bbfd-131">**onClick**</span></span>

<span data-ttu-id="4bbfd-132">這會定義滑鼠按一下按鈕時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-132">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="4bbfd-133">這個事件屬性的值稱為「事件處理常式」（event handler），它會是 Microsoft JScript 程式碼的行，或是由 **視圖** 的 **loadScript** 屬性所載入之外部文字檔中的 jscript 函數。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-133">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="4bbfd-134">在此情況下，JScript 程式碼會呼叫 Windows Media Player 的 **URL** 方法，這個方法會載入並開始播放名為 "laure" 的檔案。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-134">In this case, the JScript code calls the **URL** method of Windows Media Player, which loads and starts playing a file named "laure.wma".</span></span> <span data-ttu-id="4bbfd-135">請注意，在引號內以分號結尾的行，這是良好的 JScript 編碼作法。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-135">Note that the line ends with a semicolon inside the quotes, which is good JScript coding practice.</span></span> <span data-ttu-id="4bbfd-136">也請注意，在雙引號內使用單引號來設定檔案名。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-136">Note also the use of single quotes inside the double quotes to set off the file name.</span></span> <span data-ttu-id="4bbfd-137">如需 JScript 的詳細資訊，請參閱此 SDK 的「關於面板」一節中的「 [使用 jscript](using-jscript.md) 」。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-137">For more information about JScript, see [Using JScript](using-jscript.md) in the About Skins section of this SDK.</span></span>

<span data-ttu-id="4bbfd-138">請注意，沒有結束的 **BUTTONELEMENT** 標記。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-138">Notice that there is no ending **BUTTONELEMENT** tag.</span></span> <span data-ttu-id="4bbfd-139">如果專案未括住另一個元素，您可以在右角括弧前面加上正斜線來關閉它。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-139">If an element does not enclose another element, you can close it off with the forward slash just before the closing angle bracket.</span></span> <span data-ttu-id="4bbfd-140">這會告訴 XML 您已完成該元素。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-140">This tells XML that you are finished with that element.</span></span> <span data-ttu-id="4bbfd-141">例如，</span><span class="sxs-lookup"><span data-stu-id="4bbfd-141">For example,</span></span>


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



<span data-ttu-id="4bbfd-142">及</span><span class="sxs-lookup"><span data-stu-id="4bbfd-142">and</span></span>


```C++
<BUTTONELEMENT/>
```



<span data-ttu-id="4bbfd-143">以 XML 傳達相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-143">convey the same information in XML.</span></span>

<span data-ttu-id="4bbfd-144">面板的威力來自于使用事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-144">The power of skins comes from using event handlers.</span></span> <span data-ttu-id="4bbfd-145">如果使用者使用滑鼠來執行某項工作，您可以使用 JScript 來處理該事件。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-145">If the user does something with a mouse, you can handle that event with JScript.</span></span> <span data-ttu-id="4bbfd-146">您的程式碼可以是單一行，讓 Windows Media Player 執行簡單的作業，例如播放，或者可以是以 JScript 撰寫的完整應用程式。</span><span class="sxs-lookup"><span data-stu-id="4bbfd-146">Your code can be a single line that makes Windows Media Player do something simple like play, or it can be a complete application written in JScript.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bbfd-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="4bbfd-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bbfd-148">**建立外觀定義檔**</span><span class="sxs-lookup"><span data-stu-id="4bbfd-148">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




