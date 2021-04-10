---
title: MicrosoftDNS_SIGType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示 (SIG) 資源記錄的簽章。
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- MicrosoftDNS_SIGType 類別 DNS
- MicrosoftDNS_SIGType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685598"
---
# <a name="microsoftdns_sigtype-class"></a><span data-ttu-id="64c90-105">MicrosoftDNS \_ SIGType 類別</span><span class="sxs-lookup"><span data-stu-id="64c90-105">MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="64c90-106">[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示 (SIG) 資源記錄的簽章。</span><span class="sxs-lookup"><span data-stu-id="64c90-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Signature (SIG) Resource Record.</span></span>

<span data-ttu-id="64c90-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="64c90-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c90-108">語法</span><span class="sxs-lookup"><span data-stu-id="64c90-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a><span data-ttu-id="64c90-109">成員</span><span class="sxs-lookup"><span data-stu-id="64c90-109">Members</span></span>

<span data-ttu-id="64c90-110">**MicrosoftDNS \_ SIGType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="64c90-110">The **MicrosoftDNS\_SIGType** class has these types of members:</span></span>

-   [<span data-ttu-id="64c90-111">方法</span><span class="sxs-lookup"><span data-stu-id="64c90-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="64c90-112">屬性</span><span class="sxs-lookup"><span data-stu-id="64c90-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="64c90-113">方法</span><span class="sxs-lookup"><span data-stu-id="64c90-113">Methods</span></span>

<span data-ttu-id="64c90-114">**MicrosoftDNS \_ SIGType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="64c90-114">The **MicrosoftDNS\_SIGType** class has these methods.</span></span>



| <span data-ttu-id="64c90-115">方法</span><span class="sxs-lookup"><span data-stu-id="64c90-115">Method</span></span>                             | <span data-ttu-id="64c90-116">描述</span><span class="sxs-lookup"><span data-stu-id="64c90-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c90-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="64c90-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="64c90-118">根據方法的輸入參數中的資料具現化 SIG RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及 WINS 對應旗標、反向查閱超時、WINS 快取超時和要附加的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="64c90-118">Instantiates an SIG RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="64c90-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="64c90-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="64c90-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="64c90-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="64c90-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="64c90-121">**Modify**</span></span>                         | <span data-ttu-id="64c90-122">將 TTL、對應旗標、查閱超時、快取超時和結果網域更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="64c90-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="64c90-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="64c90-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="64c90-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="64c90-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="64c90-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="64c90-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="64c90-126">**Windows Server 2003：** 這個方法也會將 TypeCovered、演算法、標籤、OriginalTTL、SignatureExpiration、SignatureInception、KeyTag、SignerName 和簽章更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="64c90-126">**Windows Server 2003:** This method also updates the TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName and Signature to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="64c90-127">屬性</span><span class="sxs-lookup"><span data-stu-id="64c90-127">Properties</span></span>

<span data-ttu-id="64c90-128">**MicrosoftDNS \_ SIGType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="64c90-128">The **MicrosoftDNS\_SIGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64c90-129">**演算法**</span><span class="sxs-lookup"><span data-stu-id="64c90-129">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c90-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c90-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c90-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c90-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c90-132">與資源記錄中指定的金鑰搭配使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="64c90-132">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="64c90-133">指派的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="64c90-133">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="64c90-134">值</span><span class="sxs-lookup"><span data-stu-id="64c90-134">Value</span></span>                                                                                                | <span data-ttu-id="64c90-135">意義</span><span class="sxs-lookup"><span data-stu-id="64c90-135">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="64c90-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="64c90-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="64c90-137">RSA/MD5 (RFC 2537) </span><span class="sxs-lookup"><span data-stu-id="64c90-137">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="64c90-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="64c90-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="64c90-139">Diffie-Hellman (RFC 2539) </span><span class="sxs-lookup"><span data-stu-id="64c90-139">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="64c90-140"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="64c90-140"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="64c90-141">DSA (RFC 2536) </span><span class="sxs-lookup"><span data-stu-id="64c90-141">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="64c90-142"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="64c90-142"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="64c90-143">橢圓曲線密碼編譯</span><span class="sxs-lookup"><span data-stu-id="64c90-143">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="64c90-144">**KeyTag**</span><span class="sxs-lookup"><span data-stu-id="64c90-144">**KeyTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c90-145">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c90-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c90-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c90-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c90-147">方法，用來選擇驗證 SIG 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="64c90-147">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="64c90-148">如需用來計算 KeyTag 的方法，請參閱 RFC 2535、附錄 C。</span><span class="sxs-lookup"><span data-stu-id="64c90-148">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="64c90-149">**標籤**</span><span class="sxs-lookup"><span data-stu-id="64c90-149">**Labels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c90-150">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c90-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c90-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c90-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c90-152">原始 SIG RR 擁有者名稱中的標籤計數（不帶正負號）。</span><span class="sxs-lookup"><span data-stu-id="64c90-152">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="64c90-153">此計數不包含根的 Null 標籤，也不包含任何初始萬用字元。</span><span class="sxs-lookup"><span data-stu-id="64c90-153">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="64c90-154">**OriginalTTL**</span><span class="sxs-lookup"><span data-stu-id="64c90-154">**OriginalTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c90-155">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64c90-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64c90-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c90-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c90-157">由 SIG 簽署之 RR 集合的 TTL。</span><span class="sxs-lookup"><span data-stu-id="64c90-157">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="64c90-158">**簽名**</span><span class="sxs-lookup"><span data-stu-id="64c90-158">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c90-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c90-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c90-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c90-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c90-161">以 base 64 表示的簽章，格式如 RFC 2535 中所定義，附錄 A。</span><span class="sxs-lookup"><span data-stu-id="64c90-161">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="64c90-162">**SignatureExpiration**</span><span class="sxs-lookup"><span data-stu-id="64c90-162">**SignatureExpiration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c90-163">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64c90-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64c90-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c90-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c90-165">簽章到期日（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。</span><span class="sxs-lookup"><span data-stu-id="64c90-165">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="64c90-166">**SignatureInception**</span><span class="sxs-lookup"><span data-stu-id="64c90-166">**SignatureInception**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c90-167">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64c90-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64c90-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c90-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c90-169">簽章變成有效的日期和時間（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。</span><span class="sxs-lookup"><span data-stu-id="64c90-169">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="64c90-170">**SignerName**</span><span class="sxs-lookup"><span data-stu-id="64c90-170">**SignerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c90-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c90-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c90-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c90-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c90-173">產生 SIG RR 之簽署者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="64c90-173">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="64c90-174">**TypeCovered**</span><span class="sxs-lookup"><span data-stu-id="64c90-174">**TypeCovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c90-175">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c90-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c90-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c90-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c90-177">此 SIG 所涵蓋的 RR 類型。</span><span class="sxs-lookup"><span data-stu-id="64c90-177">Type of RR covered by this SIG.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64c90-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="64c90-178">Requirements</span></span>



| <span data-ttu-id="64c90-179">需求</span><span class="sxs-lookup"><span data-stu-id="64c90-179">Requirement</span></span> | <span data-ttu-id="64c90-180">值</span><span class="sxs-lookup"><span data-stu-id="64c90-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64c90-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64c90-181">Minimum supported client</span></span><br/> | <span data-ttu-id="64c90-182">都不支援</span><span class="sxs-lookup"><span data-stu-id="64c90-182">None supported</span></span><br/>                                                              |
| <span data-ttu-id="64c90-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64c90-183">Minimum supported server</span></span><br/> | <span data-ttu-id="64c90-184">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64c90-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="64c90-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="64c90-185">Namespace</span></span><br/>                | <span data-ttu-id="64c90-186">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="64c90-186">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="64c90-187">MOF</span><span class="sxs-lookup"><span data-stu-id="64c90-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64c90-188"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="64c90-188"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64c90-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64c90-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c90-190">**MicrosoftDNS SIGType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="64c90-190">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="64c90-191">**Modify MicrosoftDNS \_ SIGType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="64c90-191">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="64c90-192">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="64c90-192">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





