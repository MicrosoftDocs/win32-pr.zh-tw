---
title: 音訊和影片串流
description: 音訊和影片串流
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows Media Format SDK，音訊串流
- Advanced Systems Format (ASF) 、音訊串流
- ASF (Advanced Systems Format) 、音訊串流
- Windows Media Format SDK、影片串流
- Advanced Systems Format (ASF) 、影片串流
- ASF (Advanced 系統格式) 、影片串流
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 音訊串流，關於
- 影片串流，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021379"
---
# <a name="audio-and-video-streams"></a><span data-ttu-id="89e3c-114">音訊和影片串流</span><span class="sxs-lookup"><span data-stu-id="89e3c-114">Audio and Video Streams</span></span>

<span data-ttu-id="89e3c-115">使用 Windows Media 格式 SDK 建立的檔案中最常見的資料流程類型是音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="89e3c-115">The most common types of streams used in files created by using the Windows Media Format SDK are audio and video streams.</span></span> <span data-ttu-id="89e3c-116">音訊和影片資料的數位表示很複雜，而且會佔用海量儲存體。</span><span class="sxs-lookup"><span data-stu-id="89e3c-116">Digital representations of audio and video data are complex and take up large amounts of memory.</span></span> <span data-ttu-id="89e3c-117">在大部分的情況下，音訊和影片都會先壓縮，然後再新增至 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="89e3c-117">Under most circumstances, both audio and video are compressed before being added to an ASF file.</span></span> <span data-ttu-id="89e3c-118">壓縮會使用壓縮程式/解壓縮程式 (編解碼器) 來完成。</span><span class="sxs-lookup"><span data-stu-id="89e3c-118">Compression is accomplished using a compressor/decompressor (codec).</span></span>

<span data-ttu-id="89e3c-119">此 SDK 包含數個 Windows Media 編解碼器，並為數字媒體提供絕佳的品質壓縮。</span><span class="sxs-lookup"><span data-stu-id="89e3c-119">Several Windows Media codecs are included with this SDK, and they provide excellent quality compression for digital media.</span></span> <span data-ttu-id="89e3c-120">如需 Windows Media 編解碼器的詳細資訊，請參閱 [編解碼器功能](codec-features.md)。</span><span class="sxs-lookup"><span data-stu-id="89e3c-120">For more information about the Windows Media codecs, see [Codec Features](codec-features.md).</span></span> <span data-ttu-id="89e3c-121">許多其他編解碼器都可以從各種來源取得。</span><span class="sxs-lookup"><span data-stu-id="89e3c-121">Many other codecs are available from various sources.</span></span> <span data-ttu-id="89e3c-122">您可以在建立 ASF 檔案時使用您喜歡的任何編解碼器，但此 SDK 的物件只會直接支援 Windows Media 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="89e3c-122">You can use whatever codecs you like when creating ASF files, but only the Windows Media codecs are directly supported by the objects of this SDK.</span></span> <span data-ttu-id="89e3c-123">若要使用其他編解碼器，您必須壓縮範例，並將它們以任意資料的形式傳遞至寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="89e3c-123">To use other codecs, you must compress samples and pass them to the writer object as arbitrary data.</span></span>

<span data-ttu-id="89e3c-124">音訊或影片串流與任意資料流程之間最重要的差別在於，包含 Windows Media 音訊或影片資料的資料流程是由 Windows Media Format SDK 的物件所驗證。</span><span class="sxs-lookup"><span data-stu-id="89e3c-124">The most important distinction between audio or video streams and arbitrary streams is that streams containing Windows Media audio or video data are validated by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="89e3c-125">任意的資料流程都不會自動驗證，而且應該檢查您的應用程式是否有完整性。</span><span class="sxs-lookup"><span data-stu-id="89e3c-125">Arbitrary data streams are not validated automatically, and should be checked for integrity by your application.</span></span>

<span data-ttu-id="89e3c-126">音訊或影片資料流程的屬性會在用來建立檔案的設定檔中說明。</span><span class="sxs-lookup"><span data-stu-id="89e3c-126">The properties of an audio or video stream are described in the profile used to create the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89e3c-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="89e3c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89e3c-128">**任意資料流程**</span><span class="sxs-lookup"><span data-stu-id="89e3c-128">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="89e3c-129">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="89e3c-129">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="89e3c-130">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="89e3c-130">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




