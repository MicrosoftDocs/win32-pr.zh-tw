---
title: 副檔名
description: 副檔名
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
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
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965814"
---
# <a name="file-name-extensions"></a><span data-ttu-id="98f8a-109">副檔名</span><span class="sxs-lookup"><span data-stu-id="98f8a-109">File Name Extensions</span></span>

<span data-ttu-id="98f8a-110">使用 Windows Media 中繼檔的副檔名時，有特定的指導方針。</span><span class="sxs-lookup"><span data-stu-id="98f8a-110">There are specific guidelines for the use of file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="98f8a-111">Windows Media 中繼檔名稱延伸模組是用來識別不同類型的 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="98f8a-111">Windows Media metafile name extensions are used to identify the different types of Windows Media files.</span></span> <span data-ttu-id="98f8a-112">副檔名可提供獨立軟體廠商 (ISV) 包含使用特定延伸模組之應用程式轉譯需求的相關資訊，並讓內容作者以一般類型的媒體播放機為目標。</span><span class="sxs-lookup"><span data-stu-id="98f8a-112">A file name extension provides an Independent Software Vendor (ISV) with information about the rendering requirements of an application that uses a particular extension, and enables content authors to target general types of media players.</span></span>

<span data-ttu-id="98f8a-113">下表列出檔案名延伸指導方針。</span><span class="sxs-lookup"><span data-stu-id="98f8a-113">The file name extension guidelines are listed in the following table.</span></span> <span data-ttu-id="98f8a-114">建議您將檔案標頭中的檔案 MIME 類型用於檔案類型識別。</span><span class="sxs-lookup"><span data-stu-id="98f8a-114">It is recommended that a file's MIME type, located in the file header, be used for file-type identification.</span></span>



| <span data-ttu-id="98f8a-115">副檔名</span><span class="sxs-lookup"><span data-stu-id="98f8a-115">File name extension</span></span> | <span data-ttu-id="98f8a-116">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="98f8a-116">MIME type</span></span>      | <span data-ttu-id="98f8a-117">檔案內容</span><span class="sxs-lookup"><span data-stu-id="98f8a-117">File content</span></span>                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f8a-118">.wma</span><span class="sxs-lookup"><span data-stu-id="98f8a-118">.wma</span></span>                | <span data-ttu-id="98f8a-119">音訊/x-ms-wma</span><span class="sxs-lookup"><span data-stu-id="98f8a-119">audio/x-ms-wma</span></span> | <span data-ttu-id="98f8a-120">只有音訊內容的 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="98f8a-120">Windows Media file with audio content only.</span></span> <span data-ttu-id="98f8a-121">通常用來下載及播放檔案，或串流內容。</span><span class="sxs-lookup"><span data-stu-id="98f8a-121">Typically used to download and play files or to stream content.</span></span>                                                                             |
| <span data-ttu-id="98f8a-122">.wmv</span><span class="sxs-lookup"><span data-stu-id="98f8a-122">.wmv</span></span>                | <span data-ttu-id="98f8a-123">影片/x-ms-wmv</span><span class="sxs-lookup"><span data-stu-id="98f8a-123">video/x-ms-wmv</span></span> | <span data-ttu-id="98f8a-124">具有音訊和/或影片內容的 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="98f8a-124">Windows Media file with audio and/or video content.</span></span> <span data-ttu-id="98f8a-125">通常用來下載及播放檔案，或串流內容。</span><span class="sxs-lookup"><span data-stu-id="98f8a-125">Typically used to download and play files or to stream content.</span></span>                                                                     |
| <span data-ttu-id="98f8a-126">.asf</span><span class="sxs-lookup"><span data-stu-id="98f8a-126">.asf</span></span>                | <span data-ttu-id="98f8a-127">video/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="98f8a-127">video/x-ms-asf</span></span> | <span data-ttu-id="98f8a-128">舊版內容。</span><span class="sxs-lookup"><span data-stu-id="98f8a-128">Legacy content.</span></span> <span data-ttu-id="98f8a-129">通常用來下載及播放檔案，或串流內容。</span><span class="sxs-lookup"><span data-stu-id="98f8a-129">Typically used to download and play files or to stream content.</span></span> <span data-ttu-id="98f8a-130">可能包含音訊和/或影片內容。</span><span class="sxs-lookup"><span data-stu-id="98f8a-130">May contain audio and/or video content.</span></span> <span data-ttu-id="98f8a-131">通常用來下載及播放檔案，或串流內容。</span><span class="sxs-lookup"><span data-stu-id="98f8a-131">Typically used to download and play files or to stream content.</span></span> |
| <span data-ttu-id="98f8a-132">.wm</span><span class="sxs-lookup"><span data-stu-id="98f8a-132">.wm</span></span>                 | <span data-ttu-id="98f8a-133">影片/x-ms-wm</span><span class="sxs-lookup"><span data-stu-id="98f8a-133">video/x-ms-wm</span></span>  | <span data-ttu-id="98f8a-134">保留</span><span class="sxs-lookup"><span data-stu-id="98f8a-134">Reserved</span></span>                                                                                                                                                                                |
| <span data-ttu-id="98f8a-135">. 地板蠟</span><span class="sxs-lookup"><span data-stu-id="98f8a-135">.wax</span></span>                | <span data-ttu-id="98f8a-136">音訊/x-地板蠟</span><span class="sxs-lookup"><span data-stu-id="98f8a-136">audio/x-ms-wax</span></span> | <span data-ttu-id="98f8a-137">參考具有 .asf、.wma 或副檔名為地板蠟之 Windows Media 檔案的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="98f8a-137">Metafiles that reference Windows Media files with .asf, .wma, or .wax file name extensions.</span></span>                                                                                             |
| <span data-ttu-id="98f8a-138">. 300k.wvx</span><span class="sxs-lookup"><span data-stu-id="98f8a-138">.wvx</span></span>                | <span data-ttu-id="98f8a-139">影片/x-300k.wvx</span><span class="sxs-lookup"><span data-stu-id="98f8a-139">video/x-ms-wvx</span></span> | <span data-ttu-id="98f8a-140">參考包含 .wma、.wmv、. 300k.wvx 或. 地板蠟副檔名之 Windows Media 檔案的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="98f8a-140">Metafiles that reference Windows Media files with .wma, .wmv, .wvx, or .wax file name extensions.</span></span>                                                                                       |
| <span data-ttu-id="98f8a-141">.asx</span><span class="sxs-lookup"><span data-stu-id="98f8a-141">.asx</span></span>                | <span data-ttu-id="98f8a-142">video/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="98f8a-142">video/x-ms-asf</span></span> | <span data-ttu-id="98f8a-143">參考包含 .wma、. 地板蠟、.wmv、. 300k.wvx、.asf 或 .asx 副檔名之 Windows Media 檔案的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="98f8a-143">Metafiles that reference Windows Media files with .wma, .wax, .wmv, .wvx, .asf, or .asx file name extensions.</span></span>                                                                           |
| <span data-ttu-id="98f8a-144">.wmx</span><span class="sxs-lookup"><span data-stu-id="98f8a-144">.wmx</span></span>                | <span data-ttu-id="98f8a-145">影片/x-300k.wvx</span><span class="sxs-lookup"><span data-stu-id="98f8a-145">video/x-ms-wvx</span></span> | <span data-ttu-id="98f8a-146">保留的。</span><span class="sxs-lookup"><span data-stu-id="98f8a-146">Reserved.</span></span>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="98f8a-147">備註</span><span class="sxs-lookup"><span data-stu-id="98f8a-147">Remarks</span></span>

<span data-ttu-id="98f8a-148">轉譯 Windows Media 檔案的任何應用程式都必須支援腳本和數位版權管理 (DRM) 。</span><span class="sxs-lookup"><span data-stu-id="98f8a-148">Scripting and digital rights management (DRM) must be supported by any application that renders Windows Media files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98f8a-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="98f8a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98f8a-150">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="98f8a-150">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="98f8a-151">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="98f8a-151">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="98f8a-152">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="98f8a-152">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 




