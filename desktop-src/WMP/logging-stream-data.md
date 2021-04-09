---
title: 記錄資料流程資料
description: 記錄資料流程資料
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Windows Media 中繼檔播放清單，記錄資料流程資料
- 播放清單、記錄資料流程資料
- 中繼檔播放清單，記錄資料流程資料
- Windows Media 中繼檔播放清單，資料流程資料記錄
- 播放清單、串流資料記錄
- 中繼檔播放清單，資料流程資料記錄
- 記錄資料流程資料
- 串流資料記錄
- Windows Media Player，記錄串流資料
- Windows Media Player，資料流程資料記錄
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092319"
---
# <a name="logging-stream-data"></a><span data-ttu-id="52a5d-113">記錄資料流程資料</span><span class="sxs-lookup"><span data-stu-id="52a5d-113">Logging Stream Data</span></span>

<span data-ttu-id="52a5d-114">您可以取得並使用已記錄的資訊來判斷檢視器行為，例如，查看資料流程的頻率，或特定使用者是否已查看串流以及品質的時間長度。</span><span class="sxs-lookup"><span data-stu-id="52a5d-114">Logged information can be acquired and used to determine viewer behavior, for example, how often a stream is viewed, or if a specific user viewed a stream and for how long at what quality.</span></span>

<span data-ttu-id="52a5d-115">記錄資訊會自動傳送至從中產生播放清單的伺服器。</span><span class="sxs-lookup"><span data-stu-id="52a5d-115">Logging information is automatically sent to the server from which the playlist originated.</span></span> <span data-ttu-id="52a5d-116">您也可以將記錄資訊傳送到其他伺服器，包括您專門用於記錄的網頁伺服器。</span><span class="sxs-lookup"><span data-stu-id="52a5d-116">You can also send logging information to additional servers, including web servers you use exclusively for logging.</span></span> <span data-ttu-id="52a5d-117">若要這樣做，請使用 **LOGURL** 元素，並指定 **HREF** 屬性的有效 URL。</span><span class="sxs-lookup"><span data-stu-id="52a5d-117">To do this, use the **LOGURL** element, specifying a valid URL for the **HREF** attribute.</span></span> <span data-ttu-id="52a5d-118">您可以將 **LOGURL** 元素包含為 **ASX** 元素的子系，以及做為個別 **專案** 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="52a5d-118">You can include **LOGURL** elements as children of the **ASX** element and as children of individual **ENTRY** elements.</span></span> <span data-ttu-id="52a5d-119">當播放清單第一次開啟時，會將記錄資訊傳送至源伺服器，並傳送至該 **ASX** 元素的 **LOGURL** 子系中指定的每個 URL。</span><span class="sxs-lookup"><span data-stu-id="52a5d-119">When the playlist is first opened, logging information is sent to the origin server and to each URL specified in **LOGURL** children of the **ASX** element.</span></span> <span data-ttu-id="52a5d-120">然後，當達到每個專案時，就會將該專案特定的記錄資訊傳送至 **Entry 專案** 的 **LOGURL** 子系中指定的每個 URL。</span><span class="sxs-lookup"><span data-stu-id="52a5d-120">Then, as each entry is reached, logging information specific to that entry is sent to each URL specified in **LOGURL** children of the **ENTRY** element.</span></span>

<span data-ttu-id="52a5d-121">Windows Media Format SDK 透過 **IWMSReaderNetworkConfig** 介面和下列方法支援 **LOGURL** 元素：</span><span class="sxs-lookup"><span data-stu-id="52a5d-121">The Windows Media Format SDK supports the **LOGURL** element through the **IWMSReaderNetworkConfig** interface and the following methods:</span></span>


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



<span data-ttu-id="52a5d-122">除了自動記錄的資訊之外，中繼檔播放清單也可以透過使用 **PARAM** 元素來記錄自訂資訊。</span><span class="sxs-lookup"><span data-stu-id="52a5d-122">In addition to the information that is automatically logged, a metafile playlist can log custom information through the use of the **PARAM** element.</span></span> <span data-ttu-id="52a5d-123">若要以這種方式使用 **PARAM** 專案，請將 **NAME** 屬性設定為 "log："，後面接著另一個冒號 ( "：" ) ，並以另一個冒號分隔的記錄功能變數名稱和選擇性 XML 命名空間。</span><span class="sxs-lookup"><span data-stu-id="52a5d-123">To use the **PARAM** element in this way, set the **NAME** attribute to "log:" followed by a log field name and an optional XML namespace separated from the field name by another colon (":").</span></span> <span data-ttu-id="52a5d-124">第二個冒號之後的所有專案都會被視為命名空間，因此功能變數名稱不應包含冒號。</span><span class="sxs-lookup"><span data-stu-id="52a5d-124">Everything after the second colon is treated as a namespace, so the field name should not contain a colon.</span></span>

<span data-ttu-id="52a5d-125">**NAME** 屬性中指定的記錄欄位設定為 **value** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="52a5d-125">The log field specified in the **NAME** attribute is set to the value of the **VALUE** attribute.</span></span> <span data-ttu-id="52a5d-126">如果記錄檔尚未包含具有指定名稱的欄位，則會加入該欄位。</span><span class="sxs-lookup"><span data-stu-id="52a5d-126">If the log does not already contain a field with the specified name, it will be added.</span></span>

<span data-ttu-id="52a5d-127">**範例程式碼**</span><span class="sxs-lookup"><span data-stu-id="52a5d-127">**Example Code**</span></span>


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a><span data-ttu-id="52a5d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="52a5d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52a5d-129">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="52a5d-129">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="52a5d-130">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="52a5d-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




