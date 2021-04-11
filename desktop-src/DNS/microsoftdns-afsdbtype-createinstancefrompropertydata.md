---
title: MicrosoftDNS_AFSDBType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化 Andrew 檔案系統資料庫伺服器 (AFSDB) 資源記錄。
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_AFSDBType 類別
- MicrosoftDNS_AFSDBType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934386"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="9aa86-106">MicrosoftDNS AFSDBType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9aa86-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="9aa86-107">**CreateInstanceFromPropertyData** 方法會具現化 Andrew 檔案系統資料庫伺服器 (AFSDB) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="9aa86-107">The **CreateInstanceFromPropertyData** method instantiates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa86-108">語法</span><span class="sxs-lookup"><span data-stu-id="9aa86-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9aa86-109">參數</span><span class="sxs-lookup"><span data-stu-id="9aa86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa86-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9aa86-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa86-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9aa86-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9aa86-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9aa86-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa86-113">包含此 RR 之 Zone、Cache 或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="9aa86-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9aa86-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9aa86-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa86-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="9aa86-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="9aa86-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9aa86-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa86-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="9aa86-117">Class of the RR.</span></span> <span data-ttu-id="9aa86-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="9aa86-118">Default value is 1.</span></span> <span data-ttu-id="9aa86-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="9aa86-119">The following values are valid.</span></span>



| <span data-ttu-id="9aa86-120">值</span><span class="sxs-lookup"><span data-stu-id="9aa86-120">Value</span></span>                                                                                                | <span data-ttu-id="9aa86-121">意義</span><span class="sxs-lookup"><span data-stu-id="9aa86-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="9aa86-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9aa86-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9aa86-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="9aa86-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="9aa86-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9aa86-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9aa86-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="9aa86-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="9aa86-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="9aa86-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="9aa86-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="9aa86-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="9aa86-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="9aa86-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="9aa86-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="9aa86-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="9aa86-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9aa86-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa86-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9aa86-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9aa86-132">*子類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9aa86-132">*Subtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa86-133">主機 AFS 伺服器的子類型。</span><span class="sxs-lookup"><span data-stu-id="9aa86-133">Subtype of the host AFS server.</span></span> <span data-ttu-id="9aa86-134">針對子類型 1 (值 = 1) ，主機具有適用于已命名 AFS 資料格的 AFS 3.0 磁片區位置伺服器。</span><span class="sxs-lookup"><span data-stu-id="9aa86-134">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="9aa86-135">在子類型 2 (值 = 2) 的情況下，主機會有經過驗證的名稱伺服器，保留命名的 DCE/NCA 資料格的資料格根目錄節點。</span><span class="sxs-lookup"><span data-stu-id="9aa86-135">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="9aa86-136">*ServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9aa86-136">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa86-137">FQDN 指定主機，該主機的擁有者名稱中指定的 AFS 資料格具有伺服器。</span><span class="sxs-lookup"><span data-stu-id="9aa86-137">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="9aa86-138">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="9aa86-138">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa86-139">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="9aa86-139">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa86-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="9aa86-140">Return value</span></span>

<span data-ttu-id="9aa86-141">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9aa86-141">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa86-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="9aa86-142">Requirements</span></span>



| <span data-ttu-id="9aa86-143">需求</span><span class="sxs-lookup"><span data-stu-id="9aa86-143">Requirement</span></span> | <span data-ttu-id="9aa86-144">值</span><span class="sxs-lookup"><span data-stu-id="9aa86-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa86-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9aa86-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa86-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="9aa86-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9aa86-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9aa86-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa86-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9aa86-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9aa86-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="9aa86-149">Namespace</span></span><br/>                | <span data-ttu-id="9aa86-150">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="9aa86-150">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9aa86-151">MOF</span><span class="sxs-lookup"><span data-stu-id="9aa86-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9aa86-152"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="9aa86-152"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aa86-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9aa86-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa86-154">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="9aa86-154">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="9aa86-155">**Modify MicrosoftDNS \_ AFSDBType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="9aa86-155">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="9aa86-156">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="9aa86-156">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





