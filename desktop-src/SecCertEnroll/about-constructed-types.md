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
# <a name="constructed-types"></a><span data-ttu-id="77b0d-104">結構化類型</span><span class="sxs-lookup"><span data-stu-id="77b0d-104">Constructed Types</span></span>

<span data-ttu-id="77b0d-105">結構化的 [*抽象語法標記法 (一)*](/windows/desktop/SecGloss/a-gly) (asn.1) 類型是由基本類型、字串類型或其他結構化類型所組成。</span><span class="sxs-lookup"><span data-stu-id="77b0d-105">A constructed [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) type is made up from basic types, string types, or other constructed types.</span></span> <span data-ttu-id="77b0d-106">例如，x.509 憑證延伸是由下列範例所示的三個基本 ASN. 1 類型所組成。</span><span class="sxs-lookup"><span data-stu-id="77b0d-106">For example, an X.509 certificate extension is composed from three basic ASN.1 types as shown by the following example.</span></span>

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

<span data-ttu-id="77b0d-107">延伸模組是由 (OID) 的 [*物件識別碼*](/windows/desktop/SecGloss/o-gly) 、識別延伸模組是否為關鍵的布林值，以及包含值的位元組陣列所組成。</span><span class="sxs-lookup"><span data-stu-id="77b0d-107">An extension consists of an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the value.</span></span> <span data-ttu-id="77b0d-108">憑證註冊 API 支援下列已建立的 ASN. 1 類型。</span><span class="sxs-lookup"><span data-stu-id="77b0d-108">The Certificate Enrollment API supports the following constructed ASN.1 types.</span></span>

## <a name="sequence-and-sequence-of"></a><span data-ttu-id="77b0d-109">的順序和順序</span><span class="sxs-lookup"><span data-stu-id="77b0d-109">SEQUENCE and SEQUENCE OF</span></span>

<span data-ttu-id="77b0d-110">編碼標記：0x30<</span><span class="sxs-lookup"><span data-stu-id="77b0d-110">Encoding tag: 0x30</span></span>

<span data-ttu-id="77b0d-111">包含一或多個類型的已排序欄位系列。</span><span class="sxs-lookup"><span data-stu-id="77b0d-111">Contains an ordered series of fields of one or more types.</span></span> <span data-ttu-id="77b0d-112">欄位可以標記為 **選擇性** 或 **預設值**。</span><span class="sxs-lookup"><span data-stu-id="77b0d-112">Fields can be marked **OPTIONAL** or **DEFAULT**.</span></span> <span data-ttu-id="77b0d-113">此外，為了避免在解碼時出現不明確的情況，您可以使用唯一識別碼 (有括弧的整數（例如 \[ 1 \]) 和從下列範例所示的必要欄位），以使連續的選擇性欄位彼此不同。</span><span class="sxs-lookup"><span data-stu-id="77b0d-113">Also, to avoid ambiguity when decoding, successive optional fields should differ from one another by use of a unique identifier (a bracketed integer such as \[1\]) and from a following required field as shown by the following example.</span></span>

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

<span data-ttu-id="77b0d-114">**Sequence** 與 **sequence** 之間的差異在於，一 **系列** 結構的元素必須屬於相同的型別。</span><span class="sxs-lookup"><span data-stu-id="77b0d-114">The difference between **SEQUENCE** and **SEQUENCE OF** is that the elements of a **SEQUENCE OF** construct must be of the same type.</span></span> <span data-ttu-id="77b0d-115">請參閱下列範例。</span><span class="sxs-lookup"><span data-stu-id="77b0d-115">See the following example.</span></span> <span data-ttu-id="77b0d-116">在編碼時，這兩個結構的標記值 (0x30<) 相同。</span><span class="sxs-lookup"><span data-stu-id="77b0d-116">Both constructs have the same tag value (0x30) when encoded.</span></span>

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

<span data-ttu-id="77b0d-117">另一種查看 **sequence** 與 **sequence** 之間差異的方法，是用 C 程式設計語言來比較它們與其對應專案。</span><span class="sxs-lookup"><span data-stu-id="77b0d-117">Another way to look at the difference between **SEQUENCE** and **SEQUENCE OF** is to compare them to their counterparts in the C programming language.</span></span> <span data-ttu-id="77b0d-118">也就是說， **sequence** 大致上相當於結構，而 **序列** 則大致等同于陣列。</span><span class="sxs-lookup"><span data-stu-id="77b0d-118">That is, **SEQUENCE** is roughly equivalent to a structure and **SEQUENCE OF** is roughly equivalent to an array.</span></span>

## <a name="set-and-set-of"></a><span data-ttu-id="77b0d-119">集合和集合</span><span class="sxs-lookup"><span data-stu-id="77b0d-119">SET and SET OF</span></span>

<span data-ttu-id="77b0d-120">編碼標記：0x31</span><span class="sxs-lookup"><span data-stu-id="77b0d-120">Encoding tag: 0x31</span></span>

<span data-ttu-id="77b0d-121">包含一或多個類型之未排序的欄位系列。</span><span class="sxs-lookup"><span data-stu-id="77b0d-121">Contains an unordered series of fields of one or more types.</span></span> <span data-ttu-id="77b0d-122">這與包含已排序清單的 **順序** 不同。</span><span class="sxs-lookup"><span data-stu-id="77b0d-122">This differs from a **SEQUENCE** which contains an ordered list.</span></span> <span data-ttu-id="77b0d-123">指定未排序的清單可讓應用程式以最適當的順序將結構欄位提供給編碼器。</span><span class="sxs-lookup"><span data-stu-id="77b0d-123">Specifying an unordered list enables an application to provide the structure fields to the encoder in the most appropriate order.</span></span> <span data-ttu-id="77b0d-124">如同 **順序** 一樣， **SET** 結構的欄位可以使用 **選擇性** 或 **預設值** 來標記，而且必須使用唯一識別碼來區分解碼處理常式。</span><span class="sxs-lookup"><span data-stu-id="77b0d-124">As with **SEQUENCE**, the fields of a **SET** construct can be marked with **OPTIONAL** or **DEFAULT**, and unique identifiers must be used to disambiguate the decoding process.</span></span> <span data-ttu-id="77b0d-125">**Set** 和 **set** 之間的差異在於，一 **組** 結構的元素必須屬於相同的型別。</span><span class="sxs-lookup"><span data-stu-id="77b0d-125">The difference between **SET** and **SET OF** is that the elements of a **SET OF** construct must be of the same type.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a><span data-ttu-id="77b0d-126">選擇</span><span class="sxs-lookup"><span data-stu-id="77b0d-126">CHOICE</span></span>

<span data-ttu-id="77b0d-127">編碼標記：不適用</span><span class="sxs-lookup"><span data-stu-id="77b0d-127">Encoding tag: not applicable</span></span>

<span data-ttu-id="77b0d-128">定義替代專案之間的選擇。</span><span class="sxs-lookup"><span data-stu-id="77b0d-128">Defines a choice between alternatives.</span></span> <span data-ttu-id="77b0d-129">每個替代項都必須以括弧括住的整數來唯一識別，以避免在解碼時有混淆。</span><span class="sxs-lookup"><span data-stu-id="77b0d-129">Each alternative must be uniquely identified by a bracketed integer to avoid ambiguity when decoding.</span></span> <span data-ttu-id="77b0d-130">編碼之後， **選擇** 結構將會有所選替代的編碼標記值。</span><span class="sxs-lookup"><span data-stu-id="77b0d-130">When encoded, the **CHOICE** construct will have the encoding tag value of the chosen alternative.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="77b0d-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="77b0d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77b0d-132">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="77b0d-132">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="77b0d-133">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="77b0d-133">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="77b0d-134">可辨別編碼規則</span><span class="sxs-lookup"><span data-stu-id="77b0d-134">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
