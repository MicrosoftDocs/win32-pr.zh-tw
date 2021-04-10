---
title: " (已淘汰) 建立 Windows Media 下載套件"
description: " (已淘汰) 建立 Windows Media 下載套件"
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Windows Media 中繼檔，Windows Media 下載套件
- Windows Media Player，Windows Media 下載套件
- 中繼檔，Windows Media 下載套件
- Windows Media、Windows Media 下載套件
- Windows Media 下載套件，建立
- 建立 Windows Media 下載套件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021654"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a><span data-ttu-id="0cd18-109"> (已淘汰) 建立 Windows Media 下載套件</span><span class="sxs-lookup"><span data-stu-id="0cd18-109">Creating a Windows Media Download Package (deprecated)</span></span>

<span data-ttu-id="0cd18-110">本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="0cd18-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="0cd18-111">請遵循下列步驟來建立 Windows Media 下載套件。</span><span class="sxs-lookup"><span data-stu-id="0cd18-111">Follow these steps to create a Windows Media Download package.</span></span>

1.  <span data-ttu-id="0cd18-112">**建立框線。**</span><span class="sxs-lookup"><span data-stu-id="0cd18-112">**Create a border.**</span></span> <span data-ttu-id="0cd18-113">使用您用來建立 Windows Media Player 面板的相同技術。</span><span class="sxs-lookup"><span data-stu-id="0cd18-113">Use the same techniques you would use to build a skin for Windows Media Player.</span></span> <span data-ttu-id="0cd18-114">設計框線，以便調整大小 Windows Media Player 不會損毀框線元素的組合。</span><span class="sxs-lookup"><span data-stu-id="0cd18-114">Design the border so that resizing Windows Media Player will not ruin the composition of the border elements.</span></span> <span data-ttu-id="0cd18-115">例如，使用純色或視覺效果做為背景，因為在調整大小 Windows Media Player 時，將會相應縮小。</span><span class="sxs-lookup"><span data-stu-id="0cd18-115">For instance, use a solid color or visualization as a background because these will scale well as Windows Media Player is resized.</span></span>
2.  <span data-ttu-id="0cd18-116">**壓縮框線內容。**</span><span class="sxs-lookup"><span data-stu-id="0cd18-116">**Compress the border contents.**</span></span> <span data-ttu-id="0cd18-117">建立副檔名為 .zip 的壓縮資料夾 () 包含 border 檔案：影像、JScript 檔案，以及具有 wms 副檔名的外觀定義檔。</span><span class="sxs-lookup"><span data-stu-id="0cd18-117">Create a compressed folder (with a .zip file name extension) that contains the border files: images, JScript files, and the skin definition file with a .wms file name extension.</span></span> <span data-ttu-id="0cd18-118">重新命名壓縮檔案，使其副檔名為 wmz。</span><span class="sxs-lookup"><span data-stu-id="0cd18-118">Rename the compressed file so that it has a .wmz file name extension.</span></span>
3.  <span data-ttu-id="0cd18-119">**撰寫 Windows Media 中繼檔。**</span><span class="sxs-lookup"><span data-stu-id="0cd18-119">**Write a Windows Media metafile.**</span></span> <span data-ttu-id="0cd18-120">除非您建立的 Windows Media 中繼檔的副檔名為 **.asx，否則** Windows Media Player 不會載入框線。</span><span class="sxs-lookup"><span data-stu-id="0cd18-120">Windows Media Player will not load the border unless you create a Windows Media metafile with an .asx file name extension that implements the **SKIN** element.</span></span> <span data-ttu-id="0cd18-121">中繼檔也可以用來建立播放清單，以描述套件中所含的內容。</span><span class="sxs-lookup"><span data-stu-id="0cd18-121">The metafile can also be used to create a playlist that describes the content included in the package.</span></span>
4.  <span data-ttu-id="0cd18-122">**組合您的內容。**</span><span class="sxs-lookup"><span data-stu-id="0cd18-122">**Assemble your content.**</span></span> <span data-ttu-id="0cd18-123">將您想要使用的所有檔案放在資料夾中。</span><span class="sxs-lookup"><span data-stu-id="0cd18-123">Put all the files that you want to use into a folder.</span></span> <span data-ttu-id="0cd18-124">這包括音訊檔案、影片檔案、中繼檔和框線定義檔。</span><span class="sxs-lookup"><span data-stu-id="0cd18-124">This includes audio files, video files, metafiles, and border definition files.</span></span>
5.  <span data-ttu-id="0cd18-125">**建立套件。**</span><span class="sxs-lookup"><span data-stu-id="0cd18-125">**Create the package.**</span></span> <span data-ttu-id="0cd18-126">建立副檔名為 .zip 的壓縮資料夾 () ，其中包含 border 檔案、內容檔案和中繼檔。</span><span class="sxs-lookup"><span data-stu-id="0cd18-126">Create a compressed folder (with a .zip file name extension) that contains the border file, content files, and the metafile.</span></span> <span data-ttu-id="0cd18-127">將這個 .zip 檔案的副檔名變更為 wmd 副檔名。</span><span class="sxs-lookup"><span data-stu-id="0cd18-127">Change the file name extension of this .zip file to a .wmd file name extension.</span></span>
6.  <span data-ttu-id="0cd18-128">**將套件張貼至網站。**</span><span class="sxs-lookup"><span data-stu-id="0cd18-128">**Post the package to a website.**</span></span> <span data-ttu-id="0cd18-129">完成的封裝已準備好發佈至網站，並由使用者下載。</span><span class="sxs-lookup"><span data-stu-id="0cd18-129">The completed package is ready to be posted to a website and downloaded by users.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cd18-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="0cd18-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cd18-131">**(淘汰的 Windows Media 下載套件)**</span><span class="sxs-lookup"><span data-stu-id="0cd18-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




