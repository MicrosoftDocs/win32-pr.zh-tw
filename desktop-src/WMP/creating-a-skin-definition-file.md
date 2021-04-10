---
title: 建立外觀定義檔
description: 建立外觀定義檔
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Windows Media Player 行動外觀、面板定義檔
- 外觀、面板定義檔
- 面板的檔案、外觀定義
- 外觀定義檔，建立
- 建立外觀，關於
- 建立外觀 Windows Media Player 行動裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674015"
---
# <a name="creating-a-skin-definition-file"></a><span data-ttu-id="518b9-109">建立外觀定義檔</span><span class="sxs-lookup"><span data-stu-id="518b9-109">Creating a Skin Definition File</span></span>

<span data-ttu-id="518b9-110">面板定義檔是用來定義面板及其所有複合元件的文字檔。</span><span class="sxs-lookup"><span data-stu-id="518b9-110">A skin definition file is a text file that defines a skin and all its composite parts.</span></span> <span data-ttu-id="518b9-111">副檔名必須是. skn。</span><span class="sxs-lookup"><span data-stu-id="518b9-111">The file name extension must be .skn.</span></span>

<span data-ttu-id="518b9-112">每個面板定義檔的開頭都必須是下列程式程式碼，以指定面板檔案版本號碼。</span><span class="sxs-lookup"><span data-stu-id="518b9-112">Every skin definition file must start with the following line, which specifies the skin file version number.</span></span> <span data-ttu-id="518b9-113">下表顯示 Windows Media Player 版本以及應用來在面板定義檔中識別每個版本的程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="518b9-113">The following table shows Windows Media Player versions and the code line that should be used to identify each in a skin definition file.</span></span> <span data-ttu-id="518b9-114">雖然程式程式碼中的一些數位不是您預期的，但它們是正確的，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="518b9-114">Although some of the numbers in the code lines are not what you would expect, they are correct as shown in the following table.</span></span>



| <span data-ttu-id="518b9-115">Windows Media Player 版本</span><span class="sxs-lookup"><span data-stu-id="518b9-115">Windows Media Player version</span></span> | <span data-ttu-id="518b9-116">外觀定義檔案的第一行</span><span class="sxs-lookup"><span data-stu-id="518b9-116">First line of skin definition file</span></span> |
|------------------------------|------------------------------------|
| <span data-ttu-id="518b9-117">1.01.1</span><span class="sxs-lookup"><span data-stu-id="518b9-117">1.01.1</span></span><br/>            | <span data-ttu-id="518b9-118">\[Pocket WMP 皮檔1.0 版\]</span><span class="sxs-lookup"><span data-stu-id="518b9-118">\[Pocket WMP Skin File v1.0\]</span></span>      |
| <span data-ttu-id="518b9-119">1.2</span><span class="sxs-lookup"><span data-stu-id="518b9-119">1.2</span></span>                          | <span data-ttu-id="518b9-120">\[Pocket WMP 面板檔案 v 1。2\]</span><span class="sxs-lookup"><span data-stu-id="518b9-120">\[Pocket WMP Skin File v1.2\]</span></span>      |
| <span data-ttu-id="518b9-121">7.0</span><span class="sxs-lookup"><span data-stu-id="518b9-121">7.0</span></span>                          | <span data-ttu-id="518b9-122">\[Pocket WMP 皮檔 v2。0\]</span><span class="sxs-lookup"><span data-stu-id="518b9-122">\[Pocket WMP Skin File v2.0\]</span></span>      |
| <span data-ttu-id="518b9-123">7.1</span><span class="sxs-lookup"><span data-stu-id="518b9-123">7.1</span></span>                          | <span data-ttu-id="518b9-124">\[Pocket WMP 皮檔8.0 版\]</span><span class="sxs-lookup"><span data-stu-id="518b9-124">\[Pocket WMP Skin File v8.0\]</span></span>      |
| <span data-ttu-id="518b9-125">9系列</span><span class="sxs-lookup"><span data-stu-id="518b9-125">9 Series</span></span>                     | <span data-ttu-id="518b9-126">\[Pocket WMP 皮檔9.0。1\]</span><span class="sxs-lookup"><span data-stu-id="518b9-126">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="518b9-127">10 行動裝置版</span><span class="sxs-lookup"><span data-stu-id="518b9-127">10 Mobile</span></span>                    | <span data-ttu-id="518b9-128">\[Pocket WMP 皮檔9.0。1\]</span><span class="sxs-lookup"><span data-stu-id="518b9-128">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="518b9-129">10.1 行動裝置</span><span class="sxs-lookup"><span data-stu-id="518b9-129">10.1 Mobile</span></span>                  | <span data-ttu-id="518b9-130">\[Pocket WMP 皮檔9.0。1\]</span><span class="sxs-lookup"><span data-stu-id="518b9-130">\[Pocket WMP Skin File v9.0.1\]</span></span>    |



 

<span data-ttu-id="518b9-131">版本號碼9.0.1 適用于特別針對 Windows Media Player 9 系列或更新版本所建立的外觀。</span><span class="sxs-lookup"><span data-stu-id="518b9-131">The version number 9.0.1 is for skins created specifically for Windows Media Player 9 Series or later.</span></span> <span data-ttu-id="518b9-132">具有舊版號碼的面板會以 Windows Media Player 9 系列或更新版本的形式開啟為直向模式，每英寸96點 (DPI) 的外觀。</span><span class="sxs-lookup"><span data-stu-id="518b9-132">Skins having an earlier version number are opened by Windows Media Player 9 Series or later as portrait mode, 96 dots per inch (DPI) skins.</span></span>

<span data-ttu-id="518b9-133">外觀定義檔包含數個區段。</span><span class="sxs-lookup"><span data-stu-id="518b9-133">The skin definition file consists of several sections.</span></span> <span data-ttu-id="518b9-134">每個區段都會定義外觀的特定區域。</span><span class="sxs-lookup"><span data-stu-id="518b9-134">Each section defines a particular area of the skin.</span></span> <span data-ttu-id="518b9-135">這些區段必須以下列順序放置：</span><span class="sxs-lookup"><span data-stu-id="518b9-135">The sections must be placed in the following order:</span></span>

1.  <span data-ttu-id="518b9-136">Description</span><span class="sxs-lookup"><span data-stu-id="518b9-136">Description</span></span>
2.  <span data-ttu-id="518b9-137">點陣圖</span><span class="sxs-lookup"><span data-stu-id="518b9-137">Bitmaps</span></span>
3.  <span data-ttu-id="518b9-138">影片</span><span class="sxs-lookup"><span data-stu-id="518b9-138">Video</span></span>
4.  <span data-ttu-id="518b9-139">按鈕</span><span class="sxs-lookup"><span data-stu-id="518b9-139">Buttons</span></span>
5.  <span data-ttu-id="518b9-140">狀態</span><span class="sxs-lookup"><span data-stu-id="518b9-140">Status</span></span>
6.  <span data-ttu-id="518b9-141">Text</span><span class="sxs-lookup"><span data-stu-id="518b9-141">Text</span></span>
7.  <span data-ttu-id="518b9-142">Marquee</span><span class="sxs-lookup"><span data-stu-id="518b9-142">Marquee</span></span>
8.  <span data-ttu-id="518b9-143">Trackbars</span><span class="sxs-lookup"><span data-stu-id="518b9-143">Trackbars</span></span>

<span data-ttu-id="518b9-144">每個區段的開頭都是以方括弧括住的區段名稱，例如：</span><span class="sxs-lookup"><span data-stu-id="518b9-144">Each section starts with the name of the section in square brackets, for example:</span></span>


```C++
[ Bitmaps ]

```



> [!Note]  
> <span data-ttu-id="518b9-145">除非您在括弧和區段名稱之間包含空格，否則您的面板定義檔將不會正確剖析。</span><span class="sxs-lookup"><span data-stu-id="518b9-145">Your skin definition file will not be parsed correctly unless you include spaces between the brackets and the name of the section.</span></span>

 

<span data-ttu-id="518b9-146">然後，一或多行定義個別的影像、按鈕等等。</span><span class="sxs-lookup"><span data-stu-id="518b9-146">Then, one or more lines define individual images, buttons, and so on.</span></span> <span data-ttu-id="518b9-147">例如，點陣圖區段可能包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="518b9-147">For example, a Bitmaps section might include the following:</span></span>


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="518b9-148">不需要對齊資料行中的值，但可協助您的程式碼更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="518b9-148">It is not necessary to line up the values in columns, but it will help your code to be more readable.</span></span> <span data-ttu-id="518b9-149">如需有關面板定義檔各區段的詳細資訊，請參閱面板 [參考](skin-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="518b9-149">For more details about each section of the skin definition file, see the [Skin Reference](skin-reference.md).</span></span>

> [!Note]  
> <span data-ttu-id="518b9-150">請勿在檔案中的任何位置使用 tab 鍵;請改用額外的空間。</span><span class="sxs-lookup"><span data-stu-id="518b9-150">Do not use tabs anywhere in the file; use extra spaces instead.</span></span> <span data-ttu-id="518b9-151">這非常重要，因為在撰寫或編輯面板定義檔時按下 TAB 鍵會導致整個面板失敗。</span><span class="sxs-lookup"><span data-stu-id="518b9-151">This is very important, because pressing the TAB key while writing or editing your skin definition file will cause the entire skin to fail.</span></span> <span data-ttu-id="518b9-152">每行都必須完成，而且無法繼續到第二行。</span><span class="sxs-lookup"><span data-stu-id="518b9-152">Each line must be complete and cannot continue onto a second line.</span></span> <span data-ttu-id="518b9-153">此外，與 Windows Media Player 10 行動裝置版或更新版本搭配使用的面板也會取代區域和超級值。</span><span class="sxs-lookup"><span data-stu-id="518b9-153">Also, the Region and Super values are deprecated for skins used with Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="518b9-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="518b9-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="518b9-155">**外觀定義檔**</span><span class="sxs-lookup"><span data-stu-id="518b9-155">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 





