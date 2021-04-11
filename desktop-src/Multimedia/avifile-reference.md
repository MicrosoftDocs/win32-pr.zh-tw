---
title: AVIFile 參考
description: AVIFile 參考
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0291d0ac5864a9b370e79a98fa061770d05bca03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022001"
---
# <a name="avifile-reference"></a><span data-ttu-id="a6daa-103">AVIFile 參考</span><span class="sxs-lookup"><span data-stu-id="a6daa-103">AVIFile Reference</span></span>

<span data-ttu-id="a6daa-104">本節說明使用 AVIFile 服務之應用程式的函式、結構和宏。</span><span class="sxs-lookup"><span data-stu-id="a6daa-104">This section describes the functions, structures, and macros for applications using the AVIFile services.</span></span> <span data-ttu-id="a6daa-105">這些元素的分組方式如下：</span><span class="sxs-lookup"><span data-stu-id="a6daa-105">These elements are grouped as follows:</span></span>

## <a name="avifile-library-operations"></a><span data-ttu-id="a6daa-106">AVIFile 程式庫作業</span><span class="sxs-lookup"><span data-stu-id="a6daa-106">AVIFile Library Operations</span></span>

-   [<span data-ttu-id="a6daa-107">**AVIFileInit**</span><span class="sxs-lookup"><span data-stu-id="a6daa-107">**AVIFileInit**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [<span data-ttu-id="a6daa-108">**AVIFileExit**</span><span class="sxs-lookup"><span data-stu-id="a6daa-108">**AVIFileExit**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a><span data-ttu-id="a6daa-109">開啟和關閉 AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="a6daa-109">Opening and Closing AVI Files</span></span>

-   [<span data-ttu-id="a6daa-110">**AVIFileOpen**</span><span class="sxs-lookup"><span data-stu-id="a6daa-110">**AVIFileOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [<span data-ttu-id="a6daa-111">**AVIFileAddRef**</span><span class="sxs-lookup"><span data-stu-id="a6daa-111">**AVIFileAddRef**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [<span data-ttu-id="a6daa-112">**AVIFileRelease**</span><span class="sxs-lookup"><span data-stu-id="a6daa-112">**AVIFileRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [<span data-ttu-id="a6daa-113">**GetOpenFileNamePreview**</span><span class="sxs-lookup"><span data-stu-id="a6daa-113">**GetOpenFileNamePreview**</span></span>](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a><span data-ttu-id="a6daa-114">從檔案讀取</span><span class="sxs-lookup"><span data-stu-id="a6daa-114">Reading from a File</span></span>

-   [<span data-ttu-id="a6daa-115">**AVIFileInfo**</span><span class="sxs-lookup"><span data-stu-id="a6daa-115">**AVIFileInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [<span data-ttu-id="a6daa-116">**AVIFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="a6daa-116">**AVIFILEINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [<span data-ttu-id="a6daa-117">**AVIFileReadData**</span><span class="sxs-lookup"><span data-stu-id="a6daa-117">**AVIFileReadData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a><span data-ttu-id="a6daa-118">寫入檔案</span><span class="sxs-lookup"><span data-stu-id="a6daa-118">Writing to a File</span></span>

-   [<span data-ttu-id="a6daa-119">**AVIFileWriteData**</span><span class="sxs-lookup"><span data-stu-id="a6daa-119">**AVIFileWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a><span data-ttu-id="a6daa-120">使用剪貼簿</span><span class="sxs-lookup"><span data-stu-id="a6daa-120">Using the Clipboard</span></span>

-   [<span data-ttu-id="a6daa-121">**AVIPutFileOnClipboard**</span><span class="sxs-lookup"><span data-stu-id="a6daa-121">**AVIPutFileOnClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [<span data-ttu-id="a6daa-122">**AVIGetFromClipboard**</span><span class="sxs-lookup"><span data-stu-id="a6daa-122">**AVIGetFromClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [<span data-ttu-id="a6daa-123">**AVIClearClipboard**</span><span class="sxs-lookup"><span data-stu-id="a6daa-123">**AVIClearClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a><span data-ttu-id="a6daa-124">開啟和關閉資料流程</span><span class="sxs-lookup"><span data-stu-id="a6daa-124">Opening and Closing Streams</span></span>

-   [<span data-ttu-id="a6daa-125">**AVIFileGetStream**</span><span class="sxs-lookup"><span data-stu-id="a6daa-125">**AVIFileGetStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [<span data-ttu-id="a6daa-126">**AVIStreamOpenFromFile**</span><span class="sxs-lookup"><span data-stu-id="a6daa-126">**AVIStreamOpenFromFile**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [<span data-ttu-id="a6daa-127">**AVIStreamAddRef**</span><span class="sxs-lookup"><span data-stu-id="a6daa-127">**AVIStreamAddRef**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [<span data-ttu-id="a6daa-128">**AVIStreamRelease**</span><span class="sxs-lookup"><span data-stu-id="a6daa-128">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a><span data-ttu-id="a6daa-129">讀取資料流程資訊</span><span class="sxs-lookup"><span data-stu-id="a6daa-129">Reading Stream Information</span></span>

-   [<span data-ttu-id="a6daa-130">**AVISTREAMINFO**</span><span class="sxs-lookup"><span data-stu-id="a6daa-130">**AVISTREAMINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [<span data-ttu-id="a6daa-131">**AVIStreamReadData**</span><span class="sxs-lookup"><span data-stu-id="a6daa-131">**AVIStreamReadData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [<span data-ttu-id="a6daa-132">**AVIStreamDataSize**</span><span class="sxs-lookup"><span data-stu-id="a6daa-132">**AVIStreamDataSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [<span data-ttu-id="a6daa-133">**AVIStreamReadFormat**</span><span class="sxs-lookup"><span data-stu-id="a6daa-133">**AVIStreamReadFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [<span data-ttu-id="a6daa-134">**AVIStreamFormatSize**</span><span class="sxs-lookup"><span data-stu-id="a6daa-134">**AVIStreamFormatSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [<span data-ttu-id="a6daa-135">**AVIStreamRead**</span><span class="sxs-lookup"><span data-stu-id="a6daa-135">**AVIStreamRead**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [<span data-ttu-id="a6daa-136">**AVIStreamSampleSize**</span><span class="sxs-lookup"><span data-stu-id="a6daa-136">**AVIStreamSampleSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [<span data-ttu-id="a6daa-137">**AVIStreamBeginStreaming**</span><span class="sxs-lookup"><span data-stu-id="a6daa-137">**AVIStreamBeginStreaming**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [<span data-ttu-id="a6daa-138">**AVIStreamEndStreaming**</span><span class="sxs-lookup"><span data-stu-id="a6daa-138">**AVIStreamEndStreaming**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a><span data-ttu-id="a6daa-139">在資料流程中解壓縮影片資料</span><span class="sxs-lookup"><span data-stu-id="a6daa-139">Decompressing Video Data in a Stream</span></span>

-   [<span data-ttu-id="a6daa-140">**AVIStreamGetFrameOpen**</span><span class="sxs-lookup"><span data-stu-id="a6daa-140">**AVIStreamGetFrameOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [<span data-ttu-id="a6daa-141">**AVIStreamGetFrame**</span><span class="sxs-lookup"><span data-stu-id="a6daa-141">**AVIStreamGetFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [<span data-ttu-id="a6daa-142">**AVIStreamGetFrameClose**</span><span class="sxs-lookup"><span data-stu-id="a6daa-142">**AVIStreamGetFrameClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a><span data-ttu-id="a6daa-143">從現有的資料流程建立檔案</span><span class="sxs-lookup"><span data-stu-id="a6daa-143">Creating a File from Existing Streams</span></span>

-   [<span data-ttu-id="a6daa-144">**AVISave**</span><span class="sxs-lookup"><span data-stu-id="a6daa-144">**AVISave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [<span data-ttu-id="a6daa-145">**AVISaveV**</span><span class="sxs-lookup"><span data-stu-id="a6daa-145">**AVISaveV**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [<span data-ttu-id="a6daa-146">**AVISaveOptions**</span><span class="sxs-lookup"><span data-stu-id="a6daa-146">**AVISaveOptions**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [<span data-ttu-id="a6daa-147">**GetSaveFileNamePreview**</span><span class="sxs-lookup"><span data-stu-id="a6daa-147">**GetSaveFileNamePreview**</span></span>](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [<span data-ttu-id="a6daa-148">**AVIMakeFileFromStreams**</span><span class="sxs-lookup"><span data-stu-id="a6daa-148">**AVIMakeFileFromStreams**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a><span data-ttu-id="a6daa-149">撰寫個別資料流程</span><span class="sxs-lookup"><span data-stu-id="a6daa-149">Writing Individual Streams</span></span>

-   [<span data-ttu-id="a6daa-150">**AVIFileCreateStream**</span><span class="sxs-lookup"><span data-stu-id="a6daa-150">**AVIFileCreateStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [<span data-ttu-id="a6daa-151">**AVIStreamSetFormat**</span><span class="sxs-lookup"><span data-stu-id="a6daa-151">**AVIStreamSetFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [<span data-ttu-id="a6daa-152">**AVIStreamWrite**</span><span class="sxs-lookup"><span data-stu-id="a6daa-152">**AVIStreamWrite**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [<span data-ttu-id="a6daa-153">**AVIFileWriteData**</span><span class="sxs-lookup"><span data-stu-id="a6daa-153">**AVIFileWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [<span data-ttu-id="a6daa-154">**AVIStreamWriteData**</span><span class="sxs-lookup"><span data-stu-id="a6daa-154">**AVIStreamWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [<span data-ttu-id="a6daa-155">**AVIStreamRelease**</span><span class="sxs-lookup"><span data-stu-id="a6daa-155">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a><span data-ttu-id="a6daa-156">尋找資料流程中的開始位置</span><span class="sxs-lookup"><span data-stu-id="a6daa-156">Finding the Starting Position in a Stream</span></span>

-   [<span data-ttu-id="a6daa-157">**AVIStreamStart**</span><span class="sxs-lookup"><span data-stu-id="a6daa-157">**AVIStreamStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [<span data-ttu-id="a6daa-158">**AVIStreamStartTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-158">**AVIStreamStartTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [<span data-ttu-id="a6daa-159">**AVIStreamLength**</span><span class="sxs-lookup"><span data-stu-id="a6daa-159">**AVIStreamLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [<span data-ttu-id="a6daa-160">**AVIStreamLengthTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-160">**AVIStreamLengthTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [<span data-ttu-id="a6daa-161">**AVIStreamFindSample**</span><span class="sxs-lookup"><span data-stu-id="a6daa-161">**AVIStreamFindSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [<span data-ttu-id="a6daa-162">**AVIStreamEnd**</span><span class="sxs-lookup"><span data-stu-id="a6daa-162">**AVIStreamEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [<span data-ttu-id="a6daa-163">**AVIStreamEndTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-163">**AVIStreamEndTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a><span data-ttu-id="a6daa-164">尋找範例和主要畫面格</span><span class="sxs-lookup"><span data-stu-id="a6daa-164">Finding Sample and Key Frames</span></span>

-   [<span data-ttu-id="a6daa-165">**AVIStreamFindSample**</span><span class="sxs-lookup"><span data-stu-id="a6daa-165">**AVIStreamFindSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [<span data-ttu-id="a6daa-166">**AVIStreamIsKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="a6daa-166">**AVIStreamIsKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [<span data-ttu-id="a6daa-167">**AVIStreamNearestKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="a6daa-167">**AVIStreamNearestKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [<span data-ttu-id="a6daa-168">**AVIStreamNearestKeyFrameTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-168">**AVIStreamNearestKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [<span data-ttu-id="a6daa-169">**AVIStreamNearestSample**</span><span class="sxs-lookup"><span data-stu-id="a6daa-169">**AVIStreamNearestSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [<span data-ttu-id="a6daa-170">**AVIStreamNearestSampleTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-170">**AVIStreamNearestSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [<span data-ttu-id="a6daa-171">**AVIStreamNextKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="a6daa-171">**AVIStreamNextKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [<span data-ttu-id="a6daa-172">**AVIStreamNextKeyFrameTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-172">**AVIStreamNextKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [<span data-ttu-id="a6daa-173">**AVIStreamNextSample**</span><span class="sxs-lookup"><span data-stu-id="a6daa-173">**AVIStreamNextSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [<span data-ttu-id="a6daa-174">**AVIStreamNextSampleTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-174">**AVIStreamNextSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [<span data-ttu-id="a6daa-175">**AVIStreamPrevKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="a6daa-175">**AVIStreamPrevKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [<span data-ttu-id="a6daa-176">**AVIStreamPrevKeyFrameTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-176">**AVIStreamPrevKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [<span data-ttu-id="a6daa-177">**AVIStreamPrevSample**</span><span class="sxs-lookup"><span data-stu-id="a6daa-177">**AVIStreamPrevSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [<span data-ttu-id="a6daa-178">**AVIStreamPrevSampleTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-178">**AVIStreamPrevSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [<span data-ttu-id="a6daa-179">**AVIStreamSampleToSample**</span><span class="sxs-lookup"><span data-stu-id="a6daa-179">**AVIStreamSampleToSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a><span data-ttu-id="a6daa-180">在範例和時間之間切換</span><span class="sxs-lookup"><span data-stu-id="a6daa-180">Switching Between Samples and Time</span></span>

-   [<span data-ttu-id="a6daa-181">**AVIStreamSampleToTime**</span><span class="sxs-lookup"><span data-stu-id="a6daa-181">**AVIStreamSampleToTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [<span data-ttu-id="a6daa-182">**AVIStreamTimeToSample**</span><span class="sxs-lookup"><span data-stu-id="a6daa-182">**AVIStreamTimeToSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a><span data-ttu-id="a6daa-183">建立暫存資料流程</span><span class="sxs-lookup"><span data-stu-id="a6daa-183">Creating Temporary Streams</span></span>

-   [<span data-ttu-id="a6daa-184">**AVIStreamCreate**</span><span class="sxs-lookup"><span data-stu-id="a6daa-184">**AVIStreamCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [<span data-ttu-id="a6daa-185">**AVIMakeCompressedStream**</span><span class="sxs-lookup"><span data-stu-id="a6daa-185">**AVIMakeCompressedStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [<span data-ttu-id="a6daa-186">**AVIStreamRelease**</span><span class="sxs-lookup"><span data-stu-id="a6daa-186">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a><span data-ttu-id="a6daa-187">編輯 AVI 資料流程</span><span class="sxs-lookup"><span data-stu-id="a6daa-187">Editing AVI Streams</span></span>

-   [<span data-ttu-id="a6daa-188">**CreateEditableStream**</span><span class="sxs-lookup"><span data-stu-id="a6daa-188">**CreateEditableStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [<span data-ttu-id="a6daa-189">**EditStreamCut**</span><span class="sxs-lookup"><span data-stu-id="a6daa-189">**EditStreamCut**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [<span data-ttu-id="a6daa-190">**EditStreamCopy**</span><span class="sxs-lookup"><span data-stu-id="a6daa-190">**EditStreamCopy**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [<span data-ttu-id="a6daa-191">**EditStreamPaste**</span><span class="sxs-lookup"><span data-stu-id="a6daa-191">**EditStreamPaste**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [<span data-ttu-id="a6daa-192">**EditStreamClone**</span><span class="sxs-lookup"><span data-stu-id="a6daa-192">**EditStreamClone**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [<span data-ttu-id="a6daa-193">**EditStreamSetInfo**</span><span class="sxs-lookup"><span data-stu-id="a6daa-193">**EditStreamSetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [<span data-ttu-id="a6daa-194">**EditStreamSetName**</span><span class="sxs-lookup"><span data-stu-id="a6daa-194">**EditStreamSetName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a><span data-ttu-id="a6daa-195">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6daa-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6daa-196">AVIFile 函式和宏</span><span class="sxs-lookup"><span data-stu-id="a6daa-196">AVIFile Functions and Macros</span></span>](avifile-functions-and-macros.md)
</dt> </dl>

 

 




