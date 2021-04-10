---
title: MicrosoftDNS_WKSType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化 Well-Known 服務 (WKS) 資源記錄。
ms.assetid: 6d910716-74f9-48a0-b43c-3243f5518caf
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_WKSType 類別
- MicrosoftDNS_WKSType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e27b62bd2008c58d283d0e7564fa7821c452cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843863"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="32def-106">MicrosoftDNS WKSType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="32def-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="32def-107">**CreateInstanceFromPropertyData** 方法會具現化 Well-Known 服務 (WKS) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="32def-107">The **CreateInstanceFromPropertyData** method instantiates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="32def-108">語法</span><span class="sxs-lookup"><span data-stu-id="32def-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               InternetAddress,
  [in]           string               IPProtocol,
  [in]           string               Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="32def-109">參數</span><span class="sxs-lookup"><span data-stu-id="32def-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32def-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32def-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32def-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="32def-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="32def-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32def-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32def-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="32def-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="32def-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32def-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32def-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="32def-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="32def-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="32def-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="32def-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="32def-117">Class of the RR.</span></span> <span data-ttu-id="32def-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="32def-118">Default value is 1.</span></span> <span data-ttu-id="32def-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="32def-119">The following values are valid.</span></span>



| <span data-ttu-id="32def-120">值</span><span class="sxs-lookup"><span data-stu-id="32def-120">Value</span></span>                                                                                                | <span data-ttu-id="32def-121">意義</span><span class="sxs-lookup"><span data-stu-id="32def-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="32def-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="32def-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="32def-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="32def-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="32def-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="32def-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="32def-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="32def-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="32def-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="32def-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="32def-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="32def-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="32def-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="32def-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="32def-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="32def-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="32def-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="32def-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="32def-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="32def-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="32def-132">*InternetAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32def-132">*InternetAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32def-133">記錄擁有者的網際網路 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="32def-133">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="32def-134">*IPProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32def-134">*IPProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32def-135">代表此記錄之 IP 通訊協定的字串。</span><span class="sxs-lookup"><span data-stu-id="32def-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="32def-136">有效的值為 UDP 或 TCP。</span><span class="sxs-lookup"><span data-stu-id="32def-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="32def-137">*服務* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32def-137">*Services* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32def-138">字串，其中包含已知服務 (WKS) 記錄所使用的所有服務。</span><span class="sxs-lookup"><span data-stu-id="32def-138">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="32def-139">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="32def-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="32def-140">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="32def-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32def-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="32def-141">Return value</span></span>

<span data-ttu-id="32def-142">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="32def-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="32def-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="32def-143">Requirements</span></span>



| <span data-ttu-id="32def-144">需求</span><span class="sxs-lookup"><span data-stu-id="32def-144">Requirement</span></span> | <span data-ttu-id="32def-145">值</span><span class="sxs-lookup"><span data-stu-id="32def-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32def-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32def-146">Minimum supported client</span></span><br/> | <span data-ttu-id="32def-147">都不支援</span><span class="sxs-lookup"><span data-stu-id="32def-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="32def-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32def-148">Minimum supported server</span></span><br/> | <span data-ttu-id="32def-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32def-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="32def-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="32def-150">Namespace</span></span><br/>                | <span data-ttu-id="32def-151">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="32def-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="32def-152">MOF</span><span class="sxs-lookup"><span data-stu-id="32def-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32def-153"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="32def-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32def-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32def-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32def-155">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="32def-155">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="32def-156">**Modify MicrosoftDNS \_ WKSType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="32def-156">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="32def-157">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="32def-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





