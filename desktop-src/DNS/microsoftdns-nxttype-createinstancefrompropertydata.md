---
title: MicrosoftDNS_NXTType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化下一個 (NXT) 資源記錄。
ms.assetid: d0e4f3bf-f835-4341-a614-539975e6be11
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_NXTType 類別
- MicrosoftDNS_NXTType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee00cd0afdb6ac629a981dbdb586a30252eac1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465845"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="a37a5-106">MicrosoftDNS NXTType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a37a5-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="a37a5-107">**CreateInstanceFromPropertyData** 方法會具現化下一個 (NXT) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="a37a5-107">The **CreateInstanceFromPropertyData** method instantiates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a37a5-108">語法</span><span class="sxs-lookup"><span data-stu-id="a37a5-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a37a5-109">參數</span><span class="sxs-lookup"><span data-stu-id="a37a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a37a5-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a37a5-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37a5-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a37a5-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a37a5-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a37a5-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37a5-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="a37a5-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a37a5-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a37a5-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37a5-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="a37a5-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="a37a5-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a37a5-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a37a5-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="a37a5-117">Class of the RR.</span></span> <span data-ttu-id="a37a5-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="a37a5-118">Default value is 1.</span></span> <span data-ttu-id="a37a5-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="a37a5-119">The following values are valid.</span></span>



| <span data-ttu-id="a37a5-120">值</span><span class="sxs-lookup"><span data-stu-id="a37a5-120">Value</span></span>                                                                                                | <span data-ttu-id="a37a5-121">意義</span><span class="sxs-lookup"><span data-stu-id="a37a5-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a37a5-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a37a5-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a37a5-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="a37a5-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="a37a5-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a37a5-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a37a5-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="a37a5-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="a37a5-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="a37a5-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="a37a5-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="a37a5-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="a37a5-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="a37a5-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="a37a5-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="a37a5-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a37a5-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a37a5-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a37a5-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a37a5-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a37a5-132">*NextDomainName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a37a5-132">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37a5-133">下一個功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="a37a5-133">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="a37a5-134">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a37a5-134">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37a5-135">針對 NXT 資源記錄的擁有者名稱，以空格分隔的 RR 類型助憶鍵清單。</span><span class="sxs-lookup"><span data-stu-id="a37a5-135">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="a37a5-136">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="a37a5-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a37a5-137">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a37a5-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a37a5-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="a37a5-138">Return value</span></span>

<span data-ttu-id="a37a5-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a37a5-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a37a5-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="a37a5-140">Requirements</span></span>



| <span data-ttu-id="a37a5-141">需求</span><span class="sxs-lookup"><span data-stu-id="a37a5-141">Requirement</span></span> | <span data-ttu-id="a37a5-142">值</span><span class="sxs-lookup"><span data-stu-id="a37a5-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a37a5-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a37a5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a37a5-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="a37a5-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a37a5-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a37a5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a37a5-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a37a5-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a37a5-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="a37a5-147">Namespace</span></span><br/>                | <span data-ttu-id="a37a5-148">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="a37a5-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a37a5-149">MOF</span><span class="sxs-lookup"><span data-stu-id="a37a5-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a37a5-150"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="a37a5-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a37a5-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a37a5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a37a5-152">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="a37a5-152">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="a37a5-153">**Modify MicrosoftDNS \_ NXTType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="a37a5-153">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="a37a5-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a37a5-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





