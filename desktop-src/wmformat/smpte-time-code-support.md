---
title: SMPTE 時間代碼支援
description: SMPTE 時間代碼支援
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Media Format SDK、SMPTE 時間碼
- Advanced Systems Format (ASF) 、SMPTE 時間碼
- ASF (Advanced Systems Format) ，SMPTE 時間碼
- Windows Media Format SDK，IWMReaderTimecode 介面
- Advanced Systems Format (ASF) ，IWMReaderTimecode 介面
- ASF (Advanced Systems Format) ，IWMReaderTimecode 介面
- SMPTE 時間代碼，關於
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507796"
---
# <a name="smpte-time-code-support"></a><span data-ttu-id="f78c6-111">SMPTE 時間代碼支援</span><span class="sxs-lookup"><span data-stu-id="f78c6-111">SMPTE Time Code Support</span></span>

<span data-ttu-id="f78c6-112">Windows Media Format SDK 提供有限的 SMPTE 時間代碼支援，這是適用于電影和電視的標準時間代碼格式。</span><span class="sxs-lookup"><span data-stu-id="f78c6-112">The Windows Media Format SDK provides limited support for SMPTE time code, which is a standard time code format for movies and television.</span></span> <span data-ttu-id="f78c6-113">您可以使用範例作為資料單位延伸模組來包含 SMPTE 時間代碼資料。</span><span class="sxs-lookup"><span data-stu-id="f78c6-113">You can include SMPTE time code data with samples as data unit extensions.</span></span> <span data-ttu-id="f78c6-114">延伸模組的資料部分是 WMT 時間 [**\_ 碼 \_ 延伸模組 \_ 資料**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) 結構，其中包含來自原始 SMPTE 時間戳記的資訊。</span><span class="sxs-lookup"><span data-stu-id="f78c6-114">The data portion of the extension is a [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structure containing the information from the original SMPTE time stamp.</span></span>

<span data-ttu-id="f78c6-115">在您的 ASF 檔案中維護 SMPTE 時間代碼會有效能限制。</span><span class="sxs-lookup"><span data-stu-id="f78c6-115">Maintaining SMPTE time code in your ASF files comes with performance limits.</span></span> <span data-ttu-id="f78c6-116">具有相關聯之 SMPTE 時間戳記的每個範例，都需要在時間戳記結構中傳輸14個位元組。</span><span class="sxs-lookup"><span data-stu-id="f78c6-116">Each sample with an associated SMPTE time stamp requires transport of the 14 bytes in the time stamp structure.</span></span> <span data-ttu-id="f78c6-117">在串流處理案例中，這種增加的頻寬需求可能會很嚴重。</span><span class="sxs-lookup"><span data-stu-id="f78c6-117">In a streaming scenario, this increased bandwidth requirement could be catastrophic.</span></span> <span data-ttu-id="f78c6-118">因此，建議在影片編輯程式期間，僅將 SMPTE 時間代碼保存在 ASF 檔案中，這通常是使用本機檔案來完成。</span><span class="sxs-lookup"><span data-stu-id="f78c6-118">As a result, it is suggested that SMPTE time codes only be persisted in ASF files during the video editing process, which is typically done with local files.</span></span> <span data-ttu-id="f78c6-119">建立最後的檔案時，您應該移除資料單位延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f78c6-119">When the final file is created, you should remove the data unit extensions.</span></span>

<span data-ttu-id="f78c6-120">您可以讀取「SMPTE 時間戳記」，就像讀取任何其他資料單位延伸一樣，但是讀取物件會提供以 SMPTE 時間碼搜尋的整合支援。</span><span class="sxs-lookup"><span data-stu-id="f78c6-120">You can read SMPTE time stamps just as you would read any other data unit extension, but the reading objects provide integrated support for searching by SMPTE time code.</span></span> <span data-ttu-id="f78c6-121">若要能夠搜尋 SMPTE 時間戳記，您必須先以 SMPTE 時間代碼為檔案編制索引。</span><span class="sxs-lookup"><span data-stu-id="f78c6-121">To be able to search for SMPTE time stamps, you must first index the file by SMPTE time code.</span></span> <span data-ttu-id="f78c6-122">您可以使用 [**IWMIndexer2：： configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) 方法，將索引子設定為編制時間碼的索引。</span><span class="sxs-lookup"><span data-stu-id="f78c6-122">You can configure the indexer to index time codes by using the [**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) method.</span></span>

<span data-ttu-id="f78c6-123">使用非同步讀取器時，您可以使用 [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) 介面的方法和 [**IWMReaderAdvanced3：： StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) 方法，依 SMPTE 時間戳記流覽檔案。</span><span class="sxs-lookup"><span data-stu-id="f78c6-123">Using the asynchronous reader, you can navigate a file by SMPTE time stamps using the methods of the [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) interface and the [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) method.</span></span> <span data-ttu-id="f78c6-124">使用同步讀取器時，請使用 [**IWMSyncReader2：： SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode)。</span><span class="sxs-lookup"><span data-stu-id="f78c6-124">With the synchronous reader, use [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f78c6-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f78c6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f78c6-126">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="f78c6-126">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="f78c6-127">**設定資料單位延伸模組**</span><span class="sxs-lookup"><span data-stu-id="f78c6-127">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




