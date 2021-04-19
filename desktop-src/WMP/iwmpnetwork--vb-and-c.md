---
title: 'IWMPNetwork (VB 和 C ) 介面 (h.264. h) '
description: 提供屬性和方法來存取與網路連接品質相關的統計資料，以及指定和取出網路 proxy 設定。IWMPNetwork 介面會公開下列屬性。
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- IWMPNetwork (VB 和 C ) 介面 Windows Media Player
- IWMPNetwork (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976069"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a><span data-ttu-id="3c169-105">IWMPNetwork (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="3c169-105">IWMPNetwork (VB and C#) interface</span></span>

<span data-ttu-id="3c169-106">提供屬性和方法來存取與網路連接品質相關的統計資料，以及指定和取出網路 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="3c169-106">Provides properties and methods to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="3c169-107">**IWMPNetwork** 介面會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="3c169-107">The **IWMPNetwork** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="3c169-108">成員</span><span class="sxs-lookup"><span data-stu-id="3c169-108">Members</span></span>

<span data-ttu-id="3c169-109">**IWMPNetwork (VB 和 c # )** 介面都有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3c169-109">The **IWMPNetwork (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="3c169-110">方法</span><span class="sxs-lookup"><span data-stu-id="3c169-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3c169-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3c169-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3c169-112">方法</span><span class="sxs-lookup"><span data-stu-id="3c169-112">Methods</span></span>

<span data-ttu-id="3c169-113">**IWMPNetwork (VB 和 c # )** 介面都有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3c169-113">The **IWMPNetwork (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="3c169-114">方法</span><span class="sxs-lookup"><span data-stu-id="3c169-114">Method</span></span>                                                                                           | <span data-ttu-id="3c169-115">描述</span><span class="sxs-lookup"><span data-stu-id="3c169-115">Description</span></span>                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c169-116">**getProxyBypassForLocal**</span><span class="sxs-lookup"><span data-stu-id="3c169-116">**getProxyBypassForLocal**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | <span data-ttu-id="3c169-117">傳回值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3c169-117">Returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/> |
| [<span data-ttu-id="3c169-118">**getProxyExceptionList**</span><span class="sxs-lookup"><span data-stu-id="3c169-118">**getProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="3c169-119">傳回 proxy 例外清單。</span><span class="sxs-lookup"><span data-stu-id="3c169-119">Returns the proxy exception list.</span></span><br/>                                                                           |
| [<span data-ttu-id="3c169-120">**getProxyName**</span><span class="sxs-lookup"><span data-stu-id="3c169-120">**getProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | <span data-ttu-id="3c169-121">傳回要使用之 proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c169-121">Returns the name of the proxy server being used.</span></span><br/>                                                            |
| [<span data-ttu-id="3c169-122">**getProxyPort**</span><span class="sxs-lookup"><span data-stu-id="3c169-122">**getProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | <span data-ttu-id="3c169-123">傳回要使用的 proxy 埠。</span><span class="sxs-lookup"><span data-stu-id="3c169-123">Returns the proxy port being used.</span></span><br/>                                                                          |
| [<span data-ttu-id="3c169-124">**getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="3c169-124">**getProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | <span data-ttu-id="3c169-125">傳回通訊協定的 proxy 設定相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3c169-125">Returns information about the proxy settings for a protocol.</span></span><br/>                                                |
| [<span data-ttu-id="3c169-126">**setProxyBypassForLocal**</span><span class="sxs-lookup"><span data-stu-id="3c169-126">**setProxyBypassForLocal**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | <span data-ttu-id="3c169-127">指定如果源伺服器是在區域網路上，是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3c169-127">Specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/>                  |
| [<span data-ttu-id="3c169-128">**setProxyExceptionList**</span><span class="sxs-lookup"><span data-stu-id="3c169-128">**setProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="3c169-129">指定 proxy 例外清單。</span><span class="sxs-lookup"><span data-stu-id="3c169-129">Specifies the proxy exception list.</span></span><br/>                                                                         |
| [<span data-ttu-id="3c169-130">**setProxyName**</span><span class="sxs-lookup"><span data-stu-id="3c169-130">**setProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | <span data-ttu-id="3c169-131">指定要使用之 proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c169-131">Specifies the name of the proxy server to use.</span></span><br/>                                                              |
| [<span data-ttu-id="3c169-132">**setProxyPort**</span><span class="sxs-lookup"><span data-stu-id="3c169-132">**setProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | <span data-ttu-id="3c169-133">指定要使用的 proxy 埠。</span><span class="sxs-lookup"><span data-stu-id="3c169-133">Specifies the proxy port to use.</span></span><br/>                                                                            |
| [<span data-ttu-id="3c169-134">**setProxySettings**</span><span class="sxs-lookup"><span data-stu-id="3c169-134">**setProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | <span data-ttu-id="3c169-135">指定通訊協定的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="3c169-135">Specifies the proxy settings for a protocol.</span></span><br/>                                                                |



 

### <a name="properties"></a><span data-ttu-id="3c169-136">屬性</span><span class="sxs-lookup"><span data-stu-id="3c169-136">Properties</span></span>

<span data-ttu-id="3c169-137">**IWMPNetwork (VB 和 c # )** 介面都有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3c169-137">The **IWMPNetwork (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="3c169-138">屬性</span><span class="sxs-lookup"><span data-stu-id="3c169-138">Property</span></span>                                                                                          | <span data-ttu-id="3c169-139">存取類型</span><span class="sxs-lookup"><span data-stu-id="3c169-139">Access type</span></span>           | <span data-ttu-id="3c169-140">Description</span><span class="sxs-lookup"><span data-stu-id="3c169-140">Description</span></span>                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c169-141">**頻寬**</span><span class="sxs-lookup"><span data-stu-id="3c169-141">**bandWidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | <span data-ttu-id="3c169-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-142">Read-only</span></span><br/>  | <span data-ttu-id="3c169-143">取得媒體專案目前的頻寬。</span><span class="sxs-lookup"><span data-stu-id="3c169-143">Gets the current bandwidth of the media item.</span></span><br/>                                     |
| [<span data-ttu-id="3c169-144">**位元速率**</span><span class="sxs-lookup"><span data-stu-id="3c169-144">**bitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | <span data-ttu-id="3c169-145">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-145">Read-only</span></span><br/>  | <span data-ttu-id="3c169-146">取得所接收的目前位速率。</span><span class="sxs-lookup"><span data-stu-id="3c169-146">Gets the current bit rate being received.</span></span><br/>                                         |
| [<span data-ttu-id="3c169-147">**bufferingCount**</span><span class="sxs-lookup"><span data-stu-id="3c169-147">**bufferingCount**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | <span data-ttu-id="3c169-148">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-148">Read-only</span></span><br/>  | <span data-ttu-id="3c169-149">取得在播放期間發生緩衝處理的次數。</span><span class="sxs-lookup"><span data-stu-id="3c169-149">Gets the number of times buffering occurred during playback.</span></span><br/>                      |
| [<span data-ttu-id="3c169-150">**bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="3c169-150">**bufferingProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | <span data-ttu-id="3c169-151">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-151">Read-only</span></span><br/>  | <span data-ttu-id="3c169-152">取得緩衝處理已完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="3c169-152">Gets the percentage of buffering completed.</span></span><br/>                                       |
| [<span data-ttu-id="3c169-153">**bufferingTime**</span><span class="sxs-lookup"><span data-stu-id="3c169-153">**bufferingTime**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | <span data-ttu-id="3c169-154">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c169-154">Read/write</span></span><br/> | <span data-ttu-id="3c169-155">取得或設定播放開始之前的緩衝時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3c169-155">Gets or sets the amount of buffering time in milliseconds before playback begins.</span></span><br/> |
| [<span data-ttu-id="3c169-156">**downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="3c169-156">**downloadProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | <span data-ttu-id="3c169-157">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-157">Read-only</span></span><br/>  | <span data-ttu-id="3c169-158">取得下載已完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="3c169-158">Gets the percentage of downloading completed.</span></span><br/>                                     |
| [<span data-ttu-id="3c169-159">**encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="3c169-159">**encodedFrameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | <span data-ttu-id="3c169-160">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-160">Read-only</span></span><br/>  | <span data-ttu-id="3c169-161">取得內容作者指定的影片畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="3c169-161">Gets the video frame rate specified by the content author.</span></span><br/>                        |
| [<span data-ttu-id="3c169-162">**頻**</span><span class="sxs-lookup"><span data-stu-id="3c169-162">**frameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | <span data-ttu-id="3c169-163">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-163">Read-only</span></span><br/>  | <span data-ttu-id="3c169-164">取得目前的影片畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="3c169-164">Gets the current video frame rate.</span></span><br/>                                                |
| [<span data-ttu-id="3c169-165">**framesSkipped**</span><span class="sxs-lookup"><span data-stu-id="3c169-165">**framesSkipped**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | <span data-ttu-id="3c169-166">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-166">Read-only</span></span><br/>  | <span data-ttu-id="3c169-167">取得播放期間略過的總畫面格數。</span><span class="sxs-lookup"><span data-stu-id="3c169-167">Gets the total number of frames skipped during playback.</span></span><br/>                          |
| [<span data-ttu-id="3c169-168">**lostPackets**</span><span class="sxs-lookup"><span data-stu-id="3c169-168">**lostPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | <span data-ttu-id="3c169-169">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-169">Read-only</span></span><br/>  | <span data-ttu-id="3c169-170">取得遺失的封包數目。</span><span class="sxs-lookup"><span data-stu-id="3c169-170">Gets the number of packets lost.</span></span><br/>                                                  |
| [<span data-ttu-id="3c169-171">**maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="3c169-171">**maxBandwidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | <span data-ttu-id="3c169-172">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c169-172">Read/write</span></span><br/> | <span data-ttu-id="3c169-173">取得或設定允許的最大頻寬。</span><span class="sxs-lookup"><span data-stu-id="3c169-173">Gets or sets the maximum allowed bandwidth.</span></span><br/>                                       |
| [<span data-ttu-id="3c169-174">**maxBitRate**</span><span class="sxs-lookup"><span data-stu-id="3c169-174">**maxBitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | <span data-ttu-id="3c169-175">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-175">Read-only</span></span><br/>  | <span data-ttu-id="3c169-176">取得最大可能的影片位速率。</span><span class="sxs-lookup"><span data-stu-id="3c169-176">Gets the maximum possible video bit rate.</span></span><br/>                                         |
| [<span data-ttu-id="3c169-177">**receivedPackets**</span><span class="sxs-lookup"><span data-stu-id="3c169-177">**receivedPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | <span data-ttu-id="3c169-178">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-178">Read-only</span></span><br/>  | <span data-ttu-id="3c169-179">取得已接收的封包數目。</span><span class="sxs-lookup"><span data-stu-id="3c169-179">Gets the number of packets received.</span></span><br/>                                              |
| [<span data-ttu-id="3c169-180">**receptionQuality**</span><span class="sxs-lookup"><span data-stu-id="3c169-180">**receptionQuality**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | <span data-ttu-id="3c169-181">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-181">Read-only</span></span><br/>  | <span data-ttu-id="3c169-182">取得過去30秒內未遺失的封包百分比。</span><span class="sxs-lookup"><span data-stu-id="3c169-182">Gets the percentage of packets not lost in the last 30 seconds.</span></span><br/>                   |
| [<span data-ttu-id="3c169-183">**recoveredPackets**</span><span class="sxs-lookup"><span data-stu-id="3c169-183">**recoveredPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | <span data-ttu-id="3c169-184">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-184">Read-only</span></span><br/>  | <span data-ttu-id="3c169-185">取得已復原的封包數目。</span><span class="sxs-lookup"><span data-stu-id="3c169-185">Gets the number of recovered packets.</span></span><br/>                                             |
| [<span data-ttu-id="3c169-186">**sourceProtocol**</span><span class="sxs-lookup"><span data-stu-id="3c169-186">**sourceProtocol**</span></span>](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | <span data-ttu-id="3c169-187">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c169-187">Read-only</span></span><br/>  | <span data-ttu-id="3c169-188">取得用來接收資料的來源通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3c169-188">Gets the source protocol used to receive data.</span></span><br/>                                    |



 

<span data-ttu-id="3c169-189">使用下列屬性來取得 **IWMPNetwork** 介面。</span><span class="sxs-lookup"><span data-stu-id="3c169-189">Get an **IWMPNetwork** interface by using the following property.</span></span>



| <span data-ttu-id="3c169-190">Object</span><span class="sxs-lookup"><span data-stu-id="3c169-190">Object</span></span>                                                                   | <span data-ttu-id="3c169-191">屬性</span><span class="sxs-lookup"><span data-stu-id="3c169-191">Property</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="3c169-192">AxWindowsMediaPlayer 物件</span><span class="sxs-lookup"><span data-stu-id="3c169-192">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="3c169-193">**network**</span><span class="sxs-lookup"><span data-stu-id="3c169-193">**network**</span></span>](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="3c169-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c169-194">Requirements</span></span>



| <span data-ttu-id="3c169-195">需求</span><span class="sxs-lookup"><span data-stu-id="3c169-195">Requirement</span></span> | <span data-ttu-id="3c169-196">值</span><span class="sxs-lookup"><span data-stu-id="3c169-196">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c169-197">標頭</span><span class="sxs-lookup"><span data-stu-id="3c169-197">Header</span></span><br/> | <dl> <span data-ttu-id="3c169-198"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c169-198"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c169-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c169-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c169-200">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="3c169-200">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





