---
description: ASF 媒體接收器是編碼管線中的最後一個元件，可讓應用程式寫入 ASF 檔。
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: ASF 媒體接收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106989121"
---
# <a name="asf-media-sinks"></a><span data-ttu-id="62295-103">ASF 媒體接收</span><span class="sxs-lookup"><span data-stu-id="62295-103">ASF Media Sinks</span></span>

<span data-ttu-id="62295-104">ASF 媒體接收器是編碼管線中的最後一個元件，可讓應用程式寫入 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="62295-104">The ASF media sink is the final component in the encoding pipeline that enables an application to write an ASF file.</span></span>

<span data-ttu-id="62295-105">媒體基礎提供兩種類型的 ASF 媒體接收器：</span><span class="sxs-lookup"><span data-stu-id="62295-105">Media Foundation provides two types of ASF media sinks:</span></span>

-   <span data-ttu-id="62295-106">*Asf 檔案接收* 可用來將 asf 媒體資料封存至檔案。</span><span class="sxs-lookup"><span data-stu-id="62295-106">*ASF file sink* is used to archive ASF media data to a file.</span></span>
-   <span data-ttu-id="62295-107">*Asf 串流接收器* 用來在可透過網路串流處理的位元組資料流程中寫入 asf 內容。</span><span class="sxs-lookup"><span data-stu-id="62295-107">*ASF streaming sink* is used to write ASF content in a byte stream that can be streamed across the network.</span></span>

<span data-ttu-id="62295-108">ASF 媒體接收器包含一或多個資料流程接收，其代表要針對輸出 ASF 檔案中的每個資料流程寫入的資料。</span><span class="sxs-lookup"><span data-stu-id="62295-108">ASF media sinks contain one or more stream sinks, which represents the data to write for each stream in the output ASF file.</span></span> <span data-ttu-id="62295-109">針對在 Windows Vista 上執行的應用程式進行編碼，您必須建立及設定 ASF 媒體接收器，然後將它新增至拓撲，以手動方式設定編碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="62295-109">For encoding applications that run on Windows Vista, you must manually configure the encoding topology by creating and configuring the ASF media sink and then adding it to the topology.</span></span> <span data-ttu-id="62295-110">在 Windows 7 中，如果您使用快速轉碼物件來建立拓撲，則不會直接建立媒體接收器，而且應用程式不會呼叫媒體接收或任何資料流程接收上的任何方法。</span><span class="sxs-lookup"><span data-stu-id="62295-110">In Windows 7, if you are using the fast transcode objects to create the topology, you do not have create the media sink directly and the application does not call any methods on the media sink or any of the stream sinks.</span></span> <span data-ttu-id="62295-111">Fast 轉碼物件可具現化所需的媒體接收，並將其新增至拓撲，然後再傳回呼叫端應用程式的參考。</span><span class="sxs-lookup"><span data-stu-id="62295-111">The fast transcode objects instantiate the required media sinks and add it to the topology before returning a reference to the caller application.</span></span> <span data-ttu-id="62295-112">不過，對於快速轉碼物件，有一些限制會根據編碼類型而套用。</span><span class="sxs-lookup"><span data-stu-id="62295-112">However for fast transcode objects, there are some restrictions that apply depending on the type of encoding.</span></span>

-   [<span data-ttu-id="62295-113">ASF 媒體接收物件模型</span><span class="sxs-lookup"><span data-stu-id="62295-113">ASF Media Sink Object Model</span></span>](#asf-media-sink-object-model)
-   [<span data-ttu-id="62295-114">ASF 檔接收器</span><span class="sxs-lookup"><span data-stu-id="62295-114">ASF File Sink</span></span>](#asf-file-sink)
-   [<span data-ttu-id="62295-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="62295-115">Related topics</span></span>](#related-topics)

## <a name="asf-media-sink-object-model"></a><span data-ttu-id="62295-116">ASF 媒體接收物件模型</span><span class="sxs-lookup"><span data-stu-id="62295-116">ASF Media Sink Object Model</span></span>

<span data-ttu-id="62295-117">ASF 媒體接收器會執行 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) 介面並公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="62295-117">ASF media sinks implement the [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface and exposes the following interfaces.</span></span> <span data-ttu-id="62295-118">應用程式可以在用來產生輸出範例的 ASF 媒體接收器上呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，以取得這些介面的參考。</span><span class="sxs-lookup"><span data-stu-id="62295-118">An application can get a reference to these interfaces by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the ASF media sink it is using for generating output samples.</span></span>



| <span data-ttu-id="62295-119">介面</span><span class="sxs-lookup"><span data-stu-id="62295-119">Interface</span></span>                                                  | <span data-ttu-id="62295-120">描述</span><span class="sxs-lookup"><span data-stu-id="62295-120">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62295-121">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="62295-121">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | <span data-ttu-id="62295-122">所有媒體接收都需要。</span><span class="sxs-lookup"><span data-stu-id="62295-122">Required for all media sinks.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="62295-123">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="62295-123">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | <span data-ttu-id="62295-124">由可將產生的媒體內容寫入檔案的 ASF 檔案接收所執行。</span><span class="sxs-lookup"><span data-stu-id="62295-124">Implemented by the ASF file sink that writes the generated media content to a file.</span></span> <span data-ttu-id="62295-125">您可以使用此介面上的方法來排清資料，並更新最終輸出檔案的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="62295-125">You can use the methods on this interface to flush data and update the ASF Header Object of the final output file.</span></span> |
| [<span data-ttu-id="62295-126">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="62295-126">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | <span data-ttu-id="62295-127">從呈現時鐘接收狀態變更通知。</span><span class="sxs-lookup"><span data-stu-id="62295-127">Receives state-change notifications from the presentation clock.</span></span>                                                                                                                                       |
| [<span data-ttu-id="62295-128">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="62295-128">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | <span data-ttu-id="62295-129">ASF ContentInfo 物件是 WMContainer 層級物件，主要儲存 ASF 標頭物件資訊。</span><span class="sxs-lookup"><span data-stu-id="62295-129">The ASF ContentInfo object is a WMContainer level object that mainly stores ASF Header Object information.</span></span> <span data-ttu-id="62295-130">這是用來建立 ASF 媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="62295-130">This is used to create ASF media sinks.</span></span>                                                     |
| [<span data-ttu-id="62295-131">**IMFMetadata**</span><span class="sxs-lookup"><span data-stu-id="62295-131">**IMFMetadata**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | <span data-ttu-id="62295-132">用來描述 ASF 檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="62295-132">Used to describe the metadata for the ASF file.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="62295-133">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="62295-133">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | <span data-ttu-id="62295-134">取得中繼資料的集合，不論是針對整個簡報，或是簡報中的一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="62295-134">Retrieves a collection of metadata, either for an entire presentation, or for one stream in the presentation.</span></span>                                                                                          |



 

## <a name="asf-file-sink"></a><span data-ttu-id="62295-135">ASF 檔接收器</span><span class="sxs-lookup"><span data-stu-id="62295-135">ASF File Sink</span></span>

<span data-ttu-id="62295-136">ASF 檔案接收是媒體基礎所提供的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ，可讓應用程式用來將 ASF 媒體資料封存至檔案。</span><span class="sxs-lookup"><span data-stu-id="62295-136">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span>

<span data-ttu-id="62295-137">如果您使用管線層物件來寫入新的 ASF 檔案，您需要在檔案接收或其任何資料流程接收上建立、設定和呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="62295-137">You need to create, configure, and call methods on the file sink or any of its stream sinks if you are using the pipeline layer objects to write a new ASF file.</span></span> <span data-ttu-id="62295-138">設定檔案接收器之後，您可以將它新增至編碼管線。</span><span class="sxs-lookup"><span data-stu-id="62295-138">After configuring the file sink you can then add it to the encoding pipeline.</span></span>

<span data-ttu-id="62295-139">以下是使用 ASF file 接收器的一般步驟：</span><span class="sxs-lookup"><span data-stu-id="62295-139">Here are the general steps for using the ASF file sink:</span></span>

1.  <span data-ttu-id="62295-140">建立同進程或跨進程的檔案接收。</span><span class="sxs-lookup"><span data-stu-id="62295-140">Create the file sink in-process or out-of-process.</span></span>
2.  <span data-ttu-id="62295-141">使用所有資料流程、編碼屬性和中繼資料資訊來設定 file sink。</span><span class="sxs-lookup"><span data-stu-id="62295-141">Configure the file sink with all the streams, encoding properties, and metadata information.</span></span>
3.  <span data-ttu-id="62295-142">藉由列舉資料流程接收或在接收中追蹤資料流程號碼，來將檔案接收與輸出拓撲節點建立關聯。</span><span class="sxs-lookup"><span data-stu-id="62295-142">Associate the file sink with the output topology node either by enumerating the stream sinks or by keeping track of the stream numbers with in the sink.</span></span>

<span data-ttu-id="62295-143">下列主題包含有關使用 ASF 檔案接收的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="62295-143">The following topics contain detailed information about working with the ASF file sink:</span></span>

-   [<span data-ttu-id="62295-144">建立 ASF 檔接收器</span><span class="sxs-lookup"><span data-stu-id="62295-144">Creating the ASF File Sink</span></span>](creating-the-asf-file-sink.md)
-   [<span data-ttu-id="62295-145">將資料流程資訊新增至 ASF 檔案接收</span><span class="sxs-lookup"><span data-stu-id="62295-145">Adding Stream Information to the ASF File Sink</span></span>](adding-stream-information-to-the-asf-file-sink.md)
-   [<span data-ttu-id="62295-146">設定 File 接收中的屬性</span><span class="sxs-lookup"><span data-stu-id="62295-146">Setting Properties in the File Sink</span></span>](setting-properties-in-the-file-sink.md)
-   [<span data-ttu-id="62295-147">將中繼資料新增至 File 接收器</span><span class="sxs-lookup"><span data-stu-id="62295-147">Adding Metadata to the File Sink</span></span>](adding-metadata-to-the-file-sink.md)
-   [<span data-ttu-id="62295-148">有漏洞 Bucket 緩衝區模型</span><span class="sxs-lookup"><span data-stu-id="62295-148">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a><span data-ttu-id="62295-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="62295-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62295-150">管線層 ASF 元件</span><span class="sxs-lookup"><span data-stu-id="62295-150">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="62295-151">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="62295-151">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
