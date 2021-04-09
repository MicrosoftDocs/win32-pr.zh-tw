---
description: X.509 第1版憑證包含下欄欄位。 第2版欄位中會討論第2版欄位。 第3版的延伸模組會討論第3版欄位。
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: 基本欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad24afa21787227b3fe47ab187a97c7886c9c9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849250"
---
# <a name="basic-fields"></a>基本欄位

X.509 第1版憑證包含下欄欄位。 第 [2 版欄位](about-version-2-fields.md)中會討論第2版欄位。 第3版的 [延伸](about-version-3-extensions.md)模組會討論第3版欄位。

## <a name="version"></a>版本

指定編碼憑證的版本編號。 目前，此欄位的可能值為0、1或2，但未來可能會擴大。

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a>序號

包含一個由憑證授權單位 (CA) 指派給憑證的唯一正整數。

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a>簽章演算法

包含 (OID) 的 [*物件識別碼*](/windows/desktop/SecGloss/o-gly) ，可指定 CA 用來簽署憑證的演算法。 例如，1.2.840.113549.1.1.5 指定 SHA-1 雜湊演算法結合來自 RSA Laboratories 制定的 RSA 加密演算法。

``` syntax
---------------------------------------------------------------------
-- Signature OID
---------------------------------------------------------------------
signature ::= AlgorithmIdentifier

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="issuer"></a>Issuer

包含建立和簽署憑證之 CA (DN) 的 [*x.500 辨別名稱。*](/windows/desktop/SecGloss/x-gly)

``` syntax
---------------------------------------------------------------------
-- Issuer name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="validity"></a>有效期

指定憑證有效的時間間隔。 2049結尾的日期會使用國際標準時間 (格林尼治平均時間) 格式 (*yymmddhhmmssz*) 。 從2050年1月1日開始的日期會使用一般化時間格式 (*yyyymmddhhmmssz*) 。

``` syntax
---------------------------------------------------------------------
-- Validity period 
---------------------------------------------------------------------
Validity ::= SEQUENCE 
{
  notBefore           ChoiceOfTime,
  notAfter            ChoiceOfTime
}

ChoiceOfTime ::= CHOICE 
{
  utcTime                 UTCTime,
  generalTime             GeneralizedTime
}
```

## <a name="subject"></a>主體

包含實體的 X.500 辨別名稱，該實體與憑證中包含的公開金鑰相關聯。

``` syntax
---------------------------------------------------------------------
-- Subject name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="public-key"></a>公開金鑰

包含公開金鑰和相關聯的演算法資訊。

``` syntax
---------------------------------------------------------------------
--  Subject public key information
---------------------------------------------------------------------
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
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[第2版欄位](about-version-2-fields.md)
</dt> <dt>

[第3版擴充功能](about-version-3-extensions.md)
</dt> <dt>

[X.509 公開金鑰憑證](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
