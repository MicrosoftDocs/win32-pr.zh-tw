---
description: 列出驗證 Api 中使用的列舉。
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: 驗證列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5640151967867f610aa8b18c81940c684d23c18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690144"
---
# <a name="authentication-enumerations"></a>驗證列舉

驗證列舉會根據使用方式進行分類，如下所示：

-   [認證管理列舉](#credentials-management-enumerations)
-   [LSA 列舉](#lsa-enumerations)
-   [網路提供者列舉](#network-provider-enumerations)
-   [認證安全性支援提供者 (CredSSP) 列舉](#credential-security-support-provider-credssp-enumerations)
-   [其他列舉](#other-enumerations)

## <a name="credentials-management-enumerations"></a>認證管理列舉

認證管理會使用下列列舉。



| 列舉型別                                            | 描述                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**認證 \_ 封送處理 \_ 類型**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | 包含可由 [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) 封送處理或由 [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala)取消封送處理的認證類型。<br/> |
| [**認證 \_ 保護 \_ 類型**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | 指定在使用 [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) 函式時，用來加密認證的安全性內容。<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>LSA 列舉

LSA 使用下列列舉。



| 列舉型別                                                                                   | 描述                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KERB \_ 登入 \_ 提交 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | 列出所要求的登入類型。<br/>                                                                                                                                                                                                                  |
| [**KERB \_ 設定檔 \_ 緩衝區 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | 列出傳回的登入配置檔案類型。<br/>                                                                                                                                                                                                                 |
| [**KERB \_ 通訊協定 \_ 訊息 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | 列出可透過呼叫 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)傳送至 [*Kerberos*](/windows/desktop/SecGloss/k-gly)驗證套件的訊息類型。<br/> |
| [**LSA \_ 樹系 \_ 信任 \_ 衝突 \_ 記錄 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | 定義 LSA 樹系信任記錄之間可能發生的衝突類型。<br/>                                                                                                                                                                           |
| [**LSA \_ 樹系 \_ 信任 \_ 記錄 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | 定義 LSA 樹系信任記錄的類型。<br/>                                                                                                                                                                                                           |
| [**LSA \_ TOKEN \_ 資訊 \_ 類型**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | 指定可包含在登入權杖中的資訊層級。<br/>                                                                                                                                                                                |
| [**MSV1 \_ 0 \_ 登入 \_ 提交 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | 列出所要求的登入類型。<br/>                                                                                                                                                                                                                  |
| [**MSV1 \_ 0 \_ 設定檔 \_ 緩衝區 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | 列出傳回的登入配置檔案類型。<br/>                                                                                                                                                                                                                 |
| [**MSV1 \_ 0 \_ 通訊協定 \_ 訊息 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | 列出可透過呼叫 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)傳送至 [MSV1 \_ 0 驗證套件](msv1-0-authentication-package.md)的訊息類型。<br/>                                                 |
| [**原則 \_ 網域 \_ 資訊 \_ 類別**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | 定義原則網域資訊的類型。<br/>                                                                                                                                                                                                            |
| [**安全性 \_ 登入 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | 指出登入處理常式要求的登入類型。<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>網路提供者列舉

網路提供者會使用下列列舉。



| 列舉型別                                                                       | 描述                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SECPKG \_ 擴充的 \_ 資訊 \_ 類別**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | 列舉類型，指定要設定或針對 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)取得的資訊類型。<br/> |
| [**SECPKG \_ 名稱 \_ 類型**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | 列舉值，指定為帳戶指定的名稱類型。<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>認證安全性支援提供者 (CredSSP) 列舉

CredSSP 使用下列列舉。



| 列舉型別                                          | 描述                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**CREDSPP \_ 提交 \_ 類型**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | 指定 [**CREDSSP \_**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) 認證結構所指定的認證類型。<br/> |



 

## <a name="other-enumerations"></a>其他列舉

以下是驗證所使用的其他列舉。



| 列舉型別                                                   | 描述                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**身分識別 \_ 類型**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | 指定要列舉的身分識別類型。<br/>                                                                                                                                                                  |
| [**PKU2U \_ 登入 \_ 提交 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | 指出傳入 [**PKU2U \_ 憑證 \_ S4U \_ 登**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) 入結構的登入訊息類型。<br/>                                                                                |
| [**SECPKG \_ ATTR \_ LCT \_ 狀態**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | 指出最近呼叫 [**InitializeSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數的權杖是否為用戶端的最後一個 token。<br/>                               |
| [**SECPKG \_ 認證 \_ 類別**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | 指出用戶端內容中使用的認證類型。 [**SECPKG 認證 \_ \_ 類別**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)列舉用於 [**SecPkgCoNtext \_ CredInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo)結構中。<br/> |



 

 

