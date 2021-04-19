---
title: '參考元素 (已被取代) '
description: '參考元素 (已被取代) '
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Windows Media 中繼檔，reference 元素
- 中繼檔，reference 元素
- reference 元素
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966810"
---
# <a name="reference-element-deprecated"></a><span data-ttu-id="96233-106">參考元素 (已被取代) </span><span class="sxs-lookup"><span data-stu-id="96233-106">reference Element (deprecated)</span></span>

<span data-ttu-id="96233-107">本主題說明在目前版本的 Windows Media 中繼檔中不再使用的功能。</span><span class="sxs-lookup"><span data-stu-id="96233-107">This topic documents a feature that is no longer used in the current version of Windows Media Metafiles.</span></span>

<span data-ttu-id="96233-108">**Reference** 元素包含 url 的參考清單。</span><span class="sxs-lookup"><span data-stu-id="96233-108">The **reference** element contains a list of references to URLs.</span></span> <span data-ttu-id="96233-109">清單中的每個專案都有格式 Ref *XX*  =  *URL*，其中 *XX* 是整數，而 *url* 是 Advanced 系統格式的 url (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="96233-109">Each item in the list has the form Ref *XX* = *URL*, where *XX* is an integer and *URL* is the URL of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="96233-110">**語法**</span><span class="sxs-lookup"><span data-stu-id="96233-110">**Syntax**</span></span>


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



<span data-ttu-id="96233-111">以 *XX* 表示的整數必須是遞增順序。</span><span class="sxs-lookup"><span data-stu-id="96233-111">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="96233-112">也就是說，每一行中的整數必須大於上一行中的整數。</span><span class="sxs-lookup"><span data-stu-id="96233-112">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="96233-113">當用戶端程式讀取參考專案時，它會嘗試連接至清單中第一個 URL 所代表的媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="96233-113">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="96233-114">如果失敗，用戶端程式會嘗試連接到清單中下一個 URL 所代表的檔案。</span><span class="sxs-lookup"><span data-stu-id="96233-114">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="96233-115">用戶端程式會繼續執行清單，直到成功連接或到達清單結尾為止。</span><span class="sxs-lookup"><span data-stu-id="96233-115">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="96233-116">請注意，如果用戶端程式成功連接，則不會讀取清單中的任何後續 Url。</span><span class="sxs-lookup"><span data-stu-id="96233-116">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

<span data-ttu-id="96233-117">**範例程式碼**</span><span class="sxs-lookup"><span data-stu-id="96233-117">**Example Code**</span></span>

<span data-ttu-id="96233-118">在下列範例中，用戶端程式會先嘗試連接到以 mms URL 表示的檔案。</span><span class="sxs-lookup"><span data-stu-id="96233-118">In the following example, the client program would first attempt to connect to the file represented by the mms URL.</span></span> <span data-ttu-id="96233-119">如果失敗，用戶端程式會嘗試連接至 HTTP URL 所表示的檔案。</span><span class="sxs-lookup"><span data-stu-id="96233-119">If that failed, the client program would attempt to connect to the file represented by the http URL.</span></span>


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a><span data-ttu-id="96233-120">備註</span><span class="sxs-lookup"><span data-stu-id="96233-120">Remarks</span></span>

<span data-ttu-id="96233-121">ASF 檔案格式包含各種不同的媒體類型，包括音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="96233-121">The ASF file format encompasses a wide variety of media types including audio and video.</span></span> <span data-ttu-id="96233-122">ASF 檔案也會使用數種不同的副檔名，包括 .wma 和 .wmv。</span><span class="sxs-lookup"><span data-stu-id="96233-122">ASF files also use several different file name extensions, including .wma and .wmv.</span></span>

<span data-ttu-id="96233-123">以 *XX* 表示的整數必須是遞增順序。</span><span class="sxs-lookup"><span data-stu-id="96233-123">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="96233-124">也就是說，每一行中的整數必須大於上一行中的整數。</span><span class="sxs-lookup"><span data-stu-id="96233-124">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="96233-125">當用戶端程式讀取參考專案時，它會嘗試連接至清單中第一個 URL 所代表的媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="96233-125">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="96233-126">如果失敗，用戶端程式會嘗試連接到清單中下一個 URL 所代表的檔案。</span><span class="sxs-lookup"><span data-stu-id="96233-126">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="96233-127">用戶端程式會繼續執行清單，直到成功連接或到達清單結尾為止。</span><span class="sxs-lookup"><span data-stu-id="96233-127">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="96233-128">請注意，如果用戶端程式成功連接，則不會讀取清單中的任何後續 Url。</span><span class="sxs-lookup"><span data-stu-id="96233-128">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96233-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="96233-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96233-130">**舊版的 Windows Media 中繼檔 (已淘汰)**</span><span class="sxs-lookup"><span data-stu-id="96233-130">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




