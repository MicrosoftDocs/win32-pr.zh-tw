---
title: MicrosoftDNS_ResourceRecord 類別
description: MicrosoftDNS \_ ResourceRecord 類別代表 DNS RR 的一般屬性。以下是從 MOF 程式碼簡化的語法。
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- MicrosoftDNS_ResourceRecord 類別 DNS
- MicrosoftDNS_ResourceRecord 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934530"
---
# <a name="microsoftdns_resourcerecord-class"></a><span data-ttu-id="6c99b-105">MicrosoftDNS \_ ResourceRecord 類別</span><span class="sxs-lookup"><span data-stu-id="6c99b-105">MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="6c99b-106">**MicrosoftDNS \_ ResourceRecord** 類別代表 DNS RR 的一般屬性。</span><span class="sxs-lookup"><span data-stu-id="6c99b-106">The **MicrosoftDNS\_ResourceRecord** class represents the general properties of a DNS RR.</span></span>

<span data-ttu-id="6c99b-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="6c99b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c99b-108">語法</span><span class="sxs-lookup"><span data-stu-id="6c99b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a><span data-ttu-id="6c99b-109">成員</span><span class="sxs-lookup"><span data-stu-id="6c99b-109">Members</span></span>

<span data-ttu-id="6c99b-110">**MicrosoftDNS \_ ResourceRecord** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6c99b-110">The **MicrosoftDNS\_ResourceRecord** class has these types of members:</span></span>

-   [<span data-ttu-id="6c99b-111">方法</span><span class="sxs-lookup"><span data-stu-id="6c99b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6c99b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="6c99b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6c99b-113">方法</span><span class="sxs-lookup"><span data-stu-id="6c99b-113">Methods</span></span>

<span data-ttu-id="6c99b-114">**MicrosoftDNS \_ ResourceRecord** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6c99b-114">The **MicrosoftDNS\_ResourceRecord** class has these methods.</span></span>



| <span data-ttu-id="6c99b-115">方法</span><span class="sxs-lookup"><span data-stu-id="6c99b-115">Method</span></span>                                   | <span data-ttu-id="6c99b-116">描述</span><span class="sxs-lookup"><span data-stu-id="6c99b-116">Description</span></span>                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c99b-117">**CreateInstanceFromTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="6c99b-117">**CreateInstanceFromTextRepresentation**</span></span> | <span data-ttu-id="6c99b-118">剖析 TextRepresentation 字串中的 RR，以及輸入 DNS 伺服器和容器名稱、定義和具現化 ResourceRecord 物件。</span><span class="sxs-lookup"><span data-stu-id="6c99b-118">Parses the RR in the TextRepresentation string, and with the input DNS Server and Container Names, defines, and instantiates a ResourceRecord object.</span></span> <span data-ttu-id="6c99b-119">方法會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="6c99b-119">The method returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="6c99b-120">限定詞︰無</span><span class="sxs-lookup"><span data-stu-id="6c99b-120">Qualifiers: None</span></span><br/> |
| <span data-ttu-id="6c99b-121">**GetObjectByTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="6c99b-121">**GetObjectByTextRepresentation**</span></span>        | <span data-ttu-id="6c99b-122">抓取 MicrosoftDns ResourceRecord 子類別的現有實例 \_ ，並以 TextRepresentation 字串和 DNS 伺服器和容器名稱表示。</span><span class="sxs-lookup"><span data-stu-id="6c99b-122">Retrieves an existing instance of the MicrosoftDns\_ResourceRecord subclass, represented by the TextRepresentation string along with the DNS Server and Container Name.</span></span> <br/> <span data-ttu-id="6c99b-123">限定詞︰無</span><span class="sxs-lookup"><span data-stu-id="6c99b-123">Qualifiers: None</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="6c99b-124">屬性</span><span class="sxs-lookup"><span data-stu-id="6c99b-124">Properties</span></span>

<span data-ttu-id="6c99b-125">**MicrosoftDNS \_ ResourceRecord** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6c99b-125">The **MicrosoftDNS\_ResourceRecord** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c99b-126">**容器**</span><span class="sxs-lookup"><span data-stu-id="6c99b-126">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c99b-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c99b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c99b-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c99b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c99b-129">指出包含 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="6c99b-129">Indicates the name of the Container for the Zone, Cache, or RootHints instance that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="6c99b-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="6c99b-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c99b-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c99b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c99b-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c99b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c99b-133">指出包含 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6c99b-133">Indicates the FQDN or IP address of the DNS Server that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="6c99b-134">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="6c99b-134">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c99b-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c99b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c99b-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c99b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c99b-137">代表包含 RR 之網域的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6c99b-137">Represents the FQDN of the Domain that contains the RR.</span></span> <span data-ttu-id="6c99b-138">這個屬性可能包含字串 \\ 。Cache \\ 或 \\ .。。RootHints \\ ，如果內部快取或 RootHints 分別包含 RR。</span><span class="sxs-lookup"><span data-stu-id="6c99b-138">This property may contain the strings \\..Cache\\ or \\..RootHints\\ if the internal cache or RootHints contain the RR, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="6c99b-139">**OwnerName**</span><span class="sxs-lookup"><span data-stu-id="6c99b-139">**OwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c99b-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c99b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c99b-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c99b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c99b-142">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="6c99b-142">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="6c99b-143">**RecordClass = 1**</span><span class="sxs-lookup"><span data-stu-id="6c99b-143">**RecordClass=1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c99b-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6c99b-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c99b-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c99b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c99b-146">\* \* Windows Server 2003： \* \*</span><span class="sxs-lookup"><span data-stu-id="6c99b-146">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="6c99b-147">這個字串代表資源記錄的類別。</span><span class="sxs-lookup"><span data-stu-id="6c99b-147">This string represents the class of the Resource Record.</span></span> <span data-ttu-id="6c99b-148">有效值包括：</span><span class="sxs-lookup"><span data-stu-id="6c99b-148">Valid values include:</span></span>

<span data-ttu-id="6c99b-149">1：在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="6c99b-149">1: IN (Internet)</span></span>

<span data-ttu-id="6c99b-150">2： CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="6c99b-150">2: CS (CSNET)</span></span>

<span data-ttu-id="6c99b-151">3： CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="6c99b-151">3: CH (CHAOS)</span></span>

<span data-ttu-id="6c99b-152">4： HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="6c99b-152">4: HS (Hesiod)</span></span>

</dd> <dt>

<span data-ttu-id="6c99b-153">**RecordData**</span><span class="sxs-lookup"><span data-stu-id="6c99b-153">**RecordData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c99b-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c99b-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c99b-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c99b-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c99b-156">資源記錄資料。</span><span class="sxs-lookup"><span data-stu-id="6c99b-156">Resource record data.</span></span>

</dd> <dt>

<span data-ttu-id="6c99b-157">**TextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="6c99b-157">**TextRepresentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c99b-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c99b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c99b-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c99b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c99b-160">整個 RR 的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="6c99b-160">Text representation of the entire RR.</span></span>

</dd> <dt>

<span data-ttu-id="6c99b-161">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="6c99b-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c99b-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6c99b-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c99b-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c99b-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c99b-164">上次重新整理 RR 的時間，以1601年1月1日起的經過時程表示，格林尼治平均時間 (GMT) 。</span><span class="sxs-lookup"><span data-stu-id="6c99b-164">Time at which the RR was last refreshed, expressed in elapsed hours since January 1, 1601, Greenwich Mean Time (GMT).</span></span>

</dd> <dt>

<span data-ttu-id="6c99b-165">**Ttl**</span><span class="sxs-lookup"><span data-stu-id="6c99b-165">**TTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c99b-166">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6c99b-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c99b-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c99b-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c99b-168">DNS [*解析程式*](r-gly.md)可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6c99b-168">Time, in seconds, that the RR can be cached by a DNS [*resolver*](r-gly.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c99b-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c99b-169">Requirements</span></span>



| <span data-ttu-id="6c99b-170">需求</span><span class="sxs-lookup"><span data-stu-id="6c99b-170">Requirement</span></span> | <span data-ttu-id="6c99b-171">值</span><span class="sxs-lookup"><span data-stu-id="6c99b-171">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c99b-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c99b-172">Minimum supported client</span></span><br/> | <span data-ttu-id="6c99b-173">都不支援</span><span class="sxs-lookup"><span data-stu-id="6c99b-173">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6c99b-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c99b-174">Minimum supported server</span></span><br/> | <span data-ttu-id="6c99b-175">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c99b-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6c99b-176">命名空間</span><span class="sxs-lookup"><span data-stu-id="6c99b-176">Namespace</span></span><br/>                | <span data-ttu-id="6c99b-177">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="6c99b-177">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6c99b-178">MOF</span><span class="sxs-lookup"><span data-stu-id="6c99b-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c99b-179"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c99b-179"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c99b-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c99b-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c99b-181">**MicrosoftDNS ResourceRecord 類別的 CreateInstanceFromTextRepresentation 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="6c99b-181">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[<span data-ttu-id="6c99b-182">**MicrosoftDNS ResourceRecord 類別的 GetObjectByTextRepresentation 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="6c99b-182">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





