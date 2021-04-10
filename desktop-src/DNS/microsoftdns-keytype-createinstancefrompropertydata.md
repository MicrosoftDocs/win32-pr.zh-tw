---
title: MicrosoftDNS_KEYType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化金鑰資源記錄。
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_KEYType 類別
- MicrosoftDNS_KEYType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16dc8f3f591ba3aaf5ac9883cdd3a15c85146d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025463"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="bbe9d-106">MicrosoftDNS KEYType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bbe9d-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="bbe9d-107">**CreateInstanceFromPropertyData** 方法會具現化金鑰資源記錄。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-107">The **CreateInstanceFromPropertyData** method instantiates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe9d-108">語法</span><span class="sxs-lookup"><span data-stu-id="bbe9d-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="bbe9d-109">參數</span><span class="sxs-lookup"><span data-stu-id="bbe9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbe9d-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="bbe9d-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="bbe9d-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="bbe9d-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-117">Class of the RR.</span></span> <span data-ttu-id="bbe9d-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-118">Default value is 1.</span></span> <span data-ttu-id="bbe9d-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-119">The following values are valid.</span></span>



| <span data-ttu-id="bbe9d-120">值</span><span class="sxs-lookup"><span data-stu-id="bbe9d-120">Value</span></span>                                                                                                | <span data-ttu-id="bbe9d-121">意義</span><span class="sxs-lookup"><span data-stu-id="bbe9d-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="bbe9d-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="bbe9d-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="bbe9d-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="bbe9d-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="bbe9d-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="bbe9d-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="bbe9d-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="bbe9d-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="bbe9d-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="bbe9d-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="bbe9d-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="bbe9d-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="bbe9d-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="bbe9d-132">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-132">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-133">用來指定對應的旗標，如 IETF RFC 2535 中所述。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-133">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="bbe9d-134">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-134">*Protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-135">可以使用資源記錄中所指定金鑰的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-135">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="bbe9d-136">指派的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="bbe9d-137">值</span><span class="sxs-lookup"><span data-stu-id="bbe9d-137">Value</span></span>                                                                                                    | <span data-ttu-id="bbe9d-138">意義</span><span class="sxs-lookup"><span data-stu-id="bbe9d-138">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="bbe9d-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-139"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="bbe9d-140">TLS</span><span class="sxs-lookup"><span data-stu-id="bbe9d-140">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="bbe9d-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-141"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="bbe9d-142">電子郵件</span><span class="sxs-lookup"><span data-stu-id="bbe9d-142">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="bbe9d-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-143"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="bbe9d-144">dnssec</span><span class="sxs-lookup"><span data-stu-id="bbe9d-144">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="bbe9d-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-145"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="bbe9d-146">IPsec</span><span class="sxs-lookup"><span data-stu-id="bbe9d-146">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="bbe9d-147"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-147"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="bbe9d-148">所有通訊協定</span><span class="sxs-lookup"><span data-stu-id="bbe9d-148">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bbe9d-149">*演算法* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-149">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-150">與資源記錄中指定的金鑰搭配使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-150">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="bbe9d-151">指派的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="bbe9d-152">值</span><span class="sxs-lookup"><span data-stu-id="bbe9d-152">Value</span></span>                                                                                                | <span data-ttu-id="bbe9d-153">意義</span><span class="sxs-lookup"><span data-stu-id="bbe9d-153">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="bbe9d-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-154"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="bbe9d-155">RSA/MD5 (RFC 2537) </span><span class="sxs-lookup"><span data-stu-id="bbe9d-155">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="bbe9d-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-156"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="bbe9d-157">Diffie-Hellman (RFC 2539) </span><span class="sxs-lookup"><span data-stu-id="bbe9d-157">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="bbe9d-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-158"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="bbe9d-159">DSA (RFC 2536) </span><span class="sxs-lookup"><span data-stu-id="bbe9d-159">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="bbe9d-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-160"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="bbe9d-161">橢圓曲線密碼編譯</span><span class="sxs-lookup"><span data-stu-id="bbe9d-161">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bbe9d-162">*PublicKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-162">*PublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-163">公開金鑰，以基底64表示，如 RFC 2535 的附錄 A 所述。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-163">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="bbe9d-164">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-164">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-165">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-165">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbe9d-166">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbe9d-166">Return value</span></span>

<span data-ttu-id="bbe9d-167">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bbe9d-167">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe9d-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbe9d-168">Requirements</span></span>



| <span data-ttu-id="bbe9d-169">需求</span><span class="sxs-lookup"><span data-stu-id="bbe9d-169">Requirement</span></span> | <span data-ttu-id="bbe9d-170">值</span><span class="sxs-lookup"><span data-stu-id="bbe9d-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe9d-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbe9d-171">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe9d-172">都不支援</span><span class="sxs-lookup"><span data-stu-id="bbe9d-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bbe9d-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbe9d-173">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe9d-174">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbe9d-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bbe9d-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="bbe9d-175">Namespace</span></span><br/>                | <span data-ttu-id="bbe9d-176">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="bbe9d-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="bbe9d-177">MOF</span><span class="sxs-lookup"><span data-stu-id="bbe9d-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbe9d-178"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbe9d-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbe9d-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe9d-180">**MicrosoftDNS \_ KEYType**</span><span class="sxs-lookup"><span data-stu-id="bbe9d-180">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="bbe9d-181">**Modify MicrosoftDNS \_ KEYType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="bbe9d-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="bbe9d-182">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="bbe9d-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





