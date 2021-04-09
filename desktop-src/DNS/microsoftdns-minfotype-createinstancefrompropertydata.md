---
title: MicrosoftDNS_MINFOType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化郵件資訊 (MINFO) 資源記錄。
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_MINFOType 類別
- MicrosoftDNS_MINFOType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a565b1575dc51a59a09faea6fd271d719518f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024624"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="f7d27-106">MicrosoftDNS MINFOType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f7d27-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="f7d27-107">**CreateInstanceFromPropertyData** 方法會具現化郵件資訊 (MINFO) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="f7d27-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d27-108">語法</span><span class="sxs-lookup"><span data-stu-id="f7d27-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 ResponsibleMailbox,
  [in]           string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f7d27-109">參數</span><span class="sxs-lookup"><span data-stu-id="f7d27-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d27-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7d27-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d27-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f7d27-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f7d27-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7d27-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d27-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="f7d27-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f7d27-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7d27-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d27-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="f7d27-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f7d27-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f7d27-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d27-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="f7d27-117">Class of the RR.</span></span> <span data-ttu-id="f7d27-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="f7d27-118">Default value is 1.</span></span> <span data-ttu-id="f7d27-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="f7d27-119">The following values are valid.</span></span>



| <span data-ttu-id="f7d27-120">值</span><span class="sxs-lookup"><span data-stu-id="f7d27-120">Value</span></span>                                                                                                | <span data-ttu-id="f7d27-121">意義</span><span class="sxs-lookup"><span data-stu-id="f7d27-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f7d27-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f7d27-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f7d27-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="f7d27-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f7d27-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f7d27-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f7d27-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="f7d27-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f7d27-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f7d27-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f7d27-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="f7d27-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f7d27-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f7d27-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f7d27-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="f7d27-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f7d27-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f7d27-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d27-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f7d27-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f7d27-132">*ResponsibleMailbox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7d27-132">*ResponsibleMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d27-133">FQDN，指定負責記錄的擁有者名稱中所指定之郵寄清單或信箱的信箱。</span><span class="sxs-lookup"><span data-stu-id="f7d27-133">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="f7d27-134">*ErrorMailbox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7d27-134">*ErrorMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d27-135">FQDN，指定信箱以接收與郵寄清單相關的錯誤訊息，或 MINFO 記錄的擁有者名稱所指定的信箱。</span><span class="sxs-lookup"><span data-stu-id="f7d27-135">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="f7d27-136">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="f7d27-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d27-137">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="f7d27-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d27-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7d27-138">Return value</span></span>

<span data-ttu-id="f7d27-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f7d27-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d27-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7d27-140">Requirements</span></span>



| <span data-ttu-id="f7d27-141">需求</span><span class="sxs-lookup"><span data-stu-id="f7d27-141">Requirement</span></span> | <span data-ttu-id="f7d27-142">值</span><span class="sxs-lookup"><span data-stu-id="f7d27-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d27-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7d27-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d27-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="f7d27-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f7d27-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7d27-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d27-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7d27-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f7d27-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="f7d27-147">Namespace</span></span><br/>                | <span data-ttu-id="f7d27-148">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="f7d27-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f7d27-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f7d27-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7d27-150"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7d27-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d27-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7d27-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d27-152">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="f7d27-152">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="f7d27-153">**Modify MicrosoftDNS \_ MINFOType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="f7d27-153">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="f7d27-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f7d27-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





