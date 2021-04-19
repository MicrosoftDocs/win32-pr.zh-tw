---
description: 提供的服務可讓應用程式開發人員根據密碼編譯將安全性新增至應用程式。
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: CAPICOM 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b828f3b5b35e3e0ef799529f866c23416c8df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000334"
---
# <a name="capicom-reference"></a><span data-ttu-id="395d5-103">CAPICOM 參考</span><span class="sxs-lookup"><span data-stu-id="395d5-103">CAPICOM Reference</span></span>

<span data-ttu-id="395d5-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="395d5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista and Windows XP.</span></span> <span data-ttu-id="395d5-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="395d5-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="395d5-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="395d5-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="395d5-107">CAPICOM COM 用戶端提供的服務可讓應用程式開發人員根據 [*密碼*](../secgloss/c-gly.md) 編譯將安全性新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="395d5-107">The CAPICOM COM client provides services that enable application developers to add security based on [*cryptography*](../secgloss/c-gly.md) to applications.</span></span> <span data-ttu-id="395d5-108">CryptoAPI 包含使用 [*數位簽章*](../secgloss/d-gly.md)進行驗證、封套訊息以及加密和解密資料的功能。</span><span class="sxs-lookup"><span data-stu-id="395d5-108">CryptoAPI includes functionality for authentication using [*digital signatures*](../secgloss/d-gly.md), for enveloping messages, and for encrypting and decrypting data.</span></span>



| <span data-ttu-id="395d5-109">類別</span><span class="sxs-lookup"><span data-stu-id="395d5-109">Category</span></span>                    | <span data-ttu-id="395d5-110">描述</span><span class="sxs-lookup"><span data-stu-id="395d5-110">Description</span></span>                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="395d5-111">憑證存放區物件</span><span class="sxs-lookup"><span data-stu-id="395d5-111">Certificate Store Objects</span></span>   | <span data-ttu-id="395d5-112">可用來在這些存放區中使用憑證存放區和憑證的物件。</span><span class="sxs-lookup"><span data-stu-id="395d5-112">Objects available for using certificate stores and the certificates in those stores.</span></span>                                       |
| <span data-ttu-id="395d5-113">數位簽章物件</span><span class="sxs-lookup"><span data-stu-id="395d5-113">Digital Signature Objects</span></span>   | <span data-ttu-id="395d5-114">用來數位簽署資料和驗證數位簽章的物件。</span><span class="sxs-lookup"><span data-stu-id="395d5-114">Objects used to digitally sign data and to verify digital signatures.</span></span>                                                      |
| <span data-ttu-id="395d5-115">封裝的資料物件</span><span class="sxs-lookup"><span data-stu-id="395d5-115">Enveloped Data Objects</span></span>      | <span data-ttu-id="395d5-116">物件，可用來建立用於隱私權的封包資料訊息，以及解密封包訊息中的資料。</span><span class="sxs-lookup"><span data-stu-id="395d5-116">Objects used to create enveloped data messages for privacy and to decrypt data in enveloped messages.</span></span>                      |
| <span data-ttu-id="395d5-117">資料加密物件</span><span class="sxs-lookup"><span data-stu-id="395d5-117">Data Encryption Objects</span></span>     | <span data-ttu-id="395d5-118">用來加密資料和解密加密資料的物件。</span><span class="sxs-lookup"><span data-stu-id="395d5-118">Objects used to encrypt data and to decrypt encrypted data.</span></span>                                                                |
| <span data-ttu-id="395d5-119">輔助物件</span><span class="sxs-lookup"><span data-stu-id="395d5-119">Auxiliary Objects</span></span>           | <span data-ttu-id="395d5-120">用來變更預設行為，以及管理憑證、憑證存放區和使用者介面 (UI) 訊息的物件。</span><span class="sxs-lookup"><span data-stu-id="395d5-120">Objects used to change default behaviors and to manage certificates, certificate stores, and user interface (UI) messages.</span></span> |
| <span data-ttu-id="395d5-121">互通性介面</span><span class="sxs-lookup"><span data-stu-id="395d5-121">Interoperability Interfaces</span></span> | <span data-ttu-id="395d5-122">允許衍生 CryptoAPI 以與 CAPICOM 2.0 一起運作的介面。</span><span class="sxs-lookup"><span data-stu-id="395d5-122">Interfaces that allow derivations of CryptoAPI to work together with CAPICOM 2.0.</span></span>                                          |
| <span data-ttu-id="395d5-123">列舉類型</span><span class="sxs-lookup"><span data-stu-id="395d5-123">Enumeration Types</span></span>           | <span data-ttu-id="395d5-124">用於 CAPICOM 的列舉類型。</span><span class="sxs-lookup"><span data-stu-id="395d5-124">Enumeration types used with CAPICOM.</span></span>                                                                                       |



 

## <a name="certificate-store-objects"></a><span data-ttu-id="395d5-125">憑證存放區物件</span><span class="sxs-lookup"><span data-stu-id="395d5-125">Certificate Store Objects</span></span>

<span data-ttu-id="395d5-126">下列物件適用于 [*憑證存放區*](../secgloss/c-gly.md) 和這些存放區中的憑證。</span><span class="sxs-lookup"><span data-stu-id="395d5-126">The following objects work with [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="395d5-127">CAPICOM 支援使用目前的使用者、本機電腦、記憶體和 Active Directory 憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="395d5-127">CAPICOM supports the use of Current User, Local Machine, Memory, and Active Directory certificate stores.</span></span>



| <span data-ttu-id="395d5-128">Object</span><span class="sxs-lookup"><span data-stu-id="395d5-128">Object</span></span>                                             | <span data-ttu-id="395d5-129">描述</span><span class="sxs-lookup"><span data-stu-id="395d5-129">Description</span></span>                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="395d5-130">**憑證**</span><span class="sxs-lookup"><span data-stu-id="395d5-130">**Certificate**</span></span>](certificate.md)                 | <span data-ttu-id="395d5-131">單一數位憑證。</span><span class="sxs-lookup"><span data-stu-id="395d5-131">A single digital certificate.</span></span>                                                                                           |
| [<span data-ttu-id="395d5-132">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="395d5-132">**CertificatePolicies**</span></span>](certificatepolicies.md) | <span data-ttu-id="395d5-133">[**PolicyInformation**](policyinformation.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-133">A collection of [**PolicyInformation**](policyinformation.md) objects.</span></span>                                                 |
| [<span data-ttu-id="395d5-134">**憑證**</span><span class="sxs-lookup"><span data-stu-id="395d5-134">**Certificates**</span></span>](certificates.md)               | <span data-ttu-id="395d5-135">[**憑證**](certificate.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-135">Collection of [**Certificate**](certificate.md) objects.</span></span>                                                               |
| [<span data-ttu-id="395d5-136">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="395d5-136">**CertificateStatus**</span></span>](certificatestatus.md)     | <span data-ttu-id="395d5-137">提供憑證的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="395d5-137">Provides status information on a certificate.</span></span>                                                                           |
| [<span data-ttu-id="395d5-138">**鏈**</span><span class="sxs-lookup"><span data-stu-id="395d5-138">**Chain**</span></span>](chain.md)                             | <span data-ttu-id="395d5-139">根據數位憑證建立和檢查憑證驗證鏈。</span><span class="sxs-lookup"><span data-stu-id="395d5-139">Creates and checks a certificate validation chain based on a digital certificate.</span></span>                                       |
| [<span data-ttu-id="395d5-140">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="395d5-140">**ExtendedProperties**</span></span>](extendedproperties.md)   | <span data-ttu-id="395d5-141">代表 [**ExtendedProperty**](extendedproperty.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-141">Represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span>                                        |
| [<span data-ttu-id="395d5-142">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="395d5-142">**ExtendedProperty**</span></span>](extendedproperty.md)       | <span data-ttu-id="395d5-143">表示 Microsoft 擴充的屬性。</span><span class="sxs-lookup"><span data-stu-id="395d5-143">Represents a Microsoft-extended property.</span></span>                                                                               |
| [<span data-ttu-id="395d5-144">**延伸模組**</span><span class="sxs-lookup"><span data-stu-id="395d5-144">**Extension**</span></span>](extension.md)                     | <span data-ttu-id="395d5-145">代表單一憑證延伸。</span><span class="sxs-lookup"><span data-stu-id="395d5-145">Represents a single certificate extension.</span></span>                                                                              |
| [<span data-ttu-id="395d5-146">**延伸模組**</span><span class="sxs-lookup"><span data-stu-id="395d5-146">**Extensions**</span></span>](extensions.md)                   | <span data-ttu-id="395d5-147">表示 [**擴充**](extension.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-147">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                      |
| [<span data-ttu-id="395d5-148">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="395d5-148">**PrivateKey**</span></span>](privatekey.md)                   | <span data-ttu-id="395d5-149">代表私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="395d5-149">Represents a private key.</span></span>                                                                                               |
| [<span data-ttu-id="395d5-150">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="395d5-150">**PublicKey**</span></span>](publickey.md)                     | <span data-ttu-id="395d5-151">代表 [**憑證**](certificate.md) 物件中的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="395d5-151">Represents a public key in a [**Certificate**](certificate.md) object.</span></span>                                                 |
| [<span data-ttu-id="395d5-152">**市集**</span><span class="sxs-lookup"><span data-stu-id="395d5-152">**Store**</span></span>](store.md)                             | <span data-ttu-id="395d5-153">提供屬性和方法，以選擇、管理及使用憑證存放區和這些存放區中的憑證。</span><span class="sxs-lookup"><span data-stu-id="395d5-153">Provides the properties and methods to choose, manage, and use certificate stores and the certificates in those stores.</span></span> |
| [<span data-ttu-id="395d5-154">**範本**</span><span class="sxs-lookup"><span data-stu-id="395d5-154">**Template**</span></span>](template.md)                       | <span data-ttu-id="395d5-155">代表憑證的憑證延伸範本。</span><span class="sxs-lookup"><span data-stu-id="395d5-155">Represents the certificate extension template of the certificate.</span></span>                                                       |



 

## <a name="digital-signature-objects"></a><span data-ttu-id="395d5-156">數位簽章物件</span><span class="sxs-lookup"><span data-stu-id="395d5-156">Digital Signature Objects</span></span>

<span data-ttu-id="395d5-157">系統會匯出下列物件以數位方式簽署資料，並驗證數位簽章。</span><span class="sxs-lookup"><span data-stu-id="395d5-157">The following objects are exported to digitally sign data and to verify digital signatures.</span></span>



| <span data-ttu-id="395d5-158">Object</span><span class="sxs-lookup"><span data-stu-id="395d5-158">Object</span></span>                           | <span data-ttu-id="395d5-159">描述</span><span class="sxs-lookup"><span data-stu-id="395d5-159">Description</span></span>                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="395d5-160">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="395d5-160">**SignedCode**</span></span>](signedcode.md) | <span data-ttu-id="395d5-161">提供使用 Authenticode 數位簽章來簽署內容的功能。</span><span class="sxs-lookup"><span data-stu-id="395d5-161">Provides functionality for signing content with an Authenticode digital signature.</span></span> |
| [<span data-ttu-id="395d5-162">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="395d5-162">**SignedData**</span></span>](signeddata.md) | <span data-ttu-id="395d5-163">用來簽署資料和驗證簽署資料簽章的物件。</span><span class="sxs-lookup"><span data-stu-id="395d5-163">Object used to sign data and to verify the signature on signed data.</span></span>               |
| [<span data-ttu-id="395d5-164">**簽署者**</span><span class="sxs-lookup"><span data-stu-id="395d5-164">**Signer**</span></span>](signer.md)         | <span data-ttu-id="395d5-165">單一資料簽署者的資訊，包括簽署者的憑證。</span><span class="sxs-lookup"><span data-stu-id="395d5-165">Information on a single data signer, including the signer's certificate.</span></span>           |
| [<span data-ttu-id="395d5-166">**簽名**</span><span class="sxs-lookup"><span data-stu-id="395d5-166">**Signers**</span></span>](signers.md)       | <span data-ttu-id="395d5-167">[**簽署者**](signer.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-167">Collection of [**Signer**](signer.md) objects.</span></span>                                    |



 

## <a name="enveloped-data-objects"></a><span data-ttu-id="395d5-168">封裝的資料物件</span><span class="sxs-lookup"><span data-stu-id="395d5-168">Enveloped Data Objects</span></span>

<span data-ttu-id="395d5-169">系統會匯出下列物件，以建立用於隱私權的封包資料訊息，以及解密封包訊息中的資料。</span><span class="sxs-lookup"><span data-stu-id="395d5-169">The following objects are exported to create enveloped data messages for privacy and to decrypt data in enveloped messages.</span></span>



| <span data-ttu-id="395d5-170">Object</span><span class="sxs-lookup"><span data-stu-id="395d5-170">Object</span></span>                                 | <span data-ttu-id="395d5-171">描述</span><span class="sxs-lookup"><span data-stu-id="395d5-171">Description</span></span>                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="395d5-172">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="395d5-172">**EnvelopedData**</span></span>](envelopeddata.md) | <span data-ttu-id="395d5-173">用來建立、傳送和接收封包資料的物件。</span><span class="sxs-lookup"><span data-stu-id="395d5-173">Objects used to create, send, and receive enveloped data.</span></span> <span data-ttu-id="395d5-174">封包資料會經過加密，因此只有預期的收件者可以將它解密。</span><span class="sxs-lookup"><span data-stu-id="395d5-174">Enveloped data is encrypted so that only the intended recipients can decrypt it.</span></span> |
| [<span data-ttu-id="395d5-175">**收件者**</span><span class="sxs-lookup"><span data-stu-id="395d5-175">**Recipients**</span></span>](recipients.md)       | <span data-ttu-id="395d5-176">封裝訊息的預定收件者之 [**憑證**](certificate.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-176">Collection of the [**Certificate**](certificate.md) objects of the intended recipients of an enveloped message.</span></span>                           |



 

## <a name="data-encryption-objects"></a><span data-ttu-id="395d5-177">資料加密物件</span><span class="sxs-lookup"><span data-stu-id="395d5-177">Data Encryption Objects</span></span>

<span data-ttu-id="395d5-178">下列物件會被匯出，以加密隱私權的任意資料，並將加密的資料解密。</span><span class="sxs-lookup"><span data-stu-id="395d5-178">The following object is exported to encrypt arbitrary data for privacy and to decrypt encrypted data.</span></span>



| <span data-ttu-id="395d5-179">Object</span><span class="sxs-lookup"><span data-stu-id="395d5-179">Object</span></span>                                 | <span data-ttu-id="395d5-180">描述</span><span class="sxs-lookup"><span data-stu-id="395d5-180">Description</span></span>                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="395d5-181">**A**</span><span class="sxs-lookup"><span data-stu-id="395d5-181">**EncryptedData**</span></span>](encrypteddata.md) | <span data-ttu-id="395d5-182">用來加密資料的物件。</span><span class="sxs-lookup"><span data-stu-id="395d5-182">Objects used to encrypt data.</span></span> <span data-ttu-id="395d5-183">[**A**](encrypteddata.md)物件中的加密資料可以進行解密。</span><span class="sxs-lookup"><span data-stu-id="395d5-183">Encrypted data in an [**EncryptedData**](encrypteddata.md) object can be decrypted.</span></span> |



 

## <a name="auxiliary-objects"></a><span data-ttu-id="395d5-184">輔助物件</span><span class="sxs-lookup"><span data-stu-id="395d5-184">Auxiliary Objects</span></span>

<span data-ttu-id="395d5-185">系統會匯出下列物件，以變更其他物件的預設行為，以及管理憑證、憑證存放區和訊息。</span><span class="sxs-lookup"><span data-stu-id="395d5-185">The following objects are exported to change default behaviors of other objects and to manage certificates, certificate stores, and messages.</span></span>



| <span data-ttu-id="395d5-186">Object</span><span class="sxs-lookup"><span data-stu-id="395d5-186">Object</span></span>                                         | <span data-ttu-id="395d5-187">描述</span><span class="sxs-lookup"><span data-stu-id="395d5-187">Description</span></span>                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="395d5-188">**演算法**</span><span class="sxs-lookup"><span data-stu-id="395d5-188">**Algorithm**</span></span>](algorithm.md)                 | <span data-ttu-id="395d5-189">設定密碼編譯作業中所使用的演算法和 [*金鑰長度*](../secgloss/k-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="395d5-189">Sets the algorithm and [*key length*](../secgloss/k-gly.md) to be used in cryptographic operations.</span></span> |
| [<span data-ttu-id="395d5-190">**屬性**</span><span class="sxs-lookup"><span data-stu-id="395d5-190">**Attribute**</span></span>](attribute.md)                 | <span data-ttu-id="395d5-191">提供與簽章相關的一段新增資訊，例如簽署的時間。</span><span class="sxs-lookup"><span data-stu-id="395d5-191">Provides a single piece of added information about a signature, such as the time of signing.</span></span>                                                    |
| [<span data-ttu-id="395d5-192">**屬性**</span><span class="sxs-lookup"><span data-stu-id="395d5-192">**Attributes**</span></span>](attributes.md)               | <span data-ttu-id="395d5-193">[**屬性**](attribute.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-193">Collection of [**Attribute**](attribute.md) objects.</span></span>                                                                                           |
| [<span data-ttu-id="395d5-194">**BasicConstraints**</span><span class="sxs-lookup"><span data-stu-id="395d5-194">**BasicConstraints**</span></span>](basicconstraints.md)   | <span data-ttu-id="395d5-195">提供對憑證使用基本條件約束的唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="395d5-195">Provides read-only access to basic constraints on the uses of a certificate.</span></span>                                                                    |
| [<span data-ttu-id="395d5-196">**EKU**</span><span class="sxs-lookup"><span data-stu-id="395d5-196">**EKU**</span></span>](eku.md)                             | <span data-ttu-id="395d5-197">提供憑證之 EKU 屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="395d5-197">Provides access to EKU properties of certificates.</span></span>                                                                                              |
| [<span data-ttu-id="395d5-198">**Eku**</span><span class="sxs-lookup"><span data-stu-id="395d5-198">**EKUs**</span></span>](ekus.md)                           | <span data-ttu-id="395d5-199">[**EKU**](eku.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-199">Collection of [**EKU**](eku.md) objects.</span></span>                                                                                                       |
| [<span data-ttu-id="395d5-200">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="395d5-200">**EncodedData**</span></span>](encodeddata.md)             | <span data-ttu-id="395d5-201">代表編碼資料的區塊。</span><span class="sxs-lookup"><span data-stu-id="395d5-201">Represents a block of encoded data.</span></span>                                                                                                             |
| [<span data-ttu-id="395d5-202">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="395d5-202">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)   | <span data-ttu-id="395d5-203">提供對憑證擴充金鑰使用方式屬性的唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="395d5-203">Provides read-only access to the extended key usage properties of certificates.</span></span>                                                                 |
| [<span data-ttu-id="395d5-204">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="395d5-204">**HashedData**</span></span>](hasheddata.md)               | <span data-ttu-id="395d5-205">提供將雜湊演算法套用至字串的功能。</span><span class="sxs-lookup"><span data-stu-id="395d5-205">Provides functionality for applying a hash algorithm to a string.</span></span>                                                                               |
| [<span data-ttu-id="395d5-206">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="395d5-206">**KeyUsage**</span></span>](keyusage.md)                   | <span data-ttu-id="395d5-207">提供憑證的金鑰使用方式屬性的唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="395d5-207">Provides read-only access to key usage properties of certificates.</span></span>                                                                              |
| [<span data-ttu-id="395d5-208">**老**</span><span class="sxs-lookup"><span data-stu-id="395d5-208">**OID**</span></span>](oid.md)                             | <span data-ttu-id="395d5-209">代表數個 CAPICOM 屬性所使用的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="395d5-209">Represents an object identifier that is used by several CAPICOM properties.</span></span>                                                                     |
| [<span data-ttu-id="395d5-210">**Oid**</span><span class="sxs-lookup"><span data-stu-id="395d5-210">**OIDs**</span></span>](oids.md)                           | <span data-ttu-id="395d5-211">表示 [**OID**](oid.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-211">Represents a collection of [**OID**](oid.md) objects.</span></span>                                                                                          |
| [<span data-ttu-id="395d5-212">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="395d5-212">**PolicyInformation**</span></span>](policyinformation.md) | <span data-ttu-id="395d5-213">提供對延伸模組之原則 Oid 的存取。</span><span class="sxs-lookup"><span data-stu-id="395d5-213">Provides access to the policy OIDs of an extension.</span></span>                                                                                             |
| [<span data-ttu-id="395d5-214">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="395d5-214">**Qualifier**</span></span>](qualifier.md)                 | <span data-ttu-id="395d5-215">代表 (CPS) 指標或使用者注意事項辨識符號的認證實務聲明。</span><span class="sxs-lookup"><span data-stu-id="395d5-215">Represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>                                                           |
| [<span data-ttu-id="395d5-216">**限定詞**</span><span class="sxs-lookup"><span data-stu-id="395d5-216">**Qualifiers**</span></span>](qualifiers.md)               | <span data-ttu-id="395d5-217">表示限定詞的集合。</span><span class="sxs-lookup"><span data-stu-id="395d5-217">Represents a collection of qualifiers.</span></span>                                                                                                          |
| [<span data-ttu-id="395d5-218">**設定**</span><span class="sxs-lookup"><span data-stu-id="395d5-218">**Settings**</span></span>](settings.md)                   | <span data-ttu-id="395d5-219">啟用或停用對話方塊，以在未指定身分識別的情況下提示輸入簽署者或寄件者身分識別。</span><span class="sxs-lookup"><span data-stu-id="395d5-219">Enables or disables dialog boxes to prompt for signer or sender identity if that identity is not specified.</span></span>                                     |
| [<span data-ttu-id="395d5-220">**公用程式**</span><span class="sxs-lookup"><span data-stu-id="395d5-220">**Utilities**</span></span>](utilities.md)                 | <span data-ttu-id="395d5-221">提供一般工作的功能。</span><span class="sxs-lookup"><span data-stu-id="395d5-221">Provides functionality for common tasks.</span></span>                                                                                                        |



 

## <a name="interoperability-interfaces"></a><span data-ttu-id="395d5-222">互通性介面</span><span class="sxs-lookup"><span data-stu-id="395d5-222">Interoperability Interfaces</span></span>

<span data-ttu-id="395d5-223">下列介面可讓 CryptoAPI 的衍生與 CAPICOM 2.0 一起運作。</span><span class="sxs-lookup"><span data-stu-id="395d5-223">The following interfaces allow derivations of CryptoAPI to work together with CAPICOM 2.0.</span></span>



| <span data-ttu-id="395d5-224">介面</span><span class="sxs-lookup"><span data-stu-id="395d5-224">Interface</span></span>                              | <span data-ttu-id="395d5-225">描述</span><span class="sxs-lookup"><span data-stu-id="395d5-225">Description</span></span>                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="395d5-226">**ICertCoNtext**</span><span class="sxs-lookup"><span data-stu-id="395d5-226">**ICertContext**</span></span>](icertcontext.md)   | <span data-ttu-id="395d5-227">提供 CAPICOM x.509v3 [**憑證**](certificate.md) 物件內容的存取權。</span><span class="sxs-lookup"><span data-stu-id="395d5-227">Provides access to the context of a CAPICOM X.509v3 [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="395d5-228">此內容可讓 CAPICOM 憑證用於其他的 CryptoAPI 衍生。</span><span class="sxs-lookup"><span data-stu-id="395d5-228">This context allows the CAPICOM certificate to be used in other derivations of CryptoAPI.</span></span> |
| [<span data-ttu-id="395d5-229">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="395d5-229">**ICertStore**</span></span>](icertstore.md)       | <span data-ttu-id="395d5-230">提供 CAPICOM [**存放區**](store.md) 物件內容的存取權。</span><span class="sxs-lookup"><span data-stu-id="395d5-230">Provides access to the context of a CAPICOM [**Store**](store.md) object.</span></span> <span data-ttu-id="395d5-231">此內容允許將 CAPICOM 憑證存放區用於其他的 CryptoAPI 衍生。</span><span class="sxs-lookup"><span data-stu-id="395d5-231">This context allows the CAPICOM certificate store to be used in other derivations of CryptoAPI.</span></span>               |
| [<span data-ttu-id="395d5-232">**IChainCoNtext**</span><span class="sxs-lookup"><span data-stu-id="395d5-232">**IChainContext**</span></span>](ichaincontext.md) | <span data-ttu-id="395d5-233">提供 CAPICOM [**鏈**](chain.md) 物件內容的存取權。</span><span class="sxs-lookup"><span data-stu-id="395d5-233">Provides access to the context of a CAPICOM [**Chain**](chain.md) object.</span></span> <span data-ttu-id="395d5-234">此內容允許將 CAPICOM 憑證信任鏈用於其他的 CryptoAPI 衍生。</span><span class="sxs-lookup"><span data-stu-id="395d5-234">This context allows the CAPICOM certificate trust chain to be used in other derivations of CryptoAPI.</span></span>         |



 

## <a name="enumeration-types"></a><span data-ttu-id="395d5-235">列舉類型</span><span class="sxs-lookup"><span data-stu-id="395d5-235">Enumeration Types</span></span>

<span data-ttu-id="395d5-236">CAPICOM 定義下列列舉類型：</span><span class="sxs-lookup"><span data-stu-id="395d5-236">CAPICOM defines the following enumeration types:</span></span>

-   [<span data-ttu-id="395d5-237">**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 搜尋 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="395d5-237">**CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION**</span></span>](capicom-active-directory-search-location.md)
-   [<span data-ttu-id="395d5-238">**CAPICOM \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="395d5-238">**CAPICOM\_ATTRIBUTE**</span></span>](capicom-attribute.md)
-   [<span data-ttu-id="395d5-239">**CAPICOM \_ CERT \_ 資訊 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="395d5-239">**CAPICOM\_CERT\_INFO\_TYPE**</span></span>](capicom-cert-info-type.md)
-   [<span data-ttu-id="395d5-240">**CAPICOM \_ 憑證 \_ 尋找 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="395d5-240">**CAPICOM\_CERTIFICATE\_FIND\_TYPE**</span></span>](capicom-certificate-find-type.md)
-   [<span data-ttu-id="395d5-241">**CAPICOM \_ 憑證 \_ 包含 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="395d5-241">**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**</span></span>](capicom-certificate-include-option.md)
-   [<span data-ttu-id="395d5-242">**CAPICOM \_ 憑證 \_ 另存新檔 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="395d5-242">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE**</span></span>](capicom-certificate-save-as-type.md)
-   [<span data-ttu-id="395d5-243">**CAPICOM \_ 憑證 \_ 另存新檔 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="395d5-243">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE**</span></span>](capicom-certificates-save-as-type.md)
-   [<span data-ttu-id="395d5-244">**CAPICOM \_ 檢查 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="395d5-244">**CAPICOM\_CHECK\_FLAG**</span></span>](capicom-check-flag.md)
-   [<span data-ttu-id="395d5-245">**CAPICOM \_ EKU**</span><span class="sxs-lookup"><span data-stu-id="395d5-245">**CAPICOM\_EKU**</span></span>](capicom-eku.md)
-   [<span data-ttu-id="395d5-246">**CAPICOM \_ 編碼 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="395d5-246">**CAPICOM\_ENCODING\_TYPE**</span></span>](capicom-encoding-type.md)
-   [<span data-ttu-id="395d5-247">**CAPICOM \_ 加密 \_ 演算法**</span><span class="sxs-lookup"><span data-stu-id="395d5-247">**CAPICOM\_ENCRYPTION\_ALGORITHM**</span></span>](capicom-encryption-algorithm.md)
-   [<span data-ttu-id="395d5-248">**CAPICOM \_ 加密 \_ 金鑰 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="395d5-248">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH**</span></span>](capicom-encryption-key-length.md)
-   [<span data-ttu-id="395d5-249">**CAPICOM \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="395d5-249">**CAPICOM\_ERROR\_CODE**</span></span>](capicom-error-code.md)
-   [<span data-ttu-id="395d5-250">**CAPICOM \_ 匯出 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="395d5-250">**CAPICOM\_EXPORT\_FLAG**</span></span>](capicom-export-flag.md)
-   [<span data-ttu-id="395d5-251">**CAPICOM \_ 雜湊 \_ 演算法**</span><span class="sxs-lookup"><span data-stu-id="395d5-251">**CAPICOM\_HASH\_ALGORITHM**</span></span>](capicom-hash-algorithm.md)
-   [<span data-ttu-id="395d5-252">**CAPICOM \_ 金鑰 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="395d5-252">**CAPICOM\_KEY\_LOCATION**</span></span>](capicom-key-location.md)
-   [<span data-ttu-id="395d5-253">**CAPICOM \_ 金鑰 \_ 規格**</span><span class="sxs-lookup"><span data-stu-id="395d5-253">**CAPICOM\_KEY\_SPEC**</span></span>](capicom-key-spec.md)
-   [<span data-ttu-id="395d5-254">**CAPICOM \_ 金鑰 \_ 儲存 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="395d5-254">**CAPICOM\_KEY\_STORAGE\_FLAG**</span></span>](capicom-key-storage-flag.md)
-   [<span data-ttu-id="395d5-255">**CAPICOM \_ OID**</span><span class="sxs-lookup"><span data-stu-id="395d5-255">**CAPICOM\_OID**</span></span>](capicom-oid.md)
-   [<span data-ttu-id="395d5-256">**CAPICOM \_ PROPID**</span><span class="sxs-lookup"><span data-stu-id="395d5-256">**CAPICOM\_PROPID**</span></span>](capicom-propid.md)
-   [<span data-ttu-id="395d5-257">**CAPICOM \_ >PROV \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="395d5-257">**CAPICOM\_PROV\_TYPE**</span></span>](capicom-prov-type.md)
-   [<span data-ttu-id="395d5-258">**CAPICOM \_ 秘密 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="395d5-258">**CAPICOM\_SECRET\_TYPE**</span></span>](capicom-secret-type.md)
-   [<span data-ttu-id="395d5-259">**CAPICOM \_ 簽署的 \_ 資料 \_ 驗證 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="395d5-259">**CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG**</span></span>](capicom-signed-data-verify-flag.md)
-   [<span data-ttu-id="395d5-260">**CAPICOM \_ 存放區 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="395d5-260">**CAPICOM\_STORE\_LOCATION**</span></span>](capicom-store-location.md)
-   [<span data-ttu-id="395d5-261">**CAPICOM \_ 存放區 \_ 開啟 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="395d5-261">**CAPICOM\_STORE\_OPEN\_MODE**</span></span>](capicom-store-open-mode.md)
-   [<span data-ttu-id="395d5-262">**CAPICOM \_ 存放 \_ 區 \_ 的儲存 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="395d5-262">**CAPICOM\_STORE\_SAVE\_AS\_TYPE**</span></span>](capicom-store-save-as-type.md)

 

 
