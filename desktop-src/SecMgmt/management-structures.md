---
description: 列出與安全性管理 Api 搭配使用的結構。
ms.assetid: 8df25095-a215-464a-abac-39a6ea05f6a3
title: 安全性管理結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2212332b65d89a8d2c1f5a24601a59cca041ff42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980469"
---
# <a name="security-management-structures"></a>安全性管理結構

本章節包含下列結構群組的參考頁面：

-   [LSA 原則管理結構](#lsa-policy-management-structures)
-   [附件結構](#attachment-structures)
-   [更安全的結構](#safer-structures)

## <a name="lsa-policy-management-structures"></a>LSA 原則管理結構

[*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 原則管理功能使用下列結構。



| 結構                                                                       | Description                                                                                                                                   |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**LSA \_ 驗證 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_auth_information)                          | 包含受信任網域的驗證資訊。                                                                                     |
| [**LSA \_ 列舉 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_enumeration_information)            | 包含 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (SID) 的指標。    |
| [**LSA \_ 物件 \_ 屬性**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_object_attributes)                        | 指定與 [**原則**](policy-object.md) 物件之連接的屬性。                                                       |
| [**LSA \_ 參考的 \_ 定義域 \_ 清單**](/windows/win32/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list)             | 包含查閱作業中所參考之網域的相關資訊。                                                                      |
| [**LSA \_ 轉譯 \_ 名稱**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_name)                            | 包含 SID 所識別之帳戶的相關資訊。                                                                                   |
| [**LSA \_ 轉譯的 \_ SID**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_translated_sid)                              | 包含識別帳戶之 SID 的相關資訊。                                                                                |
| [**LSA \_ 轉譯 \_ SID2**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_sid2)                            | 包含識別帳戶之 SID 的相關資訊。                                                                                |
| [**LSA \_ 信任 \_ 資訊**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)                        | 識別網域。                                                                                                                          |
| [**LSA \_ UNICODE \_ 字串**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string)                              | 包含字串及其長度資訊。                                                                                                 |
| [**原則 \_ 帳戶 \_ 網域 \_ 資訊**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_account_domain_info)             | 用來設定和查詢系統帳戶網域的名稱和 SID。                                                                        |
| [**原則 \_ 審核 \_ 事件 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_audit_events_info)                 | 用來設定和查詢系統的審核規則。                                                                                            |
| [**原則 \_ DNS \_ 網域 \_ 資訊**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info)                     | 用來設定和查詢網域名稱系統 (DNS) 與 [**原則**](policy-object.md) 物件相關聯之主域的相關資訊。 |
| [**原則 \_ LSA \_ 伺服器 \_ 角色 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_lsa_server_role_info)          | 用來設定及查詢 LSA 伺服器的角色。                                                                                              |
| [**\_修改原則 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_modification_info)                  | 用來查詢有關 LSA 資料庫的建立時間和上次修改的資訊。                                                  |
| [**原則 \_ PD \_ 帳戶 \_ 資訊**](policy-pd-account-info.md)                     | 已過時。 工作站會使用工作站名稱，後面接著 $ 做為帳戶名稱。                                                          |
| [**原則 \_ 主域 \_ \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_primary_domain_info)             | 已過時。 請改用 **PolicyDnsDomainInformation** 和 [**原則 \_ DNS \_ 網域 \_ 資訊**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info) 結構。           |
| [**受信任的 \_ 網域 \_ 驗證 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_auth_information)   | 用來取得受信任網域的驗證資訊。                                                                             |
| [**受信任的 \_ 網域 \_ 完整 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_full_information)   | 用來取得受信任網域的完整資訊。                                                                                 |
| [**信任的 \_ 網域 \_ 資訊 \_ 基本**](/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)) | 受信任網域的相關資訊。 此結構與 [**LSA \_ 信任 \_ 資訊**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)相同。                  |
| [**受信任的 \_ 網域 \_ 資訊， \_ 例如**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_information_ex)       | 用來取得受信任網域的延伸資訊。                                                                                 |
| [**受信任的 \_ 功能變數名稱 \_ \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_name_info)                 | 用來查詢或設定受信任網域的名稱。                                                                                            |
| [**受信任的 \_ 密碼 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_password_info)                        | 用來查詢或設定受信任網域的密碼。                                                                                       |
| [**受信任的 \_ POSIX \_ 位移 \_ 資訊**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_posix_offset_info)               | 用來查詢或設定用來產生 Posix 使用者和群組識別碼的值。                                                             |



 

下列結構類型已過時，或已保留供日後使用：

-   **原則 \_ 審核 \_ 完整 \_ 查詢 \_ 資訊**
-   **原則 \_ 審核 \_ 完整 \_ 設定 \_ 資訊**
-   **原則 \_ 審核 \_ 記錄 \_ 資訊**
-   **原則 \_ 預設 \_ 配額 \_ 資訊**
-   **原則 \_ 複本 \_ 來源 \_ 資訊**
-   **信任的 \_ 控制器 \_ 資訊**

## <a name="attachment-structures"></a>附件結構

安全性設定附件 Dll 和其支援的函式會使用下列結構。 這些結構是在 Scesvc 中定義。



| 結構                                                        | Description                                                                                                                                     |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCESVC \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info) | 包含服務的設定資訊。                                                                                               |
| [**SCESVC \_ 設置 \_ 行**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line) | 包含有關設定資料行的資訊。                                                                                        |
| [**SCESVC \_ 分析 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info)           | 包含分析資訊。                                                                                                              |
| [**SCESVC \_ 分析 \_ 行**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line)           | 包含 [**SCESVC \_ 分析 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info) 結構所指定之特定行的索引鍵、值和值長度。 |
| [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)           | 包含不透明的資料庫控制碼，以及用來查詢、設定和釋放資訊的回呼函式指標。                                          |



 

## <a name="safer-structures"></a>更安全的結構

下列結構和列舉型別會以更安全的方式使用。 它們是在 WinSafer 中定義。



| 結構                                                                | Description                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**更安全的程式 \_ 代碼 \_ 屬性**](/windows/desktop/api/WinSafer/ns-winsafer-safer_code_properties_v2)                 | 包含要在程式碼映射上檢查的程式碼影像資訊和準則。 這些結構的陣列會傳遞至 [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) 函數。                                                                  |
| [**更安全的 \_ 識別 \_ 標頭**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header)     | [**更安全的 \_ 路徑名稱 \_ 識別**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification)、[**更安全的 \_ 雜湊 \_ 識別**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)，以及 [**更安全的 \_ URLZONE \_ 識別**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification)結構的標頭結構。 |
| [**更安全的 \_ 路徑名稱 \_ 識別**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification) | 保存要檢查的程式碼映射的路徑名稱。                                                                                                                                                                                                      |
| [**更安全的 \_ 雜湊 \_ 識別**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)         | 識別要檢查之程式碼映射的雜湊。                                                                                                                                                                                                      |
| [**更安全的 \_ URLZONE \_ 識別**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification)   | 識別要檢查的程式碼影像來源的 URL 區域。                                                                                                                                                                                      |



 

 

 
