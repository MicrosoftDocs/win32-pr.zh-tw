---
title: 使用同步讀取器取出壓縮的範例
description: 使用同步讀取器取出壓縮的範例
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Advanced Systems Format (ASF) ，正在抓取壓縮的範例
- ASF (Advanced 系統格式) ，正在抓取壓縮的範例
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- Advanced Systems Format (ASF) 、壓縮的範例
- ASF (Advanced Systems Format) ，壓縮的範例
- 同步讀取器，正在抓取壓縮的範例
- 同步讀取器，壓縮的範例
- 壓縮的範例，正在抓取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092540"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a><span data-ttu-id="1c94c-112">使用同步讀取器取出壓縮的範例</span><span class="sxs-lookup"><span data-stu-id="1c94c-112">To Retrieve Compressed Samples with the Synchronous Reader</span></span>

<span data-ttu-id="1c94c-113">如同非同步讀取器，同步讀取器也可以取出壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="1c94c-113">Like the asynchronous reader, the synchronous reader can also retrieve compressed samples.</span></span> <span data-ttu-id="1c94c-114">將資料流程從某個檔案複製到另一個檔案時，應使用壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="1c94c-114">Compressed samples should be used when copying streams from one file to another.</span></span>

<span data-ttu-id="1c94c-115">Windows Media Format SDK 不提供任何方法，可在資料從 ASF 檔案解壓縮之後進行解碼。</span><span class="sxs-lookup"><span data-stu-id="1c94c-115">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="1c94c-116">如果您收到壓縮的範例，之後想要將它們解壓縮，您必須提供自己的程式碼來進行。</span><span class="sxs-lookup"><span data-stu-id="1c94c-116">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="1c94c-117">解決這項限制的其中一種方法是將壓縮的範例寫入至新的 ASF 檔案，然後將它們重新讀取為一般、未壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="1c94c-117">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="1c94c-118">若要使用同步讀取器接收壓縮的範例，請在播放之前或期間呼叫 [**IWMSyncReader：： SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) 。</span><span class="sxs-lookup"><span data-stu-id="1c94c-118">To receive compressed samples with the synchronous reader, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) before or during playback.</span></span> <span data-ttu-id="1c94c-119">針對 *fCompressed* 傳遞 true。</span><span class="sxs-lookup"><span data-stu-id="1c94c-119">Pass true for *fCompressed*.</span></span>

> [!Note]  
> <span data-ttu-id="1c94c-120">影像串流對壓縮的資料流程傳遞而言無效。</span><span class="sxs-lookup"><span data-stu-id="1c94c-120">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="1c94c-121">如果您將影像串流從某個檔案複製到另一個檔案，它就無法在新的檔案中使用。</span><span class="sxs-lookup"><span data-stu-id="1c94c-121">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="1c94c-122">若要從檔案複製影像串流至檔案，請依輸出號碼抓取影像串流範例，並將它們包含在新的檔案中，如同包含新的影像串流一樣。</span><span class="sxs-lookup"><span data-stu-id="1c94c-122">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1c94c-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c94c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c94c-124">**使用同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="1c94c-124">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




