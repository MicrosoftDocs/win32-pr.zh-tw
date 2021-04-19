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
# <a name="pkcs-10-extensions"></a><span data-ttu-id="92dd3-104">PKCS \# 10 擴充功能</span><span class="sxs-lookup"><span data-stu-id="92dd3-104">PKCS \#10 Extensions</span></span>

<span data-ttu-id="92dd3-105">延伸模組會包含在 PKCS \# 10 憑證要求中，方法是將它們新增至下列 asn.1 語法範例所示 **CertificationRequestInfo** 結構的 [**屬性**] 欄位。</span><span class="sxs-lookup"><span data-stu-id="92dd3-105">Extensions are included in a PKCS \#10 certificate request by adding them to the **attributes** field of the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="92dd3-106">如需詳細資訊，請參閱 [屬性](attributes.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="92dd3-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

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

<span data-ttu-id="92dd3-107">下列程式討論如何使用憑證註冊 API，將延伸模組新增至 PKCS \# 10 憑證要求：</span><span class="sxs-lookup"><span data-stu-id="92dd3-107">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a PKCS \#10 certificate request:</span></span>

1.  <span data-ttu-id="92dd3-108">藉由呼叫 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)物件上的 [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions)屬性來取出 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)集合。</span><span class="sxs-lookup"><span data-stu-id="92dd3-108">Retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection by calling the [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) property on the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>
2.  <span data-ttu-id="92dd3-109">使用任何衍生自 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 介面的可用介面，建立擴充功能。</span><span class="sxs-lookup"><span data-stu-id="92dd3-109">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface.</span></span>
3.  <span data-ttu-id="92dd3-110">將步驟2中建立的延伸模組新增至步驟1中所取出的 [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) 集合。</span><span class="sxs-lookup"><span data-stu-id="92dd3-110">Add the extensions created in step 2 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92dd3-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="92dd3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92dd3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="92dd3-112">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="92dd3-113">屬性架構</span><span class="sxs-lookup"><span data-stu-id="92dd3-113">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="92dd3-114">PKCS \# 10 屬性</span><span class="sxs-lookup"><span data-stu-id="92dd3-114">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
</dt> <dt>

[<span data-ttu-id="92dd3-115">擴充功能</span><span class="sxs-lookup"><span data-stu-id="92dd3-115">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



