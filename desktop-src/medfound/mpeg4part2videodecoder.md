---
description: MPEG4 Part 2 影片解碼會將根據 MPEG4 第2部分標準編碼的影片串流進行編碼。
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: 'MPEG-2 第2部影片解碼 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191775"
---
# <a name="mpeg-4-part-2-video-decoder"></a><span data-ttu-id="01f3c-103">MPEG 4 第2部分影片解碼</span><span class="sxs-lookup"><span data-stu-id="01f3c-103">MPEG-4 Part 2 Video Decoder</span></span>

<span data-ttu-id="01f3c-104">MPEG4 Part 2 影片解碼會將根據 MPEG4 第2部分標準編碼的影片串流進行編碼。</span><span class="sxs-lookup"><span data-stu-id="01f3c-104">The MPEG4 Part 2 Video decoder decodes video streams that were encoded according to the MPEG4 Part 2 standard.</span></span>

<span data-ttu-id="01f3c-105">您可以藉由呼叫 **CoCreateInstance** 來建立 MPEG4 Part 2 Video 解碼的實例。</span><span class="sxs-lookup"><span data-stu-id="01f3c-105">You can create an instance of the MPEG4 Part 2 Video decoder by calling **CoCreateInstance**.</span></span> <span data-ttu-id="01f3c-106">若要建立作為 DirectX 媒體物件的解碼器實例， (的) ，請使用類別識別碼 **CLSID \_ CMpeg4sDecMediaObject**。</span><span class="sxs-lookup"><span data-stu-id="01f3c-106">To create an instance of the decoder that behaves as a DirectX Media Object (DMO), use the class identifier **CLSID\_CMpeg4sDecMediaObject**.</span></span> <span data-ttu-id="01f3c-107">若要建立媒體基礎轉換 (MFT) 的解碼器實例，請使用類別識別碼 **CLSID \_ CMpeg4sDecMFT**。</span><span class="sxs-lookup"><span data-stu-id="01f3c-107">To create an istance of the decoder that behaves as a Media Foundation Transform (MFT), use the class identifier **CLSID\_CMpeg4sDecMFT**.</span></span>

## <a name="input-types"></a><span data-ttu-id="01f3c-108">輸入類型</span><span class="sxs-lookup"><span data-stu-id="01f3c-108">Input Types</span></span>

<span data-ttu-id="01f3c-109">MPEG4 Part 2 影片解碼支援下列輸入媒體類型。</span><span class="sxs-lookup"><span data-stu-id="01f3c-109">The MPEG4 Part 2 Video decoder supports the following input media types.</span></span>

-   <span data-ttu-id="01f3c-110">MEDIASUBTYPE \_ M4S2</span><span class="sxs-lookup"><span data-stu-id="01f3c-110">MEDIASUBTYPE\_M4S2</span></span>
-   <span data-ttu-id="01f3c-111">MEDIASUBTYPE \_ m4s2</span><span class="sxs-lookup"><span data-stu-id="01f3c-111">MEDIASUBTYPE\_m4s2</span></span>
-   <span data-ttu-id="01f3c-112">MEDIASUBTYPE \_ MP4V</span><span class="sxs-lookup"><span data-stu-id="01f3c-112">MEDIASUBTYPE\_MP4V</span></span>
-   <span data-ttu-id="01f3c-113">MEDIASUBTYPE \_ mp4v</span><span class="sxs-lookup"><span data-stu-id="01f3c-113">MEDIASUBTYPE\_mp4v</span></span>
-   <span data-ttu-id="01f3c-114">MEDIASUBTYPE \_ mp4 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="01f3c-114">MEDIASUBTYPE\_MP4S (deprecated)</span></span>
-   <span data-ttu-id="01f3c-115">MEDIASUBTYPE \_ mp4 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="01f3c-115">MEDIASUBTYPE\_mp4s (deprecated)</span></span>

## <a name="output-types"></a><span data-ttu-id="01f3c-116">輸出型別</span><span class="sxs-lookup"><span data-stu-id="01f3c-116">Output Types</span></span>

<span data-ttu-id="01f3c-117">MPEG4 Part 2 影片解碼可支援下列輸出媒體子類型作為一種。</span><span class="sxs-lookup"><span data-stu-id="01f3c-117">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="01f3c-118">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="01f3c-118">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="01f3c-119">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="01f3c-119">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="01f3c-120">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="01f3c-120">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="01f3c-121">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="01f3c-121">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="01f3c-122">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="01f3c-122">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="01f3c-123">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="01f3c-123">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="01f3c-124">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="01f3c-124">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="01f3c-125">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="01f3c-125">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="01f3c-126">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="01f3c-126">MEDIASUBTYPE\_ RGB565</span></span>
-   <span data-ttu-id="01f3c-127">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="01f3c-127">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="01f3c-128">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="01f3c-128">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="01f3c-129">MPEG4 Part 2 影片解碼可支援下列輸出媒體子類型作為 MFT。</span><span class="sxs-lookup"><span data-stu-id="01f3c-129">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="01f3c-130">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="01f3c-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="01f3c-131">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="01f3c-131">MEDIASUBTYPE\_YV12</span></span>

## <a name="formats"></a><span data-ttu-id="01f3c-132">格式</span><span class="sxs-lookup"><span data-stu-id="01f3c-132">Formats</span></span>

<span data-ttu-id="01f3c-133">MPEG4 Part 2 影片解碼接受下列格式。</span><span class="sxs-lookup"><span data-stu-id="01f3c-133">The MPEG4 Part 2 Video decoder accepts the following formats.</span></span>

-   [<span data-ttu-id="01f3c-134">**VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="01f3c-134">**VIDEOINFOHEADER**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   <span data-ttu-id="01f3c-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2) </span><span class="sxs-lookup"><span data-stu-id="01f3c-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span></span>
-   [<span data-ttu-id="01f3c-136">**MFVideoInfo**</span><span class="sxs-lookup"><span data-stu-id="01f3c-136">**MFVideoInfo**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   <span data-ttu-id="01f3c-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (只會使用標頭的 VIH2 部分。 ) </span><span class="sxs-lookup"><span data-stu-id="01f3c-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (Only the VIH2 portion of the header is used.)</span></span>

## <a name="interfaces-for-the-dmo"></a><span data-ttu-id="01f3c-138">SQL-DMO 介面</span><span class="sxs-lookup"><span data-stu-id="01f3c-138">Interfaces for the DMO</span></span>

<span data-ttu-id="01f3c-139">如果您將 MPEG4 第2部分影片解碼的實例建立為 i，則此解碼器會公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="01f3c-139">If you create an instance of the MPEG4 Part 2 Video decoder as a DMO, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="01f3c-140">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="01f3c-140">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="01f3c-141">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="01f3c-141">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)

<span data-ttu-id="01f3c-142">您可以藉由呼叫 **CoCreateInstance** 來取得 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)介面，也可以藉由呼叫 **QueryInterface** 來取得 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)介面。</span><span class="sxs-lookup"><span data-stu-id="01f3c-142">You can obtain an [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface by calling **CoCreateInstance**, and you can obtain an [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface by calling **QueryInterface**.</span></span>

## <a name="interfaces-for-the-mft"></a><span data-ttu-id="01f3c-143">適用于 MFT 的介面</span><span class="sxs-lookup"><span data-stu-id="01f3c-143">Interfaces for the MFT</span></span>

<span data-ttu-id="01f3c-144">如果您建立了 MPEG2 第2部分影片解碼器的實例作為 MFT，則此解碼器會公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="01f3c-144">If you create an instance of the MPEG2 Part 2 Video decoder as an MFT, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="01f3c-145">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="01f3c-145">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="01f3c-146">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="01f3c-146">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="01f3c-147">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="01f3c-147">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="01f3c-148">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="01f3c-148">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="01f3c-149">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="01f3c-149">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="01f3c-150">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="01f3c-150">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

<span data-ttu-id="01f3c-151">您可以藉由呼叫 **CoCreateInstance** 來取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面的指標，也可以藉由呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="01f3c-151">You can obtain a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface by calling **CoCreateInstance**, and you can obtain a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface by calling [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span></span> <span data-ttu-id="01f3c-152">您可以藉由呼叫 MFT 上的 **QueryInterface** 來取得 [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)或 [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="01f3c-152">You can obtain a pointer to the [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) or [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) interface by calling **QueryInterface** on the MFT.</span></span> <span data-ttu-id="01f3c-153">您可以藉由呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)並傳遞服務識別碼 **MF \_ 速率 \_ 控制 \_ 服務**，來取得 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)或 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="01f3c-153">You can obtain a pointer to the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) or [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and passing the service identifier **MF\_RATE\_CONTROL\_SERVICE**.</span></span>

## <a name="profiles-and-levels"></a><span data-ttu-id="01f3c-154">設定檔和層級</span><span class="sxs-lookup"><span data-stu-id="01f3c-154">Profiles and Levels</span></span>

<span data-ttu-id="01f3c-155">MPEG4 規格會定義數個設定檔，其中每個設定檔都會指定編碼器可用來產生編碼資料流程的工具。</span><span class="sxs-lookup"><span data-stu-id="01f3c-155">The MPEG4 specification defines several profiles, each of which specifies the tools that an encoder can use to generate an encoded stream.</span></span> <span data-ttu-id="01f3c-156">MPEG4 第2部分 Video 解碼支援下列兩個設定檔：簡單的視覺化設定檔和 Advanced Simple Profile。</span><span class="sxs-lookup"><span data-stu-id="01f3c-156">The MPEG4 Part2 Video Decoder supports two of those profiles: Simple Visual Profile and Advanced Simple Profile.</span></span> <span data-ttu-id="01f3c-157">換句話說，MPEG4 Part 2 影片解碼可將根據簡單視覺化設定檔或 Advanced Simple Profile 編碼的資料流程解碼。</span><span class="sxs-lookup"><span data-stu-id="01f3c-157">In other words, the MPEG4 Part 2 Video decoder can decode streams that were encoded according to either the Simple Visual Profile or the Advanced Simple Profile.</span></span>

<span data-ttu-id="01f3c-158">簡單的視覺效果設定檔支援漸進式模式下低位速率影片的基本傳輸。</span><span class="sxs-lookup"><span data-stu-id="01f3c-158">The Simple Visual Profile supports basic transmission of low bit-rate video in progressive mode.</span></span> <span data-ttu-id="01f3c-159">它僅支援內部和預測圖片。</span><span class="sxs-lookup"><span data-stu-id="01f3c-159">It supports only Intra and Prediction pictures.</span></span> <span data-ttu-id="01f3c-160">它也支援簡短的標頭模式，它可回溯相容于 .H 基準設定檔。</span><span class="sxs-lookup"><span data-stu-id="01f3c-160">It also supports the short header mode, which is backward compatible with the H.263 baseline profile.</span></span> <span data-ttu-id="01f3c-161">從 Windows 10 開始，MPEG 4 第2部分影片解碼器也支援支援自訂圖片大小的 263v2 (.H +) 。</span><span class="sxs-lookup"><span data-stu-id="01f3c-161">Starting with Windows 10, the MPEG-4 Part 2 Video Decoder also supports H.263v2 (H.263+) which supports custom picture sizes.</span></span>

<span data-ttu-id="01f3c-162">先進的簡單設定檔支援簡單的視覺效果設定檔的所有工具，此外也支援交錯式影片、B 框架、季-pel 運動補償、額外的量化資料表，以及全球動作補償。</span><span class="sxs-lookup"><span data-stu-id="01f3c-162">The Advanced Simple Profile supports all the tools of the Simple Visual Profile and, in addition, supports interlaced video, B-frames, quarter-pel motion compensation, additional quantization tables, and global motion compensation.</span></span>

<span data-ttu-id="01f3c-163">MPEG4 規格也會定義數個層級，其中每個層級都會針對編碼器所產生的輸出資料流程指定條件約束。</span><span class="sxs-lookup"><span data-stu-id="01f3c-163">The MPEG4 specification also defines several levels, each of which specifies constraints on the output stream generated by an encoder.</span></span>

<span data-ttu-id="01f3c-164">下表顯示 MPEG4 第2部分影片解碼所支援的設定檔和層級，以及一般的解決方案。</span><span class="sxs-lookup"><span data-stu-id="01f3c-164">The following table shows the profiles and levels, along with typical resolutions, supported by the MPEG4 Part 2 Video decoder.</span></span>



| <span data-ttu-id="01f3c-165">設定檔</span><span class="sxs-lookup"><span data-stu-id="01f3c-165">Profile</span></span>         | <span data-ttu-id="01f3c-166">層級</span><span class="sxs-lookup"><span data-stu-id="01f3c-166">Level</span></span> | <span data-ttu-id="01f3c-167">一般解決方式</span><span class="sxs-lookup"><span data-stu-id="01f3c-167">Typical Resolution</span></span> |
|-----------------|-------|--------------------|
| <span data-ttu-id="01f3c-168">簡單視覺效果</span><span class="sxs-lookup"><span data-stu-id="01f3c-168">Simple Visual</span></span>   | <span data-ttu-id="01f3c-169">0</span><span class="sxs-lookup"><span data-stu-id="01f3c-169">0</span></span>     | <span data-ttu-id="01f3c-170">176 x 144</span><span class="sxs-lookup"><span data-stu-id="01f3c-170">176 x 144</span></span>          |
| <span data-ttu-id="01f3c-171">簡單視覺效果</span><span class="sxs-lookup"><span data-stu-id="01f3c-171">Simple Visual</span></span>   | <span data-ttu-id="01f3c-172">1</span><span class="sxs-lookup"><span data-stu-id="01f3c-172">1</span></span>     | <span data-ttu-id="01f3c-173">176 x 144</span><span class="sxs-lookup"><span data-stu-id="01f3c-173">176 x 144</span></span>          |
| <span data-ttu-id="01f3c-174">簡單視覺效果</span><span class="sxs-lookup"><span data-stu-id="01f3c-174">Simple Visual</span></span>   | <span data-ttu-id="01f3c-175">2</span><span class="sxs-lookup"><span data-stu-id="01f3c-175">2</span></span>     | <span data-ttu-id="01f3c-176">352 x 288</span><span class="sxs-lookup"><span data-stu-id="01f3c-176">352 x 288</span></span>          |
| <span data-ttu-id="01f3c-177">簡單視覺效果</span><span class="sxs-lookup"><span data-stu-id="01f3c-177">Simple Visual</span></span>   | <span data-ttu-id="01f3c-178">3</span><span class="sxs-lookup"><span data-stu-id="01f3c-178">3</span></span>     | <span data-ttu-id="01f3c-179">352 x 288</span><span class="sxs-lookup"><span data-stu-id="01f3c-179">352 x 288</span></span>          |
| <span data-ttu-id="01f3c-180">SimpleVisual</span><span class="sxs-lookup"><span data-stu-id="01f3c-180">SimpleVisual</span></span>    | <span data-ttu-id="01f3c-181">4a</span><span class="sxs-lookup"><span data-stu-id="01f3c-181">4a</span></span>    | <span data-ttu-id="01f3c-182">640 x 480</span><span class="sxs-lookup"><span data-stu-id="01f3c-182">640 x 480</span></span>          |
| <span data-ttu-id="01f3c-183">簡單視覺效果</span><span class="sxs-lookup"><span data-stu-id="01f3c-183">Simple Visual</span></span>   | <span data-ttu-id="01f3c-184">5</span><span class="sxs-lookup"><span data-stu-id="01f3c-184">5</span></span>     | <span data-ttu-id="01f3c-185">720 x 576</span><span class="sxs-lookup"><span data-stu-id="01f3c-185">720 x 576</span></span>          |
| <span data-ttu-id="01f3c-186">Advanced Simple</span><span class="sxs-lookup"><span data-stu-id="01f3c-186">Advanced Simple</span></span> | <span data-ttu-id="01f3c-187">0</span><span class="sxs-lookup"><span data-stu-id="01f3c-187">0</span></span>     | <span data-ttu-id="01f3c-188">176 x 144</span><span class="sxs-lookup"><span data-stu-id="01f3c-188">176 x 144</span></span>          |
| <span data-ttu-id="01f3c-189">Advanced Simple</span><span class="sxs-lookup"><span data-stu-id="01f3c-189">Advanced Simple</span></span> | <span data-ttu-id="01f3c-190">1</span><span class="sxs-lookup"><span data-stu-id="01f3c-190">1</span></span>     | <span data-ttu-id="01f3c-191">176 x 144</span><span class="sxs-lookup"><span data-stu-id="01f3c-191">176 x 144</span></span>          |
| <span data-ttu-id="01f3c-192">Advanced Simple</span><span class="sxs-lookup"><span data-stu-id="01f3c-192">Advanced Simple</span></span> | <span data-ttu-id="01f3c-193">2</span><span class="sxs-lookup"><span data-stu-id="01f3c-193">2</span></span>     | <span data-ttu-id="01f3c-194">352 x 288</span><span class="sxs-lookup"><span data-stu-id="01f3c-194">352 x 288</span></span>          |
| <span data-ttu-id="01f3c-195">Advanced Simple</span><span class="sxs-lookup"><span data-stu-id="01f3c-195">Advanced Simple</span></span> | <span data-ttu-id="01f3c-196">3</span><span class="sxs-lookup"><span data-stu-id="01f3c-196">3</span></span>     | <span data-ttu-id="01f3c-197">352 x 288</span><span class="sxs-lookup"><span data-stu-id="01f3c-197">352 x 288</span></span>          |
| <span data-ttu-id="01f3c-198">Advanced Simple</span><span class="sxs-lookup"><span data-stu-id="01f3c-198">Advanced Simple</span></span> | <span data-ttu-id="01f3c-199">3b</span><span class="sxs-lookup"><span data-stu-id="01f3c-199">3b</span></span>    | <span data-ttu-id="01f3c-200">352 x 288</span><span class="sxs-lookup"><span data-stu-id="01f3c-200">352 x 288</span></span>          |
| <span data-ttu-id="01f3c-201">Advanced Simple</span><span class="sxs-lookup"><span data-stu-id="01f3c-201">Advanced Simple</span></span> | <span data-ttu-id="01f3c-202">4</span><span class="sxs-lookup"><span data-stu-id="01f3c-202">4</span></span>     | <span data-ttu-id="01f3c-203">352 x 756</span><span class="sxs-lookup"><span data-stu-id="01f3c-203">352 x 756</span></span>          |
| <span data-ttu-id="01f3c-204">Advanced Simple</span><span class="sxs-lookup"><span data-stu-id="01f3c-204">Advanced Simple</span></span> | <span data-ttu-id="01f3c-205">5</span><span class="sxs-lookup"><span data-stu-id="01f3c-205">5</span></span>     | <span data-ttu-id="01f3c-206">720 x 576</span><span class="sxs-lookup"><span data-stu-id="01f3c-206">720 x 576</span></span>          |



 

<span data-ttu-id="01f3c-207">如需設定檔和層級的詳細資訊，請參閱 MPEG4 第2部分規格 (ISO/IEC 14496-2) ：資訊技術--音訊-視覺化物件的編碼--第2部分：視覺效果。</span><span class="sxs-lookup"><span data-stu-id="01f3c-207">For more information about profiles and levels, see the MPEG4 Part 2 specification (ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual.</span></span>

## <a name="decoder-properties"></a><span data-ttu-id="01f3c-208">解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="01f3c-208">Decoder Properties</span></span>

<span data-ttu-id="01f3c-209">若要設定 MPEG4 第2部分影片解碼器上的屬性，請使用 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面或 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="01f3c-209">To set properties on the MPEG4 Part 2 Video decoder, use the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface or the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="01f3c-210">MPEG4 Part 2 影片解碼支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="01f3c-210">The MPEG4 Part 2 Video decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="01f3c-211">屬性</span><span class="sxs-lookup"><span data-stu-id="01f3c-211">Property</span></span></th>
<th><span data-ttu-id="01f3c-212">描述</span><span class="sxs-lookup"><span data-stu-id="01f3c-212">Description</span></span></th>
<th><span data-ttu-id="01f3c-213">預設值</span><span class="sxs-lookup"><span data-stu-id="01f3c-213">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01f3c-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span><span class="sxs-lookup"><span data-stu-id="01f3c-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span></span></td>
<td><span data-ttu-id="01f3c-215">指定電源等級。</span><span class="sxs-lookup"><span data-stu-id="01f3c-215">Specifies the power level.</span></span><br/> <dl> <span data-ttu-id="01f3c-216">Windows 7。</span><span class="sxs-lookup"><span data-stu-id="01f3c-216">Windows 7.</span></span><br />
<span data-ttu-id="01f3c-217">唯寫。</span><span class="sxs-lookup"><span data-stu-id="01f3c-217">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="01f3c-218">100</span><span class="sxs-lookup"><span data-stu-id="01f3c-218">100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01f3c-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="01f3c-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span></span></td>
<td><span data-ttu-id="01f3c-220">指定縮圖產生模式。</span><span class="sxs-lookup"><span data-stu-id="01f3c-220">Specifies the thumbnail generation mode.</span></span><br/> <dl> <span data-ttu-id="01f3c-221">Windows 7。</span><span class="sxs-lookup"><span data-stu-id="01f3c-221">Windows 7.</span></span><br />
<span data-ttu-id="01f3c-222">唯寫。</span><span class="sxs-lookup"><span data-stu-id="01f3c-222">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="01f3c-223"><strong>VARIANT_FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="01f3c-223"><strong>VARIANT_FALSE</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="01f3c-224">備註</span><span class="sxs-lookup"><span data-stu-id="01f3c-224">Remarks</span></span>

<span data-ttu-id="01f3c-225">針對 RGB 媒體子類型 (Guid) 的全域唯一識別碼，會根據解碼器是以 SQL-DMO 或 MFT 作為依據而有所不同。</span><span class="sxs-lookup"><span data-stu-id="01f3c-225">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="01f3c-226">非 RGB 媒體子類型的 Guid 是相同的，不論是以 SQL-DMO 或 MFT 的形式來表示。</span><span class="sxs-lookup"><span data-stu-id="01f3c-226">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="01f3c-227">如需表示媒體子類型之 Guid 的詳細資訊，請參閱 [媒體類型](media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="01f3c-227">For information about the GUIDs that represent media subtypes, see [Media Types](media-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01f3c-228">規格需求</span><span class="sxs-lookup"><span data-stu-id="01f3c-228">Requirements</span></span>



| <span data-ttu-id="01f3c-229">需求</span><span class="sxs-lookup"><span data-stu-id="01f3c-229">Requirement</span></span> | <span data-ttu-id="01f3c-230">值</span><span class="sxs-lookup"><span data-stu-id="01f3c-230">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01f3c-231">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01f3c-231">Minimum supported client</span></span><br/> | <span data-ttu-id="01f3c-232">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01f3c-232">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="01f3c-233">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01f3c-233">Minimum supported server</span></span><br/> | <span data-ttu-id="01f3c-234">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01f3c-234">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="01f3c-235">標頭</span><span class="sxs-lookup"><span data-stu-id="01f3c-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="01f3c-236"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="01f3c-236"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="01f3c-237">DLL</span><span class="sxs-lookup"><span data-stu-id="01f3c-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f3c-238"><dt>MP4SDecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01f3c-238"><dt>MP4SDecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01f3c-239">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01f3c-239">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f3c-240">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="01f3c-240">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
