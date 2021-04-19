---
description: 憑證註冊 API 支援下列屬性。 您可以使用下列各節中所識別的對應介面，建立個別的屬性。
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: 支援的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bfff5785a0b891e98e6d78d59b4688e2d5c11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972439"
---
# <a name="supported-attributes"></a><span data-ttu-id="da725-104">支援的屬性</span><span class="sxs-lookup"><span data-stu-id="da725-104">Supported Attributes</span></span>

<span data-ttu-id="da725-105">憑證註冊 API 支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="da725-105">The Certificate Enrollment API supports the following attributes.</span></span> <span data-ttu-id="da725-106">您可以使用下列各節中所識別的對應介面，建立個別的屬性。</span><span class="sxs-lookup"><span data-stu-id="da725-106">You can create an individual attribute by using the corresponding interface identified in each of the following sections.</span></span>

## <a name="clientid"></a><span data-ttu-id="da725-107">ClientId</span><span class="sxs-lookup"><span data-stu-id="da725-107">ClientId</span></span>

<span data-ttu-id="da725-108">[**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)介面可用來定義屬性，其中包含傳送憑證要求之用戶端電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da725-108">The [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) interface can be used to define an attribute that contains information about the client computer that sent the certificate request.</span></span> <span data-ttu-id="da725-109">您可以使用此資訊進行診斷。</span><span class="sxs-lookup"><span data-stu-id="da725-109">The information can be used for diagnostics.</span></span>

<span data-ttu-id="da725-110">**適用于：** PKCS \# 10 或 CMC 要求。</span><span class="sxs-lookup"><span data-stu-id="da725-110">**Applies To:** PKCS \#10 or CMC request.</span></span>

<span data-ttu-id="da725-111">**OID：** XCN \_ OID \_ 要求 \_ 用戶端 \_ 資訊 (1.3.6.1.4.1.311.21.20) </span><span class="sxs-lookup"><span data-stu-id="da725-111">**OID:** XCN\_OID\_REQUEST\_CLIENT\_INFO (1.3.6.1.4.1.311.21.20)</span></span>

## <a name="extensions"></a><span data-ttu-id="da725-112">延伸模組</span><span class="sxs-lookup"><span data-stu-id="da725-112">Extensions</span></span>

<span data-ttu-id="da725-113">[**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)介面可以用來定義一組 x.509 第3版憑證延伸。</span><span class="sxs-lookup"><span data-stu-id="da725-113">The [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface can be used to define a set of X.509 version 3 certificate extensions.</span></span> <span data-ttu-id="da725-114">支援下列擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da725-114">The following extensions are supported.</span></span> <span data-ttu-id="da725-115">如需詳細資訊，請參閱擴充介面主題。</span><span class="sxs-lookup"><span data-stu-id="da725-115">For more information, see the Extension Interfaces topic.</span></span>



| <span data-ttu-id="da725-116">分機</span><span class="sxs-lookup"><span data-stu-id="da725-116">Extension</span></span>              | <span data-ttu-id="da725-117">Description</span><span class="sxs-lookup"><span data-stu-id="da725-117">Description</span></span>                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da725-118">AlternativeNames</span><span class="sxs-lookup"><span data-stu-id="da725-118">AlternativeNames</span></span>       | <span data-ttu-id="da725-119">包含與憑證相關聯之簽發者的一或多個替代名稱形式。</span><span class="sxs-lookup"><span data-stu-id="da725-119">Contains one or more alternative name forms of the issuer associated with the certificate.</span></span>                                                                                                                                       |
| <span data-ttu-id="da725-120">AuthorityKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="da725-120">AuthorityKeyIdentifier</span></span> | <span data-ttu-id="da725-121">包含唯一的索引鍵識別碼，用來區分 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 的多個憑證簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="da725-121">Contains a unique key identifier to differentiate between multiple certificate signing keys of the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span> |
| <span data-ttu-id="da725-122">BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="da725-122">BasicConstraints</span></span>       | <span data-ttu-id="da725-123">指出主體是否可作為 CA。</span><span class="sxs-lookup"><span data-stu-id="da725-123">Indicates whether the subject can act as a CA.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="da725-124">CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="da725-124">CertificatePolicies</span></span>    | <span data-ttu-id="da725-125">識別與憑證相關聯的原則和選用的辨識符號資訊。</span><span class="sxs-lookup"><span data-stu-id="da725-125">Identifies the policies and optional qualifier information associated with the certificate.</span></span>                                                                                                                                      |
| <span data-ttu-id="da725-126">MSApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="da725-126">MSApplicationPolicies</span></span>  | <span data-ttu-id="da725-127">識別憑證的一或多個用途。</span><span class="sxs-lookup"><span data-stu-id="da725-127">Identifies one or more uses for the certificate.</span></span> <span data-ttu-id="da725-128">此延伸模組類似于 EnhancedKeyUsage 延伸模組，但卻是由 Microsoft 定義。</span><span class="sxs-lookup"><span data-stu-id="da725-128">This extension is similar to the EnhancedKeyUsage extension but is Microsoft-defined.</span></span>                                                                                           |
| <span data-ttu-id="da725-129">EnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="da725-129">EnhancedKeyUsage</span></span>       | <span data-ttu-id="da725-130">識別憑證中包含之公開金鑰的一或多個用法。</span><span class="sxs-lookup"><span data-stu-id="da725-130">Identifies one or more uses of the public key contained in the certificate.</span></span> <span data-ttu-id="da725-131">除了金鑰使用延伸模組之外，還可以使用增強金鑰使用方法擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da725-131">The enhanced key usage extension can be used in addition to or in place of the key usage extension.</span></span>                                                  |
| <span data-ttu-id="da725-132">KeyUsage</span><span class="sxs-lookup"><span data-stu-id="da725-132">KeyUsage</span></span>               | <span data-ttu-id="da725-133">識別憑證中包含的公開金鑰可執行之作業的限制。</span><span class="sxs-lookup"><span data-stu-id="da725-133">Identifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                                                  |
| <span data-ttu-id="da725-134">SmimeCapabilities</span><span class="sxs-lookup"><span data-stu-id="da725-134">SmimeCapabilities</span></span>      | <span data-ttu-id="da725-135">將電子郵件收件者的解密功能報告給電子郵件寄件者，讓寄件者選擇雙方所支援之最安全的對稱演算法。</span><span class="sxs-lookup"><span data-stu-id="da725-135">Reports the decryption capabilities of an email recipient to the email sender to enable the sender to choose the most secure symmetric algorithm supported by both parties.</span></span>                                                      |
| <span data-ttu-id="da725-136">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="da725-136">SubjectKeyIdentifier</span></span>   | <span data-ttu-id="da725-137">包含唯一金鑰識別碼，可用來區分與憑證擁有者相關聯的多個簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="da725-137">Contains a unique key identifier that can be used to differentiate between multiple signing keys associated with the certificate owner.</span></span>                                                                                          |
| <span data-ttu-id="da725-138">範本</span><span class="sxs-lookup"><span data-stu-id="da725-138">Template</span></span>               | <span data-ttu-id="da725-139">識別發行或更新憑證時要使用的範本。</span><span class="sxs-lookup"><span data-stu-id="da725-139">Identifies the template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="da725-140">延伸模組包含範本 (OID) 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="da725-140">The extension contains the object identifier (OID) of the template.</span></span>                                                                                       |
| <span data-ttu-id="da725-141">TemplateName</span><span class="sxs-lookup"><span data-stu-id="da725-141">TemplateName</span></span>           | <span data-ttu-id="da725-142">識別發行或更新憑證時要使用的範本。</span><span class="sxs-lookup"><span data-stu-id="da725-142">Identifies the template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="da725-143">延伸模組包含範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="da725-143">The extension contains the name of the template.</span></span>                                                                                                          |



 

<span data-ttu-id="da725-144">**適用于：** PKCS \# 10 要求。</span><span class="sxs-lookup"><span data-stu-id="da725-144">**Applies To:** PKCS \#10 request.</span></span>

<span data-ttu-id="da725-145">**OID：** XCN \_ OID \_ RSA \_ certExtensions (1.2.840.113549.1.9.14) </span><span class="sxs-lookup"><span data-stu-id="da725-145">**OID:** XCN\_OID\_RSA\_certExtensions (1.2.840.113549.1.9.14)</span></span>

## <a name="archivekey"></a><span data-ttu-id="da725-146">ArchiveKey</span><span class="sxs-lookup"><span data-stu-id="da725-146">ArchiveKey</span></span>

<span data-ttu-id="da725-147">[**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)介面可用來定義屬性，其中包含提交給 CA 以進行封存的加密私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="da725-147">The [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) interface can be used to define an attribute that contains an encrypted private key submitted to a CA for archiving.</span></span>

<span data-ttu-id="da725-148">**適用于：** CMC 要求。</span><span class="sxs-lookup"><span data-stu-id="da725-148">**Applies To:** CMC request.</span></span>

<span data-ttu-id="da725-149">**OID：** XCN \_ OID \_ 封存 \_ 金鑰 \_ ATTR (1.3.6.1.4.1.311.21.13) </span><span class="sxs-lookup"><span data-stu-id="da725-149">**OID:** XCN\_OID\_ARCHIVED\_KEY\_ATTR (1.3.6.1.4.1.311.21.13)</span></span>

## <a name="archivekeyhash"></a><span data-ttu-id="da725-150">ArchiveKeyHash</span><span class="sxs-lookup"><span data-stu-id="da725-150">ArchiveKeyHash</span></span>

<span data-ttu-id="da725-151">[**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)介面可以用來定義 **ArchiveKey** 屬性中所包含之私密金鑰的雜湊。</span><span class="sxs-lookup"><span data-stu-id="da725-151">The [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) interface can be used to define a hash of the private key contained in the **ArchiveKey** attribute.</span></span>

<span data-ttu-id="da725-152">**適用于：** CMC 要求。</span><span class="sxs-lookup"><span data-stu-id="da725-152">**Applies To:** CMC request.</span></span>

<span data-ttu-id="da725-153">**OID：** XCN \_ OID \_ ENCRYPTED \_ KEY \_ HASH (1.3.6.1.4.1.311.21.21) </span><span class="sxs-lookup"><span data-stu-id="da725-153">**OID:** XCN\_OID\_ENCRYPTED\_KEY\_HASH (1.3.6.1.4.1.311.21.21)</span></span>

## <a name="cspprovider"></a><span data-ttu-id="da725-154">CspProvider</span><span class="sxs-lookup"><span data-stu-id="da725-154">CspProvider</span></span>

<span data-ttu-id="da725-155">[**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)介面可用來定義屬性，其中包含要求者用來進行密碼編譯作業之 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) (CSP) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da725-155">The [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) interface can be used to define an attribute that contains information about the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) used by the requester for cryptographic operations.</span></span>

<span data-ttu-id="da725-156">**適用于：** PKCS \# 10 要求。</span><span class="sxs-lookup"><span data-stu-id="da725-156">**Applies To:** PKCS \#10 request.</span></span> <span data-ttu-id="da725-157">當您建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件時，會自動建立這個屬性。</span><span class="sxs-lookup"><span data-stu-id="da725-157">This attribute is automatically created when you create an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>

<span data-ttu-id="da725-158">**OID：** XCN \_ OID \_ 註冊 \_ CSP \_ 提供者 (1.3.6.1.4.1.311.13.2.2) </span><span class="sxs-lookup"><span data-stu-id="da725-158">**OID:** XCN\_OID\_ENROLLMENT\_CSP\_PROVIDER (1.3.6.1.4.1.311.13.2.2)</span></span>

## <a name="osversion"></a><span data-ttu-id="da725-159">OSVersion</span><span class="sxs-lookup"><span data-stu-id="da725-159">OSVersion</span></span>

<span data-ttu-id="da725-160">[**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)介面可以用來建立包含用戶端作業系統版本資訊的屬性。</span><span class="sxs-lookup"><span data-stu-id="da725-160">The [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) interface can be used to create an attribute that contains version information about the client operating system.</span></span> <span data-ttu-id="da725-161">CA 可以使用此資訊來決定建立憑證時要套用的處理類型。</span><span class="sxs-lookup"><span data-stu-id="da725-161">The information can be used by the CA to determine the type of processing to apply when creating the certificate.</span></span>

<span data-ttu-id="da725-162">**適用于：** PKCS \# 10 或 CMC 要求。</span><span class="sxs-lookup"><span data-stu-id="da725-162">**Applies To:** PKCS \#10 or CMC request.</span></span>

<span data-ttu-id="da725-163">**OID：** XCN \_ OID \_ OS \_ VERSION (1.3.6.1.4.1.311.13.2.3) </span><span class="sxs-lookup"><span data-stu-id="da725-163">**OID:** XCN\_OID\_OS\_VERSION (1.3.6.1.4.1.311.13.2.3)</span></span>

## <a name="renewalcertificate"></a><span data-ttu-id="da725-164">RenewalCertificate</span><span class="sxs-lookup"><span data-stu-id="da725-164">RenewalCertificate</span></span>

<span data-ttu-id="da725-165">[**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)介面可以用來建立包含要更新之憑證的屬性。</span><span class="sxs-lookup"><span data-stu-id="da725-165">The [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) interface can be used to create an attribute that contains the certificate being renewed.</span></span>

<span data-ttu-id="da725-166">**適用于：** PKCS \# 10 要求。</span><span class="sxs-lookup"><span data-stu-id="da725-166">**Applies To:** PKCS \#10 request.</span></span> <span data-ttu-id="da725-167">如果您藉 \# 由使用正在更新的憑證來初始化 PKCS 10 要求來建立 PKCS 10 要求，就會自動建立這個屬性。</span><span class="sxs-lookup"><span data-stu-id="da725-167">This attribute is automatically created if you create a PKCS \#10 request by initiating it with the certificate being renewed.</span></span>

<span data-ttu-id="da725-168">**OID：** XCN \_ OID \_ 更新 \_ 憑證 (1.3.6.1.4.1.311.13.1) </span><span class="sxs-lookup"><span data-stu-id="da725-168">**OID:** XCN\_OID\_RENEWAL\_CERTIFICATE (1.3.6.1.4.1.311.13.1)</span></span>

 

 
