---
title: MicrosoftDNS_SIGType 類別的 CreateInstanceFromPropertyData 方法
description: CreateInstanceFromPropertyData 方法會具現化簽章 (SIG) 資源記錄。
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- CreateInstanceFromPropertyData 方法 DNS
- CreateInstanceFromPropertyData 方法 DNS，MicrosoftDNS_SIGType 類別
- MicrosoftDNS_SIGType 類別 DNS，CreateInstanceFromPropertyData 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024717"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="057ff-106">MicrosoftDNS SIGType 類別的 CreateInstanceFromPropertyData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="057ff-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="057ff-107">**CreateInstanceFromPropertyData** 方法會具現化簽章 (SIG) 資源記錄。</span><span class="sxs-lookup"><span data-stu-id="057ff-107">The **CreateInstanceFromPropertyData** method instantiates a Signature (SIG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="057ff-108">語法</span><span class="sxs-lookup"><span data-stu-id="057ff-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="057ff-109">參數</span><span class="sxs-lookup"><span data-stu-id="057ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="057ff-110">*DnsServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-111">包含此 RR 之 DNS 伺服器的 FQDN 或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="057ff-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-112">*容器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-113">包含此 RR 之區域、快取或 RootHints 實例的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="057ff-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-114">*OwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-115">RR 的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="057ff-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-116">*RecordClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="057ff-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-117">RR 的類別。</span><span class="sxs-lookup"><span data-stu-id="057ff-117">Class of the RR.</span></span> <span data-ttu-id="057ff-118">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="057ff-118">Default value is 1.</span></span> <span data-ttu-id="057ff-119">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="057ff-119">The following values are valid.</span></span>



| <span data-ttu-id="057ff-120">值</span><span class="sxs-lookup"><span data-stu-id="057ff-120">Value</span></span>                                                                                                | <span data-ttu-id="057ff-121">意義</span><span class="sxs-lookup"><span data-stu-id="057ff-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="057ff-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="057ff-123">在 (網際網路) </span><span class="sxs-lookup"><span data-stu-id="057ff-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="057ff-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="057ff-125">CS (CSNET) </span><span class="sxs-lookup"><span data-stu-id="057ff-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="057ff-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="057ff-127">CH (混亂) </span><span class="sxs-lookup"><span data-stu-id="057ff-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="057ff-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="057ff-129">HS (Hesiod) </span><span class="sxs-lookup"><span data-stu-id="057ff-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="057ff-130">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="057ff-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-131">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="057ff-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-132">*TypeCovered* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-132">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-133">此 SIG 所涵蓋的 RR 類型。</span><span class="sxs-lookup"><span data-stu-id="057ff-133">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-134">*演算法* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-134">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-135">與資源記錄中指定的金鑰搭配使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="057ff-135">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="057ff-136">指派的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="057ff-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="057ff-137">值</span><span class="sxs-lookup"><span data-stu-id="057ff-137">Value</span></span>                                                                                                | <span data-ttu-id="057ff-138">意義</span><span class="sxs-lookup"><span data-stu-id="057ff-138">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="057ff-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-139"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="057ff-140">RSA/MD5 (RFC 2537) </span><span class="sxs-lookup"><span data-stu-id="057ff-140">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="057ff-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-141"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="057ff-142">Diffie-Hellman (RFC 2539) </span><span class="sxs-lookup"><span data-stu-id="057ff-142">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="057ff-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-143"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="057ff-144">DSA (RFC 2536) </span><span class="sxs-lookup"><span data-stu-id="057ff-144">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="057ff-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-145"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="057ff-146">橢圓曲線密碼編譯</span><span class="sxs-lookup"><span data-stu-id="057ff-146">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="057ff-147">*標籤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-147">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-148">原始 SIG RR 擁有者名稱中的標籤計數（不帶正負號）。</span><span class="sxs-lookup"><span data-stu-id="057ff-148">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="057ff-149">此計數不包含根的 Null 標籤，也不包含任何初始萬用字元。</span><span class="sxs-lookup"><span data-stu-id="057ff-149">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-150">*OriginalTTL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-150">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-151">由 SIG 簽署之 RR 集合的 TTL。</span><span class="sxs-lookup"><span data-stu-id="057ff-151">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-152">*SignatureExpiration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-152">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-153">簽章到期日（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。</span><span class="sxs-lookup"><span data-stu-id="057ff-153">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-154">*SignatureInception* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-154">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-155">簽章變成有效的日期和時間（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。</span><span class="sxs-lookup"><span data-stu-id="057ff-155">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-156">*KeyTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-156">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-157">方法，用來選擇驗證 SIG 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="057ff-157">Method used to choose a key that verifies an SIG.</span></span> <span data-ttu-id="057ff-158">如需用來計算 KeyTag 的方法，請參閱 RFC 2535、附錄 C。</span><span class="sxs-lookup"><span data-stu-id="057ff-158">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-159">*SignerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-159">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-160">產生 SIG RR 之簽署者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="057ff-160">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-161">簽章 \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ff-161">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-162">以 base 64 表示的簽章，格式如 RFC 2535 中所定義，附錄 A。</span><span class="sxs-lookup"><span data-stu-id="057ff-162">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="057ff-163">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="057ff-163">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="057ff-164">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="057ff-164">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="057ff-165">傳回值</span><span class="sxs-lookup"><span data-stu-id="057ff-165">Return value</span></span>

<span data-ttu-id="057ff-166">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="057ff-166">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="057ff-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="057ff-167">Requirements</span></span>



| <span data-ttu-id="057ff-168">需求</span><span class="sxs-lookup"><span data-stu-id="057ff-168">Requirement</span></span> | <span data-ttu-id="057ff-169">值</span><span class="sxs-lookup"><span data-stu-id="057ff-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="057ff-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="057ff-170">Minimum supported client</span></span><br/> | <span data-ttu-id="057ff-171">都不支援</span><span class="sxs-lookup"><span data-stu-id="057ff-171">None supported</span></span><br/>                                                              |
| <span data-ttu-id="057ff-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="057ff-172">Minimum supported server</span></span><br/> | <span data-ttu-id="057ff-173">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="057ff-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="057ff-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="057ff-174">Namespace</span></span><br/>                | <span data-ttu-id="057ff-175">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="057ff-175">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="057ff-176">MOF</span><span class="sxs-lookup"><span data-stu-id="057ff-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="057ff-177"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-177"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="057ff-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="057ff-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057ff-179">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="057ff-179">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="057ff-180">**Modify MicrosoftDNS \_ SIGType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="057ff-180">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="057ff-181">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="057ff-181">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





