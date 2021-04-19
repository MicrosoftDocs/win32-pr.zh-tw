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
# <a name="supported-certificate-formats"></a><span data-ttu-id="9dbaf-103">支援的憑證格式</span><span class="sxs-lookup"><span data-stu-id="9dbaf-103">Supported Certificate Formats</span></span>

<span data-ttu-id="9dbaf-104">憑證服務可以發出下列類型的憑證。</span><span class="sxs-lookup"><span data-stu-id="9dbaf-104">Certificate Services can issue the following types of certificates.</span></span>



| <span data-ttu-id="9dbaf-105">詞彙</span><span class="sxs-lookup"><span data-stu-id="9dbaf-105">Term</span></span>                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="9dbaf-106">描述</span><span class="sxs-lookup"><span data-stu-id="9dbaf-106">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dbaf-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) 第3版 SSL 相容用戶端驗證憑證</span><span class="sxs-lookup"><span data-stu-id="9dbaf-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) version 3 SSL-compatible client authentication certificate</span></span><br/> | <span data-ttu-id="9dbaf-108">此用戶端驗證憑證會識別用戶端，並由伺服器用來驗證要求伺服器存取的用戶端。</span><span class="sxs-lookup"><span data-stu-id="9dbaf-108">This client authentication certificate identifies a client and is used by servers to authenticate a client that requests server access.</span></span><br/>     |
| <span data-ttu-id="9dbaf-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL 相容伺服器驗證憑證</span><span class="sxs-lookup"><span data-stu-id="9dbaf-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL-compatible server authentication certificate</span></span><br/>                                                                                         | <span data-ttu-id="9dbaf-110">此伺服器驗證憑證會識別伺服器，並供用戶端用來驗證用戶端想要存取的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9dbaf-110">This server authentication certificate identifies a server and is used by clients to authenticate a server that the client wants to access.</span></span><br/> |
| <span data-ttu-id="9dbaf-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME*](../secgloss/s-gly.md) 憑證</span><span class="sxs-lookup"><span data-stu-id="9dbaf-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME*](../secgloss/s-gly.md) certificate</span></span><br/>                                                                                                           | <span data-ttu-id="9dbaf-112">用戶端會使用此憑證在 S/MIME (安全/多用途網際網路郵件延伸) 通訊協定下的安全電子郵件。</span><span class="sxs-lookup"><span data-stu-id="9dbaf-112">This certificate is used by clients for secure email under the S/MIME (Secure/Multipurpose Internet Mail Extensions) protocol.</span></span><br/>              |



 

<span data-ttu-id="9dbaf-113">除了這些憑證之外，憑證服務也可以藉由撰寫自訂原則模組，用來發出其他的 x.509 憑證。</span><span class="sxs-lookup"><span data-stu-id="9dbaf-113">In addition to these certificates, Certificate Services can also be used to issue other X.509 certificates by writing a custom policy module.</span></span>

> [!Note]  
> <span data-ttu-id="9dbaf-114">「伺服器驗證憑證」和「伺服器憑證」以及「用戶端驗證憑證」和「用戶端憑證」是可互換的詞彙。</span><span class="sxs-lookup"><span data-stu-id="9dbaf-114">"Server authentication certificate" and "server certificate" as well as "client authentication certificate" and "client certificate" are interchangeable terms.</span></span>

 

<span data-ttu-id="9dbaf-115">此外，憑證服務還包含 Microsoft 企業憑證授權單位單位設定中的憑證範本。</span><span class="sxs-lookup"><span data-stu-id="9dbaf-115">Additionally, Certificate Services includes certificate templates in the Microsoft enterprise certification authority configuration.</span></span> <span data-ttu-id="9dbaf-116">請參閱 Windows 說明文件中的憑證範本，以瞭解它們如何定義憑證用途。</span><span class="sxs-lookup"><span data-stu-id="9dbaf-116">Consult the Windows Help documentation for certificate templates to understand how they define certificate purposes.</span></span>

 

 
