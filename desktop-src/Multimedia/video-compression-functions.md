---
title: 影片壓縮函數
description: 影片壓縮函數
ms.assetid: 193961a5-b882-4769-bce7-a53d625fc9dd
keywords:
- 適用于 Windows (VFW) ，BC-VCM-LVM-HYPERV 函式的影片
- 適用于 Windows) 、BC-VCM-LVM-HYPERV 函式的 VFW (影片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0876b67c74ddac2d2f498583fe058dd9ea39436
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092696"
---
# <a name="video-compression-functions"></a><span data-ttu-id="bd229-105">影片壓縮函數</span><span class="sxs-lookup"><span data-stu-id="bd229-105">Video Compression Functions</span></span>

<span data-ttu-id="bd229-106">下列函式可用於視訊壓縮。</span><span class="sxs-lookup"><span data-stu-id="bd229-106">The following functions are used with video compression.</span></span>

-   [<span data-ttu-id="bd229-107">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="bd229-107">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [<span data-ttu-id="bd229-108">**ICCompress**</span><span class="sxs-lookup"><span data-stu-id="bd229-108">**ICCompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompress)
-   [<span data-ttu-id="bd229-109">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="bd229-109">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [<span data-ttu-id="bd229-110">**ICCompressorFree**</span><span class="sxs-lookup"><span data-stu-id="bd229-110">**ICCompressorFree**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [<span data-ttu-id="bd229-111">**ICDecompress**</span><span class="sxs-lookup"><span data-stu-id="bd229-111">**ICDecompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompress)
-   [<span data-ttu-id="bd229-112">**ICDecompressEx**</span><span class="sxs-lookup"><span data-stu-id="bd229-112">**ICDecompressEx**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressex)
-   [<span data-ttu-id="bd229-113">**ICDecompressExBegin**</span><span class="sxs-lookup"><span data-stu-id="bd229-113">**ICDecompressExBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [<span data-ttu-id="bd229-114">**ICDecompressExQuery**</span><span class="sxs-lookup"><span data-stu-id="bd229-114">**ICDecompressExQuery**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [<span data-ttu-id="bd229-115">**ICDraw**</span><span class="sxs-lookup"><span data-stu-id="bd229-115">**ICDraw**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdraw)
-   [<span data-ttu-id="bd229-116">**ICDrawBegin**</span><span class="sxs-lookup"><span data-stu-id="bd229-116">**ICDrawBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin)
-   [<span data-ttu-id="bd229-117">**ICDrawSuggestFormat**</span><span class="sxs-lookup"><span data-stu-id="bd229-117">**ICDrawSuggestFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [<span data-ttu-id="bd229-118">**ICGetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="bd229-118">**ICGetDisplayFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [<span data-ttu-id="bd229-119">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="bd229-119">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="bd229-120">**ICImageCompress**</span><span class="sxs-lookup"><span data-stu-id="bd229-120">**ICImageCompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)
-   [<span data-ttu-id="bd229-121">**ICImageDecompress**</span><span class="sxs-lookup"><span data-stu-id="bd229-121">**ICImageDecompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)
-   [<span data-ttu-id="bd229-122">**ICInfo**</span><span class="sxs-lookup"><span data-stu-id="bd229-122">**ICInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icinfo)
-   [<span data-ttu-id="bd229-123">**ICInstall**</span><span class="sxs-lookup"><span data-stu-id="bd229-123">**ICInstall**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [<span data-ttu-id="bd229-124">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="bd229-124">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="bd229-125">**ICOpen**</span><span class="sxs-lookup"><span data-stu-id="bd229-125">**ICOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icopen)
-   [<span data-ttu-id="bd229-126">**ICOpenFunction**</span><span class="sxs-lookup"><span data-stu-id="bd229-126">**ICOpenFunction**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)
-   [<span data-ttu-id="bd229-127">**ICRemove**</span><span class="sxs-lookup"><span data-stu-id="bd229-127">**ICRemove**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [<span data-ttu-id="bd229-128">**ICSendMessage**</span><span class="sxs-lookup"><span data-stu-id="bd229-128">**ICSendMessage**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)
-   [<span data-ttu-id="bd229-129">**ICSeqCompressFrame**</span><span class="sxs-lookup"><span data-stu-id="bd229-129">**ICSeqCompressFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [<span data-ttu-id="bd229-130">**ICSeqCompressFrameEnd**</span><span class="sxs-lookup"><span data-stu-id="bd229-130">**ICSeqCompressFrameEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)
-   [<span data-ttu-id="bd229-131">**ICSeqCompressFrameStart**</span><span class="sxs-lookup"><span data-stu-id="bd229-131">**ICSeqCompressFrameStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [<span data-ttu-id="bd229-132">**ICSetStatusProc**</span><span class="sxs-lookup"><span data-stu-id="bd229-132">**ICSetStatusProc**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc)
-   <span data-ttu-id="bd229-133">[**MyStatusProc**](/previous-versions//dd743620(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd229-133">[**MyStatusProc**](/previous-versions//dd743620(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd229-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd229-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd229-135">影片壓縮管理員參考</span><span class="sxs-lookup"><span data-stu-id="bd229-135">Video Compression Manager Reference</span></span>](video-compression-manager-reference.md)
</dt> </dl>

 

 