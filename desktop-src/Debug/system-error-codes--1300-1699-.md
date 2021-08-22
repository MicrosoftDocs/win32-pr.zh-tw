---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼1300-1699，適用于開發人員。
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: '系統錯誤碼 (1300-1699)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7aeb1c3642331db8ed3215d55a6d77e1e7b2a98c3859a5eb64a1d5b60350d24a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119310918"
---
# <a name="system-error-codes-1300-1699"></a>系統錯誤碼 (1300-1699) 

> [!NOTE]
> 這項資訊適用于程式設計人員偵測系統錯誤。 針對其他錯誤（例如 Windows Update 的問題），[[錯誤碼](system-error-codes.md)] 頁面上有資源清單。

下列清單描述錯誤1300到1699的 [系統錯誤碼](system-error-codes.md) 。 當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。

<dl> <dt>

<span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**\_未 \_ 全部 \_ 指派的錯誤**
</dt> <dd> <dl> <dt>

1300 (0x514)
</dt> <dt>



並非所有被參考的許可權或群組都會指派給呼叫者。


</dt> </dl> </dd> <dt>

<span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**\_部分 \_ 未 \_ 對應的錯誤**
</dt> <dd> <dl> <dt>

1301 (0x515) 
</dt> <dt>



帳戶名稱與安全性識別碼之間的部分對應尚未完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**\_沒有 \_ \_ 帳戶的配額 \_ 錯誤**
</dt> <dd> <dl> <dt>

1302 (0x516)
</dt> <dt>



未特別為此帳戶設定任何系統配額限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**\_本機 \_ 使用者 \_ 會話 \_ 金鑰錯誤**
</dt> <dd> <dl> <dt>

1303 (0x517)
</dt> <dt>



沒有可用的加密金鑰。 已傳回已知的加密金鑰。


</dt> </dl> </dd> <dt>

<span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**錯誤 \_ Null \_ LM \_ 密碼**
</dt> <dd> <dl> <dt>

1304 (0x518)
</dt> <dt>



密碼太複雜，無法轉換為 LAN Manager 密碼。 傳回的 LAN Manager 密碼是 **Null** 字串。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**錯誤 \_ 不明 \_ 修訂**
</dt> <dd> <dl> <dt>

1305 (0x519)
</dt> <dt>



修訂層級未知。


</dt> </dl> </dd> <dt>

<span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**錯誤 \_ 修訂 \_ 不相符**
</dt> <dd> <dl> <dt>

1306 (0x51A)
</dt> <dt>



表示兩個修訂層級不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**錯誤 \_ 不正確 \_ 擁有者**
</dt> <dd> <dl> <dt>

1307 (0x51B)
</dt> <dt>



此安全識別碼可能不會被指派為此物件的擁有者。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**錯誤 \_ 不正確 \_ 主要 \_ 群組**
</dt> <dd> <dl> <dt>

1308 (0x51C)
</dt> <dt>



此安全識別碼可能不會被指派為物件的主要群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**錯誤 \_ 無 \_ 模擬 \_ 權杖**
</dt> <dd> <dl> <dt>

1309 (0x51D)
</dt> <dt>



嘗試透過目前未模擬用戶端的執行緒，對模擬權杖操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**錯誤 \_ 無法 \_ 停用 \_ 強制**
</dt> <dd> <dl> <dt>

1310 (0x51E)
</dt> <dt>



群組可能未停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**\_沒有 \_ 登入 \_ 伺服器的錯誤**
</dt> <dd> <dl> <dt>

1311 (0x51F)
</dt> <dt>



目前沒有登入伺服器可用來服務登入要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**\_沒有 \_ 這類 \_ 登入 \_ 會話的錯誤**
</dt> <dd> <dl> <dt>

1312 (0x520)
</dt> <dt>



指定的登入工作階段不存在。 它可能已經被終止。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**錯誤 \_ 沒有 \_ 這類 \_ 許可權**
</dt> <dd> <dl> <dt>

1313 (0x521)
</dt> <dt>



指定的許可權不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**\_ \_ 未保留錯誤 \_ 許可權**
</dt> <dd> <dl> <dt>

1314 (0x522)
</dt> <dt>



用戶端沒有必要的權限。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**錯誤 \_ 不正確 \_ 帳戶 \_ 名稱**
</dt> <dd> <dl> <dt>

1315 (0x523) 
</dt> <dt>



提供的名稱不是正確格式的帳戶名稱。


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**\_使用者 \_ 存在錯誤**
</dt> <dd> <dl> <dt>

1316 (0x524)
</dt> <dt>



指定的帳戶已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**\_沒有 \_ 這類 \_ 使用者的錯誤**
</dt> <dd> <dl> <dt>

1317 (0x525)
</dt> <dt>



指定的帳號不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**錯誤 \_ 群組 \_ 存在**
</dt> <dd> <dl> <dt>

1318 (0x526)
</dt> <dt>



指定的群組已存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**錯誤 \_ 的 \_ \_ 群組**
</dt> <dd> <dl> <dt>

1319 (0x527)
</dt> <dt>



指定的群組不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_ \_ 群組中的錯誤成員 \_**
</dt> <dd> <dl> <dt>

1320 (0x528)
</dt> <dt>



指定的使用者帳戶已經是指定群組的成員，或無法刪除指定的群組，因為它包含成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**錯誤 \_ 成員 \_ 不 \_ 在 \_ 群組中**
</dt> <dd> <dl> <dt>

1321 (0x529)
</dt> <dt>



指定的使用者帳戶不是指定之群組帳戶的成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**\_上次系統 \_ 管理員錯誤**
</dt> <dd> <dl> <dt>

1322 (0x52A)
</dt> <dt>



不允許此作業，因為它可能會導致系統管理帳戶被停用、刪除或無法登入。


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**錯誤 \_ 的 \_ 密碼**
</dt> <dd> <dl> <dt>

1323 (0x52B)
</dt> <dt>



無法更新密碼。 提供的值為目前的密碼不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**\_格式錯誤 \_ 的 \_ 密碼**
</dt> <dd> <dl> <dt>

1324 (0x52C)
</dt> <dt>



無法更新密碼。 提供給新密碼的值包含密碼中不允許的值。


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**錯誤 \_ 密碼 \_ 限制**
</dt> <dd> <dl> <dt>

1325 (0x52D) 
</dt> <dt>



無法更新密碼。 針對新密碼所提供的值不符合網域的長度、複雜度或歷程記錄需求。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**錯誤 \_ 登入 \_ 失敗**
</dt> <dd> <dl> <dt>

1326 (0x52E)
</dt> <dt>



使用者名稱或密碼不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**錯誤 \_ 帳戶 \_ 限制**
</dt> <dd> <dl> <dt>

1327 (0x52F)
</dt> <dt>



帳戶限制導致此使用者無法登入。 例如：不允許空白密碼、登入時間有限，或已強制執行原則限制。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**錯誤 \_ 不正確 \_ 登入 \_ 時段**
</dt> <dd> <dl> <dt>

1328 (0x530) 
</dt> <dt>



您的帳戶有時間限制，讓您無法立即登入。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**錯誤 \_ 不正確 \_ 工作站**
</dt> <dd> <dl> <dt>

1329 (0x531)
</dt> <dt>



此使用者不允許登入這部電腦。


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**錯誤 \_ 密碼已 \_ 過期**
</dt> <dd> <dl> <dt>

1330 (0x532) 
</dt> <dt>



此帳戶的密碼已過期。


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**錯誤 \_ 帳戶 \_ 已停用**
</dt> <dd> <dl> <dt>

1331 (0x533) 
</dt> <dt>



此使用者無法登入，因為此帳戶目前已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**\_未 \_ 對應的錯誤**
</dt> <dd> <dl> <dt>

1332 (0x534) 
</dt> <dt>



帳戶名稱與安全識別碼之間沒有對應。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**\_ \_ \_ LUID 要求的錯誤太多 \_**
</dt> <dd> <dl> <dt>

1333 (0x535)
</dt> <dt>



 (Luid) 一次要求的本機使用者識別碼太多。


</dt> </dl> </dd> <dt>

<span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**錯誤 \_ LUID 已 \_ 用盡**
</dt> <dd> <dl> <dt>

1334 (0x536)
</dt> <dt>



沒有 (Luid) 可用的本機使用者識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**錯誤 \_ 不正確 \_ 子 \_ 授權單位**
</dt> <dd> <dl> <dt>

1335 (0x537) 
</dt> <dt>



安全識別碼的 subauthority 部分對於此特定用途無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**錯誤 \_ 不正確 \_ ACL**
</dt> <dd> <dl> <dt>

1336 (0x538)
</dt> <dt>



ACL) 結構 (的存取控制清單無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**錯誤 \_ 不正確 \_ SID**
</dt> <dd> <dl> <dt>

1337 (0x539)
</dt> <dt>



安全性識別碼結構無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**錯誤 \_ 不正確 \_ 安全性 \_ 描述**
</dt> <dd> <dl> <dt>

1338 (0x53A)
</dt> <dt>



安全描述項結構無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**錯誤 \_ 的 \_ 繼承 \_ ACL 錯誤**
</dt> <dd> <dl> <dt>

1340 (0x53C) 
</dt> <dt>



無法建立繼承的存取控制清單 (ACL) 或存取控制專案 (ACE) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**錯誤 \_ 伺服器 \_ 已停用**
</dt> <dd> <dl> <dt>

1341 (0x53D)
</dt> <dt>



伺服器目前已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**錯誤 \_ 伺服器 \_ 未 \_ 停用**
</dt> <dd> <dl> <dt>

1342 (0x53E)
</dt> <dt>



伺服器目前已啟用。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**錯誤 \_ 不正確 \_ 識別碼 \_ 授權單位**
</dt> <dd> <dl> <dt>

1343 (0x53F)
</dt> <dt>



提供的值對識別碼授權單位而言是無效值。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**\_超過錯誤分配 \_ 空間 \_**
</dt> <dd> <dl> <dt>

1344 (0x540)
</dt> <dt>



沒有更多可用的記憶體可進行安全性資訊更新。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**錯誤 \_ 不正確 \_ 群組 \_ 屬性**
</dt> <dd> <dl> <dt>

1345 (0x541)
</dt> <dt>



指定的屬性無效，或與整個群組的屬性不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**錯誤的模擬 \_ \_ \_ 層級錯誤**
</dt> <dd> <dl> <dt>

1346 (0x542)
</dt> <dt>



未提供所要求的模擬層，或所提供的模擬層不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**錯誤 \_ 無法 \_ 開啟 \_ 匿名**
</dt> <dd> <dl> <dt>

1347 (0x543)
</dt> <dt>



無法開啟匿名層級安全性權杖。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**錯誤 \_ 的 \_ 驗證 \_ 類別**
</dt> <dd> <dl> <dt>

1348 (0x544)
</dt> <dt>



要求的驗證資訊類別無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**錯誤錯誤的 \_ \_ 標記 \_ 類型**
</dt> <dd> <dl> <dt>

1349 (0x545)
</dt> <dt>



權杖的類型不適用於其嘗試的使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**\_沒有 \_ \_ 物件的安全性 \_ 錯誤**
</dt> <dd> <dl> <dt>

1350 (0x546)
</dt> <dt>



無法在沒有相關聯安全性的物件上執行安全性操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**無法 \_ \_ 存取 \_ 網域 \_ 資訊時發生錯誤**
</dt> <dd> <dl> <dt>

1351 (0x547)
</dt> <dt>



無法從網域控制站讀取設定資訊，可能是因為電腦無法使用，或存取遭到拒絕。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**錯誤 \_ 不正確 \_ 伺服器 \_ 狀態**
</dt> <dd> <dl> <dt>

1352 (0x548)
</dt> <dt>



安全性帳戶管理員 (SAM) 或本地安全機構 (LSA) 伺服器的狀態不正確，無法執行安全性作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**錯誤 \_ 不正確 \_ 網域 \_ 狀態**
</dt> <dd> <dl> <dt>

1353 (0x549)
</dt> <dt>



網域的狀態不正確，無法執行安全性作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**錯誤 \_ 不正確 \_ 網域 \_ 角色**
</dt> <dd> <dl> <dt>

1354 (0x54A)
</dt> <dt>



這項作業只允許用於網域的主域控制站。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**\_沒有 \_ 這類 \_ 網域的錯誤**
</dt> <dd> <dl> <dt>

1355 (0x54B) 
</dt> <dt>



指定的網域可能不存在或無法連絡。


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**錯誤 \_ 網域 \_ 存在**
</dt> <dd> <dl> <dt>

1356 (0x54C)
</dt> <dt>



指定的網域已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**\_超過錯誤網域 \_ 限制 \_**
</dt> <dd> <dl> <dt>

1357 (0x54D) 
</dt> <dt>



嘗試超過每一伺服器的網域數目上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**\_內部 \_ 資料庫 \_ 損毀錯誤**
</dt> <dd> <dl> <dt>

1358 (0x54E) 
</dt> <dt>



無法完成要求的操作，因為磁片上發生重大媒體失敗或資料結構損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**錯誤 \_ 內部 \_ 錯誤**
</dt> <dd> <dl> <dt>

1359 (0x54F) 
</dt> <dt>



發生內部錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**錯誤 \_ 泛型 \_ 未 \_ 對應**
</dt> <dd> <dl> <dt>

1360 (0x550) 
</dt> <dt>



一般存取類型包含在應該已經對應到非泛型型別的存取遮罩中。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**錯誤 \_ \_ 描述項 \_ 格式錯誤**
</dt> <dd> <dl> <dt>

1361 (0x551) 
</dt> <dt>



安全描述項的格式不正確 (絕對或自我相對) 。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**錯誤 \_ 未 \_ 登入 \_ 進程**
</dt> <dd> <dl> <dt>

1362 (0x552) 
</dt> <dt>



要求的動作僅限登入處理常式使用。 呼叫進程尚未註冊為登入程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**錯誤 \_ 登入 \_ 會話 \_ 存在**
</dt> <dd> <dl> <dt>

1363 (0x553) 
</dt> <dt>



無法以已在使用中的識別碼啟動新的登入會話。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**錯誤 \_ 沒有 \_ 這類 \_ 套件**
</dt> <dd> <dl> <dt>

1364 (0x554) 
</dt> <dt>



指定的驗證封裝未知。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**錯誤 \_ 的 \_ 登入 \_ 會話 \_ 狀態錯誤**
</dt> <dd> <dl> <dt>

1365 (0x555) 
</dt> <dt>



登入會話的狀態與要求的作業不一致。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**錯誤 \_ 登入 \_ 會話 \_ 衝突**
</dt> <dd> <dl> <dt>

1366 (0x556) 
</dt> <dt>



登入會話識別碼已在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**錯誤 \_ 不正確 \_ 登入 \_ 類型**
</dt> <dd> <dl> <dt>

1367 (0x557) 
</dt> <dt>



登入要求包含不正確登入類型值。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**錯誤 \_ 無法 \_ 模擬**
</dt> <dd> <dl> <dt>

1368 (0x558)
</dt> <dt>



除非已從該管道讀取資料，否則無法使用具名管道進行模擬。


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**\_RXACT \_ 無效 \_ 狀態時發生錯誤**
</dt> <dd> <dl> <dt>

1369 (0x559) 
</dt> <dt>



登錄子樹的交易狀態與要求的作業不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**\_RXACT \_ 認可 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

1370 (0x55A) 
</dt> <dt>



發生內部安全性資料庫損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**錯誤 \_ 特殊 \_ 帳戶**
</dt> <dd> <dl> <dt>

1371 (0x55B) 
</dt> <dt>



無法對內建帳戶執行這項作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**錯誤 \_ 特殊 \_ 群組**
</dt> <dd> <dl> <dt>

1372 (0x55C) 
</dt> <dt>



無法在這個內建的特殊群組上執行這項作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**\_特殊 \_ 使用者錯誤**
</dt> <dd> <dl> <dt>

1373 (0x55D)
</dt> <dt>



無法對這個內建的特殊使用者執行這項作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**錯誤 \_ 成員 \_ 主要 \_ 群組**
</dt> <dd> <dl> <dt>

1374 (0x55E)
</dt> <dt>



無法從群組中移除使用者，因為群組目前是使用者的主要群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**錯誤 \_ 權杖 \_ 已 \_ 在 \_ 使用中**
</dt> <dd> <dl> <dt>

1375 (0x55F) 
</dt> <dt>



權杖已使用做為主要權杖。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**錯誤 \_ 沒有 \_ 這類 \_ 別名**
</dt> <dd> <dl> <dt>

1376 (0x560) 
</dt> <dt>



指定的本機群組不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**錯誤 \_ 成員 \_ 不 \_ 在 \_ 別名中**
</dt> <dd> <dl> <dt>

1377 (0x561)
</dt> <dt>



指定的帳號名稱不是群組的成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_ \_ 別名中的錯誤成員 \_**
</dt> <dd> <dl> <dt>

1378 (0x562)
</dt> <dt>



指定的帳號名稱已是群組的成員。


</dt> </dl> </dd> <dt>

<span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**錯誤 \_ 別名 \_ 存在**
</dt> <dd> <dl> <dt>

1379 (0x563)
</dt> <dt>



指定的本機群組已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**\_ \_ 未 \_ 授與錯誤登入**
</dt> <dd> <dl> <dt>

1380 (0x564)
</dt> <dt>



登入失敗：未在這部電腦上授與使用者所要求的登入類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**錯誤 \_ 太 \_ 多 \_ 秘密**
</dt> <dd> <dl> <dt>

1381 (0x565)
</dt> <dt>



已超過可能儲存在單一系統中的秘密數目上限。


</dt> </dl> </dd> <dt>

<span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**錯誤 \_ 密碼 \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

1382 (0x566)
</dt> <dt>



秘密的長度超過允許的最大長度。


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**錯誤 \_ 內部 \_ 資料庫 \_ 錯誤**
</dt> <dd> <dl> <dt>

1383 (0x567)
</dt> <dt>



本地安全機構資料庫包含內部不一致的情況。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**錯誤 \_ 太 \_ 多 \_ 內容 \_ 識別碼**
</dt> <dd> <dl> <dt>

1384 (0x568)
</dt> <dt>



在登入嘗試期間，使用者的安全性內容累積了太多的安全識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_ \_ \_ 未 \_ 授與錯誤登入類型**
</dt> <dd> <dl> <dt>

1385 (0x569)
</dt> <dt>



登入失敗：未在這部電腦上授與使用者所要求的登入類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**錯誤 \_ NT \_ \_ 需要跨加密 \_**
</dt> <dd> <dl> <dt>

1386 (0x56A)
</dt> <dt>



需要跨加密密碼才能變更使用者密碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**錯誤 \_ 的 \_ \_ 成員**
</dt> <dd> <dl> <dt>

1387 (0x56B)
</dt> <dt>



無法在本機群組中加入或移除成員，因為該成員不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**錯誤 \_ 不正確 \_ 成員**
</dt> <dd> <dl> <dt>

1388 (0x56C)
</dt> <dt>



因為成員的帳戶類型錯誤，所以無法將新成員新增至本機群組。


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**錯誤 \_ 太 \_ 多 \_ SID**
</dt> <dd> <dl> <dt>

1389 (0x56D) 
</dt> <dt>



指定了太多的安全性識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**\_需要 LM \_ 跨 \_ 加密 \_ 的錯誤**
</dt> <dd> <dl> <dt>

1390 (0x56E)
</dt> <dt>



需要跨加密密碼才能變更此使用者密碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**錯誤 \_ 無 \_ 繼承**
</dt> <dd> <dl> <dt>

1391 (0x56F) 
</dt> <dt>



表示 ACL 未包含可繼承的元件。


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**錯誤檔案已損毀 \_ \_**
</dt> <dd> <dl> <dt>

1392 (0x570)
</dt> <dt>



檔案或目錄已損毀且無法讀取。


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**錯誤 \_ 磁片 \_ 已損毀**
</dt> <dd> <dl> <dt>

1393 (0x571)
</dt> <dt>



磁片結構已損毀且無法讀取。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**錯誤 \_ 的 \_ 使用者 \_ 會話 \_ 金鑰**
</dt> <dd> <dl> <dt>

1394 (0x572)
</dt> <dt>



指定的登入會話沒有使用者工作階段金鑰。


</dt> </dl> </dd> <dt>

<span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**\_超過錯誤授權 \_ 配額 \_**
</dt> <dd> <dl> <dt>

1395 (0x573)
</dt> <dt>



正在存取的服務已獲得特定數目的連線授權。 目前無法再對服務進行連接，因為服務可以接受的連線數目已經過多。


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**錯誤 \_ 的 \_ 目標 \_ 名稱錯誤**
</dt> <dd> <dl> <dt>

1396 (0x574)
</dt> <dt>



目標帳戶名稱不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**錯誤 \_ 相互 \_ 驗證 \_ 失敗**
</dt> <dd> <dl> <dt>

1397 (0x575)
</dt> <dt>



相互驗證失敗。 伺服器的密碼在網域控制站上已過期。


</dt> </dl> </dd> <dt>

<span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**錯誤 \_ 時間 \_ 誤差**
</dt> <dd> <dl> <dt>

1398 (0x576)
</dt> <dt>



用戶端與伺服器之間有時間及/或日期的差異。


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**\_ \_ \_ 不允許目前的網域錯誤 \_**
</dt> <dd> <dl> <dt>

1399 (0x577)
</dt> <dt>



無法在目前的網域上執行此作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**錯誤 \_ 不正確 \_ 視窗 \_ 控制碼**
</dt> <dd> <dl> <dt>

1400 (0x578)
</dt> <dt>



不正確視窗控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**\_不正確 \_ 功能表 \_ 控制碼時發生錯誤**
</dt> <dd> <dl> <dt>

1401 (0x579)
</dt> <dt>



功能表控制碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**錯誤 \_ 不正確資料 \_ 指標 \_ 控制碼**
</dt> <dd> <dl> <dt>

1402 (0x57A)
</dt> <dt>



不正確資料指標控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**錯誤 \_ 不正確 \_ ACCEL \_ 控制碼**
</dt> <dd> <dl> <dt>

1403 (0x57B)
</dt> <dt>



快速鍵對應表控制碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**錯誤 \_ 不正確攔截 \_ \_ 控制碼**
</dt> <dd> <dl> <dt>

1404 (0x57C) 
</dt> <dt>



不正確攔截控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**錯誤 \_ 不正確 \_ .DWP \_ 控制碼**
</dt> <dd> <dl> <dt>

1405 (0x57D)
</dt> <dt>



多視窗位置結構的控制碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**\_ \_ 使用 WSCHILD TLW \_ 錯誤**
</dt> <dd> <dl> <dt>

1406 (0x57E) 
</dt> <dt>



無法建立最上層子視窗。


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**\_找不 \_ 到 \_ WND<> \_ 類別的錯誤**
</dt> <dd> <dl> <dt>

1407 (0x57F) 
</dt> <dt>



找不到視窗類別。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_ \_ \_ 其他 \_ 執行緒的錯誤視窗**
</dt> <dd> <dl> <dt>

1408 (0x580) 
</dt> <dt>



不正確視窗;它屬於其他執行緒。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**\_ \_ 已 \_ 註冊錯誤的熱鍵**
</dt> <dd> <dl> <dt>

1409 (0x581) 
</dt> <dt>



快速鍵已註冊。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**錯誤 \_ 類別 \_ 已 \_ 存在**
</dt> <dd> <dl> <dt>

1410 (0x582) 
</dt> <dt>



類別已經存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**錯誤 \_ 類別 \_ 不 \_ \_ 存在**
</dt> <dd> <dl> <dt>

1411 (0x583) 
</dt> <dt>



類別不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**ERROR \_ 類別 \_ 具有 \_ WINDOWS**
</dt> <dd> <dl> <dt>

1412 (0x584) 
</dt> <dt>



類別仍有開啟的視窗。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**錯誤 \_ 不正確 \_ 索引**
</dt> <dd> <dl> <dt>

1413 (0x585) 
</dt> <dt>



不正確索引。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**錯誤 \_ 不正確 \_ 圖示 \_ 控制碼**
</dt> <dd> <dl> <dt>

1414 (0x586) 
</dt> <dt>



不正確圖示控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**\_私用 \_ 對話 \_ 索引錯誤**
</dt> <dd> <dl> <dt>

1415 (0x587) 
</dt> <dt>



使用私用交談視窗文字。


</dt> </dl> </dd> <dt>

<span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 LISTBOX 識別碼**
</dt> <dd> <dl> <dt>

1416 (0x588) 
</dt> <dt>



找不到清單方塊識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**錯誤 \_ 沒有 \_ 萬用字元 \_**
</dt> <dd> <dl> <dt>

1417 (0x589) 
</dt> <dt>



找不到任何萬用字元。


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**錯誤 \_ 剪貼簿 \_ 未 \_ 開啟**
</dt> <dd> <dl> <dt>

1418 (0x58A) 
</dt> <dt>



執行緒沒有開啟剪貼簿。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**錯誤的 \_ 熱鍵 \_ 未 \_ 註冊**
</dt> <dd> <dl> <dt>

1419 (0x58B) 
</dt> <dt>



快速鍵未註冊。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**錯誤 \_ 視窗 \_ 未 \_ 對話方塊**
</dt> <dd> <dl> <dt>

1420 (0x58C) 
</dt> <dt>



視窗不是有效的交談視窗。


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**\_ \_ \_ \_ 找不到錯誤控制識別碼**
</dt> <dd> <dl> <dt>

1421 (0x58D) 
</dt> <dt>



找不到控制項識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**\_不正確 \_ COMBOBOX \_ 訊息錯誤**
</dt> <dd> <dl> <dt>

1422 (0x58E) 
</dt> <dt>



下拉式方塊的訊息無效，因為它沒有編輯控制項。


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**錯誤 \_ 視窗 \_ 不是 \_ COMBOBOX**
</dt> <dd> <dl> <dt>

1423 (0x58F) 
</dt> <dt>



視窗不是下拉式方塊。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**錯誤 \_ 不正確 \_ 編輯 \_ 高度**
</dt> <dd> <dl> <dt>

1424 (0x590) 
</dt> <dt>



高度必須小於256。


</dt> </dl> </dd> <dt>

<span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**\_ \_ 找不到錯誤 DC \_**
</dt> <dd> <dl> <dt>

1425 (0x591) 
</dt> <dt>



裝置內容 (DC) 控制碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**錯誤 \_ 不正確攔截 \_ \_ 篩選**
</dt> <dd> <dl> <dt>

1426 (0x592) 
</dt> <dt>



不正確掛勾程式類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**錯誤 \_ 不正確 \_ 篩選器 \_ 進程**
</dt> <dd> <dl> <dt>

1427 (0x593) 
</dt> <dt>



不正確攔截程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**錯誤 \_ 攔截 \_ 需要 \_ HMOD**
</dt> <dd> <dl> <dt>

1428 (0x594) 
</dt> <dt>



無法在沒有模組控制碼的情況下設定非本機掛勾。


</dt> </dl> </dd> <dt>

<span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**\_全域 \_ 唯一攔截 \_ 錯誤**
</dt> <dd> <dl> <dt>

1429 (0x595) 
</dt> <dt>



此攔截程式只能在全域設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**錯誤 \_ 日誌 \_ 掛勾 \_ 設定**
</dt> <dd> <dl> <dt>

1430 (0x596) 
</dt> <dt>



已安裝日誌攔截程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**\_ \_ 未 \_ 安裝錯誤攔截**
</dt> <dd> <dl> <dt>

1431 (0x597) 
</dt> <dt>



未安裝攔截程式。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**錯誤 \_ 不正確 \_ LB \_ 訊息**
</dt> <dd> <dl> <dt>

1432 (0x598) 
</dt> <dt>



單一選取清單方塊的訊息無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**錯誤 \_ \_ LB 上的錯誤 SETCOUNT \_ \_**
</dt> <dd> <dl> <dt>

1433 (0x599) 
</dt> <dt>



LB \_ SETCOUNT 傳送至非延遲清單方塊。


</dt> </dl> </dd> <dt>

<span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**錯誤 \_ LB \_ 但沒有 \_ TABSTOPS**
</dt> <dd> <dl> <dt>

1434 (0x59A) 
</dt> <dt>



此清單方塊不支援定位停駐點。


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**損 \_ 毀 \_ \_ \_ 其他執行緒的 \_ 物件時發生錯誤**
</dt> <dd> <dl> <dt>

1435 (0x59B) 
</dt> <dt>



無法終結另一個執行緒所建立的物件。


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**錯誤 \_ 子 \_ 視窗 \_ 功能表**
</dt> <dd> <dl> <dt>

1436 (0x59C) 
</dt> <dt>



子視窗不可以有功能表。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**錯誤 \_ 的 \_ 系統 \_ 功能表**
</dt> <dd> <dl> <dt>

1437 (0x59D) 
</dt> <dt>



視窗沒有系統功能表。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**\_不正確 \_ MSGBOX \_ 樣式錯誤**
</dt> <dd> <dl> <dt>

1438 (0x59E) 
</dt> <dt>



訊息方塊樣式無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**錯誤 \_ 不正確 \_ SPI \_ 值**
</dt> <dd> <dl> <dt>

1439 (0x59F) 
</dt> <dt>



不正確全系統 (SPI \_ \*) 參數。


</dt> </dl> </dd> <dt>

<span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**錯誤 \_ 畫面 \_ 已 \_ 鎖定**
</dt> <dd> <dl> <dt>

1440 (0x5A0) 
</dt> <dt>



螢幕已鎖定。


</dt> </dl> </dd> <dt>

<span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**錯誤 \_ HWND \_ 具有 \_ 差異 \_ 父系**
</dt> <dd> <dl> <dt>

1441 (0x5A1) 
</dt> <dt>



多視窗位置結構中的所有 windows 控制碼都必須具有相同的父系。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**錯誤 \_ 不是 \_ 子 \_ 視窗**
</dt> <dd> <dl> <dt>

1442 (0x5A2) 
</dt> <dt>



視窗不是子視窗。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**錯誤 \_ 不正確 \_ GW \_ 命令**
</dt> <dd> <dl> <dt>

1443 (0x5A3) 
</dt> <dt>



GW \_ \* 命令無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**錯誤 \_ 不正確 \_ 執行緒 \_ 識別碼**
</dt> <dd> <dl> <dt>

1444 (0x5A4) 
</dt> <dt>



不正確執行緒識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**錯誤 \_ 非 \_ MDICHILD \_ 視窗**
</dt> <dd> <dl> <dt>

1445 (0x5A5) 
</dt> <dt>



無法從非多重文件介面 (MDI) 視窗的視窗處理訊息。


</dt> </dl> </dd> <dt>

<span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**錯誤 \_ 快顯視窗 \_ 已在 \_ 使用中**
</dt> <dd> <dl> <dt>

1446 (0x5A6) 
</dt> <dt>



快顯功能表已在使用中。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**錯誤 \_ 的 \_ 捲軸**
</dt> <dd> <dl> <dt>

1447 (0x5A7) 
</dt> <dt>



視窗沒有捲軸。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**錯誤 \_ 的 \_ 捲軸 \_ 範圍無效**
</dt> <dd> <dl> <dt>

1448 (0x5A8) 
</dt> <dt>



捲軸範圍不能大於 MAXLONG。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**錯誤 \_ 不正確 \_ SHOWWIN \_ 命令**
</dt> <dd> <dl> <dt>

1449 (0x5A9) 
</dt> <dt>



無法以指定的方式顯示或移除視窗。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**錯誤 \_ 的 \_ 系統 \_ 資源**
</dt> <dd> <dl> <dt>

1450 (0x5AA) 
</dt> <dt>



沒有足夠的系統資源，無法完成要求的服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**錯誤的未 \_ 分頁 \_ 系統 \_ 資源**
</dt> <dd> <dl> <dt>

1451 (0x5AB) 
</dt> <dt>



沒有足夠的系統資源，無法完成要求的服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**\_分頁 \_ 系統 \_ 資源錯誤**
</dt> <dd> <dl> <dt>

1452 (0x5AC) 
</dt> <dt>



沒有足夠的系統資源，無法完成要求的服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**\_工作 \_ 集 \_ 配額錯誤**
</dt> <dd> <dl> <dt>

1453 (0x5AD) 
</dt> <dt>



配額不足，無法完成要求的服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**錯誤 \_ 分頁檔 \_ 配額**
</dt> <dd> <dl> <dt>

1454 (0x5AE) 
</dt> <dt>



配額不足，無法完成要求的服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**錯誤 \_ 承諾用量 \_ 限制**
</dt> <dd> <dl> <dt>

1455 (0x5AF) 
</dt> <dt>



分頁檔案太小，所以無法完成此操作。


</dt> </dl> </dd> <dt>

<span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**\_ \_ \_ \_ 找不到錯誤功能表項目**
</dt> <dd> <dl> <dt>

1456 (0x5B0) 
</dt> <dt>



找不到功能表項目。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**\_不正確 \_ 鍵盤 \_ 控制碼錯誤**
</dt> <dd> <dl> <dt>

1457 (0x5B1) 
</dt> <dt>



鍵盤配置控制碼無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**\_ \_ \_ 不 \_ 允許錯誤攔截類型**
</dt> <dd> <dl> <dt>

1458 (0x5B2) 
</dt> <dt>



不允許使用勾點類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**錯誤 \_ 需要 \_ 互動式 \_ WINDOWSTATION**
</dt> <dd> <dl> <dt>

1459 (0x5B3) 
</dt> <dt>



這種操作需要互動式的視窗站。


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**錯誤 \_ 超時**
</dt> <dd> <dl> <dt>

1460 (0x5B4) 
</dt> <dt>



因為超時時間已過，所以會傳回此作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**錯誤 \_ 不正確 \_ 監視器 \_ 控制碼**
</dt> <dd> <dl> <dt>

1461 (0x5B5) 
</dt> <dt>



不正確監視器控制碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**錯誤 \_ 的 \_ 大小不正確**
</dt> <dd> <dl> <dt>

1462 (0x5B6) 
</dt> <dt>



大小引數不正確。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**錯誤 \_ 符號符號 \_ 類別 \_ 已停用**
</dt> <dd> <dl> <dt>

1463 (0x5B7) 
</dt> <dt>



無法遵循符號連結，因為它的類型已停用。


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**\_ \_ 不支援錯誤符號符號 \_**
</dt> <dd> <dl> <dt>

1464 (0x5B8) 
</dt> <dt>



此應用程式不支援符號連結上的目前作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**錯誤 \_ XML \_ 剖析 \_ 錯誤**
</dt> <dd> <dl> <dt>

1465 (0x5B9) 
</dt> <dt>



Windows 無法剖析要求的 XML 資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**錯誤 \_ XMLDSIG \_ 錯誤**
</dt> <dd> <dl> <dt>

1466 (0x5BA) 
</dt> <dt>



處理 XML 數位簽章時發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**\_重新開機 \_ 應用程式時發生錯誤**
</dt> <dd> <dl> <dt>

1467 (0x5BB) 
</dt> <dt>



此應用程式必須重新開機。


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**錯誤 \_ 的 \_ 區間**
</dt> <dd> <dl> <dt>

1468 (0x5BC) 
</dt> <dt>



呼叫者在錯誤的路由區間中提出了連線要求。


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**錯誤 \_ AUTHIP \_ 失敗**
</dt> <dd> <dl> <dt>

1469 (0x5BD) 
</dt> <dt>



嘗試連接到遠端主機時發生 AuthIP 失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**錯誤 \_ 的 \_ NVRAM \_ 資源**
</dt> <dd> <dl> <dt>

1470 (0x5BE) 
</dt> <dt>



沒有足夠的 NVRAM 資源，無法完成要求的服務。 可能需要重新開機。


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**錯誤 \_ 而非 \_ GUI \_ 進程**
</dt> <dd> <dl> <dt>

1471 (0x5BF) 
</dt> <dt>



無法完成要求的操作，因為指定的進程不是 GUI 進程。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**錯誤 \_ EVENTLOG \_ 檔 \_ 已損毀**
</dt> <dd> <dl> <dt>

1500 (0x5DC) 
</dt> <dt>



事件記錄檔已損毀。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**錯誤 \_ EVENTLOG \_ 無法 \_ 啟動**
</dt> <dd> <dl> <dt>

1501 (0x5DD) 
</dt> <dt>



無法開啟任何事件記錄檔，因此事件記錄服務無法啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**錯誤 \_ 記錄檔已 \_ \_ 滿**
</dt> <dd> <dl> <dt>

1502 (0x5DE) 
</dt> <dt>



事件記錄檔已滿。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**錯誤 \_ EVENTLOG \_ 檔 \_ 已變更**
</dt> <dd> <dl> <dt>

1503 (0x5DF) 
</dt> <dt>



事件記錄檔已在讀取作業之間變更。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**錯誤 \_ 不正確工作 \_ \_ 名稱**
</dt> <dd> <dl> <dt>

1550 (0x60E)
</dt> <dt>



指定的工作名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**錯誤 \_ 不正確工作 \_ \_ 索引**
</dt> <dd> <dl> <dt>

1551 (0x60F)
</dt> <dt>



指定的任務索引無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**工作 \_ \_ 中已經 \_ 有錯誤執行緒 \_**
</dt> <dd> <dl> <dt>

1552 (0x610)
</dt> <dt>



指定的執行緒已經加入工作。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**\_安裝 \_ 服務 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

1601 (0x641) 
</dt> <dt>



無法存取 Windows Installer 服務。 如果未正確安裝 Windows Installer，就可能發生這種情況。 請洽詢支援人員以取得協助。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**\_安裝 \_ USEREXIT 時發生錯誤**
</dt> <dd> <dl> <dt>

1602 (0x642) 
</dt> <dt>



使用者已取消安裝。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**\_安裝 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

1603 (0x643) 
</dt> <dt>



安裝時發生嚴重錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**\_安裝 \_ 暫止時發生錯誤**
</dt> <dd> <dl> <dt>

1604 (0x644) 
</dt> <dt>



安裝已暫停，未完成。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**錯誤 \_ 未知的 \_ 產品**
</dt> <dd> <dl> <dt>

1605 (0x645) 
</dt> <dt>



這個動作只對目前安裝的產品有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**錯誤 \_ 未知的 \_ 功能**
</dt> <dd> <dl> <dt>

1606 (0x646) 
</dt> <dt>



未註冊功能識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**錯誤 \_ 不明的 \_ 元件**
</dt> <dd> <dl> <dt>

1607 (0x647) 
</dt> <dt>



未註冊元件識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**錯誤 \_ 未知的 \_ 屬性**
</dt> <dd> <dl> <dt>

1608 (0x648) 
</dt> <dt>



未知的屬性。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**錯誤 \_ 不正確 \_ 控制碼 \_ 狀態**
</dt> <dd> <dl> <dt>

1609 (0x649) 
</dt> <dt>



控制碼處於不正確狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**錯誤的設定不 \_ 正確 \_**
</dt> <dd> <dl> <dt>

1610 (0x64A) 
</dt> <dt>



此產品的設定資料已損毀。 請聯絡支援人員。


</dt> </dl> </dd> <dt>

<span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**錯誤 \_ 索引不 \_ 存在**
</dt> <dd> <dl> <dt>

1611 (0x64B) 
</dt> <dt>



元件辨識符號不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**\_安裝 \_ 來源不 \_ 存在時發生錯誤**
</dt> <dd> <dl> <dt>

1612 (0x64C) 
</dt> <dt>



無法使用此產品的安裝來源。 請確認來源是否存在，以及您是否可以存取它。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**\_安裝 \_ 套件 \_ 版本時發生錯誤**
</dt> <dd> <dl> <dt>

1613 (0x64D) 
</dt> <dt>



Windows Installer 服務無法安裝這個安裝套件。 您必須安裝 Windows service pack，其中包含較新版本的 Windows Installer 服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**卸載的錯誤 \_ 產品 \_**
</dt> <dd> <dl> <dt>

1614 (0x64E) 
</dt> <dt>



解除安裝產品。


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**錯誤 \_ \_ 查詢 \_ 語法錯誤**
</dt> <dd> <dl> <dt>

1615 (0x64F) 
</dt> <dt>



SQL 的查詢語法無效或不受支援。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**錯誤 \_ 不正確 \_ 欄位**
</dt> <dd> <dl> <dt>

1616 (0x650) 
</dt> <dt>



記錄欄位不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**\_ \_ 已移除錯誤裝置**
</dt> <dd> <dl> <dt>

1617 (0x651) 
</dt> <dt>



裝置已移除。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**\_安裝 \_ 已在執行中時發生錯誤 \_**
</dt> <dd> <dl> <dt>

1618 (0x652) 
</dt> <dt>



另一個安裝已在進行中。 繼續進行此安裝之前，請先完成該安裝。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**錯誤 \_ 安裝 \_ 套件 \_ 開啟 \_ 失敗**
</dt> <dd> <dl> <dt>

1619 (0x653) 
</dt> <dt>



無法開啟此安裝套件。 請確認封裝存在，而且您可以存取它，或洽詢應用程式廠商，確認這是有效的 Windows Installer 套件。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**\_安裝 \_ 套件 \_ 不正確錯誤**
</dt> <dd> <dl> <dt>

1620 (0x654) 
</dt> <dt>



無法開啟此安裝套件。 請聯繫應用程式廠商，確認這是有效的 Windows Installer 套件。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**\_安裝 \_ UI \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

1621 (0x655) 
</dt> <dt>



啟動 Windows Installer 服務使用者介面時發生錯誤。 請聯絡支援人員。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**\_安裝 \_ 記錄檔 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

1622 (0x656) 
</dt> <dt>



開啟安裝記錄檔時發生錯誤。 確認指定的記錄檔位置存在，而且您可以寫入它。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**\_ \_ 不支援的安裝語言錯誤 \_**
</dt> <dd> <dl> <dt>

1623 (0x657) 
</dt> <dt>



系統不支援此安裝套件的語言。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**\_安裝 \_ 轉換 \_ 失敗時發生錯誤**
</dt> <dd> <dl> <dt>

1624 (0x658) 
</dt> <dt>



套用轉換時發生錯誤。 確認指定的轉換路徑有效。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**\_拒絕安裝 \_ 套件的錯誤 \_**
</dt> <dd> <dl> <dt>

1625 (0x659) 
</dt> <dt>



系統原則禁止此安裝。 請連絡您的系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**\_ \_ 未 \_ 呼叫錯誤函式**
</dt> <dd> <dl> <dt>

1626 (0x65A) 
</dt> <dt>



無法執行函數。


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**錯誤函式 \_ \_ 失敗**
</dt> <dd> <dl> <dt>

1627 (0x65B) 
</dt> <dt>



函數在執行期間失敗。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**錯誤 \_ 不正確 \_ 資料表**
</dt> <dd> <dl> <dt>

1628 (0x65C) 
</dt> <dt>



指定的資料表無效或未知。


</dt> </dl> </dd> <dt>

<span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**錯誤 \_ 資料類型 \_ 不相符**
</dt> <dd> <dl> <dt>

1629 (0x65D) 
</dt> <dt>



提供的資料類型錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**錯誤 \_ 不支援的 \_ 類型**
</dt> <dd> <dl> <dt>

1630 (0x65E) 
</dt> <dt>



不支援此類型的資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**錯誤 \_ 建立 \_ 失敗**
</dt> <dd> <dl> <dt>

1631 (0x65F) 
</dt> <dt>



Windows Installer 服務無法啟動。 請聯絡支援人員。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**\_安裝 \_ TEMP \_ 資料流程時發生錯誤**
</dt> <dd> <dl> <dt>

1632 (0x660) 
</dt> <dt>



Temp 資料夾位於已滿或無法存取的磁片磁碟機上。 釋放磁片磁碟機上的空間，或確認您擁有 Temp 資料夾的寫入權限。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**\_ \_ 不支援的安裝平臺錯誤 \_**
</dt> <dd> <dl> <dt>

1633 (0x661) 
</dt> <dt>



此處理器類型不支援此安裝套件。 請洽詢您的產品廠商。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**\_安裝 \_ NOTUSED 時發生錯誤**
</dt> <dd> <dl> <dt>

1634 (0x662) 
</dt> <dt>



元件未在這部電腦上使用。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**錯誤 \_ 修補 \_ 套件 \_ 開啟 \_ 失敗**
</dt> <dd> <dl> <dt>

1635 (0x663) 
</dt> <dt>



無法開啟此更新套件。 確認更新封裝存在，而且您可以存取它，或聯繫應用程式廠商，確認這是有效的 Windows Installer 更新套件。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**錯誤 \_ 修補程式 \_ 套件 \_ 無效**
</dt> <dd> <dl> <dt>

1636 (0x664) 
</dt> <dt>



無法開啟此更新套件。 請聯繫應用程式廠商，確認這是有效的 Windows Installer 更新套件。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**\_不支援錯誤修補程式 \_ 套件 \_**
</dt> <dd> <dl> <dt>

1637 (0x665) 
</dt> <dt>



Windows Installer 服務無法處理此更新套件。 您必須安裝 Windows service pack，其中包含較新版本的 Windows Installer 服務。


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**錯誤 \_ 產品 \_ 版本**
</dt> <dd> <dl> <dt>

1638 (0x666) 
</dt> <dt>



已安裝此產品的其他版本。 無法繼續安裝這個版本。 若要設定或移除此產品的現有版本，請使用主控台上的 [新增/移除程式]。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**錯誤 \_ 不正確 \_ 命令 \_ 行**
</dt> <dd> <dl> <dt>

1639 (0x667) 
</dt> <dt>



不正確命令列引數。 如需詳細的命令列說明，請參閱 Windows Installer SDK。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**不 \_ \_ 允許遠端 \_ 安裝錯誤**
</dt> <dd> <dl> <dt>

1640 (0x668) 
</dt> <dt>



只有系統管理員有權在終端機服務遠端會話期間加入、移除或設定伺服器軟體。 如果您想要在伺服器上安裝或設定軟體，請洽詢您的網路系統管理員。


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**\_起始錯誤成功 \_ 重新開機 \_**
</dt> <dd> <dl> <dt>

1641 (0x669) 
</dt> <dt>



要求的作業已順利完成。 系統將會重新開機，讓變更生效。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**\_ \_ \_ \_ 找不到錯誤修補程式目標**
</dt> <dd> <dl> <dt>

1642 (0x66A) 
</dt> <dt>



Windows Installer 服務無法安裝升級，因為要升級的程式可能已遺失，或升級可能會更新不同版本的程式。 確認要升級的程式存在於您的電腦上，而且您有正確的升級。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**\_拒絕錯誤修補程式 \_ 套件 \_**
</dt> <dd> <dl> <dt>

1643 (0x66B) 
</dt> <dt>



軟體限制原則不允許更新套件。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**\_拒絕安裝 \_ 轉換的錯誤 \_**
</dt> <dd> <dl> <dt>

1644 (0x66C) 
</dt> <dt>



軟體限制原則不允許有一或多個自訂專案。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**\_禁止安裝 \_ 遠端的錯誤 \_**
</dt> <dd> <dl> <dt>

1645 (0x66D) 
</dt> <dt>



Windows Installer 不允許從遠端桌面連線進行安裝。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**\_ \_ 不支援移除錯誤修補程式 \_**
</dt> <dd> <dl> <dt>

1646 (0x66E) 
</dt> <dt>



不支援卸載更新套件。


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**錯誤 \_ 不明的 \_ 修補程式**
</dt> <dd> <dl> <dt>

1647 (0x66F) 
</dt> <dt>



此產品不會套用更新。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**錯誤 \_ 修補程式 \_ 沒有 \_ 順序**
</dt> <dd> <dl> <dt>

1648 (0x670) 
</dt> <dt>



找不到更新集的有效順序。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**不 \_ \_ 允許移除錯誤修補程式 \_**
</dt> <dd> <dl> <dt>

1649 (0x671) 
</dt> <dt>



原則不允許更新移除。


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**錯誤 \_ 不正確 \_ PATCH \_ XML**
</dt> <dd> <dl> <dt>

1650 (0x672) 
</dt> <dt>



XML 更新資料無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**錯誤 \_ 修補 \_ 受管理的 \_ 公告 \_ 產品**
</dt> <dd> <dl> <dt>

1651 (0x673) 
</dt> <dt>



Windows安裝程式不允許更新受管理的公告產品。 套用更新之前，必須先安裝產品的至少一個功能。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**\_安裝 \_ 服務 \_ 安全開機時發生錯誤**
</dt> <dd> <dl> <dt>

1652 (0x674) 
</dt> <dt>



保管庫模式無法存取 Windows Installer 服務。 請在您的電腦未處於保管庫模式時再試一次，也可以使用系統還原將電腦恢復為先前的良好狀態。


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**錯誤 \_ \_ FAST \_ 例外狀況失敗**
</dt> <dd> <dl> <dt>

1653 (0x675) 
</dt> <dt>



發生失敗的快速例外狀況。 系統將不會叫用例外狀況處理常式，而且會立即終止進程。


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**\_拒絕安裝 \_ 錯誤**
</dt> <dd> <dl> <dt>

1654 (0x676) 
</dt> <dt>



此版本的 Windows 不支援您嘗試執行的應用程式。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[系統錯誤碼](system-error-codes.md)
</dt> </dl>

 

 




