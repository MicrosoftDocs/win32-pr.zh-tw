---
description: 媒體來源
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: 媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195724"
---
# <a name="media-sources"></a><span data-ttu-id="87ceb-103">媒體來源</span><span class="sxs-lookup"><span data-stu-id="87ceb-103">Media Sources</span></span>

<span data-ttu-id="87ceb-104">*媒體來源* 是在媒體基礎管線中產生媒體資料的物件。</span><span class="sxs-lookup"><span data-stu-id="87ceb-104">*Media sources* are objects that generate media data in the Media Foundation pipeline.</span></span> <span data-ttu-id="87ceb-105">本節將詳細說明媒體來源 Api。</span><span class="sxs-lookup"><span data-stu-id="87ceb-105">This section describes the media source APIs in detail.</span></span> <span data-ttu-id="87ceb-106">如果您要執行自訂媒體來源，或使用媒體基礎管線以外的媒體來源，請閱讀本節。</span><span class="sxs-lookup"><span data-stu-id="87ceb-106">Read this section if you are implementing a custom media source, or using a media source outside of the Media Foundation pipeline.</span></span>

<span data-ttu-id="87ceb-107">如果您的應用程式使用控制層，則只需要使用有限的媒體來源 Api 子集。</span><span class="sxs-lookup"><span data-stu-id="87ceb-107">If your application uses the control layer, it needs to use only a limited subset of the media source APIs.</span></span> <span data-ttu-id="87ceb-108">如需詳細資訊，請參閱 [使用媒體來源和媒體會話](using-media-sources-with-the-media-session.md)的主題。</span><span class="sxs-lookup"><span data-stu-id="87ceb-108">For information, see the topic [Using Media Sources with the Media Session](using-media-sources-with-the-media-session.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="87ceb-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="87ceb-109">In this section</span></span>



| <span data-ttu-id="87ceb-110">主題</span><span class="sxs-lookup"><span data-stu-id="87ceb-110">Topic</span></span>                                                                                                 | <span data-ttu-id="87ceb-111">描述</span><span class="sxs-lookup"><span data-stu-id="87ceb-111">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87ceb-112">媒體來源物件模型</span><span class="sxs-lookup"><span data-stu-id="87ceb-112">Media Source Object Model</span></span>](media-source-object-model.md)<br/>                                 | <span data-ttu-id="87ceb-113">本主題說明中媒體來源的物件模型 Microsoft 媒體基礎</span><span class="sxs-lookup"><span data-stu-id="87ceb-113">This topic describes the object model for media sources in Microsoft Media Foundation</span></span><br/>                     |
| [<span data-ttu-id="87ceb-114">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="87ceb-114">Presentation Descriptors</span></span>](presentation-descriptors.md)<br/>                                   | <span data-ttu-id="87ceb-115">*簡報描述* 項是一個物件，其中包含特定簡報的描述。</span><span class="sxs-lookup"><span data-stu-id="87ceb-115">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span><br/>      |
| [<span data-ttu-id="87ceb-116">媒體來源事件</span><span class="sxs-lookup"><span data-stu-id="87ceb-116">Media Source Events</span></span>](media-source-events.md)<br/>                                             | <span data-ttu-id="87ceb-117">本主題列出媒體來源和媒體資料流程所傳送的事件。</span><span class="sxs-lookup"><span data-stu-id="87ceb-117">This topic lists the events that are sent by media sources and media streams.</span></span><br/>                             |
| [<span data-ttu-id="87ceb-118">撰寫自訂媒體來源</span><span class="sxs-lookup"><span data-stu-id="87ceb-118">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)<br/>                         | <span data-ttu-id="87ceb-119">本主題說明如何在媒體基礎中執行自訂媒體來源。</span><span class="sxs-lookup"><span data-stu-id="87ceb-119">This topic describes how to implement a custom media source in Media Foundation.</span></span><br/>                          |
| [<span data-ttu-id="87ceb-120">案例研究： MPEG-2 媒體來源</span><span class="sxs-lookup"><span data-stu-id="87ceb-120">Case Study: MPEG-1 Media Source</span></span>](tutorial--writing-a-custom-media-source.md)<br/>             | <span data-ttu-id="87ceb-121">本主題深入探討 [Mpeg-2 媒體來源](mpeg1source-sample.md) SDK 範例。</span><span class="sxs-lookup"><span data-stu-id="87ceb-121">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span><br/>        |
| [<span data-ttu-id="87ceb-122">媒體檔案的自訂中繼資料提供者</span><span class="sxs-lookup"><span data-stu-id="87ceb-122">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)<br/> | <span data-ttu-id="87ceb-123">本主題說明如何撰寫媒體基礎媒體來源的自訂 Shell 屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="87ceb-123">This topic describes how to write a custom Shell property handler for a Media Foundation media source.</span></span><br/>    |
| [<span data-ttu-id="87ceb-124">來源解析程式</span><span class="sxs-lookup"><span data-stu-id="87ceb-124">Source Resolver</span></span>](source-resolver.md)<br/>                                                     | <span data-ttu-id="87ceb-125">來源解析程式會接受 URL 或位元組資料流，然後為該內容建立適當的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="87ceb-125">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="87ceb-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="87ceb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87ceb-127">媒體基礎管線</span><span class="sxs-lookup"><span data-stu-id="87ceb-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="87ceb-128">媒體檔案的自訂中繼資料提供者</span><span class="sxs-lookup"><span data-stu-id="87ceb-128">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[<span data-ttu-id="87ceb-129">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="87ceb-129">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




