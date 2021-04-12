---
description: Windows Media 來源篩選
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows Media 來源篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe60a038cfd5109a5c55ca6c40640d39b2426d3a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195719"
---
# <a name="windows-media-source-filter"></a><span data-ttu-id="ac50c-103">Windows Media 來源篩選</span><span class="sxs-lookup"><span data-stu-id="ac50c-103">Windows Media Source Filter</span></span>

<span data-ttu-id="ac50c-104">此篩選器是 Windows Media®內容的舊版來源篩選器。</span><span class="sxs-lookup"><span data-stu-id="ac50c-104">This filter is the legacy source filter for Windows Media® content.</span></span> <span data-ttu-id="ac50c-105">它是由 Windows Media Player 6.4 所使用。</span><span class="sxs-lookup"><span data-stu-id="ac50c-105">It is used by Windows Media Player 6.4.</span></span> <span data-ttu-id="ac50c-106">一般而言，使用此篩選器的最簡單且最可靠的方式，就是使用 Windows Media Player 6.4 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="ac50c-106">In general, the simplest and most reliable way to use this filter is to use the Windows Media Player 6.4 ActiveX control.</span></span> <span data-ttu-id="ac50c-107">此篩選器公開的許多方法也會透過 ActiveX 控制項公開。</span><span class="sxs-lookup"><span data-stu-id="ac50c-107">Many of the methods exposed by this filter are also exposed through the ActiveX control.</span></span> <span data-ttu-id="ac50c-108">如需詳細資訊，請參閱 Windows Media Player SDK。</span><span class="sxs-lookup"><span data-stu-id="ac50c-108">See the Windows Media Player SDK for more information.</span></span>

<span data-ttu-id="ac50c-109">當此篩選器指定本機 ASF 檔案的名稱或遠端檔案的 URL 時，它會讀取檔案、剖析壓縮的資料流程，並為每個檔案建立輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="ac50c-109">When this filter is given the name of a local ASF file or a URL for a remote file, it reads the file, parses the compressed streams, and creates an output pin for each one.</span></span> <span data-ttu-id="ac50c-110">此篩選器不會使用 Windows Media 格式 SDK。</span><span class="sxs-lookup"><span data-stu-id="ac50c-110">This filter does not use the Windows Media Format SDK.</span></span> <span data-ttu-id="ac50c-111">它會使用 Windows Media 解碼器的可安裝編解碼器版本，而不是 SQL-DMO 版本。</span><span class="sxs-lookup"><span data-stu-id="ac50c-111">It uses the installable codec versions of the Windows Media decoders, not the DMO versions.</span></span> <span data-ttu-id="ac50c-112">音訊輸出圖釘一律會連接到 ASF 的處理常式篩選器，而影片 pin 一律會連接到 ASF ICM 處理常式。</span><span class="sxs-lookup"><span data-stu-id="ac50c-112">The audio output pin always connects to the ASF ACM Handler filter, and the video pin always connects to the ASF ICM Handler.</span></span> <span data-ttu-id="ac50c-113"> (ICM 在此案例中是指視訊壓縮管理員的原始名稱。 ) 篩選器不支援搜尋。</span><span class="sxs-lookup"><span data-stu-id="ac50c-113">(ICM in this case refers to the original name of the Video Compression Manager.) The filter does not support seeking.</span></span>

<span data-ttu-id="ac50c-114">下圖顯示具有此篩選的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="ac50c-114">The following diagram shows a filter graph with this filter.</span></span>

![windows media 來源篩選圖形](images/wms-wmv-graph.png)

<span data-ttu-id="ac50c-116">為了維持與 Windows Media Player 6.4 的回溯相容性，此篩選器是具有 .wma、.wmv 和 .asf 副檔名之檔案的預設來源篩選。</span><span class="sxs-lookup"><span data-stu-id="ac50c-116">To maintain backward compatibility with Windows Media Player 6.4, this filter is the default source filter for files with .wma, .wmv, and .asf file extensions.</span></span> <span data-ttu-id="ac50c-117">針對檔案播放，較新的應用程式應該使用 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="ac50c-117">For file playback, newer applications should use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="ac50c-118">但是，WM ASF 讀取器不支援播放資料流程內容。</span><span class="sxs-lookup"><span data-stu-id="ac50c-118">However, the WM ASF Reader does not support playback of streamed content.</span></span>

<span data-ttu-id="ac50c-119">應用程式播放資料流程式 Windows 媒體內容的最簡單方式是使用 Windows Media Player SDK。</span><span class="sxs-lookup"><span data-stu-id="ac50c-119">The simplest way for an application to play streamed Windows Media-based content is to use the Windows Media Player SDK.</span></span> <span data-ttu-id="ac50c-120">另一個選項是使用 Windows Media Format SDK。</span><span class="sxs-lookup"><span data-stu-id="ac50c-120">Another option is to use the Windows Media Format SDK.</span></span> <span data-ttu-id="ac50c-121">不建議您嘗試以 Windows Media 來源篩選器為基礎來建立自訂播放機。</span><span class="sxs-lookup"><span data-stu-id="ac50c-121">Attempting to create a custom player based on the Windows Media Source Filter is not recommended.</span></span>



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac50c-122">篩選介面</span><span class="sxs-lookup"><span data-stu-id="ac50c-122">Filter interfaces</span></span>                        | <span data-ttu-id="ac50c-123">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IAMChannelInfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo)、 [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking)、 [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)、 [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)、 [**IAMNetShowConfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig)、 [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops)、 [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll)、 [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus)、 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="ac50c-123">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMChannelInfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IAMNetShowConfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops), [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span> |
| <span data-ttu-id="ac50c-124">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="ac50c-124">Input pin media types</span></span>                    | <span data-ttu-id="ac50c-125">不適用。</span><span class="sxs-lookup"><span data-stu-id="ac50c-125">Not applicable.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ac50c-126">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="ac50c-126">Input pin interfaces</span></span>                     | <span data-ttu-id="ac50c-127">不適用。</span><span class="sxs-lookup"><span data-stu-id="ac50c-127">Not applicable.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ac50c-128">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="ac50c-128">Output pin media types</span></span>                   | <span data-ttu-id="ac50c-129">會根據 ASF 檔案內的資料流程而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ac50c-129">Varies depending on the streams within the ASF file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ac50c-130">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="ac50c-130">Output pin interfaces</span></span>                    | [<span data-ttu-id="ac50c-131">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="ac50c-131">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ac50c-132">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="ac50c-132">Filter CLSID</span></span>                             | <span data-ttu-id="ac50c-133">請參閱備註</span><span class="sxs-lookup"><span data-stu-id="ac50c-133">See Remarks</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ac50c-134">可執行檔</span><span class="sxs-lookup"><span data-stu-id="ac50c-134">Executable</span></span>                               | <span data-ttu-id="ac50c-135">dxmasf.dll</span><span class="sxs-lookup"><span data-stu-id="ac50c-135">dxmasf.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="ac50c-136">優點</span><span class="sxs-lookup"><span data-stu-id="ac50c-136">Merit</span></span>](merit.md)                       | <span data-ttu-id="ac50c-137">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="ac50c-137">MERIT\_NORMAL</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="ac50c-138">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="ac50c-138">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ac50c-139">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ac50c-139">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="ac50c-140">備註</span><span class="sxs-lookup"><span data-stu-id="ac50c-140">Remarks</span></span>

<span data-ttu-id="ac50c-141">Qnetwork 中未定義篩選的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="ac50c-141">The filter's CLSID is not defined in qnetwork.h.</span></span> <span data-ttu-id="ac50c-142">在您自己的標頭檔中使用此宏：</span><span class="sxs-lookup"><span data-stu-id="ac50c-142">Use this macro in your own header file:</span></span>


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a><span data-ttu-id="ac50c-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac50c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac50c-144">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="ac50c-144">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="ac50c-145">在 DirectShow 中讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="ac50c-145">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="ac50c-146">WM ASF 讀取器篩選器</span><span class="sxs-lookup"><span data-stu-id="ac50c-146">WM ASF Reader Filter</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 



