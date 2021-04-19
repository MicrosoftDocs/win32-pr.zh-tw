---
description: PKCS \# 7 是一種密碼編譯訊息語法標準。
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: PKCS \# 7 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0c7bc9b991a6625cae36ae9857275a9d86786a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997565"
---
# <a name="pkcs-7-attributes"></a><span data-ttu-id="3bd90-103">PKCS \# 7 屬性</span><span class="sxs-lookup"><span data-stu-id="3bd90-103">PKCS \#7 Attributes</span></span>

<span data-ttu-id="3bd90-104">PKCS \# 7 是一種密碼編譯訊息語法標準。</span><span class="sxs-lookup"><span data-stu-id="3bd90-104">PKCS \#7 is a cryptographic message syntax standard.</span></span> <span data-ttu-id="3bd90-105">PKCS \# 7 訊息本身不會構成憑證要求，但可 \# 使用下列其中一種內容類型，將 pkcs 10 或 CMC 要求封裝在 **ContentInfo** 的 asn.1 結構中。</span><span class="sxs-lookup"><span data-stu-id="3bd90-105">A PKCS \#7 message does not, by itself, constitute a certificate request, but it can encapsulate a PKCS \#10 or CMC request in a **ContentInfo** ASN.1 structure by using one of the following content types.</span></span> <span data-ttu-id="3bd90-106">封裝可讓您新增額外的功能，例如多個簽章，但無法使用。</span><span class="sxs-lookup"><span data-stu-id="3bd90-106">Encapsulation enables you to add extra functionality, such as multiple signatures, that is not otherwise available.</span></span>

-   <span data-ttu-id="3bd90-107">**資料**</span><span class="sxs-lookup"><span data-stu-id="3bd90-107">**Data**</span></span>
-   <span data-ttu-id="3bd90-108">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="3bd90-108">**SignedData**</span></span>
-   <span data-ttu-id="3bd90-109">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="3bd90-109">**EnvelopedData**</span></span>
-   <span data-ttu-id="3bd90-110">**SignedAndEnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="3bd90-110">**SignedAndEnvelopedData**</span></span>
-   <span data-ttu-id="3bd90-111">**DigestedData**</span><span class="sxs-lookup"><span data-stu-id="3bd90-111">**DigestedData**</span></span>
-   <span data-ttu-id="3bd90-112">**A**</span><span class="sxs-lookup"><span data-stu-id="3bd90-112">**EncryptedData**</span></span>

<span data-ttu-id="3bd90-113">您可以將屬性新增至 **SignedData** 內容類型的 **authenticatedAttributes** 和 **unauthenticatedAttributes** 欄位。</span><span class="sxs-lookup"><span data-stu-id="3bd90-113">Attributes can be added to the **authenticatedAttributes** and **unauthenticatedAttributes** fields of the **SignedData** content type.</span></span>

``` syntax
SignedData ::= SEQUENCE 
{
   version             INTEGER,
   digestAlgorithms    DigestAlgorithmIdentifiers,
   contentInfo         ContentInfo,
   certificates        [0] IMPLICIT Certificates OPTIONAL,
   crls                [1] IMPLICIT CertificateRevocationLists OPTIONAL,
   signerInfos         SignerInfos
}

SignerInfos ::= SET OF SignerInfo

SignerInfo ::= SEQUENCE 
{
    version                     INTEGER,
    sid                         CertIdentifier,
    digestAlgorithm             DigestAlgorithmIdentifier,
    authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
    digestEncryptionAlgorithm   DigestEncryptionAlgId,
    encryptedDigest             EncryptedDigest,
    unauthenticatedAttributes   [1] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="3bd90-114">在憑證授權單位單位 (CA 上封存用戶端私密金鑰所需的程式) 會提供已驗證 (簽署) 屬性的完整範例，以及如何使用未驗證的屬性：</span><span class="sxs-lookup"><span data-stu-id="3bd90-114">The process required to archive a client's private key on a certification authority (CA) provides a comprehensive example of how authenticated (signed) attributes and the unauthenticated attributes can be used:</span></span>

-   <span data-ttu-id="3bd90-115">用戶端會建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件，並針對所要求的憑證類型新增適當的資料。</span><span class="sxs-lookup"><span data-stu-id="3bd90-115">The client creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and adds appropriate data for the type of certificate being requested.</span></span>
-   <span data-ttu-id="3bd90-116">用戶端會使用 PKCS \# 10 要求來初始化 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件。</span><span class="sxs-lookup"><span data-stu-id="3bd90-116">The client uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="3bd90-117">PKCS \# 10 要求會放入 CMC 要求中的 **TaggedRequest** 結構。</span><span class="sxs-lookup"><span data-stu-id="3bd90-117">The PKCS \#10 request is placed into the **TaggedRequest** structure in the CMC request.</span></span> <span data-ttu-id="3bd90-118">如需詳細資訊，請參閱 [CMC 屬性](cmc-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="3bd90-118">For more information, see [CMC Attributes](cmc-attributes.md).</span></span>
-   <span data-ttu-id="3bd90-119">用戶端會加密私用金鑰，並使用它來初始化 [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) 物件。</span><span class="sxs-lookup"><span data-stu-id="3bd90-119">The client encrypts a private key and uses it to initialize an [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) object.</span></span> <span data-ttu-id="3bd90-120">新的 **ArchiveKey** 屬性會封裝在 **EnvelopedData** 結構中。</span><span class="sxs-lookup"><span data-stu-id="3bd90-120">The new **ArchiveKey** attribute is encapsulated in an **EnvelopedData** structure.</span></span>

    ``` syntax
    EnvelopedData ::= SEQUENCE 
    {
        version                 INTEGER,
        recipientInfos          RecipientInfos,
        encryptedContentInfo    EncryptedContentInfo
    } 

    RecipientInfos ::= SET OF RecipientInfo

    EncryptedContentInfo ::= SEQUENCE 
    {
        contentType                 ContentType,
        contentEncryptionAlgorithm  ContentEncryptionAlgId,
        encryptedContent            [0] IMPLICIT EncryptedContent OPTIONAL
    } 

    EncryptedContent ::= OCTET STRING

    RecipientInfo ::= SEQUENCE 
    {
        version                 INTEGER,
        issuerAndSerialNumber   IssuerAndSerialNumber,
        keyEncryptionAlgorithm  KeyEncryptionAlgId,
        encryptedKey            EncryptedKey
    } 
    ```

-   <span data-ttu-id="3bd90-121">用戶端會建立加密金鑰的 SHA-1 雜湊，並用它來初始化 [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) 物件。</span><span class="sxs-lookup"><span data-stu-id="3bd90-121">The client creates a SHA-1 hash of the encrypted key and uses it to initialize an [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) object.</span></span>
-   <span data-ttu-id="3bd90-122">用戶端會從 CMC 要求抓取 [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) 集合，並將 **ArchiveKey** 和 **ArchiveKeyHash** 屬性新增至其中。</span><span class="sxs-lookup"><span data-stu-id="3bd90-122">The client retrieves the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) collection from the CMC request and adds the **ArchiveKey** and the **ArchiveKeyHash** attributes to it.</span></span> <span data-ttu-id="3bd90-123">這些屬性會放入 CMC 要求的 **TaggedAttributes** 結構中。</span><span class="sxs-lookup"><span data-stu-id="3bd90-123">The attributes are placed into the **TaggedAttributes** structure of the CMC request.</span></span>
-   <span data-ttu-id="3bd90-124">用戶端會使用 CMC 要求來初始化 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 物件。</span><span class="sxs-lookup"><span data-stu-id="3bd90-124">The client uses the CMC request to initialize an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object.</span></span> <span data-ttu-id="3bd90-125">這會將 CMC 要求放入 PKCS \# 7 **SignedData** 結構的 contentInfo 欄位中。</span><span class="sxs-lookup"><span data-stu-id="3bd90-125">This places the CMC request into the **contentInfo** field of the PKCS \#7 **SignedData** structure.</span></span>
-   <span data-ttu-id="3bd90-126">**ArchiveKeyHash** 屬性已簽署，並放在 **SignerInfo** 結構的 **authenticatedAttributes** 序列中。</span><span class="sxs-lookup"><span data-stu-id="3bd90-126">The **ArchiveKeyHash** attribute is signed and placed in the **authenticatedAttributes** sequence of the **SignerInfo** structure.</span></span>
-   <span data-ttu-id="3bd90-127">**ArchiveKey** 屬性會放在與 PKCS 7 訊息的主要簽署者相關聯之 **SignerInfo** 結構的 **unauthenticatedAttributes** 序列中 \# 。</span><span class="sxs-lookup"><span data-stu-id="3bd90-127">The **ArchiveKey** attribute is placed in the **unauthenticatedAttributes** sequence of the **SignerInfo** structure associated with the primary signer of the PKCS \#7 message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bd90-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="3bd90-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bd90-129">支援的屬性</span><span class="sxs-lookup"><span data-stu-id="3bd90-129">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



