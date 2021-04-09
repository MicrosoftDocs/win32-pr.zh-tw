---
title: MicrosoftDNS_MBType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化信箱 (MB) 資源記錄。
ms.assetid: ac160a4d-2af7-428e-9cbd-bdd28f7c0910
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_MBType 類別
- MicrosoftDNS_MBType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e340d78057c12e58159a293468598da7dbf53e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843772"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="29680-106">MicrosoftDNS MBType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="29680-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="29680-107">**CreateInstanceFromPropertyData** 方法會具現化信箱 (MB) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="29680-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="29680-108">語法</span><span class="sxs-lookup"><span data-stu-id="29680-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]       string              DnsServerName,
  [in]       string              ContainerName,
  [in]       string              OwnerName,
  [in]       uint32              RecordClass = 1,
  [in]       uint32              TTL,
  [in]       string              MBHost,
  [out, ref] MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="29680-109">參數</span><span class="sxs-lookup"><span data-stu-id="29680-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29680-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29680-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29680-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="29680-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="29680-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29680-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29680-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="29680-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="29680-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29680-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29680-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="29680-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="29680-116">*RecordClass* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29680-116">*RecordClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29680-117">選擇性。</span><span class="sxs-lookup"><span data-stu-id="29680-117">Optional.</span></span> <span data-ttu-id="29680-118">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="29680-118">Class of the RR.</span></span> <span data-ttu-id="29680-119">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="29680-119">Default value is 1.</span></span> <span data-ttu-id="29680-120">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="29680-120">The following values are valid.</span></span>



| <span data-ttu-id="29680-121">值</span><span class="sxs-lookup"><span data-stu-id="29680-121">Value</span></span>                                                                                                | <span data-ttu-id="29680-122">意義</span><span class="sxs-lookup"><span data-stu-id="29680-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="29680-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="29680-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="29680-124">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="29680-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="29680-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="29680-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="29680-126">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="29680-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="29680-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="29680-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="29680-128">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="29680-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="29680-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="29680-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="29680-130">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="29680-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="29680-131">*TTL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29680-131">*TTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29680-132">選擇性。</span><span class="sxs-lookup"><span data-stu-id="29680-132">Optional.</span></span> <span data-ttu-id="29680-133">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="29680-133">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="29680-134">*MBHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29680-134">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29680-135">RR 的信箱主機名稱。</span><span class="sxs-lookup"><span data-stu-id="29680-135">Mailbox host name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="29680-136">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="29680-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="29680-137">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="29680-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29680-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="29680-138">Return value</span></span>

<span data-ttu-id="29680-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="29680-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="29680-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="29680-140">Requirements</span></span>



| <span data-ttu-id="29680-141">需求</span><span class="sxs-lookup"><span data-stu-id="29680-141">Requirement</span></span> | <span data-ttu-id="29680-142">值</span><span class="sxs-lookup"><span data-stu-id="29680-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29680-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29680-143">Minimum supported client</span></span><br/> | <span data-ttu-id="29680-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="29680-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="29680-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29680-145">Minimum supported server</span></span><br/> | <span data-ttu-id="29680-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29680-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="29680-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="29680-147">Namespace</span></span><br/>                | <span data-ttu-id="29680-148">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="29680-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="29680-149">MOF</span><span class="sxs-lookup"><span data-stu-id="29680-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29680-150"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="29680-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29680-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29680-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29680-152">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="29680-152">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="29680-153">**Modify MicrosoftDNS \_ MBType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="29680-153">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="29680-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="29680-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





