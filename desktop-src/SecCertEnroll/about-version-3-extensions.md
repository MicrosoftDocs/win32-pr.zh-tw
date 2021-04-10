---
description: X.509 版本 3 憑證包含版本 1 和版本 2 中定義的欄位，並新增憑證延伸。 下列範例顯示的是憑證延伸的 asn.1 語法。
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: 第3版擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192743"
---
# <a name="version-3-extensions"></a><span data-ttu-id="8fc16-104">第3版擴充功能</span><span class="sxs-lookup"><span data-stu-id="8fc16-104">Version 3 Extensions</span></span>

<span data-ttu-id="8fc16-105">X.509 版本 3 憑證包含版本 1 和版本 2 中定義的欄位，並新增憑證延伸。</span><span class="sxs-lookup"><span data-stu-id="8fc16-105">An X.509 version 3 certificate contains the fields defined in version 1 and version 2 and adds certificate extensions.</span></span> <span data-ttu-id="8fc16-106">下列範例顯示的是憑證延伸的 asn.1 語法。</span><span class="sxs-lookup"><span data-stu-id="8fc16-106">The ASN.1 syntax of certificate extensions is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

<span data-ttu-id="8fc16-107">下表列出標準的第3版擴充功能及其 (Oid) 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fc16-107">The standard version 3 extensions and their object identifiers (OIDs) are listed in the following table.</span></span> <span data-ttu-id="8fc16-108">Microsoft 支援這些功能，並包含額外的自訂擴充功能。</span><span class="sxs-lookup"><span data-stu-id="8fc16-108">Microsoft supports these and includes additional custom extensions.</span></span> <span data-ttu-id="8fc16-109">如需詳細資訊，請參閱 [擴充](extensions.md)功能。</span><span class="sxs-lookup"><span data-stu-id="8fc16-109">For more information, see [Extensions](extensions.md).</span></span>

| <span data-ttu-id="8fc16-110">分機</span><span class="sxs-lookup"><span data-stu-id="8fc16-110">Extension</span></span>                                         | <span data-ttu-id="8fc16-111">Description</span><span class="sxs-lookup"><span data-stu-id="8fc16-111">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc16-112">授權單位金鑰識別碼 (2.5.29.19) </span><span class="sxs-lookup"><span data-stu-id="8fc16-112">Authority Key Identifier(2.5.29.19)</span></span><br/>    | <span data-ttu-id="8fc16-113">識別憑證授權單位 (CA) 公開金鑰，這個金鑰會對應到用來簽署憑證的 CA 私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="8fc16-113">Identifies the certification authority (CA) public key that corresponds to the CA private key used to sign the certificate.</span></span>                                                                              |
| <span data-ttu-id="8fc16-114">2.5.29.35) 的基本條件約束 (</span><span class="sxs-lookup"><span data-stu-id="8fc16-114">Basic Constraints(2.5.29.35)</span></span><br/>           | <span data-ttu-id="8fc16-115">指定實體是否可以用來做為 CA，如果可以，可以存在於憑證鏈結中該 CA 下方的次級 CA 數目。</span><span class="sxs-lookup"><span data-stu-id="8fc16-115">Specifies whether the entity can be used as a CA and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>                                                           |
| <span data-ttu-id="8fc16-116"> (2.5.29.32) 的憑證原則</span><span class="sxs-lookup"><span data-stu-id="8fc16-116">Certificate Policies(2.5.29.32)</span></span><br/>        | <span data-ttu-id="8fc16-117">指定簽發憑證的原則和憑證的用途。</span><span class="sxs-lookup"><span data-stu-id="8fc16-117">Specifies the policies under which the certificate has been issued and the purposes for which it can be used.</span></span>                                                                                            |
| <span data-ttu-id="8fc16-118">CRL 發佈點 (2.5.29.31) </span><span class="sxs-lookup"><span data-stu-id="8fc16-118">CRL Distribution Points(2.5.29.31)</span></span><br/>     | <span data-ttu-id="8fc16-119">包含基底 [*憑證撤銷清單*](/windows/desktop/SecGloss/c-gly) 的 URI (CRL) 。</span><span class="sxs-lookup"><span data-stu-id="8fc16-119">Contains the URI of the base [*certificate revocation list*](/windows/desktop/SecGloss/c-gly) (CRL).</span></span>                                  |
| <span data-ttu-id="8fc16-120">增強金鑰使用方法 (2.5.29.46) </span><span class="sxs-lookup"><span data-stu-id="8fc16-120">Enhanced Key Usage(2.5.29.46)</span></span><br/>          | <span data-ttu-id="8fc16-121">指定憑證所含公開金鑰的使用方法。</span><span class="sxs-lookup"><span data-stu-id="8fc16-121">Specifies the manner in which the public key contained in the certificate can be used.</span></span>                                                                                                                   |
| <span data-ttu-id="8fc16-122">簽發者替代名稱 (2.5.29.8) </span><span class="sxs-lookup"><span data-stu-id="8fc16-122">Issuer Alternative Name(2.5.29.8)</span></span><br/>      | <span data-ttu-id="8fc16-123">針對憑證要求的簽發者指定一或多個別名形式。</span><span class="sxs-lookup"><span data-stu-id="8fc16-123">Specifies one or more alternative name forms for the issuer of the certificate request.</span></span>                                                                                                                  |
| <span data-ttu-id="8fc16-124">金鑰使用方法 (2.5.29.15) </span><span class="sxs-lookup"><span data-stu-id="8fc16-124">Key Usage(2.5.29.15)</span></span><br/>                   | <span data-ttu-id="8fc16-125">指定憑證中所含公開金鑰可以執行的操作限制。</span><span class="sxs-lookup"><span data-stu-id="8fc16-125">Specifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                           |
| <span data-ttu-id="8fc16-126">名稱條件約束 (2.5.29.30) </span><span class="sxs-lookup"><span data-stu-id="8fc16-126">Name Constraints(2.5.29.30)</span></span><br/>            | <span data-ttu-id="8fc16-127">指定憑證階層中所有主體名稱必須放置的命名空間。</span><span class="sxs-lookup"><span data-stu-id="8fc16-127">Specifies the namespace within which all subject names in a certificate hierarchy must be located.</span></span> <span data-ttu-id="8fc16-128">這個延伸只能用於一個 CA 憑證中。</span><span class="sxs-lookup"><span data-stu-id="8fc16-128">The extension is used only in a CA certificate.</span></span>                                                       |
| <span data-ttu-id="8fc16-129">原則條件約束 (2.5.29.36) </span><span class="sxs-lookup"><span data-stu-id="8fc16-129">Policy Constraints(2.5.29.36)</span></span><br/>          | <span data-ttu-id="8fc16-130">透過禁止原則對應，或是要求階層中的每個憑證包含可接受的原則識別碼來限制路徑驗證。</span><span class="sxs-lookup"><span data-stu-id="8fc16-130">Constrains path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span> <span data-ttu-id="8fc16-131">這個延伸只能用於一個 CA 憑證中。</span><span class="sxs-lookup"><span data-stu-id="8fc16-131">The extension is used only in a CA certificate.</span></span> |
| <span data-ttu-id="8fc16-132">原則對應 (2.5.29.33) </span><span class="sxs-lookup"><span data-stu-id="8fc16-132">Policy Mappings(2.5.29.33)</span></span><br/>             | <span data-ttu-id="8fc16-133">指定次級 CA 中的原則，這個次級 CA 會對應到發行 CA 中的原則。</span><span class="sxs-lookup"><span data-stu-id="8fc16-133">Specifies the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span>                                                                                                                |
| <span data-ttu-id="8fc16-134">私密金鑰使用期間 (2.5.29.16) </span><span class="sxs-lookup"><span data-stu-id="8fc16-134">Private Key Usage Period(2.5.29.16)</span></span><br/>    | <span data-ttu-id="8fc16-135">指定私密金鑰的有效期間，且要與該私密金鑰相關聯憑證不同的有效期間。</span><span class="sxs-lookup"><span data-stu-id="8fc16-135">Specifies a different validity period for the private key than for the certificate with which the private key is associated.</span></span>                                                                             |
| <span data-ttu-id="8fc16-136">2.5.29.17) 的主體替代名稱 (</span><span class="sxs-lookup"><span data-stu-id="8fc16-136">Subject Alternative Name(2.5.29.17)</span></span><br/>    | <span data-ttu-id="8fc16-137">針對憑證要求的主體指定一或多個別名形式。</span><span class="sxs-lookup"><span data-stu-id="8fc16-137">Specifies one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="8fc16-138">別名形式範例包含電子郵件地址、DNS 名稱、IP 位址及 URI。</span><span class="sxs-lookup"><span data-stu-id="8fc16-138">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>                           |
| <span data-ttu-id="8fc16-139">主體目錄屬性 (2.5.29.9) </span><span class="sxs-lookup"><span data-stu-id="8fc16-139">Subject Directory Attributes(2.5.29.9)</span></span><br/> | <span data-ttu-id="8fc16-140">傳遞身分識別屬性，例如憑證主體的國籍。</span><span class="sxs-lookup"><span data-stu-id="8fc16-140">Conveys identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="8fc16-141">延伸值是 OID 值配對的序列。</span><span class="sxs-lookup"><span data-stu-id="8fc16-141">The extension value is a sequence of OID-value pairs.</span></span>                                                              |
| <span data-ttu-id="8fc16-142">主體金鑰識別碼 (2.5.29.14) </span><span class="sxs-lookup"><span data-stu-id="8fc16-142">Subject Key Identifier(2.5.29.14)</span></span><br/>      | <span data-ttu-id="8fc16-143">區別憑證主體持有的多個公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="8fc16-143">Differentiates between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="8fc16-144">延伸值通常是金鑰的 SHA-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="8fc16-144">The extension value is typically a SHA-1 hash of the key.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="8fc16-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="8fc16-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fc16-146">基本欄位</span><span class="sxs-lookup"><span data-stu-id="8fc16-146">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="8fc16-147">第2版欄位</span><span class="sxs-lookup"><span data-stu-id="8fc16-147">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="8fc16-148">X.509 公開金鑰憑證</span><span class="sxs-lookup"><span data-stu-id="8fc16-148">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

