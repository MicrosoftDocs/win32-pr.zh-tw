---
description: 本節說明如何撰寫自訂媒體基礎轉換 (MFT) 。
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: 撰寫自訂的 MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849517"
---
# <a name="writing-a-custom-mft"></a><span data-ttu-id="c3766-103">撰寫自訂的 MFT</span><span class="sxs-lookup"><span data-stu-id="c3766-103">Writing a Custom MFT</span></span>

<span data-ttu-id="c3766-104">本節說明如何撰寫自訂媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="c3766-104">This section describes how to write a custom Media Foundation Transform (MFT).</span></span>

## <a name="mft-checklist"></a><span data-ttu-id="c3766-105">MFT 檢查清單</span><span class="sxs-lookup"><span data-stu-id="c3766-105">MFT Checklist</span></span>

<span data-ttu-id="c3766-106">當您執行自訂的 MFT 時，請使用下列檢查清單來判斷需求：</span><span class="sxs-lookup"><span data-stu-id="c3766-106">When you implement a custom MFT, use the following checklist to determine the requirements:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c3766-107">所有 MFTs</span><span class="sxs-lookup"><span data-stu-id="c3766-107">All MFTs</span></span></td>
<td><span data-ttu-id="c3766-108">所有 MFTs 都必須執行 <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="c3766-108">All MFTs must implement <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span></span><br/> <span data-ttu-id="c3766-109">下列主題提供有關如何執行此介面的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="c3766-109">The following topics give more information about implementing this interface:</span></span>
<ul>
<li><span data-ttu-id="c3766-110"><a href="basic-mft-processing-model.md">基本 MFT 處理模型</a></span><span class="sxs-lookup"><span data-stu-id="c3766-110"><a href="basic-mft-processing-model.md">Basic MFT Processing Model</a></span></span></li>
<li><span data-ttu-id="c3766-111"><a href="time-stamps-and-durations.md">時間戳記和持續時間</a></span><span class="sxs-lookup"><span data-stu-id="c3766-111"><a href="time-stamps-and-durations.md">Time Stamps and Durations</a></span></span></li>
<li><span data-ttu-id="c3766-112"><a href="handling-stream-changes.md">處理資料流程變更</a></span><span class="sxs-lookup"><span data-stu-id="c3766-112"><a href="handling-stream-changes.md">Handling Stream Changes</a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3766-113">編碼器和解碼器</span><span class="sxs-lookup"><span data-stu-id="c3766-113">Encoders and decoders</span></span></td>
<td><span data-ttu-id="c3766-114">需求：請參閱 <a href="implementing-a-codec-mft.md">執行編解碼器 MFT</a>。</span><span class="sxs-lookup"><span data-stu-id="c3766-114">Requirements: See <a href="implementing-a-codec-mft.md">Implementing a Codec MFT</a>.</span></span><br/> <span data-ttu-id="c3766-115">建議：執行 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> 或 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>，以支援服務品質 (QoS) 通知。</span><span class="sxs-lookup"><span data-stu-id="c3766-115">Recommended: Implement <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> or <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>, to support quality-of-service (QoS) notifications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3766-116">影片解碼器和視頻處理器</span><span class="sxs-lookup"><span data-stu-id="c3766-116">Video decoders and video processors</span></span></td>
<td><span data-ttu-id="c3766-117">選用：支援 DirectX Video 加速。</span><span class="sxs-lookup"><span data-stu-id="c3766-117">Optional: Support DirectX Video Acceleration.</span></span><br/>
<ul>
<li><span data-ttu-id="c3766-118"><a href="direct3d-aware-mfts.md">Direct3D 感知 MFTs</a></span><span class="sxs-lookup"><span data-stu-id="c3766-118"><a href="direct3d-aware-mfts.md">Direct3D-Aware MFTs</a></span></span></li>
<li><span data-ttu-id="c3766-119"><a href="supporting-dxva-2-0-in-media-foundation.md">媒體基礎中支援 DXVA 2。0</a></span><span class="sxs-lookup"><span data-stu-id="c3766-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Supporting DXVA 2.0 in Media Foundation</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3766-120">硬體編解碼器</span><span class="sxs-lookup"><span data-stu-id="c3766-120">Hardware codecs</span></span></td>
<td><span data-ttu-id="c3766-121">請參閱 <a href="hardware-mfts.md">硬體 MFTs</a>。</span><span class="sxs-lookup"><span data-stu-id="c3766-121">See <a href="hardware-mfts.md">Hardware MFTs</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3766-122">讓應用程式可探索您的 MFT .。。</span><span class="sxs-lookup"><span data-stu-id="c3766-122">To make your MFT discoverable by applications...</span></span></td>
<td><span data-ttu-id="c3766-123">請參閱 <a href="registering-and-enumerating-mfts.md">註冊和列舉 MFTs</a>。</span><span class="sxs-lookup"><span data-stu-id="c3766-123">See <a href="registering-and-enumerating-mfts.md">Registering and Enumerating MFTs</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3766-124">非同步資料處理</span><span class="sxs-lookup"><span data-stu-id="c3766-124">Asynchronous data processing</span></span></td>
<td><span data-ttu-id="c3766-125">預設的 MFT 模型會使用同步 (封鎖) 呼叫來處理資料。</span><span class="sxs-lookup"><span data-stu-id="c3766-125">The default MFT model uses synchronous (blocking) calls to process data.</span></span> <span data-ttu-id="c3766-126">針對某些 MFTs，非同步處理可能更有效率。</span><span class="sxs-lookup"><span data-stu-id="c3766-126">For some MFTs, asynchronous processing can be more efficient.</span></span> <span data-ttu-id="c3766-127">但是，它也比較複雜。</span><span class="sxs-lookup"><span data-stu-id="c3766-127">However, it is also more complex to implement.</span></span><br/> <span data-ttu-id="c3766-128">如需詳細資訊，請參閱 <a href="asynchronous-mfts.md">非同步 MFTs</a>。</span><span class="sxs-lookup"><span data-stu-id="c3766-128">For more information, see <a href="asynchronous-mfts.md">Asynchronous MFTs</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3766-129">速率控制、訣竅模式或反向播放</span><span class="sxs-lookup"><span data-stu-id="c3766-129">Rate control, trick mode, or reverse playback</span></span></td>
<td><span data-ttu-id="c3766-130">請參閱 <a href="implementing-rate-control.md">執行速率控制</a>。</span><span class="sxs-lookup"><span data-stu-id="c3766-130">See <a href="implementing-rate-control.md">Implementing Rate Control</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3766-131">如果您的 MFT 建立執行緒 .。。</span><span class="sxs-lookup"><span data-stu-id="c3766-131">If your MFT creates threads...</span></span></td>
<td><span data-ttu-id="c3766-132">執行 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="c3766-132">Implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3766-133">如果您的 MFT 有授許可權制 .。。</span><span class="sxs-lookup"><span data-stu-id="c3766-133">If your MFT has licensing restrictions...</span></span></td>
<td><span data-ttu-id="c3766-134">請考慮使用「使用欄位」機制。</span><span class="sxs-lookup"><span data-stu-id="c3766-134">Consider using the field-of-use mechanism.</span></span> <span data-ttu-id="c3766-135">請參閱 <a href="field-of-use-restrictions.md">使用限制的領域</a>。</span><span class="sxs-lookup"><span data-stu-id="c3766-135">See <a href="field-of-use-restrictions.md">Field of Use Restrictions</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3766-136">如果您正在移植現有的 DirectX 媒體物件 (]) .。。</span><span class="sxs-lookup"><span data-stu-id="c3766-136">If you are porting an existing DirectX Media Object (DMO)...</span></span></td>
<td><span data-ttu-id="c3766-137">請參閱 <a href="comparison-of-mfts-and-dmos.md">MFTs 和 DMOs 的比較</a>。</span><span class="sxs-lookup"><span data-stu-id="c3766-137">See <a href="comparison-of-mfts-and-dmos.md">Comparison of MFTs and DMOs</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c3766-138">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="c3766-138">This section contains the following topics:</span></span>

-   [<span data-ttu-id="c3766-139">時間戳記和持續時間</span><span class="sxs-lookup"><span data-stu-id="c3766-139">Time Stamps and Durations</span></span>](time-stamps-and-durations.md)
-   [<span data-ttu-id="c3766-140">處理資料流程變更</span><span class="sxs-lookup"><span data-stu-id="c3766-140">Handling Stream Changes</span></span>](handling-stream-changes.md)
-   [<span data-ttu-id="c3766-141">執行編解碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="c3766-141">Implementing a Codec MFT</span></span>](implementing-a-codec-mft.md)
-   [<span data-ttu-id="c3766-142">Direct3D 感知 MFTs</span><span class="sxs-lookup"><span data-stu-id="c3766-142">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
-   [<span data-ttu-id="c3766-143">硬體 MFTs</span><span class="sxs-lookup"><span data-stu-id="c3766-143">Hardware MFTs</span></span>](hardware-mfts.md)
-   [<span data-ttu-id="c3766-144">編解碼器的優點</span><span class="sxs-lookup"><span data-stu-id="c3766-144">Codec Merit</span></span>](codec-merit.md)

## <a name="related-topics"></a><span data-ttu-id="c3766-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3766-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3766-146">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="c3766-146">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




