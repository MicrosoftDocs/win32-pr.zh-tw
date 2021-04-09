---
title: Modify MicrosoftDNS_KEYType 類別的方法
description: Modify 方法會更新金鑰資源記錄。
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- 修改方法 DNS
- 修改方法 DNS，MicrosoftDNS_KEYType 類別
- MicrosoftDNS_KEYType 類別 DNS，Modify 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106127"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="803c1-106">Modify MicrosoftDNS \_ KEYType 類別的方法</span><span class="sxs-lookup"><span data-stu-id="803c1-106">Modify method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="803c1-107">**Modify** 方法會更新金鑰資源記錄。</span><span class="sxs-lookup"><span data-stu-id="803c1-107">The **Modify** method updates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="803c1-108">語法</span><span class="sxs-lookup"><span data-stu-id="803c1-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="803c1-109">參數</span><span class="sxs-lookup"><span data-stu-id="803c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="803c1-110">*TTL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="803c1-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="803c1-111">DNS 解析程式可以快取 RR 的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="803c1-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="803c1-112">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="803c1-112">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="803c1-113">用來指定對應的旗標，如 IETF RFC 2535 中所述。</span><span class="sxs-lookup"><span data-stu-id="803c1-113">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="803c1-114">*通訊協定* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="803c1-114">*Protocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="803c1-115">可使用在 RR 中指定之金鑰的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="803c1-115">Protocol for which the key specified in the RR can be used.</span></span> <span data-ttu-id="803c1-116">指派的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="803c1-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="803c1-117">值</span><span class="sxs-lookup"><span data-stu-id="803c1-117">Value</span></span>                                                                                                    | <span data-ttu-id="803c1-118">意義</span><span class="sxs-lookup"><span data-stu-id="803c1-118">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="803c1-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-119"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="803c1-120">TLS</span><span class="sxs-lookup"><span data-stu-id="803c1-120">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="803c1-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-121"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="803c1-122">電子郵件</span><span class="sxs-lookup"><span data-stu-id="803c1-122">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="803c1-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-123"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="803c1-124">dnssec</span><span class="sxs-lookup"><span data-stu-id="803c1-124">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="803c1-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-125"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="803c1-126">IPsec</span><span class="sxs-lookup"><span data-stu-id="803c1-126">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="803c1-127"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-127"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="803c1-128">所有通訊協定</span><span class="sxs-lookup"><span data-stu-id="803c1-128">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="803c1-129">*演算法* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="803c1-129">*Algorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="803c1-130">與資源記錄中指定的金鑰搭配使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="803c1-130">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="803c1-131">指派的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="803c1-131">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="803c1-132">值</span><span class="sxs-lookup"><span data-stu-id="803c1-132">Value</span></span>                                                                                                | <span data-ttu-id="803c1-133">意義</span><span class="sxs-lookup"><span data-stu-id="803c1-133">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="803c1-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="803c1-135">RSA/MD5 (RFC 2537) </span><span class="sxs-lookup"><span data-stu-id="803c1-135">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="803c1-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="803c1-137">Diffie-Hellman (RFC 2539) </span><span class="sxs-lookup"><span data-stu-id="803c1-137">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="803c1-138"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-138"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="803c1-139">DSA (RFC 2536) </span><span class="sxs-lookup"><span data-stu-id="803c1-139">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="803c1-140"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-140"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="803c1-141">橢圓曲線密碼編譯</span><span class="sxs-lookup"><span data-stu-id="803c1-141">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="803c1-142">*PublicKey* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="803c1-142">*PublicKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="803c1-143">公開金鑰，以基底64表示，如 RFC 2535 的附錄 A 所述。</span><span class="sxs-lookup"><span data-stu-id="803c1-143">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="803c1-144">*RR* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="803c1-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="803c1-145">新物件的參考。</span><span class="sxs-lookup"><span data-stu-id="803c1-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="803c1-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="803c1-146">Return value</span></span>

<span data-ttu-id="803c1-147">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="803c1-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="803c1-148">備註</span><span class="sxs-lookup"><span data-stu-id="803c1-148">Remarks</span></span>

<span data-ttu-id="803c1-149">任何未指定的參數在修改過的記錄中都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="803c1-149">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="803c1-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="803c1-150">Requirements</span></span>



| <span data-ttu-id="803c1-151">需求</span><span class="sxs-lookup"><span data-stu-id="803c1-151">Requirement</span></span> | <span data-ttu-id="803c1-152">值</span><span class="sxs-lookup"><span data-stu-id="803c1-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="803c1-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="803c1-153">Minimum supported client</span></span><br/> | <span data-ttu-id="803c1-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="803c1-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="803c1-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="803c1-155">Minimum supported server</span></span><br/> | <span data-ttu-id="803c1-156">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="803c1-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="803c1-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="803c1-157">Namespace</span></span><br/>                | <span data-ttu-id="803c1-158">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="803c1-158">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="803c1-159">MOF</span><span class="sxs-lookup"><span data-stu-id="803c1-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="803c1-160"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="803c1-160"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803c1-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="803c1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803c1-162">**MicrosoftDNS \_ KEYType**</span><span class="sxs-lookup"><span data-stu-id="803c1-162">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="803c1-163">**MicrosoftDNS KEYType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="803c1-163">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="803c1-164">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="803c1-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





