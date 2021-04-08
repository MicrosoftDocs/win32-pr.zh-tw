---
title: 防火牆埠登錄設定
description: 防火牆埠登錄設定
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player，防火牆埠登錄設定
- Windows Media Player，埠登錄設定
- Windows Media Player，登錄
- 登錄，防火牆通訊埠設定
- 登錄，埠設定
- 登錄，Windows Media Player 的設定
- 防火牆埠登錄設定
- 埠登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839448"
---
# <a name="firewall-port-registry-settings"></a><span data-ttu-id="5b50e-111">防火牆埠登錄設定</span><span class="sxs-lookup"><span data-stu-id="5b50e-111">Firewall Port Registry Settings</span></span>

<span data-ttu-id="5b50e-112">Windows Media Player 將專案放在登錄中，讓防火牆可以決定是否要開啟或關閉媒體媒體櫃共用所使用的埠。</span><span class="sxs-lookup"><span data-stu-id="5b50e-112">Windows Media Player places entries in the registry so that firewalls can determine whether to open or close the ports that are used by media library sharing.</span></span>

<span data-ttu-id="5b50e-113">**AcceptedEULA 登錄專案**</span><span class="sxs-lookup"><span data-stu-id="5b50e-113">**AcceptedEULA Registry Entry**</span></span>

<span data-ttu-id="5b50e-114">Windows Media Player 使用下列登錄專案，指出使用者是否已接受使用者授權合約 (EULA) 。</span><span class="sxs-lookup"><span data-stu-id="5b50e-114">Windows Media Player uses the following registry entry to indicate whether the user has accepted the end user license agreement (EULA).</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



<span data-ttu-id="5b50e-115">值為1時，表示使用者已接受授權合約。</span><span class="sxs-lookup"><span data-stu-id="5b50e-115">A value of 1 indicates that the user has accepted the license agreement.</span></span> <span data-ttu-id="5b50e-116">值為0表示使用者尚未接受授權合約。</span><span class="sxs-lookup"><span data-stu-id="5b50e-116">A value of 0 indicates that the user has not accepted the license agreement.</span></span>

<span data-ttu-id="5b50e-117">**WMPNSSFirewallPortsOpen 登錄專案**</span><span class="sxs-lookup"><span data-stu-id="5b50e-117">**WMPNSSFirewallPortsOpen Registry Entry**</span></span>

<span data-ttu-id="5b50e-118">Windows Media Player 使用下列登錄專案，指出使用者是否已選擇與家用網路上的其他電腦共用其媒體媒體櫃。</span><span class="sxs-lookup"><span data-stu-id="5b50e-118">Windows Media Player uses the following registry entry to indicate whether the user has chosen to share his or her media library with other computers on a home network.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



<span data-ttu-id="5b50e-119">值為1時，表示使用者已選擇要共用程式庫。</span><span class="sxs-lookup"><span data-stu-id="5b50e-119">A value of 1 indicates that the user has chosen to share the library.</span></span> <span data-ttu-id="5b50e-120">值為0表示使用者已選擇不共用程式庫。</span><span class="sxs-lookup"><span data-stu-id="5b50e-120">A value of 0 indicates that the user has chosen not to share the library.</span></span>

<span data-ttu-id="5b50e-121">**與媒體媒體櫃共用相關的埠**</span><span class="sxs-lookup"><span data-stu-id="5b50e-121">**Ports Related to Media Library Sharing**</span></span>

<span data-ttu-id="5b50e-122">在 Windows Vista 上，如果 **WMPNSSFirewallPortsOpen** 登錄專案的值為1，則應該開啟下列埠。</span><span class="sxs-lookup"><span data-stu-id="5b50e-122">On Windows Vista, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="5b50e-123">連接埠</span><span class="sxs-lookup"><span data-stu-id="5b50e-123">Port</span></span>          | <span data-ttu-id="5b50e-124">通訊協定</span><span class="sxs-lookup"><span data-stu-id="5b50e-124">Protocol</span></span>                  | <span data-ttu-id="5b50e-125">處理序</span><span class="sxs-lookup"><span data-stu-id="5b50e-125">Process</span></span>                         | <span data-ttu-id="5b50e-126">方向</span><span class="sxs-lookup"><span data-stu-id="5b50e-126">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="5b50e-127">554</span><span class="sxs-lookup"><span data-stu-id="5b50e-127">554</span></span>           | <span data-ttu-id="5b50e-128">TCP RTSP</span><span class="sxs-lookup"><span data-stu-id="5b50e-128">TCP RTSP</span></span>                  | <span data-ttu-id="5b50e-129">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="5b50e-129">wmpnetwk.exe</span></span>                    | <span data-ttu-id="5b50e-130">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-130">inbound and outbound</span></span> |
| <span data-ttu-id="5b50e-131">8554-8558</span><span class="sxs-lookup"><span data-stu-id="5b50e-131">8554 - 8558</span></span>   | <span data-ttu-id="5b50e-132">TCP RTSP</span><span class="sxs-lookup"><span data-stu-id="5b50e-132">TCP RTSP</span></span>                  | <span data-ttu-id="5b50e-133">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="5b50e-133">wmpnetwk.exe</span></span>                    | <span data-ttu-id="5b50e-134">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-134">inbound and outbound</span></span> |
| <span data-ttu-id="5b50e-135">5004、5005</span><span class="sxs-lookup"><span data-stu-id="5b50e-135">5004, 5005</span></span>    | <span data-ttu-id="5b50e-136">UDP RTCP/RTP</span><span class="sxs-lookup"><span data-stu-id="5b50e-136">UDP RTCP/RTP</span></span>              | <span data-ttu-id="5b50e-137">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="5b50e-137">wmpnetwk.exe</span></span>                    | <span data-ttu-id="5b50e-138">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-138">inbound and outbound</span></span> |
| <span data-ttu-id="5b50e-139">50004-50013</span><span class="sxs-lookup"><span data-stu-id="5b50e-139">50004 - 50013</span></span> | <span data-ttu-id="5b50e-140">UDP RTCP/RTP</span><span class="sxs-lookup"><span data-stu-id="5b50e-140">UDP RTCP/RTP</span></span>              | <span data-ttu-id="5b50e-141">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="5b50e-141">wmpnetwk.exe</span></span>                    | <span data-ttu-id="5b50e-142">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-142">inbound and outbound</span></span> |
| <span data-ttu-id="5b50e-143">1900</span><span class="sxs-lookup"><span data-stu-id="5b50e-143">1900</span></span>          | <span data-ttu-id="5b50e-144">UDP SSDP</span><span class="sxs-lookup"><span data-stu-id="5b50e-144">UDP SSDP</span></span>                  | <span data-ttu-id="5b50e-145">svchost.exe 中的 SSDPsrv</span><span class="sxs-lookup"><span data-stu-id="5b50e-145">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="5b50e-146">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-146">inbound and outbound</span></span> |
| <span data-ttu-id="5b50e-147">2869</span><span class="sxs-lookup"><span data-stu-id="5b50e-147">2869</span></span>          | <span data-ttu-id="5b50e-148">TCP SSDP、UPnP</span><span class="sxs-lookup"><span data-stu-id="5b50e-148">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="5b50e-149">svchost.exe 中的 SSDPsrv/UPnPHost</span><span class="sxs-lookup"><span data-stu-id="5b50e-149">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="5b50e-150">進入</span><span class="sxs-lookup"><span data-stu-id="5b50e-150">inbound</span></span>              |
| <span data-ttu-id="5b50e-151">10280-10284</span><span class="sxs-lookup"><span data-stu-id="5b50e-151">10280 - 10284</span></span> | <span data-ttu-id="5b50e-152">UDP WMDRM-ND 註冊</span><span class="sxs-lookup"><span data-stu-id="5b50e-152">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="5b50e-153">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="5b50e-153">wmpnetwk.exe</span></span>                    | <span data-ttu-id="5b50e-154">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-154">inbound and outbound</span></span> |
| <span data-ttu-id="5b50e-155">10243</span><span class="sxs-lookup"><span data-stu-id="5b50e-155">10243</span></span>         | <span data-ttu-id="5b50e-156">TCP HTTP</span><span class="sxs-lookup"><span data-stu-id="5b50e-156">TCP HTTP</span></span>                  | <span data-ttu-id="5b50e-157">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="5b50e-157">wmpnetwk.exe</span></span>                    | <span data-ttu-id="5b50e-158">進入</span><span class="sxs-lookup"><span data-stu-id="5b50e-158">inbound</span></span>              |
| <span data-ttu-id="5b50e-159">2177</span><span class="sxs-lookup"><span data-stu-id="5b50e-159">2177</span></span>          | <span data-ttu-id="5b50e-160">TCP UDP qWAVE</span><span class="sxs-lookup"><span data-stu-id="5b50e-160">TCP UDP qWAVE</span></span>             | <span data-ttu-id="5b50e-161">svchost.exe</span><span class="sxs-lookup"><span data-stu-id="5b50e-161">svchost.exe</span></span>                     | <span data-ttu-id="5b50e-162">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-162">inbound and outbound</span></span> |



 

<span data-ttu-id="5b50e-163">在 Windows Vista 上，如果 **AcceptedEULA** 登錄專案的值為1，則應該開啟下列埠。</span><span class="sxs-lookup"><span data-stu-id="5b50e-163">On Windows Vista, if the **AcceptedEULA** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="5b50e-164">連接埠</span><span class="sxs-lookup"><span data-stu-id="5b50e-164">Port</span></span>          | <span data-ttu-id="5b50e-165">通訊協定</span><span class="sxs-lookup"><span data-stu-id="5b50e-165">Protocol</span></span>       | <span data-ttu-id="5b50e-166">處理序</span><span class="sxs-lookup"><span data-stu-id="5b50e-166">Process</span></span>                         | <span data-ttu-id="5b50e-167">方向</span><span class="sxs-lookup"><span data-stu-id="5b50e-167">Direction</span></span>            |
|---------------|----------------|---------------------------------|----------------------|
| <span data-ttu-id="5b50e-168">所有 UDP 埠</span><span class="sxs-lookup"><span data-stu-id="5b50e-168">All UDP ports</span></span> | <span data-ttu-id="5b50e-169">UDP RTP、MSB</span><span class="sxs-lookup"><span data-stu-id="5b50e-169">UDP RTP, MSB</span></span>   | <span data-ttu-id="5b50e-170">wmplayer.exe，任何子網</span><span class="sxs-lookup"><span data-stu-id="5b50e-170">wmplayer.exe, any subnet</span></span>        | <span data-ttu-id="5b50e-171">進入</span><span class="sxs-lookup"><span data-stu-id="5b50e-171">inbound</span></span>              |
| <span data-ttu-id="5b50e-172">1900</span><span class="sxs-lookup"><span data-stu-id="5b50e-172">1900</span></span>          | <span data-ttu-id="5b50e-173">UDP SSDP</span><span class="sxs-lookup"><span data-stu-id="5b50e-173">UDP SSDP</span></span>       | <span data-ttu-id="5b50e-174">svchost.exe 中的 SSDPsrv/UPnPHost</span><span class="sxs-lookup"><span data-stu-id="5b50e-174">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="5b50e-175">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-175">inbound and outbound</span></span> |
| <span data-ttu-id="5b50e-176">2869</span><span class="sxs-lookup"><span data-stu-id="5b50e-176">2869</span></span>          | <span data-ttu-id="5b50e-177">TCP SSDP、UPnP</span><span class="sxs-lookup"><span data-stu-id="5b50e-177">TCP SSDP, UPnP</span></span> | <span data-ttu-id="5b50e-178">SSDPsrv，UPnPHost</span><span class="sxs-lookup"><span data-stu-id="5b50e-178">SSDPsrv, UPnPHost</span></span>               | <span data-ttu-id="5b50e-179">進入</span><span class="sxs-lookup"><span data-stu-id="5b50e-179">inbound</span></span>              |



 

<span data-ttu-id="5b50e-180">在 Microsoft Windows XP 上，如果 **WMPNSSFirewallPortsOpen** 登錄專案的值為1，則應該開啟下列埠。</span><span class="sxs-lookup"><span data-stu-id="5b50e-180">On Microsoft Windows XP, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="5b50e-181">連接埠</span><span class="sxs-lookup"><span data-stu-id="5b50e-181">Port</span></span>          | <span data-ttu-id="5b50e-182">通訊協定</span><span class="sxs-lookup"><span data-stu-id="5b50e-182">Protocol</span></span>                  | <span data-ttu-id="5b50e-183">處理序</span><span class="sxs-lookup"><span data-stu-id="5b50e-183">Process</span></span>                         | <span data-ttu-id="5b50e-184">方向</span><span class="sxs-lookup"><span data-stu-id="5b50e-184">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="5b50e-185">1900</span><span class="sxs-lookup"><span data-stu-id="5b50e-185">1900</span></span>          | <span data-ttu-id="5b50e-186">UDP SSDP</span><span class="sxs-lookup"><span data-stu-id="5b50e-186">UDP SSDP</span></span>                  | <span data-ttu-id="5b50e-187">svchost.exe 中的 SSDPsrv</span><span class="sxs-lookup"><span data-stu-id="5b50e-187">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="5b50e-188">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-188">inbound and outbound</span></span> |
| <span data-ttu-id="5b50e-189">2869</span><span class="sxs-lookup"><span data-stu-id="5b50e-189">2869</span></span>          | <span data-ttu-id="5b50e-190">TCP SSDP、UPnP</span><span class="sxs-lookup"><span data-stu-id="5b50e-190">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="5b50e-191">svchost.exe 中的 SSDPsrv/UPnPHost</span><span class="sxs-lookup"><span data-stu-id="5b50e-191">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="5b50e-192">進入</span><span class="sxs-lookup"><span data-stu-id="5b50e-192">inbound</span></span>              |
| <span data-ttu-id="5b50e-193">10280-10284</span><span class="sxs-lookup"><span data-stu-id="5b50e-193">10280 - 10284</span></span> | <span data-ttu-id="5b50e-194">UDP WMDRM-ND 註冊</span><span class="sxs-lookup"><span data-stu-id="5b50e-194">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="5b50e-195">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="5b50e-195">wmpnetwk.exe</span></span>                    | <span data-ttu-id="5b50e-196">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5b50e-196">inbound and outbound</span></span> |
| <span data-ttu-id="5b50e-197">10243</span><span class="sxs-lookup"><span data-stu-id="5b50e-197">10243</span></span>         | <span data-ttu-id="5b50e-198">TCP HTTP</span><span class="sxs-lookup"><span data-stu-id="5b50e-198">TCP HTTP</span></span>                  | <span data-ttu-id="5b50e-199">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="5b50e-199">wmpnetwk.exe</span></span>                    | <span data-ttu-id="5b50e-200">進入</span><span class="sxs-lookup"><span data-stu-id="5b50e-200">inbound</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="5b50e-201">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b50e-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b50e-202">**登錄設定**</span><span class="sxs-lookup"><span data-stu-id="5b50e-202">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




