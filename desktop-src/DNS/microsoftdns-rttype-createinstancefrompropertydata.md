---
title: MicrosoftDNS_RTType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會透過 (RT) 資源記錄來具現化路由。
ms.assetid: 1ebb0543-d031-4430-acbe-708c4931b7a4
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_RTType 類別
- MicrosoftDNS_RTType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c3b8d71c41fefa9b78aa9a469ee1426c553e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508684"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="d554b-106">MicrosoftDNS RTType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d554b-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="d554b-107">**CreateInstanceFromPropertyData** 方法會透過 (RT) 資源記錄來具現化路由。</span><span class="sxs-lookup"><span data-stu-id="d554b-107">The **CreateInstanceFromPropertyData** method instantiates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d554b-108">語法</span><span class="sxs-lookup"><span data-stu-id="d554b-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d554b-109">參數</span><span class="sxs-lookup"><span data-stu-id="d554b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d554b-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d554b-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d554b-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d554b-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d554b-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d554b-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d554b-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="d554b-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d554b-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d554b-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d554b-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="d554b-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="d554b-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d554b-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d554b-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="d554b-117">Class of the RR.</span></span> <span data-ttu-id="d554b-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="d554b-118">Default value is 1.</span></span> <span data-ttu-id="d554b-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="d554b-119">The following values are valid.</span></span>



| <span data-ttu-id="d554b-120">值</span><span class="sxs-lookup"><span data-stu-id="d554b-120">Value</span></span>                                                                                                | <span data-ttu-id="d554b-121">意義</span><span class="sxs-lookup"><span data-stu-id="d554b-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d554b-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d554b-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d554b-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="d554b-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="d554b-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d554b-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d554b-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="d554b-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="d554b-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="d554b-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="d554b-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="d554b-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="d554b-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d554b-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="d554b-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="d554b-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="d554b-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d554b-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d554b-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d554b-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d554b-132">*喜好* \[ 設定在\]</span><span class="sxs-lookup"><span data-stu-id="d554b-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d554b-133">在相同擁有者的其他專案中提供給此 RR 的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="d554b-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="d554b-134">偏好較低的值。</span><span class="sxs-lookup"><span data-stu-id="d554b-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="d554b-135">*IntermediateHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d554b-135">*IntermediateHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d554b-136">FQDN，指定主機做為中繼，以達到擁有者指定的主機。</span><span class="sxs-lookup"><span data-stu-id="d554b-136">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="d554b-137">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="d554b-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d554b-138">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d554b-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d554b-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="d554b-139">Return value</span></span>

<span data-ttu-id="d554b-140">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d554b-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d554b-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="d554b-141">Requirements</span></span>



| <span data-ttu-id="d554b-142">需求</span><span class="sxs-lookup"><span data-stu-id="d554b-142">Requirement</span></span> | <span data-ttu-id="d554b-143">值</span><span class="sxs-lookup"><span data-stu-id="d554b-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d554b-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d554b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d554b-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="d554b-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d554b-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d554b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d554b-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d554b-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d554b-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="d554b-148">Namespace</span></span><br/>                | <span data-ttu-id="d554b-149">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d554b-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d554b-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d554b-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d554b-151"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="d554b-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d554b-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d554b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d554b-153">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="d554b-153">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="d554b-154">**Modify MicrosoftDNS \_ RTType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="d554b-154">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="d554b-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d554b-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





