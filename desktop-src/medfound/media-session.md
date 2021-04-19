---
description: 媒體會話是管理管線中資料流程的物件。 它可用於播放和編碼檔案。
ms.assetid: dac99908-be90-415d-8837-2f97d573feb5
title: 媒體會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3df4597e5461788f990f620875bce946570ab97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981937"
---
# <a name="media-session"></a><span data-ttu-id="bf89f-104">媒體會話</span><span class="sxs-lookup"><span data-stu-id="bf89f-104">Media Session</span></span>

<span data-ttu-id="bf89f-105">媒體會話是管理管線中資料流程的物件。</span><span class="sxs-lookup"><span data-stu-id="bf89f-105">The Media Session is an object that manages data flow in the pipeline.</span></span> <span data-ttu-id="bf89f-106">它可用於播放和編碼檔案。</span><span class="sxs-lookup"><span data-stu-id="bf89f-106">It can be used for both playing and encoding files.</span></span>

<span data-ttu-id="bf89f-107">本節說明從架構的觀點來看的媒體會話。</span><span class="sxs-lookup"><span data-stu-id="bf89f-107">This section describes the Media Session from an architectural standpoint.</span></span> <span data-ttu-id="bf89f-108">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="bf89f-108">It contains the following sections:</span></span>



| <span data-ttu-id="bf89f-109">主題</span><span class="sxs-lookup"><span data-stu-id="bf89f-109">Topic</span></span>                                                                                        | <span data-ttu-id="bf89f-110">描述</span><span class="sxs-lookup"><span data-stu-id="bf89f-110">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf89f-111">關於媒體會話</span><span class="sxs-lookup"><span data-stu-id="bf89f-111">About the Media Session</span></span>](about-the-media-session.md)                                       | <span data-ttu-id="bf89f-112">提供媒體會話的總覽、應用程式如何建立媒體會話，以及媒體會話如何管理呈現時間。</span><span class="sxs-lookup"><span data-stu-id="bf89f-112">Provides an overview of the Media Session, how an application can create the Media Session, and how the Media Session manages presentation time.</span></span> |
| [<span data-ttu-id="bf89f-113">拓撲</span><span class="sxs-lookup"><span data-stu-id="bf89f-113">Topologies</span></span>](topologies.md)                                                                 | <span data-ttu-id="bf89f-114">拓撲是物件，代表管線中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="bf89f-114">A topology is an object that represents the flow of data in the pipeline.</span></span>                                                                        |
| [<span data-ttu-id="bf89f-115">媒體會話事件</span><span class="sxs-lookup"><span data-stu-id="bf89f-115">Media Session Events</span></span>](media-session-events.md)                                             | <span data-ttu-id="bf89f-116">描述應用程式可能會從媒體會話接收的事件。</span><span class="sxs-lookup"><span data-stu-id="bf89f-116">Describes the events that an application might receive from the Media Session.</span></span>                                                                   |
| [<span data-ttu-id="bf89f-117">如何控制簡報狀態</span><span class="sxs-lookup"><span data-stu-id="bf89f-117">How to Control Presentation States</span></span>](how-to-control-presentation-states.md)                 | <span data-ttu-id="bf89f-118">描述媒體會話傳輸控制項：播放、暫停和停止。</span><span class="sxs-lookup"><span data-stu-id="bf89f-118">Describes the Media Session transport controls: Play, Pause, and Stop.</span></span>                                                                           |
| [<span data-ttu-id="bf89f-119">以媒體會話使用媒體來源</span><span class="sxs-lookup"><span data-stu-id="bf89f-119">Using Media Sources with the Media Session</span></span>](using-media-sources-with-the-media-session.md) | <span data-ttu-id="bf89f-120">如何搭配媒體會話使用媒體來源。</span><span class="sxs-lookup"><span data-stu-id="bf89f-120">How to use media sources with the Media Session.</span></span>                                                                                                 |
| [<span data-ttu-id="bf89f-121">速率控制</span><span class="sxs-lookup"><span data-stu-id="bf89f-121">Rate Control</span></span>](rate-control.md)                                                             | <span data-ttu-id="bf89f-122">說明如何控制播放速率。</span><span class="sxs-lookup"><span data-stu-id="bf89f-122">Describes how to control playback rate.</span></span>                                                                                                          |
| [<span data-ttu-id="bf89f-123">影片品質管制</span><span class="sxs-lookup"><span data-stu-id="bf89f-123">Video Quality Management</span></span>](video-quality-management.md)                                     | <span data-ttu-id="bf89f-124">說明 Windows 7 中視頻管線的增強功能。</span><span class="sxs-lookup"><span data-stu-id="bf89f-124">Describes improvements to the video pipeline in Windows 7.</span></span>                                                                                       |
| [<span data-ttu-id="bf89f-125">PMP 媒體會話</span><span class="sxs-lookup"><span data-stu-id="bf89f-125">PMP Media Session</span></span>](pmp-media-session.md)                                                   | <span data-ttu-id="bf89f-126">說明如何在受保護的媒體路徑內建立媒體會話 (PMP) 進程。</span><span class="sxs-lookup"><span data-stu-id="bf89f-126">Describes how to create the Media Session inside a Protected Media Path (PMP) process.</span></span>                                                           |



 

<span data-ttu-id="bf89f-127">下列主題說明如何在特定應用程式案例中使用媒體會話：</span><span class="sxs-lookup"><span data-stu-id="bf89f-127">The following topics describe how to use the Media Session in specific application scenarios:</span></span>

-   [<span data-ttu-id="bf89f-128">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="bf89f-128">Audio/Video Playback</span></span>](audio-video-playback.md)
-   [<span data-ttu-id="bf89f-129">編碼與檔案編寫</span><span class="sxs-lookup"><span data-stu-id="bf89f-129">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)

## <a name="related-topics"></a><span data-ttu-id="bf89f-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf89f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf89f-131">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="bf89f-131">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="bf89f-132">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="bf89f-132">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> </dl>

 

 



