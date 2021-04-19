---
description: 資料類型的概念是抽象語法標記法 (一)  (asn.1) 標準的基礎。
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: ASN. 1 類型系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbf60bf61e32c5fca882f2e40c946c043ef93e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976585"
---
# <a name="asn1-type-system"></a>ASN. 1 類型系統

資料類型的概念是抽象語法標記法 (一)  (asn.1) 標準的基礎。 憑證要求結構的每個欄位都與型別相關聯。 例如，請考慮 \# 下列範例所示的 PKCS 10 ASN. 1 憑證語法。

``` syntax
--------------------------------------------------------------------
-- PKCS #10 Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

--------------------------------------------------------------------
-- Version number.
--------------------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

--------------------------------------------------------------------
-- Subject distinguished name (DN).
--------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}

--------------------------------------------------------------------
-- Public key information.
--------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
   algorithm           AlgorithmIdentifier,
   subjectPublicKey    BITSTRING
}

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
} 

--------------------------------------------------------------------
-- Attributes.
--------------------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   values             AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
```

高階要求結構 **CertificationRequestInfo** 是由其他類型的序列所組成的型別。 當類型為或只包含基本類型、字串類型或 **任何** 類型時，就無法進一步細分。 例如，[ **版本** ] 欄位是一種 **CertificationRequestInfoVersion** 型別，也就是 **整數** 類型，這是一個不是從其他型別組成的基本 asn.1 型別。

型別系統可讓要求的語法以視覺化方式呈現，以方便開發人員理解，並可讓要求一致地編碼，以便透過網路傳輸。 如需編碼的詳細資訊，請參閱 [可辨別編碼規則](distinguished-encoding-rules.md)。 如需有關 asn.1 類型的詳細資訊，請參閱下列主題。

[基本類型](about-basic-types.md)

討論下列資料類型：

* **位字串**
* **布林**
* **INTEGER**
* **NULL**
* **物件識別碼**
* **八位字串**

[字串類型](about-string-types.md)

討論下列字串類型：

* **BMPString**
* **IA5String**
* **PrintableString**
* **TeletexString**
* **UTF8String**

[結構化類型](about-constructed-types.md)

討論 asn.1 資料類型，其中可以包含基本類型、字串類型或其他結構化類型。




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[憑證要求編碼](about-certificate-request-encoding.md)
</dt> <dt>

[以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[可辨別編碼規則](distinguished-encoding-rules.md)
</dt> <dt>

[ASN. 1 語法和編碼簡介](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



