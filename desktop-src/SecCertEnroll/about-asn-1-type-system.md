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
# <a name="asn1-type-system"></a><span data-ttu-id="d8e9a-103">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="d8e9a-103">ASN.1 Type System</span></span>

<span data-ttu-id="d8e9a-104">資料類型的概念是抽象語法標記法 (一)  (asn.1) 標準的基礎。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-104">The concept of a data type is fundamental to the Abstract Syntax Notation One (ASN.1) standard.</span></span> <span data-ttu-id="d8e9a-105">憑證要求結構的每個欄位都與型別相關聯。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-105">Every field of a certificate request structure is associated with a type.</span></span> <span data-ttu-id="d8e9a-106">例如，請考慮 \# 下列範例所示的 PKCS 10 ASN. 1 憑證語法。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-106">Consider, for example, the PKCS \#10 ASN.1 certificate syntax shown in the following example.</span></span>

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

<span data-ttu-id="d8e9a-107">高階要求結構 **CertificationRequestInfo** 是由其他類型的序列所組成的型別。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-107">The high-level request structure, **CertificationRequestInfo**, is a type that is made up from a sequence of other types.</span></span> <span data-ttu-id="d8e9a-108">當類型為或只包含基本類型、字串類型或 **任何** 類型時，就無法進一步細分。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-108">When a type is or contains only basic types, string types, or **ANY**, it cannot be broken down further.</span></span> <span data-ttu-id="d8e9a-109">例如，[ **版本** ] 欄位是一種 **CertificationRequestInfoVersion** 型別，也就是 **整數** 類型，這是一個不是從其他型別組成的基本 asn.1 型別。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-109">For example, the **version** field is a **CertificationRequestInfoVersion** type which is, in turn, an **INTEGER** type, a basic ASN.1 type that is not composed from other types.</span></span>

<span data-ttu-id="d8e9a-110">型別系統可讓要求的語法以視覺化方式呈現，以方便開發人員理解，並可讓要求一致地編碼，以便透過網路傳輸。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-110">A type system enables the syntax of a request to be presented visually in a manner readily understood by developers, and it enables the request to be consistently encoded for transmission across a network.</span></span> <span data-ttu-id="d8e9a-111">如需編碼的詳細資訊，請參閱 [可辨別編碼規則](distinguished-encoding-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-111">For more information about encoding, see [Distinguished Encoding Rules](distinguished-encoding-rules.md).</span></span> <span data-ttu-id="d8e9a-112">如需有關 asn.1 類型的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-112">For more information about ASN.1 types, see the following topics.</span></span>

[<span data-ttu-id="d8e9a-113">基本類型</span><span class="sxs-lookup"><span data-stu-id="d8e9a-113">Basic Types</span></span>](about-basic-types.md)

<span data-ttu-id="d8e9a-114">討論下列資料類型：</span><span class="sxs-lookup"><span data-stu-id="d8e9a-114">Discusses the following data types:</span></span>

* <span data-ttu-id="d8e9a-115">**位字串**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-115">**BIT STRING**</span></span>
* <span data-ttu-id="d8e9a-116">**布林**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-116">**BOOLEAN**</span></span>
* <span data-ttu-id="d8e9a-117">**INTEGER**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-117">**INTEGER**</span></span>
* <span data-ttu-id="d8e9a-118">**NULL**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-118">**NULL**</span></span>
* <span data-ttu-id="d8e9a-119">**物件識別碼**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-119">**OBJECT IDENTIFIER**</span></span>
* <span data-ttu-id="d8e9a-120">**八位字串**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-120">**OCTET STRING**</span></span>

[<span data-ttu-id="d8e9a-121">字串類型</span><span class="sxs-lookup"><span data-stu-id="d8e9a-121">String Types</span></span>](about-string-types.md)

<span data-ttu-id="d8e9a-122">討論下列字串類型：</span><span class="sxs-lookup"><span data-stu-id="d8e9a-122">Discusses the following string types:</span></span>

* <span data-ttu-id="d8e9a-123">**BMPString**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-123">**BMPString**</span></span>
* <span data-ttu-id="d8e9a-124">**IA5String**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-124">**IA5String**</span></span>
* <span data-ttu-id="d8e9a-125">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-125">**PrintableString**</span></span>
* <span data-ttu-id="d8e9a-126">**TeletexString**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-126">**TeletexString**</span></span>
* <span data-ttu-id="d8e9a-127">**UTF8String**</span><span class="sxs-lookup"><span data-stu-id="d8e9a-127">**UTF8String**</span></span>

[<span data-ttu-id="d8e9a-128">結構化類型</span><span class="sxs-lookup"><span data-stu-id="d8e9a-128">Constructed Types</span></span>](about-constructed-types.md)

<span data-ttu-id="d8e9a-129">討論 asn.1 資料類型，其中可以包含基本類型、字串類型或其他結構化類型。</span><span class="sxs-lookup"><span data-stu-id="d8e9a-129">Discusses ASN.1 data types that can contain basic types, string types, or other constructed types.</span></span>




 

## <a name="related-topics"></a><span data-ttu-id="d8e9a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8e9a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8e9a-131">憑證要求編碼</span><span class="sxs-lookup"><span data-stu-id="d8e9a-131">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="d8e9a-132">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="d8e9a-132">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="d8e9a-133">可辨別編碼規則</span><span class="sxs-lookup"><span data-stu-id="d8e9a-133">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="d8e9a-134">ASN. 1 語法和編碼簡介</span><span class="sxs-lookup"><span data-stu-id="d8e9a-134">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



