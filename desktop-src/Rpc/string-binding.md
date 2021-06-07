---
title: 字串系結
description: 字串系結是由字串組成的不帶正負號字元字串，代表系結物件 UUID、RPC 通訊協定序列、網路位址，以及端點和端點選項。
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b3f925c03c85be3c47ab174a85f31e72e40d828
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386977"
---
# <a name="string-binding"></a><span data-ttu-id="b4cf3-103">字串系結</span><span class="sxs-lookup"><span data-stu-id="b4cf3-103">String Binding</span></span>

<span data-ttu-id="b4cf3-104">字串系結是由字串組成的不帶正負號字元字串，代表系結物件 UUID、RPC 通訊協定序列、網路位址，以及端點和端點選項。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-104">The string binding is an unsigned character string composed of strings that represent the binding object UUID, the RPC protocol sequence, the network address, and the endpoint and endpoint options.</span></span>

<span data-ttu-id="b4cf3-105">*ObjectUUID* @*ProtocolSequence*：*networkaddress.cache.ttl* \[ *端點*，*選項*\]</span><span class="sxs-lookup"><span data-stu-id="b4cf3-105">*ObjectUUID*@*ProtocolSequence*:*NetworkAddress*\[*Endpoint*,*Option*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="b4cf3-106">參數</span><span class="sxs-lookup"><span data-stu-id="b4cf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4cf3-107"><span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*</span><span class="sxs-lookup"><span data-stu-id="b4cf3-107"><span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*</span></span>
</dt> <dd>

<span data-ttu-id="b4cf3-108">遠端程序呼叫所操作之物件的[UUID](/windows/desktop/Midl/uuid) 。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-108">[UUID](/windows/desktop/Midl/uuid) of the object operated on by the remote procedure call.</span></span> <span data-ttu-id="b4cf3-109">在伺服器上，RPC 執行時間程式庫會將物件類型對應至 () 函式指標陣列來叫用正確管理員常式的管理員進入點向量。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-109">At the server, the RPC run-time library maps the object type to a manager entry-point vector (an array of function pointers) to invoke the correct manager routine.</span></span> <span data-ttu-id="b4cf3-110">如需如何將物件 Uuid 對應至經理進入點向量的討論，請參閱 [註冊介面](registering-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-110">For a discussion of how to map object UUIDs to manager entry-point vectors, see [Registering Interfaces](registering-interfaces.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cf3-111"><span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*</span><span class="sxs-lookup"><span data-stu-id="b4cf3-111"><span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*</span></span>
</dt> <dd>

<span data-ttu-id="b4cf3-112">代表 RPC 通訊協定 (的有效組合的字元字串，例如 ncacn) 、傳輸通訊協定 (例如 TCP) ，以及網路通訊協定 (例如 IP) 。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-112">Character string that represents a valid combination of an RPC protocol (such as ncacn), a transport protocol (such as TCP), and a network protocol (such as IP).</span></span> <span data-ttu-id="b4cf3-113">Microsoft RPC 支援下列 [通訊協定順序常數](protocol-sequence-constants.md)中指定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-113">Microsoft RPC supports the following protocols specified in [Protocol Sequence Constants](protocol-sequence-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4cf3-114"><span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*Networkaddress.cache.ttl*</span><span class="sxs-lookup"><span data-stu-id="b4cf3-114"><span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*NetworkAddress*</span></span>
</dt> <dd>

<span data-ttu-id="b4cf3-115">接收遠端程序呼叫之系統的網路位址。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-115">Network address of the system to receive remote procedure calls.</span></span>

> [!Note]  
> <span data-ttu-id="b4cf3-116">Windows XP 不支援下列通訊協定順序：</span><span class="sxs-lookup"><span data-stu-id="b4cf3-116">The following protocol sequences are not supported as of Windows XP:</span></span>

 

-   [<span data-ttu-id="b4cf3-117">ncacn \_ nb \_ tcp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-117">ncacn\_nb\_tcp</span></span>](/windows/desktop/Midl/ncacn-nb-tcp)
-   [<span data-ttu-id="b4cf3-118">ncacn \_ nb \_ nb</span><span class="sxs-lookup"><span data-stu-id="b4cf3-118">ncacn\_nb\_nb</span></span>](/windows/desktop/Midl/ncacn-nb-nb)
-   [<span data-ttu-id="b4cf3-119">ncacn \_ nb \_ ipx</span><span class="sxs-lookup"><span data-stu-id="b4cf3-119">ncacn\_nb\_ipx</span></span>](/windows/desktop/Midl/ncacn-nb-ipx)
-   [<span data-ttu-id="b4cf3-120">ncacn \_ dnet \_ nsp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-120">ncacn\_dnet\_nsp</span></span>](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [<span data-ttu-id="b4cf3-121">ncacn \_ vns \_ spp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-121">ncacn\_vns\_spp</span></span>](/windows/desktop/Midl/ncacn-vns-spp)
-   [<span data-ttu-id="b4cf3-122">ncadg \_ mq</span><span class="sxs-lookup"><span data-stu-id="b4cf3-122">ncadg\_mq</span></span>](/windows/desktop/Midl/ncadg-mq)
-   [<span data-ttu-id="b4cf3-123">ncadg \_ ipx</span><span class="sxs-lookup"><span data-stu-id="b4cf3-123">ncadg\_ipx</span></span>](/windows/desktop/Midl/ncadg-ipx)

<span data-ttu-id="b4cf3-124">網路位址的格式和內容取決於指定的通訊協定順序，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-124">The format and content of the network address depend on the specified protocol sequence as follows.</span></span>



| <span data-ttu-id="b4cf3-125">通訊協定順序</span><span class="sxs-lookup"><span data-stu-id="b4cf3-125">Protocol sequence</span></span>                       | <span data-ttu-id="b4cf3-126">網路位址</span><span class="sxs-lookup"><span data-stu-id="b4cf3-126">Network address</span></span>                                                                                                                                  | <span data-ttu-id="b4cf3-127">範例</span><span class="sxs-lookup"><span data-stu-id="b4cf3-127">Examples</span></span>                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="b4cf3-128">ncacn \_ nb \_ tcp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-128">ncacn\_nb\_tcp</span></span>](/windows/desktop/Midl/ncacn-nb-tcp)     | <span data-ttu-id="b4cf3-129">電腦名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-129">Computer name</span></span>                                                                                                                                    | <span data-ttu-id="b4cf3-130">myserver</span><span class="sxs-lookup"><span data-stu-id="b4cf3-130">myserver</span></span>                                               |
| [<span data-ttu-id="b4cf3-131">ncacn \_ nb \_ ipx</span><span class="sxs-lookup"><span data-stu-id="b4cf3-131">ncacn\_nb\_ipx</span></span>](/windows/desktop/Midl/ncacn-nb-ipx)     | <span data-ttu-id="b4cf3-132">電腦名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-132">Computer name</span></span>                                                                                                                                    | <span data-ttu-id="b4cf3-133">myserver</span><span class="sxs-lookup"><span data-stu-id="b4cf3-133">myserver</span></span>                                               |
| [<span data-ttu-id="b4cf3-134">ncacn \_ nb \_ nb</span><span class="sxs-lookup"><span data-stu-id="b4cf3-134">ncacn\_nb\_nb</span></span>](/windows/desktop/Midl/ncacn-nb-nb)       | <span data-ttu-id="b4cf3-135">電腦名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-135">Computer name</span></span>                                                                                                                                    | <span data-ttu-id="b4cf3-136">myserver</span><span class="sxs-lookup"><span data-stu-id="b4cf3-136">myserver</span></span>                                               |
| [<span data-ttu-id="b4cf3-137">ncacn \_ ip \_ tcp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-137">ncacn\_ip\_tcp</span></span>](/windows/desktop/Midl/ncacn-ip-tcp)     | <span data-ttu-id="b4cf3-138">四個八位的網際網路位址或主機名稱。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-138">Four-octet Internet address, or host name.</span></span> <span data-ttu-id="b4cf3-139">如果已安裝 IPv6 網路堆疊，則會完全支援 IPv6，而且也會接受 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-139">If the IPv6 network stack is installed, IPv6 is fully supported and an IPv6 address is also accepted.</span></span> | <span data-ttu-id="b4cf3-140">128.10.2.30 anynode.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b4cf3-140">128.10.2.30 anynode.microsoft.com</span></span>                      |
| [<span data-ttu-id="b4cf3-141">ncacn \_ np</span><span class="sxs-lookup"><span data-stu-id="b4cf3-141">ncacn\_np</span></span>](/windows/desktop/Midl/ncacn-np)              | <span data-ttu-id="b4cf3-142">伺服器名稱 (前置雙反斜線是選擇性的) </span><span class="sxs-lookup"><span data-stu-id="b4cf3-142">Server name (leading double backslashes are optional)</span></span>                                                                                            | <span data-ttu-id="b4cf3-143">myserver \\ \\ myotherserver</span><span class="sxs-lookup"><span data-stu-id="b4cf3-143">myserver \\\\myotherserver</span></span>                             |
| [<span data-ttu-id="b4cf3-144">ncacn \_ spx</span><span class="sxs-lookup"><span data-stu-id="b4cf3-144">ncacn\_spx</span></span>](/windows/desktop/Midl/ncacn-spx)            | <span data-ttu-id="b4cf3-145">IPX 網際網路位址或伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-145">IPX Internet address, or server name</span></span>                                                                                                             | <span data-ttu-id="b4cf3-146">~ 0000000108002B30612C myserver</span><span class="sxs-lookup"><span data-stu-id="b4cf3-146">~0000000108002B30612C myserver</span></span>                         |
| [<span data-ttu-id="b4cf3-147">ncacn \_ dnet \_ nsp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-147">ncacn\_dnet\_nsp</span></span>](/windows/desktop/Midl/ncacn-dnet-nsp) | <span data-ttu-id="b4cf3-148">區域和節點語法</span><span class="sxs-lookup"><span data-stu-id="b4cf3-148">Area and node syntax</span></span>                                                                                                                             | <span data-ttu-id="b4cf3-149">4.120</span><span class="sxs-lookup"><span data-stu-id="b4cf3-149">4.120</span></span>                                                  |
| [<span data-ttu-id="b4cf3-150">\_在 \_ dsp ncacn</span><span class="sxs-lookup"><span data-stu-id="b4cf3-150">ncacn\_at\_dsp</span></span>](/windows/desktop/Midl/ncacn-at-dsp)     | <span data-ttu-id="b4cf3-151">電腦名稱稱，選擇性地接著 @ 和 AppleTalk 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-151">Computer name, optionally followed by @ and the AppleTalk zone name.</span></span> <span data-ttu-id="b4cf3-152">預設為 @ \* 、用戶端的區域（如果未提供任何區域）</span><span class="sxs-lookup"><span data-stu-id="b4cf3-152">Defaults to @\*, the client's zone, if no zone provided</span></span>                     | <span data-ttu-id="b4cf3-153">servername@zonename servername</span><span class="sxs-lookup"><span data-stu-id="b4cf3-153">servername@zonename servername</span></span>                         |
| [<span data-ttu-id="b4cf3-154">ncacn \_ vns \_ spp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-154">ncacn\_vns\_spp</span></span>](/windows/desktop/Midl/ncacn-vns-spp)   | <span data-ttu-id="b4cf3-155">表單的 StreetTalk 伺服器名稱 item@group@organization</span><span class="sxs-lookup"><span data-stu-id="b4cf3-155">StreetTalk server name of the form item@group@organization</span></span>                                                                                       | printserver@sdkdocs@microsoft                          |
| [<span data-ttu-id="b4cf3-156">ncadg \_ mq</span><span class="sxs-lookup"><span data-stu-id="b4cf3-156">ncadg\_mq</span></span>](/windows/desktop/Midl/ncadg-mq)              | <span data-ttu-id="b4cf3-157">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-157">Server name</span></span>                                                                                                                                      | <span data-ttu-id="b4cf3-158">myserver</span><span class="sxs-lookup"><span data-stu-id="b4cf3-158">myserver</span></span>                                               |
| [<span data-ttu-id="b4cf3-159">ncacn \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="b4cf3-159">ncacn\_http</span></span>](/windows/desktop/Midl/ncacn-http)          | <span data-ttu-id="b4cf3-160">網際網路位址 (四個八位或易記名稱，或本機伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-160">Internet address (either four-octet or friendly name, or local server name</span></span>                                                                       | <span data-ttu-id="b4cf3-161">128.10.2.30 somesvr@anywhere.com mylocalsvr</span><span class="sxs-lookup"><span data-stu-id="b4cf3-161">128.10.2.30 somesvr@anywhere.com mylocalsvr</span></span><br/> |
| [<span data-ttu-id="b4cf3-162">ncadg \_ ip \_ udp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-162">ncadg\_ip\_udp</span></span>](/windows/desktop/Midl/ncadg-ip-udp)     | <span data-ttu-id="b4cf3-163">四個八位的網際網路位址或主機名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-163">Four-octet Internet address, or host name</span></span>                                                                                                        | <span data-ttu-id="b4cf3-164">128.10.2.30 anynode.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b4cf3-164">128.10.2.30 anynode.microsoft.com</span></span>                      |
| [<span data-ttu-id="b4cf3-165">ncadg \_ ipx</span><span class="sxs-lookup"><span data-stu-id="b4cf3-165">ncadg\_ipx</span></span>](/windows/desktop/Midl/ncadg-ipx)            | <span data-ttu-id="b4cf3-166">IPX 網際網路位址或伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-166">IPX Internet address, or server name</span></span>                                                                                                             | <span data-ttu-id="b4cf3-167">~ 0000000108002B30612C myserver</span><span class="sxs-lookup"><span data-stu-id="b4cf3-167">~0000000108002B30612C myserver</span></span>                         |
| [<span data-ttu-id="b4cf3-168">ncalrpc</span><span class="sxs-lookup"><span data-stu-id="b4cf3-168">ncalrpc</span></span>](/windows/desktop/Midl/ncalrpc)                 | <span data-ttu-id="b4cf3-169">電腦名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-169">Machine name</span></span>                                                                                                                                     | <span data-ttu-id="b4cf3-170">thismachine</span><span class="sxs-lookup"><span data-stu-id="b4cf3-170">thismachine</span></span>                                            |



 

<span data-ttu-id="b4cf3-171">[網路位址] 欄位是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-171">The network-address field is optional.</span></span> <span data-ttu-id="b4cf3-172">當您未指定網路位址時，字串系結會參考您的本機主機。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-172">When you do not specify a network address, the string binding refers to your local host.</span></span> <span data-ttu-id="b4cf3-173">當您使用 **ncalrpc** 通訊協定順序時，可以指定本機電腦的名稱，不過這樣做完全不需要。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-173">It is possible to specify the name of the local computer when you use the **ncalrpc** protocol sequence, however doing so is completely unnecessary.</span></span>

</dd> <dt>

<span data-ttu-id="b4cf3-174"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*端點*</span><span class="sxs-lookup"><span data-stu-id="b4cf3-174"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Endpoint*</span></span>
</dt> <dd>

<span data-ttu-id="b4cf3-175">接收遠端程序呼叫之進程的端點或位址。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-175">Endpoint, or address, of the process to receive remote procedure calls.</span></span> <span data-ttu-id="b4cf3-176">端點之前可以有關鍵詞 **端點 =**。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-176">An endpoint can be preceded by the keyword **endpoint=**.</span></span> <span data-ttu-id="b4cf3-177">如果伺服器已向端點對應程式註冊其系結，則指定端點是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-177">Specifying the endpoint is optional if the server has registered its bindings with the endpoint mapper.</span></span> <span data-ttu-id="b4cf3-178">請參閱 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-178">See [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).</span></span>

<span data-ttu-id="b4cf3-179">端點的格式和內容取決於指定的通訊協定順序，如下列端點/選項表所示。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-179">The format and content of an endpoint depend on the specified protocol sequence as shown in the following Endpoint/Option Table.</span></span>

</dd> <dt>

<span data-ttu-id="b4cf3-180"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>*選項*</span><span class="sxs-lookup"><span data-stu-id="b4cf3-180"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Option*</span></span>
</dt> <dd>

<span data-ttu-id="b4cf3-181">通訊協定特定的選項。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-181">Protocol-specific options.</span></span> <span data-ttu-id="b4cf3-182">選項欄位不是必要的。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-182">The option field is not required.</span></span> <span data-ttu-id="b4cf3-183">每個選項都是由使用語法 *選項名稱* = *選項值* 的 {name，value} 配對所指定。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-183">Each option is specified by a {name, value} pair that uses the syntax *option name*=*option value*.</span></span> <span data-ttu-id="b4cf3-184">系統會為每個通訊協定序列定義選項，如下列端點/選項表格所示。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-184">Options are defined for each protocol sequence as shown in the following Endpoint/Option table.</span></span>



| <span data-ttu-id="b4cf3-185">通訊協定順序</span><span class="sxs-lookup"><span data-stu-id="b4cf3-185">Protocol sequence</span></span>                       | <span data-ttu-id="b4cf3-186">端點</span><span class="sxs-lookup"><span data-stu-id="b4cf3-186">Endpoint</span></span>                                                                                           | <span data-ttu-id="b4cf3-187">範例</span><span class="sxs-lookup"><span data-stu-id="b4cf3-187">Examples</span></span>             | <span data-ttu-id="b4cf3-188">選項名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-188">Option name</span></span>                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [<span data-ttu-id="b4cf3-189">ncacn \_ nb \_ tcp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-189">ncacn\_nb\_tcp</span></span>](/windows/desktop/Midl/ncacn-nb-tcp)     | <span data-ttu-id="b4cf3-190">介於1到254之間的整數。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-190">Integer between 1 and 254.</span></span> <span data-ttu-id="b4cf3-191">0和32之間的許多值都是由 Microsoft 所保留。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-191">Many values between 0 and 32 are reserved by Microsoft.</span></span>                 | <span data-ttu-id="b4cf3-192">100</span><span class="sxs-lookup"><span data-stu-id="b4cf3-192">100</span></span>                  | <span data-ttu-id="b4cf3-193">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-193">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-194">ncacn \_ nb \_ ipx</span><span class="sxs-lookup"><span data-stu-id="b4cf3-194">ncacn\_nb\_ipx</span></span>](/windows/desktop/Midl/ncacn-nb-ipx)     | <span data-ttu-id="b4cf3-195"> (如上所示) </span><span class="sxs-lookup"><span data-stu-id="b4cf3-195">(as above)</span></span>                                                                                         | <span data-ttu-id="b4cf3-196"> (如上所示) </span><span class="sxs-lookup"><span data-stu-id="b4cf3-196">(as above)</span></span>           | <span data-ttu-id="b4cf3-197">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-197">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-198">ncacn \_ nb \_ nb</span><span class="sxs-lookup"><span data-stu-id="b4cf3-198">ncacn\_nb\_nb</span></span>](/windows/desktop/Midl/ncacn-nb-nb)       | <span data-ttu-id="b4cf3-199"> (如上所示) </span><span class="sxs-lookup"><span data-stu-id="b4cf3-199">(as above)</span></span>                                                                                         | <span data-ttu-id="b4cf3-200"> (如上所示) </span><span class="sxs-lookup"><span data-stu-id="b4cf3-200">(as above)</span></span>           | <span data-ttu-id="b4cf3-201">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-201">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-202">ncacn \_ ip \_ tcp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-202">ncacn\_ip\_tcp</span></span>](/windows/desktop/Midl/ncacn-ip-tcp)     | <span data-ttu-id="b4cf3-203">網際網路埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-203">Internet port number.</span></span>                                                                              | <span data-ttu-id="b4cf3-204">1025</span><span class="sxs-lookup"><span data-stu-id="b4cf3-204">1025</span></span>                 | <span data-ttu-id="b4cf3-205">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-205">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-206">ncacn \_ np</span><span class="sxs-lookup"><span data-stu-id="b4cf3-206">ncacn\_np</span></span>](/windows/desktop/Midl/ncacn-np)              | <span data-ttu-id="b4cf3-207">具名管道。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-207">Named pipe.</span></span> <span data-ttu-id="b4cf3-208">名稱必須以 " \\ \\ pipe" 開頭。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-208">Name must start with "\\\\pipe".</span></span>                                                       | <span data-ttu-id="b4cf3-209">\\\\管道 \\ \\ pipename</span><span class="sxs-lookup"><span data-stu-id="b4cf3-209">\\\\pipe\\\\pipename</span></span> | <span data-ttu-id="b4cf3-210">安全性</span><span class="sxs-lookup"><span data-stu-id="b4cf3-210">Security</span></span>                                               |
| [<span data-ttu-id="b4cf3-211">ncacn \_ spx</span><span class="sxs-lookup"><span data-stu-id="b4cf3-211">ncacn\_spx</span></span>](/windows/desktop/Midl/ncacn-spx)            | <span data-ttu-id="b4cf3-212">介於1到65535之間的整數。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-212">Integer between 1 and 65535.</span></span>                                                                       | <span data-ttu-id="b4cf3-213">5000</span><span class="sxs-lookup"><span data-stu-id="b4cf3-213">5000</span></span>                 | <span data-ttu-id="b4cf3-214">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-214">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-215">ncacn \_ dnet \_ nsp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-215">ncacn\_dnet\_nsp</span></span>](/windows/desktop/Midl/ncacn-dnet-nsp) | <span data-ttu-id="b4cf3-216">DECnet 階段 IV 物件編號 (前面必須加 \# 上字元) 或物件名稱。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-216">DECnet phase IV object number (must be preceded by the \# character), or object name.</span></span>              | <span data-ttu-id="b4cf3-217">mailserver \# 17</span><span class="sxs-lookup"><span data-stu-id="b4cf3-217">mailserver \#17</span></span>      | <span data-ttu-id="b4cf3-218">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-218">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-219">\_在 \_ dsp ncacn</span><span class="sxs-lookup"><span data-stu-id="b4cf3-219">ncacn\_at\_dsp</span></span>](/windows/desktop/Midl/ncacn-at-dsp)     | <span data-ttu-id="b4cf3-220">字元字串，長度最多為22個位元組。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-220">A character string, up to 22 bytes long.</span></span>                                                           | <span data-ttu-id="b4cf3-221">myservicesendpoint</span><span class="sxs-lookup"><span data-stu-id="b4cf3-221">myservicesendpoint</span></span>   | <span data-ttu-id="b4cf3-222">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-222">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-223">ncacn \_ vns \_ spp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-223">ncacn\_vns\_spp</span></span>](/windows/desktop/Midl/ncacn-vns-spp)   | <span data-ttu-id="b4cf3-224">Vines 在250到511之間的 SPP 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-224">Vines SPP port number between 250 and 511.</span></span>                                                         | <span data-ttu-id="b4cf3-225">500</span><span class="sxs-lookup"><span data-stu-id="b4cf3-225">500</span></span>                  | <span data-ttu-id="b4cf3-226">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-226">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-227">ncadg \_ mq</span><span class="sxs-lookup"><span data-stu-id="b4cf3-227">ncadg\_mq</span></span>](/windows/desktop/Midl/ncadg-mq)              | <span data-ttu-id="b4cf3-228">介於1到65535之間的整數。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-228">Integer between 1 and 65535.</span></span>                                                                       | <span data-ttu-id="b4cf3-229">5000</span><span class="sxs-lookup"><span data-stu-id="b4cf3-229">5000</span></span>                 | <span data-ttu-id="b4cf3-230">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-230">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-231">ncacn \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="b4cf3-231">ncacn\_http</span></span>](/windows/desktop/Midl/ncacn-http)          | <span data-ttu-id="b4cf3-232">網際網路埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-232">Internet port number.</span></span>                                                                              | <span data-ttu-id="b4cf3-233">2215</span><span class="sxs-lookup"><span data-stu-id="b4cf3-233">2215</span></span>                 | <span data-ttu-id="b4cf3-234">HTTP 和 RPC proxy 伺服器名稱，HttpConnection 選項</span><span class="sxs-lookup"><span data-stu-id="b4cf3-234">HTTP and RPC proxy server names, HttpConnection option</span></span> |
| [<span data-ttu-id="b4cf3-235">ncadg \_ ip \_ udp</span><span class="sxs-lookup"><span data-stu-id="b4cf3-235">ncadg\_ip\_udp</span></span>](/windows/desktop/Midl/ncadg-ip-udp)     | <span data-ttu-id="b4cf3-236">網際網路埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-236">Internet port number.</span></span>                                                                              | <span data-ttu-id="b4cf3-237">1025</span><span class="sxs-lookup"><span data-stu-id="b4cf3-237">1025</span></span>                 | <span data-ttu-id="b4cf3-238">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-238">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-239">ncadg \_ ipx</span><span class="sxs-lookup"><span data-stu-id="b4cf3-239">ncadg\_ipx</span></span>](/windows/desktop/Midl/ncadg-ipx)            | <span data-ttu-id="b4cf3-240">介於1到65535之間的整數。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-240">Integer between 1 and 65535.</span></span>                                                                       | <span data-ttu-id="b4cf3-241">5000</span><span class="sxs-lookup"><span data-stu-id="b4cf3-241">5000</span></span>                 | <span data-ttu-id="b4cf3-242">無</span><span class="sxs-lookup"><span data-stu-id="b4cf3-242">None</span></span>                                                   |
| [<span data-ttu-id="b4cf3-243">ncalrpc</span><span class="sxs-lookup"><span data-stu-id="b4cf3-243">ncalrpc</span></span>](/windows/desktop/Midl/ncalrpc)                 | <span data-ttu-id="b4cf3-244">指定應用程式或服務名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-244">String specifying application or service name.</span></span> <span data-ttu-id="b4cf3-245">字串不能包含任何反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-245">The string cannot include any backslash characters.</span></span> | <span data-ttu-id="b4cf3-246">我的 \_ 印表機</span><span class="sxs-lookup"><span data-stu-id="b4cf3-246">my\_printer</span></span>          | <span data-ttu-id="b4cf3-247">安全性</span><span class="sxs-lookup"><span data-stu-id="b4cf3-247">Security</span></span>                                               |



 

<span data-ttu-id="b4cf3-248">Ncacn HTTP 通訊協定序列支援的 **HttpConnectionOption** 選項名稱 \_ 會採用下列值。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-248">The **HttpConnectionOption** option name, supported for the ncacn\_http protocol sequence, takes the following value.</span></span>



| <span data-ttu-id="b4cf3-249">選項名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-249">Option name</span></span>       | <span data-ttu-id="b4cf3-250">值</span><span class="sxs-lookup"><span data-stu-id="b4cf3-250">Value</span></span>            |
|-------------------|------------------|
| <span data-ttu-id="b4cf3-251">HttpConnectOption</span><span class="sxs-lookup"><span data-stu-id="b4cf3-251">HttpConnectOption</span></span> | <span data-ttu-id="b4cf3-252">**UseHttpProxy**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-252">**UseHttpProxy**</span></span> |



 

<span data-ttu-id="b4cf3-253">**HttpConnectionOption** 可讓您在進行 HTTP 連線時，指示 RPC s 的行為。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-253">The **HttpConnectionOption** allows you to direct RPC s behavior when making HTTP connections.</span></span> <span data-ttu-id="b4cf3-254">**UseHttpProxy** 值會指示 RPC 隨時透過 Http proxy 路由傳送流量，包括當用戶端的網際網路選項設定在 Internet Explorer 中，以略過本機位址的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-254">The **UseHttpProxy** value instructs RPC to route its traffic through the Http proxy at all times, including when the client has the Internet Options set in Internet Explorer to  Bypass proxy server for local addresses.</span></span>  <span data-ttu-id="b4cf3-255">此選項會指示用戶端透過 Http proxy 強制連接至 RPC proxy。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-255">This option directs the client to forcefully connect to the RPC proxy through the Http proxy.</span></span> <span data-ttu-id="b4cf3-256">這可加速建立連接的時間，因為它會略過在使用 HTTP proxy 之前，直接搜尋 RPC 伺服器的任何延遲。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-256">This speeds up the time to establish a connection since it bypasses any delay searching for the RPC server directly prior to using the HTTP proxy.</span></span>

<span data-ttu-id="b4cf3-257">如果使用此 **HttpConnectionOption** 選項，且用戶端上的 Internet Explorer 未設定為使用該 Http proxy，則連線可能會失敗，並出現 **RPC \_ S 不正確 \_ \_ 網路 \_ 選項**。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-257">If this **HttpConnectionOption** option is used and Internet Explorer on the client is not configured to use that Http proxy, connections may fail with **RPC\_S\_INVALID\_NETWORK\_OPTIONS**.</span></span>

``` syntax
HttpConnectOption=UseHttpProxy
```

<span data-ttu-id="b4cf3-258">如需 **HttpConnectionOption** 的詳細資訊，請參閱 [使用 HTTP 做為 RPC 傳輸](using-http-as-an-rpc-transport.md)。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-258">For more information about the **HttpConnectionOption**, see [Using HTTP as an RPC Transport](using-http-as-an-rpc-transport.md).</span></span>

<span data-ttu-id="b4cf3-259">Ncalrpc  、ncacn \_ np、ncadg \_ ip \_ udp 和 ncadg ipx 通訊協定序列支援的安全性選項名稱 \_ 會採用下列選項值。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-259">The **Security** option name, supported for the ncalrpc, ncacn\_np, ncadg\_ip\_udp, and ncadg\_ipx protocol sequences, takes the following option values.</span></span>



| <span data-ttu-id="b4cf3-260">選項名稱</span><span class="sxs-lookup"><span data-stu-id="b4cf3-260">Option name</span></span>  | <span data-ttu-id="b4cf3-261">選項值</span><span class="sxs-lookup"><span data-stu-id="b4cf3-261">Option value</span></span>                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cf3-262">**安全性**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-262">**Security**</span></span> | <span data-ttu-id="b4cf3-263">{識別 \| 匿名模擬 \| } {動態 \| 靜態} {**true** \| **false**}</span><span class="sxs-lookup"><span data-stu-id="b4cf3-263">{identification \| anonymous \| impersonation} {dynamic \| static} {**true** \| **false**}</span></span> |



 

<span data-ttu-id="b4cf3-264">如果指定了安全性選項名稱，也必須提供每個安全性選項值集合中的一個專案。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-264">If the security option name is specified, one entry from each of the sets of security option values must also be supplied.</span></span> <span data-ttu-id="b4cf3-265">選項值必須以單一空白字元分隔。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-265">The option values must be separated by a single-space character.</span></span> <span data-ttu-id="b4cf3-266">例如，下列 *選項* 欄位有效：</span><span class="sxs-lookup"><span data-stu-id="b4cf3-266">For example, the following *Option* fields are valid:</span></span>

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

<span data-ttu-id="b4cf3-267">安全性選項值具有下列意義。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-267">The security option values have the following meanings.</span></span>



| <span data-ttu-id="b4cf3-268">安全性選項值</span><span class="sxs-lookup"><span data-stu-id="b4cf3-268">Security option value</span></span> | <span data-ttu-id="b4cf3-269">Description</span><span class="sxs-lookup"><span data-stu-id="b4cf3-269">Description</span></span>                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cf3-270">匿名</span><span class="sxs-lookup"><span data-stu-id="b4cf3-270">Anonymous</span></span>             | <span data-ttu-id="b4cf3-271">用戶端對伺服器而言是匿名。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-271">The client is anonymous to the server.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b4cf3-272">動態</span><span class="sxs-lookup"><span data-stu-id="b4cf3-272">Dynamic</span></span>               | <span data-ttu-id="b4cf3-273">當伺服器使用傳輸安全性時，伺服器會看到用戶端安全性識別中的變更。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-273">Changes in the client security identity are seen by the server when the server uses transport security.</span></span> <span data-ttu-id="b4cf3-274">這是 LRPC (ncalrpc) 傳輸層級安全性，以及區域具名管道 (ncacn \_ np) 傳輸層級安全性的預設模式。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-274">This is the default mode for LRPC (ncalrpc) transport level security, and for local named pipe (ncacn\_np) transport level security.</span></span>                                                                                                             |
| <span data-ttu-id="b4cf3-275">**False**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-275">**False**</span></span>             | <span data-ttu-id="b4cf3-276">有效 = **FALSE**;所有的權杖許可權設定（包括設定為 OFF 的設定）都會包含在伺服器上的權杖中，而且可由伺服器啟用。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-276">Effective = **FALSE**; all token privileges settings, including those set to OFF, are included in the token on the server and can be enabled by the server.</span></span> <span data-ttu-id="b4cf3-277">許可權僅與相同電腦 RPC 呼叫相關。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-277">Privileges are relevant for same-machine RPC calls only.</span></span>                                                                                                                                     |
| <span data-ttu-id="b4cf3-278">**識別**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-278">**Identification**</span></span>    | <span data-ttu-id="b4cf3-279">伺服器具有用戶端的相關資訊，但無法模擬。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-279">The server has information about the client but cannot impersonate.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b4cf3-280">**模擬**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-280">**Impersonation**</span></span>     | <span data-ttu-id="b4cf3-281">伺服器可在本機系統內代表用戶端執行動作 (傳輸層級安全性不支援委派) 。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-281">The server can act on behalf of the client within the local system (transport-level security does not support delegation).</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="b4cf3-282">**靜態**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-282">**Static**</span></span>            | <span data-ttu-id="b4cf3-283">當伺服器使用傳輸安全性時，伺服器不會看到用戶端安全性識別中的變更。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-283">Changes in the client security identity are not seen by the server when the server uses transport security.</span></span> <span data-ttu-id="b4cf3-284">這是遠端具名管道唯一可用的模式 (ncacn \_ np) 傳輸層級安全性。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-284">This is the only mode available to remote named pipe (ncacn\_np) transport level security.</span></span> <span data-ttu-id="b4cf3-285">呼叫端的身分識別會在該系結控制碼上的第一個遠端程序呼叫期間儲存，而不是在建立系結控制碼時儲存。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-285">The identity of the caller is saved during the first remote procedure call on that binding handle, not at the time the binding handle is created.</span></span> |
| <span data-ttu-id="b4cf3-286">**True**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-286">**True**</span></span>              | <span data-ttu-id="b4cf3-287">有效 = **TRUE**;只有設定為 ON 的權杖許可權設定才會包含在伺服器的權杖中。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-287">Effective = **TRUE**; only token privileges settings set to ON are included in the token on the server.</span></span> <span data-ttu-id="b4cf3-288">如果使用此選項，伺服器便無法開啟設定為 OFF 的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-288">Privileges set to OFF cannot be turned on by the server if this option is used.</span></span> <span data-ttu-id="b4cf3-289">許可權僅與相同電腦 RPC 呼叫相關。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-289">Privileges are relevant for same-machine RPC calls only.</span></span>                                                                                                         |



 

<span data-ttu-id="b4cf3-290">如需安全性選項的詳細資訊，請閱讀 [安全性](security.md)。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-290">For more information about security options, [Security](security.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4cf3-291">備註</span><span class="sxs-lookup"><span data-stu-id="b4cf3-291">Remarks</span></span>

<span data-ttu-id="b4cf3-292">除了 *Option* 語法所要求的位置之外，字串系結中不允許空白字元。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-292">White space is not allowed in string bindings except where required by the *Option* syntax.</span></span> <span data-ttu-id="b4cf3-293">[ *Networkaddress.cache.ttl*]、[ *端點*] 和 [ *選項* ] 欄位的預設設定會根據 *ProtocolSequence* 成員的值而不同。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-293">Default settings for the *NetworkAddress*, *Endpoint*, and *Option* fields vary according to the value of the *ProtocolSequence* member.</span></span>

<span data-ttu-id="b4cf3-294">針對所有字串系結欄位，會將單一反斜線字元 (\\) 被解釋為一個 escape 字元。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-294">For all string-binding fields, a single backslash character (\\) is interpreted as an escape character.</span></span> <span data-ttu-id="b4cf3-295">若要指定單一常值反斜線字元，您必須 () 提供兩個反斜線字元 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-295">To specify a single literal backslash character, you must supply two backslash characters (\\\\).</span></span>

<span data-ttu-id="b4cf3-296">字串系結包含系結控制碼的字元標記法，以及有時候系結控制碼的部分。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-296">A string binding contains the character representation of a binding handle and occasionally portions of a binding handle.</span></span> <span data-ttu-id="b4cf3-297">字串系結很方便表示系結控制碼的部分，但無法用於進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-297">String bindings are convenient for representing portions of a binding handle, but they can't be used for making remote procedure calls.</span></span> <span data-ttu-id="b4cf3-298">您必須先呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)，將它們轉換成系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-298">They must first be converted to a binding handle by calling [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span></span>

<span data-ttu-id="b4cf3-299">此外，字串系結不包含系結控制碼的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-299">Additionally, a string binding does not contain all of the information from a binding handle.</span></span> <span data-ttu-id="b4cf3-300">例如，與系結控制碼相關聯的驗證資訊（如果有的話）不會轉譯成呼叫 [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)所傳回的字串系結。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-300">For example, the authentication information, if any, associated with a binding handle is not translated into the string binding returned by calling the [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span>

<span data-ttu-id="b4cf3-301">在分散式應用程式的開發過程中，伺服器可以使用字串系結將其系結資訊傳達給用戶端，以建立用戶端伺服器關聯性，而不需要使用端點對應資料庫或名稱服務資料庫。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-301">During the development of a distributed application, servers can communicate their binding information to clients using string bindings to establish a client-server relationship without using the endpoint-map database or name-service database.</span></span> <span data-ttu-id="b4cf3-302">若要建立這類關聯性，請使用函數 [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) ，將一個或多個系結控制碼向量的系結控制碼轉換成字串系結，並提供字串系結給用戶端。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-302">To establish such a relationship, use the function [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) to convert one or more binding handles from a binding-handle vector to a string binding, and provide the string binding to the client.</span></span>

## <a name="examples"></a><span data-ttu-id="b4cf3-303">範例</span><span class="sxs-lookup"><span data-stu-id="b4cf3-303">Examples</span></span>

<span data-ttu-id="b4cf3-304">以下是有效字串系結的範例。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-304">The following are examples of valid string bindings.</span></span> <span data-ttu-id="b4cf3-305">在這些範例中，會使用 *obj uuid* 以方便表示字串格式的有效 uuid。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-305">In these examples, *obj-uuid* is used for convenience to represent a valid UUID in string form.</span></span> <span data-ttu-id="b4cf3-306">這些範例不會顯示 UUID 308FB580-1EB2-11CA-923B-08002B1075A7，而是顯示 *obj uuid*。</span><span class="sxs-lookup"><span data-stu-id="b4cf3-306">Instead of showing the UUID 308FB580-1EB2-11CA-923B-08002B1075A7, the examples show *obj-uuid*.</span></span>

``` syntax
obj-uuid@ncadg_mq:mymqserver
obj-uuid@ncacn_http:major7.microsoft.com[2225]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80,HttpConnectOption=UseHttpProxy]
obj-uuid@ncacn_ip_tcp:16.20.16.27[2001]
obj-uuid@ncacn_ip_tcp:16.20.16.27[endpoint=2001]
obj-uuid@ncacn_nb_nb:
obj-uuid@ncacn_nb_nb:[100]
obj-uuid@ncacn_np:
obj-uuid@ncacn_np:[\\pipe\\p3,Security=impersonation static true]
obj-uuid@ncacn_np:\\\\marketing[\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\marketing[endpoint=\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\sales
obj-uuid@ncacn_np:\\\\sales[\\pipe\\p1,Security=identification dynamic true]
obj-uuid@ncalrpc:
obj-uuid@ncalrpc:[object1_name_demonstrating_that_these_can_be_lengthy]
obj-uuid@ncalrpc:[object2_name,Security=anonymous static true]
obj-uuid@ncacn_vns_spp:server@group@org[500]
obj-uuid@ncacn_dnet_nsp:took[elf_server]
obj-uuid@ncacn_dnet_nsp:took[endpoint=elf_server]
obj-uuid@ncadg_ip_udp:128.10.2.30
obj-uuid@ncadg_ip_udp:maryos.microsoft.com[1025]
obj-uuid@ncadg_ipx: ~0000000108002B30612C[5000]
obj-uuid@ncadg_ipx:printserver
obj-uuid@ncacn_spx:annaw[4390]
obj-uuid@ncacn_spx:~0000000108002B30612C
```

## <a name="related-topics"></a><span data-ttu-id="b4cf3-307">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4cf3-307">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4cf3-308">**RpcBindingFromStringBinding**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-308">**RpcBindingFromStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[<span data-ttu-id="b4cf3-309">**RpcBindingToStringBinding**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-309">**RpcBindingToStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)
</dt> <dt>

[<span data-ttu-id="b4cf3-310">**RpcEpRegister**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-310">**RpcEpRegister**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)
</dt> <dt>

[<span data-ttu-id="b4cf3-311">使用 HTTP 做為 RPC 傳輸</span><span class="sxs-lookup"><span data-stu-id="b4cf3-311">Using HTTP as an RPC Transport</span></span>](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

