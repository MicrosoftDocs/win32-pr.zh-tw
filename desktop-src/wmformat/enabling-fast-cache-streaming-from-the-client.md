---
title: 從用戶端啟用快速快取串流
description: 從用戶端啟用快速快取串流
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows Media Format SDK，啟用快取記憶體串流
- Windows Media Format SDK，快速快取串流
- Advanced Systems Format (ASF) ，啟用快速快取串流
- ASF (Advanced Systems Format) ，啟用快速快取串流
- Advanced Systems Format (ASF) 、Fast Cache 串流
- ASF (Advanced Systems Format) 、Fast Cache 串流
- 資料流程，啟用快取記憶體串流
- 快取記憶體串流，啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374431"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a><span data-ttu-id="6ce2c-111">從用戶端啟用快速快取串流</span><span class="sxs-lookup"><span data-stu-id="6ce2c-111">Enabling Fast Cache Streaming from the Client</span></span>

<span data-ttu-id="6ce2c-112">快取是一種串流技術，在此技術中，伺服器伺機會以比播放所需的位元速率更高的位元速率來串流處理內容。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-112">Fast Cache is a streaming technology in which the server opportunistically streams content at a higher bit rate than what is needed for playback.</span></span>

<span data-ttu-id="6ce2c-113">如果可用的頻寬高於內容的位元速率，以較高的速率快取資料流程，並緩衝處理內容。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-113">If the available bandwidth is higher than the bit rate of the content, Fast Cache streams at the higher rate and buffers the content.</span></span> <span data-ttu-id="6ce2c-114">這有助於在網路變得擁塞時減少中斷。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-114">This helps to reduce interruptions later if the network becomes congested.</span></span> <span data-ttu-id="6ce2c-115">如果網路頻寬低於內容的位元速率，則快速快取會在播放開始之前緩衝部分資料。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-115">If network bandwidth is lower than the bit rate of the content, Fast Cache buffers a portion of the data before playback starts.</span></span> <span data-ttu-id="6ce2c-116">針對不可靠的網路（例如無線網路），或遇到網路流量（例如纜線數據機）大量波動的網路，建議使用 Fast Cache。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-116">Fast Cache is recommended for unreliable networks, such as wireless networks, or networks that experience large fluctuations in network traffic, such as cable modems.</span></span> <span data-ttu-id="6ce2c-117">此外，也建議將變數位元速率 (VBR) 內容。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-117">It is also recommended for variable bit rate (VBR) content.</span></span> <span data-ttu-id="6ce2c-118">VBR 內容的頻寬需求不是常數，而 Fast Cache 可讓讀取器在較低位的部分期間緩衝串流。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-118">The bandwidth requirements for VBR content are not constant, and Fast Cache enables the reader to buffer the stream during the lower-bit-rate portions.</span></span>

<span data-ttu-id="6ce2c-119">快速快取串流僅支援隨選內容。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-119">Fast Cache streaming is supported only for on-demand content.</span></span> <span data-ttu-id="6ce2c-120">此外，伺服器必須設定為使用快速快取串流。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-120">In addition, the server must be configured to use Fast Cache streaming.</span></span>

<span data-ttu-id="6ce2c-121">若要啟用讀取器物件中的快速快取，請使用值 **TRUE** 來呼叫 [**IWMReaderNetworkConfig2：： SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching)和 [**IWMReaderNetworkConfig2：： SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache)方法。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-121">To enable Fast Cache in the reader object, call the [**IWMReaderNetworkConfig2::SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) and [**IWMReaderNetworkConfig2::SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) methods with the value **TRUE**.</span></span> <span data-ttu-id="6ce2c-122">第一個方法可讓讀取器快取資料流程處理的內容。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-122">The first method enables the reader to cache streamed content.</span></span> <span data-ttu-id="6ce2c-123">第二個可讓您特別使用快速快取。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-123">The second enables the use of Fast Cache in particular.</span></span>

<span data-ttu-id="6ce2c-124">使用這些設定時，如果網路頻寬明顯高於或低於內容的位元速率，且伺服器支援，則讀取器會依預設啟用快速快取。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-124">With these settings, the reader will activate Fast Cache by default if the network bandwidth is significantly higher or lower than the bit rate of the content, and if the server supports it.</span></span> <span data-ttu-id="6ce2c-125">使用者也可以藉由將下列一或多個修飾詞新增至 URL，來控制 reader 物件是否使用快速快取。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-125">The user can also control whether the reader object uses Fast Cache by adding one or more of the following modifiers to the URL.</span></span>



| <span data-ttu-id="6ce2c-126">修飾詞</span><span class="sxs-lookup"><span data-stu-id="6ce2c-126">Modifier</span></span>         | <span data-ttu-id="6ce2c-127">Description</span><span class="sxs-lookup"><span data-stu-id="6ce2c-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce2c-128">WMCache</span><span class="sxs-lookup"><span data-stu-id="6ce2c-128">WMCache</span></span>          | <span data-ttu-id="6ce2c-129">如果有此修飾詞，值 ' 0 ' 會明確停用快取，而值 ' 1 ' 則會明確啟用快取。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-129">If this modifier is present, the value '0' explicitly disables Fast Cache, while the value '1' explicitly enables it.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="6ce2c-130">WMBitrate</span><span class="sxs-lookup"><span data-stu-id="6ce2c-130">WMBitrate</span></span>        | <span data-ttu-id="6ce2c-131">此修飾詞會指定伺服器的最大位元速率。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-131">This modifier specifies the maximum bit rate from the server.</span></span> <span data-ttu-id="6ce2c-132">此修飾詞可用來限制快速快取為特定的頻寬限制。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-132">This modifier can be used to restrict Fast Cache to a certain bandwidth limit.</span></span> <span data-ttu-id="6ce2c-133">如果已透過呼叫 [**IWMReaderNetworkConfig：： SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth)來設定明確的連接頻寬，則會忽略此修飾詞。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-133">This modifier is ignored if an explicit connection bandwidth is already set with a call to [**IWMReaderNetworkConfig::SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span></span> |
| <span data-ttu-id="6ce2c-134">WMContentBitrate</span><span class="sxs-lookup"><span data-stu-id="6ce2c-134">WMContentBitrate</span></span> | <span data-ttu-id="6ce2c-135">此修飾詞會指定內容的位元速率。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-135">This modifier specifies the bit rate for the content.</span></span> <span data-ttu-id="6ce2c-136">如果有的話，讀取器會使用這個修飾詞（如果有的話）會從多位元率選取資料流程 (MBR) 檔。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-136">The reader uses this modifier, if present, when it selects streams from a multiple bit rate (MBR) file.</span></span> <span data-ttu-id="6ce2c-137">這可能會導致讀取器透過慢速連線接收較高的位元速率內容，這會導致很長的緩衝時間和延遲。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-137">This can cause the reader to receive high bit rate content over a slow connection, which results in very long buffering times and delays.</span></span>                                          |



 

<span data-ttu-id="6ce2c-138">無論網路頻寬或內容的位元速率，WMCache = 1 都會強制讀取器使用快速快取串流，而不考慮任何先前對 **SetEnableFastCache** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-138">The modifier WMCache=1 forces the reader to use Fast Cache streaming, regardless of the network bandwith or the bit rate of the content and regardless of any previous calls to **SetEnableFastCache**.</span></span> <span data-ttu-id="6ce2c-139">但是，它不會覆寫讀取器上的 **SetEnableContentCaching** 設定;也不會覆寫伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="6ce2c-139">However, it does not override the **SetEnableContentCaching** setting on the reader; nor does it override the server configuration.</span></span>

<span data-ttu-id="6ce2c-140">URL 修飾詞的格式如下：</span><span class="sxs-lookup"><span data-stu-id="6ce2c-140">URL modifiers have the following form:</span></span>

<span data-ttu-id="6ce2c-141">*url*？*修飾* = 詞 *值*</span><span class="sxs-lookup"><span data-stu-id="6ce2c-141">*url*?*modifier*=*value*</span></span>

<span data-ttu-id="6ce2c-142">例如：</span><span class="sxs-lookup"><span data-stu-id="6ce2c-142">For example:</span></span>

<span data-ttu-id="6ce2c-143">mms://MyServer/MyVideo.wmv 嗎？WMCache = 1</span><span class="sxs-lookup"><span data-stu-id="6ce2c-143">mms://MyServer/MyVideo.wmv?WMCache=1</span></span>

<span data-ttu-id="6ce2c-144">可以指定一個以上的修飾詞;使用連字號 (&) 來分隔它們：</span><span class="sxs-lookup"><span data-stu-id="6ce2c-144">More than one modifier can specified; use an ampersand (&) to separate them:</span></span>

<span data-ttu-id="6ce2c-145">mms://MyServer/MyVideo.wmv 嗎？WMCache = 1&WMContentBitrate = 56000</span><span class="sxs-lookup"><span data-stu-id="6ce2c-145">mms://MyServer/MyVideo.wmv?WMCache=1&WMContentBitrate=56000</span></span>

 

 




