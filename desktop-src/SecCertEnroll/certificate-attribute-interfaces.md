---
description: 下列介面可以用來建立憑證屬性。
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: 憑證屬性介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973472"
---
# <a name="certificate-attribute-interfaces"></a>憑證屬性介面

下列介面可以用來建立憑證屬性。



| 介面                                                                    | 描述                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | 代表憑證要求中的密碼編譯屬性。                                                                              |
| [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | 管理 [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) 物件的集合。                                                                 |
| [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | 表示 PKCS \# 7、pkcs \# 10 或 CMC 憑證要求中的屬性。                                                               |
| [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | 表示可用於識別產生憑證要求之用戶端的屬性。                                       |
| [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | 代表憑證要求中的憑證延伸。                                                                             |
| [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | 表示屬性，其中包含要由憑證授權單位單位封存的加密私密金鑰。                                 |
| [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | 表示屬性，其中包含要由憑證授權單位單位封存之加密私密金鑰的 SHA-1 雜湊。                |
| [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | 代表屬性，這個屬性會識別要求憑證之實體所使用的密碼編譯提供者。                           |
| [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | 表示屬性，其中包含產生憑證要求之用戶端作業系統的版本資訊。 |
| [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | 表示包含要更新之憑證的屬性。                                                                        |
| [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | 管理 [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) 物件的集合。                                                                   |
| [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | 表示泛型名稱/值配對。                                                                                                       |
| [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | 管理 [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) 物件的集合。                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CertEnroll 介面](certenroll-interfaces.md)
</dt> </dl>

 

 



