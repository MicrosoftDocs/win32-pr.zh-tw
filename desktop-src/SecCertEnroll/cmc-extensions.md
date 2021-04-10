---
description: 在 CMC 要求中新增延伸模組，方法是將它們新增至下列 asn.1 語法範例中所示的 TaggedAttributes 結構。 如需詳細資訊，請參閱屬性主題。
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: CMC 延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193901"
---
# <a name="cmc-extensions"></a><span data-ttu-id="c26ee-104">CMC 延伸模組</span><span class="sxs-lookup"><span data-stu-id="c26ee-104">CMC Extensions</span></span>

<span data-ttu-id="c26ee-105">在 CMC 要求中新增延伸模組，方法是將它們新增至下列 asn.1 語法範例中所示的 **TaggedAttributes** 結構。</span><span class="sxs-lookup"><span data-stu-id="c26ee-105">Extensions are included in a CMC request by adding them to the **TaggedAttributes** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="c26ee-106">如需詳細資訊，請參閱 [屬性](attributes.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="c26ee-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

<span data-ttu-id="c26ee-107">**TaggedAttributes** 集合中的每個結構都包含一個整數識別碼、一個 asn.1 物件識別碼 (OID) 和一組值。</span><span class="sxs-lookup"><span data-stu-id="c26ee-107">Each structure in the **TaggedAttributes** collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="c26ee-108">藉由將 **CmcAddExtensions** 結構新增至 [ **值** ] 欄位，即可將擴充功能併入要求中。</span><span class="sxs-lookup"><span data-stu-id="c26ee-108">Extensions are incorporated into a request by adding a **CmcAddExtensions** structure to the **values** field.</span></span> <span data-ttu-id="c26ee-109">下列範例會顯示 asn.1 結構語法。</span><span class="sxs-lookup"><span data-stu-id="c26ee-109">The ASN.1 structure syntax is shown in the following example.</span></span> <span data-ttu-id="c26ee-110">物件識別碼是 **XCN \_ OID \_ CMC \_ 新增 \_ 延伸** 模組 (1.3.6.1.5.5.7.7.8) 。</span><span class="sxs-lookup"><span data-stu-id="c26ee-110">The object identifier is **XCN\_OID\_CMC\_ADD\_EXTENSIONS** (1.3.6.1.5.5.7.7.8).</span></span>

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

<span data-ttu-id="c26ee-111">下列程式討論如何使用憑證註冊 API，將延伸模組新增至 CMC 憑證要求。</span><span class="sxs-lookup"><span data-stu-id="c26ee-111">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a CMC certificate request.</span></span>

<span data-ttu-id="c26ee-112">**使用憑證註冊 API 將擴充功能新增至 CMC 憑證要求**</span><span class="sxs-lookup"><span data-stu-id="c26ee-112">**To use the Certificate Enrollment API to add extensions to a CMC certificate request**</span></span>

1.  <span data-ttu-id="c26ee-113">使用任何衍生自 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 介面的可用介面建立擴充功能，或直接使用 **IX509Extension** 物件來建立自訂延伸模組。</span><span class="sxs-lookup"><span data-stu-id="c26ee-113">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface or use the **IX509Extension** object directly to create custom extensions.</span></span>
2.  <span data-ttu-id="c26ee-114">呼叫 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)物件上的 [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions)屬性，以取出 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合。</span><span class="sxs-lookup"><span data-stu-id="c26ee-114">Call the [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) property on the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object to retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
3.  <span data-ttu-id="c26ee-115">將步驟1中建立的延伸模組新增至 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) 集合。</span><span class="sxs-lookup"><span data-stu-id="c26ee-115">Add the extensions created in step 1 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
4.  <span data-ttu-id="c26ee-116">呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) 以自動執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="c26ee-116">Call [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) to automatically perform the following actions:</span></span>
    -   <span data-ttu-id="c26ee-117">從 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)物件取出 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)物件。</span><span class="sxs-lookup"><span data-stu-id="c26ee-117">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
    -   <span data-ttu-id="c26ee-118">使用步驟2中取出的 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合來建立和初始化 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)物件。</span><span class="sxs-lookup"><span data-stu-id="c26ee-118">Create and initialize an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object by using the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 2.</span></span>
    -   <span data-ttu-id="c26ee-119">建立 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合，並在其中新增 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) 物件。</span><span class="sxs-lookup"><span data-stu-id="c26ee-119">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object to it.</span></span>
    -   <span data-ttu-id="c26ee-120">使用 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合來初始化 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件。</span><span class="sxs-lookup"><span data-stu-id="c26ee-120">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
    -   <span data-ttu-id="c26ee-121">將 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件加入至 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) 集合。</span><span class="sxs-lookup"><span data-stu-id="c26ee-121">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c26ee-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="c26ee-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c26ee-123">屬性</span><span class="sxs-lookup"><span data-stu-id="c26ee-123">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="c26ee-124">屬性架構</span><span class="sxs-lookup"><span data-stu-id="c26ee-124">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="c26ee-125">CMC 屬性</span><span class="sxs-lookup"><span data-stu-id="c26ee-125">CMC Attributes</span></span>](cmc-attributes.md)
</dt> <dt>

[<span data-ttu-id="c26ee-126">擴充功能</span><span class="sxs-lookup"><span data-stu-id="c26ee-126">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



