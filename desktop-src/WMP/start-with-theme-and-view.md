---
title: 開始使用主題和視圖
description: 開始使用主題和視圖
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- 建立外觀，主題元素
- Windows Media Player 的外觀，主題元素
- 外觀，主題元素
- 外觀定義檔，主題元素
- 主題元素
- 建立外觀、VIEW 元素
- Windows Media Player 的外觀、VIEW 元素
- 外觀，VIEW 元素
- 外觀定義檔，VIEW 元素
- VIEW 元素
- 元素、VIEW
- 元素，主題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840711"
---
# <a name="start-with-theme-and-view"></a><span data-ttu-id="24f14-115">開始使用主題和視圖</span><span class="sxs-lookup"><span data-stu-id="24f14-115">Start with THEME and VIEW</span></span>

<span data-ttu-id="24f14-116">每個面板都必須只有一個 **主題** 元素，以及至少一個 **VIEW** 元素。</span><span class="sxs-lookup"><span data-stu-id="24f14-116">Every skin must have exactly one **THEME** element and at least one **VIEW** element.</span></span>

<span data-ttu-id="24f14-117">使用文字編輯器，建立下列文字：</span><span class="sxs-lookup"><span data-stu-id="24f14-117">Using your text editor, create the following text:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



<span data-ttu-id="24f14-118">在關閉 **視圖** 標記之前保留一些空白行，因為稍後會在此新增更多程式碼。</span><span class="sxs-lookup"><span data-stu-id="24f14-118">Leave some blank lines before the closing **VIEW** tag because you'll be adding more code here later.</span></span>

<span data-ttu-id="24f14-119">使用您想要的任何檔案名來儲存您的檔案，但請確定副檔名為 wms。</span><span class="sxs-lookup"><span data-stu-id="24f14-119">Save your file with any file name you wish, but be sure that the extension is .wms.</span></span> <span data-ttu-id="24f14-120">例如，一般的檔案名可能是 skinone。</span><span class="sxs-lookup"><span data-stu-id="24f14-120">For example, a typical file name might be skinone.wms.</span></span>

<span data-ttu-id="24f14-121">每個面板的開頭都必須是 <THEME> ，並以結尾 </THEME>。</span><span class="sxs-lookup"><span data-stu-id="24f14-121">Every skin must start with <THEME> and end with </THEME>.</span></span> <span data-ttu-id="24f14-122">您的面板中只能有一個 **主題** 元素，但您必須有一個。</span><span class="sxs-lookup"><span data-stu-id="24f14-122">You can only have one **THEME** element in your skin, but you must have one.</span></span>

<span data-ttu-id="24f14-123">您也必須有至少一個 **VIEW** 元素。</span><span class="sxs-lookup"><span data-stu-id="24f14-123">You must also have at least one **VIEW** element.</span></span> <span data-ttu-id="24f14-124">您可以有一個以上的 **視圖**，但這個範例只有一個。</span><span class="sxs-lookup"><span data-stu-id="24f14-124">You can have more than one **VIEW**, but this example only has one.</span></span> <span data-ttu-id="24f14-125">您必須有開頭 <VIEW> 和結尾 <VIEW>。請注意，開頭 </VIEW> 標記不會立即關閉標記，但會在右角括弧 (>) 之前包含數個屬性。</span><span class="sxs-lookup"><span data-stu-id="24f14-125">You must have an opening <VIEW> and a closing <VIEW>. Notice that the opening </VIEW> tag does not close the tag right away, but includes several attributes before the closing angle bracket (>).</span></span> <span data-ttu-id="24f14-126">下列屬性用於此範例中的 **主題** 元素：</span><span class="sxs-lookup"><span data-stu-id="24f14-126">The following attributes are used in the **THEME** element in this example:</span></span>

<span data-ttu-id="24f14-127">**clippingColor**</span><span class="sxs-lookup"><span data-stu-id="24f14-127">**clippingColor**</span></span>

<span data-ttu-id="24f14-128">如果您的面板邊緣是矩形，您就不一定需要 **clippingColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="24f14-128">You will not always need the **clippingColor** attribute if the edges of your skin are rectangular.</span></span> <span data-ttu-id="24f14-129">此範例中的面板是橢圓形的，因此您需要您想要查看桌面的面板部分的裁剪色彩;基本上是 oval 以外的所有部分。</span><span class="sxs-lookup"><span data-stu-id="24f14-129">The skin in this example is oval-shaped, so you need a clipping color for the parts of the skin that you want to see the desktop through; essentially all parts outside the oval.</span></span> <span data-ttu-id="24f14-130">在此範例面板中，我們將使用以 Web 格式指定為 " \# CCCC00" 的深黃色。</span><span class="sxs-lookup"><span data-stu-id="24f14-130">In this example skin, we will use a dark yellow, specified as "\#CCCC00" in Web format.</span></span> <span data-ttu-id="24f14-131">這項選擇的原因是為了 [建立主要藝術](creating-the-primary-art-file.md)檔案而提供。</span><span class="sxs-lookup"><span data-stu-id="24f14-131">The reasons for this choice are given in [Creating the Primary Art File](creating-the-primary-art-file.md).</span></span> <span data-ttu-id="24f14-132">基本上，這個值一律是您從藝術節目中取得的數位。</span><span class="sxs-lookup"><span data-stu-id="24f14-132">Essentially, this value will always be a number that you get from your art program.</span></span>

<span data-ttu-id="24f14-133">**backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="24f14-133">**backgroundImage**</span></span>

<span data-ttu-id="24f14-134">這是主要藝術檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="24f14-134">This is the name of the primary art file.</span></span> <span data-ttu-id="24f14-135">它應該是您的主要圖片檔案的確切檔案名和路徑。</span><span class="sxs-lookup"><span data-stu-id="24f14-135">It should be the exact file name and path of your primary art file.</span></span> <span data-ttu-id="24f14-136">僅支援 BMP、JPG、GIF 和 PNG 檔案，建議使用 BMP。</span><span class="sxs-lookup"><span data-stu-id="24f14-136">Only BMP, JPG, GIF, and PNG files are supported, and BMP is recommended.</span></span>

<span data-ttu-id="24f14-137">**標題列**</span><span class="sxs-lookup"><span data-stu-id="24f14-137">**titleBar**</span></span>

<span data-ttu-id="24f14-138">此面板沒有 **標題列**，因此值會是 "false"。</span><span class="sxs-lookup"><span data-stu-id="24f14-138">This skin does not have a **titleBar**, so the value will be "false".</span></span> <span data-ttu-id="24f14-139">如果您想要讓面板具有背景色彩且為矩形，您只需要標題列。</span><span class="sxs-lookup"><span data-stu-id="24f14-139">You will only want a title bar if you want your skin to have a background color and be rectangular.</span></span>

<span data-ttu-id="24f14-140">確定您將結尾角括弧放 (>) **標題** 值之後，表示您已完成定義此 **視圖**。</span><span class="sxs-lookup"><span data-stu-id="24f14-140">Be sure that you put the closing angle bracket (>) after the **titleBar** value to indicate that you are finished defining the **VIEW**.</span></span> <span data-ttu-id="24f14-141">在關閉 **視圖** 和 **主題** 標記之前留下幾行空白行。</span><span class="sxs-lookup"><span data-stu-id="24f14-141">Leave a few blank lines before the closing **VIEW** and **THEME** tags.</span></span> <span data-ttu-id="24f14-142">您將需要稍後將加入的程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="24f14-142">You will need the lines for code that you will add later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24f14-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="24f14-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24f14-144">**建立外觀定義檔**</span><span class="sxs-lookup"><span data-stu-id="24f14-144">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




