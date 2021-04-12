---
title: MicrosoftDNS_NSType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化名稱伺服器 (NS) 資源記錄。
ms.assetid: f2399a9d-840d-4392-86c4-610894e60f8e
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_NSType 類別
- MicrosoftDNS_NSType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37b21323da53c592375a00be9303c321d270f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508575"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nstype-class"></a><span data-ttu-id="87913-106">MicrosoftDNS NSType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="87913-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="87913-107">**CreateInstanceFromPropertyData** 方法會具現化名稱伺服器 (NS) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="87913-107">The **CreateInstanceFromPropertyData** method instantiates a Name Server (NS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="87913-108">語法</span><span class="sxs-lookup"><span data-stu-id="87913-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="87913-109">參數</span><span class="sxs-lookup"><span data-stu-id="87913-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87913-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87913-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87913-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="87913-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="87913-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87913-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87913-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="87913-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="87913-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87913-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87913-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="87913-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="87913-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="87913-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87913-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="87913-117">Class of the RR.</span></span> <span data-ttu-id="87913-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="87913-118">Default value is 1.</span></span> <span data-ttu-id="87913-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="87913-119">The following values are valid.</span></span>



| <span data-ttu-id="87913-120">值</span><span class="sxs-lookup"><span data-stu-id="87913-120">Value</span></span>                                                                                                | <span data-ttu-id="87913-121">意義</span><span class="sxs-lookup"><span data-stu-id="87913-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="87913-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="87913-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="87913-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="87913-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="87913-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="87913-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="87913-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="87913-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="87913-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="87913-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="87913-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="87913-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="87913-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="87913-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="87913-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="87913-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="87913-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="87913-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87913-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="87913-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="87913-132">*NSHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87913-132">*NSHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87913-133">網域的授權主機。</span><span class="sxs-lookup"><span data-stu-id="87913-133">Authoritative host for the domain.</span></span>

</dd> <dt>

<span data-ttu-id="87913-134">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="87913-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="87913-135">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="87913-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87913-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="87913-136">Return value</span></span>

<span data-ttu-id="87913-137">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="87913-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="87913-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="87913-138">Requirements</span></span>



| <span data-ttu-id="87913-139">需求</span><span class="sxs-lookup"><span data-stu-id="87913-139">Requirement</span></span> | <span data-ttu-id="87913-140">值</span><span class="sxs-lookup"><span data-stu-id="87913-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87913-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87913-141">Minimum supported client</span></span><br/> | <span data-ttu-id="87913-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="87913-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="87913-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87913-143">Minimum supported server</span></span><br/> | <span data-ttu-id="87913-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87913-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="87913-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="87913-145">Namespace</span></span><br/>                | <span data-ttu-id="87913-146">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="87913-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="87913-147">MOF</span><span class="sxs-lookup"><span data-stu-id="87913-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87913-148"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="87913-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87913-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87913-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87913-150">**MicrosoftDNS \_ NSType**</span><span class="sxs-lookup"><span data-stu-id="87913-150">**MicrosoftDNS\_NSType**</span></span>](microsoftdns-nstype.md)
</dt> <dt>

[<span data-ttu-id="87913-151">**Modify MicrosoftDNS \_ NSType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="87913-151">**Modify Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-modify.md)
</dt> <dt>

[<span data-ttu-id="87913-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="87913-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





