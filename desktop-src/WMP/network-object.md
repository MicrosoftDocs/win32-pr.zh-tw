---
title: Network 物件
description: Network 物件提供的屬性和方法可用來存取與網路連接品質相關的統計資料，以及指定和取出網路 proxy 設定。
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- 網路物件 Windows Media Player
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104373463"
---
# <a name="network-object"></a><span data-ttu-id="4ad26-104">Network 物件</span><span class="sxs-lookup"><span data-stu-id="4ad26-104">Network Object</span></span>

<span data-ttu-id="4ad26-105">**Network** 物件提供的屬性和方法可用來存取與網路連接品質相關的統計資料，以及指定和取出網路 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="4ad26-105">The **Network** object provides properties and methods used to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="4ad26-106">**Network** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="4ad26-106">The **Network** object supports the following properties.</span></span>



| <span data-ttu-id="4ad26-107">屬性</span><span class="sxs-lookup"><span data-stu-id="4ad26-107">Property</span></span>                                           | <span data-ttu-id="4ad26-108">描述</span><span class="sxs-lookup"><span data-stu-id="4ad26-108">Description</span></span>                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ad26-109">頻寬</span><span class="sxs-lookup"><span data-stu-id="4ad26-109">bandWidth</span></span>](network-bandwidth.md)                 | <span data-ttu-id="4ad26-110">抓取媒體專案目前的頻寬。</span><span class="sxs-lookup"><span data-stu-id="4ad26-110">Retrieves the current bandwidth of the media item.</span></span>                                          |
| [<span data-ttu-id="4ad26-111">位元速率</span><span class="sxs-lookup"><span data-stu-id="4ad26-111">bitRate</span></span>](network-bitrate.md)                     | <span data-ttu-id="4ad26-112">抓取正在接收的目前位速率。</span><span class="sxs-lookup"><span data-stu-id="4ad26-112">Retrieves the current bit rate being received.</span></span>                                              |
| [<span data-ttu-id="4ad26-113">bufferingCount</span><span class="sxs-lookup"><span data-stu-id="4ad26-113">bufferingCount</span></span>](network-bufferingcount.md)       | <span data-ttu-id="4ad26-114">抓取在播放期間發生緩衝處理的次數。</span><span class="sxs-lookup"><span data-stu-id="4ad26-114">Retrieves the number of times buffering occurred during playback.</span></span>                           |
| [<span data-ttu-id="4ad26-115">bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="4ad26-115">bufferingProgress</span></span>](network-bufferingprogress.md) | <span data-ttu-id="4ad26-116">抓取已完成的緩衝百分比。</span><span class="sxs-lookup"><span data-stu-id="4ad26-116">Retrieves the percentage of buffering completed.</span></span>                                            |
| [<span data-ttu-id="4ad26-117">bufferingTime</span><span class="sxs-lookup"><span data-stu-id="4ad26-117">bufferingTime</span></span>](network-bufferingtime.md)         | <span data-ttu-id="4ad26-118">指定或抓取播放開始之前的緩衝時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4ad26-118">Specifies or retrieves the amount of buffering time in milliseconds before playback begins.</span></span> |
| [<span data-ttu-id="4ad26-119">downloadProgress</span><span class="sxs-lookup"><span data-stu-id="4ad26-119">downloadProgress</span></span>](network-downloadprogress.md)   | <span data-ttu-id="4ad26-120">抓取下載已完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="4ad26-120">Retrieves the percentage of download completed.</span></span>                                             |
| [<span data-ttu-id="4ad26-121">encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="4ad26-121">encodedFrameRate</span></span>](network-encodedframerate.md)   | <span data-ttu-id="4ad26-122">抓取內容作者指定的影片畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="4ad26-122">Retrieves the video frame rate specified by the content author.</span></span>                             |
| [<span data-ttu-id="4ad26-123">頻</span><span class="sxs-lookup"><span data-stu-id="4ad26-123">frameRate</span></span>](network-framerate.md)                 | <span data-ttu-id="4ad26-124">抓取目前的影片畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="4ad26-124">Retrieves the current video frame rate.</span></span>                                                     |
| [<span data-ttu-id="4ad26-125">framesSkipped</span><span class="sxs-lookup"><span data-stu-id="4ad26-125">framesSkipped</span></span>](network-framesskipped.md)         | <span data-ttu-id="4ad26-126">抓取播放期間略過的總畫面格數。</span><span class="sxs-lookup"><span data-stu-id="4ad26-126">Retrieves the total number of frames skipped during playback.</span></span>                               |
| [<span data-ttu-id="4ad26-127">lostPackets</span><span class="sxs-lookup"><span data-stu-id="4ad26-127">lostPackets</span></span>](network-lostpackets.md)             | <span data-ttu-id="4ad26-128">捕獲遺失的封包數目。</span><span class="sxs-lookup"><span data-stu-id="4ad26-128">Retrieves the number of packets lost.</span></span>                                                       |
| [<span data-ttu-id="4ad26-129">maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="4ad26-129">maxBandwidth</span></span>](network-maxbandwidth.md)           | <span data-ttu-id="4ad26-130">指定或抓取允許的最大頻寬。</span><span class="sxs-lookup"><span data-stu-id="4ad26-130">Specifies or retrieves the maximum allowed bandwidth.</span></span>                                       |
| [<span data-ttu-id="4ad26-131">maxBitRate</span><span class="sxs-lookup"><span data-stu-id="4ad26-131">maxBitRate</span></span>](network-maxbitrate.md)               | <span data-ttu-id="4ad26-132">抓取最大可能的影片位元速率。</span><span class="sxs-lookup"><span data-stu-id="4ad26-132">Retrieves the maximum possible video bit rate.</span></span>                                              |
| [<span data-ttu-id="4ad26-133">receivedPackets</span><span class="sxs-lookup"><span data-stu-id="4ad26-133">receivedPackets</span></span>](network-receivedpackets.md)     | <span data-ttu-id="4ad26-134">抓取收到的封包數目。</span><span class="sxs-lookup"><span data-stu-id="4ad26-134">Retrieves the number of packets received.</span></span>                                                   |
| [<span data-ttu-id="4ad26-135">receptionQuality</span><span class="sxs-lookup"><span data-stu-id="4ad26-135">receptionQuality</span></span>](network-receptionquality.md)   | <span data-ttu-id="4ad26-136">抓取過去30秒內收到的封包百分比。</span><span class="sxs-lookup"><span data-stu-id="4ad26-136">Retrieves the percentage of packets received in the last 30 seconds.</span></span>                        |
| [<span data-ttu-id="4ad26-137">recoveredPackets</span><span class="sxs-lookup"><span data-stu-id="4ad26-137">recoveredPackets</span></span>](network-recoveredpackets.md)   | <span data-ttu-id="4ad26-138">抓取已復原的封包數目。</span><span class="sxs-lookup"><span data-stu-id="4ad26-138">Retrieves the number of recovered packets.</span></span>                                                  |
| [<span data-ttu-id="4ad26-139">sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="4ad26-139">sourceProtocol</span></span>](network-sourceprotocol.md)       | <span data-ttu-id="4ad26-140">抓取用來接收資料的來源通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4ad26-140">Retrieves the source protocol used to receive data.</span></span>                                         |



 

<span data-ttu-id="4ad26-141">**Network** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="4ad26-141">The **Network** object supports the following methods.</span></span>



| <span data-ttu-id="4ad26-142">方法</span><span class="sxs-lookup"><span data-stu-id="4ad26-142">Method</span></span>                                                       | <span data-ttu-id="4ad26-143">描述</span><span class="sxs-lookup"><span data-stu-id="4ad26-143">Description</span></span>                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ad26-144">getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="4ad26-144">getProxyBypassForLocal</span></span>](network-getproxybypassforlocal.md) | <span data-ttu-id="4ad26-145">抓取值，指出如果源伺服器是在區域網路上，是否應略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4ad26-145">Retrieves a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="4ad26-146">getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="4ad26-146">getProxyExceptionList</span></span>](network-getproxyexceptionlist.md)   | <span data-ttu-id="4ad26-147">抓取 proxy 例外清單。</span><span class="sxs-lookup"><span data-stu-id="4ad26-147">Retrieves the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="4ad26-148">getProxyName</span><span class="sxs-lookup"><span data-stu-id="4ad26-148">getProxyName</span></span>](network-getproxyname.md)                     | <span data-ttu-id="4ad26-149">抓取要使用的 proxy 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad26-149">Retrieves the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="4ad26-150">getProxyPort</span><span class="sxs-lookup"><span data-stu-id="4ad26-150">getProxyPort</span></span>](network-getproxyport.md)                     | <span data-ttu-id="4ad26-151">抓取要使用的 proxy 埠。</span><span class="sxs-lookup"><span data-stu-id="4ad26-151">Retrieves the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="4ad26-152">getProxySettings</span><span class="sxs-lookup"><span data-stu-id="4ad26-152">getProxySettings</span></span>](network-getproxysettings.md)             | <span data-ttu-id="4ad26-153">抓取指定通訊協定的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="4ad26-153">Retrieves the proxy setting for a given protocol.</span></span>                                                                    |
| [<span data-ttu-id="4ad26-154">setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="4ad26-154">setProxyBypassForLocal</span></span>](network-setproxybypassforlocal.md) | <span data-ttu-id="4ad26-155">指定值，指出如果源伺服器是在區域網路上，是否應略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4ad26-155">Specifies a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="4ad26-156">setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="4ad26-156">setProxyExceptionList</span></span>](network-setproxyexceptionlist.md)   | <span data-ttu-id="4ad26-157">指定 proxy 例外清單。</span><span class="sxs-lookup"><span data-stu-id="4ad26-157">Specifies the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="4ad26-158">setProxyName</span><span class="sxs-lookup"><span data-stu-id="4ad26-158">setProxyName</span></span>](network-setproxyname.md)                     | <span data-ttu-id="4ad26-159">指定要使用之 proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad26-159">Specifies the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="4ad26-160">setProxyPort</span><span class="sxs-lookup"><span data-stu-id="4ad26-160">setProxyPort</span></span>](network-setproxyport.md)                     | <span data-ttu-id="4ad26-161">指定要使用的 proxy 埠。</span><span class="sxs-lookup"><span data-stu-id="4ad26-161">Specifies the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="4ad26-162">setProxySettings</span><span class="sxs-lookup"><span data-stu-id="4ad26-162">setProxySettings</span></span>](network-setproxysettings.md)             | <span data-ttu-id="4ad26-163">指定指定通訊協定的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="4ad26-163">Specifies the proxy setting for a given protocol.</span></span>                                                                    |



 

<span data-ttu-id="4ad26-164">**網路** 物件是透過下列屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="4ad26-164">The **Network** object is accessed through the following property.</span></span>



| <span data-ttu-id="4ad26-165">Object</span><span class="sxs-lookup"><span data-stu-id="4ad26-165">Object</span></span>                      | <span data-ttu-id="4ad26-166">屬性</span><span class="sxs-lookup"><span data-stu-id="4ad26-166">Property</span></span>                      |
|-----------------------------|-------------------------------|
| [<span data-ttu-id="4ad26-167">球員</span><span class="sxs-lookup"><span data-stu-id="4ad26-167">Player</span></span>](player-object.md) | [<span data-ttu-id="4ad26-168">network</span><span class="sxs-lookup"><span data-stu-id="4ad26-168">network</span></span>](player-network.md) |



 

## <a name="see-also"></a><span data-ttu-id="4ad26-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ad26-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad26-170">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="4ad26-170">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




