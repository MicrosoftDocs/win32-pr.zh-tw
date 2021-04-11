---
title: MicrosoftDNS_RPType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化負責任人員 (RP) 資源記錄。
ms.assetid: 6d9366c3-fc82-4c1f-8fa3-c107f6a1ff74
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_RPType 類別
- MicrosoftDNS_RPType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c150a8a91a7a94fbea8492faea08b61d437a4c9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187288"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="640c1-106">MicrosoftDNS RPType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="640c1-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="640c1-107">**CreateInstanceFromPropertyData** 方法會具現化負責任人員 (RP) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="640c1-107">The **CreateInstanceFromPropertyData** method instantiates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="640c1-108">語法</span><span class="sxs-lookup"><span data-stu-id="640c1-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              RPMailbox,
  [in]           string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="640c1-109">參數</span><span class="sxs-lookup"><span data-stu-id="640c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="640c1-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="640c1-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640c1-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="640c1-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="640c1-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="640c1-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640c1-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="640c1-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="640c1-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="640c1-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640c1-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="640c1-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="640c1-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="640c1-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="640c1-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="640c1-117">Class of the RR.</span></span> <span data-ttu-id="640c1-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="640c1-118">Default value is 1.</span></span> <span data-ttu-id="640c1-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="640c1-119">The following values are valid.</span></span>



| <span data-ttu-id="640c1-120">值</span><span class="sxs-lookup"><span data-stu-id="640c1-120">Value</span></span>                                                                                                | <span data-ttu-id="640c1-121">意義</span><span class="sxs-lookup"><span data-stu-id="640c1-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="640c1-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="640c1-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="640c1-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="640c1-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="640c1-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="640c1-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="640c1-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="640c1-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="640c1-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="640c1-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="640c1-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="640c1-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="640c1-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="640c1-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="640c1-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="640c1-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="640c1-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="640c1-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="640c1-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="640c1-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="640c1-132">*RPMailbox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="640c1-132">*RPMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640c1-133">指定負責任人員信箱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="640c1-133">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="640c1-134">*TXTDomainName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="640c1-134">*TXTDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="640c1-135">存在 TXT 資源記錄的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="640c1-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="640c1-136">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="640c1-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="640c1-137">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="640c1-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="640c1-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="640c1-138">Return value</span></span>

<span data-ttu-id="640c1-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="640c1-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="640c1-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="640c1-140">Requirements</span></span>



| <span data-ttu-id="640c1-141">需求</span><span class="sxs-lookup"><span data-stu-id="640c1-141">Requirement</span></span> | <span data-ttu-id="640c1-142">值</span><span class="sxs-lookup"><span data-stu-id="640c1-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="640c1-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="640c1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="640c1-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="640c1-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="640c1-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="640c1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="640c1-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="640c1-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="640c1-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="640c1-147">Namespace</span></span><br/>                | <span data-ttu-id="640c1-148">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="640c1-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="640c1-149">MOF</span><span class="sxs-lookup"><span data-stu-id="640c1-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="640c1-150"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="640c1-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="640c1-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="640c1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640c1-152">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="640c1-152">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="640c1-153">**Modify MicrosoftDNS \_ RPType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="640c1-153">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="640c1-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="640c1-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





