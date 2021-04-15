---
description: 本主題說明如何在 Microsoft 媒體基礎中使用 ASF 設定檔。
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: ASF 設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510826"
---
# <a name="asf-profile"></a><span data-ttu-id="3124d-103">ASF 設定檔</span><span class="sxs-lookup"><span data-stu-id="3124d-103">ASF Profile</span></span>

<span data-ttu-id="3124d-104">本主題說明如何在 Microsoft 媒體基礎中使用 ASF 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3124d-104">This topic describes how to work with ASF profiles in Microsoft Media Foundation.</span></span>

<span data-ttu-id="3124d-105">Advanced Systems Format (ASF) 檔案包含一或多個資料流程。</span><span class="sxs-lookup"><span data-stu-id="3124d-105">An Advanced Systems Format (ASF) file contains one or more streams.</span></span> <span data-ttu-id="3124d-106">針對每個資料流程，ASF 標頭包含描述資料流程的資料流程屬性標頭。</span><span class="sxs-lookup"><span data-stu-id="3124d-106">For each stream, the ASF header contains a Stream Properties Header that describes the stream.</span></span> <span data-ttu-id="3124d-107">在 [WMContainer](wmcontainer-asf-components.md) 層，下列物件會用來設定或讀取 ASF 資料流程的屬性：</span><span class="sxs-lookup"><span data-stu-id="3124d-107">At the [WMContainer](wmcontainer-asf-components.md) layer, the following objects are used to set or read the properties of the ASF streams:</span></span>

-   <span data-ttu-id="3124d-108">*ASF 設定檔* 物件：描述資料流程及其與彼此之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="3124d-108">*ASF profile* object: Describes the streams and their relationships with each other.</span></span> <span data-ttu-id="3124d-109">ASF 設定檔物件會公開 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面。</span><span class="sxs-lookup"><span data-stu-id="3124d-109">The ASF profile object exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>
-   <span data-ttu-id="3124d-110">*串流* 設定物件：描述一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="3124d-110">*Stream configuration* object: Describes one stream.</span></span> <span data-ttu-id="3124d-111">資料流程設定物件包含描述資料流程格式的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3124d-111">The stream configuration object contains a media type that describes the format of the stream.</span></span> <span data-ttu-id="3124d-112">針對音訊和影片串流，媒體類型會確切描述資料流程的設定方式，並由編解碼器編碼或解碼資料流程使用。</span><span class="sxs-lookup"><span data-stu-id="3124d-112">For audio and video streams, the media type describes exactly how the stream is configured, and is used by codecs that encode or decode the stream.</span></span> <span data-ttu-id="3124d-113">Stream configuration 物件會公開 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面。</span><span class="sxs-lookup"><span data-stu-id="3124d-113">The stream configuration object exposes the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="3124d-114">有效的 ASF 設定檔至少包含一個資料流程設定物件。</span><span class="sxs-lookup"><span data-stu-id="3124d-114">A valid ASF profile contains at least one stream configuration object.</span></span>
-   <span data-ttu-id="3124d-115">*相互排除* 物件：描述不會同時讀取的多個資料流程。</span><span class="sxs-lookup"><span data-stu-id="3124d-115">*Mutual exclusion* object: Describes multiple streams that are not intended be read concurrently.</span></span> <span data-ttu-id="3124d-116">相互排除物件會公開 [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) 介面。</span><span class="sxs-lookup"><span data-stu-id="3124d-116">A mutual exclusion object exposes the [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) interface.</span></span> <span data-ttu-id="3124d-117">ASF 設定檔包含零或多個相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="3124d-117">An ASF profile contains zero or more mutual exclusion objects.</span></span>

<span data-ttu-id="3124d-118">下圖顯示 ASF 設定檔與設定檔中所包含之物件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="3124d-118">The following diagram shows the relationship between the ASF profile and the objects that are contained in the profile.</span></span>

![具有串流設定子節點之 asf 設定檔節點的樹狀結構圖;第一個指向媒體類型，接下來的兩個對相互排除](images/asf-components02.png)

<span data-ttu-id="3124d-120">為了播放，會使用 ASF 設定檔來列舉資料流程並尋找資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="3124d-120">For playback, the ASF profile is used to enumerate the streams and find the stream formats.</span></span> <span data-ttu-id="3124d-121">若為編碼，則會使用 ASF 設定檔來設定目的地檔案中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="3124d-121">For encoding, the ASF profile is used to configure the streams in the destination file.</span></span>

<span data-ttu-id="3124d-122">ASF 設定檔也用來設定 [Asf 媒體接收器](asf-media-sinks.md)。</span><span class="sxs-lookup"><span data-stu-id="3124d-122">The ASF profile is also used to configure the [ASF Media Sink](asf-media-sinks.md).</span></span> <span data-ttu-id="3124d-123">針對 ASF 設定檔中的每個資料流程，ASF 媒體接收器會建立對應的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="3124d-123">For each stream in the ASF profile, the ASF media sink creates a corresponding stream sink.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3124d-124">本節內容</span><span class="sxs-lookup"><span data-stu-id="3124d-124">In this section</span></span>



| <span data-ttu-id="3124d-125">主題</span><span class="sxs-lookup"><span data-stu-id="3124d-125">Topic</span></span>                                                                                           | <span data-ttu-id="3124d-126">描述</span><span class="sxs-lookup"><span data-stu-id="3124d-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="3124d-127">建立 ASF 設定檔</span><span class="sxs-lookup"><span data-stu-id="3124d-127">Creating an ASF Profile</span></span>](creating-an-asf-profile.md)<br/>                               | <span data-ttu-id="3124d-128">說明如何建立 ASF 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="3124d-128">Describes how to create an ASF profile object.</span></span><br/>          |
| [<span data-ttu-id="3124d-129">建立和設定 ASF 資料流程</span><span class="sxs-lookup"><span data-stu-id="3124d-129">Creating and Configuring ASF Streams</span></span>](creating-and-configuring-asf-streams.md)<br/>     | <span data-ttu-id="3124d-130">說明如何將資料流程新增至 ASF 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3124d-130">Describes how to add streams to an ASF profile.</span></span><br/>         |
| [<span data-ttu-id="3124d-131">針對 ASF 資料流程使用相互排除</span><span class="sxs-lookup"><span data-stu-id="3124d-131">Using Mutual Exclusion for ASF Streams</span></span>](using-mutual-exclusion-for-asf-streams.md)<br/> | <span data-ttu-id="3124d-132">說明如何將相互排除專案新增至 ASF 資料流程。</span><span class="sxs-lookup"><span data-stu-id="3124d-132">Describes how to add mutual exclusions to ASF streams.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3124d-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="3124d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3124d-134">媒體類型</span><span class="sxs-lookup"><span data-stu-id="3124d-134">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="3124d-135">教學課程： 1-傳遞 Windows Media 編碼</span><span class="sxs-lookup"><span data-stu-id="3124d-135">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="3124d-136">教學課程：使用 CBR 編碼方式撰寫 WMA 檔案</span><span class="sxs-lookup"><span data-stu-id="3124d-136">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[<span data-ttu-id="3124d-137">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="3124d-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 




