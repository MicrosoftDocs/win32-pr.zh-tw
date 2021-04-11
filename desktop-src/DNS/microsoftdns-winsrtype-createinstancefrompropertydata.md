---
title: MicrosoftDNS_WINSRType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化 WINS 反向對應 (WINSR) 資源記錄。
ms.assetid: e14e81be-fc5c-4a6f-b6d1-cb3ce5005e00
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_WINSRType 類別
- MicrosoftDNS_WINSRType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c35863e00ace6c0772383604d0fbdfd7915cd02c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104730"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="8ea49-106">MicrosoftDNS WINSRType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8ea49-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="8ea49-107">**CreateInstanceFromPropertyData** 方法會具現化 WINS 反向對應 (WINSR) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="8ea49-107">The **CreateInstanceFromPropertyData** method instantiates a WINS Reverse Lookup (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea49-108">語法</span><span class="sxs-lookup"><span data-stu-id="8ea49-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint32                 MappingFlag,
  [in]           uint32                 LookupTimeout,
  [in]           uint32                 CacheTimeout,
  [in]           string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8ea49-109">參數</span><span class="sxs-lookup"><span data-stu-id="8ea49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea49-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8ea49-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8ea49-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="8ea49-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8ea49-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="8ea49-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8ea49-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="8ea49-117">Class of the RR.</span></span> <span data-ttu-id="8ea49-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="8ea49-118">Default value is 1.</span></span> <span data-ttu-id="8ea49-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="8ea49-119">The following values are valid.</span></span>



| <span data-ttu-id="8ea49-120">值</span><span class="sxs-lookup"><span data-stu-id="8ea49-120">Value</span></span>                                                                                                | <span data-ttu-id="8ea49-121">意義</span><span class="sxs-lookup"><span data-stu-id="8ea49-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8ea49-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8ea49-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8ea49-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="8ea49-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8ea49-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8ea49-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8ea49-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="8ea49-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8ea49-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8ea49-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8ea49-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="8ea49-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8ea49-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8ea49-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8ea49-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="8ea49-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8ea49-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8ea49-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8ea49-132">*MappingFlag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-133">WINSR 對應旗標，指定是否必須將記錄包含在區域複寫中。</span><span class="sxs-lookup"><span data-stu-id="8ea49-133">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="8ea49-134">它只能有兩個值：對應于複寫的0x80000000 和0x00010000，以及) 旗標的 (本機記錄。</span><span class="sxs-lookup"><span data-stu-id="8ea49-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="8ea49-135">*LookupTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-135">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-136">使用 WINS 反向查閱之 DNS 伺服器的超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8ea49-136">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="8ea49-137">*CacheTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-137">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-138">使用 WINS 查詢的 DNS 伺服器可能會快取 WINS 伺服器的回應時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8ea49-138">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="8ea49-139">*ResultDomain* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-139">*ResultDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-140">要附加至所傳回 NetBIOS 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="8ea49-140">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="8ea49-141">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-141">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea49-142">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="8ea49-142">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea49-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ea49-143">Return value</span></span>

<span data-ttu-id="8ea49-144">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8ea49-144">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ea49-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ea49-145">Requirements</span></span>



| <span data-ttu-id="8ea49-146">需求</span><span class="sxs-lookup"><span data-stu-id="8ea49-146">Requirement</span></span> | <span data-ttu-id="8ea49-147">值</span><span class="sxs-lookup"><span data-stu-id="8ea49-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea49-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ea49-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea49-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="8ea49-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8ea49-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ea49-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea49-151">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ea49-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8ea49-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="8ea49-152">Namespace</span></span><br/>                | <span data-ttu-id="8ea49-153">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8ea49-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8ea49-154">MOF</span><span class="sxs-lookup"><span data-stu-id="8ea49-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ea49-155"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ea49-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ea49-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ea49-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea49-157">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="8ea49-157">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="8ea49-158">**Modify MicrosoftDNS \_ WINSRType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="8ea49-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="8ea49-159">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8ea49-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





