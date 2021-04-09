---
title: MicrosoftDNS_SRVType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會將服務 (SRV) 資源記錄具現化。
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_SRVType 類別
- MicrosoftDNS_SRVType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 607ed606bf12e9e2a6f90a6e7f309aa708b7f230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686378"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="745c9-106">MicrosoftDNS SRVType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="745c9-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="745c9-107">**CreateInstanceFromPropertyData** 方法會將服務 (SRV) 資源記錄具現化。</span><span class="sxs-lookup"><span data-stu-id="745c9-107">The **CreateInstanceFromPropertyData** method instantiates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="745c9-108">語法</span><span class="sxs-lookup"><span data-stu-id="745c9-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="745c9-109">參數</span><span class="sxs-lookup"><span data-stu-id="745c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="745c9-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745c9-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="745c9-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="745c9-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745c9-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="745c9-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="745c9-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745c9-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="745c9-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="745c9-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="745c9-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="745c9-117">Class of the RR.</span></span> <span data-ttu-id="745c9-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="745c9-118">Default value is 1.</span></span> <span data-ttu-id="745c9-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="745c9-119">The following values are valid.</span></span>



| <span data-ttu-id="745c9-120">值</span><span class="sxs-lookup"><span data-stu-id="745c9-120">Value</span></span>                                                                                                | <span data-ttu-id="745c9-121">意義</span><span class="sxs-lookup"><span data-stu-id="745c9-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="745c9-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="745c9-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="745c9-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="745c9-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="745c9-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="745c9-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="745c9-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="745c9-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="745c9-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="745c9-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="745c9-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="745c9-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="745c9-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="745c9-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="745c9-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="745c9-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="745c9-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="745c9-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="745c9-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="745c9-132">*優先順序* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745c9-132">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-133">擁有者名稱中指定的目標主機優先權。</span><span class="sxs-lookup"><span data-stu-id="745c9-133">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="745c9-134">數位下限表示較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="745c9-134">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="745c9-135">*權數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745c9-135">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-136">目標主機的加權。</span><span class="sxs-lookup"><span data-stu-id="745c9-136">Weight of the target host.</span></span> <span data-ttu-id="745c9-137">在具有相同優先順序的主機之間進行選取時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="745c9-137">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="745c9-138">使用此主機的機率應與其權數成正比。</span><span class="sxs-lookup"><span data-stu-id="745c9-138">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="745c9-139">*埠* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745c9-139">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-140">通訊協定服務的目標主機上所使用的埠。</span><span class="sxs-lookup"><span data-stu-id="745c9-140">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="745c9-141">*SRVDomainName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745c9-141">*SRVDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-142">目標主機的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="745c9-142">FQDN of the target host.</span></span> <span data-ttu-id="745c9-143">的目標 \\ 。 \\ 表示此網域無法使用由於原子服務。</span><span class="sxs-lookup"><span data-stu-id="745c9-143">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="745c9-144">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="745c9-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="745c9-145">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="745c9-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="745c9-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="745c9-146">Return value</span></span>

<span data-ttu-id="745c9-147">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="745c9-147">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="745c9-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="745c9-148">Requirements</span></span>



| <span data-ttu-id="745c9-149">需求</span><span class="sxs-lookup"><span data-stu-id="745c9-149">Requirement</span></span> | <span data-ttu-id="745c9-150">值</span><span class="sxs-lookup"><span data-stu-id="745c9-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="745c9-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="745c9-151">Minimum supported client</span></span><br/> | <span data-ttu-id="745c9-152">都不支援</span><span class="sxs-lookup"><span data-stu-id="745c9-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="745c9-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="745c9-153">Minimum supported server</span></span><br/> | <span data-ttu-id="745c9-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="745c9-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="745c9-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="745c9-155">Namespace</span></span><br/>                | <span data-ttu-id="745c9-156">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="745c9-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="745c9-157">MOF</span><span class="sxs-lookup"><span data-stu-id="745c9-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="745c9-158"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="745c9-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="745c9-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="745c9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="745c9-160">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="745c9-160">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="745c9-161">**Modify MicrosoftDNS \_ SRVType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="745c9-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="745c9-162">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="745c9-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





