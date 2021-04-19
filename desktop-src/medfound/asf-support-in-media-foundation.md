---
description: 媒體基礎中的 ASF 支援
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: 媒體基礎中的 ASF 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986439"
---
# <a name="asf-support-in-media-foundation"></a><span data-ttu-id="00da6-103">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="00da6-103">ASF Support in Media Foundation</span></span>

<span data-ttu-id="00da6-104">媒體基礎支援 (ASF) 的 Advanced Systems 格式媒體檔案：</span><span class="sxs-lookup"><span data-stu-id="00da6-104">Media Foundation supports media files in the Advanced Systems Format (ASF):</span></span>

-   <span data-ttu-id="00da6-105">Windows Media 視訊 (WMV 檔案) </span><span class="sxs-lookup"><span data-stu-id="00da6-105">Windows Media Video (WMV files)</span></span>
-   <span data-ttu-id="00da6-106">Windows Media 音訊 (WMA 檔案) </span><span class="sxs-lookup"><span data-stu-id="00da6-106">Windows Media Audio (WMA files)</span></span>

<span data-ttu-id="00da6-107">媒體基礎提供數個物件來讀取和寫入 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="00da6-107">Media Foundation provides several objects for reading and writing ASF files.</span></span> <span data-ttu-id="00da6-108">這些物件是在兩個不同的架構層中提供。</span><span class="sxs-lookup"><span data-stu-id="00da6-108">These objects are provided in two different architectural layers.</span></span>

<span data-ttu-id="00da6-109">首先， *管線* 層包含可在 [媒體基礎管線](media-foundation-pipeline.md) 內運作，且符合管線所定義之 api 的物件。</span><span class="sxs-lookup"><span data-stu-id="00da6-109">First, the *pipeline* layer contains objects that work inside the [Media Foundation pipeline](media-foundation-pipeline.md) and conform to the APIs defined by the pipeline.</span></span> <span data-ttu-id="00da6-110">ASF 管線層包含：</span><span class="sxs-lookup"><span data-stu-id="00da6-110">The ASF pipeline layer contains:</span></span>

-   <span data-ttu-id="00da6-111">[Asf 媒體來源](asf-media-source.md)：剖析 asf 檔案並傳遞音訊/影片資料封包。</span><span class="sxs-lookup"><span data-stu-id="00da6-111">[ASF Media Source](asf-media-source.md): Parses ASF files and delivers the audio/video data packets.</span></span>
-   <span data-ttu-id="00da6-112">[Windows Media 編解碼器](windows-media-codecs.md)：對 Windows media 音訊或影片串流進行解碼或編碼。</span><span class="sxs-lookup"><span data-stu-id="00da6-112">[Windows Media Codecs](windows-media-codecs.md): Decode or encode Windows Media audio or video streams.</span></span>
-   <span data-ttu-id="00da6-113">[Asf 媒體接收器](asf-media-sinks.md)：接收資料封包並寫入 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="00da6-113">[ASF Media Sink](asf-media-sinks.md): Receives data packets and writes an ASF file.</span></span>

<span data-ttu-id="00da6-114">其次，WM 容器層提供對剖析和寫入 ASF 檔案的低層級控制。</span><span class="sxs-lookup"><span data-stu-id="00da6-114">Second, the WM Container layer provides low-level control over parsing and writing an ASF file.</span></span> <span data-ttu-id="00da6-115">管線層會在內部使用 WMContainer。</span><span class="sxs-lookup"><span data-stu-id="00da6-115">The pipeline layer uses WMContainer internally.</span></span> <span data-ttu-id="00da6-116">應用程式也可以使用 WMContainer 進行低層級的 ASF 剖析和寫入。</span><span class="sxs-lookup"><span data-stu-id="00da6-116">Applications can also use WMContainer for low-level ASF parsing and writing.</span></span>

![顯示管線層和 wm 容器元素的圖表](images/asf-components.png)

## <a name="in-this-section"></a><span data-ttu-id="00da6-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="00da6-118">In this section</span></span>



| <span data-ttu-id="00da6-119">主題</span><span class="sxs-lookup"><span data-stu-id="00da6-119">Topic</span></span>                                                                         | <span data-ttu-id="00da6-120">描述</span><span class="sxs-lookup"><span data-stu-id="00da6-120">Description</span></span>                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00da6-121">ASF 檔案結構</span><span class="sxs-lookup"><span data-stu-id="00da6-121">ASF File Structure</span></span>](asf-file-structure.md)<br/>                       | <span data-ttu-id="00da6-122">介紹 ASF 檔案結構以及媒體基礎所提供的物件，以使用 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="00da6-122">Overview of the ASF file structure and the objects provided by Media Foundation to work with ASF files.</span></span><br/> |
| [<span data-ttu-id="00da6-123">管線層 ASF 元件</span><span class="sxs-lookup"><span data-stu-id="00da6-123">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)<br/> | <span data-ttu-id="00da6-124">說明如何使用管線層來剖析及撰寫 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="00da6-124">Describes how to parse and author ASF files using the pipeline layer.</span></span><br/>                                   |
| [<span data-ttu-id="00da6-125">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="00da6-125">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)<br/>       | <span data-ttu-id="00da6-126">說明如何使用 WMContainer 層來剖析及撰寫 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="00da6-126">Describes how to parse and author ASF files using the WMContainer layer.</span></span><br/>                                |



 

<span data-ttu-id="00da6-127">如需 ASF 檔案結構的詳細資訊，請參閱您可以從這個 [Microsoft 網站](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)下載的 asf 規格。</span><span class="sxs-lookup"><span data-stu-id="00da6-127">For detailed information about the structure of an ASF file, see the ASF specification, which can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00da6-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="00da6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00da6-129">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="00da6-129">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




