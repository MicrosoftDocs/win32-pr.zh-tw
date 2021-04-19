---
title: LOGURL 元素
description: LOGURL 元素會指示 Windows Media Player 將任何記錄資料提交至指定的 URL。
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- LOGURL 元素 Windows Media Player
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977503"
---
# <a name="logurl-element"></a><span data-ttu-id="b0cbf-104">LOGURL 元素</span><span class="sxs-lookup"><span data-stu-id="b0cbf-104">LOGURL Element</span></span>

<span data-ttu-id="b0cbf-105">**LOGURL** 元素會指示 Windows Media Player 將任何記錄資料提交至指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-105">The **LOGURL** element instructs Windows Media Player to submit any log data to the specified URL.</span></span>

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="b0cbf-106">屬性</span><span class="sxs-lookup"><span data-stu-id="b0cbf-106">Attributes</span></span>

<span data-ttu-id="b0cbf-107">需要) **HREF** (</span><span class="sxs-lookup"><span data-stu-id="b0cbf-107">**HREF** (required)</span></span>

<span data-ttu-id="b0cbf-108">可以處理記錄要求的主機 URL。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-108">URL to a host that is able to process logging requests.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b0cbf-109">父/子項目</span><span class="sxs-lookup"><span data-stu-id="b0cbf-109">Parent/Child Elements</span></span>



| <span data-ttu-id="b0cbf-110">階層</span><span class="sxs-lookup"><span data-stu-id="b0cbf-110">Hierarchy</span></span>       | <span data-ttu-id="b0cbf-111">元素</span><span class="sxs-lookup"><span data-stu-id="b0cbf-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="b0cbf-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b0cbf-112">Parent elements</span></span> | <span data-ttu-id="b0cbf-113">**ASX**， **進入**</span><span class="sxs-lookup"><span data-stu-id="b0cbf-113">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="b0cbf-114">子元素</span><span class="sxs-lookup"><span data-stu-id="b0cbf-114">Child elements</span></span>  | <span data-ttu-id="b0cbf-115">無</span><span class="sxs-lookup"><span data-stu-id="b0cbf-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="b0cbf-116">備註</span><span class="sxs-lookup"><span data-stu-id="b0cbf-116">Remarks</span></span>

<span data-ttu-id="b0cbf-117">**LOGURL** 元素可讓用戶端中繼檔播放清單將其他記錄資訊傳送到指定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-117">The **LOGURL** element enables a client metafile playlist to send additional logging information to specified servers.</span></span> <span data-ttu-id="b0cbf-118">當檔案開啟時，記錄資訊會自動傳送到播放清單的源伺服器，而且會在每個 **LOGURL** 中指定給 **ASX** 元素（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-118">Logging information is automatically sent to the origin server of a playlist when it is opened and to each **LOGURL** specified for the **ASX** element, if any are present.</span></span> <span data-ttu-id="b0cbf-119">當到達專案時，記錄資訊也會傳送到針對 **entry** 元素指定的每個 **LOGURL** 。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-119">Logging information is also sent to each **LOGURL** specified for an **ENTRY** element when that entry is reached.</span></span> <span data-ttu-id="b0cbf-120">在 **LOGURL** 元素的 **HREF** 屬性中指定的 URL 必須是能夠處理記錄要求的主控制項位址。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-120">The URL specified in the **HREF** attribute of a **LOGURL** element must be the address of a host that is able to process logging requests.</span></span> <span data-ttu-id="b0cbf-121">URL 可以是任何有效的 HTTP URL。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-121">The URL can be any valid HTTP URL.</span></span> <span data-ttu-id="b0cbf-122">URL 也可以指出 CGI 腳本的位置。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-122">The URL can also indicate the location of a CGI script.</span></span>

<span data-ttu-id="b0cbf-123">**LOGURL** 元素唯一有效的通訊協定為 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-123">The only valid protocols for a **LOGURL** element are HTTP and HTTPS.</span></span>

<span data-ttu-id="b0cbf-124">在 **ASX** 元素範圍內的 **LOGURL** 元素只適用于它所在的中繼檔，不論該中繼檔是否從其他中繼檔參考。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-124">A **LOGURL** element within the scope of an **ASX** element is applicable only to the metafile in which it resides, regardless of whether that metafile is referenced from another metafile.</span></span> <span data-ttu-id="b0cbf-125">**LOGURL** 元素會強制提交從其定義範圍內串流處理之所有內容的記錄資料，而且只會針對從其定義範圍內串流的內容進行提交。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-125">A **LOGURL** element forces the submission of log data for all content streamed from within its defined scope and only for content streamed from within its defined scope.</span></span> <span data-ttu-id="b0cbf-126">記錄檔資料會提交至源伺服器，以及範圍內每個 **LOGURL** 專案中所列的所有 url。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-126">Log data will be submitted to the origin server and to all URLs listed in every **LOGURL** element in scope.</span></span> <span data-ttu-id="b0cbf-127">記錄檔資料只會提交到每個列出的 URL 一次，即使相同的 URL 在指定的範圍內列出一次以上。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-127">Log data will be submitted only once to each listed URL, even if the same URL is listed more than once in a given scope.</span></span> <span data-ttu-id="b0cbf-128">重複 **專案** 會導致另一個提交至列出的 url。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-128">A repeat of an **ENTRY** would result in another submission to the listed URLs.</span></span>

<span data-ttu-id="b0cbf-129">中繼檔播放清單中的 **LOGURL** 元素數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-129">There is no limit to the number of **LOGURL** elements in a metafile playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="b0cbf-130">範例</span><span class="sxs-lookup"><span data-stu-id="b0cbf-130">Examples</span></span>


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



<span data-ttu-id="b0cbf-131">以下是有效 Url 的範例。</span><span class="sxs-lookup"><span data-stu-id="b0cbf-131">The following are examples of valid URLs.</span></span>

<span data-ttu-id="b0cbf-132">ISAPI 應用程式的 URL：</span><span class="sxs-lookup"><span data-stu-id="b0cbf-132">URL of an ISAPI application:</span></span>


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



<span data-ttu-id="b0cbf-133">CGI 腳本的 URL：</span><span class="sxs-lookup"><span data-stu-id="b0cbf-133">URL of a CGI script:</span></span>


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



<span data-ttu-id="b0cbf-134">有效的 HTTP URL：</span><span class="sxs-lookup"><span data-stu-id="b0cbf-134">A valid HTTP URL:</span></span>


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a><span data-ttu-id="b0cbf-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0cbf-135">Requirements</span></span>



| <span data-ttu-id="b0cbf-136">需求</span><span class="sxs-lookup"><span data-stu-id="b0cbf-136">Requirement</span></span> | <span data-ttu-id="b0cbf-137">值</span><span class="sxs-lookup"><span data-stu-id="b0cbf-137">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="b0cbf-138">版本</span><span class="sxs-lookup"><span data-stu-id="b0cbf-138">Version</span></span><br/> | <span data-ttu-id="b0cbf-139">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="b0cbf-139">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0cbf-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0cbf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0cbf-141">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="b0cbf-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b0cbf-142">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="b0cbf-142">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





