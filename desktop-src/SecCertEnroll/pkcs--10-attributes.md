---
description: 屬性會包含在 PKCS \# 10 憑證要求中，方法是將它們新增至下列 asn.1 語法範例中所示的 CertificationRequestInfo 結構。
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: PKCS \# 10 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7922f7d308c6956af4c0098ea278a859113af45861ef3d21a20548081e7eee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993288"
---
# <a name="pkcs-10-attributes"></a>PKCS \# 10 屬性

屬性會包含在 PKCS \# 10 憑證要求中，方法是將它們新增至下列 asn.1 語法範例中所示的 **CertificationRequestInfo** 結構。 如需如何將屬性新增至要求的詳細資訊，請參閱 [屬性架構](attribute-architecture.md) 主題。

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

最常新增至 PKCS \# 10 要求的屬性是由 [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) 物件定義的第3版擴充功能集合。 由於 PKCS \# 10 要求不包含可直接新增擴充功能的欄位，因此必須將它們新增為屬性。 **ClientId**、 **CspProvider**、 **OSVersion** 和 **RenewalCertificate** 屬性也可以新增至 PKCS ) 主題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[支援的屬性](supported-attributes.md)
</dt> </dl>

 

 



