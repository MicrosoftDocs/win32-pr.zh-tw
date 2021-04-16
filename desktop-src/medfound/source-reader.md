---
description: 來源讀取器是使用媒體會話和 Microsoft 媒體基礎管線來處理媒體資料的替代方法。
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: 來源讀取程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512548"
---
# <a name="source-reader"></a><span data-ttu-id="77a1c-103">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="77a1c-103">Source Reader</span></span>

<span data-ttu-id="77a1c-104">來源讀取器是使用 [媒體會話](media-session.md) 和 Microsoft 媒體基礎管線來處理媒體資料的替代方法。</span><span class="sxs-lookup"><span data-stu-id="77a1c-104">The Source Reader is an alternative to using the [Media Session](media-session.md) and the Microsoft Media Foundation pipeline to process media data.</span></span>

## <a name="why-use-the-source-reader"></a><span data-ttu-id="77a1c-105">為何要使用來源讀取器？</span><span class="sxs-lookup"><span data-stu-id="77a1c-105">Why Use the Source Reader?</span></span>

<span data-ttu-id="77a1c-106">媒體基礎提供已針對播放優化的管線。</span><span class="sxs-lookup"><span data-stu-id="77a1c-106">Media Foundation provides a pipeline that is optimized for playback.</span></span> <span data-ttu-id="77a1c-107">管線是端對端的，這表示它會處理來自來源的資料流程 (例如影片檔案) 一直到目的地 (例如圖形顯示) 。</span><span class="sxs-lookup"><span data-stu-id="77a1c-107">The pipeline is end-to-end, meaning it handles data flow from the source (such as a video file) all the way to the destination (such as the graphics display).</span></span> <span data-ttu-id="77a1c-108">但是，如果您想要在資料通過管線時讀取或修改資料，您必須撰寫自訂外掛程式。</span><span class="sxs-lookup"><span data-stu-id="77a1c-108">However, if you want to read or modify the data as it goes through the pipeline, you must write a custom plug-in.</span></span> <span data-ttu-id="77a1c-109">這需要對媒體基礎管線有相當深入的瞭解。</span><span class="sxs-lookup"><span data-stu-id="77a1c-109">That requires a fairly deep knowledge of the Media Foundation pipeline.</span></span> <span data-ttu-id="77a1c-110">針對某些工作，建立新外掛程式的負荷會太多。</span><span class="sxs-lookup"><span data-stu-id="77a1c-110">For certain tasks, creating a new plug-in is too much overhead.</span></span> <span data-ttu-id="77a1c-111">當您想要從來源取得未經處理的資料，而不會產生整個管線的額外負荷時，來源讀取器是針對這類情況所設計。</span><span class="sxs-lookup"><span data-stu-id="77a1c-111">The source reader is designed for this type of situation, when you want to get the raw data from a source without the overhead of the entire pipeline.</span></span>

<span data-ttu-id="77a1c-112">來源讀取器會在內部保存媒體來源的指標。</span><span class="sxs-lookup"><span data-stu-id="77a1c-112">Internally, the source reader holds a pointer to a media source.</span></span> <span data-ttu-id="77a1c-113">*媒體來源* 是媒體基礎的物件，可從外部來源（例如媒體檔案或影片捕獲裝置）產生媒體資料。</span><span class="sxs-lookup"><span data-stu-id="77a1c-113">A *media source* is a Media Foundation object that generates media data from an external source, such as a media file or video capture device.</span></span> <span data-ttu-id="77a1c-114">來源讀取器會管理媒體來源的所有方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="77a1c-114">The source reader manages all of the method calls to the media source.</span></span> <span data-ttu-id="77a1c-115"> (如需媒體來源的詳細資訊，請參閱 [媒體來源](media-sources.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="77a1c-115">(For more information about media sources, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="77a1c-116">如果媒體來源提供壓縮的資料，您可以使用來源讀取器將資料解碼。</span><span class="sxs-lookup"><span data-stu-id="77a1c-116">If the media source delivers compressed data, you can use the source reader to decode the data.</span></span> <span data-ttu-id="77a1c-117">在此情況下，來源讀取器將會載入正確的解碼器，並管理媒體來源與解碼器之間的資料流程。</span><span class="sxs-lookup"><span data-stu-id="77a1c-117">In that case, the source reader will load the correct decoder and manage the data flow between the media source and the decoder.</span></span> <span data-ttu-id="77a1c-118">來源讀取器也可以執行一些有限的影片處理：從 YUV 到 RGB-32 的色彩轉換，以及軟體去交錯，不過不建議針對即時影片轉譯進行這些作業。</span><span class="sxs-lookup"><span data-stu-id="77a1c-118">The source reader can also perform some limited video processing: color conversion from YUV to RGB-32, and software deinterlacing, although these operations are not recommended for real-time video rendering.</span></span> <span data-ttu-id="77a1c-119">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="77a1c-119">The following image illustrates this process.</span></span>

![來源讀取器的圖表](images/sourcereader.png)

<span data-ttu-id="77a1c-121">來源讀取器不會將資料傳送至目的地;應用程式會耗用資料。</span><span class="sxs-lookup"><span data-stu-id="77a1c-121">The source reader does not send the data to a destination; it is up to the application to consume the data.</span></span> <span data-ttu-id="77a1c-122">例如，來源讀取器可以讀取影片檔案，但不會將影片轉譯至螢幕。</span><span class="sxs-lookup"><span data-stu-id="77a1c-122">For example, the source reader can read a video file, but it will not render the video to the screen.</span></span> <span data-ttu-id="77a1c-123">此外，來源讀取器不會管理簡報時鐘、處理計時問題，或同步處理影片與音訊。</span><span class="sxs-lookup"><span data-stu-id="77a1c-123">Also, the source reader does not manage a presentation clock, handle timing issues, or synchronize video with audio.</span></span>

<span data-ttu-id="77a1c-124">當下列情況時，請考慮使用來源讀取器：</span><span class="sxs-lookup"><span data-stu-id="77a1c-124">Consider using the source reader when:</span></span>

-   <span data-ttu-id="77a1c-125">您想要從媒體檔案取得資料，而不需要擔心基礎檔結構。</span><span class="sxs-lookup"><span data-stu-id="77a1c-125">You want to get data from a media file without worrying about the underlying file structure.</span></span>
-   <span data-ttu-id="77a1c-126">您想要從音訊或影片捕獲裝置取得資料。</span><span class="sxs-lookup"><span data-stu-id="77a1c-126">You want to get data from an audio or video capture device.</span></span>
-   <span data-ttu-id="77a1c-127">您的資料處理工作不會區分時間，或是您不需要簡報時鐘。</span><span class="sxs-lookup"><span data-stu-id="77a1c-127">Your data-processing tasks are not time sensitive, or you do not require a presentation clock.</span></span>
-   <span data-ttu-id="77a1c-128">您已經有不是以媒體基礎為基礎的媒體管線，而您想要將媒體基礎的媒體來源併入您自己的管線。</span><span class="sxs-lookup"><span data-stu-id="77a1c-128">You already have a media pipeline that is not based on Media Foundation, and you want to incorporate the Media Foundation media sources into your own pipeline.</span></span>

<span data-ttu-id="77a1c-129">在下列情況下，不建議使用來源讀取器：</span><span class="sxs-lookup"><span data-stu-id="77a1c-129">The source reader is not recommended in the following situations:</span></span>

-   <span data-ttu-id="77a1c-130">適用于受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="77a1c-130">For protected content.</span></span> <span data-ttu-id="77a1c-131">來源讀取器不支援 (DRM) 的數位版權管理。</span><span class="sxs-lookup"><span data-stu-id="77a1c-131">The source reader does not support digital rights management (DRM).</span></span>
-   <span data-ttu-id="77a1c-132">如果您在意基礎檔結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="77a1c-132">If you care about the details of the underlying file structure.</span></span> <span data-ttu-id="77a1c-133">來源讀取器會隱藏該類型的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="77a1c-133">The source reader hides that type of detail.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77a1c-134">本節內容</span><span class="sxs-lookup"><span data-stu-id="77a1c-134">In this section</span></span>



| <span data-ttu-id="77a1c-135">主題</span><span class="sxs-lookup"><span data-stu-id="77a1c-135">Topic</span></span>                                                                                                        | <span data-ttu-id="77a1c-136">描述</span><span class="sxs-lookup"><span data-stu-id="77a1c-136">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77a1c-137">使用來源讀取器來處理媒體資料</span><span class="sxs-lookup"><span data-stu-id="77a1c-137">Using the Source Reader to Process Media Data</span></span>](processing-media-data-with-the-source-reader.md)<br/> | <span data-ttu-id="77a1c-138">本主題說明如何使用來源讀取器來處理媒體資料。</span><span class="sxs-lookup"><span data-stu-id="77a1c-138">This topic describes how to use the Source Reader to process media data.</span></span><br/>                                               |
| [<span data-ttu-id="77a1c-139">使用非同步模式的來源讀取器</span><span class="sxs-lookup"><span data-stu-id="77a1c-139">Using the Source Reader in Asynchronous Mode</span></span>](using-the-source-reader-in-asynchronous-mode.md)<br/>  | <span data-ttu-id="77a1c-140">本主題說明如何使用非同步模式的來源讀取器。</span><span class="sxs-lookup"><span data-stu-id="77a1c-140">This topic describes how to use the Source Reader in asynchronous mode.</span></span><br/>                                                |
| [<span data-ttu-id="77a1c-141">教學課程：解碼音訊</span><span class="sxs-lookup"><span data-stu-id="77a1c-141">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)<br/>                                          | <span data-ttu-id="77a1c-142">本教學課程示範如何使用來源讀取器將音訊從媒體檔案解碼，並將音訊寫入 WAVE 檔案。</span><span class="sxs-lookup"><span data-stu-id="77a1c-142">This tutorial shows how to use the Source Reader to decode audio from a media file and write the audio to a WAVE file.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="77a1c-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="77a1c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77a1c-144">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="77a1c-144">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="77a1c-145">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="77a1c-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="77a1c-146">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="77a1c-146">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




