---
description: 下列介面可以用來建立憑證要求。
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: 憑證要求介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba4f16c6aba1be724fcf2639dd64d7988e40b79a5b29a2d500beb3ae66f4ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902557"
---
# <a name="certificate-request-interfaces"></a>憑證要求介面

下列介面可以用來建立憑證要求。



| 介面                                                                          | 描述                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | 表示憑證要求的抽象最上層介面。                                                                                        |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | 可讓您直接建立憑證，而不需經過註冊或憑證授權單位單位。                                                  |
| [**IX509CertificateRequestCertificate2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | 擴充 [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) 介面，以從範本啟用初始化。              |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | 表示 CMC 要求。                                                                                                                                     |
| [**IX509CertificateRequestCmc2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | 擴充 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 介面，以從範本啟用初始化。                              |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | 表示 PKCS \# 10 要求。                                                                                                                               |
| [**IX509CertificateRequestPkcs10V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | 擴充 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 介面，以從範本啟用初始化。                        |
| [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | 擴充 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 介面，並新增可啟用 TPM 憑證證明的屬性。 |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | 表示 PKCS \# 7 要求。                                                                                                                                |
| [**IX509CertificateRequestPkcs7V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | 擴充 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) 介面，以從範本啟用初始化。                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CertEnroll 介面](certenroll-interfaces.md)
</dt> </dl>

 

 



