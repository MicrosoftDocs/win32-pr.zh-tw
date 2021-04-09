---
description: 在實務上，使用下列語法所示的 CMC 要求結構相當複雜，因為它通常包含了嵌套的要求。
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: CMC 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6778575a9359ad5b8764528fb0351b68efc1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694023"
---
# <a name="cmc-attributes"></a><span data-ttu-id="3dc14-103">CMC 屬性</span><span class="sxs-lookup"><span data-stu-id="3dc14-103">CMC Attributes</span></span>

<span data-ttu-id="3dc14-104">在實務上，使用下列語法所示的 CMC 要求結構相當複雜，因為它通常包含了嵌套的要求。</span><span class="sxs-lookup"><span data-stu-id="3dc14-104">In practice, the structure of a CMC request, shown by the following syntax, is relatively complex because it often contains nested requests.</span></span> <span data-ttu-id="3dc14-105">例如，CMC 要求可以在 TaggedRequest 序列中包含零個或一個 PKCS \# 10 要求，而且可以 \# 在 **TaggedContentInfo** 序列中包含零個或一個 pkcs 7 訊息。</span><span class="sxs-lookup"><span data-stu-id="3dc14-105">For example, a CMC request can contain zero or one PKCS \#10 requests in a **TaggedRequest** sequence, and it can contain zero or one PKCS \#7 messages in a **TaggedContentInfo** sequence.</span></span> <span data-ttu-id="3dc14-106">每個嵌套 \# 的 PKCS 7 訊息都可以包含 CMC 要求，進而包含更多要求。</span><span class="sxs-lookup"><span data-stu-id="3dc14-106">Each nested PKCS \#7 message can contain a CMC request which can, in turn, contain more requests.</span></span> <span data-ttu-id="3dc14-107">嵌套層級的數目理論上是無限制的，但 (CA) 的憑證授權單位單位通常會設定為限制要求的大小。</span><span class="sxs-lookup"><span data-stu-id="3dc14-107">The number of nesting levels is theoretically unlimited, but the certification authority (CA) is typically configured to limit the size of a request.</span></span> <span data-ttu-id="3dc14-108">屬性可以套用至最上層要求或嵌套要求。</span><span class="sxs-lookup"><span data-stu-id="3dc14-108">Attributes can be applied to the top level request or to the nested requests.</span></span> <span data-ttu-id="3dc14-109">這將在下列各節中討論。</span><span class="sxs-lookup"><span data-stu-id="3dc14-109">This is discussed in the following sections.</span></span>

## <a name="cmcdata-structure"></a><span data-ttu-id="3dc14-110">CMCData 結構</span><span class="sxs-lookup"><span data-stu-id="3dc14-110">CMCData Structure</span></span>

<span data-ttu-id="3dc14-111">CMC 要求包含 **TaggedAttribute**、 **TaggedRequest** 和 **TaggedContentInfo** ASN. 1 結構的序列。</span><span class="sxs-lookup"><span data-stu-id="3dc14-111">A CMC request contains sequences of **TaggedAttribute**, **TaggedRequest**, and **TaggedContentInfo** ASN.1 structures.</span></span>

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

## <a name="taggedattribute-structure"></a><span data-ttu-id="3dc14-112">TaggedAttribute 結構</span><span class="sxs-lookup"><span data-stu-id="3dc14-112">TaggedAttribute Structure</span></span>

<span data-ttu-id="3dc14-113">將屬性新增至 **TaggedAttribute** 集合，以將屬性包含在 CMC 憑證要求中。</span><span class="sxs-lookup"><span data-stu-id="3dc14-113">Attributes are included in a CMC certificate request by adding them to the **TaggedAttribute** collection.</span></span> <span data-ttu-id="3dc14-114">集合中的每個結構都包含一個整數識別碼、一個 asn.1 物件識別碼 (OID) 和一組值。</span><span class="sxs-lookup"><span data-stu-id="3dc14-114">Each structure in the collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="3dc14-115">可能的值可以是下列任何一項。</span><span class="sxs-lookup"><span data-stu-id="3dc14-115">The possible values can be any of the following.</span></span>

``` syntax
CmcAddAttributes ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   attributes              Attributes
}

Attributes ::= SET OF Attribute
Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

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

SenderNonce ::= OCTET STRING

TransactID ::= OCTET STRING

RegInfo ::= OCTET STRING
```

## <a name="cmcaddattributes"></a><span data-ttu-id="3dc14-116">CMCAddAttributes</span><span class="sxs-lookup"><span data-stu-id="3dc14-116">CMCAddAttributes</span></span>

<span data-ttu-id="3dc14-117">如果此結構中的屬性適用于嵌套的 PKCS \# 10 要求， **certReferences** 欄位會包含可識別要求的 **BodyPartID** 。</span><span class="sxs-lookup"><span data-stu-id="3dc14-117">If the attributes in this structure apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="3dc14-118">如果將屬性套用至嵌套的 CMC 要求， **pkiDataReference** 欄位將會包含要求的 **BodyPartID** 。</span><span class="sxs-lookup"><span data-stu-id="3dc14-118">If the attributes apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="3dc14-119">目前，只有其中一個欄位可以是非零。</span><span class="sxs-lookup"><span data-stu-id="3dc14-119">Currently, only one of these fields can be nonzero.</span></span> <span data-ttu-id="3dc14-120">可包含的屬性會列在 [支援的屬性](supported-attributes.md) 主題中。</span><span class="sxs-lookup"><span data-stu-id="3dc14-120">The attributes that can be included are listed in the [Supported Attributes](supported-attributes.md) topic.</span></span>

## <a name="cmcaddextensions"></a><span data-ttu-id="3dc14-121">CmcAddExtensions</span><span class="sxs-lookup"><span data-stu-id="3dc14-121">CmcAddExtensions</span></span>

<span data-ttu-id="3dc14-122">此結構可包含 x.509 第3版擴充功能，以及由 Microsoft 定義的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3dc14-122">This structure can contain X.509 version 3 extensions plus extensions defined by Microsoft.</span></span> <span data-ttu-id="3dc14-123">這個屬性是使用 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) 介面所定義。</span><span class="sxs-lookup"><span data-stu-id="3dc14-123">This attribute is defined by using the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface.</span></span> <span data-ttu-id="3dc14-124">如果延伸模組適用于嵌套的 PKCS \# 10 要求， **certReferences** 欄位會包含可識別要求的 **BodyPartID** 。</span><span class="sxs-lookup"><span data-stu-id="3dc14-124">If the extensions apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="3dc14-125">如果延伸模組適用于嵌套的 CMC 要求， **pkiDataReference** 欄位將包含要求的 **BodyPartID** 。</span><span class="sxs-lookup"><span data-stu-id="3dc14-125">If the extensions apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="3dc14-126">目前，只有其中一個欄位可以是非零。</span><span class="sxs-lookup"><span data-stu-id="3dc14-126">Currently, only one of these fields can be nonzero.</span></span>

## <a name="sendernonce"></a><span data-ttu-id="3dc14-127">SenderNonce</span><span class="sxs-lookup"><span data-stu-id="3dc14-127">SenderNonce</span></span>

<span data-ttu-id="3dc14-128">Nonce 是隨機或虛擬隨機的二進位資料，可包含在憑證要求和回應交易中，以協助確保回應或要求不會重複先前的訊息。</span><span class="sxs-lookup"><span data-stu-id="3dc14-128">A nonce is random or pseudo-random binary data that can be included in a certificate request and response transaction to help ensure that the response or request is not a repeat of a previous message.</span></span> <span data-ttu-id="3dc14-129">如需詳細資訊，請參閱 [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) 屬性。</span><span class="sxs-lookup"><span data-stu-id="3dc14-129">For more information, see the [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) property.</span></span>

## <a name="transactid"></a><span data-ttu-id="3dc14-130">TransactID</span><span class="sxs-lookup"><span data-stu-id="3dc14-130">TransactID</span></span>

<span data-ttu-id="3dc14-131">您可以使用識別碼追蹤來回行程憑證要求和回應交易。</span><span class="sxs-lookup"><span data-stu-id="3dc14-131">A round trip certificate request and response transaction can be tracked using an identifier.</span></span> <span data-ttu-id="3dc14-132">用戶端會產生交易識別碼並保留它，直到憑證或註冊授權單位以完成交易的訊息回應為止。</span><span class="sxs-lookup"><span data-stu-id="3dc14-132">The client generates a transaction ID and retains it until the certificate or registration authority responds with a message that completes the transaction.</span></span> <span data-ttu-id="3dc14-133">回應包括識別碼。</span><span class="sxs-lookup"><span data-stu-id="3dc14-133">The response includes the identifier.</span></span> <span data-ttu-id="3dc14-134">如需詳細資訊，請參閱 [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) 屬性。</span><span class="sxs-lookup"><span data-stu-id="3dc14-134">For more information, see the [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) property.</span></span>

## <a name="reginfo"></a><span data-ttu-id="3dc14-135">RegInfo</span><span class="sxs-lookup"><span data-stu-id="3dc14-135">RegInfo</span></span>

<span data-ttu-id="3dc14-136">這個屬性可用來包含用戶端選擇要放入 CMC 要求中的任何註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="3dc14-136">This attribute can be used to contain any registration information that the client chooses to put into the CMC request.</span></span> <span data-ttu-id="3dc14-137">屬性值是包含串連的名稱/值組的字串。</span><span class="sxs-lookup"><span data-stu-id="3dc14-137">The attribute value is string that contains concatenated name-value pairs.</span></span> <span data-ttu-id="3dc14-138">如需詳細資訊，請參閱 [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) 屬性。</span><span class="sxs-lookup"><span data-stu-id="3dc14-138">For more information, see the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dc14-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="3dc14-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dc14-140">支援的屬性</span><span class="sxs-lookup"><span data-stu-id="3dc14-140">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



