---
description: 事件屬性
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: '事件屬性 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510794"
---
# <a name="event-attributes-microsoft-media-foundation"></a><span data-ttu-id="feb36-103">事件屬性 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="feb36-103">Event Attributes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="feb36-104">下列屬性適用于事件。</span><span class="sxs-lookup"><span data-stu-id="feb36-104">The following attributes apply to events.</span></span>



| <span data-ttu-id="feb36-105">屬性</span><span class="sxs-lookup"><span data-stu-id="feb36-105">Attribute</span></span>                                                                                                        | <span data-ttu-id="feb36-106">描述</span><span class="sxs-lookup"><span data-stu-id="feb36-106">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="feb36-107">**MF \_ 事件 \_ DO \_ THINNING**</span><span class="sxs-lookup"><span data-stu-id="feb36-107">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)                                                | <span data-ttu-id="feb36-108">當媒體來源要求新的播放速率時，會指定來源是否也要求 thinning。</span><span class="sxs-lookup"><span data-stu-id="feb36-108">When a media source requests a new playback rate, specifies whether the source also requests thinning.</span></span>                |
| [<span data-ttu-id="feb36-109">**MF \_ 事件 \_ 輸出 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="feb36-109">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)                                                | <span data-ttu-id="feb36-110">識別資料流程接收的拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="feb36-110">Identifies the topology node for a stream sink.</span></span>                                                                       |
| [<span data-ttu-id="feb36-111">**MF \_ 事件 \_ 呈現 \_ 時間 \_ 位移**</span><span class="sxs-lookup"><span data-stu-id="feb36-111">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)                     | <span data-ttu-id="feb36-112">呈現時間與媒體來源時間戳記之間的位移。</span><span class="sxs-lookup"><span data-stu-id="feb36-112">Offset between the presentation time and the media source's time stamps.</span></span>                                              |
| [<span data-ttu-id="feb36-113">**MF \_ 事件 \_ SCRUBSAMPLE \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="feb36-113">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)                                      | <span data-ttu-id="feb36-114">在清除時轉譯之樣本的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="feb36-114">Presentation time for a sample that was rendered while scrubbing.</span></span>                                                     |
| [<span data-ttu-id="feb36-115">**MF \_ 事件 \_ SESSIONCAPS**</span><span class="sxs-lookup"><span data-stu-id="feb36-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)                                                 | <span data-ttu-id="feb36-116">包含根據目前的簡報定義媒體會話功能的旗標。</span><span class="sxs-lookup"><span data-stu-id="feb36-116">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>                  |
| [<span data-ttu-id="feb36-117">**MF \_ 事件 \_ SESSIONCAPS \_ 差異**</span><span class="sxs-lookup"><span data-stu-id="feb36-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md)                                    | <span data-ttu-id="feb36-118">包含旗標，這些旗標會根據目前的簡報，指出媒體會話中的哪些功能已變更。</span><span class="sxs-lookup"><span data-stu-id="feb36-118">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span> |
| [<span data-ttu-id="feb36-119">**MF \_ 事件 \_ 來源 \_ 實際 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="feb36-119">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)                               | <span data-ttu-id="feb36-120">包含媒體來源從其目前位置重新開機的開始時間。</span><span class="sxs-lookup"><span data-stu-id="feb36-120">Contains the start time when a media source restarts from its current position.</span></span>                                       |
| [<span data-ttu-id="feb36-121">**MF \_ 事件 \_ 來源 \_ 特性**</span><span class="sxs-lookup"><span data-stu-id="feb36-121">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)                          | <span data-ttu-id="feb36-122">指定媒體來源的目前特性。</span><span class="sxs-lookup"><span data-stu-id="feb36-122">Specifies the current characteristics of the media source.</span></span>                                                            |
| [<span data-ttu-id="feb36-123">**MF \_ 事件 \_ 來源 \_ 特性 \_ 舊**</span><span class="sxs-lookup"><span data-stu-id="feb36-123">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)                 | <span data-ttu-id="feb36-124">指定媒體來源的先前特性。</span><span class="sxs-lookup"><span data-stu-id="feb36-124">Specifies the previous characteristics of the media source.</span></span>                                                           |
| [<span data-ttu-id="feb36-125">**MF \_ 事件 \_ 來源 \_ 假 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="feb36-125">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)                                   | <span data-ttu-id="feb36-126">指定目前區段拓撲是否為空白。</span><span class="sxs-lookup"><span data-stu-id="feb36-126">Specifies whether the current segment topology is empty.</span></span>                                                              |
| [<span data-ttu-id="feb36-127">**MF \_ 事件 \_ 來源 \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="feb36-127">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)                                | <span data-ttu-id="feb36-128">指定區段拓撲的開始時間。</span><span class="sxs-lookup"><span data-stu-id="feb36-128">Specifies the start time for a segment topology.</span></span>                                                                      |
| [<span data-ttu-id="feb36-129">**\_已取消 MF 事件 \_ 來源 \_ 拓撲 \_**</span><span class="sxs-lookup"><span data-stu-id="feb36-129">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)                     | <span data-ttu-id="feb36-130">指定 sequencer 來源是否取消拓撲。</span><span class="sxs-lookup"><span data-stu-id="feb36-130">Specifies whether the sequencer source canceled a topology.</span></span>                                                           |
| [<span data-ttu-id="feb36-131">**MF \_ 事件 \_ 開始 \_ 簡報 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="feb36-131">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)                       | <span data-ttu-id="feb36-132">簡報的開始時間，以 100-納秒為單位，以呈現時鐘測量。</span><span class="sxs-lookup"><span data-stu-id="feb36-132">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>               |
| [<span data-ttu-id="feb36-133">**MF \_ 事件 \_ \_ \_ \_ 在輸出時開始展示時間 \_**</span><span class="sxs-lookup"><span data-stu-id="feb36-133">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md) | <span data-ttu-id="feb36-134">媒體接收器轉譯新拓撲第一個樣本的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="feb36-134">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>                      |
| [<span data-ttu-id="feb36-135">**MF \_ 事件 \_ 拓撲 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="feb36-135">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)                                        | <span data-ttu-id="feb36-136">指定播放期間拓撲的狀態。</span><span class="sxs-lookup"><span data-stu-id="feb36-136">Specifies the status of a topology during playback.</span></span>                                                                   |
| [<span data-ttu-id="feb36-137">**MF \_ 會話 \_ 大約 \_ 發生事件 \_ 發生 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="feb36-137">**MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME**</span></span>](mf-session-approx-event-occurrence-time-attribute.md)        | <span data-ttu-id="feb36-138">媒體會話引發事件的大約時間。</span><span class="sxs-lookup"><span data-stu-id="feb36-138">The approximate time when the Media Session raised an event.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="feb36-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="feb36-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feb36-140">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="feb36-140">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[<span data-ttu-id="feb36-141">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="feb36-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="feb36-142">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="feb36-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



