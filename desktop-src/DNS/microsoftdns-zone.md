---
title: MicrosoftDNS_Zone 類別
description: MicrosoftDNS \_ 區域類別描述 DNS 區域。 MicrosoftDNS 區域類別的每個實例都 \_ 必須只指派給一部 DNS 伺服器。 區域可能會與多個 MicrosoftDNS \_ 網域或 MicrosoftDNS ResourceRecord 類別的實例相關聯 \_ 。
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- MicrosoftDNS_Zone 類別 DNS
- MicrosoftDNS_Zone 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025594"
---
# <a name="microsoftdns_zone-class"></a><span data-ttu-id="ace84-107">MicrosoftDNS \_ 區域類別</span><span class="sxs-lookup"><span data-stu-id="ace84-107">MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="ace84-108">本文包含「從屬」一詞的參考，Microsoft 已不再使用該字詞。</span><span class="sxs-lookup"><span data-stu-id="ace84-108">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="ace84-109">從軟體中移除該字詞時，我們也會將其從本文中移除。</span><span class="sxs-lookup"><span data-stu-id="ace84-109">When the term is removed from the software, we’ll remove it from this article.</span></span>

> [!NOTE]
> <span data-ttu-id="ace84-110">本文包含「主伺服器」一詞的參考，也就是 Microsoft 不再使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="ace84-110">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="ace84-111">從軟體中移除該字詞時，我們也會將其從本文中移除。</span><span class="sxs-lookup"><span data-stu-id="ace84-111">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="ace84-112">**MicrosoftDNS \_ 區域** 類別描述 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-112">The **MicrosoftDNS\_Zone** class describes a DNS Zone.</span></span> <span data-ttu-id="ace84-113">**MicrosoftDNS \_ 區域** 類別的每個實例都必須只指派給一部 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ace84-113">Every instance of the **MicrosoftDNS\_Zone** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="ace84-114">區域可能會與多個 [**MicrosoftDNS \_ 網域**](microsoftdns-domain.md) 或 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 類別的實例相關聯。</span><span class="sxs-lookup"><span data-stu-id="ace84-114">Zones may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="ace84-115">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="ace84-115">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace84-116">語法</span><span class="sxs-lookup"><span data-stu-id="ace84-116">Syntax</span></span>

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a><span data-ttu-id="ace84-117">成員</span><span class="sxs-lookup"><span data-stu-id="ace84-117">Members</span></span>

<span data-ttu-id="ace84-118">**MicrosoftDNS \_ 區域** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ace84-118">The **MicrosoftDNS\_Zone** class has these types of members:</span></span>

-   [<span data-ttu-id="ace84-119">方法</span><span class="sxs-lookup"><span data-stu-id="ace84-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="ace84-120">屬性</span><span class="sxs-lookup"><span data-stu-id="ace84-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ace84-121">方法</span><span class="sxs-lookup"><span data-stu-id="ace84-121">Methods</span></span>

<span data-ttu-id="ace84-122">**MicrosoftDNS \_ 區域** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ace84-122">The **MicrosoftDNS\_Zone** class has these methods.</span></span>



| <span data-ttu-id="ace84-123">方法</span><span class="sxs-lookup"><span data-stu-id="ace84-123">Method</span></span>                   | <span data-ttu-id="ace84-124">描述</span><span class="sxs-lookup"><span data-stu-id="ace84-124">Description</span></span>                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace84-125">**AgeAllRecords**</span><span class="sxs-lookup"><span data-stu-id="ace84-125">**AgeAllRecords**</span></span>        | <span data-ttu-id="ace84-126">啟用部分或所有非 NS 和非 SOA 記錄的過時。</span><span class="sxs-lookup"><span data-stu-id="ace84-126">Enables aging for some or all non-NS and non-SOA records.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="ace84-127">**ChangeZoneType**</span><span class="sxs-lookup"><span data-stu-id="ace84-127">**ChangeZoneType**</span></span>       | <span data-ttu-id="ace84-128">變更區欄位型別。</span><span class="sxs-lookup"><span data-stu-id="ace84-128">Changes zone types.</span></span> <br/> <span data-ttu-id="ace84-129">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="ace84-129">Qualifiers: Implemented</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="ace84-130">**CreateZone**</span><span class="sxs-lookup"><span data-stu-id="ace84-130">**CreateZone**</span></span>           | <span data-ttu-id="ace84-131">建立新的區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-131">Creates a new zone.</span></span> <br/> <span data-ttu-id="ace84-132">限定詞：無。</span><span class="sxs-lookup"><span data-stu-id="ace84-132">Qualifiers: None.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="ace84-133">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="ace84-133">**ForceRefresh**</span></span>         | <span data-ttu-id="ace84-134">強制更新主要 DNS 伺服器的次要複本。</span><span class="sxs-lookup"><span data-stu-id="ace84-134">Forces an update of the secondary from the Master DNS Server.</span></span> <br/> <span data-ttu-id="ace84-135">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="ace84-135">Qualifiers: Implemented</span></span><br/>                                                                                               |
| <span data-ttu-id="ace84-136">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="ace84-136">**GetDistinguishedName**</span></span> | <span data-ttu-id="ace84-137">取得區域的 DS 分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="ace84-137">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="ace84-138">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="ace84-138">Qualifiers: Implemented</span></span><br/>                                                                                                                 |
| <span data-ttu-id="ace84-139">**PauseZone**</span><span class="sxs-lookup"><span data-stu-id="ace84-139">**PauseZone**</span></span>            | <span data-ttu-id="ace84-140">暫停區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-140">Pauses the Zone.</span></span> <br/> <span data-ttu-id="ace84-141">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="ace84-141">Qualifiers: Implemented</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="ace84-142">**ReloadZone**</span><span class="sxs-lookup"><span data-stu-id="ace84-142">**ReloadZone**</span></span>           | <span data-ttu-id="ace84-143">重載區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-143">Reloads the Zone.</span></span> <br/> <span data-ttu-id="ace84-144">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="ace84-144">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="ace84-145">**ResetSecondaries**</span><span class="sxs-lookup"><span data-stu-id="ace84-145">**ResetSecondaries**</span></span>     | <span data-ttu-id="ace84-146">重設次要 ip 位址陣列。</span><span class="sxs-lookup"><span data-stu-id="ace84-146">Resets the secondary ip address array.</span></span> <br/> <span data-ttu-id="ace84-147">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="ace84-147">Qualifiers: Implemented</span></span><br/>                                                                                                                      |
| <span data-ttu-id="ace84-148">**ResumeZone**</span><span class="sxs-lookup"><span data-stu-id="ace84-148">**ResumeZone**</span></span>           | <span data-ttu-id="ace84-149">繼續區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-149">Resumes the Zone.</span></span> <br/> <span data-ttu-id="ace84-150">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="ace84-150">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="ace84-151">**UpdateFromDS**</span><span class="sxs-lookup"><span data-stu-id="ace84-151">**UpdateFromDS**</span></span>         | <span data-ttu-id="ace84-152">從目錄服務強制更新區域 (DS) 。</span><span class="sxs-lookup"><span data-stu-id="ace84-152">Forces an update of the Zone from the Directory Service (DS).</span></span> <span data-ttu-id="ace84-153">若要讓這個方法有效，ZoneType 必須是0。區域必須確實儲存在 DS 中。</span><span class="sxs-lookup"><span data-stu-id="ace84-153">For this method to be valid, the ZoneType must be 0 the Zone must indeed be stored in the DS.</span></span> <br/> <span data-ttu-id="ace84-154">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="ace84-154">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="ace84-155">**WriteBackZone**</span><span class="sxs-lookup"><span data-stu-id="ace84-155">**WriteBackZone**</span></span>        | <span data-ttu-id="ace84-156">將區域資料儲存至其區域檔案。</span><span class="sxs-lookup"><span data-stu-id="ace84-156">Saves Zone data to its zone file.</span></span> <br/> <span data-ttu-id="ace84-157">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="ace84-157">Qualifiers: Implemented, static</span></span><br/>                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="ace84-158">屬性</span><span class="sxs-lookup"><span data-stu-id="ace84-158">Properties</span></span>

<span data-ttu-id="ace84-159">**MicrosoftDNS \_ 區域** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ace84-159">The **MicrosoftDNS\_Zone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ace84-160">**老化**</span><span class="sxs-lookup"><span data-stu-id="ace84-160">**Aging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-161">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-163">指定區域的過時和清除行為。</span><span class="sxs-lookup"><span data-stu-id="ace84-163">Specifies the aging and scavenging behavior of the zone.</span></span> <span data-ttu-id="ace84-164">零表示清除已停用。</span><span class="sxs-lookup"><span data-stu-id="ace84-164">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="ace84-165">停用清除時，區域中記錄的時間戳記不會重新整理，而且記錄不會被清除。</span><span class="sxs-lookup"><span data-stu-id="ace84-165">When scavenging is disabled, the timestamps of records in the zone are not refreshed, and the records are not subjected to scavenging.</span></span> <span data-ttu-id="ace84-166">當設定為1時，會對記錄進行清除，並在伺服器收到記錄的動態更新要求時重新整理其時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ace84-166">When set to one, records are subjected to scavenging and their timestamps are refreshed when the server receives the dynamic update request for the records.</span></span> <span data-ttu-id="ace84-167">針對 Active Directory 整合的區域，此值會設定為建立區域之 DNS 伺服器的 *DefaultAgingState* 屬性。</span><span class="sxs-lookup"><span data-stu-id="ace84-167">For Active Directory-integrated zones, this value is set to the *DefaultAgingState* property of the DNS Server where the zone is created.</span></span> <span data-ttu-id="ace84-168">標準主要區域的預設值為零。</span><span class="sxs-lookup"><span data-stu-id="ace84-168">For standard primary zones, the default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-169">**AllowUpdate**</span><span class="sxs-lookup"><span data-stu-id="ace84-169">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-172">指出區域是否接受動態更新要求。</span><span class="sxs-lookup"><span data-stu-id="ace84-172">Indicates whether the Zone accepts dynamic update requests.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-173">**自動建立**</span><span class="sxs-lookup"><span data-stu-id="ace84-173">**AutoCreated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-174">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-176">指出區域是否自動建立。</span><span class="sxs-lookup"><span data-stu-id="ace84-176">Indicates whether the Zone is autocreated.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-177">**AvailForScavengeTime**</span><span class="sxs-lookup"><span data-stu-id="ace84-177">**AvailForScavengeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-178">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-180">指定伺服器可能嘗試清除區域的時間。</span><span class="sxs-lookup"><span data-stu-id="ace84-180">Specifies the time when the server may attempt scavenging the zone.</span></span> <span data-ttu-id="ace84-181">即使已將區域設定為啟用清除，但在這段時間之前，DNS 伺服器不會嘗試清除此區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-181">Even if the zone is configured to enable scavenging the DNS server will not attempt scavenging this zone until after this moment.</span></span> <span data-ttu-id="ace84-182">此值會設定為目前的時間加上區域的重新整理間隔（每次載入區域時）。</span><span class="sxs-lookup"><span data-stu-id="ace84-182">This value is set to the current time plus the Refresh Interval of the zone whenever the zone is loaded.</span></span> <span data-ttu-id="ace84-183">此參數會儲存在本機，而不會複寫至區域的其他複本。</span><span class="sxs-lookup"><span data-stu-id="ace84-183">This parameter is stored locally, and is not replicated to other copies of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-184">**檔**</span><span class="sxs-lookup"><span data-stu-id="ace84-184">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ace84-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-187">指出區域檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ace84-187">Indicates the name of the zone file.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-188">**DisableWINSRecordReplication**</span><span class="sxs-lookup"><span data-stu-id="ace84-188">**DisableWINSRecordReplication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-189">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-191">指出 WINS 記錄是否已複寫。</span><span class="sxs-lookup"><span data-stu-id="ace84-191">Indicates whether the WINS record is replicated.</span></span> <span data-ttu-id="ace84-192">如果設定為 TRUE，則會停用 WINS 記錄複寫。</span><span class="sxs-lookup"><span data-stu-id="ace84-192">If set to TRUE, WINS record replication is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-193">**DsIntegrated**</span><span class="sxs-lookup"><span data-stu-id="ace84-193">**DsIntegrated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-194">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-196">指定區域是否為 DS 整合。</span><span class="sxs-lookup"><span data-stu-id="ace84-196">Specifies whether the zone is DS integrated.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-197">**ForwarderSlave**</span><span class="sxs-lookup"><span data-stu-id="ace84-197">**ForwarderSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-198">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-200">指出當解析指定轉寄區域的名稱時，DNS 是否使用遞迴。</span><span class="sxs-lookup"><span data-stu-id="ace84-200">Indicates whether the DNS uses recursion when resolving the names for the specified forward zone.</span></span> <span data-ttu-id="ace84-201">僅適用于條件式轉送區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-201">Applicable to Conditional Forwarding zones only.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-202">**ForwarderTimeout**</span><span class="sxs-lookup"><span data-stu-id="ace84-202">**ForwarderTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-203">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-205">表示在轉送區域下轉送名稱查詢的 DNS 伺服器在嘗試解決查詢本身之前，會等待轉寄站解析的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ace84-205">Indicates the time, in seconds, a DNS server forwarding a query for the name under the forward zone waits for resolution from the forwarder before attempting to resolve the query itself.</span></span> <span data-ttu-id="ace84-206">此參數僅適用于轉寄區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-206">This parameter is applicable to the Forward zones only.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-207">**LastSuccessfulSoaCheck**</span><span class="sxs-lookup"><span data-stu-id="ace84-207">**LastSuccessfulSoaCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-208">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-210">自1970年1月1日開始起算的秒數，因為區域的 SOA 序號是上次檢查時間。</span><span class="sxs-lookup"><span data-stu-id="ace84-210">Number of seconds since the beginning of January 1, 1970 GMT, since the SOA serial number for the zone was last checked.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-211">**LastSuccessfulXfr**</span><span class="sxs-lookup"><span data-stu-id="ace84-211">**LastSuccessfulXfr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-212">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-214">從1970年1月1日開始，自從上次從主伺服器傳送區域以來的秒數。</span><span class="sxs-lookup"><span data-stu-id="ace84-214">Number of seconds since the beginning of January 1, 1970 GMT, since the zone was last transferred from a master server.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-215">**LocalMasterServers**</span><span class="sxs-lookup"><span data-stu-id="ace84-215">**LocalMasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-216">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ace84-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ace84-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-218">此區域主要 DNS 伺服器的本機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ace84-218">Local IP addresses of the master DNS servers for this zone.</span></span> <span data-ttu-id="ace84-219">如果設定，這些主要 MasterServers 會在 Active Directory 中找到。</span><span class="sxs-lookup"><span data-stu-id="ace84-219">If set, these masters over-ride the MasterServers found in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-220">**MasterServers**</span><span class="sxs-lookup"><span data-stu-id="ace84-220">**MasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-221">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ace84-221">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ace84-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-223">此區域之主要 DNS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ace84-223">IP addresses of the master DNS servers for this zone.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-224">**NoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="ace84-224">**NoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-225">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-227">指定上次更新記錄的時間戳記與重新整理時間戳記最早時間之間的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="ace84-227">Specifies the time interval between the last update of a record's timestamp and the earliest moment when the timestamp can be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-228">**通知**</span><span class="sxs-lookup"><span data-stu-id="ace84-228">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-229">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-231">指出主要區域是否會在其 Rr 資料庫中通知任何變更的次要複本。</span><span class="sxs-lookup"><span data-stu-id="ace84-231">Indicates whether the master Zone notifies secondaries of any changes in its RRs database.</span></span> <span data-ttu-id="ace84-232">設定為1以通知次要。</span><span class="sxs-lookup"><span data-stu-id="ace84-232">Set to 1 to notify secondaries.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-233">**NotifyServers**</span><span class="sxs-lookup"><span data-stu-id="ace84-233">**NotifyServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-234">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ace84-234">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ace84-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-236">列舉 DNS 伺服器 IP 位址的字串陣列，這些 IP 位址會在此區域中收到變更通知。</span><span class="sxs-lookup"><span data-stu-id="ace84-236">Array of strings enumerating IP addresses of DNS servers to be notified of changes in this zone.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-237">**已暫停**</span><span class="sxs-lookup"><span data-stu-id="ace84-237">**Paused**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-238">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-238">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-240">指出是否暫停區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-240">Indicates whether the Zone is paused.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-241">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="ace84-241">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-242">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-244">指定重新整理間隔，在這段期間，會將具有非零時間戳記的記錄重新整理為保留在區域中。</span><span class="sxs-lookup"><span data-stu-id="ace84-244">Specifies the refresh interval, during which the records with nonzero timestamp are expected to be refreshed to remain in the zone.</span></span> <span data-ttu-id="ace84-245">重新整理間隔到期尚未重新整理的記錄，可能會由伺服器執行的下一個清除作業移除。</span><span class="sxs-lookup"><span data-stu-id="ace84-245">Records that have not been refreshed by expiration of the Refresh interval could be removed by the next scavenging performed by a server.</span></span> <span data-ttu-id="ace84-246">此值絕不能小於區域中所註冊記錄的最長重新整理時間。</span><span class="sxs-lookup"><span data-stu-id="ace84-246">This value should never be less than the longest refresh period of the records registered in the zone.</span></span> <span data-ttu-id="ace84-247">太小的值可能會導致移除有效的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="ace84-247">Values that are too small may lead to removal of valid DNS records.</span></span> <span data-ttu-id="ace84-248">太大的值會延長過時記錄的存留期。</span><span class="sxs-lookup"><span data-stu-id="ace84-248">values that are too large prolong the lifetime of stale records.</span></span> <span data-ttu-id="ace84-249">此值會設定為建立區域之 DNS 伺服器的 *DefaultRefreshInterval* 屬性。</span><span class="sxs-lookup"><span data-stu-id="ace84-249">This value is set to the *DefaultRefreshInterval* property of the DNS server where the zone is created.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-250">**反向**</span><span class="sxs-lookup"><span data-stu-id="ace84-250">**Reverse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-251">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-253">指出區域是否反向 (TRUE) 或轉寄 (FALSE) 。</span><span class="sxs-lookup"><span data-stu-id="ace84-253">Indicates whether the Zone is reverse (TRUE) or forward (FALSE).</span></span>

</dd> <dt>

<span data-ttu-id="ace84-254">**ScavengeServers**</span><span class="sxs-lookup"><span data-stu-id="ace84-254">**ScavengeServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-255">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ace84-255">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ace84-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-257">列舉 DNS 伺服器 IP 位址清單的字串陣列，這些 IP 位址允許對此區域的過時記錄進行清除。</span><span class="sxs-lookup"><span data-stu-id="ace84-257">Array of strings that enumerates the list of IP addresses of DNS servers that are allowed to perform scavenging of stale records of this zone.</span></span> <span data-ttu-id="ace84-258">如果未指定清單，則在符合其他必要條件時，允許區域的任何主要 DNS 伺服器會清除區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-258">If the list is not specified, any primary DNS server authoritative for the zone is allowed to scavenge the zone when other prerequisites are met.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-259">**SecondaryServers**</span><span class="sxs-lookup"><span data-stu-id="ace84-259">**SecondaryServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-260">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ace84-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ace84-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-262">列舉 DNS 伺服器 IP 位址的字串陣列，這些 IP 位址允許透過區域複寫接收此區域。</span><span class="sxs-lookup"><span data-stu-id="ace84-262">Array of strings enumerating IP addresses of DNS servers allowed to receive this zone through zone replication.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-263">**SecureSecondaries**</span><span class="sxs-lookup"><span data-stu-id="ace84-263">**SecureSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-264">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-266">指出是否只允許區域傳輸給指定的次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="ace84-266">Indicates whether zone transfer is allowed to designated secondaries only.</span></span> <span data-ttu-id="ace84-267">指定的次要複本是 DNS 伺服器，其 IP 位址會列在 SecondariesIPAddressesArray 中。</span><span class="sxs-lookup"><span data-stu-id="ace84-267">Designated secondaries are DNS Servers whose IP addresses are listed in SecondariesIPAddressesArray.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-268">**關機**</span><span class="sxs-lookup"><span data-stu-id="ace84-268">**Shutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-269">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-271">指出區域的複本是否已過期。</span><span class="sxs-lookup"><span data-stu-id="ace84-271">Indicates whether the copy of the Zone is expired.</span></span> <span data-ttu-id="ace84-272">若為 TRUE，則表示區域已過期或已關閉。</span><span class="sxs-lookup"><span data-stu-id="ace84-272">If TRUE, the Zone is expired, or shut down.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-273">**UseNBStat**</span><span class="sxs-lookup"><span data-stu-id="ace84-273">**UseNBStat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-274">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-276">此布林值會指出區域是否使用 NBStat 反向查閱。</span><span class="sxs-lookup"><span data-stu-id="ace84-276">This Boolean indicates whether the Zone uses NBStat reverse lookup.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-277">**UseWins**</span><span class="sxs-lookup"><span data-stu-id="ace84-277">**UseWins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-278">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ace84-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-280">指出區域是否使用 WINS 查閱。</span><span class="sxs-lookup"><span data-stu-id="ace84-280">Indicates whether the Zone uses WINS look up.</span></span>

</dd> <dt>

<span data-ttu-id="ace84-281">**ZoneType**</span><span class="sxs-lookup"><span data-stu-id="ace84-281">**ZoneType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace84-282">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ace84-282">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace84-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ace84-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace84-284">表示區域的類型。</span><span class="sxs-lookup"><span data-stu-id="ace84-284">Indicates the type of the Zone.</span></span> <span data-ttu-id="ace84-285">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ace84-285">Valid values are:</span></span>

-   <span data-ttu-id="ace84-286">DS 整合</span><span class="sxs-lookup"><span data-stu-id="ace84-286">DS integrated</span></span>
-   <span data-ttu-id="ace84-287">Primary</span><span class="sxs-lookup"><span data-stu-id="ace84-287">Primary</span></span>
-   <span data-ttu-id="ace84-288">次要</span><span class="sxs-lookup"><span data-stu-id="ace84-288">Secondary</span></span>

<span data-ttu-id="ace84-289">\* \* Windows Server 2003： \* \*</span><span class="sxs-lookup"><span data-stu-id="ace84-289">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="ace84-290">其他值：</span><span class="sxs-lookup"><span data-stu-id="ace84-290">Additional values:</span></span>

-   <span data-ttu-id="ace84-291">快取</span><span class="sxs-lookup"><span data-stu-id="ace84-291">Cache</span></span>
-   <span data-ttu-id="ace84-292">存根</span><span class="sxs-lookup"><span data-stu-id="ace84-292">Stub</span></span>
-   <span data-ttu-id="ace84-293">轉寄站</span><span class="sxs-lookup"><span data-stu-id="ace84-293">Forwarder</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ace84-294">規格需求</span><span class="sxs-lookup"><span data-stu-id="ace84-294">Requirements</span></span>



| <span data-ttu-id="ace84-295">需求</span><span class="sxs-lookup"><span data-stu-id="ace84-295">Requirement</span></span> | <span data-ttu-id="ace84-296">值</span><span class="sxs-lookup"><span data-stu-id="ace84-296">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ace84-297">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ace84-297">Minimum supported client</span></span><br/> | <span data-ttu-id="ace84-298">都不支援</span><span class="sxs-lookup"><span data-stu-id="ace84-298">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ace84-299">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ace84-299">Minimum supported server</span></span><br/> | <span data-ttu-id="ace84-300">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ace84-300">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ace84-301">命名空間</span><span class="sxs-lookup"><span data-stu-id="ace84-301">Namespace</span></span><br/>                | <span data-ttu-id="ace84-302">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ace84-302">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ace84-303">MOF</span><span class="sxs-lookup"><span data-stu-id="ace84-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ace84-304"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="ace84-304"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ace84-305">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ace84-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace84-306">**MicrosoftDNS \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="ace84-306">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="ace84-307">**MicrosoftDNS 區域類別的 AgeAllRecords 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-307">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="ace84-308">**MicrosoftDNS 區域類別的 ChangeZoneType 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-308">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="ace84-309">**MicrosoftDNS 區域類別的 CreateZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-309">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="ace84-310">**MicrosoftDNS 區域類別的 ForceRefresh 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-310">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="ace84-311">**MicrosoftDNS 區域類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-311">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="ace84-312">**MicrosoftDNS 區域類別的 PauseZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-312">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="ace84-313">**MicrosoftDNS 區域類別的 ReloadZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-313">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="ace84-314">**MicrosoftDNS 區域類別的 ResetSecondaries 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-314">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="ace84-315">**MicrosoftDNS 區域類別的 ResumeZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-315">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="ace84-316">**MicrosoftDNS 區域類別的 UpdateFromDS 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-316">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="ace84-317">**MicrosoftDNS 區域類別的 WriteBackZone 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="ace84-317">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





