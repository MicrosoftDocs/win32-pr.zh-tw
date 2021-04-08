---
title: 在 DirectShow 中播放 Web 串流
description: 在 DirectShow 中播放 Web 串流
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，Web 串流播放
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、Web stream 播放
- ASF (Advanced Systems Format) 、Web stream 播放
- DirectShow，Web 串流播放
- Web 串流，DirectShow
- Web 串流，在 DirectShow 中播放
- 串流，在 DirectShow 中播放 Web 串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932035"
---
# <a name="web-stream-playback-in-directshow"></a><span data-ttu-id="387cc-113">在 DirectShow 中播放 Web 串流</span><span class="sxs-lookup"><span data-stu-id="387cc-113">Web Stream Playback in DirectShow</span></span>

<span data-ttu-id="387cc-114">Microsoft DirectShow 支援 Web 串流 (查看 [Web 串流](web-streams.md) ，以取得透過 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選檔案播放案例中) 的詳細資訊，但您必須撰寫自己的 DirectShow 篩選器來捕捉和保存資料流程。</span><span class="sxs-lookup"><span data-stu-id="387cc-114">Microsoft DirectShow supports Web streams (see [Web Streams](web-streams.md) for more information) in file playback scenarios through the [WM ASF Reader](wm-asf-reader-filter.md) filter, but you must write your own DirectShow filter to capture and persist the stream.</span></span>

> [!Note]  
> <span data-ttu-id="387cc-115">若要在從執行 Windows Media Services 的伺服器串流處理的內容中播放 Web 串流，請使用內嵌在網頁中的 Windows Media Player 9 系列 ActiveX®控制項。</span><span class="sxs-lookup"><span data-stu-id="387cc-115">To play back Web streams in content that is being streamed from a server running Windows Media Services, use the Windows Media Player 9 Series ActiveX® control embedded in a Web page.</span></span>

 

<span data-ttu-id="387cc-116">當提供包含 WMMEDIATYPE FileTransfer 類型資料流程的檔案時 \_ ，WM ASF 讀取器將會為其建立輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="387cc-116">When given a file containing streams of type WMMEDIATYPE\_FileTransfer, the WM ASF Reader will create an output pin for it.</span></span> <span data-ttu-id="387cc-117">格式區塊將會是 [**WMT \_ WEBSTREAM \_ 格式**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) 結構。</span><span class="sxs-lookup"><span data-stu-id="387cc-117">The format block will be a [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure.</span></span> <span data-ttu-id="387cc-118">如果沒有可用來處理該媒體類型的下游篩選器，則 pin 將保持未連線，但檔案仍會播放音訊和/或影片串流。</span><span class="sxs-lookup"><span data-stu-id="387cc-118">If no downstream filter is available that can handle that media type, then the pin will remain unconnected, but the file will still play the audio and/or video streams.</span></span>

<span data-ttu-id="387cc-119">請務必瞭解，Web stream 中的每個媒體範例都包含 [**WMT \_ WEBSTREAM \_ 範例 \_ 標頭**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) 結構，此結構的長度取決於其 **wszURL** 成員的長度。</span><span class="sxs-lookup"><span data-stu-id="387cc-119">It is important to understand that each media sample in a Web stream contains a [**WMT\_WEBSTREAM\_SAMPLE\_HEADER**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) structure, which has a variable length depending on the length of its **wszURL** member.</span></span> <span data-ttu-id="387cc-120">範例資料的指標一開始會指向此結構，而您必須將指標前移到結構的上方，才能存取資料流程中的實際資料。</span><span class="sxs-lookup"><span data-stu-id="387cc-120">The pointer to the sample data initially points to this structure, and you must advance the pointer past the structure in order to access the actual data in the stream.</span></span> <span data-ttu-id="387cc-121">您的 Web 資料流程處理常式篩選應以 **CBaseRenderer** 類別為基礎。</span><span class="sxs-lookup"><span data-stu-id="387cc-121">Your Web stream handler filter should be based on the **CBaseRenderer** class.</span></span> <span data-ttu-id="387cc-122">在 **DoRenderSample** 方法中，篩選準則將需要剖析結構以取得 Web 資料流程的相關資訊，然後執行適當的動作。</span><span class="sxs-lookup"><span data-stu-id="387cc-122">In the **DoRenderSample** method, the filter will need to parse the structure for information about the Web stream, and then perform the appropriate action.</span></span> <span data-ttu-id="387cc-123">一般而言，這會牽涉到將檔案儲存到磁片，然後呼叫 **CommitUrlCacheEntry** 和 **CreateUrlCacheEntry** 將檔案放入 Internet Explorer 快取中。</span><span class="sxs-lookup"><span data-stu-id="387cc-123">Typically, this will involve saving the file to disk, and then calling **CommitUrlCacheEntry** and **CreateUrlCacheEntry** to place the files into the Internet Explorer cache.</span></span> <span data-ttu-id="387cc-124">篩選準則必須處理多部分檔案，也就是大於一個樣本的檔案，而且也必須處理轉譯命令（由 **WMT \_ WEBSTREAM \_ 範例 \_ 標頭 wSampleType** 成員指定）。</span><span class="sxs-lookup"><span data-stu-id="387cc-124">The filter must handle multipart files, that is, files that are larger than one sample, and also must handle render commands, which are specified by the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wSampleType** member.</span></span> <span data-ttu-id="387cc-125">篩選準則會將 **EC \_ OLE \_ 事件** 連同 **WMT \_ WEBSTREAM \_ 範例 \_ 標頭** 的文字傳送至應用程式。 wszURL 字串包含要轉譯的檔案名。</span><span class="sxs-lookup"><span data-stu-id="387cc-125">The filter sends an **EC\_OLE\_EVENT** to the application, along with the text of the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wszURL** string which contains the name of the file to be rendered.</span></span> <span data-ttu-id="387cc-126">然後，應用程式會導致瀏覽器顯示指定的頁面。</span><span class="sxs-lookup"><span data-stu-id="387cc-126">The application then causes the browser to display the specified page.</span></span> <span data-ttu-id="387cc-127">如果已正確撰寫 Web 資料流程，檔案應該已經在快取中。</span><span class="sxs-lookup"><span data-stu-id="387cc-127">If the Web stream has been authored correctly, the file should already be in the cache.</span></span>

<span data-ttu-id="387cc-128">如需有關 **CBaseRenderer**、 **DoRenderSample** 和 **EC \_ OLE \_ 事件** 的詳細資訊，請參閱 DirectShow SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="387cc-128">For more information on **CBaseRenderer**, **DoRenderSample**, and **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="387cc-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="387cc-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="387cc-130">**Web 串流**</span><span class="sxs-lookup"><span data-stu-id="387cc-130">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




