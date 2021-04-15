---
description: 關於 Sequencer 來源
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: 關於 Sequencer 來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511736"
---
# <a name="about-the-sequencer-source"></a><span data-ttu-id="c4a6b-103">關於 Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="c4a6b-103">About the Sequencer Source</span></span>

<span data-ttu-id="c4a6b-104">Sequencer 來源可讓應用程式依序播放 [媒體來源](media-sources.md) 的集合，並在來源之間進行無縫轉換。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-104">The sequencer source enables an application to play a collection of [Media Sources](media-sources.md) sequentially, with seamless transitions between the sources.</span></span> <span data-ttu-id="c4a6b-105">Sequencer 來源可以用於下列案例：</span><span class="sxs-lookup"><span data-stu-id="c4a6b-105">The sequencer source can be used for the following scenarios:</span></span>

-   <span data-ttu-id="c4a6b-106">建立可順暢地從某個媒體來源切換至下一個媒體來源的播放清單。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-106">Create a playlist that switches seamlessly from one media source to the next.</span></span>
-   <span data-ttu-id="c4a6b-107">同時播放多個來源的資料流程;例如，從另一個檔案中的影片播放音訊。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-107">Play streams from multiple sources simultaneously; for example, play the audio from one file with the video from another.</span></span>
-   <span data-ttu-id="c4a6b-108">在連續播放清單專案中，于不同媒體來源的串流之間切換;例如，在每個專案都包含不同的音訊來源時，播放清單可以有共用相同影片來源的專案。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-108">Switch between streams in different media sources in consecutive playlist entries; for example, a playlist can have entries that share the same video source while each entry contains a different audio source.</span></span>

<span data-ttu-id="c4a6b-109">針對播放清單的每個元素，應用程式會建立個別的拓撲。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-109">For each element of a playlist, the application creates a separate topology.</span></span> <span data-ttu-id="c4a6b-110">這些拓撲中的媒體來源稱為 *原生來源*，可區別它們與 sequencer 來源。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-110">The media sources in these topologies are referred to as *native sources*, to distinguish them from the sequencer source.</span></span> <span data-ttu-id="c4a6b-111">在播放期間，整個拓撲順序稱為 *簡報*，而序列內的每個拓撲都稱為 *區段*。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-111">During playback, the entire sequence of topologies is called a *presentation*, and each topology within the sequence is called a *segment*.</span></span>

<span data-ttu-id="c4a6b-112">播放是由 [媒體會話](media-session.md)控制，提供傳輸控制項，例如播放、暫停和停止。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-112">Playback is controlled by the [Media Session](media-session.md), which provides transport controls, such as play, pause, and stop.</span></span> <span data-ttu-id="c4a6b-113">媒體會話也會管理展示時間，並將事件傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-113">The Media Session also manages the presentation time and sends events to the application.</span></span> <span data-ttu-id="c4a6b-114">從 sequencer 來源 (事件會透過媒體會話轉送至應用程式。 ) </span><span class="sxs-lookup"><span data-stu-id="c4a6b-114">(Events from the sequencer source are forwarded to the application through the Media Session.)</span></span>

<span data-ttu-id="c4a6b-115">若要建立播放清單，應用程式會建立一或多個播放拓撲，並以所需的播放順序將它們排入 sequencer 來源上。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-115">To create a playlist, the application creates one or more playback topologies and queues them on the sequencer source in the desired order of playback.</span></span> <span data-ttu-id="c4a6b-116">就內部而言，sequencer 來源會修改拓撲，使來源節點指向 sequencer 來源，而不是原生來源。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-116">Internally, the sequencer source modifies the topologies so that the source nodes point to the sequencer source instead of the native source.</span></span> <span data-ttu-id="c4a6b-117">應用程式會將這些修改過的拓撲（而不是原始的拓撲）傳送至媒體會話。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-117">The application sends these modified topologies, rather than the original topologies, to the Media Session.</span></span> <span data-ttu-id="c4a6b-118">這可讓 sequencer 來源匯總原生來源，以及與媒體會話進行通訊。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-118">This enables the sequencer source to aggregate the native sources and to communicate with the Media Session.</span></span>

<span data-ttu-id="c4a6b-119">若要在區段之間達成無縫轉換，sequencer 來源會 prerolls 每個區段。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-119">To achieve seamless transitions between segments, the sequencer source prerolls each segment.</span></span> <span data-ttu-id="c4a6b-120">當一個區段現正播放，而且在開始播放下列區段之前，sequencer 來源會引發包含展示描述項的 [MENewPresentation](menewpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-120">While one segment is playing, and before it is time to play the following segment, the sequencer source fires an [MENewPresentation](menewpresentation.md) event that contains a presentation descriptor.</span></span> <span data-ttu-id="c4a6b-121">應用程式會使用這個展示描述項來取得簡報中下一個區段的拓撲，並將拓撲排入媒體會話上的佇列。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-121">The application uses this presentation descriptor to get the topology for the next segment in the presentation, and queues the topology on the Media Session.</span></span>

<span data-ttu-id="c4a6b-122">下圖顯示透過 sequencer 來源的播放清單專案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-122">The following illustration shows the data flow for playlist entries through the sequencer source.</span></span> <span data-ttu-id="c4a6b-123">應用程式會使用來源解析程式來建立原生來源、為每個區段建立拓撲，以及將拓撲排入 sequencer 來源上的佇列。</span><span class="sxs-lookup"><span data-stu-id="c4a6b-123">The application uses the source resolver to create the native sources, builds topologies for each segment, and queues the topologies on the sequencer source.</span></span>

![顯示 imfmediasession、imfsequencersource 和播放清單區段之資料流程的圖表，這些區段會導致 imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a><span data-ttu-id="c4a6b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4a6b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4a6b-126">如何建立播放清單</span><span class="sxs-lookup"><span data-stu-id="c4a6b-126">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="c4a6b-127">拓撲</span><span class="sxs-lookup"><span data-stu-id="c4a6b-127">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="c4a6b-128">使用 Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="c4a6b-128">Using the Sequencer Source</span></span>](using-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="c4a6b-129">Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="c4a6b-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



