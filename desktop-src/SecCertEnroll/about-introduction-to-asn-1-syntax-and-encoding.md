---
description: 憑證註冊 API 使用抽象語法標記法 (一)  (asn.1) 來定義、編碼和解碼在用戶端電腦和憑證授權單位單位之間傳輸的憑證要求和憑證。
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: ASN. 1 語法和編碼簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849247"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a><span data-ttu-id="0f834-103">ASN. 1 語法和編碼簡介</span><span class="sxs-lookup"><span data-stu-id="0f834-103">Introduction to ASN.1 Syntax and Encoding</span></span>

<span data-ttu-id="0f834-104">憑證註冊 API 使用抽象語法標記法 (一)  (asn.1) 來定義、編碼和解碼在用戶端電腦和憑證授權單位單位之間傳輸的憑證要求和憑證。</span><span class="sxs-lookup"><span data-stu-id="0f834-104">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to define, encode, and decode the certificate requests and certificates that it transfers between client computers and certification authorities.</span></span> <span data-ttu-id="0f834-105">Asn.1 可以概念分為一組語法規則和一組編碼規則，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0f834-105">ASN.1 can be conceptually divided into a set of syntax rules and a set of encoding rules as shown by the following examples.</span></span>

## <a name="asn1-syntax-example"></a><span data-ttu-id="0f834-106">ASN. 1 語法範例</span><span class="sxs-lookup"><span data-stu-id="0f834-106">ASN.1 Syntax Example</span></span>

<span data-ttu-id="0f834-107">憑證要求包含了提出要求之實體的名稱，或提出要求的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="0f834-107">A certificate request contains, among other things, the name of the entity that is making the request or for which the request is being made.</span></span> <span data-ttu-id="0f834-108">名稱是 X. 500 相對辨別名稱 (RDNs) 的序列。</span><span class="sxs-lookup"><span data-stu-id="0f834-108">The name is a sequence of X.500 relative distinguished names (RDNs).</span></span> <span data-ttu-id="0f834-109">順序中的每個 RDN 都包含物件識別碼 (OID) 和值。</span><span class="sxs-lookup"><span data-stu-id="0f834-109">Each RDN in the sequence consists of an object identifier (OID) and a value.</span></span> <span data-ttu-id="0f834-110">下列範例顯示的是主體名稱的 asn.1 語法。</span><span class="sxs-lookup"><span data-stu-id="0f834-110">The ASN.1 syntax for a subject name is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a><span data-ttu-id="0f834-111">ASN. 1 編碼範例</span><span class="sxs-lookup"><span data-stu-id="0f834-111">ASN.1 Encoding Example</span></span>

<span data-ttu-id="0f834-112">憑證註冊 API 會使用 [*可辨別編碼規則*](/windows/desktop/SecGloss/d-gly) (DER) 來編碼先前的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="0f834-112">The Certificate Enrollment API uses [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) to encode the preceding subject name.</span></span> <span data-ttu-id="0f834-113">DER 要求名稱中的每個專案都是以每個的 TLV 表示，其中 T 包含 asn.1 類型的標記編號、L 包含長度，而 V 則包含相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="0f834-113">DER requires that each item in the name be represented by a TLV triplet where T contains the tag number of the ASN.1 type, L contains the length, and V contains the associated value.</span></span> <span data-ttu-id="0f834-114">下列範例顯示如何編碼主體名稱 TestCN. TestOrg。</span><span class="sxs-lookup"><span data-stu-id="0f834-114">The following example shows how the subject name TestCN.TestOrg is encoded.</span></span>

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

<span data-ttu-id="0f834-115">請注意下列幾點：</span><span class="sxs-lookup"><span data-stu-id="0f834-115">Note the following points:</span></span>

-   <span data-ttu-id="0f834-116">第1行：</span><span class="sxs-lookup"><span data-stu-id="0f834-116">Line 1:</span></span><dl> <span data-ttu-id="0f834-117">名稱是一系列的相對辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="0f834-117">The name is a sequence of relative distinguished names.</span></span>  
    <span data-ttu-id="0f834-118">**序列** 類型的標記編號為0x30<。</span><span class="sxs-lookup"><span data-stu-id="0f834-118">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="0f834-119">TestCN 的主體名稱 TestOrg 需要 35 (0x23) 個位元組。</span><span class="sxs-lookup"><span data-stu-id="0f834-119">The subject name of TestCN.TestOrg requires 35 (0x23) bytes.</span></span>  
    </dl>
-   Line 2:<dl> <span data-ttu-id="0f834-120">一般名稱 TestCN 是一組 **AttributeTypeValue** 結構。</span><span class="sxs-lookup"><span data-stu-id="0f834-120">The Common Name, TestCN, is a single set of **AttributeTypeValue** structures.</span></span>  
    <span data-ttu-id="0f834-121">**集合** 的標記編號為0x31。</span><span class="sxs-lookup"><span data-stu-id="0f834-121">The tag number for a **SET** is 0x31.</span></span>  
    </dl><span data-ttu-id="0f834-122">
-   第3行：</span><span class="sxs-lookup"><span data-stu-id="0f834-122">
-   Line 3:</span></span><dl> <span data-ttu-id="0f834-123">**AttributeTypeValue** 結構是一種序列。</span><span class="sxs-lookup"><span data-stu-id="0f834-123">The **AttributeTypeValue** structure is a sequence.</span></span>  
    <span data-ttu-id="0f834-124">**序列** 類型的標記編號為0x30<。</span><span class="sxs-lookup"><span data-stu-id="0f834-124">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="0f834-125">結構需要 13 (0xD) 個位元組。</span><span class="sxs-lookup"><span data-stu-id="0f834-125">The structure requires 13 (0xD) bytes.</span></span>  
    </dl><span data-ttu-id="0f834-126">
-   第4到6行：</span><span class="sxs-lookup"><span data-stu-id="0f834-126">
-   Lines 4 to 6:</span></span><dl> <span data-ttu-id="0f834-127">一般名稱 (OID) 的物件識別碼是2.5.4.3。</span><span class="sxs-lookup"><span data-stu-id="0f834-127">The object identifier (OID) for the Common Name is 2.5.4.3.</span></span>  
    <span data-ttu-id="0f834-128">OID 是三個位元組的 **物件 \_ 識別碼** 型別。</span><span class="sxs-lookup"><span data-stu-id="0f834-128">The OID is a three byte **OBJECT\_ID** type.</span></span>  
    <span data-ttu-id="0f834-129">**物件 \_ 識別碼** 類型的標記編號為0x06。</span><span class="sxs-lookup"><span data-stu-id="0f834-129">The tag number for the **OBJECT\_ID** type is 0x06.</span></span>  
    </dl><span data-ttu-id="0f834-130">
-   第7到第9行：</span><span class="sxs-lookup"><span data-stu-id="0f834-130">
-   Lines 7 to 9:</span></span><dl> <span data-ttu-id="0f834-131">一般名稱 TestCN 是一個字串值。</span><span class="sxs-lookup"><span data-stu-id="0f834-131">The Common Name, TestCN, is a string value.</span></span>  
    <span data-ttu-id="0f834-132">字串是6個位元組的 **可列印 \_ 字串** 類型。</span><span class="sxs-lookup"><span data-stu-id="0f834-132">The string is a six byte **PRINTABLE\_STRING** type.</span></span>  
    <span data-ttu-id="0f834-133">**可列印 \_ 字串** 類型的標記編號為0x13。</span><span class="sxs-lookup"><span data-stu-id="0f834-133">The tag number for the **PRINTABLE\_STRING** type is 0x13.</span></span>  
    </dl>

## <a name="related-topics"></a><span data-ttu-id="0f834-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f834-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f834-135">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="0f834-135">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="0f834-136">憑證要求編碼</span><span class="sxs-lookup"><span data-stu-id="0f834-136">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="0f834-137">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="0f834-137">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="0f834-138">可辨別編碼規則</span><span class="sxs-lookup"><span data-stu-id="0f834-138">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
