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
# <a name="pkcs-7-attributes"></a>PKCS \# 7 屬性

PKCS \# 7 是一種密碼編譯訊息語法標準。 PKCS \# 7 訊息本身不會構成憑證要求，但可 \# 使用下列其中一種內容類型，將 pkcs 10 或 CMC 要求封裝在 **ContentInfo** 的 asn.1 結構中。 封裝可讓您新增額外的功能，例如多個簽章，但無法使用。

-   **資料**
-   **SignedData**
-   **EnvelopedData**
-   **SignedAndEnvelopedData**
-   **DigestedData**
-   **A**

您可以將屬性新增至 **SignedData** 內容類型的 **authenticatedAttributes** 和 **unauthenticatedAttributes** 欄位。

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

在憑證授權單位單位 (CA 上封存用戶端私密金鑰所需的程式) 會提供已驗證 (簽署) 屬性的完整範例，以及如何使用未驗證的屬性：

-   用戶端會建立 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件，並針對所要求的憑證類型新增適當的資料。
-   用戶端會使用 PKCS \# 10 要求來初始化 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件。 PKCS \# 10 要求會放入 CMC 要求中的 **TaggedRequest** 結構。 如需詳細資訊，請參閱 [CMC 屬性](cmc-attributes.md)。
-   用戶端會加密私用金鑰，並使用它來初始化 [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) 物件。 新的 **ArchiveKey** 屬性會封裝在 **EnvelopedData** 結構中。

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

-   用戶端會建立加密金鑰的 SHA-1 雜湊，並用它來初始化 [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) 物件。
-   用戶端會從 CMC 要求抓取 [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) 集合，並將 **ArchiveKey** 和 **ArchiveKeyHash** 屬性新增至其中。 這些屬性會放入 CMC 要求的 **TaggedAttributes** 結構中。
-   用戶端會使用 CMC 要求來初始化 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 物件。 這會將 CMC 要求放入 PKCS \# 7 **SignedData** 結構的 contentInfo 欄位中。
-   **ArchiveKeyHash** 屬性已簽署，並放在 **SignerInfo** 結構的 **authenticatedAttributes** 序列中。
-   **ArchiveKey** 屬性會放在與 PKCS 7 訊息的主要簽署者相關聯之 **SignerInfo** 結構的 **unauthenticatedAttributes** 序列中 \# 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[支援的屬性](supported-attributes.md)
</dt> </dl>

 

 



