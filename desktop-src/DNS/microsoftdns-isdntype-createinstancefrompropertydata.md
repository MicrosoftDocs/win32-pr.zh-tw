---
title: MicrosoftDNS_ISDNType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化 ISDN 資源記錄。
ms.assetid: cd3b98e3-a804-473e-8831-5f045d43a54f
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_ISDNType 類別
- MicrosoftDNS_ISDNType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f6adaaf374cac56d7d29d04d83c8765b0080ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508895"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="edb2e-106">MicrosoftDNS ISDNType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="edb2e-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="edb2e-107">**CreateInstanceFromPropertyData** 方法會具現化 ISDN 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="edb2e-107">The **CreateInstanceFromPropertyData** method instantiates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb2e-108">語法</span><span class="sxs-lookup"><span data-stu-id="edb2e-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                ISDNNumber,
  [in]           string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="edb2e-109">參數</span><span class="sxs-lookup"><span data-stu-id="edb2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb2e-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edb2e-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb2e-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="edb2e-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="edb2e-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edb2e-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb2e-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="edb2e-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="edb2e-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edb2e-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb2e-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="edb2e-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="edb2e-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="edb2e-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edb2e-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="edb2e-117">Class of the RR.</span></span> <span data-ttu-id="edb2e-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="edb2e-118">Default value is 1.</span></span> <span data-ttu-id="edb2e-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="edb2e-119">The following values are valid.</span></span>



| <span data-ttu-id="edb2e-120">值</span><span class="sxs-lookup"><span data-stu-id="edb2e-120">Value</span></span>                                                                                                | <span data-ttu-id="edb2e-121">意義</span><span class="sxs-lookup"><span data-stu-id="edb2e-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="edb2e-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="edb2e-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="edb2e-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="edb2e-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="edb2e-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="edb2e-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="edb2e-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="edb2e-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="edb2e-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="edb2e-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="edb2e-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="edb2e-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="edb2e-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="edb2e-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="edb2e-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="edb2e-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="edb2e-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="edb2e-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edb2e-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="edb2e-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="edb2e-132">*ISDNNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edb2e-132">*ISDNNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb2e-133">記錄擁有者的 ISDN 號碼和 DDI。</span><span class="sxs-lookup"><span data-stu-id="edb2e-133">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="edb2e-134">子 *位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edb2e-134">*SubAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb2e-135">擁有者的子位址（若已定義）。</span><span class="sxs-lookup"><span data-stu-id="edb2e-135">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="edb2e-136">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="edb2e-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="edb2e-137">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="edb2e-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb2e-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="edb2e-138">Return value</span></span>

<span data-ttu-id="edb2e-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="edb2e-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb2e-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="edb2e-140">Requirements</span></span>



| <span data-ttu-id="edb2e-141">需求</span><span class="sxs-lookup"><span data-stu-id="edb2e-141">Requirement</span></span> | <span data-ttu-id="edb2e-142">值</span><span class="sxs-lookup"><span data-stu-id="edb2e-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edb2e-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edb2e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="edb2e-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="edb2e-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="edb2e-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edb2e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="edb2e-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edb2e-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="edb2e-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="edb2e-147">Namespace</span></span><br/>                | <span data-ttu-id="edb2e-148">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="edb2e-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="edb2e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="edb2e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edb2e-150"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="edb2e-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb2e-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edb2e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb2e-152">**MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="edb2e-152">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="edb2e-153">**Modify MicrosoftDNS \_ ISDNType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="edb2e-153">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="edb2e-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="edb2e-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





