---
title: IKE/AuthIP 結構
description: IKE/AuthIP 結構
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1b5c8f69ec0ac667dee5fc541c84b8e9e66ceb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/27/2020
ms.locfileid: "104374681"
---
# <a name="ikeauthip-structures"></a>IKE/AuthIP 結構

## <a name="in-this-section"></a>本節內容

-   [**IKEEXT \_ 驗證 \_ METHOD0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**IKEEXT \_ 驗證 \_ METHOD1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**IKEEXT \_ 驗證 \_ METHOD2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**IKEEXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**IKEEXT \_ CERT \_ .name0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IKEEXT \_ 憑證 \_ 根 \_ CONFIG0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**IKEEXT \_ 憑證 \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**IKEEXT \_ 憑證 \_ AUTHENTICATION1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**IKEEXT \_ 憑證 \_ AUTHENTICATION2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**IKEEXT \_ 憑證 \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**IKEEXT \_ 憑證 \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**IKEEXT \_ 憑證 \_ CRITERIA0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**IKEEXT \_ 加密 \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**IKEEXT \_ 一般 \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**IKEEXT \_ 一般 \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**IKEEXT \_ COOKIE \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**IKEEXT \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**IKEEXT \_ CREDENTIAL2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**IKEEXT \_ CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**IKEEXT \_ CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**IKEEXT \_ CREDENTIALS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**IKEEXT \_ 認證 \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**IKEEXT \_ 認證 \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**IKEEXT \_ 認證 \_ PAIR2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**IKEEXT \_ EAP \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**IKEEXT \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**IKEEXT \_ EM \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**IKEEXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**IKEEXT \_ 完整性 \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**IKEEXT \_ IP \_ 版本 \_ 特定的 \_ 通用 \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**IKEEXT \_ IP \_ 版本 \_ 特定的 \_ 通用 \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**IKEEXT \_ IP \_ 版本 \_ 特定的 \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**IKEEXT \_ IP \_ 版本 \_ 特定的 \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**IKEEXT \_ IPV6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**IKEEXT \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**IKEEXT \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**IKEEXT \_ 名稱 \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**IKEEXT \_ NTLM \_ V2 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**IKEEXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**IKEEXT \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**IKEEXT \_ 預先共用 \_ 金鑰 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**IKEEXT \_ 預先共用 \_ 金鑰 \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**IKEEXT \_ PROPOSAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**IKEEXT \_ 保留的 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**IKEEXT \_ SA \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**IKEEXT \_ SA \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**IKEEXT \_ SA \_ DETAILS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**IKEEXT \_ SA \_ 列舉 \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**IKEEXT \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**IKEEXT \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**IKEEXT \_ TRAFFIC0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




