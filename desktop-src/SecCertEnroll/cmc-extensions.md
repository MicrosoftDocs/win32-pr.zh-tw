---
description: 在 CMC 要求中新增延伸模組，方法是將它們新增至下列 asn.1 語法範例中所示的 TaggedAttributes 結構。 如需詳細資訊，請參閱屬性主題。
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: CMC 延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d29873bc43f7a7229b363a7b09cdf03a23127cc5d5e0e738036c6005a6cc7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901841"
---
# <a name="cmc-extensions"></a>CMC 延伸模組

在 CMC 要求中新增延伸模組，方法是將它們新增至下列 asn.1 語法範例中所示的 **TaggedAttributes** 結構。 如需詳細資訊，請參閱 [屬性](attributes.md) 主題。

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

**TaggedAttributes** 集合中的每個結構都包含一個整數識別碼、一個 asn.1 物件識別碼 (OID) 和一組值。 藉由將 **CmcAddExtensions** 結構新增至 [ **值** ] 欄位，即可將擴充功能併入要求中。 下列範例會顯示 asn.1 結構語法。 物件識別碼是 **XCN \_ OID \_ CMC \_ 新增 \_ 延伸** 模組 (1.3.6.1.5.5.7.7.8) 。

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

下列程式討論如何使用憑證註冊 API，將延伸模組新增至 CMC 憑證要求。

**使用憑證註冊 API 將擴充功能新增至 CMC 憑證要求**

1.  使用任何衍生自 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 介面的可用介面建立擴充功能，或直接使用 **IX509Extension** 物件來建立自訂延伸模組。
2.  呼叫 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)物件上的 [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions)屬性，以取出 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合。
3.  將步驟1中建立的延伸模組新增至 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) 集合。
4.  呼叫 [**註冊**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) 以自動執行下列動作：
    -   從 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)物件取出 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)物件。
    -   使用步驟2中取出的 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合來建立和初始化 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)物件。
    -   建立 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合，並在其中新增 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) 物件。
    -   使用 [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) 集合來初始化 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件。
    -   將 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件加入至 [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) 集合。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[屬性](attributes.md)
</dt> <dt>

[屬性架構](attribute-architecture.md)
</dt> <dt>

[CMC 屬性](cmc-attributes.md)
</dt> <dt>

[擴充功能](extensions.md)
</dt> </dl>

 

 



