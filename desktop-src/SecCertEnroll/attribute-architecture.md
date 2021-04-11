---
description: 用來將屬性新增至憑證要求。
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: 屬性架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d83171985c062fd2d8d4ae968c2ef4d36a29ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318956"
---
# <a name="attribute-architecture"></a><span data-ttu-id="409ed-103">屬性架構</span><span class="sxs-lookup"><span data-stu-id="409ed-103">Attribute Architecture</span></span>

<span data-ttu-id="409ed-104">下列介面是用來將屬性新增至憑證要求：</span><span class="sxs-lookup"><span data-stu-id="409ed-104">The following interfaces are used to add attributes to a certificate request:</span></span>

-   [<span data-ttu-id="409ed-105">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="409ed-105">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [<span data-ttu-id="409ed-106">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="409ed-106">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [<span data-ttu-id="409ed-107">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="409ed-107">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [<span data-ttu-id="409ed-108">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="409ed-108">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

<span data-ttu-id="409ed-109">架構如下所示，在 PKCS \# 10 認證要求語法的 asn.1 模組中定義。</span><span class="sxs-lookup"><span data-stu-id="409ed-109">The architecture follows that defined in the ASN.1 module of the PKCS \#10 certification request syntax.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="409ed-110">[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)集合會對應到 [**屬性**] 欄位，而集合中的每個 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)物件都會對應到一個 asn.1 **屬性** 結構。</span><span class="sxs-lookup"><span data-stu-id="409ed-110">The [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection corresponds to the **attributes** field, and each [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object in the collection corresponds to an ASN.1 **Attribute** structure.</span></span>

<span data-ttu-id="409ed-111">每個 **屬性** 都包含 (oid) 的物件識別碼，以及與 oid 相關聯的零或多個值。</span><span class="sxs-lookup"><span data-stu-id="409ed-111">Each **Attribute** consists of an object identifier (OID) and zero or more values associated with the OID.</span></span> <span data-ttu-id="409ed-112">單一 OID/值組會以 [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="409ed-112">A single OID-value pair is represented by an [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) interface.</span></span> <span data-ttu-id="409ed-113">您可以使用 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合來初始化 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件，但集合中的每個屬性都必須與相同的 OID 相關聯。</span><span class="sxs-lookup"><span data-stu-id="409ed-113">You can use an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object, but each attribute in the collection must be associated with the same OID.</span></span> <span data-ttu-id="409ed-114">一般來說，屬性只有一個值。</span><span class="sxs-lookup"><span data-stu-id="409ed-114">Typically, an attribute has only one value.</span></span>

<span data-ttu-id="409ed-115">您可以使用下列任何衍生自 [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)的介面，建立單一 OID/值屬性組：</span><span class="sxs-lookup"><span data-stu-id="409ed-115">You can use any of the following interfaces, which derive from [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute), to create a single OID/value attribute pair:</span></span>

-   [<span data-ttu-id="409ed-116">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="409ed-116">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [<span data-ttu-id="409ed-117">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="409ed-117">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [<span data-ttu-id="409ed-118">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="409ed-118">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [<span data-ttu-id="409ed-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="409ed-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [<span data-ttu-id="409ed-120">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="409ed-120">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [<span data-ttu-id="409ed-121">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="409ed-121">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [<span data-ttu-id="409ed-122">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="409ed-122">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

<span data-ttu-id="409ed-123">例如，下列程式說明如何建立 **ClientId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="409ed-123">For example, the following procedure shows how to create a **ClientId** attribute.</span></span>

<span data-ttu-id="409ed-124">**若要建立 **ClientId** 屬性**</span><span class="sxs-lookup"><span data-stu-id="409ed-124">**To create a **ClientId** attribute**</span></span>

1.  <span data-ttu-id="409ed-125">從 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)或 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)物件取出 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)物件。</span><span class="sxs-lookup"><span data-stu-id="409ed-125">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) or [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
2.  <span data-ttu-id="409ed-126">建立並初始化 [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) 物件。</span><span class="sxs-lookup"><span data-stu-id="409ed-126">Create and initialize an [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) object.</span></span>
3.  <span data-ttu-id="409ed-127">建立 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合，並新增 [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) 物件。</span><span class="sxs-lookup"><span data-stu-id="409ed-127">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) object.</span></span>
4.  <span data-ttu-id="409ed-128">使用 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合來初始化 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件。</span><span class="sxs-lookup"><span data-stu-id="409ed-128">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
5.  <span data-ttu-id="409ed-129">將 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件新增至步驟1中所取出的集合。</span><span class="sxs-lookup"><span data-stu-id="409ed-129">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the collection retrieved in step 1.</span></span>

<span data-ttu-id="409ed-130">下列範例顯示 **ClientId** 屬性的 asn.1 輸出。</span><span class="sxs-lookup"><span data-stu-id="409ed-130">The following example shows the ASN.1 output of the **ClientId** attribute.</span></span> <span data-ttu-id="409ed-131">屬性包含產生要求之電腦的 DNS 名稱 (test3d.jdomcsc.nttest.microsoft.com) 、使用者的 SAM 名稱 (JDOMCSC \\ administrator) ，以及產生要求 (certreq) 的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="409ed-131">The attribute contains the DNS name of the computer on which the request was generated (test3d.jdomcsc.nttest.microsoft.com), the SAM name of the user (JDOMCSC\\administrator), and the name of the application that generated the request (certreq).</span></span>

``` syntax
0136: 30 57; SEQUENCE (57 Bytes)
0138: |  06 09                            ; OBJECT_ID (9 Bytes)
013a: |  |  2b 06 01 04 01 82 37 15  14
      |  |     ; 1.3.6.1.4.1.311.21.20 Client Information
0143: |  |  31 4a                         ; SET (4a Bytes)
0145: |  |     30 48                      ; SEQUENCE (48 Bytes)
0147: |  |        02 01                   ; INTEGER (1 Bytes)
0149: |  |        |  09
014a: |  |        0c 23                   ; UTF8_STRING (23 Bytes)
014c: |  |        |  74 65 73 74 33 64 2e 6a  64 6f 6d 63 73 63 2e 6e 
015c: |  |        |  74 74 65 73 74 2e 6d 69  63 72 6f 73 6f 66 74 2e 
016c: |  |        |  63 6f 6d                                         
      |  |        |     ; "test3d.jdomcsc.nttest.microsoft.com"
016f: |  |        0c 15                   ; UTF8_STRING (15 Bytes)
0171: |  |        |  4a 44 4f 4d 43 53 43 5c  61 64 6d 69 6e 69 73 74 
0181: |  |        |  72 61 74 6f 72                                   
      |  |        |     ; "JDOMCSC\administrator"
0186: |  |        0c 07                   ; UTF8_STRING (7 Bytes)
0188: |  |           63 65 72 74 72 65 71                             
      |  |              ; "certreq"
```

## <a name="related-topics"></a><span data-ttu-id="409ed-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="409ed-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="409ed-133">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="409ed-133">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[<span data-ttu-id="409ed-134">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="409ed-134">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[<span data-ttu-id="409ed-135">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="409ed-135">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[<span data-ttu-id="409ed-136">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="409ed-136">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



