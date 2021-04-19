---
description: 憑證註冊 API 支援下列基本的 ASN. 1 類型。
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: 基本類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f3ae64c058fce3466ca06e7bf205c4c4165fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975088"
---
# <a name="basic-types"></a><span data-ttu-id="9a376-103">基本類型</span><span class="sxs-lookup"><span data-stu-id="9a376-103">Basic Types</span></span>

<span data-ttu-id="9a376-104">憑證註冊 API 支援下列基本的 ASN. 1 類型。</span><span class="sxs-lookup"><span data-stu-id="9a376-104">The Certificate Enrollment API supports the following basic ASN.1 types.</span></span>

## <a name="bit-string"></a><span data-ttu-id="9a376-105">位字串</span><span class="sxs-lookup"><span data-stu-id="9a376-105">BIT STRING</span></span>

<span data-ttu-id="9a376-106">編碼標記：0x03</span><span class="sxs-lookup"><span data-stu-id="9a376-106">Encoding tag: 0x03</span></span>

<span data-ttu-id="9a376-107">Certreq.exe 名稱：位 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="9a376-107">Certreq.exe name: BIT\_STRING</span></span>

<span data-ttu-id="9a376-108">位或二進位字串是任意長的位陣列。</span><span class="sxs-lookup"><span data-stu-id="9a376-108">A bit or binary string is an arbitrarily long array of bits.</span></span> <span data-ttu-id="9a376-109">您可以使用以括弧括住的整數和指派的名稱來識別特定位，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="9a376-109">Specific bits can be identified by parenthesized integers and assigned names as in the following example.</span></span>

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

<span data-ttu-id="9a376-110">憑證金鑰和簽章通常會以位字串表示。</span><span class="sxs-lookup"><span data-stu-id="9a376-110">Certificate keys and signatures are often represented as bit strings.</span></span>

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

## <a name="boolean"></a><span data-ttu-id="9a376-111">BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9a376-111">BOOLEAN</span></span>

<span data-ttu-id="9a376-112">編碼標記：0x01</span><span class="sxs-lookup"><span data-stu-id="9a376-112">Encoding tag: 0x01</span></span>

<span data-ttu-id="9a376-113">Certreq.exe 名稱：布林值</span><span class="sxs-lookup"><span data-stu-id="9a376-113">Certreq.exe name: BOOLEAN</span></span>

<span data-ttu-id="9a376-114">布林值類型可以包含下列兩個值的其中一個： **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9a376-114">A Boolean type can contain one of two values, **TRUE** or **FALSE**.</span></span> <span data-ttu-id="9a376-115">下列範例顯示基本條件約束憑證延伸的 asn.1 結構。</span><span class="sxs-lookup"><span data-stu-id="9a376-115">The following example shows the ASN.1 structure for a Basic Constraints certificate extension.</span></span> <span data-ttu-id="9a376-116">**Ca** 欄位會指定憑證主體是否為憑證授權單位單位 (cA) 。</span><span class="sxs-lookup"><span data-stu-id="9a376-116">The **cA** field specifies whether a certificate subject is a certification authority (CA).</span></span> <span data-ttu-id="9a376-117">預設重要性為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9a376-117">The default criticality is **FALSE**.</span></span>

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

## <a name="integer"></a><span data-ttu-id="9a376-118">INTEGER</span><span class="sxs-lookup"><span data-stu-id="9a376-118">INTEGER</span></span>

<span data-ttu-id="9a376-119">編碼標記：0x02</span><span class="sxs-lookup"><span data-stu-id="9a376-119">Encoding tag: 0x02</span></span>

<span data-ttu-id="9a376-120">Certreq.exe 名稱：整數</span><span class="sxs-lookup"><span data-stu-id="9a376-120">Certreq.exe name: INTEGER</span></span>

<span data-ttu-id="9a376-121">整數通常可以是任何正數或負整數值。</span><span class="sxs-lookup"><span data-stu-id="9a376-121">An integer can typically be any positive or negative integral value.</span></span> <span data-ttu-id="9a376-122">下列範例顯示 RSA 公開金鑰的 asn.1 結構。</span><span class="sxs-lookup"><span data-stu-id="9a376-122">The following example shows the ASN.1 structure for an RSA public key.</span></span> <span data-ttu-id="9a376-123">請注意， **publicExponent** 欄位限制為小於4294967296的正整數。</span><span class="sxs-lookup"><span data-stu-id="9a376-123">Note that the **publicExponent** field is restricted to a positive integer less than 4,294,967,296.</span></span>

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

## <a name="null"></a><span data-ttu-id="9a376-124">NULL</span><span class="sxs-lookup"><span data-stu-id="9a376-124">NULL</span></span>

<span data-ttu-id="9a376-125">編碼標記：0x05</span><span class="sxs-lookup"><span data-stu-id="9a376-125">Encoding tag: 0x05</span></span>

<span data-ttu-id="9a376-126">Certreq.exe 名稱： **Null**</span><span class="sxs-lookup"><span data-stu-id="9a376-126">Certreq.exe name: **NULL**</span></span>

<span data-ttu-id="9a376-127">**Null** 型別包含單一位元組0x00。</span><span class="sxs-lookup"><span data-stu-id="9a376-127">A **NULL** type contains a single byte 0x00.</span></span> <span data-ttu-id="9a376-128">憑證要求必須指出空白值的任何地方都可以使用它。</span><span class="sxs-lookup"><span data-stu-id="9a376-128">It can be used anywhere that the certificate request must indicate an empty value.</span></span> <span data-ttu-id="9a376-129">例如， **AlgorithmIdentifier** 是一個序列，其中包含 (OID) 和選擇性參數的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a376-129">For example, an **AlgorithmIdentifier** is a sequence that contains an object identifier (OID) and optional parameters.</span></span>

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

<span data-ttu-id="9a376-130">如果在結構編碼時沒有任何參數，則會使用 **Null** 來表示空的值。</span><span class="sxs-lookup"><span data-stu-id="9a376-130">If there are no parameters when the structure is encoded, **NULL** is used to indicate an empty value.</span></span>

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a><span data-ttu-id="9a376-131">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="9a376-131">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="9a376-132">編碼標記：0x06</span><span class="sxs-lookup"><span data-stu-id="9a376-132">Encoding tag: 0x06</span></span>

<span data-ttu-id="9a376-133">Certreq.exe 名稱：物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="9a376-133">Certreq.exe name: OBJECT\_ID</span></span>

<span data-ttu-id="9a376-134">憑證註冊 API 使用 (Oid) 的物件識別碼，做為演算法識別碼、屬性和其他 PKI 專案的通用指標類型。</span><span class="sxs-lookup"><span data-stu-id="9a376-134">The Certificate Enrollment API uses object identifiers (OIDs) as a type of universal pointer to algorithm identifiers, attributes, and other PKI elements.</span></span> <span data-ttu-id="9a376-135">Oid 通常是以點分隔的十進位字串來呈現，例如 "2.16.840.1.101.3.4.1.42"。</span><span class="sxs-lookup"><span data-stu-id="9a376-135">OIDs are typically presented in a dotted decimal string such as "2.16.840.1.101.3.4.1.42".</span></span> <span data-ttu-id="9a376-136">字串中的個別元素（以句號分隔）代表在註冊授權單位樹狀結構中，用來唯一識別物件和所註冊之物件的弧形和離職。</span><span class="sxs-lookup"><span data-stu-id="9a376-136">The individual elements in the string, separated by periods, represent the arcs and leaves in a registration authority tree that uniquely identifies the object and the organization that registered it.</span></span> <span data-ttu-id="9a376-137">例如，先前的 OID 可以擴充為聯合-iso-itu-t (2) country (16) us (840) 組織 (1) gov (101) csor (3) nistAlgorithms (4) aesAlgs (1) ，並附加42，以唯一識別256位 AES 加密區塊鏈 (CBC) 模式演算法。</span><span class="sxs-lookup"><span data-stu-id="9a376-137">For example, the preceding OID can be expanded to joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) with .42 appended to uniquely identify the 256-bit AES cipher block chaining (CBC) mode algorithm.</span></span>

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

## <a name="octet-string"></a><span data-ttu-id="9a376-138">八位字串</span><span class="sxs-lookup"><span data-stu-id="9a376-138">OCTET STRING</span></span>

<span data-ttu-id="9a376-139">編碼標記：0x04</span><span class="sxs-lookup"><span data-stu-id="9a376-139">Encoding tag: 0x04</span></span>

<span data-ttu-id="9a376-140">Certreq.exe 名稱：八位 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="9a376-140">Certreq.exe name: OCTET\_STRING</span></span>

<span data-ttu-id="9a376-141">八位字串是任意大的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="9a376-141">An octet string is an arbitrarily large byte array.</span></span> <span data-ttu-id="9a376-142">但是不同于 **位字串** 類型，字串中的特定位和位元組不能被指派名稱。</span><span class="sxs-lookup"><span data-stu-id="9a376-142">Unlike the **BIT STRING** type, however, specific bits and bytes in the string cannot be assigned names.</span></span> <span data-ttu-id="9a376-143">八位字組是指一種與平臺無關的方式來參考記憶體單字。</span><span class="sxs-lookup"><span data-stu-id="9a376-143">The word octet is meant to be a platform independent way to refer to a memory word.</span></span> <span data-ttu-id="9a376-144">在憑證註冊 API 的內容中，八進位和位元組是可互換的。</span><span class="sxs-lookup"><span data-stu-id="9a376-144">Within the context of the Certificate Enrollment API, octet and byte are interchangeable.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9a376-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a376-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a376-146">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="9a376-146">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="9a376-147">可辨別編碼規則</span><span class="sxs-lookup"><span data-stu-id="9a376-147">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="9a376-148">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="9a376-148">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



