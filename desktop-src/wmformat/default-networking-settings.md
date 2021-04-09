---
title: 預設網路設定
description: 預設網路設定
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media Format SDK，預設網路設定
- Advanced Systems Format (ASF) ，預設網路設定
- ASF (Advanced Systems Format) ，預設網路設定
- Windows Media Format SDK，網路設定
- Advanced Systems Format (ASF) ，網路設定
- ASF (Advanced Systems Format) ，網路設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840808"
---
# <a name="default-networking-settings"></a><span data-ttu-id="f228d-109">預設網路設定</span><span class="sxs-lookup"><span data-stu-id="f228d-109">Default Networking Settings</span></span>

<span data-ttu-id="f228d-110">下表描述 Windows Media 格式 SDK （依介面分組）中網路參數的預設設定。</span><span class="sxs-lookup"><span data-stu-id="f228d-110">The following tables describe the default settings of the networking parameters in the Windows Media Format SDK, grouped by interface.</span></span>



| <span data-ttu-id="f228d-111">IWMReaderNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="f228d-111">IWMReaderNetworkConfig</span></span>                | <span data-ttu-id="f228d-112">預設設定</span><span class="sxs-lookup"><span data-stu-id="f228d-112">Default setting</span></span>              |
|---------------------------------------|------------------------------|
| <span data-ttu-id="f228d-113">緩衝時間</span><span class="sxs-lookup"><span data-stu-id="f228d-113">Buffering time</span></span>                        | <span data-ttu-id="f228d-114">5 秒</span><span class="sxs-lookup"><span data-stu-id="f228d-114">5 seconds</span></span>                    |
| <span data-ttu-id="f228d-115">UseFixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="f228d-115">UseFixedUDPPort</span></span>                       | <span data-ttu-id="f228d-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="f228d-116">FALSE</span></span>                        |
| <span data-ttu-id="f228d-117">FixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="f228d-117">FixedUDPPort</span></span>                          | <span data-ttu-id="f228d-118">0 (無效) </span><span class="sxs-lookup"><span data-stu-id="f228d-118">0 (not valid)</span></span>                |
| <span data-ttu-id="f228d-119">ProxySetting： HTTP</span><span class="sxs-lookup"><span data-stu-id="f228d-119">ProxySetting: HTTP</span></span>                    | <span data-ttu-id="f228d-120">WMT \_ PROXY \_ 設定 \_ 瀏覽器</span><span class="sxs-lookup"><span data-stu-id="f228d-120">WMT\_PROXY\_SETTING\_BROWSER</span></span> |
| <span data-ttu-id="f228d-121">ProxySetting： MMS</span><span class="sxs-lookup"><span data-stu-id="f228d-121">ProxySetting: MMS</span></span>                     | <span data-ttu-id="f228d-122">WMT \_ PROXY \_ 設定 \_ 無</span><span class="sxs-lookup"><span data-stu-id="f228d-122">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="f228d-123">ProxySetting： RTSP</span><span class="sxs-lookup"><span data-stu-id="f228d-123">ProxySetting: RTSP</span></span>                    | <span data-ttu-id="f228d-124">WMT \_ PROXY \_ 設定 \_ 無</span><span class="sxs-lookup"><span data-stu-id="f228d-124">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="f228d-125">ProxyHostName (HTTP、MMS、RTSP) </span><span class="sxs-lookup"><span data-stu-id="f228d-125">ProxyHostName (HTTP, MMS, RTSP)</span></span>       | <span data-ttu-id="f228d-126">""</span><span class="sxs-lookup"><span data-stu-id="f228d-126">""</span></span>                           |
| <span data-ttu-id="f228d-127">ProxyPort： HTTP</span><span class="sxs-lookup"><span data-stu-id="f228d-127">ProxyPort: HTTP</span></span>                       | <span data-ttu-id="f228d-128">80</span><span class="sxs-lookup"><span data-stu-id="f228d-128">80</span></span>                           |
| <span data-ttu-id="f228d-129">ProxyPort： MMS</span><span class="sxs-lookup"><span data-stu-id="f228d-129">ProxyPort: MMS</span></span>                        | <span data-ttu-id="f228d-130">1755</span><span class="sxs-lookup"><span data-stu-id="f228d-130">1755</span></span>                         |
| <span data-ttu-id="f228d-131">ProxtPort： RTSP</span><span class="sxs-lookup"><span data-stu-id="f228d-131">ProxtPort: RTSP</span></span>                       | <span data-ttu-id="f228d-132">554</span><span class="sxs-lookup"><span data-stu-id="f228d-132">554</span></span>                          |
| <span data-ttu-id="f228d-133">ProxyExceptionList (HTTP、MMS、RTSP) </span><span class="sxs-lookup"><span data-stu-id="f228d-133">ProxyExceptionList (HTTP, MMS, RTSP)</span></span>  | <span data-ttu-id="f228d-134">""</span><span class="sxs-lookup"><span data-stu-id="f228d-134">""</span></span>                           |
| <span data-ttu-id="f228d-135">ProxyBypassForLocal (HTTP、MMS、RTSP) </span><span class="sxs-lookup"><span data-stu-id="f228d-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span></span> | <span data-ttu-id="f228d-136">FALSE</span><span class="sxs-lookup"><span data-stu-id="f228d-136">FALSE</span></span>                        |
| <span data-ttu-id="f228d-137">ForceRerunAutoDetection</span><span class="sxs-lookup"><span data-stu-id="f228d-137">ForceRerunAutoDetection</span></span>               | <span data-ttu-id="f228d-138">FALSE</span><span class="sxs-lookup"><span data-stu-id="f228d-138">FALSE</span></span>                        |
| <span data-ttu-id="f228d-139">EnableMulticast</span><span class="sxs-lookup"><span data-stu-id="f228d-139">EnableMulticast</span></span>                       | <span data-ttu-id="f228d-140">true</span><span class="sxs-lookup"><span data-stu-id="f228d-140">TRUE</span></span>                         |
| <span data-ttu-id="f228d-141">Update</span><span class="sxs-lookup"><span data-stu-id="f228d-141">EnableHTTP</span></span>                            | <span data-ttu-id="f228d-142">true</span><span class="sxs-lookup"><span data-stu-id="f228d-142">TRUE</span></span>                         |
| <span data-ttu-id="f228d-143">EnableTCP</span><span class="sxs-lookup"><span data-stu-id="f228d-143">EnableTCP</span></span>                             | <span data-ttu-id="f228d-144">true</span><span class="sxs-lookup"><span data-stu-id="f228d-144">TRUE</span></span>                         |
| <span data-ttu-id="f228d-145">EnableUDP</span><span class="sxs-lookup"><span data-stu-id="f228d-145">EnableUDP</span></span>                             | <span data-ttu-id="f228d-146">true</span><span class="sxs-lookup"><span data-stu-id="f228d-146">TRUE</span></span>                         |
| <span data-ttu-id="f228d-147">連接頻寬</span><span class="sxs-lookup"><span data-stu-id="f228d-147">Connection Bandwidth</span></span>                  | <span data-ttu-id="f228d-148">0 (自動偵測) </span><span class="sxs-lookup"><span data-stu-id="f228d-148">0 (auto-detect)</span></span>              |



 



| <span data-ttu-id="f228d-149">IWMReaderNetworkConfig2</span><span class="sxs-lookup"><span data-stu-id="f228d-149">IWMReaderNetworkConfig2</span></span>        | <span data-ttu-id="f228d-150">預設設定</span><span class="sxs-lookup"><span data-stu-id="f228d-150">Default setting</span></span>        |
|--------------------------------|------------------------|
| <span data-ttu-id="f228d-151">加速串流持續時間</span><span class="sxs-lookup"><span data-stu-id="f228d-151">Accelerated streaming duration</span></span> | <span data-ttu-id="f228d-152">100000000 (10 秒) </span><span class="sxs-lookup"><span data-stu-id="f228d-152">100000000 (10 seconds)</span></span> |
| <span data-ttu-id="f228d-153">啟用內容快取</span><span class="sxs-lookup"><span data-stu-id="f228d-153">Enable content caching</span></span>         | <span data-ttu-id="f228d-154">true</span><span class="sxs-lookup"><span data-stu-id="f228d-154">TRUE</span></span>                   |
| <span data-ttu-id="f228d-155">啟用快速快取</span><span class="sxs-lookup"><span data-stu-id="f228d-155">Enable fast cache</span></span>              | <span data-ttu-id="f228d-156">true</span><span class="sxs-lookup"><span data-stu-id="f228d-156">TRUE</span></span>                   |
| <span data-ttu-id="f228d-157">啟用重新傳送</span><span class="sxs-lookup"><span data-stu-id="f228d-157">Enable resends</span></span>                 | <span data-ttu-id="f228d-158">true</span><span class="sxs-lookup"><span data-stu-id="f228d-158">TRUE</span></span>                   |
| <span data-ttu-id="f228d-159">啟用 content thinning</span><span class="sxs-lookup"><span data-stu-id="f228d-159">Enable content thinning</span></span>        | <span data-ttu-id="f228d-160">true</span><span class="sxs-lookup"><span data-stu-id="f228d-160">TRUE</span></span>                   |
| <span data-ttu-id="f228d-161">重新連線限制</span><span class="sxs-lookup"><span data-stu-id="f228d-161">Reconnect limit</span></span>                | <span data-ttu-id="f228d-162">25</span><span class="sxs-lookup"><span data-stu-id="f228d-162">25</span></span>                     |



 



| <span data-ttu-id="f228d-163">IWMWriterNetworkSink</span><span class="sxs-lookup"><span data-stu-id="f228d-163">IWMWriterNetworkSink</span></span> | <span data-ttu-id="f228d-164">預設設定</span><span class="sxs-lookup"><span data-stu-id="f228d-164">Default setting</span></span>         |
|----------------------|-------------------------|
| <span data-ttu-id="f228d-165">最大用戶端</span><span class="sxs-lookup"><span data-stu-id="f228d-165">Maximum clients</span></span>      | <span data-ttu-id="f228d-166">5</span><span class="sxs-lookup"><span data-stu-id="f228d-166">5</span></span>                       |
| <span data-ttu-id="f228d-167">網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="f228d-167">Network protocol</span></span>     | <span data-ttu-id="f228d-168">0 (WMT \_ PROTOCOL \_ HTTP) </span><span class="sxs-lookup"><span data-stu-id="f228d-168">0 (WMT\_PROTOCOL\_HTTP)</span></span> |
| <span data-ttu-id="f228d-169">主機 URL</span><span class="sxs-lookup"><span data-stu-id="f228d-169">Host URL</span></span>             | <span data-ttu-id="f228d-170">0 (無效) </span><span class="sxs-lookup"><span data-stu-id="f228d-170">0 (not valid)</span></span>           |



 



| <span data-ttu-id="f228d-171">IWMWriterAdvanced2</span><span class="sxs-lookup"><span data-stu-id="f228d-171">IWMWriterAdvanced2</span></span>  | <span data-ttu-id="f228d-172">預設設定</span><span class="sxs-lookup"><span data-stu-id="f228d-172">Default setting</span></span>             |
|---------------------|-----------------------------|
| <span data-ttu-id="f228d-173">封包大小上限</span><span class="sxs-lookup"><span data-stu-id="f228d-173">Maximum packet size</span></span> | <span data-ttu-id="f228d-174">1400</span><span class="sxs-lookup"><span data-stu-id="f228d-174">1400</span></span>                        |
| <span data-ttu-id="f228d-175">記錄用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="f228d-175">Log client ID</span></span>       | <span data-ttu-id="f228d-176">FALSE</span><span class="sxs-lookup"><span data-stu-id="f228d-176">FALSE</span></span>                       |
| <span data-ttu-id="f228d-177">播放模式</span><span class="sxs-lookup"><span data-stu-id="f228d-177">Play mode</span></span>           | <span data-ttu-id="f228d-178">WMT \_ 播放 \_ 模式的 \_ 自選</span><span class="sxs-lookup"><span data-stu-id="f228d-178">WMT\_PLAY\_MODE\_AUTOSELECT</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f228d-179">相關主題</span><span class="sxs-lookup"><span data-stu-id="f228d-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f228d-180">**執行網路功能**</span><span class="sxs-lookup"><span data-stu-id="f228d-180">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




