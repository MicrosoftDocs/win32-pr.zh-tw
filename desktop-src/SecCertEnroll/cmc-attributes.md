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
# <a name="cmc-attributes"></a>CMC 屬性

在實務上，使用下列語法所示的 CMC 要求結構相當複雜，因為它通常包含了嵌套的要求。 例如，CMC 要求可以在 TaggedRequest 序列中包含零個或一個 PKCS \# 10 要求，而且可以 \# 在 **TaggedContentInfo** 序列中包含零個或一個 pkcs 7 訊息。 每個嵌套 \# 的 PKCS 7 訊息都可以包含 CMC 要求，進而包含更多要求。 嵌套層級的數目理論上是無限制的，但 (CA) 的憑證授權單位單位通常會設定為限制要求的大小。 屬性可以套用至最上層要求或嵌套要求。 這將在下列各節中討論。

## <a name="cmcdata-structure"></a>CMCData 結構

CMC 要求包含 **TaggedAttribute**、 **TaggedRequest** 和 **TaggedContentInfo** ASN. 1 結構的序列。

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

## <a name="taggedattribute-structure"></a>TaggedAttribute 結構

將屬性新增至 **TaggedAttribute** 集合，以將屬性包含在 CMC 憑證要求中。 集合中的每個結構都包含一個整數識別碼、一個 asn.1 物件識別碼 (OID) 和一組值。 可能的值可以是下列任何一項。

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

## <a name="cmcaddattributes"></a>CMCAddAttributes

如果此結構中的屬性適用于嵌套的 PKCS \# 10 要求， **certReferences** 欄位會包含可識別要求的 **BodyPartID** 。 如果將屬性套用至嵌套的 CMC 要求， **pkiDataReference** 欄位將會包含要求的 **BodyPartID** 。 目前，只有其中一個欄位可以是非零。 可包含的屬性會列在 [支援的屬性](supported-attributes.md) 主題中。

## <a name="cmcaddextensions"></a>CmcAddExtensions

此結構可包含 x.509 第3版擴充功能，以及由 Microsoft 定義的擴充功能。 這個屬性是使用 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) 介面所定義。 如果延伸模組適用于嵌套的 PKCS \# 10 要求， **certReferences** 欄位會包含可識別要求的 **BodyPartID** 。 如果延伸模組適用于嵌套的 CMC 要求， **pkiDataReference** 欄位將包含要求的 **BodyPartID** 。 目前，只有其中一個欄位可以是非零。

## <a name="sendernonce"></a>SenderNonce

Nonce 是隨機或虛擬隨機的二進位資料，可包含在憑證要求和回應交易中，以協助確保回應或要求不會重複先前的訊息。 如需詳細資訊，請參閱 [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) 屬性。

## <a name="transactid"></a>TransactID

您可以使用識別碼追蹤來回行程憑證要求和回應交易。 用戶端會產生交易識別碼並保留它，直到憑證或註冊授權單位以完成交易的訊息回應為止。 回應包括識別碼。 如需詳細資訊，請參閱 [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) 屬性。

## <a name="reginfo"></a>RegInfo

這個屬性可用來包含用戶端選擇要放入 CMC 要求中的任何註冊資訊。 屬性值是包含串連的名稱/值組的字串。 如需詳細資訊，請參閱 [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[支援的屬性](supported-attributes.md)
</dt> </dl>

 

 



