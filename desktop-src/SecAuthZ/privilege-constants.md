---
Description: 許可權會決定使用者帳戶可以執行的系統作業類型。 系統管理員將許可權指派給使用者和群組帳戶。 每個使用者的許可權包含授與使用者的許可權，以及使用者所屬的群組。
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: " (Winnt. h) 的許可權常數"
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5da0a0e6f9ad3b0559fdf2d8e375e6d25e7d2fdf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475740"
---
# <a name="privilege-constants-authorization"></a>許可權常數 (授權) 

許可權會決定使用者帳戶可以執行的系統作業類型。 系統管理員將許可權指派給使用者和群組帳戶。 每個使用者的許可權包含授與使用者的許可權，以及使用者所屬的群組。

取得和調整 [*存取權杖*](/windows/desktop/SecGloss/a-gly) 中之許可權的函式會使用 [*本機唯一識別碼*](/windows/desktop/SecGloss/l-gly) (LUID) 類型來識別許可權。 您可以使用 [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) 函數來判斷本機系統上對應到許可權常數的 [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) 。 您可以使用 [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) 函式，將 **LUID** 轉換為其對應的字串常數。

作業系統表示許可權，方法是使用下表的 [描述] 資料行中「使用者權限」之後的字串。 作業系統會在 [本機安全性設定 Microsoft Management Console (MMC) 嵌入式管理單元的 [**使用者權限指派**] 節點的 [**原則**] 欄中顯示使用者右邊的字串。

## <a name="example"></a>範例

```cpp
BOOL EnablePrivilege()
{
    LUID PrivilegeRequired ;
    BOOL bRes = FALSE;
  
    bRes = LookupPrivilegeValue(NULL, SE_DEBUG_NAME, &PrivilegeRequired);

    // ...

    return bRes;
}
```
GitHub 上[Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c)的範例。

## <a name="constants"></a>常數



| 常數/值 | Description | 
|----------------|-------------|
| <span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl><dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt><dt>文字 ( "SeAssignPrimaryTokenPrivilege" ) </dt></dl> | 指派進程 <a href="/windows/desktop/SecGloss/p-gly"><em>主要權杖</em></a> 的必要項。 <br /> 使用者權限：取代進程層級的 token。<br /> | 
| <span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl><dt><strong>SE_AUDIT_NAME</strong></dt><dt>文字 ( "SeAuditPrivilege" ) </dt></dl> | 產生 audit 記錄檔專案的必要專案。 授與此許可權以保護伺服器。 <br /> 使用者權限：產生安全性審核。<br /> | 
| <span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl><dt><strong>SE_BACKUP_NAME</strong></dt><dt>文字 ( "SeBackupPrivilege" ) </dt></dl> | 執行備份作業所需。 此許可權可讓系統將所有讀取存取控制授與任何檔案，而不論 (ACL) 為檔案指定的 <a href="/windows/desktop/SecGloss/a-gly"><em>存取控制清單</em></a> 。 除了讀取以外的任何存取要求仍會以 ACL 進行評估。 <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegSaveKey</strong></a>和<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>函數需要此許可權。 如果保留此許可權，則會授與下列存取權限：<br /><ul><li>READ_CONTROL</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_READ</li><li>FILE_TRAVERSE</li></ul>使用者權限：備份檔案和目錄。<br />如果檔案位於卸載式磁片磁碟機上，且已啟用「Audit 可移動儲存體」，則 SE_SECURITY_NAME 必須具有 ACCESS_SYSTEM_SECURITY。 | 
| <span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl><dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt><dt>文字 ( "SeChangeNotifyPrivilege" ) </dt></dl> | 需要接收檔案或目錄變更的通知。 此許可權也會導致系統略過所有的遍歷存取檢查。 預設會針對所有使用者啟用。 <br /> 使用者權限：略過遍歷檢查。<br /> | 
| <span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl><dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt><dt>文字 ( "SeCreateGlobalPrivilege" ) </dt></dl> | 在終端機服務會話期間，必須在全域命名空間中建立指名的檔案對應物件。 系統管理員、服務和本機系統帳戶預設會啟用此許可權。<br /> 使用者權限：建立全域物件。<br /> | 
| <span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl><dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt><dt>文字 ( "SeCreatePagefilePrivilege" ) </dt></dl> | 建立分頁檔案所需。 <br /> 使用者權限：建立分頁檔。<br /> | 
| <span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl><dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt><dt>文字 ( "SeCreatePermanentPrivilege" ) </dt></dl> | 建立永久物件時所需。 <br /> 使用者權限：建立永久共用物件。<br /> | 
| <span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl><dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt><dt>文字 ( "SeCreateSymbolicLinkPrivilege" ) </dt></dl> | 建立符號連結所需。<br /> 使用者權限：建立符號連結。<br /> | 
| <span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl><dt><strong>SE_CREATE_TOKEN_NAME</strong></dt><dt>文字 ( "SeCreateTokenPrivilege" ) </dt></dl> | 建立主要權杖所需。 <br /> 使用者權限：建立 token 物件。<br /> 您無法將此許可權新增至具有「建立權杖物件」原則的使用者帳戶。 此外，您無法使用 Windows api，將此許可權新增至擁有的進程。<strong>Windows Server 2003 和 Windows XP SP1 及更早版本：</strong> Windows api 可以將此許可權新增至擁有的進程。<br /><br /> | 
| <span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl><dt><strong>SE_DEBUG_NAME</strong></dt><dt>文字 ( "SeDebugPrivilege" ) </dt></dl> | 需要對其他帳戶所擁有之進程的記憶體進行 debug 和調整。 <br /> 使用者權限：偵錯工具。<br /> | 
| <span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl><dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt><dt>文字 ( "SeDelegateSessionUserImpersonatePrivilege" ) </dt></dl> | 需要在相同的會話中取得其他使用者的模擬權杖。 <br /> 使用者權限：模擬其他使用者。<br /> | 
| <span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl><dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt><dt>文字 ( "SeEnableDelegationPrivilege" ) </dt></dl> | 將使用者和電腦帳戶標示為受信任以進行委派時，需要此參數。<br /> 使用者權限：啟用受信任的電腦和使用者帳戶以進行委派。<br /> | 
| <span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl><dt><strong>SE_IMPERSONATE_NAME</strong></dt><dt>文字 ( "SeImpersonatePrivilege" ) </dt></dl> | 需要模擬。<br /> 使用者權限：在驗證之後模擬用戶端。<br /> | 
| <span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl><dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt><dt>文字 ( "SeIncreaseBasePriorityPrivilege" ) </dt></dl> | 需要提高進程的基本優先權。 <br /> 使用者權限：提高排程優先權。<br /> | 
| <span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl><dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt><dt>文字 ( "SeIncreaseQuotaPrivilege" ) </dt></dl> | 需要增加指派給處理常式的配額。 <br /> 使用者權限：調整進程的記憶體配額。<br /> | 
| <span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl><dt><strong>SE_INC_WORKING_SET_NAME</strong></dt><dt>文字 ( "SeIncreaseWorkingSetPrivilege" ) </dt></dl> | 配置更多記憶體給在使用者的環境中執行的應用程式所需。<br /> 使用者權限：提高進程的工作集。<br /> | 
| <span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl><dt><strong>SE_LOAD_DRIVER_NAME</strong></dt><dt>文字 ( "SeLoadDriverPrivilege" ) </dt></dl> | 需要載入或卸載設備磁碟機。 <br /> 使用者權限：載入和卸載設備磁碟機。<br /> | 
| <span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl><dt><strong>SE_LOCK_MEMORY_NAME</strong></dt><dt>文字 ( "SeLockMemoryPrivilege" ) </dt></dl> | 鎖定記憶體中的實體頁面所需。 <br /> 使用者權限：鎖定記憶體中的分頁。<br /> | 
| <span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl><dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt><dt>文字 ( "SeMachineAccountPrivilege" ) </dt></dl> | 建立電腦帳戶所需。 <br /> 使用者權限：將工作站新增到網域。<br /> | 
| <span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl><dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt><dt>文字 ( "SeManageVolumePrivilege" ) </dt></dl> | 啟用磁片區管理許可權的必要元件。 <br /> 使用者權限：管理磁片區上的檔案。<br /> | 
| <span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl><dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt><dt>文字 ( "SeProfileSingleProcessPrivilege" ) </dt></dl> | 需要收集單一進程的程式碼剖析資訊。 <br /> 使用者權限：設定檔單一進程。<br /> | 
| <span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl><dt><strong>SE_RELABEL_NAME</strong></dt><dt>文字 ( "SeRelabelPrivilege" ) </dt></dl> | 修改物件的強制完整性層級所需。<br /> 使用者權限：修改物件標籤。<br /> | 
| <span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl><dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt><dt>文字 ( "SeRemoteShutdownPrivilege" ) </dt></dl> | 需要使用網路要求關閉系統。 <br /> 使用者權限：強制從遠端系統關機。<br /> | 
| <span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl><dt><strong>SE_RESTORE_NAME</strong></dt><dt>文字 ( "SeRestorePrivilege" ) </dt></dl> | 執行還原作業所需。 無論為檔案指定的 ACL 為何，此許可權都會讓系統將所有寫入存取控制授與任何檔案。 寫入以外的任何存取要求仍會以 ACL 進行評估。 此外，此許可權可讓您將任何有效的使用者或群組 SID 設定為檔案的擁有者。 <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey</strong></a>函式需要此許可權。 如果保留此許可權，則會授與下列存取權限：<br /><ul><li>WRITE_DAC</li><li>WRITE_OWNER</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_WRITE</li><li>FILE_ADD_FILE</li><li>FILE_ADD_SUBDIRECTORY</li><li>DELETE</li></ul>使用者權限：還原檔案和目錄。<br />如果檔案位於卸載式磁片磁碟機上，且已啟用「Audit 可移動儲存體」，則 SE_SECURITY_NAME 必須具有 ACCESS_SYSTEM_SECURITY。<br /> | 
| <span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl><dt><strong>SE_SECURITY_NAME</strong></dt><dt>文字 ( "SeSecurityPrivilege" ) </dt></dl> | 需要執行一些安全性相關的功能，例如控制和查看審核訊息。 此許可權會將其持有者識別為安全性操作員。 <br /> 使用者權限：管理審核和安全性記錄。<br /> | 
| <span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl><dt><strong>SE_SHUTDOWN_NAME</strong></dt><dt>文字 ( "SeShutdownPrivilege" ) </dt></dl> | 關閉本機系統的必要參數。 <br /> 使用者權限：關閉系統。<br /> | 
| <span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl><dt><strong>SE_SYNC_AGENT_NAME</strong></dt><dt>文字 ( "SeSyncAgentPrivilege" ) </dt></dl> | 網域控制站在使用 <a href="/windows/desktop/SecGloss/l-gly"><em>輕量型目錄存取協定</em></a> 目錄同步處理服務時所需。 此許可權可讓持有者讀取目錄中的所有物件和屬性，不論物件和屬性的保護為何。 依預設，它會指派給網域控制站上的系統管理員和 LocalSystem 帳戶。 <br /> 使用者權限：同步目錄服務資料。<br /> | 
| <span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl><dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt><dt>文字 ( "SeSystemEnvironmentPrivilege" ) </dt></dl> | 需要修改使用這種記憶體類型之系統的靜態 RAM 來儲存設定資訊。 <br /> 使用者權限：修改固件環境值。<br /> | 
| <span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl><dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt><dt>文字 ( "SeSystemProfilePrivilege" ) </dt></dl> | 需要收集整個系統的程式碼剖析資訊。 <br /> 使用者權限：配置檔案系統效能。<br /> | 
| <span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl><dt><strong>SE_SYSTEMTIME_NAME</strong></dt><dt>文字 ( "SeSystemtimePrivilege" ) </dt></dl> | 修改系統時間所需。 <br /> 使用者權限：變更系統時間。<br /> | 
| <span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl><dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt><dt>文字 ( "SeTakeOwnershipPrivilege" ) </dt></dl> | 取得物件擁有權而不授與任意存取權的必要項。 此許可權允許將 [擁有者] 值設定為 [擁有者] 可合法指派為物件之擁有者的值。 <br /> 使用者權限：取得檔案或其他物件的擁有權。<br /> | 
| <span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl><dt><strong>SE_TCB_NAME</strong></dt><dt>文字 ( "SeTcbPrivilege" ) </dt></dl> | 此許可權會將其持有者識別為受信任電腦基礎的一部分。 某些受信任的受保護子系統被授與此許可權。 <br /> 使用者權限：作為作業系統的一部分。<br /> | 
| <span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl><dt><strong>SE_TIME_ZONE_NAME</strong></dt><dt>文字 ( "SeTimeZonePrivilege" ) </dt></dl> | 需要調整與電腦內部時鐘相關聯的時區。<br /> 使用者權限：變更時區。<br /> | 
| <span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl><dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt><dt>文字 ( "SeTrustedCredManAccessPrivilege" ) </dt></dl> | 以信任的呼叫端存取認證管理員所需。<br /> 使用者權限：存取認證管理員作為受信任的呼叫者。<br /> | 
| <span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl><dt><strong>SE_UNDOCK_NAME</strong></dt><dt>文字 ( "SeUndockPrivilege" ) </dt></dl> | 卸載膝上型電腦的必要。<br /> 使用者權限：從銜接站移除電腦。<br /> | 
| <span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl><dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt><dt>文字 ( "SeUnsolicitedInputPrivilege" ) </dt></dl> | 從 <a href="/windows/desktop/SecGloss/t-gly"><em>終端</em></a> 機裝置讀取未經要求的輸入時需要。<br /> 使用者權限：不適用。<br /> | 




## <a name="remarks"></a>備註

許可權常數在 Winnt 中會定義為字串。 例如，SE \_ AUDIT \_ NAME 常數定義為 "SeAuditPrivilege"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Winnt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[特權](privileges.md)
</dt> </dl>

