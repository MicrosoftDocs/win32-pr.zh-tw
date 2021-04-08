---
title: 中繼檔延伸指導方針
description: 中繼檔延伸指導方針
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Windows Media 中繼檔，擴充功能
- Windows Media 中繼檔，副檔名
- 中繼檔，擴充功能
- 中繼檔，副檔名
- Windows Media，中繼檔
- Windows Media 中繼檔的副檔名
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022022"
---
# <a name="metafile-extension-guidelines"></a><span data-ttu-id="49e9e-109">中繼檔延伸指導方針</span><span class="sxs-lookup"><span data-stu-id="49e9e-109">Metafile Extension Guidelines</span></span>

<span data-ttu-id="49e9e-110">副檔名可提供獨立軟體廠商 (ISV) ，其中包含使用延伸模組之應用程式轉譯需求的相關資訊，並可讓內容作者以一般類型的播放程式為目標。</span><span class="sxs-lookup"><span data-stu-id="49e9e-110">A file name extension provides an independent software vendor (ISV) with information about the rendering requirements of an application that uses the extension, and enables content authors to target general types of players.</span></span>

<span data-ttu-id="49e9e-111">Windows Media 中繼檔副檔名用來識別中繼檔所參考之 Windows Media 檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="49e9e-111">Windows Media metafile name extensions are used to identify the format of the Windows Media files that a metafile references.</span></span> <span data-ttu-id="49e9e-112">具有. 地板蠟、. 300k.wvx 或 .asx 副檔名的 Windows Media 中繼檔會分別參考副檔名為 .wma、.wmv 和 .asf 的檔案。</span><span class="sxs-lookup"><span data-stu-id="49e9e-112">Windows Media metafiles with .wax, .wvx, or .asx extensions reference files with .wma, .wmv, and .asf extensions, respectively.</span></span> <span data-ttu-id="49e9e-113">所有的中繼檔（不論使用的副檔名為何）都有指定 **version** 屬性之檔案開頭的 **ASX** 元素標記。</span><span class="sxs-lookup"><span data-stu-id="49e9e-113">All metafiles, regardless of the file name extension used, have the **ASX** element tag at the beginning of the file with the **version** attribute specified.</span></span>

<span data-ttu-id="49e9e-114">下表顯示每種類型的中繼檔副檔名所參考的媒體檔案類型。</span><span class="sxs-lookup"><span data-stu-id="49e9e-114">The following table shows the media file types referenced by each type of metafile file name extension.</span></span> <span data-ttu-id="49e9e-115">資料行列出媒體副檔名，資料列會列出中繼檔名稱延伸。</span><span class="sxs-lookup"><span data-stu-id="49e9e-115">The columns list media file name extensions, the rows list metafile name extensions.</span></span> <span data-ttu-id="49e9e-116">資料行中的 X 表示特定的中繼檔副檔名可以參考的媒體檔案類型。</span><span class="sxs-lookup"><span data-stu-id="49e9e-116">An X in a column indicates a media file type that can be referenced by a particular metafile file name extension.</span></span>



| <span data-ttu-id="49e9e-117">分機</span><span class="sxs-lookup"><span data-stu-id="49e9e-117">Extension</span></span> | <span data-ttu-id="49e9e-118">.asf</span><span class="sxs-lookup"><span data-stu-id="49e9e-118">.asf</span></span> | <span data-ttu-id="49e9e-119">.wma</span><span class="sxs-lookup"><span data-stu-id="49e9e-119">.wma</span></span> | <span data-ttu-id="49e9e-120">.wmv</span><span class="sxs-lookup"><span data-stu-id="49e9e-120">.wmv</span></span> |
|-----------|------|------|------|
| <span data-ttu-id="49e9e-121">. 300k.wvx</span><span class="sxs-lookup"><span data-stu-id="49e9e-121">.wvx</span></span>      | <span data-ttu-id="49e9e-122">X</span><span class="sxs-lookup"><span data-stu-id="49e9e-122">X</span></span>    | <span data-ttu-id="49e9e-123">X</span><span class="sxs-lookup"><span data-stu-id="49e9e-123">X</span></span>    | <span data-ttu-id="49e9e-124">X</span><span class="sxs-lookup"><span data-stu-id="49e9e-124">X</span></span>    |
| <span data-ttu-id="49e9e-125">. 地板蠟</span><span class="sxs-lookup"><span data-stu-id="49e9e-125">.wax</span></span>      | <span data-ttu-id="49e9e-126">X</span><span class="sxs-lookup"><span data-stu-id="49e9e-126">X</span></span>    | <span data-ttu-id="49e9e-127">X</span><span class="sxs-lookup"><span data-stu-id="49e9e-127">X</span></span>    |      |
| <span data-ttu-id="49e9e-128">.asx</span><span class="sxs-lookup"><span data-stu-id="49e9e-128">.asx</span></span>      | <span data-ttu-id="49e9e-129">X</span><span class="sxs-lookup"><span data-stu-id="49e9e-129">X</span></span>    |      |      |



 

## <a name="related-topics"></a><span data-ttu-id="49e9e-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="49e9e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49e9e-131">**副檔名**</span><span class="sxs-lookup"><span data-stu-id="49e9e-131">**File Name Extensions**</span></span>](file-name-extensions.md)
</dt> <dt>

[<span data-ttu-id="49e9e-132">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="49e9e-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="49e9e-133">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="49e9e-133">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




