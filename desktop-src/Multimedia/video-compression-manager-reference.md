---
title: 影片壓縮管理員參考
description: 影片壓縮管理員參考
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- 'Windows (VFW) 的影片、視訊壓縮管理員 (BC-VCM-LVM-HYPERV) '
- '適用于 Windows) 的 VFW (影片、視訊壓縮管理員 (BC-VCM-LVM-HYPERV) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183197"
---
# <a name="video-compression-manager-reference"></a><span data-ttu-id="27540-105">影片壓縮管理員參考</span><span class="sxs-lookup"><span data-stu-id="27540-105">Video Compression Manager Reference</span></span>

<span data-ttu-id="27540-106">本節說明與 BC-VCM-LVM-HYPERV 相關聯的函式、結構、訊息和宏。</span><span class="sxs-lookup"><span data-stu-id="27540-106">This section describes the functions, structures, messages, and macros, associated with VCM.</span></span> <span data-ttu-id="27540-107">這些元素的分組方式如下。</span><span class="sxs-lookup"><span data-stu-id="27540-107">These elements are grouped as follows.</span></span>

## <a name="compressor-installation-and-removal"></a><span data-ttu-id="27540-108">壓縮安裝和移除</span><span class="sxs-lookup"><span data-stu-id="27540-108">Compressor Installation and Removal</span></span>

-   [<span data-ttu-id="27540-109">**ICInstall**</span><span class="sxs-lookup"><span data-stu-id="27540-109">**ICInstall**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [<span data-ttu-id="27540-110">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="27540-110">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="27540-111">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="27540-111">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="27540-112">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="27540-112">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [<span data-ttu-id="27540-113">**ICRemove**</span><span class="sxs-lookup"><span data-stu-id="27540-113">**ICRemove**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [<span data-ttu-id="27540-114">**ICOpenFunction**</span><span class="sxs-lookup"><span data-stu-id="27540-114">**ICOpenFunction**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a><span data-ttu-id="27540-115">尋找和開啟壓縮</span><span class="sxs-lookup"><span data-stu-id="27540-115">Locating and Opening a Compressor</span></span>

-   [<span data-ttu-id="27540-116">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="27540-116">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="27540-117">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="27540-117">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="27540-118">**ICDecompressOpen**</span><span class="sxs-lookup"><span data-stu-id="27540-118">**ICDecompressOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [<span data-ttu-id="27540-119">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="27540-119">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="27540-120">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="27540-120">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="27540-121">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="27540-121">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a><span data-ttu-id="27540-122">選取壓縮機</span><span class="sxs-lookup"><span data-stu-id="27540-122">Selecting Compressors</span></span>

-   [<span data-ttu-id="27540-123">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="27540-123">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [<span data-ttu-id="27540-124">**ICCompressorFree**</span><span class="sxs-lookup"><span data-stu-id="27540-124">**ICCompressorFree**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [<span data-ttu-id="27540-125">**COMPVARS**</span><span class="sxs-lookup"><span data-stu-id="27540-125">**COMPVARS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a><span data-ttu-id="27540-126">設定壓縮機</span><span class="sxs-lookup"><span data-stu-id="27540-126">Configuring Compressors</span></span>

-   [<span data-ttu-id="27540-127">**ICM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="27540-127">**ICM\_CONFIGURE**</span></span>](icm-configure.md)
-   [<span data-ttu-id="27540-128">**ICM \_ >GETSTATE**</span><span class="sxs-lookup"><span data-stu-id="27540-128">**ICM\_GETSTATE**</span></span>](icm-getstate.md)
-   [<span data-ttu-id="27540-129">**ICM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="27540-129">**ICM\_SETSTATE**</span></span>](icm-setstate.md)
-   [<span data-ttu-id="27540-130">**ICSendMessage**</span><span class="sxs-lookup"><span data-stu-id="27540-130">**ICSendMessage**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a><span data-ttu-id="27540-131">壓縮資訊</span><span class="sxs-lookup"><span data-stu-id="27540-131">Compressor Information</span></span>

-   [<span data-ttu-id="27540-132">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="27540-132">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="27540-133">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="27540-133">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="27540-134">**ICM \_ GETDEFAULTKEYFRAMERATE**</span><span class="sxs-lookup"><span data-stu-id="27540-134">**ICM\_GETDEFAULTKEYFRAMERATE**</span></span>](icm-getdefaultkeyframerate.md)
-   [<span data-ttu-id="27540-135">**ICGetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="27540-135">**ICGetDisplayFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [<span data-ttu-id="27540-136">**ICM \_ GETDEFAULTQUALITY**</span><span class="sxs-lookup"><span data-stu-id="27540-136">**ICM\_GETDEFAULTQUALITY**</span></span>](icm-getdefaultquality.md)
-   [<span data-ttu-id="27540-137">**關於的 ICM \_**</span><span class="sxs-lookup"><span data-stu-id="27540-137">**ICM\_ABOUT**</span></span>](icm-about.md)

## <a name="single-image-compression"></a><span data-ttu-id="27540-138">單一影像壓縮</span><span class="sxs-lookup"><span data-stu-id="27540-138">Single Image Compression</span></span>

-   [<span data-ttu-id="27540-139">**ICImageCompress**</span><span class="sxs-lookup"><span data-stu-id="27540-139">**ICImageCompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a><span data-ttu-id="27540-140">序列壓縮</span><span class="sxs-lookup"><span data-stu-id="27540-140">Sequence Compression</span></span>

-   [<span data-ttu-id="27540-141">**ICSeqCompressFrame**</span><span class="sxs-lookup"><span data-stu-id="27540-141">**ICSeqCompressFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [<span data-ttu-id="27540-142">**ICSeqCompressFrameStart**</span><span class="sxs-lookup"><span data-stu-id="27540-142">**ICSeqCompressFrameStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [<span data-ttu-id="27540-143">**ICSeqCompressFrameEnd**</span><span class="sxs-lookup"><span data-stu-id="27540-143">**ICSeqCompressFrameEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a><span data-ttu-id="27540-144">COMPVARS</span><span class="sxs-lookup"><span data-stu-id="27540-144">COMPVARS</span></span>

-   [<span data-ttu-id="27540-145">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="27540-145">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a><span data-ttu-id="27540-146">影像資料壓縮</span><span class="sxs-lookup"><span data-stu-id="27540-146">Image Data Compression</span></span>

-   [<span data-ttu-id="27540-147">**ICCOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="27540-147">**ICCOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [<span data-ttu-id="27540-148">**ICM \_ 壓縮 \_ 取得 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="27540-148">**ICM\_COMPRESS\_GET\_FORMAT**</span></span>](icm-compress-get-format.md)
-   [<span data-ttu-id="27540-149">**ICM \_ 壓縮 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="27540-149">**ICM\_COMPRESS\_QUERY**</span></span>](icm-compress-query.md)
-   [<span data-ttu-id="27540-150">**ICM \_ 壓縮 \_ 取得 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="27540-150">**ICM\_COMPRESS\_GET\_SIZE**</span></span>](icm-compress-get-size.md)
-   [<span data-ttu-id="27540-151">**ICM \_ 壓縮 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="27540-151">**ICM\_COMPRESS\_BEGIN**</span></span>](icm-compress-begin.md)
-   [<span data-ttu-id="27540-152">**ICM \_ 壓縮 \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="27540-152">**ICM\_COMPRESS\_END**</span></span>](icm-compress-end.md)

## <a name="compressor-monitoring"></a><span data-ttu-id="27540-153">壓縮監視</span><span class="sxs-lookup"><span data-stu-id="27540-153">Compressor Monitoring</span></span>

-   [<span data-ttu-id="27540-154">**ICSETSTATUSPROC**</span><span class="sxs-lookup"><span data-stu-id="27540-154">**ICSETSTATUSPROC**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a><span data-ttu-id="27540-155">解壓縮單一映射</span><span class="sxs-lookup"><span data-stu-id="27540-155">Decompressing Single Images</span></span>

-   [<span data-ttu-id="27540-156">**ICImageDecompress**</span><span class="sxs-lookup"><span data-stu-id="27540-156">**ICImageDecompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a><span data-ttu-id="27540-157">解壓縮映射資料</span><span class="sxs-lookup"><span data-stu-id="27540-157">Decompressing Image Data</span></span>

-   [<span data-ttu-id="27540-158">**ICDECOMPRESSEX**</span><span class="sxs-lookup"><span data-stu-id="27540-158">**ICDECOMPRESSEX**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [<span data-ttu-id="27540-159">**ICDecompressExBegin**</span><span class="sxs-lookup"><span data-stu-id="27540-159">**ICDecompressExBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [<span data-ttu-id="27540-160">**ICM \_ DECOMPRESSEX \_ END**</span><span class="sxs-lookup"><span data-stu-id="27540-160">**ICM\_DECOMPRESSEX\_END**</span></span>](icm-decompressex-end.md)
-   [<span data-ttu-id="27540-161">**ICM \_ 解壓縮 \_ 取得 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="27540-161">**ICM\_DECOMPRESS\_GET\_FORMAT**</span></span>](icm-decompress-get-format.md)
-   [<span data-ttu-id="27540-162">**ICM \_ 解壓縮 \_ 取得 \_ 調色板**</span><span class="sxs-lookup"><span data-stu-id="27540-162">**ICM\_DECOMPRESS\_GET\_PALETTE**</span></span>](icm-decompress-get-palette.md)
-   [<span data-ttu-id="27540-163">**ICDecompressExQuery**</span><span class="sxs-lookup"><span data-stu-id="27540-163">**ICDecompressExQuery**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [<span data-ttu-id="27540-164">**ICDECOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="27540-164">**ICDECOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [<span data-ttu-id="27540-165">**ICM \_ 解壓縮 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="27540-165">**ICM\_DECOMPRESS\_BEGIN**</span></span>](icm-decompress-begin.md)
-   [<span data-ttu-id="27540-166">**ICM \_ 解壓縮 \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="27540-166">**ICM\_DECOMPRESS\_END**</span></span>](icm-decompress-end.md)
-   [<span data-ttu-id="27540-167">**ICM \_ 解壓縮 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="27540-167">**ICM\_DECOMPRESS\_QUERY**</span></span>](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a><span data-ttu-id="27540-168">使用 Hardware-Drawing 功能</span><span class="sxs-lookup"><span data-stu-id="27540-168">Using Hardware-Drawing Capabilities</span></span>

-   [<span data-ttu-id="27540-169">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="27540-169">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="27540-170">**ICDRAWBEGIN**</span><span class="sxs-lookup"><span data-stu-id="27540-170">**ICDRAWBEGIN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [<span data-ttu-id="27540-171">**ICM \_ 繪製 \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="27540-171">**ICM\_DRAW\_END**</span></span>](icm-draw-end.md)
-   [<span data-ttu-id="27540-172">**ICM \_ 繪圖排清 \_**</span><span class="sxs-lookup"><span data-stu-id="27540-172">**ICM\_DRAW\_FLUSH**</span></span>](icm-draw-flush.md)
-   [<span data-ttu-id="27540-173">**ICM \_ 繪圖 \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="27540-173">**ICM\_DRAW\_QUERY**</span></span>](icm-draw-query.md)
-   [<span data-ttu-id="27540-174">**ICDrawSuggestFormat**</span><span class="sxs-lookup"><span data-stu-id="27540-174">**ICDrawSuggestFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [<span data-ttu-id="27540-175">**ICM \_ 繪圖 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="27540-175">**ICM\_DRAW\_START**</span></span>](icm-draw-start.md)
-   [<span data-ttu-id="27540-176">**ICM \_ 繪圖 \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="27540-176">**ICM\_DRAW\_STOP**</span></span>](icm-draw-stop.md)
-   [<span data-ttu-id="27540-177">**ICM \_ GETBUFFERSWANTED**</span><span class="sxs-lookup"><span data-stu-id="27540-177">**ICM\_GETBUFFERSWANTED**</span></span>](icm-getbufferswanted.md)
-   [<span data-ttu-id="27540-178">**ICM \_ 繪圖 \_ 實現**</span><span class="sxs-lookup"><span data-stu-id="27540-178">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="27540-179">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="27540-179">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="27540-180">**ICDRAW**</span><span class="sxs-lookup"><span data-stu-id="27540-180">**ICDRAW**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [<span data-ttu-id="27540-181">**ICM \_ 繪圖 \_ GETTIME**</span><span class="sxs-lookup"><span data-stu-id="27540-181">**ICM\_DRAW\_GETTIME**</span></span>](icm-draw-gettime.md)
-   [<span data-ttu-id="27540-182">**ICM \_ 繪圖 \_ SETTIME**</span><span class="sxs-lookup"><span data-stu-id="27540-182">**ICM\_DRAW\_SETTIME**</span></span>](icm-draw-settime.md)
-   [<span data-ttu-id="27540-183">**ICM \_ 繪圖 \_ 視窗**</span><span class="sxs-lookup"><span data-stu-id="27540-183">**ICM\_DRAW\_WINDOW**</span></span>](icm-draw-window.md)
-   [<span data-ttu-id="27540-184">**ICM \_ 繪圖 \_ 實現**</span><span class="sxs-lookup"><span data-stu-id="27540-184">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="27540-185">**ICM \_ 繪圖 \_ CHANGEPALETTE**</span><span class="sxs-lookup"><span data-stu-id="27540-185">**ICM\_DRAW\_CHANGEPALETTE**</span></span>](icm-draw-changepalette.md)
-   [<span data-ttu-id="27540-186">**ICM \_ 繪圖 \_ RENDERBUFFER**</span><span class="sxs-lookup"><span data-stu-id="27540-186">**ICM\_DRAW\_RENDERBUFFER**</span></span>](icm-draw-renderbuffer.md)

## <a name="related-topics"></a><span data-ttu-id="27540-187">相關主題</span><span class="sxs-lookup"><span data-stu-id="27540-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27540-188">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="27540-188">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 




