---
description: 設定或抓取識別碼的 CAPICOM 定義名稱。 這是預設屬性。
ms.assetid: 9a7c441d-e2c4-4c02-8910-b889f8a35e64
title: 老。Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42bd18c800bf53ca9edcf4cf72a4c7ac2cbb6933
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996316"
---
# <a name="oidname-property"></a>老。Name 屬性

\[[ **名稱** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請在 [**system.object**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)命名空間中使用 [**Oid 類別**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1)。\]

**Name** 屬性會設定或抓取此識別碼的 CAPICOM 定義名稱。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
OID.Name As CAPICOM_OID
```



## <a name="property-value"></a>屬性值

[**Capicom \_ OID**](capicom-oid.md)列舉的值，可提供 capicom 物件識別碼的名稱。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                                                                  | 意義                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_OID_OTHER"></span><span id="capicom_oid_other"></span><dl> <dt>**CAPICOM \_ OID \_ 其他**</dt> </dl>                                                                                                             | 物件不是其中一個預先定義的 CAPICOM 物件類型。<br/>                                                                                                                                                                       |
| <span id="CAPICOM_OID_AUTHORITY_KEY_IDENTIFIER_EXTENSION"></span><span id="capicom_oid_authority_key_identifier_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 授權單位 \_ 金鑰 \_ 識別碼 \_ 延伸**</dt> </dl>                   | 此物件是包含證書 [*頒發機構*](../secgloss/c-gly.md) 單位之公開金鑰識別碼的憑證延伸 (CA) 。<br/>                  |
| <span id="CAPICOM_OID_KEY_ATTRIBUTES_EXTENSION"></span><span id="capicom_oid_key_attributes_extension"></span><dl> <dt>**CAPICOM \_ OID 索引 \_ 鍵 \_ 屬性 \_ 延伸**</dt> </dl>                                                  | 物件是包含 [*公開金鑰*](../secgloss/p-gly.md)選用屬性的憑證延伸。<br/>                                                                      |
| <span id="CAPICOM_OID_CERT_POLICIES_95_EXTENSION"></span><span id="capicom_oid_cert_policies_95_extension"></span><dl> <dt>**CAPICOM \_ OID \_ CERT \_ 原則 \_ 95 \_ 擴充功能**</dt> </dl>                                           | 物件是包含舊版作業系統之 [*憑證原則*](../secgloss/c-gly.md) 資訊的憑證延伸。<br/>                             |
| <span id="CAPICOM_OID_KEY_USAGE_RESTRICTION_EXTENSION"></span><span id="capicom_oid_key_usage_restriction_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 金鑰 \_ 使用 \_ 限制 \_ 延伸模組**</dt> </dl>                            | 此物件是包含憑證 [*公開金鑰*](../secgloss/p-gly.md)使用限制的憑證延伸。<br/>                                                    |
| <span id="CAPICOM_OID_LEGACY_POLICY_MAPPINGS_EXTENSION"></span><span id="capicom_oid_legacy_policy_mappings_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 舊版 \_ 原則 \_ 對應 \_ 延伸模組**</dt> </dl>                         | 物件是包含舊版原則對應資訊的憑證延伸。<br/>                                                                                                                                              |
| <span id="CAPICOM_OID_SUBJECT_ALT_NAME_EXTENSION"></span><span id="capicom_oid_subject_alt_name_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 主體 \_ 替換 \_ 名稱 \_ 延伸模組**</dt> </dl>                                           | 物件是憑證延伸，包含憑證主體的替代名稱。<br/>                                                                                                                         |
| <span id="CAPICOM_OID_ISSUER_ALT_NAME_EXTENSION"></span><span id="capicom_oid_issuer_alt_name_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 簽發者 \_ 替換 \_ 名稱 \_ 延伸模組**</dt> </dl>                                              | 物件是憑證延伸，包含憑證簽發者的替代名稱。<br/>                                                                                                                          |
| <span id="CAPICOM_OID_BASIC_CONSTRAINTS_EXTENSION"></span><span id="capicom_oid_basic_constraints_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 基本 \_ 條件約束 \_ 延伸**</dt> </dl>                                         | 物件是憑證延伸，指出認證的主旨是否可作為 CA、終端實體或兩者。<br/>                                                                                                         |
| <span id="CAPICOM_OID_SUBJECT_KEY_IDENTIFIER_EXTENSION"></span><span id="capicom_oid_subject_key_identifier_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 主體 \_ 金鑰 \_ 識別碼 \_ 延伸**</dt> </dl>                         | 物件是憑證延伸，包含憑證主體的金鑰識別碼。<br/>                                                                                                                           |
| <span id="CAPICOM_OID_KEY_USAGE_EXTENSION"></span><span id="capicom_oid_key_usage_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 金鑰 \_ 使用方法 \_ 擴充功能**</dt> </dl>                                                                 | 物件是憑證延伸，包含憑證 [*公開金鑰*](../secgloss/p-gly.md)用途的相關資訊。<br/>                                         |
| <span id="CAPICOM_OID_PRIVATEKEY_USAGE_PERIOD_EXTENSION"></span><span id="capicom_oid_privatekey_usage_period_extension"></span><dl> <dt>**CAPICOM \_ OID \_ PRI加值稅EKEY \_ 使用 \_ 期間 \_ 延伸**</dt> </dl>                      | 物件是憑證延伸，包含憑證的 [*私密金鑰*](../secgloss/p-gly.md) 可供使用的時間週期相關資訊。<br/>                   |
| <span id="CAPICOM_OID_SUBJECT_ALT_NAME2_EXTENSION"></span><span id="capicom_oid_subject_alt_name2_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 主體 \_ ALT \_ NAME2 \_ 擴充功能**</dt> </dl>                                        | 物件是憑證延伸，包含憑證主體的替代名稱。<br/>                                                                                                                         |
| <span id="CAPICOM_OID_ISSUER_ALT_NAME2_EXTENSION"></span><span id="capicom_oid_issuer_alt_name2_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 簽發者 \_ ALT \_ NAME2 \_ 擴充功能**</dt> </dl>                                           | 物件是憑證延伸，包含憑證簽發者的替代名稱。<br/>                                                                                                                          |
| <span id="CAPICOM_OID_BASIC_CONSTRAINTS2_EXTENSION"></span><span id="capicom_oid_basic_constraints2_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 基本 \_ CONSTRAINTS2 \_ 延伸模組**</dt> </dl>                                      | 物件是憑證延伸，指出認證的主旨是否可作為 CA、終端實體或兩者。<br/>                                                                                                         |
| <span id="CAPICOM_OID_NAME_CONSTRAINTS_EXTENSION"></span><span id="capicom_oid_name_constraints_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 名稱 \_ 限制式 \_ 延伸**</dt> </dl>                                            | 物件是憑證延伸，其中包含明確允許或從信任中排除之憑證的相關資訊。<br/>                                                                                          |
| <span id="CAPICOM_OID_CRL_DIST_POINTS_EXTENSION"></span><span id="capicom_oid_crl_dist_points_extension"></span><dl> <dt>**CAPICOM \_ OID \_ CRL \_ DIST \_ 點 \_ 延伸**</dt> </dl>                                              | 物件是憑證延伸，包含用來更新 [*憑證撤銷清單*](../secgloss/c-gly.md) (CRL) 的資訊。<br/>       |
| <span id="CAPICOM_OID_CERT_POLICIES_EXTENSION"></span><span id="capicom_oid_cert_policies_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 憑證 \_ 原則 \_ 延伸**</dt> </dl>                                                     | 物件是憑證延伸，包含憑證支援的原則清單。<br/>                                                                                                                           |
| <span id="CAPICOM_OID_POLICY_MAPPINGS_EXTENSION"></span><span id="capicom_oid_policy_mappings_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 原則 \_ 對應 \_ 延伸模組**</dt> </dl>                                               | 物件是憑證延伸，可在不同網域中的原則之間提供對應。<br/>                                                                                                                                 |
| <span id="CAPICOM_OID_AUTHORITY_KEY_IDENTIFIER2_EXTENSION"></span><span id="capicom_oid_authority_key_identifier2_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 授權單位 \_ 金鑰 \_ IDENTIFIER2 \_ 延伸模組**</dt> </dl>                | 物件是包含 CA 之 [*公開金鑰*](../secgloss/p-gly.md) 識別碼的憑證延伸。<br/>                                                                      |
| <span id="CAPICOM_OID_POLICY_CONSTRAINTS_EXTENSION"></span><span id="capicom_oid_policy_constraints_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 原則 \_ 條件約束 \_ 延伸**</dt> </dl>                                      | 物件是憑證延伸，其中包含已建立的原則，可接受信任的憑證。<br/>                                                                                                                     |
| <span id="CAPICOM_OID_ENHANCED_KEY_USAGE_EXTENSION"></span><span id="capicom_oid_enhanced_key_usage_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 增強 \_ 金鑰 \_ 使用方法 \_ 擴充功能**</dt> </dl>                                     | 物件是憑證延伸，其中包含有關憑證 [*公開金鑰*](../secgloss/p-gly.md)用途的增強資訊。<br/>                                |
| <span id="CAPICOM_OID_CERTIFICATE_TEMPLATE_EXTENSION"></span><span id="capicom_oid_certificate_template_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 憑證 \_ 範本 \_ 延伸模組**</dt> </dl>                                | 此物件是包含憑證範本的憑證延伸。<br/>                                                                                                                                                         |
| <span id="CAPICOM_OID_APPLICATION_CERT_POLICIES_EXTENSION"></span><span id="capicom_oid_application_cert_policies_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 應用程式憑證 \_ \_ 原則 \_ 延伸**</dt> </dl>                | 物件是包含憑證之應用程式原則的憑證延伸。<br/>                                                                                                                                      |
| <span id="CAPICOM_OID_APPLICATION_POLICY_MAPPINGS_EXTENSION"></span><span id="capicom_oid_application_policy_mappings_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 應用程式 \_ 原則對應 \_ \_ 延伸模組**</dt> </dl>          | 物件是憑證延伸，包含不同應用程式原則之間的對應。<br/>                                                                                                                                |
| <span id="CAPICOM_OID_APPLICATION_POLICY_CONSTRAINTS_EXTENSION"></span><span id="capicom_oid_application_policy_constraints_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 應用程式 \_ 原則 \_ 條件約束 \_ 延伸**</dt> </dl> | 物件是包含憑證之應用程式原則條件約束的憑證延伸。<br/>                                                                                                                          |
| <span id="CAPICOM_OID_AUTHORITY_INFO_ACCESS_EXTENSION"></span><span id="capicom_oid_authority_info_access_extension"></span><dl> <dt>**CAPICOM \_ OID \_ 授權單位 \_ 資訊 \_ 存取 \_ 延伸模組**</dt> </dl>                            | 物件是憑證延伸，可指出如何存取憑證簽發者的 CA 資訊和服務。<br/>                                                                                                   |
| <span id="CAPICOM_OID_SERVER_AUTH_EKU"></span><span id="capicom_oid_server_auth_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 伺服器 \_ 驗證 \_ EKU**</dt> </dl>                                                                             | 物件是 [**EKU**](eku.md) 物件，指定憑證可以用來驗證服務器。<br/>                                                                                                                |
| <span id="CAPICOM_OID_CLIENT_AUTH_EKU"></span><span id="capicom_oid_client_auth_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 用戶端 \_ 驗證 \_ EKU**</dt> </dl>                                                                             | 物件是指定憑證可以用來驗證用戶端的 [**EKU**](eku.md) 物件。<br/>                                                                                                                |
| <span id="CAPICOM_OID_CODE_SIGNING_EKU"></span><span id="capicom_oid_code_signing_eku"></span><dl> <dt>**CAPICOM \_ OID 程式 \_ 代碼 \_ 簽署 \_ EKU**</dt> </dl>                                                                          | 物件是指定憑證可以用來建立數位簽章的 [**EKU**](eku.md) 物件。<br/>                                                                                                           |
| <span id="CAPICOM_OID_EMAIL_PROTECTION_EKU"></span><span id="capicom_oid_email_protection_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 電子郵件 \_ 保護 \_ EKU**</dt> </dl>                                                              | 物件是 [**EKU**](eku.md) 物件，可指定憑證可用於電子郵件保護。<br/>                                                                                                                    |
| <span id="CAPICOM_OID_IPSEC_END_SYSTEM_EKU"></span><span id="capicom_oid_ipsec_end_system_eku"></span><dl> <dt>**CAPICOM \_ OID \_ IPSEC \_ 終端 \_ 系統 \_ EKU**</dt> </dl>                                                             | 物件是指定憑證可用於 IPsec 終端系統的 [**EKU**](eku.md) 物件。<br/>                                                                                                                 |
| <span id="CAPICOM_OID_IPSEC_TUNNEL_EKU"></span><span id="capicom_oid_ipsec_tunnel_eku"></span><dl> <dt>**CAPICOM \_ OID \_ IPSEC \_ 通道 \_ EKU**</dt> </dl>                                                                          | 物件是指定憑證可用於 IPsec 通道的 [**EKU**](eku.md) 物件。<br/>                                                                                                                     |
| <span id="CAPICOM_OID_IPSEC_USER_EKU"></span><span id="capicom_oid_ipsec_user_eku"></span><dl> <dt>**CAPICOM \_ OID \_ IPSEC \_ 使用者 \_ EKU**</dt> </dl>                                                                                | 物件是指定憑證可用於 IPsec 使用者的 [**EKU**](eku.md) 物件。<br/>                                                                                                                       |
| <span id="CAPICOM_OID_TIME_STAMPING_EKU"></span><span id="capicom_oid_time_stamping_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 時間 \_ 戳 \_ EKU**</dt> </dl>                                                                       | 物件是指定憑證可用於時間戳記的 [**EKU**](eku.md) 物件。<br/>                                                                                                                       |
| <span id="CAPICOM_OID_CTL_USAGE_SIGNING_EKU"></span><span id="capicom_oid_ctl_usage_signing_eku"></span><dl> <dt>**CAPICOM \_ OID \_ CTL \_ 使用方式 \_ 簽署 \_ EKU**</dt> </dl>                                                          | 物件是 [**EKU**](eku.md) 物件，指定憑證可用來簽署憑證信任清單 (CTL) 。<br/>                                                                                                |
| <span id="CAPICOM_OID_TIME_STAMP_SIGNING_EKU"></span><span id="capicom_oid_time_stamp_signing_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 時間 \_ 戳 \_ 簽署 \_ EKU**</dt> </dl>                                                       | 物件是 [**EKU**](eku.md) 物件，可指定憑證可以用來簽署時間戳記。<br/>                                                                                                                    |
| <span id="CAPICOM_OID_SERVER_GATED_CRYPTO_EKU"></span><span id="capicom_oid_server_gated_crypto_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 伺服器 \_ 閘道 \_ 加密 \_ EKU**</dt> </dl>                                                    | 物件是指定憑證可用於 [*伺服器閘道加密*](../secgloss/s-gly.md) (SGC) 的 [**EKU**](eku.md)物件。<br/> |
| <span id="CAPICOM_OID_ENCRYPTING_FILE_SYSTEM_EKU"></span><span id="capicom_oid_encrypting_file_system_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 加密 \_ 檔 \_ 系統 \_ EKU**</dt> </dl>                                           | 物件是 [**EKU**](eku.md) 物件，指定憑證可用於 [*加密檔案系統*](../secgloss/e-gly.md) (EFS) 。<br/>          |
| <span id="CAPICOM_OID_EFS_RECOVERY_EKU"></span><span id="capicom_oid_efs_recovery_eku"></span><dl> <dt>**CAPICOM \_ OID \_ EFS \_ 復原 \_ EKU**</dt> </dl>                                                                          | 物件是 [**EKU**](eku.md) 物件，指定憑證可以用來復原 EFS。<br/>                                                                                                                 |
| <span id="CAPICOM_OID_WHQL_CRYPTO_EKU"></span><span id="capicom_oid_whql_crypto_eku"></span><dl> <dt>**CAPICOM \_ OID \_ WHQL \_ 加密 \_ EKU**</dt> </dl>                                                                             | 物件是 [**EKU**](eku.md) 物件，指定憑證可用於 WINDOWS 硬體品質實驗室 (WHQL) 密碼編譯。<br/>                                                                                   |
| <span id="CAPICOM_OID_NT5_CRYPTO_EKU"></span><span id="capicom_oid_nt5_crypto_eku"></span><dl> <dt>**CAPICOM \_ OID \_ NT5 \_ 加密 \_ EKU**</dt> </dl>                                                                                | 物件是 [**EKU**](eku.md) 物件，可指定憑證可用於 windows Server 2003 和 windows XP 密碼編譯。<br/>                                                                                     |
| <span id="CAPICOM_OID_OEM_WHQL_CRYPTO_EKU"></span><span id="capicom_oid_oem_whql_crypto_eku"></span><dl> <dt>**CAPICOM \_ OID \_ OEM \_ WHQL \_ 加密 \_ EKU**</dt> </dl>                                                                | 物件是一個 [**EKU**](eku.md) 物件，指定憑證可用於原始設備製造商 (OEM) Windows 硬體品質實驗室 (WHQL) 密碼編譯。<br/>                                             |
| <span id="CAPICOM_OID_EMBEDED_NT_CRYPTO_EKU"></span><span id="capicom_oid_embeded_nt_crypto_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 內嵌 \_ NT \_ 加密 \_ EKU**</dt> </dl>                                                          | 物件是 [**EKU**](eku.md) 物件，可指定憑證可用於某些舊版作業系統中的內嵌密碼編譯。<br/>                                                                           |
| <span id="CAPICOM_OID_ROOT_LIST_SIGNER_EKU"></span><span id="capicom_oid_root_list_signer_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 根 \_ 清單 \_ 簽署者 \_ EKU**</dt> </dl>                                                             | 物件是指定憑證可以用來簽署根清單的 [**EKU**](eku.md) 物件。<br/>                                                                                                                     |
| <span id="CAPICOM_OID_QUALIFIED_SUBORDINATION_EKU"></span><span id="capicom_oid_qualified_subordination_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 限定的 \_ 從屬 \_ EKU**</dt> </dl>                                         | 物件是 [**EKU**](eku.md) 物件，可指定憑證可用於限定的從屬。<br/>                                                                                                             |
| <span id="CAPICOM_OID_KEY_RECOVERY_EKU"></span><span id="capicom_oid_key_recovery_eku"></span><dl> <dt>**CAPICOM \_ OID \_ KEY \_ RECOVERY \_ EKU**</dt> </dl>                                                                          | 物件是 [**EKU**](eku.md) 物件，可指定憑證可用於金鑰修復。<br/>                                                                                                                        |
| <span id="CAPICOM_OID_DIGITAL_RIGHTS_EKU"></span><span id="capicom_oid_digital_rights_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 數位 \_ 版權 \_ EKU**</dt> </dl>                                                                    | 物件是指定憑證可用於數位版權的 [**EKU**](eku.md) 物件。<br/>                                                                                                                      |
| <span id="CAPICOM_OID_LICENSES_EKU"></span><span id="capicom_oid_licenses_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 授權 \_ EKU**</dt> </dl>                                                                                       | 物件是指定憑證可用於授權的 [**EKU**](eku.md) 物件。<br/>                                                                                                                            |
| <span id="CAPICOM_OID_LICENSE_SERVER_EKU"></span><span id="capicom_oid_license_server_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 授權 \_ 伺服器 \_ EKU**</dt> </dl>                                                                    | 物件是 [**EKU**](eku.md) 物件，可指定憑證可用於授權伺服器。<br/>                                                                                                                    |
| <span id="CAPICOM_OID_SMART_CARD_LOGON_EKU"></span><span id="capicom_oid_smart_card_logon_eku"></span><dl> <dt>**CAPICOM \_ OID \_ 智慧 \_ 卡 \_ 登入 \_ EKU**</dt> </dl>                                                             | 物件是 [**EKU**](eku.md) 物件，指定憑證可用於智慧卡登入。<br/>                                                                                                                    |
| <span id="CAPICOM_OID_PKIX_POLICY_QUALIFIER_CPS"></span><span id="capicom_oid_pkix_policy_qualifier_cps"></span><dl> <dt>**CAPICOM \_ OID \_ PKIX \_ 原則 \_ 限定詞 \_ CPS**</dt> </dl>                                              | 物件是 (CPS) 的認證實務聲明，可用於公開金鑰基礎結構 x.509 (PKIX) 原則限定詞。<br/>                                                                                            |
| <span id="CAPICOM_OID_PKIX_POLICY_QUALIFIER_USERNOTICE"></span><span id="capicom_oid_pkix_policy_qualifier_usernotice"></span><dl> <dt>**CAPICOM \_ OID \_ PKIX \_ 原則 \_ 限定詞 \_ USERNOTICE**</dt> </dl>                         | 物件是可用於公開金鑰基礎結構 X. x.509 (PKIX) 原則辨識符號的使用者通知。<br/>                                                                                                                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**老**](oid.md)
</dt> </dl>

 

 
