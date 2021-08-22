---
description: 列出驗證 Api 中使用的結構。
ms.assetid: 576f5dec-8bd5-4686-be68-30746de1d511
title: 驗證結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed42e076a92336a85e38435ed7be1064d7be024bf0c10fbb4c8823d64ecf0bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141381"
---
# <a name="authentication-structures"></a>驗證結構

驗證結構會根據使用方式進行分類，如下所示：

-   [SSPI 結構](#sspi-structures)
-   [Schannel 結構](#schannel-structures)
-   [自訂安全性套件結構](#custom-security-package-structures)
-   [網路提供者結構](#network-provider-structures)
-   [GINA 結構](#gina-structures)
-   [本地安全機構結構](#local-security-authority-structures)
-   [認證管理結構](#credentials-management-structures)
-   [智慧卡結構](#smart-card-structures)

## <a name="sspi-structures"></a>SSPI 結構

在 sspi 函式中使用下列結構（定義于 Sspi）。



| 結構                                                                   | 描述                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CREDSSP \_ 認證**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred)                                       | 指定 Schannel 和 Negotiate [*安全性封裝* 的驗證資料](/windows/desktop/SecGloss/s-gly)                                                                                      |
| [**秒的 \_ WINNT \_ 驗證身分 \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a)               | 用來將特定的使用者名稱和密碼傳遞至執行時間程式庫，以進行驗證。                                                                                                                                            |
| [**每秒 \_ WINNT \_ 驗證身分識別， \_ \_ 例如**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2)        | 包含使用者的相關資訊。 提供此結構的 ANSI 和 [*Unicode*](/windows/desktop/SecGloss/u-gly) 形式。                                                                                       |
| [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)                                              | 傳輸應用程式所配置以傳遞至 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)的緩衝區。                                                                                           |
| [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc)                                      | 要從傳輸應用程式傳遞至安全性封裝的 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) 結構陣列。                                                                                                                                         |
| [**SecPkgCoNtext \_ AccessToken**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_accesstoken)             | 包含 [*安全性內容*](/windows/desktop/SecGloss/s-gly)之存取權杖的控制碼。                                                                                                       |
| [**SecPkgCoNtext \_ ClientCreds**](/windows/desktop/api/Credssp/ns-credssp-secpkgcontext_clientcreds)             | 指定 [**(CredSSP)**](/windows/desktop/api/Sspi/nf-sspi-querycontextattributesa) 函數呼叫 QueryCoNtextAttributes 時的用戶端認證。                                                                                                                   |
| [**SecPkgCoNtext \_ ConnectionInfo**](/windows/desktop/api/Schannel/ns-schannel-secpkgcontext_connectioninfo)       | 包含通訊協定和密碼資訊。 [**QueryCoNtextAttributes (一般)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa)函數會使用此結構。                                                                                         |
| [**SecPkgCoNtext \_ CredentialName**](/windows/desktop/api/Sspi/ns-sspi-_secpkgcontext_credentialnamea)       | 指定認證名稱。                                                                                                                                                                                                                         |
| [**SecPkgCoNtext \_ DceInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_dceinfo)                     | 包含 DCE 服務所使用的授權資料。                                                                                                                                                                                                      |
| [**SecPkgCoNtext \_ EapKeyBlock**](/windows/desktop/api/Schannel/ns-schannel-secpkgcontext_eapkeyblock)             | 包含 EAP TLS 驗證通訊協定所使用的金鑰資料。                                                                                                                                                                                         |
| [**SecPkgCoNtext \_ 旗標**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_flags)                         | 包含安全性內容中之旗標的相關資訊。                                                                                                                                                                                          |
| [**SecPkgCoNtext \_ IssuerListInfoEx**](/windows/desktop/api/Schannel/ns-schannel-secpkgcontext_issuerlistinfoex)   | 包含受信任的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位清單， (CAs) 。                                                                                            |
| [**SecPkgCoNtext \_ 生命週期**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_lifespan)                   | 表示安全性內容的存留期範圍。                                                                                                                                                                                                         |
| [**SecPkgCoNtext \_ 名稱**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_namesa)                         | 包含與安全性內容相關聯之使用者的名稱。                                                                                                                                                                                      |
| [**SecPkgCoNtext \_ NativeNames**](/windows/desktop/api/Sspi/ns-sspi-_secpkgcontext_nativenamesa)             | 包含來自輸出票證的用戶端和伺服器主體名稱。                                                                                                                                                                               |
| [**SecPkgCoNtext \_ NegotiationInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_negotiationinfoa)     | 包含已設定或已設定之 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 的相關資訊。 它也會提供協商的狀態來設定安全性封裝。 |
| [**SecPkgCoNtext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)             | 包含 (SSP) 之 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) 的名稱。                                                                                            |
| [**SecPkgCoNtext \_ PasswordExpiry**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_passwordexpiry)       | 包含密碼或其他認證到期的相關資訊。                                                                                                                                                                           |
| [**SecPkgCoNtext \_ setsessionkey**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sessionkey)               | 包含工作階段金鑰的相關資訊。                                                                                                                                                                                                            |
| [**SecPkgCoNtext \_ 大小**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes)                         | 包含訊息支援函式中所使用之重要結構的大小。                                                                                                                                                                      |
| [**SecPkgCoNtext \_ StreamSizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes)             | 包含要與訊息支援函式搭配使用之各種資料流程屬性的大小。                                                                                                                                                        |
| [**SecPkgCoNtext \_ TargetInformation**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_targetinformation) | 包含用於安全性內容之認證的相關資訊。                                                                                                                                                                               |
| [**SecPkgCredentials \_ 名稱**](/windows/desktop/api/Sspi/ns-sspi-secpkgcredentials_namesa)                 | 保存與 [*內容*](/windows/desktop/SecGloss/c-gly)相關聯之使用者的名稱。                                                                                                                                  |
| [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)                                            | 提供 [*安全性套件*](/windows/desktop/SecGloss/s-gly)的一般資訊，例如其名稱和功能。                                                                            |
| [**安全性 \_ 整數**](/windows/desktop/api/Sspi/ns-sspi-security_integer)                               | 保存數值的結構。 它是用來定義其他類型。                                                                                                                                                                                 |
| [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea)                      | 分派資料表，包含 SSPI 中定義之函式的指標。                                                                                                                                                                                |



 

## <a name="schannel-structures"></a>Schannel 結構

下列結構已定義為搭配 Schannel 使用。



| 結構                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**.SCH \_ 認證 \_ 公用 \_ CERTCHAIN**](/windows/desktop/api/Schannel/ns-schannel-sch_cred_public_certchain)         | 包含單一憑證。 您可以從這個憑證建立憑證連結。                                                                                                                                                                                                                                                                                           |
| [**.SCH \_ 認證 \_ 秘密 \_ PRIVKEY**](/windows/desktop/api/Schannel/ns-schannel-sch_cred_secret_privkey)             | 包含驗證用戶端或伺服器所需的 [*私密金鑰*](/windows/desktop/SecGloss/p-gly) 資訊。                                                                                                                                                                                                                                |
| [**SCHANNEL \_ CERT \_ HASH**](/windows/desktop/api/Schannel/ns-schannel-schannel_cert_hash)                        | 包含 Schannel 使用之憑證的雜湊存放區資料。                                                                                                                                                                                                                                                                                                               |
| [**SCHANNEL \_ CERT \_ HASH \_ STORE**](/windows/desktop/api/Schannel/ns-schannel-schannel_cert_hash_store)           | 包含 Schannel 在核心模式中使用之憑證的雜湊存放區資料。                                                                                                                                                                                                                                                                                                |
| [**SCHANNEL \_ 警示 \_ 權杖**](/windows/desktop/api/Schannel/ns-schannel-schannel_alert_token)                    | 產生 [安全通訊端層通訊協定](secure-sockets-layer-protocol.md) (SSL) 或傳輸層安全性通訊協定 (TSL) 警示傳送至 [**InitializeSecurityCoNtext (schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) 函式或 [**AcceptSecurityCoNtext (schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式的呼叫目標。 |
| [**SCHANNEL \_ 用戶端簽章 \_**](/windows/desktop/api/Schannel/ns-schannel-schannel_client_signature)          | 當呼叫 [**InitializeSecurityCoNtext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) 函式無法存取用戶端憑證的私密金鑰時，指定用戶端簽章 (在此案例中，此函式會傳回) **\_ \_ \_ 所需的秒** 數。                                                                                                           |
| [**SCHANNEL \_ 認證**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred)                                   | 包含 Schannel 認證的資料。                                                                                                                                                                                                                                                                                                                                      |
| [**SCHANNEL \_ 會話 \_ 權杖**](/windows/desktop/api/Schannel/ns-schannel-schannel_session_token)                | 指定是否啟用透過呼叫 [**InitializeSecurityCoNtext (schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) 函數或 [**AcceptSecurityCoNtext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式所建立之驗證會話的重新開機。                                                                                |
| [**SecPkgCoNtext \_ 授權單位**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_authoritya)               | 包含驗證授權單位的名稱（如果有的話）。 它可以是 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 或驗證連線的伺服器或網域的名稱。                                                                                               |
| [**SecPkgCoNtext \_ ConnectionInfo**](/windows/desktop/api/Schannel/ns-schannel-secpkgcontext_connectioninfo)     | 包含通訊協定和密碼資訊。 [**QueryCoNtextAttributes (一般)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa)函數會使用此結構。                                                                                                                                                                                                                     |
| [**SecPkgCoNtext \_ IssuerListInfoEx**](/windows/desktop/api/Schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | 包含受信任的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly)單位清單。                                                                                                                                                                                                                              |
| [**SecPkgCoNtext \_ KeyInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_keyinfoa)                   | 包含有關 [*安全性內容*](/windows/desktop/SecGloss/s-gly)中所使用 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)的資訊。 此結構已由 [**SecPkgCoNtext \_ ConnectionInfo**](/windows/desktop/api/Schannel/ns-schannel-secpkgcontext_connectioninfo) 結構取代。                       |
| [**SecPkgCoNtext \_ ProtoInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_protoinfoa)               | 保存使用中通訊協定的相關資訊。                                                                                                                                                                                                                                                                                                                                       |
| [**SecPkgCoNtext \_ SessionAppData**](/windows/desktop/api/Schannel/ns-schannel-secpkgcontext_sessionappdata)     | 儲存會話內容的應用程式資料。                                                                                                                                                                                                                                                                                                                                     |
| [**SecPkgCred \_ CipherStrengths**](/previous-versions/windows/desktop/legacy/aa380101(v=vs.85))         | 保留指定之 Schannel 認證所使用的加密所允許的最小和最大強度。                                                                                                                                                                                                                                                                         |
| [**SecPkgCred \_ SupportedAlgs**](/previous-versions/windows/desktop/legacy/aa380102(v=vs.85))             | 包含指定之 Schannel 認證所允許之演算法的識別碼。                                                                                                                                                                                                                                                                                                |
| [**SecPkgCred \_ SupportedProtocols**](/previous-versions/windows/desktop/legacy/aa380103(v=vs.85))   | 指出指定的安全通道認證所允許的通訊協定。                                                                                                                                                                                                                                                                                                            |
| [**X509Certificate**](/windows/desktop/api/Schannel/ns-schannel-x509certificate)                                | 代表 [*x.509*](/windows/desktop/SecGloss/x-gly) 憑證。                                                                                                                                                                                                                                                                                       |



 

## <a name="custom-security-package-structures"></a>自訂安全性套件結構

自訂 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 使用下列結構。



| 結構                                                                   | 描述                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LSA \_ SECPKG \_ 函數 \_ 表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table)           | 「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) 」之指標的表格， (自訂安全性封裝可呼叫的 LSA) 函數。 |
| [**SECPKG \_ 呼叫 \_ 資訊**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_call_info)                              | 包含執行中函式呼叫的相關資訊。                                                                                                                                                        |
| [**SECPKG \_ 用戶端 \_ 資訊**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_client_info)                          | 包含安全性封裝使用者的相關資訊。                                                                                                                                                    |
| [**SECPK \_ 內容 \_ THUNK**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_context_thunks)                     | 包含將與 LSA 一起執行之安全性封裝呼叫的相關資訊。                                                                                                       |
| [**SECPKG \_ DLL 函式 \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_dll_functions)                      | 包含可供自訂安全性封裝在用戶端/伺服器應用程式中執行的功能。                                                                                           |
| [**SECPKG \_ 事件 \_ 網域 \_ 變更**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_parameters)                  | 包含 [*會話*](/windows/desktop/SecGloss/s-gly) 和電腦資訊。 此結構名稱是 [**SECPKG \_ 參數**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_parameters) 結構的別名。 |
| [**SECPKG \_ 事件 \_ 通知**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_event_notify)                        | 包含有關安全性相關事件的資訊。                                                                                                                                                          |
| [**SECPKG \_ 事件 \_ 封裝 \_ 變更**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_event_package_change)       | 包含安全性封裝可用性和使用的相關資訊。                                                                                                                                             |
| [**SECPKG \_ 擴充 \_ 資訊**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_extended_information)        | 包含有關安全性封裝的延伸資訊。                                                                                                                                                     |
| [**SECPKG 函式 \_ \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table)                    | 包含安全性封裝所執行之函式的指標。                                                                                                                                          |
| [**SECPKG \_ GSS \_ 資訊**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_gss_info)                                | 包含用來識別安全性封裝之 GSS OID 的資訊。                                                                                                                                      |
| [**SECPKG \_ 相互 \_ 驗證 \_ 層級**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_mutual_auth_level)             | 包含安全性封裝所使用之相互驗證層級的相關資訊。                                                                                                                        |
| [**SECPKG \_ 參數**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_parameters)                             | 包含 [*會話*](/windows/desktop/SecGloss/s-gly) 和電腦資訊。                                                                                                     |
| [**SECPKG \_ 主要 \_ 認證**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_primary_cred)                        | 包含 [*主要認證*](/windows/desktop/SecGloss/p-gly) 資訊。                                                                             |
| [**SECPKG \_ 補充 \_ 認證**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplemental_cred)              | 包含 [*補充認證*](/windows/desktop/SecGloss/s-gly) 資訊。                                                              |
| [**SECPKG \_ 補充 \_ 認證 \_ 陣列**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplemental_cred_array) | 包含補充認證資訊。                                                                                                                                                                |
| [**SECPKG \_ 使用者 \_ 函數 \_ 表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_user_function_table)         | 包含由用戶端/伺服器應用程式在進程中載入之安全性封裝所執行的函式。                                                                                                   |
| [**SecurityUserData**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-security_user_data)                                | 包含已登入使用者的相關資訊。                                                                                                                                                                |



 

## <a name="network-provider-structures"></a>網路提供者結構

網路提供者 Api 和相關函數會使用下列結構。



| 結構                                            | 描述                                                                  |
|------------------------------------------------------|------------------------------------------------------------------------------|
| [**NETCONNECTINFOSTRUCT**](/windows/desktop/api/Winnetwk/ns-winnetwk-netconnectinfostruct) | 包含網路連接效能的相關資訊。          |
| [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea)                   | 包含列舉網路資源的相關資訊。                   |
| [**NOTIFYADD**](/windows/desktop/api/Npapi/ns-npapi-notifyadd)                       | 包含網路連接操作的詳細資料。                         |
| [**NOTIFYCANCEL**](/windows/desktop/api/Npapi/ns-npapi-notifycancel)                 | 包含網路中斷線上作業的詳細資料。                      |
| [**NOTIFYINFO**](/windows/desktop/api/Npapi/ns-npapi-notifyinfo)                     | 包含網路連線或中斷線上作業的相關狀態資訊。 |
| [**遠端 \_ 名稱 \_ 資訊**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa)       | 包含遠端通用名稱的相關資訊。                          |
| [**通用 \_ 名稱 \_ 資訊**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) | 包含區域通用名稱。                                             |



 

## <a name="gina-structures"></a>GINA 結構

[*GINA*](/windows/desktop/SecGloss/g-gly) 介面函式和 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 支援函數會使用下列結構。



| 結構                                                                                       | 描述                                                                                               |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**WLX \_ 用戶端 \_ 認證 \_ 資訊 \_ V1 \_ 0**](/windows/win32/api/winwlx/ns-winwlx-wlx_client_credentials_info_v1_0)               | 包含用戶端認證資訊。                                                                   |
| [**WLX \_ CONSOLESWITCH \_ 認證 \_ 資訊 \_ V1 \_ 0**](/windows/win32/api/winwlx/ns-winwlx-wlx_consoleswitch_credentials_info_v1_0) | 包含用戶端認證，允許以透明方式將認證傳送至目標會話。 |
| [**WLX \_ 桌面**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_desktop)                                                             | 包含桌面資訊。                                                                             |
| [**WLX \_ 分派 \_ 版本 \_ 1 \_ 0**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_0)                                | 包含 Winlogon （1.0 版分派資料表）。                                                        |
| [**WLX \_ 分派 \_ \_ 第 1 \_ 版**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_1)                                | 包含 Winlogon （1.1 版分派資料表）。                                                        |
| [**WLX \_ 分派 \_ \_ 第 1 \_ 版**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_2)                                | 包含 Winlogon （1.2 版分派資料表）。                                                        |
| [**WLX \_ 分派 \_ \_ 第 1 \_ 版**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3)                                | 包含 Winlogon （1.3 版分派資料表）。                                                        |
| [**WLX \_ 分派 \_ \_ 第 1 \_ 版**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_4)                                | 包含 Winlogon （1.4 版分派資料表）。                                                        |
| [**WLX \_ MPR \_ 通知 \_ 資訊**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info)                                           | 包含驗證和識別資訊。                                                   |
| [**WLX \_ 設定檔 \_ V1 \_ 0**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_profile_v1_0)                                                 | 包含用來設定初始環境的資訊。                                         |
| [**WLX \_ 設定檔 \_ V2 \_ 0**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_profile_v2_0)                                                 | 包含用來設定初始環境的資訊。                                         |
| [**WLX \_ 終端機 \_ 服務 \_ 資料**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_terminal_services_data)                             | 包含終端機服務設定檔路徑和主目錄資訊。                               |



 

## <a name="local-security-authority-structures"></a>本地安全機構結構

[*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 使用下列結構。



| 結構                                                                                    | 描述                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**網域 \_ 密碼 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-domain_password_information)                         | 包含網域密碼原則的相關資訊，例如密碼的最小長度以及密碼的唯一長度。                                                                                                                                                                                                   |
| [**KERB \_ 新增 \_ 認證 \_ 要求**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_add_credentials_request)                      | 指定要新增、移除或取代登入會話之額外伺服器認證的訊息。<br/>                                                                                                                                                                                                                           |
| [**KERB \_ 新增 \_ 認證 \_ 要求， \_ 例如**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_add_credentials_request_ex)               | 指定要新增、移除或取代登入會話的額外伺服器認證的訊息，以及與該認證相關聯的 [*服務主體名稱*](/windows/desktop/SecGloss/s-gly) (spn) 。<br/>                                                     |
| [**KERB \_ 憑證 \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)                                   | 包含智慧卡 [*登入會話*](/windows/desktop/SecGloss/l-gly)的相關資訊。                                                                                                                                                                                                  |
| [**KERB \_ 憑證 \_ 解除鎖定 \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_unlock_logon)                    | 包含用來解除鎖定在互動式智慧卡 [*登入會話*](/windows/desktop/SecGloss/l-gly)期間鎖定之工作站的資訊。                                                                                                                                  |
| [**KERB \_ CHANGEPASSWORD \_ 要求**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_changepassword_request)                         | 包含用來變更密碼的資訊。                                                                                                                                                                                                                                                                                     |
| [**KERB \_ 加密 \_ 金鑰**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_crypto_key)                                                 | 包含 [*Kerberos*](/windows/desktop/SecGloss/k-gly) 密碼編譯 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)的相關資訊。                                                                                                        |
| [**KERB \_ 外部 \_ 名稱**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_external_name)                                           | 包含外部名稱的相關資訊。                                                                                                                                                                                                                                                                                        |
| [**KERB \_ 外部 \_ 票證**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_external_ticket)                                       | 包含外部票證的相關資訊。                                                                                                                                                                                                                                                                                      |
| [**KERB \_ 互動式 \_ 登錄**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_interactive_logon)                                   | 包含互動式 [*登錄會話*](/windows/desktop/SecGloss/l-gly)的相關資訊。                                                                                                                                                                                                |
| [**KERB \_ 互動 \_ 設定檔**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_interactive_profile)                               | 包含互動式登入設定檔的相關資訊。                                                                                                                                                                                                                                                                            |
| [**KERB \_ 互動式 \_ 解除鎖定 \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_interactive_unlock_logon)                    | 包含用來解除鎖定在互動式 [*登錄會話*](/windows/desktop/SecGloss/l-gly)期間鎖定之工作站的資訊。                                                                                                                                             |
| [**KERB \_ 清除 \_ TKT 快取 \_ \_ 要求**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_purge_tkt_cache_request)                     | 包含用來刪除票證快取專案的資訊。                                                                                                                                                                                                                                                                  |
| [**KERB \_ QUERY \_ TKT \_ CACHE \_ 要求**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_query_tkt_cache_request)                     | 用來針對指定的使用者登入會話，取得所有快取票證的相關資訊。                                                                                                                                                                                                                                  |
| [**KERB \_ QUERY \_ TKT 快取 \_ \_ 回應**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_query_tkt_cache_response)                   | 包含查詢票證快取的結果。                                                                                                                                                                                                                                                                                  |
| [**KERB \_ 取出 \_ TKT \_ 要求**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_retrieve_tkt_request)                            | 包含用來取出票證的資訊。                                                                                                                                                                                                                                                                                     |
| [**KERB \_ 取得 \_ TKT \_ 回應**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_retrieve_tkt_response)                          | 包含抓取票證的回應。                                                                                                                                                                                                                                                                                     |
| [**KERB \_ S4U \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_s4u_logon)                                                   | 包含使用者 (S4U) [*登入會話*](/windows/desktop/SecGloss/l-gly)的服務相關資訊。                                                                                                                                                                                      |
| [**KERB \_ 智慧卡 \_ CSP \_ 資訊**](kerb-smartcard-csp-info.md)                                | 包含智慧卡 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) (CSP) 的相關資訊。                                                                                                                                         |
| [**KERB \_ 智慧 \_ 卡 \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_smart_card_logon)                                    | 包含智慧卡 [*登入會話*](/windows/desktop/SecGloss/l-gly)的相關資訊。                                                                                                                                                                                                  |
| [**KERB \_ 智慧 \_ 卡 \_ 解除鎖定 \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_smart_card_unlock_logon)                     | 包含用來解除鎖定智慧卡 [*登入會話*](/windows/desktop/SecGloss/l-gly)期間鎖定之工作站的資訊。                                                                                                                                               |
| [**KERB \_ 票證快取 \_ \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_ticket_cache_info)                                  | 包含快取的 Kerberos 票證的相關資訊。                                                                                                                                                                                                                                                                                |
| [**KERB \_ 票證 \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_ticket_logon)                                             | 包含網路登入的設定檔資訊。                                                                                                                                                                                                                                                                                   |
| [**KERB \_ 票證 \_ 設定檔**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_ticket_profile)                                         | 包含互動式登入設定檔的相關資訊。                                                                                                                                                                                                                                                                            |
| [**KERB \_ 票證 \_ 解除鎖定 \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_ticket_unlock_logon)                              | 包含解除鎖定工作站的資訊。                                                                                                                                                                                                                                                                                       |
| [**LSA \_ 分派 \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_dispatch_table)                                           | Windows [*驗證封裝*](/windows/desktop/SecGloss/a-gly)可呼叫的 LSA 函式之指標的表格。                                                                                                                                               |
| [**LSA \_ 字串**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_string)                                                            | 包含 ANSI 字串及其長度資訊。                                                                                                                                                                                                                                                                                 |
| [**LSA \_ 樹系 \_ 信任 \_ 二進位 \_ 資料**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_forest_trust_binary_data)                     | 包含在 LSA 樹系信任作業中使用的二進位資料。                                                                                                                                                                                                                                                                           |
| [**LSA \_ 樹系 \_ 信任 \_ 衝突 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_forest_trust_collision_information) | 包含 LSA 樹系信任衝突的相關資訊。                                                                                                                                                                                                                                                                             |
| [**LSA \_ 樹系 \_ 信任 \_ 記錄**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_forest_trust_record)                                | 包含 LSA 樹系信任衝突的相關資訊。                                                                                                                                                                                                                                                                           |
| [**LSA \_ 樹系 \_ 信任 \_ 網域 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_forest_trust_domain_info)                     | 包含網域的識別資訊。                                                                                                                                                                                                                                                                                      |
| [**LSA \_ 樹系 \_ 信任 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_forest_trust_information)                      | 包含 LSA 樹系信任資訊。                                                                                                                                                                                                                                                                                              |
| [**LSA \_ 樹系 \_ 信任 \_ 記錄**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_forest_trust_record)                                | 包含 LSA 樹系信任記錄。                                                                                                                                                                                                                                                                                                |
| [**LSA \_ TOKEN \_ 資訊 \_ Null**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_token_information_null)                          | 在需要非驗證系統存取的情況下使用。 此結構沒有任何內容。                                                                                                                                                                                                                                    |
| [**LSA \_ TOKEN \_ 資訊 \_ V1**](/previous-versions/windows/desktop/legacy/aa378721(v=vs.85))                              | 包含驗證封裝可放置在第1版 Windows token 物件中的資訊。                                                                                                                                                                                                                                  |
| [**MSV1 \_ 0 \_ CHANGEPASSWORD \_ 要求**](msv1-0-changepassword-request.md)                    | 已過時。                                                                                                                                                                                                                                                                                                                           |
| [**MSV1 \_ 0 \_ CHANGEPASSWORD \_ 回應**](msv1-0-changepassword-response.md)                  | 已過時。                                                                                                                                                                                                                                                                                                                           |
| [**MSV1 \_ 0 \_ ENUMUSERS \_ 要求**](msv1-0-enumusers-request.md)                              | 已過時。                                                                                                                                                                                                                                                                                                                           |
| [**MSV1 \_ 0 \_ ENUMUSERS \_ 回應**](msv1-0-enumusers-response.md)                            | 已過時。                                                                                                                                                                                                                                                                                                                           |
| [**MSV1 \_ 0 \_ GETUSERINFO \_ 要求**](msv1-0-getuserinfo-request.md)                          | 已過時。                                                                                                                                                                                                                                                                                                                           |
| [**MSV1 \_ 0 \_ GETUSERINFO \_ 回應**](msv1-0-getuserinfo-response.md)                        | 已過時。                                                                                                                                                                                                                                                                                                                           |
| [**MSV1 \_ 0 \_ 互動式 \_ 登錄**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-msv1_0_interactive_logon)                              | 包含互動式登入的使用者登入資訊。                                                                                                                                                                                                                                                                           |
| [**MSV1 \_ 0 \_ 互動 \_ 設定檔**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-msv1_0_interactive_profile)                          | 包含互動式登入設定檔的相關資訊。                                                                                                                                                                                                                                                                            |
| [**MSV1 \_ 0 \_ LM20 \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-msv1_0_lm20_logon)                                            | 包含網路登入中使用的登入資訊。                                                                                                                                                                                                                                                                                  |
| [**MSV1 \_ 0 \_ LM20 \_ 登入 \_ 設定檔**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-msv1_0_lm20_logon_profile)                           | 包含網路登入會話的相關資訊。                                                                                                                                                                                                                                                                                 |
| [**MSV1 \_ 0 \_ SUBAUTH \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-msv1_0_subauth_logon)                                      | 由 [*子驗證*](/windows/desktop/SecGloss/s-gly) dll 使用。                                                                                                                                                                                                 |
| [**MSV1 \_ 0 \_ SUBAUTH \_ 要求**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-msv1_0_subauth_request)                                  | 包含要傳遞至 [*子驗證封裝*](/windows/desktop/SecGloss/s-gly)的資訊。                                                                                                                                                                    |
| [**MSV1 \_ 0 \_ SUBAUTH \_ 回應**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-msv1_0_subauth_response)                                | 包含 [*子驗證封裝*](/windows/desktop/SecGloss/s-gly)的回應。                                                                                                                                                                         |
| [**MSV1 \_ 0 \_ 補充 \_ 認證**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-msv1_0_supplemental_credential)                  | 用來[](/windows/desktop/SecGloss/c-gly) \_ 從 Kerberos 或自訂驗證套件將認證傳遞至 MSV1 0。                                                                                                                                                                      |
| [**NETLOGON \_ 登入身分 \_ 識別 \_ 資訊**](/windows/desktop/api/Subauth/ns-subauth-netlogon_logon_identity_info)                      | 由 [**Msv1 \_ 0SubAuthenticationRoutine**](/windows/desktop/api/Subauth/nf-subauth-msv1_0subauthenticationroutine) 和 [**Msv1 \_ 0SubAuthenticationFilter**](/windows/desktop/api/Subauth/nf-subauth-msv1_0subauthenticationfilter) 用來傳遞使用者登入 [*子驗證*](/windows/desktop/SecGloss/s-gly)的相關資訊。 |
| [**舊的 \_ 大型 \_ 整數**](/windows/desktop/api/Subauth/ns-subauth-old_large_integer)                                             | 用來將64位帶正負號的整數值表示為 2 32 位整數。                                                                                                                                                                                                                                                             |
| [**配額 \_ 限制**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)                                                        | 描述使用者可用的系統資源數量。                                                                                                                                                                                                                                                                       |
| [**SR \_ 安全 \_ 描述項**](/windows/desktop/api/Subauth/ns-subauth-sr_security_descriptor)                                   | 包含使用者安全性 [*許可權*](/windows/desktop/SecGloss/p-gly) 的資訊。                                                                                                                                                                                                    |
| [**使用者 \_ 所有 \_ 資訊**](/windows/desktop/api/Subauth/ns-subauth-user_all_information)                                       | 包含會話使用者的資訊。 搭配 [*子驗證套件*](/windows/desktop/SecGloss/s-gly)使用。                                                                                                                                                 |



 

## <a name="credentials-management-structures"></a>認證管理結構

認證管理 API 包括下列結構。



| 結構                                                                     | 描述                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CERT \_ 認證 \_ 資訊**](/windows/desktop/api/WinCred/ns-wincred-cert_credential_info)                        | 包含憑證的參考。                                                                                                                                                                                               |
| [**憑據**](/windows/desktop/api/WinCred/ns-wincred-credentiala)                                              | 包含個別的認證。                                                                                                                                                                                                   |
| [**CREDENTIAL \_ 屬性**](/windows/desktop/api/WinCred/ns-wincred-credential_attributea)                         | 包含認證的應用程式定義屬性。                                                                                                                                                                         |
| [**認證 \_ 目標 \_ 資訊**](/windows/desktop/api/WinCred/ns-wincred-credential_target_informationa)      | 包含目的電腦的名稱、網域和樹狀目錄。                                                                                                                                                                               |
| [**CREDUI \_ 資訊**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa)                                           | 控制認證管理對話方塊的外觀。                                                                                                                                                                  |
| [**使用者名稱 \_ 目標 \_ 認證 \_ 資訊**](/windows/desktop/api/WinCred/ns-wincred-username_target_credential_info) | 包含認證的參考。 此結構是用來將使用者名稱傳遞至 [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) 函式，並從 [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala)傳遞。 |



 

## <a name="smart-card-structures"></a>智慧卡結構

智慧卡提供下列結構。



| 結構                                                      | 描述                                                                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**OPENCARD \_ 搜尋 \_ 準則**](/windows/desktop/api/Winscard/ns-winscard-opencard_search_criteriaa) | 提供 [**SCardUIDlgSelectCard**](/windows/desktop/api/Winscard/nf-winscard-scarduidlgselectcarda) 函數所使用的特定搜尋資訊。 |
| [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea)                           | 提供 [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) 函數所使用的資訊。                           |
| [**OPENCARDNAME \_ EX**](/windows/desktop/api/Winscard/ns-winscard-opencardname_exa)                    | 提供 [**SCardUIDlgSelectCard**](/windows/desktop/api/Winscard/nf-winscard-scarduidlgselectcarda) 函數所使用的資訊。                 |
| [**捨棄 \_ ATRMASK**](/windows/desktop/api/Winscard/ns-winscard-scard_atrmask)                        | 使用 [**SCardLocateCardsByATR**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsbyatra)尋找卡片。                                     |
| [**捨棄 \_ IO \_ 要求**](scard-io-request.md)                 | 開始通訊協定控制資訊結構。                                                                |
| [**捨棄 \_ READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea)                | 追蹤讀卡機內的智慧卡。                                                                             |



 

 

