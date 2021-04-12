---
description: 公開金鑰基礎結構 (PKI) 最常見的用法之一，就是建立一個 x.500 辨別名稱。
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: 字串類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192744"
---
# <a name="string-types"></a>字串類型

公開金鑰基礎結構 (PKI) 最常見的用法之一，就是建立一個 x.500 辨別名稱。 例如，藉由結合一系列的相對辨別名稱來建立憑證要求的主體名稱，如下列語法範例所示。

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
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

憑證註冊 API 支援下列 ASN. 1 字串類型。

## <a name="bmpstring"></a>BMPString

編碼標記：0x1E

Certreq.exe 名稱： UNICODE \_ 字串

 (BMP) 的基本多語系平面是字元編碼，其中包含通用字元集 (UCS) 的第一個平面。 有17個平面編號為0到16。 BMP 佔據平面0，並包括從0x0000 到0xFFFF 的65536程式碼點。 這是 Unicode 字元對應的一部分，其中大部分的字元指派都有到目前為止。 其中包括拉丁、中東、亞洲、非洲和其他語言。

## <a name="ia5string"></a>IA5String

編碼標記：0x16

Certreq.exe 名稱： IA5 \_ 字串

國際字母數位 5 (IA5) 通常等同于 ASCII 字母，但不同的版本可以包含地區語言專屬的重音或其他字元。 下列範例顯示 **AlternativeNames** 憑證延伸的 asn.1 定義中使用的 **IA5String** 類型。

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a>PrintableString

編碼標記：0x13

Certreq.exe 名稱：可列印的 \_ 字串

**PrintableString** 資料類型原本是用來代表可供大型主機輸入終端機使用的有限字元集，但仍常使用。 它包含下列字元：

-   A-Z
-   a-z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>TeletexString

編碼標記：0x14

**TeletexString** 和相關的 **T61String** 資料類型會編碼在8個位 (或16位用於複合字元) 。 它們都有0x14 的標記編號。 這些都不是廣泛使用。

## <a name="utf8string"></a>UTF8String

編碼標記：0x0C

Certreq.exe 名稱： UTF8 \_ 字串

8位的 UCS/Unicode 轉換格式 (UTF-8) 是可將任何通用字元表示為 Unicode 字元的可變長度字元編碼，同時允許初始程式碼點與 ASCII 保持一致。 UTF-8 使用一到四個位元組。 標記編號為0x0C。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASN. 1 類型系統](about-asn-1-type-system.md)
</dt> <dt>

[可辨別編碼規則](distinguished-encoding-rules.md)
</dt> <dt>

[以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



