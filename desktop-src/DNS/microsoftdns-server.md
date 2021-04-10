---
title: MicrosoftDNS_Server 類別
description: MicrosoftDNS \_ 伺服器類別描述 DNS 伺服器。 這個類別的每個實例都可以與一個 MicrosoftDNS 快取的實例 \_ 、一個 MicrosoftDNS \_ RootHints 的實例，以及 MicrosoftDNS 區域的多個實例相關聯 \_ 。
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- MicrosoftDNS_Server 類別 DNS
- MicrosoftDNS_Server 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933985"
---
# <a name="microsoftdns_server-class"></a><span data-ttu-id="2e21f-106">MicrosoftDNS \_ 伺服器類別</span><span class="sxs-lookup"><span data-stu-id="2e21f-106">MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="2e21f-107">**MicrosoftDNS \_ 伺服器** 類別描述 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-107">The **MicrosoftDNS\_Server** class describes a DNS Server.</span></span> <span data-ttu-id="2e21f-108">這個類別的每個實例都可以與一個 MicrosoftDNS 快取的實例、一個 [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)的實例，以及 [**MicrosoftDNS \_ 區域**](microsoftdns-zone.md)的多個實例相關聯。 [**\_**](microsoftdns-cache.md)</span><span class="sxs-lookup"><span data-stu-id="2e21f-108">Every instance of this class may be associated with one instance of [**MicrosoftDNS\_Cache**](microsoftdns-cache.md), one instance of [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md), and multiple instances of [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

<span data-ttu-id="2e21f-109">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="2e21f-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e21f-110">語法</span><span class="sxs-lookup"><span data-stu-id="2e21f-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a><span data-ttu-id="2e21f-111">成員</span><span class="sxs-lookup"><span data-stu-id="2e21f-111">Members</span></span>

<span data-ttu-id="2e21f-112">**MicrosoftDNS \_ 伺服器** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2e21f-112">The **MicrosoftDNS\_Server** class has these types of members:</span></span>

-   [<span data-ttu-id="2e21f-113">方法</span><span class="sxs-lookup"><span data-stu-id="2e21f-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="2e21f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="2e21f-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2e21f-115">方法</span><span class="sxs-lookup"><span data-stu-id="2e21f-115">Methods</span></span>

<span data-ttu-id="2e21f-116">**MicrosoftDNS \_ 伺服器** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2e21f-116">The **MicrosoftDNS\_Server** class has these methods.</span></span>



| <span data-ttu-id="2e21f-117">方法</span><span class="sxs-lookup"><span data-stu-id="2e21f-117">Method</span></span>                   | <span data-ttu-id="2e21f-118">描述</span><span class="sxs-lookup"><span data-stu-id="2e21f-118">Description</span></span>                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| <span data-ttu-id="2e21f-119">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="2e21f-119">**GetDistinguishedName**</span></span> | <span data-ttu-id="2e21f-120">捕獲區域的 DNS 辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="2e21f-120">Retrieves DNS distinguished name for the zone.</span></span><br/>                        |
| <span data-ttu-id="2e21f-121">**StartScavenging**</span><span class="sxs-lookup"><span data-stu-id="2e21f-121">**StartScavenging**</span></span>      | <span data-ttu-id="2e21f-122">開始清除要清除之區域中的過時記錄。</span><span class="sxs-lookup"><span data-stu-id="2e21f-122">Starts scavenging stale records in the zones subjected to scavenging.</span></span><br/> |
| <span data-ttu-id="2e21f-123">**StartService**</span><span class="sxs-lookup"><span data-stu-id="2e21f-123">**StartService**</span></span>         | <span data-ttu-id="2e21f-124">啟動 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-124">Starts the DNS Server.</span></span><br/>                                                |
| <span data-ttu-id="2e21f-125">**StopService**</span><span class="sxs-lookup"><span data-stu-id="2e21f-125">**StopService**</span></span>          | <span data-ttu-id="2e21f-126">停止 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-126">Stops the DNS Server.</span></span><br/>                                                 |



 

### <a name="properties"></a><span data-ttu-id="2e21f-127">屬性</span><span class="sxs-lookup"><span data-stu-id="2e21f-127">Properties</span></span>

<span data-ttu-id="2e21f-128">**MicrosoftDNS \_ 伺服器** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2e21f-128">The **MicrosoftDNS\_Server** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e21f-129">**AddressAnswerLimit**</span><span class="sxs-lookup"><span data-stu-id="2e21f-129">**AddressAnswerLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-132">回應位址要求時傳回的主機記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="2e21f-132">Maximum number of host records returned in response to an address request.</span></span> <span data-ttu-id="2e21f-133">介於5和28之間的值是有效的。</span><span class="sxs-lookup"><span data-stu-id="2e21f-133">Values between 5 and 28 are valid.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-134">**AllowUpdate**</span><span class="sxs-lookup"><span data-stu-id="2e21f-134">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-137">指定 DNS 伺服器是否接受動態更新要求。</span><span class="sxs-lookup"><span data-stu-id="2e21f-137">Specifies whether the DNS Server accepts dynamic update requests.</span></span> <span data-ttu-id="2e21f-138">有效的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="2e21f-138">Valid values are as shown in the following table.</span></span>



| <span data-ttu-id="2e21f-139">值</span><span class="sxs-lookup"><span data-stu-id="2e21f-139">Value</span></span>                                                                                                | <span data-ttu-id="2e21f-140">意義</span><span class="sxs-lookup"><span data-stu-id="2e21f-140">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2e21f-141"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-141"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2e21f-142">無限制。</span><span class="sxs-lookup"><span data-stu-id="2e21f-142">No Restrictions.</span></span><br/>                                                                           |
| <span id="1"></span><dl> <span data-ttu-id="2e21f-143"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-143"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2e21f-144">不允許對 SOA 記錄進行動態更新。</span><span class="sxs-lookup"><span data-stu-id="2e21f-144">Does not allow dynamic updates of SOA records.</span></span><br/>                                             |
| <span id="2"></span><dl> <span data-ttu-id="2e21f-145"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-145"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2e21f-146">不允許在區域根目錄進行 NS 記錄的動態更新。</span><span class="sxs-lookup"><span data-stu-id="2e21f-146">Does not allow dynamic updates of NS records at the zone root.</span></span><br/>                             |
| <span id="4"></span><dl> <span data-ttu-id="2e21f-147"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-147"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2e21f-148">不允許在區域根目錄 (委派 NS 記錄) 的情況動態更新 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="2e21f-148">Does not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span><br/> |



 

<span data-ttu-id="2e21f-149">將這些值加總以決定設定值。</span><span class="sxs-lookup"><span data-stu-id="2e21f-149">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-150">**AutoCacheUpdate**</span><span class="sxs-lookup"><span data-stu-id="2e21f-150">**AutoCacheUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-151">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-153">指出 DNS 伺服器是否嘗試使用根伺服器的資料來更新其快取專案。</span><span class="sxs-lookup"><span data-stu-id="2e21f-153">Indicates whether the DNS Server attempts to update its cache entries using data from root servers.</span></span> <span data-ttu-id="2e21f-154">當 DNS 伺服器開機時，它需要根伺服器的 [提示] NS 的清單，以及過去稱為快取檔案的伺服器記錄。</span><span class="sxs-lookup"><span data-stu-id="2e21f-154">When a DNS Server boots, it needs a list of root server 'hints' NS and A records for the servers historically called the cache file.</span></span> <span data-ttu-id="2e21f-155">Microsoft DNS 伺服器的功能，可讓使用者根據根伺服器的回應，嘗試寫回新的快取檔案。</span><span class="sxs-lookup"><span data-stu-id="2e21f-155">Microsoft DNS Servers have a feature that enables them to attempt to write back a new cache file based on the responses from root servers.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-156">**AutoConfigFileZones**</span><span class="sxs-lookup"><span data-stu-id="2e21f-156">**AutoConfigFileZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-159">指出當名稱伺服器變更時，必須更新 DNS 伺服器名稱所授權的標準主要區域。</span><span class="sxs-lookup"><span data-stu-id="2e21f-159">Indicates which standard primary zones that are authoritative for the name of the DNS Server must be updated when the name server changes.</span></span> <span data-ttu-id="2e21f-160">下列是有效值：</span><span class="sxs-lookup"><span data-stu-id="2e21f-160">Valid values are as follows:</span></span>



| <span data-ttu-id="2e21f-161">值</span><span class="sxs-lookup"><span data-stu-id="2e21f-161">Value</span></span>                                                                                                | <span data-ttu-id="2e21f-162">意義</span><span class="sxs-lookup"><span data-stu-id="2e21f-162">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2e21f-163"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-163"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2e21f-164">無。</span><span class="sxs-lookup"><span data-stu-id="2e21f-164">None.</span></span><br/>                                           |
| <span id="1"></span><dl> <span data-ttu-id="2e21f-165"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-165"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2e21f-166">僅允許動態更新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-166">Only servers that allow dynamic updates.</span></span><br/>        |
| <span id="2"></span><dl> <span data-ttu-id="2e21f-167"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-167"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2e21f-168">僅限不允許動態更新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-168">Only servers that do not allow dynamic updates.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="2e21f-169"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-169"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2e21f-170">所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-170">All servers.</span></span><br/>                                    |



 

<span data-ttu-id="2e21f-171">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="2e21f-171">The default value is 1.</span></span>

<span data-ttu-id="2e21f-172">\* \* Windows Server 2003： \* \*</span><span class="sxs-lookup"><span data-stu-id="2e21f-172">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2e21f-173">數位3代表所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-173">The number 3 represents All servers.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-174">**BindSecondaries**</span><span class="sxs-lookup"><span data-stu-id="2e21f-174">**BindSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-175">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-176">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-176">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-177">決定傳送至非 Microsoft DNS 伺服器次要資料庫時的 AXFR 訊息格式。</span><span class="sxs-lookup"><span data-stu-id="2e21f-177">Determines the AXFR message format when sending to non-Microsoft DNS Server secondaries.</span></span> <span data-ttu-id="2e21f-178">當設定為 TRUE 時，DNS 伺服器會以未壓縮的格式將傳輸傳送至非 Microsoft DNS 伺服器次要複本。</span><span class="sxs-lookup"><span data-stu-id="2e21f-178">When set to TRUE, the DNS Server sends transfers to non-Microsoft DNS Server secondaries in the uncompressed format.</span></span> <span data-ttu-id="2e21f-179">若為 FALSE，則會以 fast 格式傳送所有傳輸。</span><span class="sxs-lookup"><span data-stu-id="2e21f-179">When FALSE, all transfers are sent in the fast format.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-180">**BootMethod**</span><span class="sxs-lookup"><span data-stu-id="2e21f-180">**BootMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-181">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-182">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-183">DNS 伺服器的初始化方法。</span><span class="sxs-lookup"><span data-stu-id="2e21f-183">Initialization method for the DNS Server.</span></span> <span data-ttu-id="2e21f-184">有效的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="2e21f-184">Valid values are shown in the following table.</span></span>



| <span data-ttu-id="2e21f-185">值</span><span class="sxs-lookup"><span data-stu-id="2e21f-185">Value</span></span>                                                                                                | <span data-ttu-id="2e21f-186">意義</span><span class="sxs-lookup"><span data-stu-id="2e21f-186">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2e21f-187"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-187"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2e21f-188">初始 化。</span><span class="sxs-lookup"><span data-stu-id="2e21f-188">Uninitialized.</span></span><br/>                    |
| <span id="1"></span><dl> <span data-ttu-id="2e21f-189"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-189"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2e21f-190">從檔案開機。</span><span class="sxs-lookup"><span data-stu-id="2e21f-190">Boot from file.</span></span><br/>                   |
| <span id="2"></span><dl> <span data-ttu-id="2e21f-191"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-191"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2e21f-192">從登錄開機。</span><span class="sxs-lookup"><span data-stu-id="2e21f-192">Boot from registry.</span></span><br/>               |
| <span id="3"></span><dl> <span data-ttu-id="2e21f-193"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-193"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="2e21f-194">從目錄和登錄開機。</span><span class="sxs-lookup"><span data-stu-id="2e21f-194">Boot from directory and registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e21f-195">**DefaultAgingState**</span><span class="sxs-lookup"><span data-stu-id="2e21f-195">**DefaultAgingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-196">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-197">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-198">為此 DNS 伺服器上建立的所有 Active Directory 整合區域設定的預設 **ScavengingInterval** 值。</span><span class="sxs-lookup"><span data-stu-id="2e21f-198">Default **ScavengingInterval** value set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="2e21f-199">預設值為零，表示清除已停用。</span><span class="sxs-lookup"><span data-stu-id="2e21f-199">The default value is zero, indicating scavenging is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-200">**DefaultNoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="2e21f-200">**DefaultNoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-201">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-202">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-203">無重新整理間隔（以小時為單位），設定為在此 DNS 伺服器上建立的所有 Active Directory 整合區域。</span><span class="sxs-lookup"><span data-stu-id="2e21f-203">No-refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="2e21f-204">預設值為168小時 (七天) 。</span><span class="sxs-lookup"><span data-stu-id="2e21f-204">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-205">**DefaultRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="2e21f-205">**DefaultRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-206">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-207">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-207">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-208">針對在此 DNS 伺服器上建立的所有 Active Directory 整合區域，設定的重新整理間隔（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e21f-208">Refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="2e21f-209">預設值為168小時 (七天) 。</span><span class="sxs-lookup"><span data-stu-id="2e21f-209">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-210">**DisableAutoReverseZones**</span><span class="sxs-lookup"><span data-stu-id="2e21f-210">**DisableAutoReverseZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-211">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-212">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-213">指出 DNS 伺服器是否自動建立標準反向查閱區域。</span><span class="sxs-lookup"><span data-stu-id="2e21f-213">Indicates whether the DNS Server automatically creates standard reverse look up zones.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-214">**DisjointNets**</span><span class="sxs-lookup"><span data-stu-id="2e21f-214">**DisjointNets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-215">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-216">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-217">指出用來將查詢傳送到遠端 DNS 伺服器之通訊端的預設埠系結是否可以覆寫。</span><span class="sxs-lookup"><span data-stu-id="2e21f-217">Indicates whether the default port binding for a socket used to send queries to remote DNS Servers can be overridden.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-218">**DsAvailable**</span><span class="sxs-lookup"><span data-stu-id="2e21f-218">**DsAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-219">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-221">指出 DNS 伺服器上是否有可用的 DS。</span><span class="sxs-lookup"><span data-stu-id="2e21f-221">Indicates whether there is an available DS on the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-222">**DsPollingInterval**</span><span class="sxs-lookup"><span data-stu-id="2e21f-222">**DsPollingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-223">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-224">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-224">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-225">輪詢 DS 整合區域的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e21f-225">Interval, in seconds, to poll the DS-integrated zones.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-226">**DsTombstoneInterval**</span><span class="sxs-lookup"><span data-stu-id="2e21f-226">**DsTombstoneInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-227">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-228">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-229">目錄服務整合區域中已加上邏輯化記錄的存留期（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e21f-229">Lifetime of tombstoned records in Directory Service integrated zones, expressed in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-230">**EDnsCacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="2e21f-230">**EDnsCacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-231">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-231">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-233">快取資訊的存留期（以秒為單位），描述其他 DNS 伺服器所支援的 EDNS 版本。</span><span class="sxs-lookup"><span data-stu-id="2e21f-233">Lifetime, in seconds, of the cached information describing the EDNS version supported by other DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-234">**EnableDirectoryPartitions**</span><span class="sxs-lookup"><span data-stu-id="2e21f-234">**EnableDirectoryPartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-235">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-236">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-237">指定是否在 DNS 伺服器上啟用應用程式目錄分割的支援。</span><span class="sxs-lookup"><span data-stu-id="2e21f-237">Specifies whether support for application directory partitions is enabled on the DNS Server.</span></span>

<span data-ttu-id="2e21f-238">\* \* Windows Server 2003： \* \*</span><span class="sxs-lookup"><span data-stu-id="2e21f-238">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2e21f-239">這個方法的名稱是 EnableDirectoryPartitionSupport。</span><span class="sxs-lookup"><span data-stu-id="2e21f-239">This method is named EnableDirectoryPartitionSupport.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-240">**EnableDnsSec**</span><span class="sxs-lookup"><span data-stu-id="2e21f-240">**EnableDnsSec**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-241">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-242">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-243">在下表中，指定 DNS 伺服器是否包含回應中的 DNSSEC 專屬 Rr、KEY、SIG 和 NXT：</span><span class="sxs-lookup"><span data-stu-id="2e21f-243">Specifies whether the DNS Server includes DNSSEC-specific RRs, KEY, SIG, and NXT in a response, per the following table:</span></span>



| <span data-ttu-id="2e21f-244">值</span><span class="sxs-lookup"><span data-stu-id="2e21f-244">Value</span></span>                                                                                                | <span data-ttu-id="2e21f-245">意義</span><span class="sxs-lookup"><span data-stu-id="2e21f-245">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2e21f-246"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-246"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2e21f-247">除非查詢要求 DNSSEC 記錄類型的資源記錄集，否則回應中不會包含任何 DNSSEC 記錄。</span><span class="sxs-lookup"><span data-stu-id="2e21f-247">No DNSSEC records are included in the response unless the query requested a resource record set of the DNSSEC record type.</span></span><br/>          |
| <span id="1"></span><dl> <span data-ttu-id="2e21f-248"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-248"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2e21f-249">根據 RFC 2535，DNSSEC 記錄會包含在回應中。</span><span class="sxs-lookup"><span data-stu-id="2e21f-249">DNSSEC records are included in the response according to RFC 2535.</span></span><br/>                                                                  |
| <span id="2"></span><dl> <span data-ttu-id="2e21f-250"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-250"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2e21f-251">只有當原始用戶端查詢包含根據 RFC 2671 的 OPT 資源記錄時，DNSSEC 記錄才會包含在回應中</span><span class="sxs-lookup"><span data-stu-id="2e21f-251">DNSSEC records are included in a response only if the original client query contained the OPT resource record according to RFC 2671</span></span><br/> |



 

<span data-ttu-id="2e21f-252">如果查詢要求 DNSSEC 類型的資源記錄集，則 DNS 伺服器一律會回應這類記錄（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2e21f-252">If a query requests a resource record set of the DNSSEC type, the DNS Server always responds with such records, if available.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-253">**EnableEDnsProbes**</span><span class="sxs-lookup"><span data-stu-id="2e21f-253">**EnableEDnsProbes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-254">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-254">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-255">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-255">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-256">指定 DNS 伺服器的行為。</span><span class="sxs-lookup"><span data-stu-id="2e21f-256">Specifies the behavior of the DNS Server.</span></span> <span data-ttu-id="2e21f-257">若為 TRUE，則 DNS 伺服器一律會根據 RFC 2671 以 OPT 資源記錄回應，除非遠端伺服器指出它不支援先前交換中的 EDNS。</span><span class="sxs-lookup"><span data-stu-id="2e21f-257">When TRUE, the DNS Server always responds with OPT resource records according to RFC 2671, unless the remote server has indicated it does not support EDNS in a prior exchange.</span></span> <span data-ttu-id="2e21f-258">若為 FALSE，則只有當選擇在原始查詢中傳送時，DNS 伺服器才會以選擇來回應查詢。</span><span class="sxs-lookup"><span data-stu-id="2e21f-258">If FALSE, the DNS Server responds to queries with OPTs only if OPTs are sent in the original query.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-259">**EventLogLevel**</span><span class="sxs-lookup"><span data-stu-id="2e21f-259">**EventLogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-260">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-260">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-261">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-261">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-262">指出 DNS 伺服器在事件檢視器系統記錄檔中所記錄的事件。</span><span class="sxs-lookup"><span data-stu-id="2e21f-262">Indicates which events the DNS Server records in the Event Viewer system log.</span></span> <span data-ttu-id="2e21f-263">使用下列值。</span><span class="sxs-lookup"><span data-stu-id="2e21f-263">The following values are used.</span></span>



| <span data-ttu-id="2e21f-264">值</span><span class="sxs-lookup"><span data-stu-id="2e21f-264">Value</span></span>                                                                                                | <span data-ttu-id="2e21f-265">意義</span><span class="sxs-lookup"><span data-stu-id="2e21f-265">Meaning</span></span>                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2e21f-266"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-266"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2e21f-267">無。</span><span class="sxs-lookup"><span data-stu-id="2e21f-267">None.</span></span><br/>                         |
| <span id="1"></span><dl> <span data-ttu-id="2e21f-268"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-268"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2e21f-269">只記錄錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e21f-269">Log only errors.</span></span><br/>              |
| <span id="2"></span><dl> <span data-ttu-id="2e21f-270"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-270"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2e21f-271">只記錄警告和錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e21f-271">Log only warnings and errors.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="2e21f-272"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-272"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2e21f-273">記錄所有事件。</span><span class="sxs-lookup"><span data-stu-id="2e21f-273">Log all events.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="2e21f-274">**ForwardDelegations**</span><span class="sxs-lookup"><span data-stu-id="2e21f-274">**ForwardDelegations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-275">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-276">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-276">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-277">指定是否轉送委派子領域的查詢。</span><span class="sxs-lookup"><span data-stu-id="2e21f-277">Specifies whether queries to delegated sub-zones are forwarded.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-278">**轉送**</span><span class="sxs-lookup"><span data-stu-id="2e21f-278">**Forwarders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-279">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2e21f-279">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-280">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-280">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-281">列舉 DNS 伺服器轉送查詢的轉寄站 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="2e21f-281">Enumerates the list of IP addresses of Forwarders to which the DNS Server forwards queries.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-282">**ForwardingTimeout**</span><span class="sxs-lookup"><span data-stu-id="2e21f-282">**ForwardingTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-283">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-284">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-284">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-285">以秒為單位的時間，DNS 伺服器轉送查詢將會等待轉寄 [*站的解析，然後再*](f-gly.md) 嘗試解決查詢本身。</span><span class="sxs-lookup"><span data-stu-id="2e21f-285">Time, in seconds, a DNS Server forwarding a query will wait for resolution from the [*forwarder*](f-gly.md) before attempting to resolve the query itself.</span></span>

<span data-ttu-id="2e21f-286">如果轉送伺服器未設定為使用遞迴，此值就沒有意義。</span><span class="sxs-lookup"><span data-stu-id="2e21f-286">This value is meaningless if the forwarding server is not set to use recursion.</span></span> <span data-ttu-id="2e21f-287">若要判斷這一點，請檢查 IsSlave 的布林值屬性。</span><span class="sxs-lookup"><span data-stu-id="2e21f-287">To determine this, check the IsSlave Boolean property.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-288">**IsSlave**</span><span class="sxs-lookup"><span data-stu-id="2e21f-288">**IsSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-289">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-290">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-291">**如果透過** 轉寄站的名稱解析失敗，則 DNS 伺服器不使用遞迴。</span><span class="sxs-lookup"><span data-stu-id="2e21f-291">**TRUE** if the DNS server does not use recursion when name-resolution through forwarders fails.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-292">**ListenAddresses**</span><span class="sxs-lookup"><span data-stu-id="2e21f-292">**ListenAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-293">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2e21f-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-294">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-294">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-295">列舉 DNS 伺服器可以接收查詢的 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="2e21f-295">Enumerates the list of IP addresses on which the DNS Server can receive queries.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-296">**LocalNetPriority**</span><span class="sxs-lookup"><span data-stu-id="2e21f-296">**LocalNetPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-297">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-298">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-298">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-299">指出當傳回記錄時，DNS 伺服器是否將優先順序提供給本機的網路位址。</span><span class="sxs-lookup"><span data-stu-id="2e21f-299">Indicates whether the DNS Server gives priority to the local net address when returning A records.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-300">**LogFileMaxSize**</span><span class="sxs-lookup"><span data-stu-id="2e21f-300">**LogFileMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-301">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-302">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-302">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-303">DNS 伺服器的偵錯工具記錄檔大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e21f-303">Size of the DNS Server debug log, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-304">**>logfilepath**</span><span class="sxs-lookup"><span data-stu-id="2e21f-304">**LogFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-305">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e21f-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-306">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-306">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-307">DNS 伺服器 debug 記錄檔的檔案名和路徑。</span><span class="sxs-lookup"><span data-stu-id="2e21f-307">File name and path for the DNS Server debug log.</span></span> <span data-ttu-id="2e21f-308">預設值為% system32% \\ dns \\ dns .log。</span><span class="sxs-lookup"><span data-stu-id="2e21f-308">Default is %system32%\\dns\\dns.log.</span></span> <span data-ttu-id="2e21f-309">相對路徑相對於% Systemroot% \\ System32。</span><span class="sxs-lookup"><span data-stu-id="2e21f-309">Relative paths are relative to %Systemroot%\\System32.</span></span> <span data-ttu-id="2e21f-310">您可以使用絕對路徑，但不支援 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="2e21f-310">Absolute paths may be used, but UNC paths are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-311">**LogIPFilterList**</span><span class="sxs-lookup"><span data-stu-id="2e21f-311">**LogIPFilterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-312">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2e21f-312">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-313">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-313">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-314">用來篩選寫入至偵錯工具記錄檔之 DNS 事件的 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="2e21f-314">List of IP addresses used to filter DNS events written to the debug log.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-315">**LogLevel**</span><span class="sxs-lookup"><span data-stu-id="2e21f-315">**LogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-316">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-317">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-317">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-318">指出事件檢視器系統記錄檔中啟用的原則。</span><span class="sxs-lookup"><span data-stu-id="2e21f-318">Indicates which policies are activated in the Event Viewer system log.</span></span>

<span data-ttu-id="2e21f-319">應根據下列演算法設定為特定值：事件檢視器系統記錄) 中 (要啟用的每個原則都會指派特定值。</span><span class="sxs-lookup"><span data-stu-id="2e21f-319">Should be set to specific values based on the following algorithm: Every policy (to be activated in the Event Viewer system log) is assigned a specific value.</span></span>



| <span data-ttu-id="2e21f-320">值</span><span class="sxs-lookup"><span data-stu-id="2e21f-320">Value</span></span>                                                                                                                  | <span data-ttu-id="2e21f-321">意義</span><span class="sxs-lookup"><span data-stu-id="2e21f-321">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="2e21f-322"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-322"><dt>**1**</dt></span></span> </dl>                   | <span data-ttu-id="2e21f-323">查詢。</span><span class="sxs-lookup"><span data-stu-id="2e21f-323">Query.</span></span><br/>                                   |
| <span id="16"></span><dl> <span data-ttu-id="2e21f-324"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-324"><dt>**16**</dt></span></span> </dl>                 | <span data-ttu-id="2e21f-325">通知。</span><span class="sxs-lookup"><span data-stu-id="2e21f-325">Notify.</span></span><br/>                                  |
| <span id="32"></span><dl> <span data-ttu-id="2e21f-326"><dt>**32**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-326"><dt>**32**</dt></span></span> </dl>                 | <span data-ttu-id="2e21f-327">Update。</span><span class="sxs-lookup"><span data-stu-id="2e21f-327">Update.</span></span><br/>                                  |
| <span id="254"></span><dl> <span data-ttu-id="2e21f-328"><dt>**254**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-328"><dt>**254**</dt></span></span> </dl>               | <span data-ttu-id="2e21f-329">Nonquery 交易。</span><span class="sxs-lookup"><span data-stu-id="2e21f-329">Nonquery transactions.</span></span><br/>                   |
| <span id="256"></span><dl> <span data-ttu-id="2e21f-330"><dt>**256**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-330"><dt>**256**</dt></span></span> </dl>               | <span data-ttu-id="2e21f-331">問題。</span><span class="sxs-lookup"><span data-stu-id="2e21f-331">Questions.</span></span><br/>                               |
| <span id="512"></span><dl> <span data-ttu-id="2e21f-332"><dt>**512**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-332"><dt>**512**</dt></span></span> </dl>               | <span data-ttu-id="2e21f-333">答案。</span><span class="sxs-lookup"><span data-stu-id="2e21f-333">Answers.</span></span><br/>                                 |
| <span id="4096"></span><dl> <span data-ttu-id="2e21f-334"><dt>**4096**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-334"><dt>**4096**</dt></span></span> </dl>             | <span data-ttu-id="2e21f-335">Send。</span><span class="sxs-lookup"><span data-stu-id="2e21f-335">Send.</span></span><br/>                                    |
| <span id="8192"></span><dl> <span data-ttu-id="2e21f-336"><dt>**8192**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-336"><dt>**8192**</dt></span></span> </dl>             | <span data-ttu-id="2e21f-337">接收。</span><span class="sxs-lookup"><span data-stu-id="2e21f-337">Receive.</span></span><br/>                                 |
| <span id="16384"></span><dl> <span data-ttu-id="2e21f-338"><dt>**16384**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-338"><dt>**16384**</dt></span></span> </dl>           | <span data-ttu-id="2e21f-339">Udp。</span><span class="sxs-lookup"><span data-stu-id="2e21f-339">UDP.</span></span><br/>                                     |
| <span id="32768"></span><dl> <span data-ttu-id="2e21f-340"><dt>**32768**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-340"><dt>**32768**</dt></span></span> </dl>           | <span data-ttu-id="2e21f-341">TCP。</span><span class="sxs-lookup"><span data-stu-id="2e21f-341">TCP.</span></span><br/>                                     |
| <span id="65535"></span><dl> <span data-ttu-id="2e21f-342"><dt>**65535**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-342"><dt>**65535**</dt></span></span> </dl>           | <span data-ttu-id="2e21f-343">所有封包。</span><span class="sxs-lookup"><span data-stu-id="2e21f-343">All packets.</span></span><br/>                             |
| <span id="65536"></span><dl> <span data-ttu-id="2e21f-344"><dt>**65536**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-344"><dt>**65536**</dt></span></span> </dl>           | <span data-ttu-id="2e21f-345">NT 目錄服務寫入交易。</span><span class="sxs-lookup"><span data-stu-id="2e21f-345">NT Directory Service write transaction.</span></span><br/>  |
| <span id="131072"></span><dl> <span data-ttu-id="2e21f-346"><dt>**131072**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-346"><dt>**131072**</dt></span></span> </dl>         | <span data-ttu-id="2e21f-347">NT 目錄服務更新交易。</span><span class="sxs-lookup"><span data-stu-id="2e21f-347">NT Directory Service update transaction.</span></span><br/> |
| <span id="16777216"></span><dl> <span data-ttu-id="2e21f-348"><dt>**16777216**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-348"><dt>**16777216**</dt></span></span> </dl>     | <span data-ttu-id="2e21f-349">完整封包。</span><span class="sxs-lookup"><span data-stu-id="2e21f-349">Full packets.</span></span><br/>                            |
| <span id="2147483648"></span><dl> <span data-ttu-id="2e21f-350"><dt>**2147483648**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-350"><dt>**2147483648**</dt></span></span> </dl> | <span data-ttu-id="2e21f-351">寫入。</span><span class="sxs-lookup"><span data-stu-id="2e21f-351">Write through.</span></span><br/>                           |



 

<span data-ttu-id="2e21f-352">這個屬性會指出對應至要啟動之所有原則的值總和。</span><span class="sxs-lookup"><span data-stu-id="2e21f-352">The sum of the values corresponding to all the policies to be activated is indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-353">**LooseWildcarding**</span><span class="sxs-lookup"><span data-stu-id="2e21f-353">**LooseWildcarding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-354">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-355">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-355">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-356">指出 DNS 伺服器是否執行鬆散式萬用字元。</span><span class="sxs-lookup"><span data-stu-id="2e21f-356">Indicates whether the DNS Server performs loose wildcarding.</span></span> <span data-ttu-id="2e21f-357">如果未定義或為零，則伺服器會遵循 DNS RFC 中指定的萬用字元行為。</span><span class="sxs-lookup"><span data-stu-id="2e21f-357">If undefined or zero, the server follows the wildcarding behavior specified in the DNS RFC.</span></span> <span data-ttu-id="2e21f-358">在此情況下，建議系統管理員針對所有無法接收郵件的主機包含 MX 記錄。</span><span class="sxs-lookup"><span data-stu-id="2e21f-358">In this case, an administrator is advised to include MX records for all hosts incapable of receiving mail.</span></span> <span data-ttu-id="2e21f-359">如果是非零值，伺服器會搜尋最接近的萬用字元節點;在此情況下，系統管理員應該將 MX 記錄放在區域根目錄和萬用字元節點 ( ' \* ' ) 直接放在區域根目錄正下方。</span><span class="sxs-lookup"><span data-stu-id="2e21f-359">If nonzero, the server seeks the closest wildcard node; in this case, an administrator should put MX records at the zone root and in a wildcard node ('\*') directly below the zone root.</span></span> <span data-ttu-id="2e21f-360">此外，系統管理員也應該在接收自己的郵件的主機上放置自我參考的 MX 記錄。</span><span class="sxs-lookup"><span data-stu-id="2e21f-360">Also, administrators should put self-referencing MX records on hosts that receive their own mail.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-361">**MaxCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="2e21f-361">**MaxCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-362">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-363">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-363">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-364">遞迴名稱查詢的記錄可能會保留在 DNS 伺服器快取中的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e21f-364">Maximum time, in seconds, the record of a recursive name query may remain in the DNS Server cache.</span></span> <span data-ttu-id="2e21f-365">當此專案的值到期時，DNS 伺服器會從快取中刪除記錄，即使記錄中的 TTL 欄位值較大也是如此。</span><span class="sxs-lookup"><span data-stu-id="2e21f-365">The DNS Server deletes records from the cache when the value of this entry expires, even if the value of the TTL field in the record is greater.</span></span>

<span data-ttu-id="2e21f-366">這個屬性的預設值為86400秒 (1 天) 。</span><span class="sxs-lookup"><span data-stu-id="2e21f-366">The default value of this property is 86,400 seconds (1 day).</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-367">**MaxNegativeCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="2e21f-367">**MaxNegativeCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-368">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-369">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-369">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-370">遞迴查詢中名稱錯誤結果的最長時間（以秒為單位）可能會保留在 DNS 伺服器快取中。</span><span class="sxs-lookup"><span data-stu-id="2e21f-370">Maximum time, in seconds, a name error result from a recursive query may remain in the DNS Server cache.</span></span> <span data-ttu-id="2e21f-371">當此計時器過期時，DNS 會刪除快取中的記錄，即使 TTL 欄位更大也是如此。</span><span class="sxs-lookup"><span data-stu-id="2e21f-371">DNS deletes records from the cache when this timer expires, even if the TTL field is greater.</span></span> <span data-ttu-id="2e21f-372">預設值為 86400 (一天) 。</span><span class="sxs-lookup"><span data-stu-id="2e21f-372">Default value is 86,400 (one day).</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-373">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2e21f-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2e21f-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e21f-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-376">DNS 伺服器的完整功能變數名稱 (FQDN) 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2e21f-376">Fully qualified domain name (FQDN) or IP address of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-377">**NameCheckFlag**</span><span class="sxs-lookup"><span data-stu-id="2e21f-377">**NameCheckFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-378">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-379">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-379">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-380">指出要在 DNS 名稱中使用的一組合格字元。</span><span class="sxs-lookup"><span data-stu-id="2e21f-380">Indicates the set of eligible characters to be used in DNS names.</span></span> <span data-ttu-id="2e21f-381">使用下列值。</span><span class="sxs-lookup"><span data-stu-id="2e21f-381">The following values are used.</span></span>



| <span data-ttu-id="2e21f-382">值</span><span class="sxs-lookup"><span data-stu-id="2e21f-382">Value</span></span>                                                                                                | <span data-ttu-id="2e21f-383">意義</span><span class="sxs-lookup"><span data-stu-id="2e21f-383">Meaning</span></span>                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2e21f-384"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-384"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2e21f-385">Strict RFC (ANSI) </span><span class="sxs-lookup"><span data-stu-id="2e21f-385">Strict RFC (ANSI)</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="2e21f-386"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-386"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2e21f-387">非 RFC (ANSI) </span><span class="sxs-lookup"><span data-stu-id="2e21f-387">Non RFC (ANSI)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="2e21f-388"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-388"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="2e21f-389">多位元組 (UTF8) </span><span class="sxs-lookup"><span data-stu-id="2e21f-389">Multibyte (UTF8)</span></span><br/>  |



 

<span data-ttu-id="2e21f-390">\* \* Windows Server 2003： \* \*</span><span class="sxs-lookup"><span data-stu-id="2e21f-390">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2e21f-391">"2" 的值表示「任何」。</span><span class="sxs-lookup"><span data-stu-id="2e21f-391">A value of "2" indicates "Any."</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-392">**NoRecursion**</span><span class="sxs-lookup"><span data-stu-id="2e21f-392">**NoRecursion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-393">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-393">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-394">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-394">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-395">指出 DNS 伺服器是否執行遞迴查詢。</span><span class="sxs-lookup"><span data-stu-id="2e21f-395">Indicates whether the DNS Server performs recursive look ups.</span></span> <span data-ttu-id="2e21f-396">TRUE 表示不執行遞迴查詢。</span><span class="sxs-lookup"><span data-stu-id="2e21f-396">TRUE indicates recursive look ups are not performed.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-397">**RecursionRetry**</span><span class="sxs-lookup"><span data-stu-id="2e21f-397">**RecursionRetry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-398">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-399">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-399">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-400">重試遞迴查閱之前經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="2e21f-400">Elapsed seconds before retrying a recursive look up.</span></span> <span data-ttu-id="2e21f-401">如果屬性未定義或為零，則會在三秒後進行重試。</span><span class="sxs-lookup"><span data-stu-id="2e21f-401">If the property is undefined or zero, retries are made after three seconds.</span></span> <span data-ttu-id="2e21f-402">不建議使用者變更此屬性。</span><span class="sxs-lookup"><span data-stu-id="2e21f-402">Users are discouraged from altering this property.</span></span> <span data-ttu-id="2e21f-403">在某些情況下，應該變更屬性;其中一個範例是當 DNS 伺服器透過低速連結將遠端伺服器連線，而且 DNS 伺服器在接收來自遠端 DNS 的回應之前正在重試。</span><span class="sxs-lookup"><span data-stu-id="2e21f-403">There are certain situations when the property should be changed; one example is when the DNS Server contacts remote servers over a slow link, and the DNS Server is retrying before receiving response from the remote DNS.</span></span> <span data-ttu-id="2e21f-404">在此情況下，比起從遠端 DNS 觀察到的回應時間，將時間提高一點會很合理。</span><span class="sxs-lookup"><span data-stu-id="2e21f-404">In this case, raising the time out to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-405">**RecursionTimeout**</span><span class="sxs-lookup"><span data-stu-id="2e21f-405">**RecursionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-406">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-406">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-407">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-407">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-408">DNS 伺服器放棄遞迴查詢之前經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="2e21f-408">Elapsed seconds before the DNS Server gives up recursive query.</span></span> <span data-ttu-id="2e21f-409">如果屬性未定義或為零，則 DNS 伺服器會在15秒後放棄。</span><span class="sxs-lookup"><span data-stu-id="2e21f-409">If the property is undefined or zero, the DNS Server gives up after 15 seconds.</span></span> <span data-ttu-id="2e21f-410">一般來說，有15秒的時間足以讓任何未完成的回應恢復到 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-410">In general, the 15-second time out is sufficient to allow any outstanding response to get back to the DNS Server.</span></span>

<span data-ttu-id="2e21f-411">不建議使用者變更此屬性。</span><span class="sxs-lookup"><span data-stu-id="2e21f-411">Users are discouraged from altering this property.</span></span> <span data-ttu-id="2e21f-412">其中一個內容應變更的情況是，當 DNS 伺服器透過低速連結將遠端伺服器連線，而且觀察到 DNS 伺服器在 \_ 收到回應之前拒絕伺服器失敗) 的查詢 (。</span><span class="sxs-lookup"><span data-stu-id="2e21f-412">One scenario where the property should be changed is when the DNS Server contacts remote servers over a slow link, and the DNS Server is observed rejecting queries (with SERVER\_FAILURE) before responses are received.</span></span>

<span data-ttu-id="2e21f-413">用戶端解析程式也會重試查詢，因此需要仔細調查，以判斷遠端回應是否真的與超時的查詢相關聯。在此情況下，將超時值提高為比從遠端 DNS 觀察到的回應時間稍微長一點，是合理的。</span><span class="sxs-lookup"><span data-stu-id="2e21f-413">Client resolvers also retry queries, so careful investigation is required to determine whether remote responses are actually associated with the query that timed out. In this case, raising the time out value to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-414">**RoundRobin**</span><span class="sxs-lookup"><span data-stu-id="2e21f-414">**RoundRobin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-415">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-416">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-416">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-417">指出 DNS 伺服器是否四捨五入 robins 多個記錄。</span><span class="sxs-lookup"><span data-stu-id="2e21f-417">Indicates whether the DNS Server round robins multiple A records.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-418">**RpcProtocol**</span><span class="sxs-lookup"><span data-stu-id="2e21f-418">**RpcProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-419">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-419">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-420">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-420">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-421">用來執行管理 RPC 的 RPC 通訊協定或通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2e21f-421">RPC protocol or protocols over which administrative RPC runs.</span></span> <span data-ttu-id="2e21f-422">下列演算法用來指派特定值：</span><span class="sxs-lookup"><span data-stu-id="2e21f-422">The following algorithm is used to assign a specific value:</span></span>



| <span data-ttu-id="2e21f-423">值</span><span class="sxs-lookup"><span data-stu-id="2e21f-423">Value</span></span>                                                                                                | <span data-ttu-id="2e21f-424">意義</span><span class="sxs-lookup"><span data-stu-id="2e21f-424">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2e21f-425"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-425"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2e21f-426">無</span><span class="sxs-lookup"><span data-stu-id="2e21f-426">None</span></span><br/>        |
| <span id="1"></span><dl> <span data-ttu-id="2e21f-427"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-427"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2e21f-428">TCP</span><span class="sxs-lookup"><span data-stu-id="2e21f-428">TCP</span></span><br/>         |
| <span id="2"></span><dl> <span data-ttu-id="2e21f-429"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-429"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2e21f-430">具名管道</span><span class="sxs-lookup"><span data-stu-id="2e21f-430">Named Pipes</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="2e21f-431"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-431"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2e21f-432">Lpc</span><span class="sxs-lookup"><span data-stu-id="2e21f-432">LPC</span></span><br/>         |



 

<span data-ttu-id="2e21f-433">值的總和表示使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2e21f-433">The sum of the values indicates the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-434">**ScavengingInterval**</span><span class="sxs-lookup"><span data-stu-id="2e21f-434">**ScavengingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-435">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-435">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-436">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-436">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-437">DNS 伺服器所執行的兩個連續清除作業之間的間隔時間（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e21f-437">Interval, in hours, between two consecutive scavenging operations performed by the DNS Server.</span></span> <span data-ttu-id="2e21f-438">零表示清除已停用。</span><span class="sxs-lookup"><span data-stu-id="2e21f-438">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="2e21f-439">預設值為168小時 (七天) 。</span><span class="sxs-lookup"><span data-stu-id="2e21f-439">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-440">**SecureResponses**</span><span class="sxs-lookup"><span data-stu-id="2e21f-440">**SecureResponses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-441">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-441">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-442">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-442">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-443">指出 DNS 伺服器是否以獨佔方式將名稱記錄儲存在與提供它們的伺服器相同的子樹中。</span><span class="sxs-lookup"><span data-stu-id="2e21f-443">Indicates whether the DNS Server exclusively saves records of names in the same subtree as the server that provided them.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-444">**SendPort**</span><span class="sxs-lookup"><span data-stu-id="2e21f-444">**SendPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-445">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-446">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-446">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-447">DNS 伺服器將 UDP 查詢傳送到其他伺服器的埠。</span><span class="sxs-lookup"><span data-stu-id="2e21f-447">Port on which the DNS Server sends UDP queries to other servers.</span></span> <span data-ttu-id="2e21f-448">根據預設，DNS 伺服器會在系結至 DNS 埠的通訊端上傳送查詢。</span><span class="sxs-lookup"><span data-stu-id="2e21f-448">By default, the DNS Server sends queries on a socket bound to the DNS port.</span></span>

<span data-ttu-id="2e21f-449">在某些情況下，這不是最佳的設定。</span><span class="sxs-lookup"><span data-stu-id="2e21f-449">Under certain situations, this is not the best configuration.</span></span> <span data-ttu-id="2e21f-450">其中一個明顯的情況是當系統管理員封鎖具有防火牆的 DNS 埠以防止外部存取 DNS 伺服器，但仍希望伺服器能夠連線到網際網路 DNS 伺服器，以提供內部用戶端的名稱解析。</span><span class="sxs-lookup"><span data-stu-id="2e21f-450">One obvious case is when an administrator blocks the DNS port with a firewall to prevent outside access to the DNS Server, but still wants the server to be able to contact Internet DNS Servers to provide name resolution for internal clients.</span></span> <span data-ttu-id="2e21f-451">另一種情況是當 DNS 伺服器支援不連續的神經網路時 (屬性 **DisjointNets** 設定為 TRUE 會識別此案例) 。</span><span class="sxs-lookup"><span data-stu-id="2e21f-451">Another case is when the DNS Server is supporting disjoint nets (the property **DisjointNets** set to TRUE identifies this scenario).</span></span> <span data-ttu-id="2e21f-452">在這些情況下，將 **SendOnNonDnsPort** 屬性設定為非零值，會指示 DNS 伺服器系結至任意埠，以傳送至遠端 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-452">In these cases, setting the **SendOnNonDnsPort** property to a nonzero value directs the DNS Server to bind to an arbitrary port for sending to remote DNS Servers.</span></span>

<span data-ttu-id="2e21f-453">如果 **SendOnNonDnsPort** 值大於1024，DNS 伺服器會明確地系結至指定的埠值。</span><span class="sxs-lookup"><span data-stu-id="2e21f-453">If the **SendOnNonDnsPort** value is greater than 1024, the DNS Server binds explicitly to the port value given.</span></span> <span data-ttu-id="2e21f-454">當系統管理員需要針對防火牆用途修正 DNS 查詢埠時，此設定選項會很有用。</span><span class="sxs-lookup"><span data-stu-id="2e21f-454">This configuration option is useful when an administrator needs to fix the DNS query port for firewall purposes.</span></span>

<span data-ttu-id="2e21f-455">\* \* Windows Server 2003： \* \*</span><span class="sxs-lookup"><span data-stu-id="2e21f-455">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2e21f-456">將 [傳送埠] 屬性設定為非零值，會導致 DNS 伺服器系結至任意埠，以傳送至遠端 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2e21f-456">Setting the SendPort property to a non-zero value causes the DNS server to bind to an arbitrary port for sending to remote DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-457">**ServerAddresses**</span><span class="sxs-lookup"><span data-stu-id="2e21f-457">**ServerAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-458">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2e21f-458">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-459">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e21f-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-460">列舉 DNS 伺服器的 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="2e21f-460">Enumerates the list of IP addresses for the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-461">**StrictFileParsing**</span><span class="sxs-lookup"><span data-stu-id="2e21f-461">**StrictFileParsing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-462">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-462">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-463">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-463">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-464">指出 DNS 伺服器是否嚴格剖析 [*區域*](z-gly.md) 檔案。</span><span class="sxs-lookup"><span data-stu-id="2e21f-464">Indicates whether the DNS Server parses [*zone files*](z-gly.md) strictly.</span></span> <span data-ttu-id="2e21f-465">如果未定義或為零，伺服器會記錄並忽略區域檔案中的錯誤資料，並繼續載入。</span><span class="sxs-lookup"><span data-stu-id="2e21f-465">If undefined or zero, the server will log and ignore bad data in the zone file and continue to load.</span></span> <span data-ttu-id="2e21f-466">如果是非零值，伺服器將會記錄並因區域檔案錯誤而失敗。</span><span class="sxs-lookup"><span data-stu-id="2e21f-466">If nonzero, the server will log and fail on zone file errors.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-467">**UpdateOptions**</span><span class="sxs-lookup"><span data-stu-id="2e21f-467">**UpdateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-468">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-469">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e21f-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-470">限制可在伺服器上動態更新的記錄類型，除了伺服器和區域物件上的 **AllowUpdate** 設定以外，還會用到它。</span><span class="sxs-lookup"><span data-stu-id="2e21f-470">Restricts the type of records that can be dynamically updated on the server, used in addition to the **AllowUpdate** settings on Server and Zone objects.</span></span>

<span data-ttu-id="2e21f-471">\* \* Windows Server 2003： \* \*</span><span class="sxs-lookup"><span data-stu-id="2e21f-471">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="2e21f-472">0：沒有限制。</span><span class="sxs-lookup"><span data-stu-id="2e21f-472">0: No restrictions.</span></span>

<span data-ttu-id="2e21f-473">1：不允許對 SOA 記錄進行動態更新。</span><span class="sxs-lookup"><span data-stu-id="2e21f-473">1: Do not allow dynamic updates of SOA records.</span></span>

<span data-ttu-id="2e21f-474">2：不允許在區域根目錄進行 NS 記錄的動態更新。</span><span class="sxs-lookup"><span data-stu-id="2e21f-474">2: Do not allow dynamic updates of NS records at the zone root.</span></span>

<span data-ttu-id="2e21f-475">4：不允許不在區域根 (委派 NS 記錄) 的 NS 記錄進行動態更新。</span><span class="sxs-lookup"><span data-stu-id="2e21f-475">4: Do not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span>

<span data-ttu-id="2e21f-476">將這些值加總以決定設定值。</span><span class="sxs-lookup"><span data-stu-id="2e21f-476">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-477">**版本**</span><span class="sxs-lookup"><span data-stu-id="2e21f-477">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-478">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-479">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2e21f-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-480">DNS 伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="2e21f-480">Version of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-481">**WriteAuthorityNS**</span><span class="sxs-lookup"><span data-stu-id="2e21f-481">**WriteAuthorityNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-482">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2e21f-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-483">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-483">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-484">指定 DNS 伺服器是否會在成功回應時，將 NS 和 SOA 記錄寫入授權單位區段。</span><span class="sxs-lookup"><span data-stu-id="2e21f-484">Specifies whether the DNS Server writes NS and SOA records to the authority section on successful response.</span></span>

</dd> <dt>

<span data-ttu-id="2e21f-485">**XfrConnectTimeout**</span><span class="sxs-lookup"><span data-stu-id="2e21f-485">**XfrConnectTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e21f-486">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2e21f-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e21f-487">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2e21f-487">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2e21f-488">DNS 伺服器在嘗試區域傳輸時，等候遠端伺服器的 TCP 連線成功的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e21f-488">Time, in seconds, the DNS Server waits for a successful TCP connection to a remote server when attempting a zone transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e21f-489">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e21f-489">Requirements</span></span>



| <span data-ttu-id="2e21f-490">需求</span><span class="sxs-lookup"><span data-stu-id="2e21f-490">Requirement</span></span> | <span data-ttu-id="2e21f-491">值</span><span class="sxs-lookup"><span data-stu-id="2e21f-491">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e21f-492">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e21f-492">Minimum supported client</span></span><br/> | <span data-ttu-id="2e21f-493">都不支援</span><span class="sxs-lookup"><span data-stu-id="2e21f-493">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2e21f-494">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e21f-494">Minimum supported server</span></span><br/> | <span data-ttu-id="2e21f-495">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e21f-495">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2e21f-496">命名空間</span><span class="sxs-lookup"><span data-stu-id="2e21f-496">Namespace</span></span><br/>                | <span data-ttu-id="2e21f-497">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="2e21f-497">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2e21f-498">MOF</span><span class="sxs-lookup"><span data-stu-id="2e21f-498">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e21f-499"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e21f-499"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e21f-500">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e21f-500">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e21f-501">**MicrosoftDNS 伺服器類別的 StartService 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2e21f-501">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="2e21f-502">**MicrosoftDNS 伺服器類別的 StopService 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2e21f-502">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="2e21f-503">**MicrosoftDNS 伺服器類別的 StartScavenging 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2e21f-503">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="2e21f-504">**MicrosoftDNS 伺服器類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="2e21f-504">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





