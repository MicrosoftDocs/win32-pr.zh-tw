---
title: 使用索引
description: 使用索引
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media Format SDK，索引
- Advanced Systems Format (ASF) 、索引
- ASF (Advanced Systems Format) ，索引
- 索引，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839648"
---
# <a name="working-with-indexes"></a><span data-ttu-id="2fc37-107">使用索引</span><span class="sxs-lookup"><span data-stu-id="2fc37-107">Working with Indexes</span></span>

<span data-ttu-id="2fc37-108">Windows Media Format SDK 支援透過內容搜尋和是昂首闊步。</span><span class="sxs-lookup"><span data-stu-id="2fc37-108">The Windows Media Format SDK supports seeking and striding through content.</span></span> <span data-ttu-id="2fc37-109">搜尋可讓您指定檔案時間軸上的位置以開始播放。</span><span class="sxs-lookup"><span data-stu-id="2fc37-109">Seeking enables you to specify a place on the file's timeline to begin playback.</span></span> <span data-ttu-id="2fc37-110">是昂首闊步可讓您向前快轉和倒轉檔案的輸出。</span><span class="sxs-lookup"><span data-stu-id="2fc37-110">Striding enables you to fast-forward and rewind the output of a file.</span></span> <span data-ttu-id="2fc37-111">您必須編制檔案的索引，才能利用這些功能。</span><span class="sxs-lookup"><span data-stu-id="2fc37-111">Files must be indexed to take advantage of these features.</span></span> <span data-ttu-id="2fc37-112">索引是一系列的值，代表檔案中的位置 (呈現時間、框架數或 SMTPE 時間碼) ，其中每個都有相對應的位移至檔案的資料區段。</span><span class="sxs-lookup"><span data-stu-id="2fc37-112">An index is a series of values representing positions in the file (either presentation times, frame numbers, or SMTPE time codes) with corresponding offsets into the data section of the file for each.</span></span> <span data-ttu-id="2fc37-113">對於影片串流來說最重要的是，因為可以輕鬆地估計音訊串流呈現時間。</span><span class="sxs-lookup"><span data-stu-id="2fc37-113">Indexing is most important for video streams, as audio stream presentation time can be easily estimated.</span></span> <span data-ttu-id="2fc37-114">不過，某些音訊串流也可能需要索引。</span><span class="sxs-lookup"><span data-stu-id="2fc37-114">However, some audio streams may require indexes as well.</span></span> <span data-ttu-id="2fc37-115">根據預設，寫入器會為每個新的 ASF 檔案編制索引。</span><span class="sxs-lookup"><span data-stu-id="2fc37-115">By default, the writer will index every new ASF file.</span></span> <span data-ttu-id="2fc37-116">如果對檔案內容進行變更，您必須使用索引子物件自行重新整理索引。</span><span class="sxs-lookup"><span data-stu-id="2fc37-116">If changes are made to the content of a file, you must refresh the index yourself using the indexer object.</span></span>

<span data-ttu-id="2fc37-117">索引子支援時態和以框架為基礎的索引編制，以及根據 SMPTE 時間代碼編制索引 (如果存在) 。</span><span class="sxs-lookup"><span data-stu-id="2fc37-117">The indexer supports both temporal and frame-based indexing as well as indexing based on SMPTE time codes (if present).</span></span> <span data-ttu-id="2fc37-118">寫入器預設會針對編碼為檔案的每個新影片資料流程建立時態索引。</span><span class="sxs-lookup"><span data-stu-id="2fc37-118">The writer will create a temporal index by default for every new video stream encoded to a file.</span></span> <span data-ttu-id="2fc37-119">您必須明確地設定和呼叫索引子，以建立以框架為基礎或 SMPTE 時間的程式碼索引。</span><span class="sxs-lookup"><span data-stu-id="2fc37-119">You must explicitly configure and call the indexer to create a frame-based or SMPTE time code index.</span></span>

<span data-ttu-id="2fc37-120">對 ASF 檔案的內容進行變更時，必須重新編制其索引。</span><span class="sxs-lookup"><span data-stu-id="2fc37-120">When changes are made to the content of an ASF file, it must be indexed again.</span></span>

<span data-ttu-id="2fc37-121">下列各節提供執行一般編制索引工作的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="2fc37-121">The following sections present example code for performing common indexing tasks.</span></span>

-   [<span data-ttu-id="2fc37-122">停用自動編制索引</span><span class="sxs-lookup"><span data-stu-id="2fc37-122">To Disable Automatic Indexing</span></span>](to-disable-automatic-indexing.md)
-   [<span data-ttu-id="2fc37-123">設定索引子</span><span class="sxs-lookup"><span data-stu-id="2fc37-123">To Configure the Indexer</span></span>](to-configure-the-indexer.md)
-   [<span data-ttu-id="2fc37-124">為 ASF 檔案編制索引</span><span class="sxs-lookup"><span data-stu-id="2fc37-124">To Index an ASF File</span></span>](to-index-an-asf-file.md)
-   [<span data-ttu-id="2fc37-125">若要停止進行編制索引</span><span class="sxs-lookup"><span data-stu-id="2fc37-125">To Stop Indexing in Progress</span></span>](to-stop-indexing-in-progress.md)

<span data-ttu-id="2fc37-126">此外，DSCopy 範例應用程式會示範如何使用索引子。</span><span class="sxs-lookup"><span data-stu-id="2fc37-126">In addition, the DSCopy sample application illustrates the use of the indexer.</span></span> <span data-ttu-id="2fc37-127">如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="2fc37-127">For more information, see [Sample Applications](sample-applications.md).</span></span>

 

 




