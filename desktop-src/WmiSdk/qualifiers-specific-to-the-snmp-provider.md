---
description: 限定詞包含執行特定的內容資訊和傳輸屬性，可定義 SNMP 提供者存取 SNMP 代理程式的方式。 以下列出 SNMP 提供者唯一的限定詞。
ms.assetid: f2ac107c-e201-4670-96d1-883419787377
ms.tgt_platform: multiple
title: SNMP 提供者專用的限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: a1405cb4d9609380fdf35d6ce05a0fc9e1255ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691515"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a><span data-ttu-id="7b575-104">SNMP 提供者專用的限定詞</span><span class="sxs-lookup"><span data-stu-id="7b575-104">Qualifiers Specific to the SNMP Provider</span></span>

<span data-ttu-id="7b575-105">限定詞包含執行特定的內容資訊和傳輸屬性，可定義 SNMP 提供者存取 SNMP 代理程式的方式。</span><span class="sxs-lookup"><span data-stu-id="7b575-105">Qualifiers contain implementation-specific context information and transport properties that define how the SNMP Provider accesses an SNMP agent.</span></span> <span data-ttu-id="7b575-106">以下列出 SNMP 提供者唯一的限定詞。</span><span class="sxs-lookup"><span data-stu-id="7b575-106">The following lists the qualifiers unique to the SNMP Provider.</span></span>

<dt>

<span data-ttu-id="7b575-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="7b575-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span></span> 
</dt> <dd>

<span data-ttu-id="7b575-108">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="7b575-108">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="7b575-109">與 SNMP 代理程式相關聯的傳輸位址，例如 IP 位址或 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="7b575-109">Transport address associated with the SNMP agent, such as an IP address or DNS name.</span></span> <span data-ttu-id="7b575-110">您應該將 **AgentAddress** 設定為有效的單點傳送主機位址，或是可透過作業系統的網域名稱解析程式來解析的網域主機名稱。</span><span class="sxs-lookup"><span data-stu-id="7b575-110">You should set **AgentAddress** to a valid unicast host address or a domain host name that can be resolved through the operating system's domain-name resolution process.</span></span> <span data-ttu-id="7b575-111">**AgentAddress** 沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="7b575-111">**AgentAddress** has no default value.</span></span>

</dd> <dt>

<span data-ttu-id="7b575-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span><span class="sxs-lookup"><span data-stu-id="7b575-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span></span> 
</dt> <dd>

<span data-ttu-id="7b575-113">資料類型： **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="7b575-113">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="7b575-114">尚未收到回應時，可傳送到此代理程式的同時未完成 SNMP 要求數目上限。</span><span class="sxs-lookup"><span data-stu-id="7b575-114">Maximum number of concurrently outstanding SNMP requests that can be sent to this agent while a response has not yet been received.</span></span> <span data-ttu-id="7b575-115">SNMP 要求會被視為未處理，直到接收到 PDU 回應或已超時。大型的視窗大小通常會改善效能，但某些代理程式在繁重的負載下可能無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7b575-115">An SNMP request is considered outstanding until a PDU response has been received or it has timed out. A large window size generally improves performance, but some agents might not work well under a heavy load.</span></span> <span data-ttu-id="7b575-116">**AgentFlowControlWindowSize** 可以設定為0，表示無限視窗大小或介於1和 2 ^ 32-1 之間的整數。</span><span class="sxs-lookup"><span data-stu-id="7b575-116">**AgentFlowControlWindowSize** can be set to 0 to indicate an infinite window size or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="7b575-117">預設值是 10。</span><span class="sxs-lookup"><span data-stu-id="7b575-117">The default value is 10.</span></span> <span data-ttu-id="7b575-118">此辨識符號是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7b575-118">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7b575-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span><span class="sxs-lookup"><span data-stu-id="7b575-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="7b575-120">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="7b575-120">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="7b575-121">SNMP 代理程式在讀取作業期間用來驗證 SNMP 通訊協定資料單位的可變長度八位字串 (PDU)  (SNMP 取得/取得下一個要求) 。</span><span class="sxs-lookup"><span data-stu-id="7b575-121">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a read operation (SNMP GET/GET NEXT requests).</span></span> <span data-ttu-id="7b575-122">群體名稱必須對應至 Unicode 字串，且僅限英數位元。</span><span class="sxs-lookup"><span data-stu-id="7b575-122">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="7b575-123">預設值為 public。</span><span class="sxs-lookup"><span data-stu-id="7b575-123">The default value is public.</span></span> <span data-ttu-id="7b575-124">此辨識符號是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7b575-124">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7b575-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span><span class="sxs-lookup"><span data-stu-id="7b575-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span></span> 
</dt> <dd>

<span data-ttu-id="7b575-126">資料類型： **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="7b575-126">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="7b575-127">在要求被視為失敗之前，單一 SNMP 要求可以重試的次數（如果沒有來自 SNMP 代理程式的回應）。</span><span class="sxs-lookup"><span data-stu-id="7b575-127">Number of times a single SNMP request can be retried when there is no response from the SNMP agent before the request is deemed to have failed.</span></span> <span data-ttu-id="7b575-128">**AgentRetryCount** 必須設定為介於0到 2 ^ 32-1 之間的整數。</span><span class="sxs-lookup"><span data-stu-id="7b575-128">**AgentRetryCount** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="7b575-129">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="7b575-129">The default value is 1.</span></span> <span data-ttu-id="7b575-130">此辨識符號是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7b575-130">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7b575-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="7b575-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span></span> 
</dt> <dd>

<span data-ttu-id="7b575-132">資料類型： **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="7b575-132">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="7b575-133">將 SNMP 通訊協定資料單位 (PDU) 之前的時間（以毫秒為單位）視為已卸載。</span><span class="sxs-lookup"><span data-stu-id="7b575-133">Time in milliseconds before the SNMP Protocol Data Unit (PDU) is considered to have been dropped.</span></span> <span data-ttu-id="7b575-134">這是等候傳送至 SNMP 代理程式的 SNMP 要求回應所需的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="7b575-134">This is the number of milliseconds to wait for a response to an SNMP request sent to the SNMP agent.</span></span> <span data-ttu-id="7b575-135">**AgentRetryTimeout** 必須設定為介於0到 2 ^ 32-1 之間的整數。</span><span class="sxs-lookup"><span data-stu-id="7b575-135">**AgentRetryTimeout** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="7b575-136">預設值為 500。</span><span class="sxs-lookup"><span data-stu-id="7b575-136">The default value is 500.</span></span> <span data-ttu-id="7b575-137">此辨識符號是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7b575-137">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7b575-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span><span class="sxs-lookup"><span data-stu-id="7b575-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span></span> 
</dt> <dd>

<span data-ttu-id="7b575-139">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="7b575-139">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="7b575-140">與 SNMP 代理程式通訊時所要使用的 SNMP 通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="7b575-140">Version of the SNMP protocol to be used when communicating with the SNMP agent.</span></span> <span data-ttu-id="7b575-141">目前，唯一有效的值為 1 (適用于 SNMPv2C) 的 SNMPv1) 和 2C (。</span><span class="sxs-lookup"><span data-stu-id="7b575-141">Currently, the only valid values are 1 (for SNMPv1) and 2C (for SNMPv2C).</span></span> <span data-ttu-id="7b575-142">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="7b575-142">The default value is 1.</span></span> <span data-ttu-id="7b575-143">此辨識符號是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7b575-143">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7b575-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="7b575-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span></span> 
</dt> <dd>

<span data-ttu-id="7b575-145">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="7b575-145">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="7b575-146">用來與 SNMP 代理程式通訊的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7b575-146">Transport protocol used to communicate with the SNMP agent.</span></span> <span data-ttu-id="7b575-147">目前唯一有效的值是網際網路通訊協定 (IP) 和網際網路封包交換 (IPX) 。</span><span class="sxs-lookup"><span data-stu-id="7b575-147">Currently the only valid values are Internet Protocol (IP) and Internet Packet Exchange (IPX).</span></span> <span data-ttu-id="7b575-148">預設值為 [IP]。</span><span class="sxs-lookup"><span data-stu-id="7b575-148">The default value is IP.</span></span> <span data-ttu-id="7b575-149">此辨識符號是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7b575-149">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7b575-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span><span class="sxs-lookup"><span data-stu-id="7b575-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span></span> 
</dt> <dd>

<span data-ttu-id="7b575-151">資料類型： **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="7b575-151">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="7b575-152">單一 SNMP PDU 內包含的最大變數系結數目。</span><span class="sxs-lookup"><span data-stu-id="7b575-152">Maximum number of variable bindings contained within a single SNMP PDU.</span></span> <span data-ttu-id="7b575-153">每個傳送至 SNMP 代理程式的 SNMP 要求都包含一或多個 SNMP 變數。</span><span class="sxs-lookup"><span data-stu-id="7b575-153">Every SNMP request sent to the SNMP agent contains one or more SNMP variables.</span></span> <span data-ttu-id="7b575-154">此參數會指定單一要求中可包含的最大變數數目。</span><span class="sxs-lookup"><span data-stu-id="7b575-154">This parameter specifies the largest number of variables that can be included in a single request.</span></span> <span data-ttu-id="7b575-155">**AgentVarBindsPerPdu** 可以設定為 0 (零) ，使實作為判斷最佳變數系結或介於1到 2 ^ 32-1 之間的整數。</span><span class="sxs-lookup"><span data-stu-id="7b575-155">**AgentVarBindsPerPdu** can be set to 0 (zero) to cause the implementation to determine the optimal variable bindings or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="7b575-156">請注意，增加此值可以改善效能，某些代理程式和網路無法處理產生的要求。</span><span class="sxs-lookup"><span data-stu-id="7b575-156">Note that while increasing this value can improve performance, some agents and networks cannot deal with the resulting request.</span></span> <span data-ttu-id="7b575-157">預設值是 10。</span><span class="sxs-lookup"><span data-stu-id="7b575-157">The default value is 10.</span></span> <span data-ttu-id="7b575-158">此辨識符號是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7b575-158">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7b575-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span><span class="sxs-lookup"><span data-stu-id="7b575-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="7b575-160">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="7b575-160">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="7b575-161">SNMP 代理程式在寫入作業期間，用來驗證 SNMP 通訊協定資料單位的可變長度八進位字串 (PDU)  (SNMP 組要求) 。</span><span class="sxs-lookup"><span data-stu-id="7b575-161">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a write operation (SNMP SET request).</span></span> <span data-ttu-id="7b575-162">群體名稱必須對應至 Unicode 字串，且僅限英數位元。</span><span class="sxs-lookup"><span data-stu-id="7b575-162">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="7b575-163">預設值為 public。</span><span class="sxs-lookup"><span data-stu-id="7b575-163">The default value is public.</span></span> <span data-ttu-id="7b575-164">此辨識符號是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7b575-164">This qualifier is optional.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b575-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b575-165">Requirements</span></span>



| <span data-ttu-id="7b575-166">需求</span><span class="sxs-lookup"><span data-stu-id="7b575-166">Requirement</span></span> | <span data-ttu-id="7b575-167">值</span><span class="sxs-lookup"><span data-stu-id="7b575-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7b575-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b575-168">Minimum supported client</span></span><br/> | <span data-ttu-id="7b575-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b575-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7b575-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b575-170">Minimum supported server</span></span><br/> | <span data-ttu-id="7b575-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b575-171">Windows Server 2008</span></span><br/> |



 

 




