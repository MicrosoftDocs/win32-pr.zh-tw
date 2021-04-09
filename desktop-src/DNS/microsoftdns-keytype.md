---
title: MicrosoftDNS_KEYType 類別
description: '\_代表金鑰資源記錄之 MicrosoftDNS ResourceRecord 的子類別。'
ms.assetid: d3fa1f35-fa0a-47ee-b2be-4464b9b21d80
keywords:
- MicrosoftDNS_KEYType 類別 DNS
- MicrosoftDNS_KEYType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
- MicrosoftDNS_KEYType.Modify
- MicrosoftDNS_KEYType.Flags
- MicrosoftDNS_KEYType.Protocol
- MicrosoftDNS_KEYType.Algorithm
- MicrosoftDNS_KEYType.PublicKey
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e814af1d22820f1722e5812dd314dd1c7f6e0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843775"
---
# <a name="microsoftdns_keytype-class"></a><span data-ttu-id="fb221-105">MicrosoftDNS \_ KEYType 類別</span><span class="sxs-lookup"><span data-stu-id="fb221-105">MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="fb221-106">代表金鑰資源記錄之 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 的子類別。</span><span class="sxs-lookup"><span data-stu-id="fb221-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a KEY Resource Record.</span></span>

<span data-ttu-id="fb221-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="fb221-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb221-108">語法</span><span class="sxs-lookup"><span data-stu-id="fb221-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_KEYType : MicrosoftDNS_ResourceRecord
{
  uint16 Flags;
  uint16 Protocol;
  uint16 Algorithm;
  string PublicKey;
};
```

## <a name="members"></a><span data-ttu-id="fb221-109">成員</span><span class="sxs-lookup"><span data-stu-id="fb221-109">Members</span></span>

<span data-ttu-id="fb221-110">**MicrosoftDNS \_ KEYType** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fb221-110">The **MicrosoftDNS\_KEYType** class has these types of members:</span></span>

-   [<span data-ttu-id="fb221-111">方法</span><span class="sxs-lookup"><span data-stu-id="fb221-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fb221-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fb221-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fb221-113">方法</span><span class="sxs-lookup"><span data-stu-id="fb221-113">Methods</span></span>

<span data-ttu-id="fb221-114">**MicrosoftDNS \_ KEYType** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fb221-114">The **MicrosoftDNS\_KEYType** class has these methods.</span></span>



| <span data-ttu-id="fb221-115">方法</span><span class="sxs-lookup"><span data-stu-id="fb221-115">Method</span></span>                             | <span data-ttu-id="fb221-116">描述</span><span class="sxs-lookup"><span data-stu-id="fb221-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb221-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fb221-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fb221-118">根據方法的輸入參數中的資料具現化金鑰資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設 = IN) 、存留時間值，以及 WINS 對應旗標、反向查閱超時、WINS 快取超時和要附加的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="fb221-118">Instantiates a KEY Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="fb221-119">它會將新物件的參考傳回做為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="fb221-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fb221-120">限定詞：實作為、靜態</span><span class="sxs-lookup"><span data-stu-id="fb221-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fb221-121">**修改**</span><span class="sxs-lookup"><span data-stu-id="fb221-121">**Modify**</span></span>                         | <span data-ttu-id="fb221-122">將 TTL、對應旗標、查閱超時、快取超時和結果網域，更新為指定為此方法之輸入參數的值。</span><span class="sxs-lookup"><span data-stu-id="fb221-122">Updates the TTL, mapping flag, look-up time out, cache time out, and result domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fb221-123">如果未指定參數的新值，則不會變更參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="fb221-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fb221-124">方法會將修改過之物件的參考傳回為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="fb221-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fb221-125">限定詞：實作為</span><span class="sxs-lookup"><span data-stu-id="fb221-125">Qualifiers: Implemented</span></span><br/>                          |



 

### <a name="properties"></a><span data-ttu-id="fb221-126">屬性</span><span class="sxs-lookup"><span data-stu-id="fb221-126">Properties</span></span>

<span data-ttu-id="fb221-127">**MicrosoftDNS \_ KEYType** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fb221-127">The **MicrosoftDNS\_KEYType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb221-128">**演算法**</span><span class="sxs-lookup"><span data-stu-id="fb221-128">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb221-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fb221-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb221-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb221-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb221-131">與資源記錄中指定的金鑰搭配使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="fb221-131">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="fb221-132">指派的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="fb221-132">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="fb221-133">值</span><span class="sxs-lookup"><span data-stu-id="fb221-133">Value</span></span>                                                                                                | <span data-ttu-id="fb221-134">意義</span><span class="sxs-lookup"><span data-stu-id="fb221-134">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="fb221-135"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-135"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="fb221-136">RSA/MD5 (RFC 2537) </span><span class="sxs-lookup"><span data-stu-id="fb221-136">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="fb221-137"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-137"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="fb221-138">Diffie-Hellman (RFC 2539) </span><span class="sxs-lookup"><span data-stu-id="fb221-138">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="fb221-139"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-139"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="fb221-140">DSA (RFC 2536) </span><span class="sxs-lookup"><span data-stu-id="fb221-140">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="fb221-141"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-141"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="fb221-142">橢圓曲線密碼編譯</span><span class="sxs-lookup"><span data-stu-id="fb221-142">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb221-143">**旗標**</span><span class="sxs-lookup"><span data-stu-id="fb221-143">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb221-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fb221-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb221-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb221-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb221-146">用來指定對應的旗標，如 IETF RFC 2535 中所述。</span><span class="sxs-lookup"><span data-stu-id="fb221-146">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="fb221-147">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="fb221-147">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb221-148">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fb221-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb221-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb221-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb221-150">可以使用資源記錄中所指定金鑰的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fb221-150">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="fb221-151">指派的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="fb221-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="fb221-152">值</span><span class="sxs-lookup"><span data-stu-id="fb221-152">Value</span></span>                                                                                                    | <span data-ttu-id="fb221-153">意義</span><span class="sxs-lookup"><span data-stu-id="fb221-153">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="fb221-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-154"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="fb221-155">TLS</span><span class="sxs-lookup"><span data-stu-id="fb221-155">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="fb221-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-156"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="fb221-157">電子郵件</span><span class="sxs-lookup"><span data-stu-id="fb221-157">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="fb221-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-158"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="fb221-159">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="fb221-159">DNSSEC</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="fb221-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-160"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="fb221-161">IPsec</span><span class="sxs-lookup"><span data-stu-id="fb221-161">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="fb221-162"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-162"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="fb221-163">所有通訊協定</span><span class="sxs-lookup"><span data-stu-id="fb221-163">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb221-164">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="fb221-164">**PublicKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb221-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fb221-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb221-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb221-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb221-167">公開金鑰，以基底64表示，如 RFC 2535 的附錄 A 所述。</span><span class="sxs-lookup"><span data-stu-id="fb221-167">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb221-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb221-168">Requirements</span></span>



| <span data-ttu-id="fb221-169">需求</span><span class="sxs-lookup"><span data-stu-id="fb221-169">Requirement</span></span> | <span data-ttu-id="fb221-170">值</span><span class="sxs-lookup"><span data-stu-id="fb221-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb221-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb221-171">Minimum supported client</span></span><br/> | <span data-ttu-id="fb221-172">都不支援</span><span class="sxs-lookup"><span data-stu-id="fb221-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fb221-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb221-173">Minimum supported server</span></span><br/> | <span data-ttu-id="fb221-174">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb221-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fb221-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="fb221-175">Namespace</span></span><br/>                | <span data-ttu-id="fb221-176">根 \\ MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="fb221-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fb221-177">MOF</span><span class="sxs-lookup"><span data-stu-id="fb221-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb221-178"><dt>Dnsprov mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb221-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb221-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb221-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb221-180">**MicrosoftDNS KEYType 類別的 CreateInstanceFromPropertyData 方法 \_**</span><span class="sxs-lookup"><span data-stu-id="fb221-180">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fb221-181">**Modify MicrosoftDNS \_ KEYType 類別的方法**</span><span class="sxs-lookup"><span data-stu-id="fb221-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="fb221-182">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="fb221-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





