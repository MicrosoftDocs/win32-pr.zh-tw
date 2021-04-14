---
description: 屬性會包含在 PKCS \# 10 憑證要求中，方法是將它們新增至下列 asn.1 語法範例中所示的 CertificationRequestInfo 結構。
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: PKCS \# 10 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c69260fa09b99c4d91fa1f8bcdafeb4b0da285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321051"
---
# <a name="pkcs-10-attributes"></a><span data-ttu-id="27c85-103">PKCS \# 10 屬性</span><span class="sxs-lookup"><span data-stu-id="27c85-103">PKCS \#10 Attributes</span></span>

<span data-ttu-id="27c85-104">屬性會包含在 PKCS \# 10 憑證要求中，方法是將它們新增至下列 asn.1 語法範例中所示的 **CertificationRequestInfo** 結構。</span><span class="sxs-lookup"><span data-stu-id="27c85-104">Attributes are included in a PKCS \#10 certificate request by adding them to the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="27c85-105">如需如何將屬性新增至要求的詳細資訊，請參閱 [屬性架構](attribute-architecture.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="27c85-105">For more information about how you can add attributes to a request, see the [Attribute Architecture](attribute-architecture.md) topic.</span></span>

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

<span data-ttu-id="27c85-106">最常新增至 PKCS \# 10 要求的屬性是由 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) 物件定義的第3版擴充功能集合。</span><span class="sxs-lookup"><span data-stu-id="27c85-106">The attribute most commonly added to a PKCS \#10 request is a collection of version 3 extensions defined by an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object.</span></span> <span data-ttu-id="27c85-107">由於 PKCS \# 10 要求不包含可直接新增擴充功能的欄位，因此必須將它們新增為屬性。</span><span class="sxs-lookup"><span data-stu-id="27c85-107">Because a PKCS \#10 request does not contain a field to which the extensions can be directly added, they must be added as an attribute.</span></span> <span data-ttu-id="27c85-108">**ClientId**、 **CspProvider**、 **OSVersion** 和 **RenewalCertificate** 屬性也可以新增至 PKCS ) 主題。</span><span class="sxs-lookup"><span data-stu-id="27c85-108">The **ClientId**, **CspProvider**, **OSVersion**, and **RenewalCertificate** attributes can also be added to a PKCS ) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27c85-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="27c85-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c85-110">支援的屬性</span><span class="sxs-lookup"><span data-stu-id="27c85-110">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



