---
description: 下列介面可以用來建立憑證延伸。
ms.assetid: 52750a0a-0cd9-40cc-8c23-839e4e20fd77
title: 憑證擴充介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c192ff7bc661c36ded8611628a1cd82dddca1697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511549"
---
# <a name="certificate-extension-interfaces"></a>憑證擴充介面

下列介面可以用來建立憑證延伸。



| 介面                                                                            | 描述                                                                                                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                         | 表示 **AlternativeNames** 延伸模組的實例。                                                                                   |
| [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames)                                       | 管理 [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) 物件的集合。                                                                  |
| [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                     | 指定憑證原則，以識別可使用憑證的目的。                                              |
| [**ICertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicies)                                 | 管理 [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy) 物件的集合。                                                              |
| [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                         | 表示可以與憑證原則相關聯的辨識符號。                                                                       |
| [**IPolicyQualifiers**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifiers)                                       | 管理 [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier) 物件的集合。                                                                  |
| [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                             | 定義憑證要求的延伸。                                                                                                |
| [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)             | 指定憑證主旨的一或多個替代名稱形式。                                                                 |
| [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier) | 表示 **AuthorityKeyIdentifier** 延伸模組。                                                                                            |
| [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)             | 指定憑證主體是否為憑證授權單位單位，如果是，則為從屬憑證授權單位單位鏈的深度。 |
| [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)       | 表示原則資訊詞彙的集合。                                                                                           |
| [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)   | 表示物件識別碼的集合，指出應用程式如何使用憑證。                                   |
| [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)             | 表示物件識別碼的集合，識別憑證中包含之公開金鑰的用途。                    |
| [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)                             | 代表可由憑證中的公開金鑰所執行之作業的限制。                                |
| [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)                                           | 管理 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 物件的集合。                                                                      |
| [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)           | 代表將電子郵件收件者的解密功能報告給電子郵件傳送者的集合。                                     |
| [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)     | 表示用來識別簽署憑證的 **SubjectKeyIdentifier** 延伸模組。                                                        |
| [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)                             | 表示包含第2版範本的 **CertificateTemplate** 延伸模組。                                                             |
| [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)                     | 表示包含第1版範本的 **CertificateTemplateName** 延伸模組。                                                         |
| [**ISmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapabilities)                                     | 管理 [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability) 物件的集合。                                                                  |
| [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                         | 代表識別電子郵件收件者之解密功能的 **SMIMECapabilities** 延伸模組。                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CertEnroll 介面](certenroll-interfaces.md)
</dt> </dl>

 

 



