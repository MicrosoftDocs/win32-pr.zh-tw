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
# <a name="basic-fields"></a><span data-ttu-id="bf9da-105">基本欄位</span><span class="sxs-lookup"><span data-stu-id="bf9da-105">Basic Fields</span></span>

<span data-ttu-id="bf9da-106">X.509 第1版憑證包含下欄欄位。</span><span class="sxs-lookup"><span data-stu-id="bf9da-106">An X.509 version 1 certificate contains the following fields.</span></span> <span data-ttu-id="bf9da-107">第 [2 版欄位](about-version-2-fields.md)中會討論第2版欄位。</span><span class="sxs-lookup"><span data-stu-id="bf9da-107">Version 2 fields are discussed in [Version 2 Fields](about-version-2-fields.md).</span></span> <span data-ttu-id="bf9da-108">第3版的 [延伸](about-version-3-extensions.md)模組會討論第3版欄位。</span><span class="sxs-lookup"><span data-stu-id="bf9da-108">Version 3 fields are discussed in [Version 3 Extensions](about-version-3-extensions.md).</span></span>

## <a name="version"></a><span data-ttu-id="bf9da-109">版本</span><span class="sxs-lookup"><span data-stu-id="bf9da-109">Version</span></span>

<span data-ttu-id="bf9da-110">指定編碼憑證的版本編號。</span><span class="sxs-lookup"><span data-stu-id="bf9da-110">Specifies the version number of the encoded certificate.</span></span> <span data-ttu-id="bf9da-111">目前，此欄位的可能值為0、1或2，但未來可能會擴大。</span><span class="sxs-lookup"><span data-stu-id="bf9da-111">Currently, the possible values of this field are 0, 1, or 2, but this may be expanded in the future.</span></span>

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a><span data-ttu-id="bf9da-112">序號</span><span class="sxs-lookup"><span data-stu-id="bf9da-112">Serial Number</span></span>

<span data-ttu-id="bf9da-113">包含一個由憑證授權單位 (CA) 指派給憑證的唯一正整數。</span><span class="sxs-lookup"><span data-stu-id="bf9da-113">Contains a positive, unique integer assigned by the certification authority (CA) to the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a><span data-ttu-id="bf9da-114">簽章演算法</span><span class="sxs-lookup"><span data-stu-id="bf9da-114">Signature Algorithm</span></span>

<span data-ttu-id="bf9da-115">包含 (OID) 的 [*物件識別碼*](/windows/desktop/SecGloss/o-gly) ，可指定 CA 用來簽署憑證的演算法。</span><span class="sxs-lookup"><span data-stu-id="bf9da-115">Contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) that specifies the algorithm used by the CA to sign the certificate.</span></span> <span data-ttu-id="bf9da-116">例如，1.2.840.113549.1.1.5 指定 SHA-1 雜湊演算法結合來自 RSA Laboratories 制定的 RSA 加密演算法。</span><span class="sxs-lookup"><span data-stu-id="bf9da-116">For example, 1.2.840.113549.1.1.5 specifies a SHA-1 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.</span></span>

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

## <a name="issuer"></a><span data-ttu-id="bf9da-117">Issuer</span><span class="sxs-lookup"><span data-stu-id="bf9da-117">Issuer</span></span>

<span data-ttu-id="bf9da-118">包含建立和簽署憑證之 CA (DN) 的 [*x.500 辨別名稱。*](/windows/desktop/SecGloss/x-gly)</span><span class="sxs-lookup"><span data-stu-id="bf9da-118">Contains the [*X.500*](/windows/desktop/SecGloss/x-gly) distinguished name (DN) of the CA that created and signed the certificate.</span></span>

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

## <a name="validity"></a><span data-ttu-id="bf9da-119">有效期</span><span class="sxs-lookup"><span data-stu-id="bf9da-119">Validity</span></span>

<span data-ttu-id="bf9da-120">指定憑證有效的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="bf9da-120">Specifies the time interval during which the certificate is valid.</span></span> <span data-ttu-id="bf9da-121">2049結尾的日期會使用國際標準時間 (格林尼治平均時間) 格式 (*yymmddhhmmssz*) 。</span><span class="sxs-lookup"><span data-stu-id="bf9da-121">Dates through the end of 2049 use the Coordinated Universal Time (Greenwich Mean Time) format (*yymmddhhmmssz*).</span></span> <span data-ttu-id="bf9da-122">從2050年1月1日開始的日期會使用一般化時間格式 (*yyyymmddhhmmssz*) 。</span><span class="sxs-lookup"><span data-stu-id="bf9da-122">Dates beginning with January 1st, 2050 use the generalized time format (*yyyymmddhhmmssz*).</span></span>

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

## <a name="subject"></a><span data-ttu-id="bf9da-123">主體</span><span class="sxs-lookup"><span data-stu-id="bf9da-123">Subject</span></span>

<span data-ttu-id="bf9da-124">包含實體的 X.500 辨別名稱，該實體與憑證中包含的公開金鑰相關聯。</span><span class="sxs-lookup"><span data-stu-id="bf9da-124">Contains an X.500 distinguished name of the entity associated with the public key contained in the certificate.</span></span>

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

## <a name="public-key"></a><span data-ttu-id="bf9da-125">公開金鑰</span><span class="sxs-lookup"><span data-stu-id="bf9da-125">Public Key</span></span>

<span data-ttu-id="bf9da-126">包含公開金鑰和相關聯的演算法資訊。</span><span class="sxs-lookup"><span data-stu-id="bf9da-126">Contains the public key and associated algorithm information.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bf9da-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf9da-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf9da-128">第2版欄位</span><span class="sxs-lookup"><span data-stu-id="bf9da-128">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="bf9da-129">第3版擴充功能</span><span class="sxs-lookup"><span data-stu-id="bf9da-129">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="bf9da-130">X.509 公開金鑰憑證</span><span class="sxs-lookup"><span data-stu-id="bf9da-130">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
