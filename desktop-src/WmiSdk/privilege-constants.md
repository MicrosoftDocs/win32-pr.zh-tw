---
description: SWbemPrivilegeSet. AddAsString 方法的 strPrivilege 參數和 SWbemPrivilegeSet 的 iPrivilege 參數。 Add 需要 WbemPrivilegeEnum 的許可權字串。
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: '許可權常數 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 38d104c99885d4328ce8b12413e91607655ab1e260a61b511e3ea4a600b80b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131020"
---
# <a name="privilege-constants"></a>許可權常數

[**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md)方法的 *StrPrivilege* 參數和 SWbemPrivilegeSet 的 *IPrivilege* 參數 [**。 Add**](swbemprivilegeset-add.md)需要 [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)的許可權字串。 如需如何使用許可權常數的詳細資訊，請參閱 [執行特殊許可權作業](executing-privileged-operations.md)。

下列常數定義于 [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)中。 下列清單包含 c + + 和字串的對等常數，用於編寫腳本。 若要形成腳本簡短名稱，請從 c + + 常數名稱中移除「Se」和「許可權」。

下列 VBScript 程式碼範例顯示如何在腳本中啟用 RemoteShutdown 許可權。


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



許多 WMI 方法都需要啟用一或多個許可權。 如果尚未授與帳戶許可權，就無法針對方法呼叫啟用該帳戶。

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



c + + 常數： **SE \_ 建立 \_ 權杖 \_ 名稱** 字串： **SeCreateTokenPrivilege**

腳本簡短名稱： **CreateToken**

建立主要權杖物件的必要參數。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**
</dt> <dd> <dl> <dt>

2 (0x2) 
</dt> <dt>



C + + 常數： **SeAssignPrimaryTokenPrivilege** 字串： **SeAssignPrimaryTokenPrivilege**

腳本簡短名稱： **AssignPrimaryToken**

取代進程層級 token 所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**
</dt> <dd> <dl> <dt>

3 (0x3) 
</dt> <dt>



c + + 常數： **SE \_ 鎖定 \_ 記憶體 \_ 名稱** 字串： **SeLockMemoryPrivilege**

腳本簡短名稱： **LockMemory**

鎖定記憶體中的分頁所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**
</dt> <dd> <dl> <dt>

4 (0x4) 
</dt> <dt>



c + + 常數： **SE \_ 增加 \_ 配額 \_ 名稱** 字串： **SeIncreaseQuotaPrivilege**

腳本簡短名稱： **IncreaseQuotaPrivilege**

調整進程的記憶體配額所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**
</dt> <dd> <dl> <dt>

5 (0x5) 
</dt> <dt>



c + + 常數： **SE \_ MACINE \_ 帳戶 \_ 名稱** 字串： **SeMachineAccountPrivilege**

腳本簡短名稱： **MachineAccount**

將工作站新增到網域的必要。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**
</dt> <dd> <dl> <dt>

6 (0x6) 
</dt> <dt>



c + + 常數： **SE \_ TCB \_ 名稱** 字串： **SeTcbPrivilege**

腳本簡短名稱： **Tcb**

需要作為作業系統的一部分。 持有者是受信任電腦基礎的一部分。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**
</dt> <dd> <dl> <dt>

7 (0x7) 
</dt> <dt>



c + + 常數： **SE \_ 安全性 \_ 名稱** 字串： **SeSecurityPrivilege**

腳本簡短名稱： **安全性**

管理審核和 NT 安全性記錄檔所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**
</dt> <dd> <dl> <dt>

8 (0x8) 
</dt> <dt>



c + + 常數： **SE \_ 取得 \_ 擁有權 \_ 名稱** 字串： **SeTakeOwnershipPrivilege**

腳本簡短名稱： **TakeOwnership**

需要擁有檔案或其他物件的擁有權，而不需要 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ACE) 在 *任意存取控制清單* (DACL) 中。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**
</dt> <dd> <dl> <dt>

9 (0x9) 
</dt> <dt>



c + + 常數： **SE \_ 載入 \_ 驅動程式** 字串： **SeLoadDriverPrivilege**

腳本簡短名稱： **LoadDriver**

需要載入或卸載設備磁碟機。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**
</dt> <dd> <dl> <dt>

10 (0xA) 
</dt> <dt>



c + + 常數： **SE \_ 系統 \_ 設定檔 \_ 名稱** 字串： **SeSystemProfilePrivilege**

腳本簡短名稱： **SystemProfile**

需要收集有關系統效能的設定檔資訊。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**
</dt> <dd> <dl> <dt>

11 (0xB) 
</dt> <dt>



c + + 常數： **SE \_ SYSTEMTIME** \_ 名稱字串： **SeSystemtimePrivilege**

腳本簡短名稱： **Systemtime**

變更系統時間所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**
</dt> <dd> <dl> <dt>

12 (0xC) 
</dt> <dt>



c + + 常數： **SE \_ 獲 \_ 單一 \_ 進程 \_ 名稱** 字串： **SeProfileSingleProcessPrivilege**

腳本簡短名稱： **ProfileSingleProcess**

需要收集單一進程的設定檔資訊。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**
</dt> <dd> <dl> <dt>

13 (0xD) 
</dt> <dt>



c + + 常數： **SE \_ inc. \_ 基底 \_ 優先順序 \_ 名稱** 字串： **SeIncreaseBasePriorityPrivilege**

腳本簡短名稱： **IncreaseBasePriority**

增加排程優先順序所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**
</dt> <dd> <dl> <dt>

14 (0xE) 
</dt> <dt>



c + + 常數： **SE \_ 建立 \_ 分頁檔 \_ 名稱** 字串： **SeCreatePagefilePrivilege**

腳本簡短名稱： **CreatePagefile**

建立分頁檔所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**
</dt> <dd> <dl> <dt>

15 (0xF) 
</dt> <dt>



c + + 常數： **SE \_ 建立 \_ 永久 \_ 名稱** 字串： **SeCreatePermanentPrivilege**

腳本簡短名稱： **CreatePermanent**

建立永久共用物件時所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**
</dt> <dd> <dl> <dt>

16 (0x10) 
</dt> <dt>



c + + 常數： **SE \_ 備份 \_ 名稱** 字串： **SeBackupPrivilege**

腳本簡短名稱： **備份**

備份檔案和目錄的必要項，不論為檔案指定的 ACL 為何。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**
</dt> <dd> <dl> <dt>

17 (0x11) 
</dt> <dt>



c + + 常數： **SE \_ 還原 \_ 名稱** 字串： **SeRestorePrivilege**

腳本簡短名稱： **還原**

還原檔案和目錄的必要項，不論為檔案指定的 ACL 為何。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**
</dt> <dd> <dl> <dt>

18 (0x12) 
</dt> <dt>



c + + 常數： **SE \_ 關閉 \_ 名稱** 字串： **SeShutdownPrivilege**

腳本簡短名稱： **關機**

關閉本機系統的必要參數。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**
</dt> <dd> <dl> <dt>

19 (0x13) 
</dt> <dt>



c + + 常數： **SE \_ DEBUG \_ NAME** string： **SeDebugPrivilege**

腳本簡短名稱： **Debug**

需要對其他帳戶所擁有之進程的記憶體進行 debug 和調整。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**
</dt> <dd> <dl> <dt>

20 (0x14) 
</dt> <dt>



c + + 常數： **SE \_ AUDIT \_ NAME** string： **SeAuditPrivilege**

腳本簡短名稱： **Audit**

在 NT 安全性記錄檔中產生 audit 專案的必要專案。 只有安全的伺服器才應該具有此許可權。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**
</dt> <dd> <dl> <dt>

21 (0x15) 
</dt> <dt>



c + + 常數： **SE \_ 系統 \_ 環境 \_ 名稱** 字串： **SeSystemEnvironmentPrivilege**

腳本簡短名稱： **SystemEnvironment**

修改使用這種記憶體類型之系統的非靜態 RAM 來儲存設定資料時，需要用到。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**
</dt> <dd> <dl> <dt>

22 (0x16) 
</dt> <dt>



c + + 常數： **SE \_ 變更 \_ 通知 \_ 名稱** 字串： **SeChangeNotifyPrivilege**

腳本簡短名稱： **ChangeNotify**

需要接收檔案或目錄變更的通知，以及略過遍歷存取檢查。 依預設，所有使用者都會啟用此許可權。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**
</dt> <dd> <dl> <dt>

23 (0x17) 
</dt> <dt>



c + + 常數： **SE \_ 遠端 \_ 關機 \_ 名稱** 字串： **SeRemoteShutdownPrivilege**

腳本簡短名稱： **RemoteShutdown**

關閉遠端電腦所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**
</dt> <dd> <dl> <dt>

24 (0x18) 
</dt> <dt>



c + + 常數： **SE \_ 移除的 \_ 名稱** 字串： **SeUndockPrivilege**

腳本簡短 **名稱：卸載**

從銜接站移除膝上型電腦的必要。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**
</dt> <dd> <dl> <dt>

25 (0x19) 
</dt> <dt>



c + + 常數： **SE \_ 同步 \_ 代理程式 \_ 名稱** 字串： **SeSyncAgentPrivilege**

腳本簡短名稱： **SyncAgent**

同步目錄服務資料所需。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**
</dt> <dd> <dl> <dt>

26 (0x1A) 
</dt> <dt>



c + + 常數： **SE \_ 啟用 \_ 委派 \_ 名稱** 字串： **SeEnableDelegationPrivilege**

腳本簡短名稱： **EnableDelegation**

讓電腦和使用者帳戶受到信任以進行委派的必要。


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**
</dt> <dd> <dl> <dt>

27 (0x1B) 
</dt> <dt>



c + + 常數： **SE \_ 管理 \_ 磁片區 \_ 名稱** 字串： **SeManageVolumePrivilege**

腳本簡短名稱： **ManageVolume**

執行磁片區維護工作的必要作業。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>Wbemdisp.tlb .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 常數](scripting-api-constants.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[執行具有特殊許可權的作業](executing-privileged-operations.md)
</dt> <dt>

[使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

