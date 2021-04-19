---
title: MicrosoftDNS_TXTType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化文字 (TXT) 資源記錄。
ms.assetid: f518bb07-e64f-4240-a7b8-9363374b83d6
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_TXTType 類別
- MicrosoftDNS_TXTType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23f9790189ca182cd65d9fe34890c31a90921d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969807"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="ad3d8-106">MicrosoftDNS TXTType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ad3d8-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="ad3d8-107">**CreateInstanceFromPropertyData** 方法會具現化文字 (TXT) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-107">The **CreateInstanceFromPropertyData** method instantiates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad3d8-108">語法</span><span class="sxs-lookup"><span data-stu-id="ad3d8-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ad3d8-109">參數</span><span class="sxs-lookup"><span data-stu-id="ad3d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad3d8-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad3d8-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3d8-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ad3d8-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad3d8-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3d8-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ad3d8-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad3d8-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3d8-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ad3d8-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ad3d8-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3d8-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-117">Class of the RR.</span></span> <span data-ttu-id="ad3d8-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-118">Default value is 1.</span></span> <span data-ttu-id="ad3d8-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-119">The following values are valid.</span></span>



| <span data-ttu-id="ad3d8-120">值</span><span class="sxs-lookup"><span data-stu-id="ad3d8-120">Value</span></span>                                                                                                | <span data-ttu-id="ad3d8-121">意義</span><span class="sxs-lookup"><span data-stu-id="ad3d8-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ad3d8-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ad3d8-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ad3d8-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="ad3d8-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ad3d8-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ad3d8-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ad3d8-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="ad3d8-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ad3d8-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ad3d8-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ad3d8-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="ad3d8-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ad3d8-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ad3d8-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ad3d8-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="ad3d8-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ad3d8-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ad3d8-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3d8-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ad3d8-132">*DescriptiveText* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad3d8-132">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3d8-133">描述性文字，相依于擁有者網域的語法。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-133">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="ad3d8-134">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="ad3d8-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3d8-135">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad3d8-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad3d8-136">Return value</span></span>

<span data-ttu-id="ad3d8-137">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ad3d8-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad3d8-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad3d8-138">Requirements</span></span>



| <span data-ttu-id="ad3d8-139">需求</span><span class="sxs-lookup"><span data-stu-id="ad3d8-139">Requirement</span></span> | <span data-ttu-id="ad3d8-140">值</span><span class="sxs-lookup"><span data-stu-id="ad3d8-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad3d8-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad3d8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ad3d8-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="ad3d8-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ad3d8-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad3d8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ad3d8-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad3d8-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ad3d8-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="ad3d8-145">Namespace</span></span><br/>                | <span data-ttu-id="ad3d8-146">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ad3d8-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ad3d8-147">MOF</span><span class="sxs-lookup"><span data-stu-id="ad3d8-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad3d8-148"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad3d8-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad3d8-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad3d8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad3d8-150">**MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="ad3d8-150">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="ad3d8-151">**Modify MicrosoftDNS \_ TXTType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="ad3d8-151">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="ad3d8-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ad3d8-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





