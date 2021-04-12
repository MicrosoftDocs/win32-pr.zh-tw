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
# <a name="string-types"></a><span data-ttu-id="080d0-103">字串類型</span><span class="sxs-lookup"><span data-stu-id="080d0-103">String Types</span></span>

<span data-ttu-id="080d0-104">公開金鑰基礎結構 (PKI) 最常見的用法之一，就是建立一個 x.500 辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="080d0-104">One of the most common uses of strings in a public key infrastructure (PKI) is to create an X.500 Distinguished Name.</span></span> <span data-ttu-id="080d0-105">例如，藉由結合一系列的相對辨別名稱來建立憑證要求的主體名稱，如下列語法範例所示。</span><span class="sxs-lookup"><span data-stu-id="080d0-105">For example, the subject name of a certificate request is created by combining a sequence of relative distinguished names as shown in the following syntax example.</span></span>

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

<span data-ttu-id="080d0-106">憑證註冊 API 支援下列 ASN. 1 字串類型。</span><span class="sxs-lookup"><span data-stu-id="080d0-106">The Certificate Enrollment API supports the following ASN.1 string types.</span></span>

## <a name="bmpstring"></a><span data-ttu-id="080d0-107">BMPString</span><span class="sxs-lookup"><span data-stu-id="080d0-107">BMPString</span></span>

<span data-ttu-id="080d0-108">編碼標記：0x1E</span><span class="sxs-lookup"><span data-stu-id="080d0-108">Encoding tag: 0x1E</span></span>

<span data-ttu-id="080d0-109">Certreq.exe 名稱： UNICODE \_ 字串</span><span class="sxs-lookup"><span data-stu-id="080d0-109">Certreq.exe name: UNICODE\_STRING</span></span>

<span data-ttu-id="080d0-110"> (BMP) 的基本多語系平面是字元編碼，其中包含通用字元集 (UCS) 的第一個平面。</span><span class="sxs-lookup"><span data-stu-id="080d0-110">The Basic Multilingual Plane (BMP) is a character encoding that encompasses the first plane of the Universal Character Set (UCS).</span></span> <span data-ttu-id="080d0-111">有17個平面編號為0到16。</span><span class="sxs-lookup"><span data-stu-id="080d0-111">There are seventeen planes numbered 0 to 16.</span></span> <span data-ttu-id="080d0-112">BMP 佔據平面0，並包括從0x0000 到0xFFFF 的65536程式碼點。</span><span class="sxs-lookup"><span data-stu-id="080d0-112">BMP occupies plane 0 and includes 65,536 code points from 0x0000 to 0xFFFF.</span></span> <span data-ttu-id="080d0-113">這是 Unicode 字元對應的一部分，其中大部分的字元指派都有到目前為止。</span><span class="sxs-lookup"><span data-stu-id="080d0-113">This is the section of the Unicode character map where most of the characters assignments have so far been made.</span></span> <span data-ttu-id="080d0-114">其中包括拉丁、中東、亞洲、非洲和其他語言。</span><span class="sxs-lookup"><span data-stu-id="080d0-114">It includes Latin, Middle Eastern, Asian, African, and other languages.</span></span>

## <a name="ia5string"></a><span data-ttu-id="080d0-115">IA5String</span><span class="sxs-lookup"><span data-stu-id="080d0-115">IA5String</span></span>

<span data-ttu-id="080d0-116">編碼標記：0x16</span><span class="sxs-lookup"><span data-stu-id="080d0-116">Encoding tag: 0x16</span></span>

<span data-ttu-id="080d0-117">Certreq.exe 名稱： IA5 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="080d0-117">Certreq.exe name: IA5\_STRING</span></span>

<span data-ttu-id="080d0-118">國際字母數位 5 (IA5) 通常等同于 ASCII 字母，但不同的版本可以包含地區語言專屬的重音或其他字元。</span><span class="sxs-lookup"><span data-stu-id="080d0-118">The International Alphabet number 5 (IA5) is generally equivalent to the ASCII alphabet, but different versions can include accents or other characters specific to a regional language.</span></span> <span data-ttu-id="080d0-119">下列範例顯示 **AlternativeNames** 憑證延伸的 asn.1 定義中使用的 **IA5String** 類型。</span><span class="sxs-lookup"><span data-stu-id="080d0-119">The following example shows the **IA5String** type used in the ASN.1 definition of the **AlternativeNames** certificate extension.</span></span>

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

## <a name="printablestring"></a><span data-ttu-id="080d0-120">PrintableString</span><span class="sxs-lookup"><span data-stu-id="080d0-120">PrintableString</span></span>

<span data-ttu-id="080d0-121">編碼標記：0x13</span><span class="sxs-lookup"><span data-stu-id="080d0-121">Encoding tag: 0x13</span></span>

<span data-ttu-id="080d0-122">Certreq.exe 名稱：可列印的 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="080d0-122">Certreq.exe name: PRINTABLE\_STRING</span></span>

<span data-ttu-id="080d0-123">**PrintableString** 資料類型原本是用來代表可供大型主機輸入終端機使用的有限字元集，但仍常使用。</span><span class="sxs-lookup"><span data-stu-id="080d0-123">The **PrintableString** data type was originally intended to represent the limited character sets available to mainframe input terminals, but it is still commonly used.</span></span> <span data-ttu-id="080d0-124">它包含下列字元：</span><span class="sxs-lookup"><span data-stu-id="080d0-124">It contains the following characters:</span></span>

-   <span data-ttu-id="080d0-125">A-Z</span><span class="sxs-lookup"><span data-stu-id="080d0-125">A-Z</span></span>
-   <span data-ttu-id="080d0-126">a-z</span><span class="sxs-lookup"><span data-stu-id="080d0-126">a-z</span></span>
-   <span data-ttu-id="080d0-127">0-9</span><span class="sxs-lookup"><span data-stu-id="080d0-127">0-9</span></span>
-   <span data-ttu-id="080d0-128">' ( ) + , - .</span><span class="sxs-lookup"><span data-stu-id="080d0-128">' ( ) + , - .</span></span> <span data-ttu-id="080d0-129">/ : = ?</span><span class="sxs-lookup"><span data-stu-id="080d0-129">/ : = ?</span></span> <span data-ttu-id="080d0-130">\[space\]</span><span class="sxs-lookup"><span data-stu-id="080d0-130">\[space\]</span></span>

## <a name="teletexstring"></a><span data-ttu-id="080d0-131">TeletexString</span><span class="sxs-lookup"><span data-stu-id="080d0-131">TeletexString</span></span>

<span data-ttu-id="080d0-132">編碼標記：0x14</span><span class="sxs-lookup"><span data-stu-id="080d0-132">Encoding tag: 0x14</span></span>

<span data-ttu-id="080d0-133">**TeletexString** 和相關的 **T61String** 資料類型會編碼在8個位 (或16位用於複合字元) 。</span><span class="sxs-lookup"><span data-stu-id="080d0-133">The **TeletexString** and the related **T61String** data types are encoded on 8 bits (or 16 bits for composite characters).</span></span> <span data-ttu-id="080d0-134">它們都有0x14 的標記編號。</span><span class="sxs-lookup"><span data-stu-id="080d0-134">They both have a tag number of 0x14.</span></span> <span data-ttu-id="080d0-135">這些都不是廣泛使用。</span><span class="sxs-lookup"><span data-stu-id="080d0-135">They are not extensively used.</span></span>

## <a name="utf8string"></a><span data-ttu-id="080d0-136">UTF8String</span><span class="sxs-lookup"><span data-stu-id="080d0-136">UTF8String</span></span>

<span data-ttu-id="080d0-137">編碼標記：0x0C</span><span class="sxs-lookup"><span data-stu-id="080d0-137">Encoding tag: 0x0C</span></span>

<span data-ttu-id="080d0-138">Certreq.exe 名稱： UTF8 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="080d0-138">Certreq.exe name: UTF8\_STRING</span></span>

<span data-ttu-id="080d0-139">8位的 UCS/Unicode 轉換格式 (UTF-8) 是可將任何通用字元表示為 Unicode 字元的可變長度字元編碼，同時允許初始程式碼點與 ASCII 保持一致。</span><span class="sxs-lookup"><span data-stu-id="080d0-139">The 8-bit UCS/Unicode Transformation Format (UTF-8) is a variable-length character encoding that can represent any universal character as a Unicode character while allowing initial code points to remain consistent with ASCII.</span></span> <span data-ttu-id="080d0-140">UTF-8 使用一到四個位元組。</span><span class="sxs-lookup"><span data-stu-id="080d0-140">UTF-8 uses one to four bytes.</span></span> <span data-ttu-id="080d0-141">標記編號為0x0C。</span><span class="sxs-lookup"><span data-stu-id="080d0-141">The tag number is 0x0C.</span></span>

## <a name="related-topics"></a><span data-ttu-id="080d0-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="080d0-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="080d0-143">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="080d0-143">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="080d0-144">可辨別編碼規則</span><span class="sxs-lookup"><span data-stu-id="080d0-144">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="080d0-145">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="080d0-145">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



