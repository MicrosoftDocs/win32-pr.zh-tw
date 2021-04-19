---
description: 拓撲屬性
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: 拓撲屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286b6dbfe922461083b49d77ad2351e98d562d3b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106998992"
---
# <a name="topology-attributes"></a><span data-ttu-id="38b6f-103">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="38b6f-103">Topology Attributes</span></span>

<span data-ttu-id="38b6f-104">下列屬性適用于拓撲。</span><span class="sxs-lookup"><span data-stu-id="38b6f-104">The following attributes apply to topologies.</span></span>



| <span data-ttu-id="38b6f-105">屬性</span><span class="sxs-lookup"><span data-stu-id="38b6f-105">Attribute</span></span>                                                                                                | <span data-ttu-id="38b6f-106">描述</span><span class="sxs-lookup"><span data-stu-id="38b6f-106">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38b6f-107">MF \_ 拓撲 \_ DXVA \_ 模式</span><span class="sxs-lookup"><span data-stu-id="38b6f-107">MF\_TOPOLOGY\_DXVA\_MODE</span></span>](mf-topology-dxva-mode.md)                                                    | <span data-ttu-id="38b6f-108">指定拓撲載入器是否會啟用拓撲中的 Microsoft DirectX Video 加速 (DXVA) 。</span><span class="sxs-lookup"><span data-stu-id="38b6f-108">Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.</span></span>                                                                                                                         |
| [<span data-ttu-id="38b6f-109">\_ \_ \_ \_ 不 \_ 允許使用 MF 拓撲動態變更</span><span class="sxs-lookup"><span data-stu-id="38b6f-109">MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED</span></span>](mf-topology-dynamic-change-not-allowed.md)                | <span data-ttu-id="38b6f-110">指定當資料流程的格式變更時，媒體會話是否嘗試修改拓撲。</span><span class="sxs-lookup"><span data-stu-id="38b6f-110">Specifies whether the Media Session attempts to modify the topology when the format of a stream changes.</span></span>                                                                                                                           |
| [<span data-ttu-id="38b6f-111">MF \_ 拓撲可 \_ 啟用 \_ XVP \_ 來 \_ 播放</span><span class="sxs-lookup"><span data-stu-id="38b6f-111">MF\_TOPOLOGY\_ENABLE\_XVP\_FOR\_PLAYBACK</span></span>](mf-topology-enable-xvp-for-playback.md)                | <span data-ttu-id="38b6f-112">指定拓撲載入器是否會啟用轉碼視頻處理器 (XVP) 。</span><span class="sxs-lookup"><span data-stu-id="38b6f-112">Specifies whether the topology loader enables the Transcode Video Processor (XVP).</span></span> <span data-ttu-id="38b6f-113">針對轉換，啟用硬體加速色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="38b6f-113">for conversions, enabling hardware accelerated color conversion.</span></span>                                                                                        |
| [<span data-ttu-id="38b6f-114">MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="38b6f-114">MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES</span></span>](mf-topology-enumerate-source-types.md)                         | <span data-ttu-id="38b6f-115">指定拓撲載入器是否列舉媒體來源所提供的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="38b6f-115">Specifies whether the topology loader enumerates the media types provided by the media source.</span></span>                                                                                                                                     |
| [<span data-ttu-id="38b6f-116">MF \_ 拓撲 \_ 硬體 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="38b6f-116">MF\_TOPOLOGY\_HARDWARE\_MODE</span></span>](mf-topology-hardware-mode.md)                                            | <span data-ttu-id="38b6f-117">指定是否要在拓撲中包含以硬體為基礎的轉換。</span><span class="sxs-lookup"><span data-stu-id="38b6f-117">Specifies whether to include hardware-based transforms in the topology.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="38b6f-118">**MF \_ 拓撲 \_ 無 \_ MARKIN \_ MARKOUT**</span><span class="sxs-lookup"><span data-stu-id="38b6f-118">**MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT**</span></span>](mf-topology-no-markin-markout-attribute.md)                     | <span data-ttu-id="38b6f-119">指定管線是否修剪範例。</span><span class="sxs-lookup"><span data-stu-id="38b6f-119">Specifies whether the pipeline trims samples.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="38b6f-120">MF \_ 拓撲 \_ 播放 \_ 畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="38b6f-120">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span>](mf-topology-playback-framerate.md)                                  | <span data-ttu-id="38b6f-121">指定監視器的重新整理頻率。</span><span class="sxs-lookup"><span data-stu-id="38b6f-121">Specifies the monitor refresh rate.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="38b6f-122">MF \_ 拓撲 \_ 播放 \_ 最大 \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="38b6f-122">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span>](mf-topology-playback-max-dims.md)                                   | <span data-ttu-id="38b6f-123">指定影片播放的目的地視窗大小。</span><span class="sxs-lookup"><span data-stu-id="38b6f-123">Specifies the size of the destination window for video playback.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="38b6f-124">**MF \_ 拓撲 \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="38b6f-124">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)                                 | <span data-ttu-id="38b6f-125">指定目前區段內的拓撲開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="38b6f-125">Specifies the topology start time within the current segment, in 100-nanosecond units.</span></span>                                                                                                                                             |
| [<span data-ttu-id="38b6f-126">**MF \_ 拓撲 \_ PROJECTSTOP**</span><span class="sxs-lookup"><span data-stu-id="38b6f-126">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)                                   | <span data-ttu-id="38b6f-127">指定目前區段內的拓撲停止時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="38b6f-127">Specifies the topology stop time within the current segment, in 100-nanosecond units.</span></span>                                                                                                                                              |
| [<span data-ttu-id="38b6f-128">**MF \_ 拓撲 \_ 解決 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="38b6f-128">**MF\_TOPOLOGY\_RESOLUTION\_STATUS**</span></span>](mf-topology-resolution-status-attribute.md)                      | <span data-ttu-id="38b6f-129">指定嘗試解析拓撲的狀態。</span><span class="sxs-lookup"><span data-stu-id="38b6f-129">Specifies the status of an attempt to resolve a topology.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="38b6f-130">\_ \_ \_ \_ \_ 展示參數上的 \_ MF 拓撲開始時間</span><span class="sxs-lookup"><span data-stu-id="38b6f-130">MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH</span></span>](mf-topology-start-time-on-presentation-switch.md) | <span data-ttu-id="38b6f-131">指定在第一個簡報之後排入的簡報開始時間。</span><span class="sxs-lookup"><span data-stu-id="38b6f-131">Specifies the start time for presentations that are queued after the first presentation.</span></span>                                                                                                                                           |
| [<span data-ttu-id="38b6f-132">MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化</span><span class="sxs-lookup"><span data-stu-id="38b6f-132">MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS</span></span>](mf-topology-static-playback-optimizations.md)           | <span data-ttu-id="38b6f-133">啟用影片管線中的靜態優化。</span><span class="sxs-lookup"><span data-stu-id="38b6f-133">Enables static optimizations in the video pipeline.</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="38b6f-134">MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="38b6f-134">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)                                | <span data-ttu-id="38b6f-135">包含 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 指標，用來將具有使用規定限制的 MFT 解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="38b6f-135">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which is used to unlock an MFT with field-of-use restrictions.</span></span> <span data-ttu-id="38b6f-136">如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="38b6f-136">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="38b6f-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="38b6f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b6f-138">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="38b6f-138">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[<span data-ttu-id="38b6f-139">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="38b6f-139">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="38b6f-140">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="38b6f-140">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 



