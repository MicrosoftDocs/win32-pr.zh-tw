---
description: SQL-DMO 架構
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: SQL-DMO 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106995796"
---
# <a name="dmo-architecture"></a><span data-ttu-id="8e50c-103">SQL-DMO 架構</span><span class="sxs-lookup"><span data-stu-id="8e50c-103">DMO Architecture</span></span>

<span data-ttu-id="8e50c-104">本章節描述的是 SQL-DMO 的整體架構。</span><span class="sxs-lookup"><span data-stu-id="8e50c-104">This section describes the overall architecture of a DMO.</span></span>

<span data-ttu-id="8e50c-105">**串流**</span><span class="sxs-lookup"><span data-stu-id="8e50c-105">**Streams**</span></span>

<span data-ttu-id="8e50c-106">SQL-DMO 是接受 *m* 輸入並產生 *n* 輸出的物件。</span><span class="sxs-lookup"><span data-stu-id="8e50c-106">A DMO is an object that takes *m* inputs and produces *n* outputs.</span></span> <span data-ttu-id="8e50c-107">輸入和輸出稱為 *資料流程*。</span><span class="sxs-lookup"><span data-stu-id="8e50c-107">The inputs and outputs are called *streams*.</span></span> <span data-ttu-id="8e50c-108">每個的每個，都至少有一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="8e50c-108">Every DMO has at least one stream.</span></span> <span data-ttu-id="8e50c-109">資料流程不是物件;它們只是在每個索引編號的上參考。</span><span class="sxs-lookup"><span data-stu-id="8e50c-109">Streams are not objects; they are simply referenced on the DMO by index number.</span></span> <span data-ttu-id="8e50c-110">資料流程的數目會在設計階段修正。</span><span class="sxs-lookup"><span data-stu-id="8e50c-110">The number of streams is fixed at design time.</span></span>

<span data-ttu-id="8e50c-111">**媒體類型**</span><span class="sxs-lookup"><span data-stu-id="8e50c-111">**Media Types**</span></span>

<span data-ttu-id="8e50c-112">所有資料都是使用 *媒體類型* 來輸入，它會定義如何解讀資料的內容。</span><span class="sxs-lookup"><span data-stu-id="8e50c-112">All data is typed using a *media type*, which defines how to interpret the contents of the data.</span></span> <span data-ttu-id="8e50c-113">例如，320 x 240 24 位 RGB video 是一種類型;44.1-千赫茲 (kHz) 16 位身歷聲 PCM 音訊是另一種類型。</span><span class="sxs-lookup"><span data-stu-id="8e50c-113">For example, 320 x 240 24-bit RGB video is one type; 44.1-kilohertz (kHz) 16-bit stereo PCM audio is another type.</span></span> <span data-ttu-id="8e50c-114">媒體類型是使用 [**Sql-dmo \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) 結構來描述。</span><span class="sxs-lookup"><span data-stu-id="8e50c-114">Media types are described using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="8e50c-115">在用戶端可以處理任何資料之前，必須先設定每個資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="8e50c-115">Before the client can process any data, it must set the media type for each stream on the DMO.</span></span>

<span data-ttu-id="8e50c-116">一般而言，資料流程可以接受一系列的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="8e50c-116">Typically, a stream can accept a range of media types.</span></span> <span data-ttu-id="8e50c-117">有些 DMOs 支援比其他類型更廣泛的型別。</span><span class="sxs-lookup"><span data-stu-id="8e50c-117">Some DMOs support a wider range of types than others.</span></span> <span data-ttu-id="8e50c-118">SQL-DMO 介面會定義方法，讓用戶端探索支援的類型。</span><span class="sxs-lookup"><span data-stu-id="8e50c-118">The DMO interfaces define methods for the client to discover the supported types.</span></span> <span data-ttu-id="8e50c-119">例如，一個的一，可能會在任何位深度支援 RGB 影片，而另一種則可能只支援24位 RGB。</span><span class="sxs-lookup"><span data-stu-id="8e50c-119">For example, one DMO might support RGB video at any bit depth, while another might support only 24-bit RGB.</span></span> <span data-ttu-id="8e50c-120">此外，每個輸入和輸出的組合也可能受限於。</span><span class="sxs-lookup"><span data-stu-id="8e50c-120">Also, a DMO might be limited to certain combinations of inputs and outputs.</span></span> <span data-ttu-id="8e50c-121">例如，如果輸入類型是16位的影片，則輸出資料流程可能需要相同的位深度。</span><span class="sxs-lookup"><span data-stu-id="8e50c-121">For example, if the input type is 16-bit video, the output stream might require the same bit depth.</span></span> <span data-ttu-id="8e50c-122">用戶端可以列舉每個資料流程的慣用類型，然後測試特定的組合。</span><span class="sxs-lookup"><span data-stu-id="8e50c-122">The client can enumerate each stream's preferred types and then test specific combinations.</span></span>

<span data-ttu-id="8e50c-123">**緩衝區**</span><span class="sxs-lookup"><span data-stu-id="8e50c-123">**Buffers**</span></span>

<span data-ttu-id="8e50c-124">在預設的 SQL-DMO 模型中，用戶端會配置個別的輸入緩衝區和輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8e50c-124">In the default DMO model, the client allocates separate input buffers and output buffers.</span></span> <span data-ttu-id="8e50c-125">它會以資料填滿輸入緩衝區，並將其傳遞至，並將新的資料寫入至輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8e50c-125">It fills the input buffers with data and delivers them to the DMO, and the DMO writes new data into the output buffers.</span></span>

<span data-ttu-id="8e50c-126">您可以選擇性地支援「就地」處理。</span><span class="sxs-lookup"><span data-stu-id="8e50c-126">Optionally, a DMO can support "in-place" processing.</span></span> <span data-ttu-id="8e50c-127">使用就地處理時，會將輸出直接寫入至輸入緩衝區，而不是原始資料。</span><span class="sxs-lookup"><span data-stu-id="8e50c-127">With in-place processing, the DMO writes the output directly into the input buffer, over the original data.</span></span> <span data-ttu-id="8e50c-128">就地處理無須個別的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8e50c-128">In-place processing eliminates the need for separate buffers.</span></span> <span data-ttu-id="8e50c-129">相反地，它會改變原始資料，有些應用程式可能無法接受。</span><span class="sxs-lookup"><span data-stu-id="8e50c-129">On the other hand, it alters the original data, which may not be acceptable for some applications.</span></span>

<span data-ttu-id="8e50c-130">預設 (非就地) 緩衝模型是透過 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) 介面支援。</span><span class="sxs-lookup"><span data-stu-id="8e50c-130">The default (non-in-place) buffering model is supported through the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="8e50c-131">所有 DMOs 都必須執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="8e50c-131">All DMOs must implement this interface.</span></span> <span data-ttu-id="8e50c-132">如果 SQL-DMO 支援就地處理，它也會公開 [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) 介面。</span><span class="sxs-lookup"><span data-stu-id="8e50c-132">If a DMO supports in-place processing, it also exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="8e50c-133">用戶端負責配置所有緩衝區，包括輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="8e50c-133">The client is responsible for allocating all buffers, both input and output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e50c-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e50c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e50c-135">關於 DMOs</span><span class="sxs-lookup"><span data-stu-id="8e50c-135">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



