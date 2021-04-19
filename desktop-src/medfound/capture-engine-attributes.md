---
description: 您可以使用下列屬性來設定「捕獲引擎」。
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Capture 引擎屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1340fa69f80d456a29331d303f313d41c31ee41
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "107000527"
---
# <a name="capture-engine-attributes"></a><span data-ttu-id="3eb98-103">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="3eb98-103">Capture Engine Attributes</span></span>

<span data-ttu-id="3eb98-104">您可以使用下列屬性來設定「捕獲引擎」。</span><span class="sxs-lookup"><span data-stu-id="3eb98-104">The following attributes can be used to configure the Capture Engine.</span></span>

<span data-ttu-id="3eb98-105">下列是與 capture 裝置相關的屬性：</span><span class="sxs-lookup"><span data-stu-id="3eb98-105">The following attributes are related to capture devices:</span></span>



| <span data-ttu-id="3eb98-106">屬性</span><span class="sxs-lookup"><span data-stu-id="3eb98-106">Attribute</span></span>                                                                                                                              | <span data-ttu-id="3eb98-107">描述</span><span class="sxs-lookup"><span data-stu-id="3eb98-107">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3eb98-108">已 \_ 封鎖 MF 捕獲 \_ 引擎 \_ 相機 \_ 串流 \_</span><span class="sxs-lookup"><span data-stu-id="3eb98-108">MF\_CAPTURE\_ENGINE\_CAMERA\_STREAM\_BLOCKED</span></span>](mf-capture-engine-camera-stream-blocked.md)                                            | <span data-ttu-id="3eb98-109">發出驅動程式封鎖視頻捕捉的信號。</span><span class="sxs-lookup"><span data-stu-id="3eb98-109">Signals that video capture is being blocked by the driver.</span></span>                                                         |
| [<span data-ttu-id="3eb98-110">已 \_ \_ 解除封鎖 MF 捕獲引擎 \_ 相機 \_ 串流 \_</span><span class="sxs-lookup"><span data-stu-id="3eb98-110">MF\_CAPTURE\_ENGINE\_CAMERA\_STREAM\_UNBLOCKED</span></span>](mf-capture-engine-camera-stream-unblocked.md)                                        | <span data-ttu-id="3eb98-111">通知影片捕捉在封鎖後會還原。</span><span class="sxs-lookup"><span data-stu-id="3eb98-111">Signals that video capture is restored after being blocked.</span></span>                                                        |
| [<span data-ttu-id="3eb98-112">MF \_ 捕獲 \_ 引擎 \_ D3D \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="3eb98-112">MF\_CAPTURE\_ENGINE\_D3D\_MANAGER</span></span>](mf-capture-engine-d3d-manager.md)                                                                 | <span data-ttu-id="3eb98-113">在 capture 引擎上設定 DXGI 裝置管理員的指標。</span><span class="sxs-lookup"><span data-stu-id="3eb98-113">Sets a pointer to the DXGI Device Manager on the capture engine.</span></span>                                                   |
| [<span data-ttu-id="3eb98-114">MF \_ CAPTURE \_ ENGINE \_ 解碼器 \_ MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="3eb98-114">MF\_CAPTURE\_ENGINE\_DECODER\_MFT\_FIELDOFUSE\_UNLOCK\_ATTRIBUTE</span></span>](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | <span data-ttu-id="3eb98-115">讓 capture engine 使用具有使用規定限制的解碼器。</span><span class="sxs-lookup"><span data-stu-id="3eb98-115">Enables the capture engine to use a decoder that has field-of-use restrictions.</span></span>                                    |
| [<span data-ttu-id="3eb98-116">MF \_ 捕獲 \_ 引擎 \_ 停用 \_ DXVA</span><span class="sxs-lookup"><span data-stu-id="3eb98-116">MF\_CAPTURE\_ENGINE\_DISABLE\_DXVA</span></span>](mf-capture-engine-disable-dxva.md)                                                               | <span data-ttu-id="3eb98-117">指定捕捉引擎是否使用 DirectX Video 加速 (DXVA) 進行影片解碼。</span><span class="sxs-lookup"><span data-stu-id="3eb98-117">Specifies whether the capture engine uses DirectX Video Acceleration (DXVA) for video decoding.</span></span>                    |
| [<span data-ttu-id="3eb98-118">MF \_ 捕獲 \_ 停用 \_ 硬體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="3eb98-118">MF\_CAPTURE\_DISABLE\_HARDWARE\_TRANSFORMS</span></span>](mf-capture-engine-disable-hardware-transforms.md)                                        | <span data-ttu-id="3eb98-119">停用在 capture 引擎中 (MFTs) 的硬體媒體基礎轉換。</span><span class="sxs-lookup"><span data-stu-id="3eb98-119">Disables the use of hardware-based Media Foundation transforms (MFTs) in the capture engine.</span></span>                       |
| [<span data-ttu-id="3eb98-120">MF \_ 捕獲 \_ 引擎 \_ 啟用 \_ 攝影機 \_ STREAMSTATE \_ 通知</span><span class="sxs-lookup"><span data-stu-id="3eb98-120">MF\_CAPTURE\_ENGINE\_ENABLE\_CAMERA\_STREAMSTATE\_NOTIFICATION</span></span>](mf-capture-engine-enable-camera-streamstate-notification.md)         | <span data-ttu-id="3eb98-121">指出是否應該啟用資料流程狀態通知。</span><span class="sxs-lookup"><span data-stu-id="3eb98-121">Indicates whether stream state notifications should be enabled.</span></span>                                                    |
| [<span data-ttu-id="3eb98-122">MF \_ 捕獲 \_ 引擎 \_ 編碼器 \_ MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="3eb98-122">MF\_CAPTURE\_ENGINE\_ENCODER\_MFT\_FIELDOFUSE\_UNLOCK\_ATTRIBUTE</span></span>](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | <span data-ttu-id="3eb98-123">讓 capture engine 使用具有使用規定限制的編碼器。</span><span class="sxs-lookup"><span data-stu-id="3eb98-123">Enables the capture engine to use an encoder that has field-of-use restrictions.</span></span>                                   |
| [<span data-ttu-id="3eb98-124">MF \_ 捕獲 \_ 引擎 \_ 事件產生器 \_ \_ GUID</span><span class="sxs-lookup"><span data-stu-id="3eb98-124">MF\_CAPTURE\_ENGINE\_EVENT\_GENERATOR\_GUID</span></span>](mf-capture-engine-event-generator-guid.md)                                              | <span data-ttu-id="3eb98-125">識別產生 capture 事件的元件。</span><span class="sxs-lookup"><span data-stu-id="3eb98-125">Identifies the component that generated a capture event.</span></span>                                                           |
| [<span data-ttu-id="3eb98-126">MF \_ 捕獲 \_ 引擎 \_ 事件 \_ 資料流程 \_ 索引</span><span class="sxs-lookup"><span data-stu-id="3eb98-126">MF\_CAPTURE\_ENGINE\_EVENT\_STREAM\_INDEX</span></span>](mf-capture-engine-event-stream-index.md)                                                  | <span data-ttu-id="3eb98-127">識別哪個資料流程產生了捕捉事件。</span><span class="sxs-lookup"><span data-stu-id="3eb98-127">Identifies which stream generated a capture event.</span></span>                                                                 |
| [<span data-ttu-id="3eb98-128">MF \_ CAPTURE \_ ENGINE \_ MEDIASOURCE \_ CONFIG</span><span class="sxs-lookup"><span data-stu-id="3eb98-128">MF\_CAPTURE\_ENGINE\_MEDIASOURCE\_CONFIG</span></span>](mf-capture-engine-mediasource-config.md)                                                   | <span data-ttu-id="3eb98-129">包含 capture 來源的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="3eb98-129">Contains configuration properties for the capture source.</span></span>                                                          |
| [<span data-ttu-id="3eb98-130">MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 音訊 \_ 最大 \_ 處理 \_ 範例</span><span class="sxs-lookup"><span data-stu-id="3eb98-130">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_PROCESSED\_SAMPLES</span></span>](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | <span data-ttu-id="3eb98-131">設定可在記錄接收音訊路徑中緩衝處理之已處理樣本的最大數目。</span><span class="sxs-lookup"><span data-stu-id="3eb98-131">Sets the maximum number of processed samples that can be buffered in the record sink audio path.</span></span>                   |
| [<span data-ttu-id="3eb98-132">MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 音訊 \_ 最 \_ 大 \_ 未處理範例</span><span class="sxs-lookup"><span data-stu-id="3eb98-132">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES</span></span>](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | <span data-ttu-id="3eb98-133">設定可在記錄接收音訊路徑中進行緩衝處理的未處理樣本數上限。</span><span class="sxs-lookup"><span data-stu-id="3eb98-133">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink audio path..</span></span> |
| [<span data-ttu-id="3eb98-134">MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 影片的 \_ 最大 \_ 處理 \_ 範例</span><span class="sxs-lookup"><span data-stu-id="3eb98-134">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_PROCESSED\_SAMPLES</span></span>](mf-capture-engine-record-sink-video-max-processed-samples.md)     | <span data-ttu-id="3eb98-135">設定可在記錄接收影片路徑中緩衝處理之已處理樣本的最大數目。</span><span class="sxs-lookup"><span data-stu-id="3eb98-135">Sets the maximum number of processed samples that can be buffered in the record sink video path.</span></span>                   |
| [<span data-ttu-id="3eb98-136">MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 影片的 \_ 最大 \_ \_ 未處理範例</span><span class="sxs-lookup"><span data-stu-id="3eb98-136">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES</span></span>](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | <span data-ttu-id="3eb98-137">設定可在記錄接收影片路徑中緩衝處理的未處理樣本數上限。</span><span class="sxs-lookup"><span data-stu-id="3eb98-137">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink video path.</span></span>  |
| [<span data-ttu-id="3eb98-138">MF \_ 捕獲 \_ 引擎 \_ 接收 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="3eb98-138">MF\_CAPTURE\_ENGINE\_SINK\_TYPE</span></span>](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | <span data-ttu-id="3eb98-139">指定捕捉接收的類型。</span><span class="sxs-lookup"><span data-stu-id="3eb98-139">Specifies a type of capture sink.</span></span>                                                                                  |
| [<span data-ttu-id="3eb98-140">MF \_ 捕獲 \_ 引擎 \_ \_ 僅使用音訊 \_ 裝置 \_</span><span class="sxs-lookup"><span data-stu-id="3eb98-140">MF\_CAPTURE\_ENGINE\_USE\_AUDIO\_DEVICE\_ONLY</span></span>](mf-capture-engine-use-audio-device-only.md)                                           | <span data-ttu-id="3eb98-141">指定捕捉引擎是否會捕捉音訊，但不會捕捉影片。</span><span class="sxs-lookup"><span data-stu-id="3eb98-141">Specifies whether the capture engine captures audio but not video.</span></span>                                                 |
| [<span data-ttu-id="3eb98-142">MF \_ 捕獲 \_ 引擎 \_ \_ 僅使用影片 \_ 裝置 \_</span><span class="sxs-lookup"><span data-stu-id="3eb98-142">MF\_CAPTURE\_ENGINE\_USE\_VIDEO\_DEVICE\_ONLY</span></span>](mf-capture-engine-use-video-device-only.md)                                           | <span data-ttu-id="3eb98-143">指定捕捉引擎是否要捕獲影片，而非音訊。</span><span class="sxs-lookup"><span data-stu-id="3eb98-143">Specifies whether the capture engine captures video but not audio.</span></span>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="3eb98-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="3eb98-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eb98-145">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="3eb98-145">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3eb98-146">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="3eb98-146">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 



