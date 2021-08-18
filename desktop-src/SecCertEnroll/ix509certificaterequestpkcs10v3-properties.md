---
description: IX509CertificateRequestPkcs10V3 介面會公開下列屬性。
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: IX509CertificateRequestPkcs10V3 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcc126c21ca5fee5e8d1c15dd2561439c7a35f0f6cef637177ff36160a22d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976218"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>IX509CertificateRequestPkcs10V3 屬性

[**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)介面會公開下列屬性。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                            | 描述                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttestationEncryptionCertificate 屬性**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | 用來從用戶端加密 EKPUB 和 EKCERT 值的憑證。 這個屬性必須設定為有效的憑證，以連結到信任的電腦根目錄。<br/>                                                                                                                                                                                |
| [**AttestPrivateKey 屬性**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | 如果所建立的私密金鑰需要證明，則為 True;否則為 false。 若為 true，則預期 [**AttestationEncryptionCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) 屬性已設定。 <br/>                                                                                                        |
| [**ChallengePassword 屬性**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | 建立具有挑戰的要求時所要使用的密碼。 若要建立不含挑戰的要求，請不要設定 [**ChallengePassword**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword) 屬性。<br/>                                                                                                                                      |
| [**EncryptionAlgorithm 屬性**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | 用來從用戶端加密 EKPUB 和 EKCERT 值的加密演算法。<br/>                                                                                                                                                                                                                                                               |
| [**EncryptionStrength 屬性**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | 識別要用於加密的 [**EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) 位長度。 如果 **EncryptionAlgorithm** 只支援一個位長度，您就不需要指定 [**EncryptionStrength**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength) 屬性的值。<br/> |
| [**NameValuePairs 屬性**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | 其他憑證屬性值的名稱/值配對集合。<br/>                                                                                                                                                                                                                                                                         |



 

 

 




