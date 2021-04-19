---
description: ASF 索引子
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: ASF 索引子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972156"
---
# <a name="asf-indexer"></a><span data-ttu-id="5a0e6-103">ASF 索引子</span><span class="sxs-lookup"><span data-stu-id="5a0e6-103">ASF Indexer</span></span>

<span data-ttu-id="5a0e6-104">ASF *索引子* 是 WMContainer 層元件，可用來以 Advanced 系統格式讀取或寫入索引物件 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="5a0e6-105">如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-105">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="5a0e6-106">應用程式可以使用索引子，根據展示時間來執行搜尋，或為 ASF 檔案產生新的索引項目。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-106">An application can use the indexer to perform seeking based on presentation time or to generate new index entries for an ASF file.</span></span> <span data-ttu-id="5a0e6-107">ASF 索引子會實 [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) 介面。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-107">The ASF indexer implements the [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) interface.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a0e6-108">索引類型</span><span class="sxs-lookup"><span data-stu-id="5a0e6-108">Index type</span></span></th>
<th><span data-ttu-id="5a0e6-109">Description</span><span class="sxs-lookup"><span data-stu-id="5a0e6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a0e6-110">以時間為基礎的簡報索引</span><span class="sxs-lookup"><span data-stu-id="5a0e6-110">Presentation time-based Index</span></span></td>
<td><span data-ttu-id="5a0e6-111">針對索引區塊中的音訊和影片資料流程提供以時間為基礎的簡報索引編制，讓索引更具空間效率。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-111">Provides presentation time-based indexing for audio and video streams in index blocks to make indexing more space efficient.</span></span> <span data-ttu-id="5a0e6-112">每個索引區塊都會參考包含位元組位移的索引項目。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-112">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="5a0e6-113">相較于 ASF 資料物件的開頭，位移是要 seeked 之資料封包的位置。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-113">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/> <span data-ttu-id="5a0e6-114">GUID_Null 必須當做索引識別碼的 GUID 類型使用。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-114">GUID_NULL must be used as the GUID type for the index identifier.</span></span> <span data-ttu-id="5a0e6-115">如需詳細資訊，請參閱 <a href="using-the-indexer-to-write-a-new-index.md">使用索引子來寫入新的索引</a>。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-115">For more information; see <a href="using-the-indexer-to-write-a-new-index.md">Using the Indexer to Write a New Index</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a0e6-116">時間碼索引</span><span class="sxs-lookup"><span data-stu-id="5a0e6-116">Timecode Index</span></span></td>
<td><span data-ttu-id="5a0e6-117">協助在包含時間碼中繼資料的資料流程中依時間碼進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-117">Facilitates seeking by timecode in streams which contain timecode metadata.</span></span> <span data-ttu-id="5a0e6-118">時間碼符合 SMPTE 格式 (<em>小時：分鐘：秒：畫面</em> 格) 。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-118">The timecodes conform to a SMPTE format (<em>Hours:Minutes:Seconds:Frames</em>).</span></span> <span data-ttu-id="5a0e6-119">每個索引區塊都會參考包含位元組位移的索引項目。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-119">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="5a0e6-120">相較于 ASF 資料物件的開頭，位移是要 seeked 之資料封包的位置。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-120">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5a0e6-121">目前不支援時間碼索引物件。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-121">Timecode index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a0e6-122">以框架為基礎的索引</span><span class="sxs-lookup"><span data-stu-id="5a0e6-122">Frame-based Index</span></span></td>
<td><span data-ttu-id="5a0e6-123">提供影片資料流程的框架型索引。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-123">Provides frame-based indexing for video streams.</span></span> <span data-ttu-id="5a0e6-124">以畫面格為基礎之索引的索引是以畫面格數目為基礎，而 ASF 檔案中資料流程的第一個框架對應到以框架為基礎的索引物件中的專案0。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-124">Indexes into the frame-based index are in terms of frame numbers, with the first frame for a stream in the ASF file corresponding to entry 0 in the frame-based index object.</span></span> <span data-ttu-id="5a0e6-125">每個索引區塊都會參考包含位元組位移的索引項目。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-125">Each index block references index entries that contain a byte offset.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5a0e6-126">目前不支援以框架為基礎的索引物件。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-126">Frame-based index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5a0e6-127">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-127">This section contains the following topics.</span></span>



| <span data-ttu-id="5a0e6-128">主題</span><span class="sxs-lookup"><span data-stu-id="5a0e6-128">Topic</span></span>                                                                                | <span data-ttu-id="5a0e6-129">描述</span><span class="sxs-lookup"><span data-stu-id="5a0e6-129">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a0e6-130">建立和設定索引子</span><span class="sxs-lookup"><span data-stu-id="5a0e6-130">Indexer Creation and Configuration</span></span>](indexer-creation-and-configuration.md)         | <span data-ttu-id="5a0e6-131">如何建立索引子物件，並將它設定為讀取現有的索引，或為檔案撰寫新的 ASF 索引物件。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-131">How to create an indexer object and configure it for reading an existing index or for writing a new ASF Index Object for a file.</span></span> |
| [<span data-ttu-id="5a0e6-132">使用索引子在檔案中搜尋</span><span class="sxs-lookup"><span data-stu-id="5a0e6-132">Using the Indexer to Seek in a File</span></span>](using-the-indexer-to-seek.md)                 | <span data-ttu-id="5a0e6-133">如何使用索引子在 ASF 檔案內搜尋。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-133">How to use the indexer to seek within an ASF file.</span></span>                                                                               |
| [<span data-ttu-id="5a0e6-134">使用索引子來寫入新的索引</span><span class="sxs-lookup"><span data-stu-id="5a0e6-134">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md) | <span data-ttu-id="5a0e6-135">如何使用索引子來產生索引項目，以及為 ASF 檔案撰寫新的索引物件。</span><span class="sxs-lookup"><span data-stu-id="5a0e6-135">How to use the indexer to generate index entries and write a new Index Object for an ASF file.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="5a0e6-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a0e6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a0e6-137">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="5a0e6-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="5a0e6-138">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="5a0e6-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




