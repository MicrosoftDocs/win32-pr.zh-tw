---
description: 結構化的抽象語法標記法 (一)  (asn.1) 類型是由基本類型、字串類型或其他結構化類型所組成。 例如，x.509 憑證延伸是由下列範例所示的三個基本 ASN. 1 類型所組成。
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: 結構化類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a515e6e03ebf3c95ff1cabc1bf7f12eb423df27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973243"
---
# <a name="constructed-types"></a>結構化類型

結構化的 [*抽象語法標記法 (一)*](/windows/desktop/SecGloss/a-gly) (asn.1) 類型是由基本類型、字串類型或其他結構化類型所組成。 例如，x.509 憑證延伸是由下列範例所示的三個基本 ASN. 1 類型所組成。

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

延伸模組是由 (OID) 的 [*物件識別碼*](/windows/desktop/SecGloss/o-gly) 、識別延伸模組是否為關鍵的布林值，以及包含值的位元組陣列所組成。 憑證註冊 API 支援下列已建立的 ASN. 1 類型。

## <a name="sequence-and-sequence-of"></a>的順序和順序

編碼標記：0x30<

包含一或多個類型的已排序欄位系列。 欄位可以標記為 **選擇性** 或 **預設值**。 此外，為了避免在解碼時出現不明確的情況，您可以使用唯一識別碼 (有括弧的整數（例如 \[ 1 \]) 和從下列範例所示的必要欄位），以使連續的選擇性欄位彼此不同。

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

**Sequence** 與 **sequence** 之間的差異在於，一 **系列** 結構的元素必須屬於相同的型別。 請參閱下列範例。 在編碼時，這兩個結構的標記值 (0x30<) 相同。

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

另一種查看 **sequence** 與 **sequence** 之間差異的方法，是用 C 程式設計語言來比較它們與其對應專案。 也就是說， **sequence** 大致上相當於結構，而 **序列** 則大致等同于陣列。

## <a name="set-and-set-of"></a>集合和集合

編碼標記：0x31

包含一或多個類型之未排序的欄位系列。 這與包含已排序清單的 **順序** 不同。 指定未排序的清單可讓應用程式以最適當的順序將結構欄位提供給編碼器。 如同 **順序** 一樣， **SET** 結構的欄位可以使用 **選擇性** 或 **預設值** 來標記，而且必須使用唯一識別碼來區分解碼處理常式。 **Set** 和 **set** 之間的差異在於，一 **組** 結構的元素必須屬於相同的型別。

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>選擇

編碼標記：不適用

定義替代專案之間的選擇。 每個替代項都必須以括弧括住的整數來唯一識別，以避免在解碼時有混淆。 編碼之後， **選擇** 結構將會有所選替代的編碼標記值。

``` syntax
AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SeqOfAny,
   directoryName           [4] EXPLICIT Name,
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASN. 1 類型系統](about-asn-1-type-system.md)
</dt> <dt>

[以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[可辨別編碼規則](distinguished-encoding-rules.md)
</dt> </dl>

 

 
