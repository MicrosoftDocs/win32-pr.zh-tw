---
title: MicrosoftDNS_MFType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化網域 (MF) 資源記錄的郵件轉送代理程式。
ms.assetid: e669d065-bfba-4a86-8519-2317e03ed4ee
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_MFType 類別
- MicrosoftDNS_MFType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26cafc766a6ea6419432b279f5389721f6572b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934352"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="48246-106">MicrosoftDNS MFType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="48246-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="48246-107">**CreateInstanceFromPropertyData** 方法會具現化網域 (MF) 資源記錄的郵件轉送代理程式。</span><span class="sxs-lookup"><span data-stu-id="48246-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="48246-108">語法</span><span class="sxs-lookup"><span data-stu-id="48246-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="48246-109">參數</span><span class="sxs-lookup"><span data-stu-id="48246-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48246-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48246-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48246-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="48246-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="48246-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48246-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48246-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="48246-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="48246-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48246-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48246-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="48246-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="48246-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="48246-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48246-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="48246-117">Class of the RR.</span></span> <span data-ttu-id="48246-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="48246-118">Default value is 1.</span></span> <span data-ttu-id="48246-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="48246-119">The following values are valid.</span></span>



| <span data-ttu-id="48246-120">值</span><span class="sxs-lookup"><span data-stu-id="48246-120">Value</span></span>                                                                                                | <span data-ttu-id="48246-121">意義</span><span class="sxs-lookup"><span data-stu-id="48246-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="48246-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="48246-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="48246-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="48246-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="48246-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="48246-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="48246-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="48246-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="48246-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="48246-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="48246-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="48246-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="48246-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="48246-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="48246-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="48246-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="48246-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="48246-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48246-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="48246-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="48246-132">*MFHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48246-132">*MFHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48246-133">提供郵件轉送代理程式的主控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="48246-133">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="48246-134">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="48246-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="48246-135">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="48246-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48246-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="48246-136">Return value</span></span>

<span data-ttu-id="48246-137">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="48246-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="48246-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="48246-138">Requirements</span></span>



| <span data-ttu-id="48246-139">需求</span><span class="sxs-lookup"><span data-stu-id="48246-139">Requirement</span></span> | <span data-ttu-id="48246-140">值</span><span class="sxs-lookup"><span data-stu-id="48246-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48246-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48246-141">Minimum supported client</span></span><br/> | <span data-ttu-id="48246-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="48246-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="48246-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48246-143">Minimum supported server</span></span><br/> | <span data-ttu-id="48246-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48246-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="48246-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="48246-145">Namespace</span></span><br/>                | <span data-ttu-id="48246-146">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="48246-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="48246-147">MOF</span><span class="sxs-lookup"><span data-stu-id="48246-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48246-148"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="48246-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48246-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48246-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48246-150">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="48246-150">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="48246-151">**Modify MicrosoftDNS \_ MFType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="48246-151">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="48246-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="48246-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





