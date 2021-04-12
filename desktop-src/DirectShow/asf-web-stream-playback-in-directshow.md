---
description: 在 DirectShow 中播放 ASF Web 串流
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: 在 DirectShow 中播放 ASF Web 串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d14a83d2baf9c11aa824f5d6358f62790c16b30
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317751"
---
# <a name="asf-web-stream-playback-in-directshow"></a><span data-ttu-id="d640c-103">在 DirectShow 中播放 ASF Web 串流</span><span class="sxs-lookup"><span data-stu-id="d640c-103">ASF Web Stream Playback in DirectShow</span></span>

<span data-ttu-id="d640c-104">Microsoft DirectShow 透過 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器在檔案播放案例中支援 web 串流，但您必須撰寫自己的 DirectShow 篩選器來捕捉和保存資料流程。</span><span class="sxs-lookup"><span data-stu-id="d640c-104">Microsoft DirectShow supports web streams in file playback scenarios through the [WM ASF Reader](wm-asf-reader-filter.md) filter, but you must write your own DirectShow filter to capture and persist the stream.</span></span>

> [!Note]  
> <span data-ttu-id="d640c-105">若要在從執行 Windows Media Services 的伺服器串流處理的內容中播放 web 串流，請使用內嵌在網頁中的 Windows Media Player 9 系列 ActiveX®控制項。</span><span class="sxs-lookup"><span data-stu-id="d640c-105">To play back web streams in content that is being streamed from a server running Windows Media Services, use the Windows Media Player 9 Series ActiveX® control embedded in a web page.</span></span>

 

<span data-ttu-id="d640c-106">當提供包含 WMMEDIATYPE FileTransfer 類型資料流程的檔案時 \_ ，WM ASF 讀取器將會為其建立輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="d640c-106">When given a file containing streams of type WMMEDIATYPE\_FileTransfer, the WM ASF Reader will create an output pin for it.</span></span> <span data-ttu-id="d640c-107">格式區塊將會是 [**WMT \_ WEBSTREAM \_ 格式**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) 結構。</span><span class="sxs-lookup"><span data-stu-id="d640c-107">The format block will be a [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure.</span></span> <span data-ttu-id="d640c-108"> (此結構記載于 Windows Media 格式 SDK 檔集。 ) 如果沒有可用來處理該媒體類型的下游篩選器，則 pin 將保持線上狀態，但檔案仍會播放音訊和/或影片串流。</span><span class="sxs-lookup"><span data-stu-id="d640c-108">(This structure is documented in the Windows Media Format SDK documentation.) If no downstream filter is available that can handle that media type, then the pin will remain unconnected, but the file will still play the audio and/or video streams.</span></span>

<span data-ttu-id="d640c-109">Web stream 中的每個媒體範例都包含 [**WMT \_ WEBSTREAM \_ 範例 \_ 標頭**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) 結構，其記載于 Windows media Format SDK 檔中。</span><span class="sxs-lookup"><span data-stu-id="d640c-109">Each media sample in a web stream contains a [**WMT\_WEBSTREAM\_SAMPLE\_HEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) structure, which is documented in the Windows Media Format SDK documentation.</span></span> <span data-ttu-id="d640c-110">根據 **wszURL** 成員的長度而定，結構的長度會有變動。</span><span class="sxs-lookup"><span data-stu-id="d640c-110">The structure has a variable length depending on the length of its **wszURL** member.</span></span> <span data-ttu-id="d640c-111">範例資料的指標一開始會指向此結構，而您必須將指標前移到結構的上方，才能存取資料流程中的實際資料。</span><span class="sxs-lookup"><span data-stu-id="d640c-111">The pointer to the sample data initially points to this structure, and you must advance the pointer past the structure in order to access the actual data in the stream.</span></span>

<span data-ttu-id="d640c-112">您的 web 資料流程處理常式篩選應以 [**CBaseRenderer**](cbaserenderer.md) 類別為基礎。</span><span class="sxs-lookup"><span data-stu-id="d640c-112">Your web stream handler filter should be based on the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="d640c-113">在 [**CBaseRenderer：:D orendersample**](cbaserenderer-dorendersample.md) 方法中，篩選準則將需要剖析結構以取得 web 資料流程的相關資訊，然後執行適當的動作。</span><span class="sxs-lookup"><span data-stu-id="d640c-113">In the [**CBaseRenderer::DoRenderSample**](cbaserenderer-dorendersample.md) method, the filter will need to parse the structure for information about the web stream, and then perform the appropriate action.</span></span> <span data-ttu-id="d640c-114">一般而言，這會牽涉到將檔案儲存到磁片，然後呼叫 [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) 和 [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) 或 [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) 函式，將檔案放入 Internet Explorer 快取中。</span><span class="sxs-lookup"><span data-stu-id="d640c-114">Typically, this will involve saving the file to disk, and then calling the [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) and [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) or [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) functions to place the files into the Internet Explorer cache.</span></span> <span data-ttu-id="d640c-115">篩選準則必須處理多部分檔案，也就是大於一個樣本的檔案，而且也必須處理轉譯命令（由 **WMT \_ WEBSTREAM \_ 範例 \_ 標頭 wSampleType** 成員指定）。</span><span class="sxs-lookup"><span data-stu-id="d640c-115">The filter must handle multipart files, that is, files that are larger than one sample, and also must handle render commands, which are specified by the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wSampleType** member.</span></span> <span data-ttu-id="d640c-116">篩選準則會將 [**EC \_ OLE \_ 事件**](ec-ole-event.md) 事件傳送至應用程式，以及 **WMT \_ WEBSTREAM \_ 範例標頭的文字 \_ 。 wszURL** 字串，其中包含要轉譯的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d640c-116">The filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event to the application, along with the text of the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wszURL** string which contains the name of the file to be rendered.</span></span> <span data-ttu-id="d640c-117">然後，應用程式會導致瀏覽器顯示指定的頁面。</span><span class="sxs-lookup"><span data-stu-id="d640c-117">The application then causes the browser to display the specified page.</span></span> <span data-ttu-id="d640c-118">如果已正確撰寫 web 資料流程，檔案應該已經在快取中。</span><span class="sxs-lookup"><span data-stu-id="d640c-118">If the web stream has been authored correctly, the file should already be in the cache.</span></span>

<span data-ttu-id="d640c-119">如需有關 WMT \_ WEBSTREAM \_ FORMAT 和 WMT \_ WEBSTREAM 範例標頭的詳細資訊 \_ \_ ，請參閱 Windows Media FORMAT SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="d640c-119">For more information on WMT\_WEBSTREAM\_FORMAT and WMT\_WEBSTREAM\_SAMPLE\_HEADER, see the Windows Media Format SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d640c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="d640c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d640c-121">在 DirectShow 中讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="d640c-121">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
