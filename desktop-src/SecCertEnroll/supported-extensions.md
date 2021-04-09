---
description: 您可以使用 IX509Extension 介面來定義任意的延伸模組。
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: 支援的延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690759"
---
# <a name="supported-extensions"></a><span data-ttu-id="057e4-103">支援的延伸模組</span><span class="sxs-lookup"><span data-stu-id="057e4-103">Supported Extensions</span></span>

<span data-ttu-id="057e4-104">您可以使用 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 介面來定義任意的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="057e4-104">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an arbitrary extension.</span></span> <span data-ttu-id="057e4-105">憑證註冊 API 也提供衍生自 **IX509Extension** 的介面，可讓您輕鬆地建立任何最常見的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="057e4-105">The Certificate Enrollment API also provides interfaces derived from **IX509Extension** to enable you to easily create any of the most common extensions.</span></span> <span data-ttu-id="057e4-106">下列清單會識別 Microsoft 憑證授權單位單位所支援的通用擴充功能，以及您可以用來建立它們的物件識別碼和介面。</span><span class="sxs-lookup"><span data-stu-id="057e4-106">The following list identifies the common extensions supported by Microsoft certification authorities, and the object identifiers and interfaces that you can use to create them.</span></span>

## <a name="alternativenames"></a><span data-ttu-id="057e4-107">AlternativeNames</span><span class="sxs-lookup"><span data-stu-id="057e4-107">AlternativeNames</span></span>

<span data-ttu-id="057e4-108">替代名稱延伸可以用來針對憑證要求的主體定義一或多個替代名稱表單。</span><span class="sxs-lookup"><span data-stu-id="057e4-108">The alternative names extension can be used to define one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="057e4-109">別名形式範例包含電子郵件地址、DNS 名稱、IP 位址及 URI。</span><span class="sxs-lookup"><span data-stu-id="057e4-109">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>

<span data-ttu-id="057e4-110">**介面：** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span><span class="sxs-lookup"><span data-stu-id="057e4-110">**Interface:** [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span></span>

<span data-ttu-id="057e4-111">**OID：** XCN \_ OID \_ SUBJECT \_ ALT \_ NAME2 (2.5.29.17) </span><span class="sxs-lookup"><span data-stu-id="057e4-111">**OID:** XCN\_OID\_SUBJECT\_ALT\_NAME2 (2.5.29.17)</span></span>

## <a name="authorityinformationaccess"></a><span data-ttu-id="057e4-112">AuthorityInformationAccess</span><span class="sxs-lookup"><span data-stu-id="057e4-112">AuthorityInformationAccess</span></span>

<span data-ttu-id="057e4-113">授權資訊存取延伸模組會識別如何存取 CA 資訊和服務。</span><span class="sxs-lookup"><span data-stu-id="057e4-113">The authority information access extension identifies how to access CA information and services.</span></span> <span data-ttu-id="057e4-114">擴充值包含一連串的 Uri。</span><span class="sxs-lookup"><span data-stu-id="057e4-114">The extension value contains a sequence of URIs.</span></span>

<span data-ttu-id="057e4-115">**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="057e4-115">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="057e4-116">**OID：** XCN \_ OID \_ 授權單位 \_ 資訊 \_ 存取 (1.3.6.1.5.5.7.1.1) </span><span class="sxs-lookup"><span data-stu-id="057e4-116">**OID:** XCN\_OID\_AUTHORITY\_INFO\_ACCESS (1.3.6.1.5.5.7.1.1)</span></span>

## <a name="authoritykeyidentifier"></a><span data-ttu-id="057e4-117">AuthorityKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="057e4-117">AuthorityKeyIdentifier</span></span>

<span data-ttu-id="057e4-118">授權單位金鑰識別碼延伸可以識別對應至簽署已發行憑證之 CA 私密金鑰的 CA 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="057e4-118">The authority key identifier extension enables identification of the CA public key that corresponds to the CA private key that signed an issued certificate.</span></span> <span data-ttu-id="057e4-119">它是由 Windows server 上的憑證路徑建立軟體用來尋找 CA 憑證。</span><span class="sxs-lookup"><span data-stu-id="057e4-119">It is used by certificate path building software on a Windows server to find the CA certificate.</span></span> <span data-ttu-id="057e4-120">當 CA 發出憑證時，會將擴充值設定為等於 CA 簽署憑證中的 **SubjectKeyIdentifier** 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="057e4-120">When a CA issues a certificate, the extension value is set equal to the **SubjectKeyIdentifier** extension in the CA signing certificate.</span></span> <span data-ttu-id="057e4-121">此值通常是公開金鑰的 SHA-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="057e4-121">The value is typically a SHA-1 hash of the public key.</span></span>

<span data-ttu-id="057e4-122">**介面：** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="057e4-122">**Interface:** [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span></span>

<span data-ttu-id="057e4-123">**OID：** XCN \_ OID \_ 授權單位 \_ 金鑰 \_ IDENTIFIER2 (2.5.29.35) </span><span class="sxs-lookup"><span data-stu-id="057e4-123">**OID:** XCN\_OID\_AUTHORITY\_KEY\_IDENTIFIER2 (2.5.29.35)</span></span>

## <a name="basicconstraints"></a><span data-ttu-id="057e4-124">BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="057e4-124">BasicConstraints</span></span>

<span data-ttu-id="057e4-125">基本限制延伸可以用來識別實體是否可做為憑證授權單位單位 (CA) ，如果是的話，則可以存在於憑證鏈中的次級 Ca 數目。</span><span class="sxs-lookup"><span data-stu-id="057e4-125">The basic constraints extension can be used to identify whether the entity can be used as a certification authority (CA) and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>

<span data-ttu-id="057e4-126">**介面：** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span><span class="sxs-lookup"><span data-stu-id="057e4-126">**Interface:** [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span></span>

<span data-ttu-id="057e4-127">**OID：** XCN \_ OID \_ BASIC \_ CONSTRAINTS2 (2.5.29.19) </span><span class="sxs-lookup"><span data-stu-id="057e4-127">**OID:** XCN\_OID\_BASIC\_CONSTRAINTS2 (2.5.29.19)</span></span>

## <a name="certificatepolicies"></a><span data-ttu-id="057e4-128">CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="057e4-128">CertificatePolicies</span></span>

<span data-ttu-id="057e4-129">憑證原則擴充可以用來識別用來發出憑證的原則，而且可以使用它的用途。</span><span class="sxs-lookup"><span data-stu-id="057e4-129">The certificate policies extension can be used to identify the policies under which the certificate has been issued and the purposes for it can be used.</span></span> <span data-ttu-id="057e4-130">這些是由 (Oid) 的物件識別碼集合所識別。</span><span class="sxs-lookup"><span data-stu-id="057e4-130">These are identified by a collection of object identifiers (OIDs).</span></span> <span data-ttu-id="057e4-131">針對組織的需求自訂原則。</span><span class="sxs-lookup"><span data-stu-id="057e4-131">Policies are customized for the requirements of an organization.</span></span>

<span data-ttu-id="057e4-132">**介面：** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span><span class="sxs-lookup"><span data-stu-id="057e4-132">**Interface:** [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span></span>

<span data-ttu-id="057e4-133">**OID：** XCN \_ OID \_ CERT \_ 原則 (2.5.29.32) </span><span class="sxs-lookup"><span data-stu-id="057e4-133">**OID:** XCN\_OID\_CERT\_POLICIES (2.5.29.32)</span></span>

## <a name="crldistributionpoints"></a><span data-ttu-id="057e4-134">CrlDistributionPoints</span><span class="sxs-lookup"><span data-stu-id="057e4-134">CrlDistributionPoints</span></span>

<span data-ttu-id="057e4-135">憑證撤銷清單 (CRL) 發佈點延伸模組包含基底憑證撤銷清單 (CRL) 的 URI。</span><span class="sxs-lookup"><span data-stu-id="057e4-135">The certificate revocation list (CRL) distribution points extension contains the URI of the base certificate revocation list (CRL).</span></span>

<span data-ttu-id="057e4-136">**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="057e4-136">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="057e4-137">**OID：** XCN \_ OID \_ CRL \_ DIST \_ (2.5.29.31) </span><span class="sxs-lookup"><span data-stu-id="057e4-137">**OID:** XCN\_OID\_CRL\_DIST\_POINTS (2.5.29.31)</span></span>

## <a name="enhancedkeyusage"></a><span data-ttu-id="057e4-138">EnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="057e4-138">EnhancedKeyUsage</span></span>

<span data-ttu-id="057e4-139">[增強金鑰使用方法] 延伸模組可以用來定義憑證中包含之公開金鑰的一或多個用法。</span><span class="sxs-lookup"><span data-stu-id="057e4-139">The enhanced key usage extension can be used to define one or more uses of the public key contained in the certificate.</span></span>

<span data-ttu-id="057e4-140">**介面：** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span><span class="sxs-lookup"><span data-stu-id="057e4-140">**Interface:** [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span></span>

<span data-ttu-id="057e4-141">**OID：** XCN \_ OID \_ 增強 \_ 金鑰 \_ 使用方法 (2.5.29.37) </span><span class="sxs-lookup"><span data-stu-id="057e4-141">**OID:** XCN\_OID\_ENHANCED\_KEY\_USAGE (2.5.29.37)</span></span>

## <a name="freshestcrl"></a><span data-ttu-id="057e4-142">FreshestCRL</span><span class="sxs-lookup"><span data-stu-id="057e4-142">FreshestCRL</span></span>

<span data-ttu-id="057e4-143">最新版的 CRL 延伸模組包含 delta CRL 的 URI。</span><span class="sxs-lookup"><span data-stu-id="057e4-143">The freshest CRL extension contains the URI of the delta CRL.</span></span> <span data-ttu-id="057e4-144">此擴充功能和 **CrlDistributionPoints** 延伸模組使用相同的 asn.1 語法。</span><span class="sxs-lookup"><span data-stu-id="057e4-144">The same ASN.1 syntax is used for this extension and the **CrlDistributionPoints** extension.</span></span>

<span data-ttu-id="057e4-145">**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="057e4-145">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="057e4-146">**OID：** XCN \_ OID \_ 最 \_ (2.5.29.46) 的 CRL</span><span class="sxs-lookup"><span data-stu-id="057e4-146">**OID:** XCN\_OID\_FRESHEST\_CRL (2.5.29.46)</span></span>

## <a name="keyusage"></a><span data-ttu-id="057e4-147">KeyUsage</span><span class="sxs-lookup"><span data-stu-id="057e4-147">KeyUsage</span></span>

<span data-ttu-id="057e4-148">金鑰使用方法延伸可以用來定義憑證中包含的公開金鑰所能執行的作業限制。</span><span class="sxs-lookup"><span data-stu-id="057e4-148">The key usage extension can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.</span></span> <span data-ttu-id="057e4-149">例如，您可以指定只使用公開金鑰來建立數位簽章、簽署憑證撤銷清單 (CRL) ，或將另一個金鑰加密。</span><span class="sxs-lookup"><span data-stu-id="057e4-149">For example, you can specify that the public key be used only to create a digital signature, sign a certificate revocation list (CRL), or encrypt another key.</span></span>

<span data-ttu-id="057e4-150">**介面：** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span><span class="sxs-lookup"><span data-stu-id="057e4-150">**Interface:** [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span></span>

<span data-ttu-id="057e4-151">**OID：** XCN \_ OID \_ 金鑰 \_ 使用方法 (2.5.29.15) </span><span class="sxs-lookup"><span data-stu-id="057e4-151">**OID:** XCN\_OID\_KEY\_USAGE (2.5.29.15)</span></span>

## <a name="msapplicationpolicies"></a><span data-ttu-id="057e4-152">MSApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="057e4-152">MSApplicationPolicies</span></span>

<span data-ttu-id="057e4-153">應用程式可以使用 Microsoft 應用程式原則擴充功能來根據允許的使用方式來篩選憑證。</span><span class="sxs-lookup"><span data-stu-id="057e4-153">The Microsoft application policies extension can be used by an application to filter certificates on the basis of permitted use.</span></span> <span data-ttu-id="057e4-154">允許的用法是由 Oid 識別。</span><span class="sxs-lookup"><span data-stu-id="057e4-154">Permitted uses are identified by OIDs.</span></span> <span data-ttu-id="057e4-155">此延伸模組類似于 **EnhancedKeyUsage** 延伸模組，但會將更嚴格的語義套用至父 CA。</span><span class="sxs-lookup"><span data-stu-id="057e4-155">This extension is similar to the **EnhancedKeyUsage** extension but with stricter semantics applied to the parent CA.</span></span> <span data-ttu-id="057e4-156">此延伸模組是 Microsoft 專有的。</span><span class="sxs-lookup"><span data-stu-id="057e4-156">The extension is Microsoft specific.</span></span>

<span data-ttu-id="057e4-157">**介面：** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span><span class="sxs-lookup"><span data-stu-id="057e4-157">**Interface:** [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span></span>

<span data-ttu-id="057e4-158">**OID：** XCN \_ OID \_ 應用程式憑證 \_ \_ 原則 (1.3.6.1.4.1.311.21.10) </span><span class="sxs-lookup"><span data-stu-id="057e4-158">**OID:** XCN\_OID\_APPLICATION\_CERT\_POLICIES (1.3.6.1.4.1.311.21.10)</span></span>

## <a name="nameconstraints"></a><span data-ttu-id="057e4-159">NameConstraints</span><span class="sxs-lookup"><span data-stu-id="057e4-159">NameConstraints</span></span>

<span data-ttu-id="057e4-160">名稱限制延伸是用來識別憑證階層中憑證的所有主體名稱必須位於其中的命名空間。</span><span class="sxs-lookup"><span data-stu-id="057e4-160">The name constraints extension is used to identify the namespace within which all subject names of certificates in a certificate hierarchy must be located.</span></span> <span data-ttu-id="057e4-161">這個延伸只能用於一個 CA 憑證中。</span><span class="sxs-lookup"><span data-stu-id="057e4-161">The extension is used only in a CA certificate.</span></span>

<span data-ttu-id="057e4-162">**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="057e4-162">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="057e4-163">**OID：** XCN \_ OID \_ 名稱 \_ 條件約束 (2.5.29.30) </span><span class="sxs-lookup"><span data-stu-id="057e4-163">**OID:** XCN\_OID\_NAME\_CONSTRAINTS (2.5.29.30)</span></span>

## <a name="policyconstraints"></a><span data-ttu-id="057e4-164">PolicyConstraints</span><span class="sxs-lookup"><span data-stu-id="057e4-164">PolicyConstraints</span></span>

<span data-ttu-id="057e4-165">原則限制延伸會新增至 CA 憑證，藉由禁止原則對應或要求階層中的每個憑證都包含可接受的原則識別碼來限制路徑驗證。</span><span class="sxs-lookup"><span data-stu-id="057e4-165">The policy constraints extension is added to CA certificates to constrain path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span>

<span data-ttu-id="057e4-166">**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="057e4-166">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="057e4-167">**OID：** XCN \_ OID \_ 原則 \_ 條件約束 (2.5.29.36) </span><span class="sxs-lookup"><span data-stu-id="057e4-167">**OID:** XCN\_OID\_POLICY\_CONSTRAINTS (2.5.29.36)</span></span>

## <a name="policymappings"></a><span data-ttu-id="057e4-168">PolicyMappings</span><span class="sxs-lookup"><span data-stu-id="057e4-168">PolicyMappings</span></span>

<span data-ttu-id="057e4-169">原則對應延伸模組是用來識別對應至發行 CA 中原則的次級 CA 中的原則。</span><span class="sxs-lookup"><span data-stu-id="057e4-169">The policy mappings extension is used to identify the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span> <span data-ttu-id="057e4-170">擴充值包含一連串的發行 CA，以及由物件識別碼表示的次級 CA 原則對應。</span><span class="sxs-lookup"><span data-stu-id="057e4-170">The extension value contains a sequence of issuing CA and subordinate CA policy mappings represented by object identifiers.</span></span>

<span data-ttu-id="057e4-171">**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="057e4-171">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="057e4-172">**OID：** XCN \_ OID \_ 原則對應 \_ (2.5.29.33) </span><span class="sxs-lookup"><span data-stu-id="057e4-172">**OID:** XCN\_OID\_POLICY\_MAPPINGS (2.5.29.33)</span></span>

## <a name="privatekeyusageperiod"></a><span data-ttu-id="057e4-173">PrivateKeyUsagePeriod</span><span class="sxs-lookup"><span data-stu-id="057e4-173">PrivateKeyUsagePeriod</span></span>

<span data-ttu-id="057e4-174">私密金鑰使用期限延伸是用來指定私密金鑰的不同有效期間，而非與金鑰相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="057e4-174">The private key usage period extension is used to specify a different validity period for the private key than for the certificate with which the key is associated.</span></span>

<span data-ttu-id="057e4-175">**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="057e4-175">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="057e4-176">**OID：** XCN \_ OID \_ PRI加值稅EKEY \_ 使用 \_ 期間 (2.5.29.16) </span><span class="sxs-lookup"><span data-stu-id="057e4-176">**OID:** XCN\_OID\_PRIVATEKEY\_USAGE\_PERIOD (2.5.29.16)</span></span>

## <a name="smimecapabilities"></a><span data-ttu-id="057e4-177">SmimeCapabilities</span><span class="sxs-lookup"><span data-stu-id="057e4-177">SmimeCapabilities</span></span>

<span data-ttu-id="057e4-178">安全/多用途網際網路郵件延伸 (S/MIME) 功能延伸模組可用來將電子郵件收件者的解密功能回報給電子郵件訊息的寄件者，讓傳送者可以選擇雙方所支援的最安全加密演算法。</span><span class="sxs-lookup"><span data-stu-id="057e4-178">The Secure/Multipurpose Internet Mail Extensions (S/MIME) capabilities extension can be used to report an email recipient's decryption capabilities to the sender of the email message so that the sender can choose the most secure encryption algorithm supported by both parties.</span></span> <span data-ttu-id="057e4-179">擴充功能值包含對稱式加密演算法 Oid 的集合，以及每個 Oid 的選擇性加密強度。</span><span class="sxs-lookup"><span data-stu-id="057e4-179">The extension value contains a collection of symmetric encryption algorithm OIDs and an optional encryption strength for each.</span></span>

<span data-ttu-id="057e4-180">**介面：** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span><span class="sxs-lookup"><span data-stu-id="057e4-180">**Interface:** [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span></span>

<span data-ttu-id="057e4-181">**OID：** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15) </span><span class="sxs-lookup"><span data-stu-id="057e4-181">**OID:** XCN\_OID\_RSA\_SMIMECapabilities (1.2.840.113549.1.9.15)</span></span>

## <a name="subjectdirectoryattributes"></a><span data-ttu-id="057e4-182">SubjectDirectoryAttributes</span><span class="sxs-lookup"><span data-stu-id="057e4-182">SubjectDirectoryAttributes</span></span>

<span data-ttu-id="057e4-183">主體目錄屬性延伸可以用來傳達識別碼屬性，例如憑證主體的國籍。</span><span class="sxs-lookup"><span data-stu-id="057e4-183">The subject directory attributes extension can be used to convey identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="057e4-184">延伸值是 OID 值配對的序列。</span><span class="sxs-lookup"><span data-stu-id="057e4-184">The extension value is a sequence of OID-value pairs.</span></span>

<span data-ttu-id="057e4-185">**介面：** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="057e4-185">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="057e4-186">**OID：** XCN \_ OID \_ SUBJECT \_ DIR \_ ATTRS (2.5.29.9) </span><span class="sxs-lookup"><span data-stu-id="057e4-186">**OID:** XCN\_OID\_SUBJECT\_DIR\_ATTRS (2.5.29.9)</span></span>

## <a name="subjectkeyidentifier"></a><span data-ttu-id="057e4-187">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="057e4-187">SubjectKeyIdentifier</span></span>

<span data-ttu-id="057e4-188">主體金鑰識別碼延伸可以用來區別憑證主體所持有的多個公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="057e4-188">The subject key identifier extension can be used to differentiate between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="057e4-189">延伸值通常是金鑰的 SHA-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="057e4-189">The extension value is typically a SHA-1 hash of the key.</span></span>

<span data-ttu-id="057e4-190">**介面：** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="057e4-190">**Interface:** [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span></span>

<span data-ttu-id="057e4-191">**OID：** XCN \_ OID \_ 主體 \_ 金鑰 \_ 識別碼 (2.5.29.14) </span><span class="sxs-lookup"><span data-stu-id="057e4-191">**OID:** XCN\_OID\_SUBJECT\_KEY\_IDENTIFIER (2.5.29.14)</span></span>

## <a name="template"></a><span data-ttu-id="057e4-192">範本</span><span class="sxs-lookup"><span data-stu-id="057e4-192">Template</span></span>

<span data-ttu-id="057e4-193">範本延伸模組可以用來識別發行或更新憑證時要使用的第2版範本。</span><span class="sxs-lookup"><span data-stu-id="057e4-193">The template extension can be used to identify the version 2 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="057e4-194">擴充值包含範本 OID 和選用的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="057e4-194">The extension value contains the template OID and optional version information.</span></span> <span data-ttu-id="057e4-195">此延伸模組是 Microsoft 專有的。</span><span class="sxs-lookup"><span data-stu-id="057e4-195">The extension is Microsoft specific.</span></span>

<span data-ttu-id="057e4-196">**介面：** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span><span class="sxs-lookup"><span data-stu-id="057e4-196">**Interface:** [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span></span>

<span data-ttu-id="057e4-197">**OID：** XCN \_ OID \_ 證書 \_ 範本 (1.3.6.1.4.1.311.21.7) </span><span class="sxs-lookup"><span data-stu-id="057e4-197">**OID:** XCN\_OID\_CERTIFICATE\_TEMPLATE (1.3.6.1.4.1.311.21.7)</span></span>

## <a name="templatename"></a><span data-ttu-id="057e4-198">TemplateName</span><span class="sxs-lookup"><span data-stu-id="057e4-198">TemplateName</span></span>

<span data-ttu-id="057e4-199">範本名稱延伸可以用來識別發行或更新憑證時要使用的第1版範本。</span><span class="sxs-lookup"><span data-stu-id="057e4-199">The template name extension can be used to identify the version 1 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="057e4-200">擴充值包含範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="057e4-200">The extension value contains the name of the template.</span></span> <span data-ttu-id="057e4-201">此延伸模組是 Microsoft 專有的。</span><span class="sxs-lookup"><span data-stu-id="057e4-201">The extension is Microsoft specific.</span></span>

<span data-ttu-id="057e4-202">**介面：** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span><span class="sxs-lookup"><span data-stu-id="057e4-202">**Interface:** [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span></span>

<span data-ttu-id="057e4-203">**OID：** XCN \_ OID \_ 註冊 \_ CERTTYPE \_ 延伸模組 (元1.3.6.1.4.1.311.20.2 參考) </span><span class="sxs-lookup"><span data-stu-id="057e4-203">**OID:** XCN\_OID\_ENROLL\_CERTTYPE\_EXTENSION (1.3.6.1.4.1.311.20.2)</span></span>

## <a name="related-topics"></a><span data-ttu-id="057e4-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="057e4-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="057e4-205">擴充功能</span><span class="sxs-lookup"><span data-stu-id="057e4-205">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



