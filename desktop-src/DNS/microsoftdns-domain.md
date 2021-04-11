---
title: MicrosoftDNS_Domain 類別
description: MicrosoftDNS \_ 網域類別代表 DNS 階層中的網域。
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- MicrosoftDNS_Domain 類別 DNS
- MicrosoftDNS_Domain 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103709"
---
# <a name="microsoftdns_domain-class"></a><span data-ttu-id="8b472-105">MicrosoftDNS \_ 網域類別</span><span class="sxs-lookup"><span data-stu-id="8b472-105">MicrosoftDNS\_Domain class</span></span>

<span data-ttu-id="8b472-106">**MicrosoftDNS \_ 網域** 類別代表 DNS 階層中的網域。</span><span class="sxs-lookup"><span data-stu-id="8b472-106">The **MicrosoftDNS\_Domain** class represents a Domain in a DNS hierarchy.</span></span>

<span data-ttu-id="8b472-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="8b472-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b472-108">語法</span><span class="sxs-lookup"><span data-stu-id="8b472-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="8b472-109">成員</span><span class="sxs-lookup"><span data-stu-id="8b472-109">Members</span></span>

<span data-ttu-id="8b472-110">**MicrosoftDNS \_ 網域** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8b472-110">The **MicrosoftDNS\_Domain** class has these types of members:</span></span>

-   [<span data-ttu-id="8b472-111">方法</span><span class="sxs-lookup"><span data-stu-id="8b472-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8b472-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8b472-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8b472-113">方法</span><span class="sxs-lookup"><span data-stu-id="8b472-113">Methods</span></span>

<span data-ttu-id="8b472-114">**MicrosoftDNS \_ 網域** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8b472-114">The **MicrosoftDNS\_Domain** class has these methods.</span></span>



| <span data-ttu-id="8b472-115">方法</span><span class="sxs-lookup"><span data-stu-id="8b472-115">Method</span></span>                   | <span data-ttu-id="8b472-116">描述</span><span class="sxs-lookup"><span data-stu-id="8b472-116">Description</span></span>                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b472-117">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="8b472-117">**GetDistinguishedName**</span></span> | <span data-ttu-id="8b472-118">取得區域的 DS 分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="8b472-118">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="8b472-119">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="8b472-119">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8b472-120">屬性</span><span class="sxs-lookup"><span data-stu-id="8b472-120">Properties</span></span>

<span data-ttu-id="8b472-121">**MicrosoftDNS \_ 網域** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8b472-121">The **MicrosoftDNS\_Domain** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b472-122">**容器**</span><span class="sxs-lookup"><span data-stu-id="8b472-122">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b472-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8b472-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b472-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b472-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b472-125">網域的容器名稱，可能是區域、快取或 RootHints。</span><span class="sxs-lookup"><span data-stu-id="8b472-125">Name of the container of the domain, which could be a Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="8b472-126">如果容器是 ([**MicrosoftDNS \_ 區域**](microsoftdns-zone.md) 類別實例的區域) ，此屬性就會包含區域的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8b472-126">In cases where the Container is a Zone (an instance of the [**MicrosoftDNS\_Zone**](microsoftdns-zone.md) class), this property contains the FQDN of the Zone.</span></span>

<span data-ttu-id="8b472-127">如果容器是根區域，則 \\ 應使用字串。 \\</span><span class="sxs-lookup"><span data-stu-id="8b472-127">When the Container is the root zone, the string \\.\\ should be used.</span></span>

<span data-ttu-id="8b472-128">如果容器是資源記錄的 DNS 快取 ([**MicrosoftDNS \_ cache**](microsoftdns-cache.md) 類別的實例) ，這個屬性會設定 \\ 為字串。快取 \\ 。</span><span class="sxs-lookup"><span data-stu-id="8b472-128">In cases where the Container is the DNS cache of resource records (an instance of the [**MicrosoftDNS\_Cache**](microsoftdns-cache.md) class), this property is set to the string \\..Cache\\.</span></span>

<span data-ttu-id="8b472-129">如果 RootHints 容器 ([**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)) 類別的實例，則此屬性應該設定為 \\ 。RootHints \\ 。</span><span class="sxs-lookup"><span data-stu-id="8b472-129">If the Container is RootHints (an instance of the [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md) class), this property should be set to \\..RootHints\\.</span></span>

</dd> <dt>

<span data-ttu-id="8b472-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="8b472-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b472-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8b472-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b472-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b472-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b472-133">包含網域之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8b472-133">FQDN or IP address of the DNS Server that contains the domain.</span></span>

</dd> <dt>

<span data-ttu-id="8b472-134">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8b472-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b472-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8b472-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b472-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b472-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b472-137">網域的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8b472-137">FQDN of the domain.</span></span>

<span data-ttu-id="8b472-138">若為 DNS 快取或 RootHints 的實例，則為字串 \\ 。快取 \\ 和 \\ .。。\\ 應分別使用 RootHints。</span><span class="sxs-lookup"><span data-stu-id="8b472-138">For instances of DNS Cache or RootHints, the strings \\..Cache\\ and \\..RootHints\\ should be used, respectively.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b472-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b472-139">Requirements</span></span>



| <span data-ttu-id="8b472-140">需求</span><span class="sxs-lookup"><span data-stu-id="8b472-140">Requirement</span></span> | <span data-ttu-id="8b472-141">值</span><span class="sxs-lookup"><span data-stu-id="8b472-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b472-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b472-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8b472-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="8b472-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8b472-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b472-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8b472-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b472-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8b472-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="8b472-146">Namespace</span></span><br/>                | <span data-ttu-id="8b472-147">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8b472-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8b472-148">MOF</span><span class="sxs-lookup"><span data-stu-id="8b472-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b472-149"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b472-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b472-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b472-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b472-151">**MicrosoftDNS 網域類別的 GetDistinguishedName 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="8b472-151">**GetDistinguishedName Method of the MicrosoftDNS\_Domain Class**</span></span>](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





