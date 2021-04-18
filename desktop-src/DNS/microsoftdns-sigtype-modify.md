---
title: Modify MicrosoftDNS_SIGType 類別的方法
description: Modify 方法會更新 (SIG) RR 的簽章。
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_SIGType 類別
- MicrosoftDNS_SIGType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464525"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="06b0a-106">Modify MicrosoftDNS \_ SIGType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="06b0a-106">Modify method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="06b0a-107">**Modify** 方法會更新 (SIG) RR 的簽章。</span><span class="sxs-lookup"><span data-stu-id="06b0a-107">The **Modify** method updates a Signature (SIG) RR.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b0a-108">語法</span><span class="sxs-lookup"><span data-stu-id="06b0a-108">Syntax</span></span>


```mof
void Modify(
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



## <a name="parameters"></a><span data-ttu-id="06b0a-109">參數</span><span class="sxs-lookup"><span data-stu-id="06b0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b0a-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="06b0a-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="06b0a-112">*TypeCovered* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-112">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-113">此 SIG 所涵蓋的 RR 類型。</span><span class="sxs-lookup"><span data-stu-id="06b0a-113">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="06b0a-114">*演算法* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-114">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-115">與資源記錄中指定的金鑰搭配使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="06b0a-115">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="06b0a-116">指派的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="06b0a-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="06b0a-117">值</span><span class="sxs-lookup"><span data-stu-id="06b0a-117">Value</span></span>                                                                                                | <span data-ttu-id="06b0a-118">意義</span><span class="sxs-lookup"><span data-stu-id="06b0a-118">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="06b0a-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="06b0a-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="06b0a-120">RSA/MD5 (RFC 2537) </span><span class="sxs-lookup"><span data-stu-id="06b0a-120">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="06b0a-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="06b0a-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="06b0a-122">Diffie-Hellman (RFC 2539) </span><span class="sxs-lookup"><span data-stu-id="06b0a-122">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="06b0a-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="06b0a-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="06b0a-124">DSA (RFC 2536) </span><span class="sxs-lookup"><span data-stu-id="06b0a-124">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="06b0a-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="06b0a-125"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="06b0a-126">橢圓曲線密碼編譯</span><span class="sxs-lookup"><span data-stu-id="06b0a-126">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="06b0a-127">*標籤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-127">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-128">原始 SIG RR 擁有者名稱中的標籤計數（不帶正負號）。</span><span class="sxs-lookup"><span data-stu-id="06b0a-128">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="06b0a-129">此計數不包含根的 Null 標籤，也不包含任何初始萬用字元。</span><span class="sxs-lookup"><span data-stu-id="06b0a-129">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="06b0a-130">*OriginalTTL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-130">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-131">由 SIG 簽署之 RR 集合的 TTL。</span><span class="sxs-lookup"><span data-stu-id="06b0a-131">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="06b0a-132">*SignatureExpiration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-132">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-133">簽章到期日（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。</span><span class="sxs-lookup"><span data-stu-id="06b0a-133">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="06b0a-134">*SignatureInception* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-134">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-135">簽章變成有效的日期和時間（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。</span><span class="sxs-lookup"><span data-stu-id="06b0a-135">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="06b0a-136">*KeyTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-136">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-137">方法，用來選擇驗證 SIG 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="06b0a-137">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="06b0a-138">如需用來計算 KeyTag 的方法，請參閱 RFC 2535、附錄 C。</span><span class="sxs-lookup"><span data-stu-id="06b0a-138">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="06b0a-139">*SignerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-139">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-140">產生 SIG RR 之簽署者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="06b0a-140">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="06b0a-141">簽章 \[在\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-141">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-142">以 base 64 表示的簽章，格式如 RFC 2535 中所定義，附錄 A。</span><span class="sxs-lookup"><span data-stu-id="06b0a-142">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="06b0a-143">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-143">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="06b0a-144">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="06b0a-144">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b0a-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="06b0a-145">Return value</span></span>

<span data-ttu-id="06b0a-146">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="06b0a-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06b0a-147">備註</span><span class="sxs-lookup"><span data-stu-id="06b0a-147">Remarks</span></span>

<span data-ttu-id="06b0a-148">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="06b0a-148">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b0a-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="06b0a-149">Requirements</span></span>



| <span data-ttu-id="06b0a-150">需求</span><span class="sxs-lookup"><span data-stu-id="06b0a-150">Requirement</span></span> | <span data-ttu-id="06b0a-151">值</span><span class="sxs-lookup"><span data-stu-id="06b0a-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06b0a-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06b0a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="06b0a-153">都不支援</span><span class="sxs-lookup"><span data-stu-id="06b0a-153">None supported</span></span><br/>                                                              |
| <span data-ttu-id="06b0a-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06b0a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="06b0a-155">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06b0a-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="06b0a-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="06b0a-156">Namespace</span></span><br/>                | <span data-ttu-id="06b0a-157">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="06b0a-157">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="06b0a-158">MOF</span><span class="sxs-lookup"><span data-stu-id="06b0a-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06b0a-159"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="06b0a-159"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06b0a-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06b0a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b0a-161">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="06b0a-161">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="06b0a-162">**MicrosoftDNS SIGType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="06b0a-162">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="06b0a-163">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="06b0a-163">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





