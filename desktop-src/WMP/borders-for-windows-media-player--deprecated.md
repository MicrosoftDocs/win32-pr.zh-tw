---
title: Windows Media Player (已淘汰) 的框線
description: Windows Media Player (已淘汰) 的框線
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows Media Player、框線
- Windows Media Player 的外觀、框線
- 外觀、框線
- 框線，相較于外觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300820"
---
# <a name="borders-for-windows-media-player-deprecated"></a><span data-ttu-id="227ef-107">Windows Media Player (已淘汰) 的框線</span><span class="sxs-lookup"><span data-stu-id="227ef-107">Borders for Windows Media Player (deprecated)</span></span>

<span data-ttu-id="227ef-108">本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="227ef-108">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="227ef-109">框線與面板類似，但不是取代 Windows Media Player compact 模式的使用者介面，而是在完整模式 Windows Media Player 的 [立即播放] 窗格中內嵌框線。</span><span class="sxs-lookup"><span data-stu-id="227ef-109">A border is similar to a skin, but instead of replacing the user interface for the compact mode of Windows Media Player, a border is embedded in the Now Playing pane of the full mode Windows Media Player.</span></span>

<span data-ttu-id="227ef-110">藉由使用 Windows Media 下載套件，您可以包含具有框線的內容，paving 多媒體應用程式的方式。</span><span class="sxs-lookup"><span data-stu-id="227ef-110">By using a Windows Media Download package, you can include content with a border, paving the way to multimedia applications.</span></span>

<span data-ttu-id="227ef-111">包含框線和內嵌內容的範例 Windows Media 下載套件包含在此 SDK 的範例目錄中。</span><span class="sxs-lookup"><span data-stu-id="227ef-111">A sample Windows Media Download package that includes a border and embedded content is included in the samples directory of this SDK.</span></span>

## <a name="creating-a-border"></a><span data-ttu-id="227ef-112">建立框線</span><span class="sxs-lookup"><span data-stu-id="227ef-112">Creating a Border</span></span>

<span data-ttu-id="227ef-113">框線的建立方式與外觀相同。</span><span class="sxs-lookup"><span data-stu-id="227ef-113">A border is created the same way as a skin.</span></span> <span data-ttu-id="227ef-114">唯一的差別是，面板內嵌在 [ **立即播放** ] 窗格內。</span><span class="sxs-lookup"><span data-stu-id="227ef-114">The only difference is that the skin is embedded inside the **Now Playing** pane.</span></span> <span data-ttu-id="227ef-115">這表示無法計算外觀大小，而且所有的面板元素都必須是相對的。</span><span class="sxs-lookup"><span data-stu-id="227ef-115">This means that the skin size cannot be calculated and that all skin elements must be relative.</span></span> <span data-ttu-id="227ef-116">如果使用者調整 Windows Media Player 的大小，則框線的某些部分可能會遭到裁剪，而且看不到。</span><span class="sxs-lookup"><span data-stu-id="227ef-116">If the user resizes Windows Media Player, portions of the border may be clipped off and not seen.</span></span>

## <a name="loading-a-border"></a><span data-ttu-id="227ef-117">載入框線</span><span class="sxs-lookup"><span data-stu-id="227ef-117">Loading a Border</span></span>

<span data-ttu-id="227ef-118">載入使用 **面板元素的** Windows Media 中繼檔時，會載入框線。</span><span class="sxs-lookup"><span data-stu-id="227ef-118">A border is loaded when a Windows Media metafile that uses the **SKIN** element is loaded.</span></span> <span data-ttu-id="227ef-119">面板 **元素的** **HREF** 屬性必須參考面板。</span><span class="sxs-lookup"><span data-stu-id="227ef-119">The **HREF** attribute of the **SKIN** element must reference a skin.</span></span> <span data-ttu-id="227ef-120">一般的 **外觀** 元素如下所示：</span><span class="sxs-lookup"><span data-stu-id="227ef-120">A typical **SKIN** element would look like this:</span></span>


```C++
<SKIN HREF="myborder.wmz">

```



<span data-ttu-id="227ef-121">如需詳細資訊，請參閱 (已淘汰的面板 [元素) ](skin-element--deprecated.md)。</span><span class="sxs-lookup"><span data-stu-id="227ef-121">For more information, see [SKIN Element (deprecated)](skin-element--deprecated.md).</span></span>

## <a name="including-content-with-a-border"></a><span data-ttu-id="227ef-122">包含具有框線的內容</span><span class="sxs-lookup"><span data-stu-id="227ef-122">Including Content with a Border</span></span>

<span data-ttu-id="227ef-123">您可以使用 Windows Media 下載檔案 (副檔名為 wmd 的) ，來包含內容。</span><span class="sxs-lookup"><span data-stu-id="227ef-123">You can include content with a border by using a Windows Media Download file (with a .wmd file name extension).</span></span> <span data-ttu-id="227ef-124">請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="227ef-124">Follow these steps:</span></span>

1.  <span data-ttu-id="227ef-125">建立框線。</span><span class="sxs-lookup"><span data-stu-id="227ef-125">Create the border.</span></span> <span data-ttu-id="227ef-126">請小心建立它，使其調整大小不會損毀框線的組合。</span><span class="sxs-lookup"><span data-stu-id="227ef-126">Take care to create it in such a way that resizing will not ruin the composition of the border.</span></span> <span data-ttu-id="227ef-127">例如，請勿包含背景檔案;使背景變成透明，讓視覺效果可以在它背後執行。</span><span class="sxs-lookup"><span data-stu-id="227ef-127">For example, do not include a background file; make the background transparent so that a visualization could run behind it.</span></span>
2.  <span data-ttu-id="227ef-128">將面板內容 (藝術、JScript 檔案和麵板定義檔) 壓縮至副檔名為 wmz 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="227ef-128">Compress the skin contents (art, JScript files, and skin definition file) into a file with a .wmz file name extension.</span></span>
3.  <span data-ttu-id="227ef-129">使用副檔名為 .asx (的副檔名) 來建立 Windows Media 中繼檔 (，其會參考副檔名為 wmz 的) 檔。</span><span class="sxs-lookup"><span data-stu-id="227ef-129">Create a Windows Media metafile (with an .asx file name extension) that references the compressed border file (with a .wmz file name extension).</span></span> <span data-ttu-id="227ef-130">中繼檔可以包含播放清單資訊，其中包含適用于特定內容之藝術和 Url 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="227ef-130">The metafile can include playlist information with metadata for art and URLs for specific content.</span></span>
4.  <span data-ttu-id="227ef-131">組合數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="227ef-131">Assemble the digital media content.</span></span>
5.  <span data-ttu-id="227ef-132">將框線、中繼檔和內容壓縮成一個檔案，並提供副檔名為 wmd 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="227ef-132">Compress the border, metafile, and content into one file and give it a .wmd file name extension.</span></span>

## <a name="using-a-border"></a><span data-ttu-id="227ef-133">使用框線</span><span class="sxs-lookup"><span data-stu-id="227ef-133">Using a Border</span></span>

<span data-ttu-id="227ef-134">當您建立 Windows Media 下載檔案之後，使用者只需按兩下該檔案。</span><span class="sxs-lookup"><span data-stu-id="227ef-134">After you have created the Windows Media Download file, all that the user has to do is double-click on it.</span></span> <span data-ttu-id="227ef-135">檔案將會下載到使用者的電腦。</span><span class="sxs-lookup"><span data-stu-id="227ef-135">The file will be downloaded to the user's computer.</span></span> <span data-ttu-id="227ef-136">封裝內的檔案將會解除封裝，播放清單會加入播放清單中，框線會出現在完整模式 Windows Media Player 的 [ **立即播放** ] 窗格中，且新播放清單上的第一個專案會開始播放。</span><span class="sxs-lookup"><span data-stu-id="227ef-136">The files inside the package will be unpacked, the playlist will be added to the playlists, the border will appear in the **Now Playing** pane of the full mode Windows Media Player, and the first item on the new playlist will begin playing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="227ef-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="227ef-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="227ef-138">**關於外觀**</span><span class="sxs-lookup"><span data-stu-id="227ef-138">**About Skins**</span></span>](about-skins.md)
</dt> <dt>

[<span data-ttu-id="227ef-139">**範例**</span><span class="sxs-lookup"><span data-stu-id="227ef-139">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="227ef-140">**(淘汰的 Windows Media 下載套件)**</span><span class="sxs-lookup"><span data-stu-id="227ef-140">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




