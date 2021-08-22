---
description: 用來將屬性新增至憑證要求。
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: 屬性架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d09a2a351635547c21357477290cb3335cb8c1da042d680762140b48b03f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903235"
---
# <a name="attribute-architecture"></a>屬性架構

下列介面是用來將屬性新增至憑證要求：

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

架構如下所示，在 PKCS \# 10 認證要求語法的 asn.1 模組中定義。

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)集合會對應到 [**屬性**] 欄位，而集合中的每個 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)物件都會對應到一個 asn.1 **屬性** 結構。

每個 **屬性** 都包含 (oid) 的物件識別碼，以及與 oid 相關聯的零或多個值。 單一 OID/值組會以 [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) 介面表示。 您可以使用 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合來初始化 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件，但集合中的每個屬性都必須與相同的 OID 相關聯。 一般來說，屬性只有一個值。

您可以使用下列任何衍生自 [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)的介面，建立單一 OID/值屬性組：

-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

例如，下列程式說明如何建立 **ClientId** 屬性。

**若要建立 **ClientId** 屬性**

1.  從 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)或 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)物件取出 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)物件。
2.  建立並初始化 [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) 物件。
3.  建立 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合，並新增 [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) 物件。
4.  使用 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合來初始化 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件。
5.  將 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件新增至步驟1中所取出的集合。

下列範例顯示 **ClientId** 屬性的 asn.1 輸出。 屬性包含產生要求之電腦的 DNS 名稱 (test3d.jdomcsc.nttest.microsoft.com) 、使用者的 SAM 名稱 (JDOMCSC \\ administrator) ，以及產生要求 (certreq) 的應用程式名稱。

``` syntax
0136: 30 57; SEQUENCE (57 Bytes)
0138: |  06 09                            ; OBJECT_ID (9 Bytes)
013a: |  |  2b 06 01 04 01 82 37 15  14
      |  |     ; 1.3.6.1.4.1.311.21.20 Client Information
0143: |  |  31 4a                         ; SET (4a Bytes)
0145: |  |     30 48                      ; SEQUENCE (48 Bytes)
0147: |  |        02 01                   ; INTEGER (1 Bytes)
0149: |  |        |  09
014a: |  |        0c 23                   ; UTF8_STRING (23 Bytes)
014c: |  |        |  74 65 73 74 33 64 2e 6a  64 6f 6d 63 73 63 2e 6e 
015c: |  |        |  74 74 65 73 74 2e 6d 69  63 72 6f 73 6f 66 74 2e 
016c: |  |        |  63 6f 6d                                         
      |  |        |     ; "test3d.jdomcsc.nttest.microsoft.com"
016f: |  |        0c 15                   ; UTF8_STRING (15 Bytes)
0171: |  |        |  4a 44 4f 4d 43 53 43 5c  61 64 6d 69 6e 69 73 74 
0181: |  |        |  72 61 74 6f 72                                   
      |  |        |     ; "JDOMCSC\administrator"
0186: |  |        0c 07                   ; UTF8_STRING (7 Bytes)
0188: |  |           63 65 72 74 72 65 71                             
      |  |              ; "certreq"
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



