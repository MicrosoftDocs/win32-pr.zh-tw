---
description: 媒體基礎平臺 Api
ms.assetid: 1eb20c44-58cb-4e34-a108-1b3c27d54ff1
title: 媒體基礎平臺 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1e8d8aa0dcd5d7b1184a406e09910a98892f4f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106974757"
---
# <a name="media-foundation-platform-apis"></a><span data-ttu-id="4bd90-103">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="4bd90-103">Media Foundation Platform APIs</span></span>

<span data-ttu-id="4bd90-104">媒體基礎的平台層包含其他層所使用的基本和 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="4bd90-104">The platform layer of Media Foundation contains primitives and helper objects used by the other layers.</span></span>

<span data-ttu-id="4bd90-105">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="4bd90-105">This section contains the following topics:</span></span>



| <span data-ttu-id="4bd90-106">主題</span><span class="sxs-lookup"><span data-stu-id="4bd90-106">Topic</span></span>                                                                           | <span data-ttu-id="4bd90-107">描述</span><span class="sxs-lookup"><span data-stu-id="4bd90-107">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bd90-108">初始化媒體基礎平臺</span><span class="sxs-lookup"><span data-stu-id="4bd90-108">Initializing the Media Foundation Platform</span></span>](initializing-media-foundation.md) | <span data-ttu-id="4bd90-109">如何初始化媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="4bd90-109">How to initialize the Media Foundation platform.</span></span>                                                                                                                  |
| [<span data-ttu-id="4bd90-110">媒體基礎和 COM</span><span class="sxs-lookup"><span data-stu-id="4bd90-110">Media Foundation and COM</span></span>](media-foundation-and-com.md)                        | <span data-ttu-id="4bd90-111">描述 COM 與 Microsoft 媒體基礎之間的互動，並定義開發媒體基礎外掛程式元件時所使用的一些最佳作法。</span><span class="sxs-lookup"><span data-stu-id="4bd90-111">Describes the interaction between COM and Microsoft Media Foundation, and defines some best practices to use when developing Media Foundation plug-in components.</span></span> |
| [<span data-ttu-id="4bd90-112">非同步回呼方法</span><span class="sxs-lookup"><span data-stu-id="4bd90-112">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)              | <span data-ttu-id="4bd90-113">如何呼叫非同步方法，以及如何在媒體基礎中執行非同步作業。</span><span class="sxs-lookup"><span data-stu-id="4bd90-113">How to call asynchronous methods and how to implement asynchronous operations in Media Foundation.</span></span>                                                                |
| [<span data-ttu-id="4bd90-114">工作佇列</span><span class="sxs-lookup"><span data-stu-id="4bd90-114">Work Queues</span></span>](work-queues.md)                                                  | <span data-ttu-id="4bd90-115">工作佇列是在另一個執行緒上執行非同步作業的有效方式。</span><span class="sxs-lookup"><span data-stu-id="4bd90-115">A work queue is an efficient way to perform asynchronous operations on another thread.</span></span>                                                                            |
| [<span data-ttu-id="4bd90-116">媒體事件產生器</span><span class="sxs-lookup"><span data-stu-id="4bd90-116">Media Event Generators</span></span>](media-event-generators.md)                            | <span data-ttu-id="4bd90-117">如何接收非同步事件，以及如何在媒體基礎中引發事件。</span><span class="sxs-lookup"><span data-stu-id="4bd90-117">How to receive asynchronous events and how to raise events in Media Foundation.</span></span>                                                                                   |
| [<span data-ttu-id="4bd90-118">服務介面</span><span class="sxs-lookup"><span data-stu-id="4bd90-118">Service Interfaces</span></span>](service-interfaces.md)                                    | <span data-ttu-id="4bd90-119">服務介面是一個物件所提供的 COM 介面，但會透過另一個物件公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="4bd90-119">A service interface is a COM interface provided by one object, but exposed to the application through another object.</span></span>                                             |
| [<span data-ttu-id="4bd90-120">啟用物件</span><span class="sxs-lookup"><span data-stu-id="4bd90-120">Activation Objects</span></span>](activation-objects.md)                                    | <span data-ttu-id="4bd90-121">啟用物件是建立另一個物件的物件。</span><span class="sxs-lookup"><span data-stu-id="4bd90-121">An activation object is an object that creates another object.</span></span>                                                                                                    |
| [<span data-ttu-id="4bd90-122">簡報時鐘</span><span class="sxs-lookup"><span data-stu-id="4bd90-122">Presentation Clock</span></span>](presentation-clock.md)                                    | <span data-ttu-id="4bd90-123">簡報時鐘會產生用來控制播放的時鐘時間，以及同步的音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="4bd90-123">The presentation clock generates the clock time that is used to control playback, and also to synchronous audio and video streams.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="4bd90-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="4bd90-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bd90-125">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="4bd90-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="4bd90-126">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="4bd90-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



