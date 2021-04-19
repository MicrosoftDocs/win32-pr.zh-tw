---
title: MicrosoftDNS_ATMAType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化 ATM 位址，以 (ATMA) 資源記錄的名稱。
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_ATMAType 類別
- MicrosoftDNS_ATMAType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968164"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="9ab8e-106">MicrosoftDNS ATMAType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9ab8e-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="9ab8e-107">**CreateInstanceFromPropertyData** 方法會具現化 ATM 位址，以 (ATMA) 資源記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-107">The **CreateInstanceFromPropertyData** method instantiates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab8e-108">語法</span><span class="sxs-lookup"><span data-stu-id="9ab8e-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9ab8e-109">參數</span><span class="sxs-lookup"><span data-stu-id="9ab8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab8e-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9ab8e-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab8e-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9ab8e-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9ab8e-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab8e-113">包含此 RR 之 Zone、Cache 或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9ab8e-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9ab8e-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab8e-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="9ab8e-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9ab8e-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab8e-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-117">Class of the RR.</span></span> <span data-ttu-id="9ab8e-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-118">Default value is 1.</span></span> <span data-ttu-id="9ab8e-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-119">The following values are valid.</span></span>



| <span data-ttu-id="9ab8e-120">值</span><span class="sxs-lookup"><span data-stu-id="9ab8e-120">Value</span></span>                                                                                                | <span data-ttu-id="9ab8e-121">意義</span><span class="sxs-lookup"><span data-stu-id="9ab8e-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="9ab8e-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9ab8e-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9ab8e-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="9ab8e-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="9ab8e-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9ab8e-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9ab8e-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="9ab8e-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="9ab8e-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="9ab8e-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="9ab8e-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="9ab8e-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="9ab8e-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="9ab8e-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="9ab8e-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="9ab8e-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="9ab8e-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9ab8e-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab8e-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9ab8e-132">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9ab8e-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab8e-133">ATM 位址格式。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-133">ATM address format.</span></span> <span data-ttu-id="9ab8e-134">格式有兩個可能的值：0表示 ATM 終端系統位址 (AESA) 格式，而1表示電子164格式。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-134">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="9ab8e-135">*ATMAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9ab8e-135">*ATMAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab8e-136">包含此 RR 所屬節點/擁有者之 ATM 位址的八位變數長度字串。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-136">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="9ab8e-137">陣列的前四個位元組是用來儲存八位字串的大小。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-137">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="9ab8e-138">最重要的位元組會儲存在位元組0中。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-138">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="9ab8e-139">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="9ab8e-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab8e-140">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab8e-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ab8e-141">Return value</span></span>

<span data-ttu-id="9ab8e-142">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9ab8e-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab8e-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ab8e-143">Requirements</span></span>



| <span data-ttu-id="9ab8e-144">需求</span><span class="sxs-lookup"><span data-stu-id="9ab8e-144">Requirement</span></span> | <span data-ttu-id="9ab8e-145">值</span><span class="sxs-lookup"><span data-stu-id="9ab8e-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab8e-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ab8e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9ab8e-147">都不支援</span><span class="sxs-lookup"><span data-stu-id="9ab8e-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9ab8e-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ab8e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9ab8e-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ab8e-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9ab8e-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="9ab8e-150">Namespace</span></span><br/>                | <span data-ttu-id="9ab8e-151">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="9ab8e-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9ab8e-152">MOF</span><span class="sxs-lookup"><span data-stu-id="9ab8e-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ab8e-153"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ab8e-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab8e-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ab8e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab8e-155">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-155">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="9ab8e-156">**Modify MicrosoftDNS \_ ATMAType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-156">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="9ab8e-157">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





