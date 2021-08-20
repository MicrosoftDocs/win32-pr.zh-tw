---
description: 憑證註冊 API 支援下列基本的 ASN. 1 類型。
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: 基本類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e2cc1b8825872789d095616e868fe39e306736583f8ea1784543808b7ec4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905043"
---
# <a name="basic-types"></a>基本類型

憑證註冊 API 支援下列基本的 ASN. 1 類型。

## <a name="bit-string"></a>位字串

編碼標記：0x03

Certreq.exe 名稱：位 \_ 字串

位或二進位字串是任意長的位陣列。 您可以使用以括弧括住的整數和指派的名稱來識別特定位，如下列範例所示。

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

憑證金鑰和簽章通常會以位字串表示。

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BIT STRING
-- Tag number: 0x03
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BIT STRING
} 
```

## <a name="boolean"></a>BOOLEAN

編碼標記：0x01

Certreq.exe 名稱：布林值

布林值類型可以包含下列兩個值的其中一個： **TRUE** 或 **FALSE**。 下列範例顯示基本條件約束憑證延伸的 asn.1 結構。 **Ca** 欄位會指定憑證主體是否為憑證授權單位單位 (cA) 。 預設重要性為 **FALSE**。

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BOOLEAN
-- Tag number: 0x01
---------------------------------------------------------------------
BasicConstraints ::= SEQUENCE 
{
  cA                  BOOLEAN DEFAULT FALSE,
  pathLenConstraint   INTEGER OPTIONAL
}
```

## <a name="integer"></a>INTEGER

編碼標記：0x02

Certreq.exe 名稱：整數

整數通常可以是任何正數或負整數值。 下列範例顯示 RSA 公開金鑰的 asn.1 結構。 請注意， **publicExponent** 欄位限制為小於4294967296的正整數。

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: INTEGER
-- Tag number: 0x02
---------------------------------------------------------------------
HUGEINTEGER ::= INTEGER

RSAPublicKey ::= SEQUENCE 
{ 
  modulus         HUGEINTEGER,    
  publicExponent  INTEGER (0..4294967295) 
} 
```

## <a name="null"></a>NULL

編碼標記：0x05

Certreq.exe 名稱： **Null**

**Null** 型別包含單一位元組0x00。 憑證要求必須指出空白值的任何地方都可以使用它。 例如， **AlgorithmIdentifier** 是一個序列，其中包含 (OID) 和選擇性參數的物件識別碼。

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: NULL
-- Tag number: 0x05
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

如果在結構編碼時沒有任何參數，則會使用 **Null** 來表示空的值。

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a>物件識別碼

編碼標記：0x06

Certreq.exe 名稱：物件 \_ 識別碼

憑證註冊 API 使用 (Oid) 的物件識別碼，做為演算法識別碼、屬性和其他 PKI 專案的通用指標類型。 Oid 通常是以點分隔的十進位字串來呈現，例如 "2.16.840.1.101.3.4.1.42"。 字串中的個別元素（以句號分隔）代表在註冊授權單位樹狀結構中，用來唯一識別物件和所註冊之物件的弧形和離職。 例如，先前的 OID 可以擴充為聯合-iso-itu-t (2) country (16) us (840) 組織 (1) gov (101) csor (3) nistAlgorithms (4) aesAlgs (1) ，並附加42，以唯一識別256位 AES 加密區塊鏈 (CBC) 模式演算法。

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OBJECT IDENTIFIER
-- Tag number: 0x06
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="octet-string"></a>八位字串

編碼標記：0x04

Certreq.exe 名稱：八位 \_ 字串

八位字串是任意大的位元組陣列。 但是不同于 **位字串** 類型，字串中的特定位和位元組不能被指派名稱。 八位字組是指一種與平臺無關的方式來參考記憶體單字。 在憑證註冊 API 的內容中，八進位和位元組是可互換的。

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OCTET STRING
-- Tag number: 0x04
---------------------------------------------------------------------
AuthorityKeyId ::= SEQUENCE 
{
  keyIdentifier       [0] IMPLICIT OCTET STRING OPTIONAL,
  certIssuer          [1] EXPLICIT NAME
  certSerialNumber    [2] IMPLICIT INTEGER OPTIONAL
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASN. 1 類型系統](about-asn-1-type-system.md)
</dt> <dt>

[可辨別編碼規則](distinguished-encoding-rules.md)
</dt> <dt>

[以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



