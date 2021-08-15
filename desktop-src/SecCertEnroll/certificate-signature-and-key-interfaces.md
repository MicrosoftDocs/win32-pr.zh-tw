---
description: 下列介面可以用來管理憑證簽章和公開金鑰和私密金鑰。
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: 憑證簽章和金鑰介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdfd4c76b0e73f2954780d797e092e6d8b7570ebaee082ef93319f74abc24e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902304"
---
# <a name="certificate-signature-and-key-interfaces"></a>憑證簽章和金鑰介面

下列介面可以用來管理憑證簽章和公開金鑰和私密金鑰。



| 介面                                                      | 描述                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | 代表可讓您簽署憑證要求的簽署憑證。                  |
| [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | 管理 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件的集合。                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | 代表可用於加密、簽署和金鑰協定的非對稱私密金鑰。 |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | 表示公開/私密金鑰組中的公開金鑰。                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | 表示用來簽署憑證要求的資訊。                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CertEnroll 介面](certenroll-interfaces.md)
</dt> </dl>

 

 



