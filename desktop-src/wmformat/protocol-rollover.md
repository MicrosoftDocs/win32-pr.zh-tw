---
title: 通訊協定變換
description: 通訊協定變換
ms.assetid: 61db5e2b-4858-446e-9a27-e0305b46683d
keywords:
- Windows Media Format SDK，通訊協定變換
- Advanced Systems Format (ASF) ，通訊協定變換
- ASF (Advanced Systems Format) ，通訊協定變換
- 通訊協定變換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2de8d0496467535f5740a10082f82e285c11ef6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023046"
---
# <a name="protocol-rollover"></a><span data-ttu-id="15304-107">通訊協定變換</span><span class="sxs-lookup"><span data-stu-id="15304-107">Protocol Rollover</span></span>

<span data-ttu-id="15304-108">通訊協定變換是一種程式，讓讀取器物件探索伺服器所提供的最佳串流通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15304-108">Protocol rollover is a process whereby the reader object discovers the best streaming protocol available from a server.</span></span> <span data-ttu-id="15304-109">只要開啟包含 "mms" 配置的 URL，讀取器就會使用通訊協定變換。</span><span class="sxs-lookup"><span data-stu-id="15304-109">The reader uses protocol rollover whenever it opens a URL that contains an "mms" scheme.</span></span>

<span data-ttu-id="15304-110">讀取器支援數個通訊協定：</span><span class="sxs-lookup"><span data-stu-id="15304-110">The reader supports several protocols:</span></span>

-   <span data-ttu-id="15304-111">即時串流通訊協定 (RTSP) </span><span class="sxs-lookup"><span data-stu-id="15304-111">Real Time Streaming Protocol (RTSP)</span></span>
-   <span data-ttu-id="15304-112">超文字傳輸通訊協定 (HTTP)</span><span class="sxs-lookup"><span data-stu-id="15304-112">Hypertext Transfer Protocol (HTTP)</span></span>
-   <span data-ttu-id="15304-113">Microsoft Media Server (MMS) </span><span class="sxs-lookup"><span data-stu-id="15304-113">Microsoft Media Server (MMS)</span></span>

<span data-ttu-id="15304-114">RTSP 和 MMS 通訊協定兩者都有兩種，一種是使用 [*UDP*](wmformat-glossary.md) 作為基礎傳遞通訊協定，而另一種使用 TCP。</span><span class="sxs-lookup"><span data-stu-id="15304-114">The RTSP and MMS protocols both come in two flavors, one using [*UDP*](wmformat-glossary.md) as the underlying delivery protocol, and the other using TCP.</span></span>

<span data-ttu-id="15304-115">讀取器物件一律會使用 TCP 來執行播放控制命令，但它可以使用 TCP 或 UDP 來傳遞資料流程內容。</span><span class="sxs-lookup"><span data-stu-id="15304-115">The reader object always uses TCP for playback control commands, but it can use either TCP or UDP for delivery of the streamed content.</span></span> <span data-ttu-id="15304-116">UDP 是內容傳遞的慣用方式，因為它的頻寬額外負荷較于 TCP。</span><span class="sxs-lookup"><span data-stu-id="15304-116">UDP is preferred for content delivery, because it imposes less bandwidth overhead than TCP.</span></span> <span data-ttu-id="15304-117">TCP 通訊協定可透過使用「虛擬電路」確保可靠的傳輸，但是這麼做的代價是，TCP 並不適合用於數位媒體串流，在此情況下，有效的頻寬使用會比較重要，因為這種情況偶爾會遺失封包。</span><span class="sxs-lookup"><span data-stu-id="15304-117">The TCP protocol ensures reliable transport through the use of "virtual circuits," but the cost of doing so means that TCP is not as well suited for digital media streams, where efficient use of bandwidth is more important that occasional lost packets.</span></span>

<span data-ttu-id="15304-118">當 URL 指定 "mms://" 時，讀取器會嘗試使用下列通訊協定來傳遞資料（依下列順序）：</span><span class="sxs-lookup"><span data-stu-id="15304-118">When a URL specifies "mms://", the reader attempts to use the following protocols for data delivery, in the following order:</span></span>

1.  <span data-ttu-id="15304-119">使用 UDP) RTSPU (RTSP</span><span class="sxs-lookup"><span data-stu-id="15304-119">RTSPU (RTSP using UDP)</span></span>
2.  <span data-ttu-id="15304-120">使用 TCP) RTSPT (RTSP</span><span class="sxs-lookup"><span data-stu-id="15304-120">RTSPT (RTSP using TCP)</span></span>
3.  <span data-ttu-id="15304-121">使用 UDP) MMSU (MMS</span><span class="sxs-lookup"><span data-stu-id="15304-121">MMSU (MMS using UDP)</span></span>
4.  <span data-ttu-id="15304-122">使用 TCP) MMST (MMS</span><span class="sxs-lookup"><span data-stu-id="15304-122">MMST (MMS using TCP)</span></span>
5.  <span data-ttu-id="15304-123">HTTP</span><span class="sxs-lookup"><span data-stu-id="15304-123">HTTP</span></span>

<span data-ttu-id="15304-124">HTTP 是以 TCP 為基礎的單向通訊協定，它是 Web 服務器所使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15304-124">HTTP is a one-way protocol based on TCP, and is the protocol used by Web servers.</span></span> <span data-ttu-id="15304-125">使用 RTSP 進行串流處理的效率較低。</span><span class="sxs-lookup"><span data-stu-id="15304-125">Streaming with HTTP is less efficient that using RTSP.</span></span> <span data-ttu-id="15304-126">不過，大部分的防火牆都會設定為接受 HTTP 要求，而通常會拒絕其他串流通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15304-126">However, most firewalls are configured to accept HTTP requests, whereas they typically reject other streaming protocols.</span></span>

<span data-ttu-id="15304-127">Microsoft Windows Server 2003 中的 windows Media Services 9 系列將會拒絕 Windows Media Format SDK 讀取器中的任何 MMSU 或 MMST 要求，因為 RTSP 是慣用的串流通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15304-127">Windows Media Services 9 Series in Microsoft Windows Server 2003 will reject any MMSU or MMST requests from a Windows Media Format SDK reader, because RTSP is the preferred streaming protocol.</span></span> <span data-ttu-id="15304-128">Windows Media Services 4.1 版及更早版本不支援 RTSP。</span><span class="sxs-lookup"><span data-stu-id="15304-128">Windows Media Services version 4.1 and earlier do not support RTSP.</span></span> <span data-ttu-id="15304-129">在此情況下，讀取器物件會切換回 MMSU 或 HTTP。</span><span class="sxs-lookup"><span data-stu-id="15304-129">In this case the reader object falls back to MMSU or HTTP.</span></span>

<span data-ttu-id="15304-130">如果 URL 配置提供特定的通訊協定（例如 RTSPU 的 "rtspu://" 或 HTTP 的 "HTTPs://"），則不適用通訊協定變換。</span><span class="sxs-lookup"><span data-stu-id="15304-130">Protocol rollover does not apply if the URL scheme gives a specific protocol, such as "rtspu://" for RTSPU or "https://" for HTTP.</span></span> <span data-ttu-id="15304-131">如果 URL 配置為 "rtsp://"，則讀取器會嘗試 RTSPU 和 RTSPT，但不會嘗試其他專案。</span><span class="sxs-lookup"><span data-stu-id="15304-131">If the URL scheme is "rtsp://", the reader tries RTSPU and RTSPT, but no others.</span></span>

<span data-ttu-id="15304-132">讀取器開啟檔案之後，您可以在讀取器上呼叫 [**IWMReaderAdvanced2：： GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname) 方法，以查詢所使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15304-132">After the reader opens a file, you can query which protocol it is using by calling the [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname) method on the reader.</span></span> <span data-ttu-id="15304-133">在串流或下載內容時，此方法會在完全快取內容時立即傳回名稱， **GetProtocolName** 方法會傳回字串 "Cache"。</span><span class="sxs-lookup"><span data-stu-id="15304-133">While the content is being streamed or downloaded, this method returns the name as soon as the content is completely cached, the **GetProtocolName** method returns the string "Cache."</span></span>

<span data-ttu-id="15304-134">若要取得讀取器支援的所有 Windows Media server 通訊協定的名稱，請在讀取器上呼叫 [**IWMReaderNetworkConfig：： GetSupportedProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname) 方法。</span><span class="sxs-lookup"><span data-stu-id="15304-134">To get the names of all the Windows Media server protocols that the reader supports, call the [**IWMReaderNetworkConfig::GetSupportedProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname) method on the reader.</span></span> <span data-ttu-id="15304-135">您可以使用 **IWMReaderNetworkConfig** 介面，在讀取器的通訊協定變換清單中停用一或多個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15304-135">You can disable one or more of the protocols in the reader's protocol rollover list, using **IWMReaderNetworkConfig** interface.</span></span> <span data-ttu-id="15304-136">例如， [**IWMReaderNetworkConfig：： SetEnableTCP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp) 方法會啟用或停用以 TCP 為基礎的通訊協定，而 [**IWMReaderNetworkConfig：： SetEnableUDP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp) 會啟用或停用以 UDP 為基礎的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15304-136">For example, the [**IWMReaderNetworkConfig::SetEnableTCP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp) method enables or disables the TCP-based protocols, and [**IWMReaderNetworkConfig::SetEnableUDP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp) enables or disables the UDP-based protocols.</span></span> <span data-ttu-id="15304-137">這些方法只適用于通訊協定變換;如果 URL 配置包含特定的通訊協定，仍然可以使用這些通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15304-137">These methods apply only to protocol rollover; the protocols are still available if the URL scheme contains a specific protocol.</span></span> <span data-ttu-id="15304-138">通常沒有理由停用通訊協定變換中使用的任何通訊協定;這樣做可能會降低效能。</span><span class="sxs-lookup"><span data-stu-id="15304-138">There is usually no reason to disable any of the protocols used in protocol rollover; doing so can degrade performance.</span></span> <span data-ttu-id="15304-139">不過，它可能適用于測試。</span><span class="sxs-lookup"><span data-stu-id="15304-139">However, it might be useful for testing.</span></span>

 

 




