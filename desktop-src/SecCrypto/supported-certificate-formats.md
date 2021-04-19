---
description: 列出憑證服務所支援的憑證格式。
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: 支援的憑證格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f37f3e4c29ae765f68484aecf0bf9d9b8aea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989439"
---
# <a name="supported-certificate-formats"></a>支援的憑證格式

憑證服務可以發出下列類型的憑證。



| 詞彙                                                                                                                                                                                                                                                                                                                                                                                             | 描述                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) 第3版 SSL 相容用戶端驗證憑證<br/> | 此用戶端驗證憑證會識別用戶端，並由伺服器用來驗證要求伺服器存取的用戶端。<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL 相容伺服器驗證憑證<br/>                                                                                         | 此伺服器驗證憑證會識別伺服器，並供用戶端用來驗證用戶端想要存取的伺服器。<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME*](../secgloss/s-gly.md) 憑證<br/>                                                                                                           | 用戶端會使用此憑證在 S/MIME (安全/多用途網際網路郵件延伸) 通訊協定下的安全電子郵件。<br/>              |



 

除了這些憑證之外，憑證服務也可以藉由撰寫自訂原則模組，用來發出其他的 x.509 憑證。

> [!Note]  
> 「伺服器驗證憑證」和「伺服器憑證」以及「用戶端驗證憑證」和「用戶端憑證」是可互換的詞彙。

 

此外，憑證服務還包含 Microsoft 企業憑證授權單位單位設定中的憑證範本。 請參閱 Windows 說明文件中的憑證範本，以瞭解它們如何定義憑證用途。

 

 
