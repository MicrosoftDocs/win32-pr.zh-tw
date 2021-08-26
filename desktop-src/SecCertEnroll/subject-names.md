---
description: PKCS 10 憑證要求的 [主旨] 欄位 \# 包含要求憑證之實體的分辨名稱。
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Subject Names
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be70af23c524e71c1a9b22f43e391e4f5c8302fba70f24fba1f8268ebfda6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101098"
---
# <a name="subject-names"></a>Subject Names

PKCS 10 憑證要求的 [主旨 **] 欄位** \# 包含要求憑證之實體的分辨名稱。

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

辨別名稱是由一系列 (RDNs) 的相對辨別名稱所組成。 每個 RDN 都包含一組屬性，而每個屬性都是由物件識別碼和值所組成。 值的資料類型是由 **DirectoryString** 結構所識別。

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

如需詳細資訊，請參閱下列主題：

-   [建立主體名稱](creating-a-subject-name.md)
-   [編碼主體名稱](encoding-a-subject-name.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[要求](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
