---
description: 您可以使用 MFTrace，藉由指定關鍵字清單來篩選追蹤結果。
ms.assetid: e7c382cb-94ac-4f90-a3dd-32f94c538396
title: MFTrace 關鍵字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d18a91aede8692209b9d5b7a2759c460e44043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114384"
---
# <a name="mftrace-keywords"></a><span data-ttu-id="302d9-103">MFTrace 關鍵字</span><span class="sxs-lookup"><span data-stu-id="302d9-103">MFTrace Keywords</span></span>

<span data-ttu-id="302d9-104">您可以使用 [MFTrace](mftrace.md)，藉由指定關鍵字清單來篩選追蹤結果。</span><span class="sxs-lookup"><span data-stu-id="302d9-104">Using [MFTrace](mftrace.md), you can filter the trace results by specifying a list of keywords.</span></span> <span data-ttu-id="302d9-105">在命令列上，使用 **-k** 命令列引數。</span><span class="sxs-lookup"><span data-stu-id="302d9-105">At the command line, use the **-k** command-line argument.</span></span> <span data-ttu-id="302d9-106">或者，在設定檔中指定 [**關鍵字**](keyword.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="302d9-106">Alternatively, specify the [**keyword**](keyword.md) element in the configuration file.</span></span> <span data-ttu-id="302d9-107">如需詳細資訊，請參閱 [使用 MFTrace](using-mftrace.md)。</span><span class="sxs-lookup"><span data-stu-id="302d9-107">For more information, see [Using MFTrace](using-mftrace.md).</span></span>

<span data-ttu-id="302d9-108">MFTrace 支援下列關鍵字。</span><span class="sxs-lookup"><span data-stu-id="302d9-108">MFTrace supports the following keywords.</span></span> <span data-ttu-id="302d9-109">大部分是指特定的介面或程式庫匯出。</span><span class="sxs-lookup"><span data-stu-id="302d9-109">Most refer to particular interfaces or library exports.</span></span>

-   <span data-ttu-id="302d9-110">"All"</span><span class="sxs-lookup"><span data-stu-id="302d9-110">"All"</span></span>
-   <span data-ttu-id="302d9-111">情況</span><span class="sxs-lookup"><span data-stu-id="302d9-111">"Default"</span></span>
-   <span data-ttu-id="302d9-112">繞道</span><span class="sxs-lookup"><span data-stu-id="302d9-112">"Detours"</span></span>
-   <span data-ttu-id="302d9-113">"IFilterGraph"</span><span class="sxs-lookup"><span data-stu-id="302d9-113">"IFilterGraph"</span></span>
-   <span data-ttu-id="302d9-114">"IGraphBuilder"</span><span class="sxs-lookup"><span data-stu-id="302d9-114">"IGraphBuilder"</span></span>
-   <span data-ttu-id="302d9-115">"IMediaControl"</span><span class="sxs-lookup"><span data-stu-id="302d9-115">"IMediaControl"</span></span>
-   <span data-ttu-id="302d9-116">"IMediaObject"</span><span class="sxs-lookup"><span data-stu-id="302d9-116">"IMediaObject"</span></span>
-   <span data-ttu-id="302d9-117">"IMemInputPin"</span><span class="sxs-lookup"><span data-stu-id="302d9-117">"IMemInputPin"</span></span>
-   <span data-ttu-id="302d9-118">"IMFActivate"</span><span class="sxs-lookup"><span data-stu-id="302d9-118">"IMFActivate"</span></span>
-   <span data-ttu-id="302d9-119">"IMFAttributes"</span><span class="sxs-lookup"><span data-stu-id="302d9-119">"IMFAttributes"</span></span>
-   <span data-ttu-id="302d9-120">"IMFByteStream"</span><span class="sxs-lookup"><span data-stu-id="302d9-120">"IMFByteStream"</span></span>
-   <span data-ttu-id="302d9-121">"IMFByteStreamHandler"</span><span class="sxs-lookup"><span data-stu-id="302d9-121">"IMFByteStreamHandler"</span></span>
-   <span data-ttu-id="302d9-122">"IMFClock"</span><span class="sxs-lookup"><span data-stu-id="302d9-122">"IMFClock"</span></span>
-   <span data-ttu-id="302d9-123">"IMFMediaEventGenerator"</span><span class="sxs-lookup"><span data-stu-id="302d9-123">"IMFMediaEventGenerator"</span></span>
-   <span data-ttu-id="302d9-124">"IMFMediaSession"</span><span class="sxs-lookup"><span data-stu-id="302d9-124">"IMFMediaSession"</span></span>
-   <span data-ttu-id="302d9-125">"IMFMediaSink"</span><span class="sxs-lookup"><span data-stu-id="302d9-125">"IMFMediaSink"</span></span>
-   <span data-ttu-id="302d9-126">"IMFMediaSource"</span><span class="sxs-lookup"><span data-stu-id="302d9-126">"IMFMediaSource"</span></span>
-   <span data-ttu-id="302d9-127">"IMFMediaStream"</span><span class="sxs-lookup"><span data-stu-id="302d9-127">"IMFMediaStream"</span></span>
-   <span data-ttu-id="302d9-128">"IMFPMediaItem"</span><span class="sxs-lookup"><span data-stu-id="302d9-128">"IMFPMediaItem"</span></span>
-   <span data-ttu-id="302d9-129">"IMFPMediaPlayer"</span><span class="sxs-lookup"><span data-stu-id="302d9-129">"IMFPMediaPlayer"</span></span>
-   <span data-ttu-id="302d9-130">"IMFPMediaPlayerCallback"</span><span class="sxs-lookup"><span data-stu-id="302d9-130">"IMFPMediaPlayerCallback"</span></span>
-   <span data-ttu-id="302d9-131">"IMFPresentationClock"</span><span class="sxs-lookup"><span data-stu-id="302d9-131">"IMFPresentationClock"</span></span>
-   <span data-ttu-id="302d9-132">"IMFQualityAdvise"</span><span class="sxs-lookup"><span data-stu-id="302d9-132">"IMFQualityAdvise"</span></span>
-   <span data-ttu-id="302d9-133">"IMFQualityAdvise2"</span><span class="sxs-lookup"><span data-stu-id="302d9-133">"IMFQualityAdvise2"</span></span>
-   <span data-ttu-id="302d9-134">"IMFQualityManager"</span><span class="sxs-lookup"><span data-stu-id="302d9-134">"IMFQualityManager"</span></span>
-   <span data-ttu-id="302d9-135">"IMFReadWriteClassFactory"</span><span class="sxs-lookup"><span data-stu-id="302d9-135">"IMFReadWriteClassFactory"</span></span>
-   <span data-ttu-id="302d9-136">"IMFSample"</span><span class="sxs-lookup"><span data-stu-id="302d9-136">"IMFSample"</span></span>
-   <span data-ttu-id="302d9-137">"IMFSchemeHandler"</span><span class="sxs-lookup"><span data-stu-id="302d9-137">"IMFSchemeHandler"</span></span>
-   <span data-ttu-id="302d9-138">"IMFSinkWriter"</span><span class="sxs-lookup"><span data-stu-id="302d9-138">"IMFSinkWriter"</span></span>
-   <span data-ttu-id="302d9-139">"IMFSourceReader"</span><span class="sxs-lookup"><span data-stu-id="302d9-139">"IMFSourceReader"</span></span>
-   <span data-ttu-id="302d9-140">"IMFSourceReaderCallback"</span><span class="sxs-lookup"><span data-stu-id="302d9-140">"IMFSourceReaderCallback"</span></span>
-   <span data-ttu-id="302d9-141">"IMFSourceResolver"</span><span class="sxs-lookup"><span data-stu-id="302d9-141">"IMFSourceResolver"</span></span>
-   <span data-ttu-id="302d9-142">"IMFStreamSink"</span><span class="sxs-lookup"><span data-stu-id="302d9-142">"IMFStreamSink"</span></span>
-   <span data-ttu-id="302d9-143">"IMFTopoLoader"</span><span class="sxs-lookup"><span data-stu-id="302d9-143">"IMFTopoLoader"</span></span>
-   <span data-ttu-id="302d9-144">"IMFTopology"</span><span class="sxs-lookup"><span data-stu-id="302d9-144">"IMFTopology"</span></span>
-   <span data-ttu-id="302d9-145">"IMFTopologyNode"</span><span class="sxs-lookup"><span data-stu-id="302d9-145">"IMFTopologyNode"</span></span>
-   <span data-ttu-id="302d9-146">"IMFTransform"</span><span class="sxs-lookup"><span data-stu-id="302d9-146">"IMFTransform"</span></span>
-   <span data-ttu-id="302d9-147">"IWMReader"</span><span class="sxs-lookup"><span data-stu-id="302d9-147">"IWMReader"</span></span>
-   <span data-ttu-id="302d9-148">"Kernel32Export"</span><span class="sxs-lookup"><span data-stu-id="302d9-148">"Kernel32Export"</span></span>
-   <span data-ttu-id="302d9-149">"MFExport"</span><span class="sxs-lookup"><span data-stu-id="302d9-149">"MFExport"</span></span>
-   <span data-ttu-id="302d9-150">"MFPlatExport"</span><span class="sxs-lookup"><span data-stu-id="302d9-150">"MFPlatExport"</span></span>
-   <span data-ttu-id="302d9-151">"MFPlayExport"</span><span class="sxs-lookup"><span data-stu-id="302d9-151">"MFPlayExport"</span></span>
-   <span data-ttu-id="302d9-152">"MFPublic"</span><span class="sxs-lookup"><span data-stu-id="302d9-152">"MFPublic"</span></span>
-   <span data-ttu-id="302d9-153">"MFReadWriteExport"</span><span class="sxs-lookup"><span data-stu-id="302d9-153">"MFReadWriteExport"</span></span>
-   <span data-ttu-id="302d9-154">"Ole32Export"</span><span class="sxs-lookup"><span data-stu-id="302d9-154">"Ole32Export"</span></span>
-   <span data-ttu-id="302d9-155">"wmvCoreExport"</span><span class="sxs-lookup"><span data-stu-id="302d9-155">"wmvCoreExport"</span></span>

## <a name="related-topics"></a><span data-ttu-id="302d9-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="302d9-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="302d9-157">MFTrace</span><span class="sxs-lookup"><span data-stu-id="302d9-157">MFTrace</span></span>](mftrace.md)
</dt> <dt>

[<span data-ttu-id="302d9-158">使用 MFTrace</span><span class="sxs-lookup"><span data-stu-id="302d9-158">Using MFTrace</span></span>](using-mftrace.md)
</dt> </dl>

 

 



