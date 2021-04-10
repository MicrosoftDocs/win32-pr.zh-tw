---
title: MicrosoftDNS_WINSType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化 Windows 網際網路名稱服務 (WINS) 資源記錄。
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_WINSType 類別
- MicrosoftDNS_WINSType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf584bd34f59391a49fd5f7ec13cb49e18ef68fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686094"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="ee735-106">MicrosoftDNS WINSType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ee735-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="ee735-107">**CreateInstanceFromPropertyData** 方法會具現化 Windows 網際網路名稱服務 (WINS) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="ee735-107">The **CreateInstanceFromPropertyData** method instantiates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee735-108">語法</span><span class="sxs-lookup"><span data-stu-id="ee735-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ee735-109">參數</span><span class="sxs-lookup"><span data-stu-id="ee735-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee735-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee735-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ee735-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ee735-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee735-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="ee735-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ee735-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee735-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="ee735-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ee735-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ee735-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="ee735-117">Class of the RR.</span></span> <span data-ttu-id="ee735-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="ee735-118">Default value is 1.</span></span> <span data-ttu-id="ee735-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="ee735-119">The following values are valid.</span></span>



| <span data-ttu-id="ee735-120">值</span><span class="sxs-lookup"><span data-stu-id="ee735-120">Value</span></span>                                                                                                | <span data-ttu-id="ee735-121">意義</span><span class="sxs-lookup"><span data-stu-id="ee735-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ee735-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ee735-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="ee735-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ee735-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ee735-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="ee735-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ee735-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ee735-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="ee735-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ee735-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ee735-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="ee735-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ee735-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ee735-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee735-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ee735-132">*MappingFlag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee735-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-133">WINS 對應旗標，指定是否必須將記錄包含在區域複寫中。</span><span class="sxs-lookup"><span data-stu-id="ee735-133">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="ee735-134">它只能有兩個值：對應于複寫的0x80000000 和0x00010000，以及) 旗標的 (本機記錄。</span><span class="sxs-lookup"><span data-stu-id="ee735-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="ee735-135">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="ee735-135">The following values are valid.</span></span>



| <span data-ttu-id="ee735-136">值</span><span class="sxs-lookup"><span data-stu-id="ee735-136">Value</span></span>                                                                                                                                               | <span data-ttu-id="ee735-137">意義</span><span class="sxs-lookup"><span data-stu-id="ee735-137">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="ee735-138"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-138"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="ee735-139">複寫旗標</span><span class="sxs-lookup"><span data-stu-id="ee735-139">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="ee735-140"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-140"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="ee735-141">無複寫 (本機記錄) 旗標</span><span class="sxs-lookup"><span data-stu-id="ee735-141">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ee735-142">*LookupTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee735-142">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-143">DNS 伺服器使用 WINS 查詢來嘗試解析的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee735-143">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="ee735-144">*CacheTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee735-144">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-145">使用 WINS 查詢的 DNS 伺服器可能會快取 WINS 伺服器的回應時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee735-145">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="ee735-146">*WinsServers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee735-146">*WinsServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-147">WINS 查詢中使用之 WINS 伺服器的逗點分隔 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="ee735-147">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="ee735-148">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="ee735-148">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-149">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="ee735-149">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee735-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee735-150">Return value</span></span>

<span data-ttu-id="ee735-151">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ee735-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee735-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee735-152">Requirements</span></span>



| <span data-ttu-id="ee735-153">需求</span><span class="sxs-lookup"><span data-stu-id="ee735-153">Requirement</span></span> | <span data-ttu-id="ee735-154">值</span><span class="sxs-lookup"><span data-stu-id="ee735-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee735-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee735-155">Minimum supported client</span></span><br/> | <span data-ttu-id="ee735-156">都不支援</span><span class="sxs-lookup"><span data-stu-id="ee735-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ee735-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee735-157">Minimum supported server</span></span><br/> | <span data-ttu-id="ee735-158">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee735-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ee735-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="ee735-159">Namespace</span></span><br/>                | <span data-ttu-id="ee735-160">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ee735-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ee735-161">MOF</span><span class="sxs-lookup"><span data-stu-id="ee735-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee735-162"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee735-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee735-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee735-164">**MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="ee735-164">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="ee735-165">**Modify MicrosoftDNS \_ WINSType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="ee735-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="ee735-166">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ee735-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





