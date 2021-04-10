---
title: MicrosoftDNS_AType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化位址 () 資源記錄。
ms.assetid: 81d67eba-f2c6-49c0-af29-be3f3724a973
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_AType 類別
- MicrosoftDNS_AType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d8d3e5c9d0ad4302da2243a3ef9611e295c86e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103715"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="5be69-106">MicrosoftDNS AType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5be69-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="5be69-107">**CreateInstanceFromPropertyData** 方法會具現化位址 () 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="5be69-107">The **CreateInstanceFromPropertyData** method instantiates an Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be69-108">語法</span><span class="sxs-lookup"><span data-stu-id="5be69-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string             DnsServerName,
  [in]           string             ContainerName,
  [in]           string             OwnerName,
  [in, optional] uint32             RecordClass = 1,
  [in, optional] uint32             TTL,
  [in]           string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="5be69-109">參數</span><span class="sxs-lookup"><span data-stu-id="5be69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5be69-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5be69-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be69-111">包含此 RR 之 DNS 伺服器的完整功能變數名稱 (FQDN) 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5be69-111">Fully Qualified Domain Name (FQDN) or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="5be69-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5be69-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be69-113">包含此 RR 之 Zone、Cache 或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="5be69-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="5be69-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5be69-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be69-115">RR 的擁有者 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5be69-115">Owner FQDN for the RR.</span></span>

> [!Note]  
> <span data-ttu-id="5be69-116">請勿使用擁有者 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="5be69-116">Do not use the owner NetBIOS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="5be69-117">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5be69-117">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5be69-118">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="5be69-118">Class of the RR.</span></span> <span data-ttu-id="5be69-119">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="5be69-119">Default value is 1.</span></span> <span data-ttu-id="5be69-120">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="5be69-120">The following values are valid.</span></span>



| <span data-ttu-id="5be69-121">值</span><span class="sxs-lookup"><span data-stu-id="5be69-121">Value</span></span>                                                                                                | <span data-ttu-id="5be69-122">意義</span><span class="sxs-lookup"><span data-stu-id="5be69-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="5be69-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="5be69-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="5be69-124">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="5be69-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="5be69-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="5be69-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="5be69-126">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="5be69-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="5be69-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="5be69-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="5be69-128">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="5be69-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="5be69-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="5be69-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="5be69-130">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="5be69-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="5be69-131">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5be69-131">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5be69-132">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5be69-132">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="5be69-133">*IPAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5be69-133">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be69-134">代表主機 IP 位址的字串。</span><span class="sxs-lookup"><span data-stu-id="5be69-134">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="5be69-135">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="5be69-135">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5be69-136">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="5be69-136">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5be69-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="5be69-137">Return value</span></span>

<span data-ttu-id="5be69-138">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5be69-138">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5be69-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="5be69-139">Requirements</span></span>



| <span data-ttu-id="5be69-140">需求</span><span class="sxs-lookup"><span data-stu-id="5be69-140">Requirement</span></span> | <span data-ttu-id="5be69-141">值</span><span class="sxs-lookup"><span data-stu-id="5be69-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5be69-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5be69-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5be69-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="5be69-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5be69-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5be69-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5be69-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5be69-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5be69-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="5be69-146">Namespace</span></span><br/>                | <span data-ttu-id="5be69-147">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="5be69-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5be69-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5be69-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5be69-149"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="5be69-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5be69-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5be69-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be69-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="5be69-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="5be69-152">**Modify MicrosoftDNS \_ AType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="5be69-152">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





