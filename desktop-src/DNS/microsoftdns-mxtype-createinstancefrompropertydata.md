---
title: MicrosoftDNS_MXType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化郵件交換 (MR) 資源記錄。
ms.assetid: 5724b14a-bb64-460c-ac49-28bac85b8620
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_MXType 類別
- MicrosoftDNS_MXType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8154e8ccdc6ac18824e2d56597ac8e0f186f3912
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103853"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="76fcd-106">MicrosoftDNS MXType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="76fcd-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="76fcd-107">**CreateInstanceFromPropertyData** 方法會具現化郵件交換 (MR) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="76fcd-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="76fcd-108">語法</span><span class="sxs-lookup"><span data-stu-id="76fcd-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="76fcd-109">參數</span><span class="sxs-lookup"><span data-stu-id="76fcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76fcd-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76fcd-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76fcd-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="76fcd-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="76fcd-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76fcd-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76fcd-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="76fcd-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="76fcd-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76fcd-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76fcd-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="76fcd-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="76fcd-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="76fcd-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76fcd-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="76fcd-117">Class of the RR.</span></span> <span data-ttu-id="76fcd-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="76fcd-118">Default value is 1.</span></span> <span data-ttu-id="76fcd-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="76fcd-119">The following values are valid.</span></span>



| <span data-ttu-id="76fcd-120">值</span><span class="sxs-lookup"><span data-stu-id="76fcd-120">Value</span></span>                                                                                                | <span data-ttu-id="76fcd-121">意義</span><span class="sxs-lookup"><span data-stu-id="76fcd-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="76fcd-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="76fcd-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="76fcd-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="76fcd-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="76fcd-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="76fcd-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="76fcd-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="76fcd-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="76fcd-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="76fcd-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="76fcd-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="76fcd-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="76fcd-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="76fcd-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="76fcd-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="76fcd-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="76fcd-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="76fcd-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76fcd-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="76fcd-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="76fcd-132">*喜好* \[ 設定在\]</span><span class="sxs-lookup"><span data-stu-id="76fcd-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76fcd-133">在相同擁有者的其他專案中提供給此 RR 的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="76fcd-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="76fcd-134">偏好較低的值。</span><span class="sxs-lookup"><span data-stu-id="76fcd-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="76fcd-135">*MailExchange* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76fcd-135">*MailExchange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76fcd-136">FQDN 指定的主機願意作為擁有者名稱的郵件交換。</span><span class="sxs-lookup"><span data-stu-id="76fcd-136">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="76fcd-137">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="76fcd-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="76fcd-138">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="76fcd-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76fcd-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="76fcd-139">Return value</span></span>

<span data-ttu-id="76fcd-140">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="76fcd-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="76fcd-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="76fcd-141">Requirements</span></span>



| <span data-ttu-id="76fcd-142">需求</span><span class="sxs-lookup"><span data-stu-id="76fcd-142">Requirement</span></span> | <span data-ttu-id="76fcd-143">值</span><span class="sxs-lookup"><span data-stu-id="76fcd-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76fcd-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76fcd-144">Minimum supported client</span></span><br/> | <span data-ttu-id="76fcd-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="76fcd-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="76fcd-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76fcd-146">Minimum supported server</span></span><br/> | <span data-ttu-id="76fcd-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76fcd-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="76fcd-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="76fcd-148">Namespace</span></span><br/>                | <span data-ttu-id="76fcd-149">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="76fcd-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="76fcd-150">MOF</span><span class="sxs-lookup"><span data-stu-id="76fcd-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76fcd-151"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="76fcd-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76fcd-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76fcd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fcd-153">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="76fcd-153">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="76fcd-154">**Modify MicrosoftDNS \_ MXType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="76fcd-154">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="76fcd-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="76fcd-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





