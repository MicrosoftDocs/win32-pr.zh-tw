---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: 使用接收寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943863"
---
# <a name="using-the-sink-writer"></a><span data-ttu-id="892ce-103">使用接收寫入器</span><span class="sxs-lookup"><span data-stu-id="892ce-103">Using the Sink Writer</span></span>

## <a name="overview"></a><span data-ttu-id="892ce-104">概觀</span><span class="sxs-lookup"><span data-stu-id="892ce-104">Overview</span></span>

### <a name="file-container-types"></a><span data-ttu-id="892ce-105">檔案容器類型</span><span class="sxs-lookup"><span data-stu-id="892ce-105">File Container Types</span></span>

<span data-ttu-id="892ce-106">接收寫入器有數個檔案容器類型的內建支援。</span><span class="sxs-lookup"><span data-stu-id="892ce-106">The sink writer has built-in support for several file container types.</span></span> <span data-ttu-id="892ce-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span><span class="sxs-lookup"><span data-stu-id="892ce-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span></span> <span data-ttu-id="892ce-108">您可以藉由撰寫自訂 [媒體接收器](media-sinks.md)來支援其他容器類型。</span><span class="sxs-lookup"><span data-stu-id="892ce-108">You can support additional container types by writing a custom [media sink](media-sinks.md).</span></span> <span data-ttu-id="892ce-109">當您建立接收寫入器的新實例時，會指定檔案容器。</span><span class="sxs-lookup"><span data-stu-id="892ce-109">The file container is specified when you create a new instance of the sink writer.</span></span>

### <a name="stream-formats"></a><span data-ttu-id="892ce-110">資料流程格式</span><span class="sxs-lookup"><span data-stu-id="892ce-110">Stream Formats</span></span>

<span data-ttu-id="892ce-111">針對每個資料流程，應用程式必須指定下列各項。</span><span class="sxs-lookup"><span data-stu-id="892ce-111">For each stream, the application must specify the following.</span></span>

-   <span data-ttu-id="892ce-112">*輸入格式* 是應用程式傳送給接收寫入器的格式。</span><span class="sxs-lookup"><span data-stu-id="892ce-112">The *input format* is the format that the application sends to the sink writer.</span></span>
-   <span data-ttu-id="892ce-113">*輸出格式* 是將寫入檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="892ce-113">The *output format* is the format that will be written to the file.</span></span>

<span data-ttu-id="892ce-114">輸入和輸出格式可以是已壓縮或未壓縮。</span><span class="sxs-lookup"><span data-stu-id="892ce-114">The input and output formats can be either compressed or uncompressed.</span></span> <span data-ttu-id="892ce-115">接收寫入器支援下列組合：</span><span class="sxs-lookup"><span data-stu-id="892ce-115">The sink writer supports the following combinations:</span></span>

-   <span data-ttu-id="892ce-116">壓縮輸出的未壓縮輸入。</span><span class="sxs-lookup"><span data-stu-id="892ce-116">Uncompressed input with compressed output.</span></span> <span data-ttu-id="892ce-117">這是一般案例，用於編碼或轉碼案例。</span><span class="sxs-lookup"><span data-stu-id="892ce-117">This is the typical case, and is used for encoding or transcoding scenarios.</span></span> <span data-ttu-id="892ce-118">Microsoft 媒體基礎編碼器必須可接受輸入類型，並對輸出類型進行編碼。</span><span class="sxs-lookup"><span data-stu-id="892ce-118">A Microsoft Media Foundation encoder must be available that accepts the input type and encodes to the output type.</span></span>
-   <span data-ttu-id="892ce-119">具有相同輸出的壓縮輸入。</span><span class="sxs-lookup"><span data-stu-id="892ce-119">Compressed input with identical output.</span></span> <span data-ttu-id="892ce-120">您可以使用此組合來 remux 沒有轉碼的檔案。</span><span class="sxs-lookup"><span data-stu-id="892ce-120">Use this combination to remux a file without transcoding.</span></span>
-   <span data-ttu-id="892ce-121">具有相同輸出的未壓縮輸入。</span><span class="sxs-lookup"><span data-stu-id="892ce-121">Uncompressed input with identical output.</span></span> <span data-ttu-id="892ce-122">使用這個組合將未壓縮的音訊或影片寫入檔案容器中。</span><span class="sxs-lookup"><span data-stu-id="892ce-122">Use this combination to write uncompressed audio or video to a file container.</span></span>

<span data-ttu-id="892ce-123">除非編碼器提供這些函式，否則接收寫入器不支援影片調整大小、畫面播放速率轉換或音訊重新取樣。</span><span class="sxs-lookup"><span data-stu-id="892ce-123">The sink writer does not support video resizing, frame-rate conversion, or audio resampling, unless these functions are provided by the encoder.</span></span> <span data-ttu-id="892ce-124">否則，應用程式可以使用 [數位訊號處理器](windowsmediadigitalsignalprocessors.md) 來轉換輸入資料，然後再將資料傳送到</span><span class="sxs-lookup"><span data-stu-id="892ce-124">Otherwise, the application can use [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) to convert the input data, before sending the data to the</span></span>

## <a name="creating-the-sink-writer"></a><span data-ttu-id="892ce-125">建立接收寫入器</span><span class="sxs-lookup"><span data-stu-id="892ce-125">Creating the Sink Writer</span></span>

<span data-ttu-id="892ce-126">有兩個函數可建立接收寫入器：</span><span class="sxs-lookup"><span data-stu-id="892ce-126">There are two functions that create the sink writer:</span></span>

-   <span data-ttu-id="892ce-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) 會採用輸出檔案的 URL 或位元組資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="892ce-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) takes the URL of an output file or a pointer to a byte stream.</span></span> <span data-ttu-id="892ce-128">此函數會在內部建立媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="892ce-128">This function creates the media sink internally.</span></span>
-   <span data-ttu-id="892ce-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) 會取得應用程式已建立之媒體接收器的指標。</span><span class="sxs-lookup"><span data-stu-id="892ce-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) takes a pointer to a media sink that has already been created by the application.</span></span>

<span data-ttu-id="892ce-130">如果您使用其中一個內建的媒體接收器， [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) 函式是較理想的作法，因為呼叫端不需要設定媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="892ce-130">If you are using one of the built-in media sinks, the [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) function is preferable, because the caller does not need to configure the media sink.</span></span>

<span data-ttu-id="892ce-131">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)方法提供數個選項來指定檔案容器的類型。</span><span class="sxs-lookup"><span data-stu-id="892ce-131">The [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) method provides several options for specifying the type of file container.</span></span> <span data-ttu-id="892ce-132">在最簡單的情況下，函數會使用 URL 中的副檔名來選取檔案容器。</span><span class="sxs-lookup"><span data-stu-id="892ce-132">In the simplest case, the function uses the file name extension in the URL to select the file container.</span></span> <span data-ttu-id="892ce-133">如需詳細資料，請參閱函數參考頁面。</span><span class="sxs-lookup"><span data-stu-id="892ce-133">For details, refer to the function reference page.</span></span>

<span data-ttu-id="892ce-134">例如，下列程式碼會為 URL 指定檔案名 "output"。</span><span class="sxs-lookup"><span data-stu-id="892ce-134">For example, the following code specifies the file name "output.wmv" for the URL.</span></span> <span data-ttu-id="892ce-135">接收寫入器會根據副檔名載入 [Asf 媒體接收器](asf-media-sinks.md) ，以建立 Advanced 系統格式 (asf) 檔。</span><span class="sxs-lookup"><span data-stu-id="892ce-135">Based on the file name extension, the sink writer will load the [ASF Media Sink](asf-media-sinks.md) to create an Advanced Systems Format (ASF) file.</span></span>


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



<span data-ttu-id="892ce-136">在 [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)的案例中，檔案類型是由媒體接收所決定。</span><span class="sxs-lookup"><span data-stu-id="892ce-136">In the case of [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), the file type is determined by the media sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="892ce-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="892ce-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="892ce-138">接收寫入器</span><span class="sxs-lookup"><span data-stu-id="892ce-138">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 



