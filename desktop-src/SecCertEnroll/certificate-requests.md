---
description: 憑證註冊 SDK 可以用來建立 PKCS \# 10、pkcs \# 7、CMC 和自我簽署的憑證要求。
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: 憑證要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974080"
---
# <a name="certificate-requests"></a>憑證要求

憑證註冊 SDK 可以用來建立 PKCS \# 10、pkcs \# 7、CMC 和自我簽署的憑證要求。 每種類型的要求都會以下表所列的其中一個介面表示。 所有的要求介面都會直接或間接繼承自 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) 介面。 

| 介面                                                                        | 描述                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | 表示 PKCS \# 10 要求。 此介面繼承自 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)。                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | 表示 PKCS \# 7 要求。 此介面繼承自 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)。                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | 代表自我簽署憑證。 此介面繼承自 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)。 |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | 表示 CMC 要求。 此介面繼承自 [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)。               |



 

下圖顯示憑證註冊 API 所支援之要求物件的繼承結構。 [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)物件可直接或間接作為所有可用要求物件的基類。

![要求介面的繼承結構](images/certificate-request-inheritance.png)

無論何種類型，憑證要求都會包含提出要求之主體的相關資訊、主體的公開金鑰、一組屬性、一組 x.509 第3版延伸 (可提交為屬性) 的一部分，以及簽章。 這些問題是由下列主題所解決：

-   [主體名稱](subject-names.md)
-   [屬性](attributes.md)
-   [擴充功能](extensions.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



