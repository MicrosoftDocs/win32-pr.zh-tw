---
description: 列出安全性設定工具集所提供的支援功能。
ms.assetid: 5a771014-1706-490f-8540-ec516652cb83
title: 安全性管理功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c17efd55b1dbb806295ac0a83763257ffcc97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851523"
---
# <a name="security-management-functions"></a>安全性管理功能

本章節包含下列功能群組的主題：

-   [附加函式回呼函數](#attachment-callback-functions)
-   [附件引擎函數](#attachment-engine-functions)
-   [LSA 原則函數](#lsa-policy-functions)
    -   [原則函數](#lsa-policy-functions)
    -   [帳戶功能](#account-functions)
    -   [受信任的網域函數](#trusted-domain-functions)
    -   [私用資料函數](#private-data-functions)
    -   [雜項函式](#miscellaneous-functions)
-   [受管理的服務帳戶功能](#managed-service-account-functions)
-   [密碼篩選函數](#password-filter-functions)
-   [更安全的函數](#safer-functions)

## <a name="attachment-callback-functions"></a>附加函式回呼函數

下列支援函式是由安全性設定工具集所提供，可供附件引擎和延伸嵌入式管理單元用來讀取和寫入設定資料。



| 回呼函數                                         | Description                                                                                 |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**PFSCE \_ 免費 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_free_info)<br/>   | 用來釋放這些支援函數所配置的記憶體。<br/>                        |
| [**PFSCE \_ 記錄 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_log_info)<br/>     | 用來將訊息記錄到設定檔或分析記錄檔。<br/>          |
| [**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)<br/> | 用來查詢特定服務的設定和分析資訊。<br/> |
| [**PFSCE \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)<br/>     | 用來設定特定服務的設定和分析資訊。<br/>       |



 

## <a name="attachment-engine-functions"></a>附件引擎函數



| 函式                                                              | 描述                                                                                                                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)<br/> | 由附件引擎 DLL 所執行。 當系統分析時，安全性設定引擎會呼叫此函式。<br/>                                                           |
| [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)<br/>   | 由附件引擎 DLL 所執行。 當系統設定時，安全性設定引擎會呼叫此函式。<br/>                                                         |
| [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)<br/>   | 由附件引擎 DLL 所執行。 當安全性設定引擎從附件嵌入式管理單元擴充功能收到設定更新要求時，就會呼叫此函式。<br/> |



 

## <a name="lsa-policy-functions"></a>LSA 原則函數

下列主題提供 [*本機安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 原則功能的參考資訊。



| 主題                               | 描述                                                                                                                                                                                   |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 原則函數<br/>         | 詳細說明用來開啟本機 [**原則**](policy-object.md) 物件，以及設定或抓取全域原則資訊的函式。<br/>                                                  |
| 帳戶功能<br/>        | 詳細說明用來管理帳戶許可權，以及建立和刪除使用者帳戶的功能。<br/>                                                                                       |
| 受信任的網域函數<br/> | 詳細說明用來建立和刪除受信任網域關聯性的函式，以及設定和取得這些受信任網域的相關資訊。<br/>                                          |
| 私用資料函數<br/>   | 請勿使用 LSA 私用資料函數。 相反地，請使用 [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) 函數。<br/> |
| 雜項函式<br/>  | 詳細資料函式未在其他地方描述。<br/>                                                                                                                                         |



 

### <a name="policy-functions"></a>原則函數

下列函式會列舉使用者帳戶和信任的網域、接收原則變更通知，以及查閱帳戶名稱和 Sid。



| 函式                                                                                          | 描述                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)<br/>         | 列舉具有指定使用者權限的所有帳戶。<br/>                                                                                                                                                                                                                                                                         |
| [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/>                   | 列舉受信任的網域。<br/>                                                                                                                                                                                                                                                                                                            |
| [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames)<br/>                                               | 將指定的名稱對應至其 Sid。 傳回 SID 做為 RID/網域 SID 組。<br/>                                                                                                                                                                                                                                                         |
| [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2)<br/>                                             | 將指定的名稱對應至其 Sid。 傳回做為單一元素的 SID。<br/>                                                                                                                                                                                                                                                               |
| [**LsaLookupPrivilegeValue**](/windows/desktop/api/ntlsa/nf-ntlsa-lsalookupprivilegevalue)<br/>                             | 抓取 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 用來代表指定的許可權名稱 (LUID) 的 [*本機唯一識別碼*](/windows/desktop/SecGloss/l-gly)。<br/> |
| [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)<br/>                                                 | 將指定的帳號名稱對應至其 Sid。<br/>                                                                                                                                                                                                                                                                                            |
| [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification)<br/>     | 註冊事件物件，以在本機原則資訊變更時接收通知。<br/>                                                                                                                                                                                                                                              |
| [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification)<br/> | 取消註冊接收原則變更通知的事件物件。<br/>                                                                                                                                                                                                                                                                 |



 

### <a name="account-functions"></a>帳戶功能

下列函式會新增、列舉和刪除帳戶的許可權。



| 函式                                                                  | 描述                                                                                                  |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights)<br/>             | 將許可權新增至帳戶。 如果帳戶不存在，就會建立該帳戶。<br/>              |
| [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)<br/> | 列舉授與帳戶的許可權。<br/>                                                  |
| [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)<br/>       | 移除帳戶的許可權。 移除擁有權限後，就會刪除該帳戶。<br/> |



 

### <a name="trusted-domain-functions"></a>受信任的網域函數

下列函式會建立、列舉及刪除信任的網域，以及設定和抓取受信任的網域資訊。



| 函式                                                                                                                                                    | 描述                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex)<br/>                                                                                     | 建立新的 [**TrustedDomain**](trusteddomain-object.md) 物件。<br/>            |
| [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)<br/>                                                                                         | 移除 [**TrustedDomain**](trusteddomain-object.md) 物件。<br/>                |
| [**LsaEnumerateTrustedDomains**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains)<br/> [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/> | 列舉本機系統目前受信任的網域。<br/>                  |
| [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname)<br/>                                                                                 | 開啟 [**TrustedDomain**](trusteddomain-object.md) 物件的控制碼。<br/>      |
| [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo)<br/>                                                                                   | 抓取受信任網域的相關資訊。 網域是由 SID 指定。<br/>  |
| [**>lsaquerytrusteddomaininfobyname**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)<br/>                                                                       | 抓取受信任網域的相關資訊。 網域是依名稱指定。<br/> |
| [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)<br/>                                                                           | 設定受信任網域的資訊。 網域是依名稱指定。<br/>        |
| [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation)<br/>                                                                         | 設定受信任網域的資訊。 網域是由 SID 指定。<br/>         |



 

### <a name="private-data-functions"></a>私用資料函數

請勿使用 LSA 私用資料函數。 相反地，請使用 [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) 函數。



| 函式                                                            | 描述                                 |
|---------------------------------------------------------------------|---------------------------------------------|
| [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)<br/> | 抓取和解密字串。<br/> |
| [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata)<br/>       | 加密並儲存字串。<br/>    |



 

### <a name="miscellaneous-functions"></a>雜項函式

LSA 原則 API 有下列三個函式，這些函式不符合任何其他 LSA 原則函數類別。



| 函式                                                          | 描述                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)<br/>                           | 關閉 [**原則**](policy-object.md) 物件或 [**TrustedDomain**](trusteddomain-object.md) 物件的控制碼。<br/> |
| [**LsaFreeMemory**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsafreememory)<br/>                 | 釋放 LSA 函數所配置的緩衝區。<br/>                                                                           |
| [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)<br/> | 將 **NTSTATUS** 值轉換為 Windows 錯誤碼。<br/>                                                                |



 

## <a name="managed-service-account-functions"></a>受管理的服務帳戶功能

下列函式可用來建立、列舉、尋找及刪除受管理的服務帳戶。



| 函式                                                                      | 描述                                                                                                                 |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**NetAddServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netaddserviceaccount)<br/>               | 建立受管理的服務帳戶。<br/>                                                                               |
| [**NetEnumerateServiceAccounts**](/windows/desktop/api/Lmaccess/nf-lmaccess-netenumerateserviceaccounts)<br/> | 列舉指定伺服器上的伺服器帳戶。<br/>                                                          |
| [**NetIsServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netisserviceaccount)<br/>                 | 測試指定的服務帳戶是否存在於指定伺服器上的 Netlogon 存放區中。<br/>                |
| [**NetRemoveServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netremoveserviceaccount)<br/>         | 從 [Active Directory](/windows/desktop/AD/active-directory-domain-services) 資料庫中刪除指定的服務帳戶。<br/> |



 

## <a name="password-filter-functions"></a>密碼篩選函數

下列 [*密碼篩選*](/windows/desktop/SecGloss/p-gly) 函式是由自訂密碼篩選 dll 所執行，以提供密碼篩選和密碼變更通知。



| 函式                                                            | 描述                                                     |
|---------------------------------------------------------------------|-----------------------------------------------------------------|
| [**InitializeChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_init_notification_routine)<br/> | 指出密碼篩選 DLL 已初始化。<br/> |
| [**PasswordChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_notification_routine)<br/>     | 指出密碼已變更。<br/>          |
| [**PasswordFilter**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_filter_routine)<br/>                 | 根據密碼原則驗證新的密碼。<br/>   |



 

## <a name="safer-functions"></a>更安全的函數

下列安全的函式可用來檢查任何可執行檔的安全性層級，以及記錄事件。



| 函式                                                         | 描述                                                                                                                                                                          |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SaferCloseLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercloselevel)                       | \_ \_ 使用 [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)函數或 [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)函數，關閉開啟的更安全層級控制碼。<br/> |
| [**SaferComputeTokenFromLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercomputetokenfromlevel) | 使用更安全 \_ 層級控制碼所指定的限制來限制權杖 \_ 。<br/>                                                                                                 |
| [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)                     | 開啟更安全的 \_ 層級 \_ 控制碼。<br/>                                                                                                                                             |
| [**SaferGetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)     | 捕獲原則層級的相關資訊。<br/>                                                                                                                               |
| [**SaferGetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetpolicyinformation)   | 捕獲原則的相關資訊。<br/>                                                                                                                                     |
| [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)                 | 捕獲層級的相關資訊。<br/>                                                                                                                                      |
| [**SaferiIsExecutableFileType**](/windows/desktop/api/WinSafer/nf-winsafer-saferiisexecutablefiletype) | 判斷指定的檔案是否為可執行檔。<br/>                                                                                                                |
| [**SaferRecordEventLogEntry**](/windows/desktop/api/WinSafer/nf-winsafer-saferrecordeventlogentry)     | 將訊息傳送至事件記錄檔。<br/>                                                                                                                                         |
| [**SaferSetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safersetlevelinformation)     | 設定原則層級的相關資訊。<br/>                                                                                                                                |
| [**SaferSetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)    | 設定全域原則控制項。<br/>                                                                                                                                          |



 

 

