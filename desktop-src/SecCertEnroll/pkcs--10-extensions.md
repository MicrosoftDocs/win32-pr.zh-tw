---
description: 延伸模組會包含在 PKCS \# 10 憑證要求中，方法是將它們新增至下列 asn.1 語法範例所示 CertificationRequestInfo 結構的 [屬性] 欄位。 如需詳細資訊，請參閱屬性主題。
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: PKCS \# 10 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba71f0a24f50503fd92b3b9670b787dea3b9ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980082"
---
# <a name="pkcs-10-extensions"></a>PKCS \# 10 擴充功能

延伸模組會包含在 PKCS \# 10 憑證要求中，方法是將它們新增至下列 asn.1 語法範例所示 **CertificationRequestInfo** 結構的 [**屬性**] 欄位。 如需詳細資訊，請參閱 [屬性](attributes.md) 主題。

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

下列程式討論如何使用憑證註冊 API，將延伸模組新增至 PKCS \# 10 憑證要求：

1.  藉由呼叫 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件上的 [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions)屬性來取出 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合。
2.  使用任何衍生自 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 介面的可用介面，建立擴充功能。
3.  將步驟2中建立的延伸模組新增至步驟1中所取出的 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) 集合。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[屬性](attributes.md)
</dt> <dt>

[屬性架構](attribute-architecture.md)
</dt> <dt>

[PKCS \# 10 屬性](pkcs--10-attributes.md)
</dt> <dt>

[擴充功能](extensions.md)
</dt> </dl>

 

 



