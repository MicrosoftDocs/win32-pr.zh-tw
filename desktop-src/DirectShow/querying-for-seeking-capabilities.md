---
description: 查詢搜尋功能
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: 查詢搜尋功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846571"
---
# <a name="querying-for-seeking-capabilities"></a><span data-ttu-id="81909-103">查詢搜尋功能</span><span class="sxs-lookup"><span data-stu-id="81909-103">Querying for Seeking Capabilities</span></span>

<span data-ttu-id="81909-104">Microsoft® DirectShow®支援 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面的搜尋。</span><span class="sxs-lookup"><span data-stu-id="81909-104">Microsoft® DirectShow® supports seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="81909-105">篩選圖形管理員會公開此介面，但搜尋功能一律會由圖形中的篩選器來執行。</span><span class="sxs-lookup"><span data-stu-id="81909-105">The Filter Graph Manager exposes this interface, but the seeking functionality is always implemented by filters in the graph.</span></span>

<span data-ttu-id="81909-106">某些資料無法 seeked。</span><span class="sxs-lookup"><span data-stu-id="81909-106">Some data cannot be seeked.</span></span> <span data-ttu-id="81909-107">例如，您不能從相機搜尋即時影片串流。</span><span class="sxs-lookup"><span data-stu-id="81909-107">For example, you cannot seek a live video stream from a camera.</span></span> <span data-ttu-id="81909-108">但是，如果資料流程是可搜尋的，則有各種類型的搜尋可能會受到支援。</span><span class="sxs-lookup"><span data-stu-id="81909-108">If a stream is seekable, however, there are various types of seeking it might support.</span></span> <span data-ttu-id="81909-109">這些包括：</span><span class="sxs-lookup"><span data-stu-id="81909-109">These include:</span></span>

-   <span data-ttu-id="81909-110">搜尋至資料流程中的任意位置。</span><span class="sxs-lookup"><span data-stu-id="81909-110">Seeking to an arbitrary position in the stream.</span></span>
-   <span data-ttu-id="81909-111">正在抓取資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="81909-111">Retrieving the duration of the stream.</span></span>
-   <span data-ttu-id="81909-112">正在抓取資料流程中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="81909-112">Retrieving the current position within the stream.</span></span>
-   <span data-ttu-id="81909-113">反向播放。</span><span class="sxs-lookup"><span data-stu-id="81909-113">Playing in reverse.</span></span>

<span data-ttu-id="81909-114">**IMediaSeeking** 介面會定義一組旗標，以尋找可描述可能搜尋功能的搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)。</span><span class="sxs-lookup"><span data-stu-id="81909-114">The **IMediaSeeking** interface defines a set of flags, [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), that describe the possible seeking capabilities.</span></span> <span data-ttu-id="81909-115">若要取出資料流程的功能，請呼叫 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 方法。</span><span class="sxs-lookup"><span data-stu-id="81909-115">To retrieve the stream's capabilities, call the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="81909-116">方法會傳回旗標的位元組合。</span><span class="sxs-lookup"><span data-stu-id="81909-116">The method returns a bitwise combination of flags.</span></span> <span data-ttu-id="81909-117">應用程式可以使用 & (位 **and**) 運算子來測試它們。</span><span class="sxs-lookup"><span data-stu-id="81909-117">The application can test them using the & (bitwise **AND**) operator.</span></span> <span data-ttu-id="81909-118">例如，下列程式碼會檢查圖形是否可以搜尋至任意位置：</span><span class="sxs-lookup"><span data-stu-id="81909-118">For example, the following code checks whether the graph can seek to an arbitrary position:</span></span>


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



