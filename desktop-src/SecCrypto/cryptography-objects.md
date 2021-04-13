---
description: 列出 CryptoAPI 提供的物件。
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: 加密物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386147"
---
# <a name="cryptography-objects"></a><span data-ttu-id="e0533-103">加密物件</span><span class="sxs-lookup"><span data-stu-id="e0533-103">Cryptography Objects</span></span>

<span data-ttu-id="e0533-104">加密物件會根據使用方式進行分類，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e0533-104">Cryptography objects are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="e0533-105">憑證存放區物件</span><span class="sxs-lookup"><span data-stu-id="e0533-105">Certificate Store Objects</span></span>](#certificate-store-objects)
-   [<span data-ttu-id="e0533-106">數位簽章物件</span><span class="sxs-lookup"><span data-stu-id="e0533-106">Digital Signature Objects</span></span>](#digital-signature-objects)
-   [<span data-ttu-id="e0533-107">封裝的資料物件</span><span class="sxs-lookup"><span data-stu-id="e0533-107">Enveloped Data Objects</span></span>](#enveloped-data-objects)
-   [<span data-ttu-id="e0533-108">資料加密物件</span><span class="sxs-lookup"><span data-stu-id="e0533-108">Data Encryption Objects</span></span>](#data-encryption-objects)
-   [<span data-ttu-id="e0533-109">輔助物件</span><span class="sxs-lookup"><span data-stu-id="e0533-109">Auxiliary Objects</span></span>](#auxiliary-objects)
-   [<span data-ttu-id="e0533-110">憑證註冊物件</span><span class="sxs-lookup"><span data-stu-id="e0533-110">Certificate Enrollment Objects</span></span>](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a><span data-ttu-id="e0533-111">憑證存放區物件</span><span class="sxs-lookup"><span data-stu-id="e0533-111">Certificate Store Objects</span></span>

<span data-ttu-id="e0533-112">下列物件適用于 [*憑證存放區*](../secgloss/c-gly.md) 和這些存放區中的憑證。</span><span class="sxs-lookup"><span data-stu-id="e0533-112">The following objects work with [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="e0533-113">CAPICOM 支援使用目前的使用者、本機電腦、記憶體和 Active Directory 憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="e0533-113">CAPICOM supports the use of Current User, Local Machine, memory, and Active Directory certificate stores.</span></span>



| <span data-ttu-id="e0533-114">Object</span><span class="sxs-lookup"><span data-stu-id="e0533-114">Object</span></span>                                             | <span data-ttu-id="e0533-115">描述</span><span class="sxs-lookup"><span data-stu-id="e0533-115">Description</span></span>                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0533-116">**憑證**</span><span class="sxs-lookup"><span data-stu-id="e0533-116">**Certificate**</span></span>](certificate.md)                 | <span data-ttu-id="e0533-117">單一數位憑證。</span><span class="sxs-lookup"><span data-stu-id="e0533-117">A single digital certificate.</span></span>                                                                                           |
| [<span data-ttu-id="e0533-118">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="e0533-118">**CertificatePolicies**</span></span>](certificatepolicies.md) | <span data-ttu-id="e0533-119">[**PolicyInformation**](policyinformation.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-119">A collection of [**PolicyInformation**](policyinformation.md) objects.</span></span>                                                 |
| [<span data-ttu-id="e0533-120">**憑證**</span><span class="sxs-lookup"><span data-stu-id="e0533-120">**Certificates**</span></span>](certificates.md)               | <span data-ttu-id="e0533-121">[**憑證**](certificate.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-121">Collection of [**Certificate**](certificate.md) objects.</span></span>                                                               |
| [<span data-ttu-id="e0533-122">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="e0533-122">**CertificateStatus**</span></span>](certificatestatus.md)     | <span data-ttu-id="e0533-123">提供憑證的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="e0533-123">Provides status information on a certificate.</span></span>                                                                           |
| [<span data-ttu-id="e0533-124">**鏈**</span><span class="sxs-lookup"><span data-stu-id="e0533-124">**Chain**</span></span>](chain.md)                             | <span data-ttu-id="e0533-125">根據數位憑證建立和檢查憑證驗證鏈。</span><span class="sxs-lookup"><span data-stu-id="e0533-125">Creates and checks a certificate validation chain based on a digital certificate.</span></span>                                       |
| [<span data-ttu-id="e0533-126">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="e0533-126">**ExtendedProperties**</span></span>](extendedproperties.md)   | <span data-ttu-id="e0533-127">代表 [**ExtendedProperty**](extendedproperty.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-127">Represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span>                                        |
| [<span data-ttu-id="e0533-128">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="e0533-128">**ExtendedProperty**</span></span>](extendedproperties.md)     | <span data-ttu-id="e0533-129">表示 Microsoft 擴充的屬性。</span><span class="sxs-lookup"><span data-stu-id="e0533-129">Represents a Microsoft-extended property.</span></span>                                                                               |
| [<span data-ttu-id="e0533-130">**延伸模組**</span><span class="sxs-lookup"><span data-stu-id="e0533-130">**Extension**</span></span>](extension.md)                     | <span data-ttu-id="e0533-131">代表單一憑證延伸。</span><span class="sxs-lookup"><span data-stu-id="e0533-131">Represents a single certificate extension.</span></span>                                                                              |
| [<span data-ttu-id="e0533-132">**延伸模組**</span><span class="sxs-lookup"><span data-stu-id="e0533-132">**Extensions**</span></span>](extensions.md)                   | <span data-ttu-id="e0533-133">表示 [**擴充**](extension.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-133">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                      |
| [<span data-ttu-id="e0533-134">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="e0533-134">**PrivateKey**</span></span>](privatekey.md)                   | <span data-ttu-id="e0533-135">代表私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="e0533-135">Represents a private key.</span></span>                                                                                               |
| [<span data-ttu-id="e0533-136">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="e0533-136">**PublicKey**</span></span>](publickey.md)                     | <span data-ttu-id="e0533-137">代表 [**憑證**](certificate.md) 物件中的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="e0533-137">Represents a public key in a [**Certificate**](certificate.md) object.</span></span>                                                 |
| [<span data-ttu-id="e0533-138">**市集**</span><span class="sxs-lookup"><span data-stu-id="e0533-138">**Store**</span></span>](store.md)                             | <span data-ttu-id="e0533-139">提供屬性和方法，以選擇、管理及使用憑證存放區和這些存放區中的憑證。</span><span class="sxs-lookup"><span data-stu-id="e0533-139">Provides the properties and methods to choose, manage, and use certificate stores and the certificates in those stores.</span></span> |
| [<span data-ttu-id="e0533-140">**範本**</span><span class="sxs-lookup"><span data-stu-id="e0533-140">**Template**</span></span>](template.md)                       | <span data-ttu-id="e0533-141">代表憑證的憑證延伸範本。</span><span class="sxs-lookup"><span data-stu-id="e0533-141">Represents the certificate extension template of the certificate.</span></span>                                                       |



 

## <a name="digital-signature-objects"></a><span data-ttu-id="e0533-142">數位簽章物件</span><span class="sxs-lookup"><span data-stu-id="e0533-142">Digital Signature Objects</span></span>

<span data-ttu-id="e0533-143">系統會匯出下列物件以數位方式簽署資料，並驗證數位簽章。</span><span class="sxs-lookup"><span data-stu-id="e0533-143">The following objects are exported to digitally sign data and to verify digital signatures.</span></span>



| <span data-ttu-id="e0533-144">Object</span><span class="sxs-lookup"><span data-stu-id="e0533-144">Object</span></span>                           | <span data-ttu-id="e0533-145">描述</span><span class="sxs-lookup"><span data-stu-id="e0533-145">Description</span></span>                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0533-146">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="e0533-146">**SignedCode**</span></span>](signedcode.md) | <span data-ttu-id="e0533-147">物件，用來以 Authenticode 數位簽章簽署程式碼，以及驗證簽署程式碼的簽章。</span><span class="sxs-lookup"><span data-stu-id="e0533-147">Object used to sign code with an Authenticode digital signature and to verify the signature on signed code.</span></span> |
| [<span data-ttu-id="e0533-148">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="e0533-148">**SignedData**</span></span>](signeddata.md) | <span data-ttu-id="e0533-149">用來簽署資料和驗證簽署資料簽章的物件。</span><span class="sxs-lookup"><span data-stu-id="e0533-149">Object used to sign data and to verify the signature on signed data.</span></span>                                        |
| [<span data-ttu-id="e0533-150">**簽署者**</span><span class="sxs-lookup"><span data-stu-id="e0533-150">**Signer**</span></span>](signer.md)         | <span data-ttu-id="e0533-151">單一資料簽署者的資訊，包括簽署者的憑證。</span><span class="sxs-lookup"><span data-stu-id="e0533-151">Information on a single data signer, including the signer's certificate.</span></span>                                    |
| [<span data-ttu-id="e0533-152">**簽名**</span><span class="sxs-lookup"><span data-stu-id="e0533-152">**Signers**</span></span>](signers.md)       | <span data-ttu-id="e0533-153">[**簽署者**](signer.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-153">Collection of [**Signer**](signer.md) objects.</span></span>                                                             |



 

## <a name="enveloped-data-objects"></a><span data-ttu-id="e0533-154">封裝的資料物件</span><span class="sxs-lookup"><span data-stu-id="e0533-154">Enveloped Data Objects</span></span>

<span data-ttu-id="e0533-155">系統會匯出下列物件，以建立用於隱私權的封包資料訊息，以及解密封包訊息中的資料。</span><span class="sxs-lookup"><span data-stu-id="e0533-155">The following objects are exported to create enveloped data messages for privacy and to decrypt data in enveloped messages.</span></span>



| <span data-ttu-id="e0533-156">Object</span><span class="sxs-lookup"><span data-stu-id="e0533-156">Object</span></span>                                 | <span data-ttu-id="e0533-157">描述</span><span class="sxs-lookup"><span data-stu-id="e0533-157">Description</span></span>                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0533-158">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="e0533-158">**EnvelopedData**</span></span>](envelopeddata.md) | <span data-ttu-id="e0533-159">用來建立、傳送和接收封包資料的物件。</span><span class="sxs-lookup"><span data-stu-id="e0533-159">Objects used to create, send, and receive enveloped data.</span></span> <span data-ttu-id="e0533-160">封包資料會經過加密，因此只有預期的收件者可以將它解密。</span><span class="sxs-lookup"><span data-stu-id="e0533-160">Enveloped data is encrypted so that only the intended recipients can decrypt it.</span></span> |
| [<span data-ttu-id="e0533-161">**收件者**</span><span class="sxs-lookup"><span data-stu-id="e0533-161">**Recipients**</span></span>](recipients.md)       | <span data-ttu-id="e0533-162">封裝訊息的預定收件者之 [**憑證**](certificate.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-162">Collection of the [**Certificate**](certificate.md) objects of the intended recipients of an enveloped message.</span></span>                           |



 

## <a name="data-encryption-objects"></a><span data-ttu-id="e0533-163">資料加密物件</span><span class="sxs-lookup"><span data-stu-id="e0533-163">Data Encryption Objects</span></span>

<span data-ttu-id="e0533-164">下列物件會被匯出，以加密隱私權的任意資料，並將加密的資料解密。</span><span class="sxs-lookup"><span data-stu-id="e0533-164">The following object is exported to encrypt arbitrary data for privacy and to decrypt encrypted data.</span></span>



| <span data-ttu-id="e0533-165">Object</span><span class="sxs-lookup"><span data-stu-id="e0533-165">Object</span></span>                                 | <span data-ttu-id="e0533-166">描述</span><span class="sxs-lookup"><span data-stu-id="e0533-166">Description</span></span>                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0533-167">**A**</span><span class="sxs-lookup"><span data-stu-id="e0533-167">**EncryptedData**</span></span>](encrypteddata.md) | <span data-ttu-id="e0533-168">用來加密資料的物件。</span><span class="sxs-lookup"><span data-stu-id="e0533-168">Objects used to encrypt data.</span></span> <span data-ttu-id="e0533-169">[**A**](encrypteddata.md)物件中的加密資料可以進行解密。</span><span class="sxs-lookup"><span data-stu-id="e0533-169">Encrypted data in an [**EncryptedData**](encrypteddata.md) object can be decrypted.</span></span> |



 

## <a name="auxiliary-objects"></a><span data-ttu-id="e0533-170">輔助物件</span><span class="sxs-lookup"><span data-stu-id="e0533-170">Auxiliary Objects</span></span>

<span data-ttu-id="e0533-171">系統會匯出下列物件，以變更其他物件的預設行為，以及管理憑證、憑證存放區和訊息。</span><span class="sxs-lookup"><span data-stu-id="e0533-171">The following objects are exported to change default behaviors of other objects and to manage certificates, certificate stores, and messages.</span></span>



| <span data-ttu-id="e0533-172">Object</span><span class="sxs-lookup"><span data-stu-id="e0533-172">Object</span></span>                                         | <span data-ttu-id="e0533-173">描述</span><span class="sxs-lookup"><span data-stu-id="e0533-173">Description</span></span>                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0533-174">**演算法**</span><span class="sxs-lookup"><span data-stu-id="e0533-174">**Algorithm**</span></span>](algorithm.md)                 | <span data-ttu-id="e0533-175">設定密碼編譯作業中所使用的演算法和 [*金鑰長度*](../secgloss/k-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="e0533-175">Sets the algorithm and [*key length*](../secgloss/k-gly.md) to be used in cryptographic operations.</span></span> |
| [<span data-ttu-id="e0533-176">**屬性**</span><span class="sxs-lookup"><span data-stu-id="e0533-176">**Attribute**</span></span>](attribute.md)                 | <span data-ttu-id="e0533-177">提供與簽章相關的一段新增資訊，例如簽署的時間。</span><span class="sxs-lookup"><span data-stu-id="e0533-177">Provides a single piece of added information about a signature, such as the time of signing.</span></span>                                                    |
| [<span data-ttu-id="e0533-178">**屬性**</span><span class="sxs-lookup"><span data-stu-id="e0533-178">**Attributes**</span></span>](attributes.md)               | <span data-ttu-id="e0533-179">[**屬性**](attribute.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-179">Collection of [**Attribute**](attribute.md) objects.</span></span>                                                                                           |
| [<span data-ttu-id="e0533-180">**BasicConstraints**</span><span class="sxs-lookup"><span data-stu-id="e0533-180">**BasicConstraints**</span></span>](basicconstraints.md)   | <span data-ttu-id="e0533-181">提供對憑證使用基本條件約束的唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="e0533-181">Provides read-only access to basic constraints on the uses of a certificate.</span></span>                                                                    |
| [<span data-ttu-id="e0533-182">**EKU**</span><span class="sxs-lookup"><span data-stu-id="e0533-182">**EKU**</span></span>](eku.md)                             | <span data-ttu-id="e0533-183">提供憑證之 EKU 屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="e0533-183">Provides access to EKU properties of certificates.</span></span>                                                                                              |
| [<span data-ttu-id="e0533-184">**Eku**</span><span class="sxs-lookup"><span data-stu-id="e0533-184">**EKUs**</span></span>](ekus.md)                           | <span data-ttu-id="e0533-185">[**EKU**](eku.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-185">Collection of [**EKU**](eku.md) objects.</span></span>                                                                                                       |
| [<span data-ttu-id="e0533-186">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="e0533-186">**EncodedData**</span></span>](encodeddata.md)             | <span data-ttu-id="e0533-187">代表編碼資料的區塊。</span><span class="sxs-lookup"><span data-stu-id="e0533-187">Represents a block of encoded data.</span></span>                                                                                                             |
| [<span data-ttu-id="e0533-188">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="e0533-188">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)   | <span data-ttu-id="e0533-189">提供對憑證擴充金鑰使用方式屬性的唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="e0533-189">Provides read-only access to the extended key usage properties of certificates.</span></span>                                                                 |
| [<span data-ttu-id="e0533-190">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="e0533-190">**HashedData**</span></span>](hasheddata.md)               | <span data-ttu-id="e0533-191">提供將雜湊演算法套用至字串的功能。</span><span class="sxs-lookup"><span data-stu-id="e0533-191">Provides functionality for applying a hash algorithm to a string.</span></span>                                                                               |
| [<span data-ttu-id="e0533-192">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="e0533-192">**KeyUsage**</span></span>](keyusage.md)                   | <span data-ttu-id="e0533-193">提供憑證的金鑰使用方式屬性的唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="e0533-193">Provides read-only access to key usage properties of certificates.</span></span>                                                                              |
| [<span data-ttu-id="e0533-194">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="e0533-194">**NoticeNumbers**</span></span>](noticenumbers.md)         | <span data-ttu-id="e0533-195">表示 [**擴充**](extension.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-195">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                                              |
| [<span data-ttu-id="e0533-196">**老**</span><span class="sxs-lookup"><span data-stu-id="e0533-196">**OID**</span></span>](oid.md)                             | <span data-ttu-id="e0533-197">代表數個 CAPICOM 屬性所使用的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0533-197">Represents an object identifier that is used by several CAPICOM properties.</span></span>                                                                     |
| [<span data-ttu-id="e0533-198">**Oid**</span><span class="sxs-lookup"><span data-stu-id="e0533-198">**OIDs**</span></span>](oids.md)                           | <span data-ttu-id="e0533-199">表示 [**OID**](oid.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-199">Represents a collection of [**OID**](oid.md) objects.</span></span>                                                                                          |
| [<span data-ttu-id="e0533-200">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="e0533-200">**PolicyInformation**</span></span>](policyinformation.md) | <span data-ttu-id="e0533-201">提供對延伸模組之原則 Oid 的存取。</span><span class="sxs-lookup"><span data-stu-id="e0533-201">Provides access to the policy OIDs of an extension.</span></span>                                                                                             |
| [<span data-ttu-id="e0533-202">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="e0533-202">**Qualifier**</span></span>](qualifier.md)                 | <span data-ttu-id="e0533-203">代表 (CPS) 指標或使用者注意事項辨識符號的認證實務聲明。</span><span class="sxs-lookup"><span data-stu-id="e0533-203">Represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>                                                           |
| [<span data-ttu-id="e0533-204">**限定詞**</span><span class="sxs-lookup"><span data-stu-id="e0533-204">**Qualifiers**</span></span>](qualifiers.md)               | <span data-ttu-id="e0533-205">表示限定詞的集合。</span><span class="sxs-lookup"><span data-stu-id="e0533-205">Represents a collection of qualifiers.</span></span>                                                                                                          |
| [<span data-ttu-id="e0533-206">**設定**</span><span class="sxs-lookup"><span data-stu-id="e0533-206">**Settings**</span></span>](settings.md)                   | <span data-ttu-id="e0533-207">啟用或停用對話方塊，以在未指定身分識別的情況下提示輸入簽署者或寄件者身分識別。</span><span class="sxs-lookup"><span data-stu-id="e0533-207">Enables or disables dialog boxes to prompt for signer or sender identity if that identity is not specified.</span></span>                                     |
| [<span data-ttu-id="e0533-208">**公用程式**</span><span class="sxs-lookup"><span data-stu-id="e0533-208">**Utilities**</span></span>](utilities.md)                 | <span data-ttu-id="e0533-209">提供一般工作的功能。</span><span class="sxs-lookup"><span data-stu-id="e0533-209">Provides functionality for common tasks.</span></span>                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a><span data-ttu-id="e0533-210">憑證註冊物件</span><span class="sxs-lookup"><span data-stu-id="e0533-210">Certificate Enrollment Objects</span></span>

<span data-ttu-id="e0533-211">下列物件用於憑證註冊。</span><span class="sxs-lookup"><span data-stu-id="e0533-211">The following object is used for certificate enrollment.</span></span>



| <span data-ttu-id="e0533-212">Object</span><span class="sxs-lookup"><span data-stu-id="e0533-212">Object</span></span>                     | <span data-ttu-id="e0533-213">描述</span><span class="sxs-lookup"><span data-stu-id="e0533-213">Description</span></span>                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0533-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e0533-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span></span> | <span data-ttu-id="e0533-215">代表憑證註冊控制項的物件。</span><span class="sxs-lookup"><span data-stu-id="e0533-215">Object that represents the Certificate Enrollment Control.</span></span> <span data-ttu-id="e0533-216">這主要用於 Visual Basic 或其他自動化語言的程式設計時。</span><span class="sxs-lookup"><span data-stu-id="e0533-216">It is primarily used when programming in Visual Basic or another Automation language.</span></span> |



 

 

 
