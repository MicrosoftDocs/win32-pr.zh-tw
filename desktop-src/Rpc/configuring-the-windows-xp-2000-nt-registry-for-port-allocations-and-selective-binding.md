---
title: 設定用於埠配置和選擇性系結的登錄
description: 從 Windows 2000 開始，Windows 資源套件中稱為 Rpccfg.exe 的公用程式應該用來設定系結。 如需詳細資訊，請參閱 Windows 資源套件以取得適當的作業系統版本。
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- 遠端程序呼叫 RPC、工作、設定埠配置和選擇性系結的登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef1749fab1beb8e637d208a7d7af64577066fe6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103933690"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a><span data-ttu-id="10e26-105">設定用於埠配置和選擇性系結的登錄</span><span class="sxs-lookup"><span data-stu-id="10e26-105">Configuring the Registry for Port Allocations and Selective Binding</span></span>

<span data-ttu-id="10e26-106">從 Windows 2000 開始，Windows 資源套件中稱為 Rpccfg.exe 的公用程式應該用來設定系結。</span><span class="sxs-lookup"><span data-stu-id="10e26-106">Starting with Windows 2000, a utility in the Windows Resource Kit called Rpccfg.exe should be used to set bindings.</span></span> <span data-ttu-id="10e26-107">如需詳細資訊，請參閱 Windows 資源套件以取得適當的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="10e26-107">For more information, consult the Windows Resource Kit for the appropriate operating system version.</span></span>

<span data-ttu-id="10e26-108">在 Windows 2000 之前的 windows 版本中，下表中的登錄機碼會指定動態埠配置的系統預設值，以及在多重主目錄電腦上系結至 Nic 的系統預設值。</span><span class="sxs-lookup"><span data-stu-id="10e26-108">For versions of windows prior to Windows 2000, the registry keys in the following table specify the system defaults for dynamic port allocation and for binding to NICs on multihomed computers.</span></span> <span data-ttu-id="10e26-109">您必須先建立這些金鑰，然後指定適當的設定。</span><span class="sxs-lookup"><span data-stu-id="10e26-109">You must first create these keys and then specify the appropriate settings.</span></span>

<span data-ttu-id="10e26-110">使用 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) 函數會影響這些設定。</span><span class="sxs-lookup"><span data-stu-id="10e26-110">Using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function affects these settings.</span></span> <span data-ttu-id="10e26-111">開發人員應該熟悉本節中說明的登錄設定，以及管理埠配置時的 **RpcServerUseProtseqEx** 函式。</span><span class="sxs-lookup"><span data-stu-id="10e26-111">Developers should be familiar with the registry settings explained in this section and the **RpcServerUseProtseqEx** function when managing port allocations.</span></span> <span data-ttu-id="10e26-112">如下表所示，其中包含三個假設性應用程式的範例，並說明這些設定和 **RpcServerUseProtseqEx** 函式如何相交互操作。</span><span class="sxs-lookup"><span data-stu-id="10e26-112">An example with three hypothetical applications follows the table below, and illustrates how these settings and the **RpcServerUseProtseqEx** function interoperate.</span></span>

<span data-ttu-id="10e26-113">如果遺失索引鍵或其包含不正確值，則會將整個設定標示為無效，而透過 [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)或 [**Ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp)的所有 **RpcServerUseProtseq \*** 呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="10e26-113">If a key is missing or if it contains an invalid value, the entire configuration is marked as invalid, and all **RpcServerUseProtseq\*** calls over [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) or [**ncadg\_ip\_udp**](/windows/desktop/Midl/ncadg-ip-udp) will fail.</span></span>

> [!Note]  
> <span data-ttu-id="10e26-114">配置給處理常式的埠會保持配置，直到該進程無法使用為止。</span><span class="sxs-lookup"><span data-stu-id="10e26-114">Ports allocated to a process remain allocated until that process dies.</span></span> <span data-ttu-id="10e26-115">如果所有可用的埠都在使用中，此函式會傳回 RPC \_ \_ \_ 的 \_ 資源不足。</span><span class="sxs-lookup"><span data-stu-id="10e26-115">If all available ports are in use, the function returns RPC\_S\_OUT\_OF\_RESOURCES.</span></span>

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10e26-116">埠金鑰</span><span class="sxs-lookup"><span data-stu-id="10e26-116">Port key</span></span></th>
<th><span data-ttu-id="10e26-117">資料類型</span><span class="sxs-lookup"><span data-stu-id="10e26-117">Data type</span></span></th>
<th><span data-ttu-id="10e26-118">描述</span><span class="sxs-lookup"><span data-stu-id="10e26-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><span data-ttu-id="10e26-119"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="10e26-119"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="10e26-120">指定一組 IP 埠範圍，其中包括可從網際網路取得的所有埠，或網際網路上所有無法使用的埠。</span><span class="sxs-lookup"><span data-stu-id="10e26-120">Specifies a set of IP port ranges consisting of either all the ports available from the Internet or all the ports not available from the Internet.</span></span> <span data-ttu-id="10e26-121">每個字串都代表一個埠或一組內含的埠 (例如 1000-1050、1984) 。</span><span class="sxs-lookup"><span data-stu-id="10e26-121">Each string represents a single port or an inclusive set of ports (for example,1000-1050, 1984).</span></span> <span data-ttu-id="10e26-122">如果有任何專案超出範圍0至65535，或如果任何字串無法解讀，則 RPC 執行時間會將整個設定視為無效。</span><span class="sxs-lookup"><span data-stu-id="10e26-122">If any entries are outside the range 0 to 65535, or if any string cannot be interpreted, the RPC run time will treat the entire configuration as invalid.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><span data-ttu-id="10e26-123"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="10e26-123"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="10e26-124">Y 或 N (不區分大小寫) 。</span><span class="sxs-lookup"><span data-stu-id="10e26-124">Y or N (not case-sensitive).</span></span> <span data-ttu-id="10e26-125">如果是 Y，埠機碼中列出的埠就是該電腦上的所有網際網路可用埠。</span><span class="sxs-lookup"><span data-stu-id="10e26-125">If Y, the ports listed in the Ports key are all the Internet-available ports on that computer.</span></span> <span data-ttu-id="10e26-126">如果是 N，埠機碼中列出的埠就是所有無法使用網際網路的通訊埠。</span><span class="sxs-lookup"><span data-stu-id="10e26-126">If N, the ports listed in the Ports key are all those ports that are not Internet-available.</span></span></td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><span data-ttu-id="10e26-127"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="10e26-127"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="10e26-128">Y 或 N (不區分大小寫) 。</span><span class="sxs-lookup"><span data-stu-id="10e26-128">Y or N (not case-sensitive).</span></span> <span data-ttu-id="10e26-129">指定系統預設原則。</span><span class="sxs-lookup"><span data-stu-id="10e26-129">Specifies the system default policy.</span></span> <span data-ttu-id="10e26-130">如果是 Y，則使用預設值的處理常式會從一組網際網路可用埠指派埠，如上面所定義。</span><span class="sxs-lookup"><span data-stu-id="10e26-130">If Y, the processes using the default will be assigned ports from the set of Internet-available ports, as defined above.</span></span> <span data-ttu-id="10e26-131">如果是 N，則會從內部網路專用埠集合中指派埠給使用預設的處理常式。</span><span class="sxs-lookup"><span data-stu-id="10e26-131">If N, processes using the default will be assigned ports from the set of intranet-only ports.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><span data-ttu-id="10e26-132"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="10e26-132"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="10e26-133">列出預設要系結之所有 Nic 的裝置名稱 (例如 \Device\AMDPCN1) 。</span><span class="sxs-lookup"><span data-stu-id="10e26-133">Lists the device names of all the NICs on which to bind by default (for example, \Device\AMDPCN1).</span></span> <span data-ttu-id="10e26-134">如果機碼不存在，則伺服器會系結至所有 Nic。</span><span class="sxs-lookup"><span data-stu-id="10e26-134">If the key does not exist, the server will bind to all NICs.</span></span> <span data-ttu-id="10e26-135">如果機碼存在，除非 NICFlags 欄位設定為 RPC_C_BIND_TO_ALL_NICS，否則伺服器會系結至機碼中指定的 Nic。</span><span class="sxs-lookup"><span data-stu-id="10e26-135">If the key does exist, the server will bind to the NICs specified in the key, unless the NICFlags field is set to RPC_C_BIND_TO_ALL_NICS.</span></span> <span data-ttu-id="10e26-136">如果索引鍵的 () 值為 null，則會將設定 &quot; &quot; 標示為無效，而對<strong>RpcServerUseProtseq \*</strong>的所有呼叫會透過<a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a>或<a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a>將會失敗。</span><span class="sxs-lookup"><span data-stu-id="10e26-136">If the key has a null (&quot;&quot;) value, the configuration will be marked as invalid and all calls to <strong>RpcServerUseProtseq\*</strong> over <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> or <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> will fail.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="10e26-137">下表說明三個範例應用程式如何受到上表中定義的設定影響，以及如何使用 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) 函數套用的設定也會受到影響。</span><span class="sxs-lookup"><span data-stu-id="10e26-137">The following table illustrates how three sample applications are affected by the settings defined in the previous table, and how settings applied using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function are also affected.</span></span>

<span data-ttu-id="10e26-138">在此範例中，會考慮三個假設的應用程式：</span><span class="sxs-lookup"><span data-stu-id="10e26-138">In this example, three hypothetical applications are considered:</span></span>

-   <span data-ttu-id="10e26-139">InternetApp：此應用程式是為了公開到網際網路，並且 \_ \_ \_ \_ 在傳遞給 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)函式的 [**rpc \_ 原則**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)結構的 **EndpointFlags** 成員中，指定了 rpc C 使用網際網路埠。</span><span class="sxs-lookup"><span data-stu-id="10e26-139">InternetApp: This application is intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTERNET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="10e26-140">LocalApp：此應用程式不是為了公開到網際網路，並且 \_ \_ \_ \_ 在傳遞給 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)函式的 [**rpc \_ 原則**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)結構的 **EndpointFlags** 成員中，指定了 rpc C USE 內部網路埠。</span><span class="sxs-lookup"><span data-stu-id="10e26-140">LocalApp: This application is not intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTRANET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="10e26-141">Builder.defaultapp：此應用程式會在傳遞給 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)函式的 [**RPC \_ 原則**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)結構的 **EndpointFlags** 成員中指定零。</span><span class="sxs-lookup"><span data-stu-id="10e26-141">DefaultApp: This application specifies zero in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>

<span data-ttu-id="10e26-142">下表根據上表所說明的登錄專案中指定的值，說明這些設定的影響。</span><span class="sxs-lookup"><span data-stu-id="10e26-142">The following table explains the impact these settings have based on values specified in the registry entries explained in the previous table.</span></span> <span data-ttu-id="10e26-143">針對格式考慮，會指派下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="10e26-143">For formatting considerations, the following codes are assigned:</span></span>

<span data-ttu-id="10e26-144">PIA = PortsInternetAvailable 金鑰值</span><span class="sxs-lookup"><span data-stu-id="10e26-144">PIA = PortsInternetAvailable Key value</span></span>

<span data-ttu-id="10e26-145">UIP = UseInternetPorts 索引鍵值</span><span class="sxs-lookup"><span data-stu-id="10e26-145">UIP = UseInternetPorts Key value</span></span>

<span data-ttu-id="10e26-146">針對此範例，埠索引鍵的值為每個專案5000-5100。</span><span class="sxs-lookup"><span data-stu-id="10e26-146">The value of the Ports key, for sake of this example, is 5000-5100 for each entry.</span></span>



| <span data-ttu-id="10e26-147">應用程式</span><span class="sxs-lookup"><span data-stu-id="10e26-147">Application</span></span> | <span data-ttu-id="10e26-148">PIA</span><span class="sxs-lookup"><span data-stu-id="10e26-148">PIA</span></span> | <span data-ttu-id="10e26-149">UIP</span><span class="sxs-lookup"><span data-stu-id="10e26-149">UIP</span></span> | <span data-ttu-id="10e26-150">結果</span><span class="sxs-lookup"><span data-stu-id="10e26-150">Result</span></span>                                  |
|-------------|-----|-----|-----------------------------------------|
| <span data-ttu-id="10e26-151">InternetApp</span><span class="sxs-lookup"><span data-stu-id="10e26-151">InternetApp</span></span> | <span data-ttu-id="10e26-152">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-152">Y</span></span>   | <span data-ttu-id="10e26-153">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-153">Y</span></span>   | <span data-ttu-id="10e26-154">使用5000和5100之間的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-154">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="10e26-155">LocalApp</span><span class="sxs-lookup"><span data-stu-id="10e26-155">LocalApp</span></span>    | <span data-ttu-id="10e26-156">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-156">Y</span></span>   | <span data-ttu-id="10e26-157">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-157">Y</span></span>   | <span data-ttu-id="10e26-158">使用5000-5100 範圍之外的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-158">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="10e26-159">Builder.defaultapp</span><span class="sxs-lookup"><span data-stu-id="10e26-159">DefaultApp</span></span>  | <span data-ttu-id="10e26-160">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-160">Y</span></span>   | <span data-ttu-id="10e26-161">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-161">Y</span></span>   | <span data-ttu-id="10e26-162">使用5000和5100之間的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-162">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="10e26-163">InternetApp</span><span class="sxs-lookup"><span data-stu-id="10e26-163">InternetApp</span></span> | <span data-ttu-id="10e26-164">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-164">Y</span></span>   | <span data-ttu-id="10e26-165">N</span><span class="sxs-lookup"><span data-stu-id="10e26-165">N</span></span>   | <span data-ttu-id="10e26-166">使用5000和5100之間的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-166">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="10e26-167">LocalApp</span><span class="sxs-lookup"><span data-stu-id="10e26-167">LocalApp</span></span>    | <span data-ttu-id="10e26-168">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-168">Y</span></span>   | <span data-ttu-id="10e26-169">N</span><span class="sxs-lookup"><span data-stu-id="10e26-169">N</span></span>   | <span data-ttu-id="10e26-170">使用5000-5100 範圍之外的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-170">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="10e26-171">Builder.defaultapp</span><span class="sxs-lookup"><span data-stu-id="10e26-171">DefaultApp</span></span>  | <span data-ttu-id="10e26-172">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-172">Y</span></span>   | <span data-ttu-id="10e26-173">N</span><span class="sxs-lookup"><span data-stu-id="10e26-173">N</span></span>   | <span data-ttu-id="10e26-174">使用5000-5100 範圍之外的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-174">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="10e26-175">InternetApp</span><span class="sxs-lookup"><span data-stu-id="10e26-175">InternetApp</span></span> | <span data-ttu-id="10e26-176">N</span><span class="sxs-lookup"><span data-stu-id="10e26-176">N</span></span>   | <span data-ttu-id="10e26-177">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-177">Y</span></span>   | <span data-ttu-id="10e26-178">使用5000-5100 範圍之外的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-178">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="10e26-179">LocalApp</span><span class="sxs-lookup"><span data-stu-id="10e26-179">LocalApp</span></span>    | <span data-ttu-id="10e26-180">N</span><span class="sxs-lookup"><span data-stu-id="10e26-180">N</span></span>   | <span data-ttu-id="10e26-181">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-181">Y</span></span>   | <span data-ttu-id="10e26-182">使用5000和5100之間的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-182">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="10e26-183">Builder.defaultapp</span><span class="sxs-lookup"><span data-stu-id="10e26-183">DefaultApp</span></span>  | <span data-ttu-id="10e26-184">N</span><span class="sxs-lookup"><span data-stu-id="10e26-184">N</span></span>   | <span data-ttu-id="10e26-185">Y</span><span class="sxs-lookup"><span data-stu-id="10e26-185">Y</span></span>   | <span data-ttu-id="10e26-186">使用5000-5100 範圍之外的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-186">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="10e26-187">InternetApp</span><span class="sxs-lookup"><span data-stu-id="10e26-187">InternetApp</span></span> | <span data-ttu-id="10e26-188">N</span><span class="sxs-lookup"><span data-stu-id="10e26-188">N</span></span>   | <span data-ttu-id="10e26-189">N</span><span class="sxs-lookup"><span data-stu-id="10e26-189">N</span></span>   | <span data-ttu-id="10e26-190">使用5000-5100 範圍之外的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-190">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="10e26-191">LocalApp</span><span class="sxs-lookup"><span data-stu-id="10e26-191">LocalApp</span></span>    | <span data-ttu-id="10e26-192">N</span><span class="sxs-lookup"><span data-stu-id="10e26-192">N</span></span>   | <span data-ttu-id="10e26-193">N</span><span class="sxs-lookup"><span data-stu-id="10e26-193">N</span></span>   | <span data-ttu-id="10e26-194">使用5000和5100之間的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-194">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="10e26-195">Builder.defaultapp</span><span class="sxs-lookup"><span data-stu-id="10e26-195">DefaultApp</span></span>  | <span data-ttu-id="10e26-196">N</span><span class="sxs-lookup"><span data-stu-id="10e26-196">N</span></span>   | <span data-ttu-id="10e26-197">N</span><span class="sxs-lookup"><span data-stu-id="10e26-197">N</span></span>   | <span data-ttu-id="10e26-198">使用5000和5100之間的埠</span><span class="sxs-lookup"><span data-stu-id="10e26-198">Uses ports between 5000 and 5100</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="10e26-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="10e26-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10e26-200">**RPC \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="10e26-200">**RPC\_POLICY**</span></span>](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[<span data-ttu-id="10e26-201">**RpcServerUseAllProtseqsEx**</span><span class="sxs-lookup"><span data-stu-id="10e26-201">**RpcServerUseAllProtseqsEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[<span data-ttu-id="10e26-202">**RpcServerUseAllProtseqsIfEx**</span><span class="sxs-lookup"><span data-stu-id="10e26-202">**RpcServerUseAllProtseqsIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[<span data-ttu-id="10e26-203">**RpcServerUseProtseqEx**</span><span class="sxs-lookup"><span data-stu-id="10e26-203">**RpcServerUseProtseqEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[<span data-ttu-id="10e26-204">**RpcServerUseProtseqEpEx**</span><span class="sxs-lookup"><span data-stu-id="10e26-204">**RpcServerUseProtseqEpEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[<span data-ttu-id="10e26-205">**RpcServerUseProtseqIfEx**</span><span class="sxs-lookup"><span data-stu-id="10e26-205">**RpcServerUseProtseqIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[<span data-ttu-id="10e26-206">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="10e26-206">**ncacn\_ip\_tcp**</span></span>](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[<span data-ttu-id="10e26-207">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="10e26-207">**ncadg\_ip\_udp**</span></span>](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 