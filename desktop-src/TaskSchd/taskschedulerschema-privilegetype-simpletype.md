---
title: privilegeType 簡單類型
description: 許可權會決定使用者帳戶可以執行的系統作業類型。 系統管理員將許可權指派給使用者和群組帳戶。 每個使用者的許可權包含授與使用者的許可權，以及使用者所屬的群組。
ms.assetid: 813b0886-ca76-4523-a1e6-42ca656851a7
keywords:
- privilegeType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- privilegeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4502c22e31ca131dabd6d776337c3693a4d4bf4d7753734cf0e6291cf234fbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002286"
---
# <a name="privilegetype-simple-type"></a>privilegeType 簡單類型

許可權會決定使用者帳戶可以執行的系統作業類型。 系統管理員將許可權指派給使用者和群組帳戶。 每個使用者的許可權包含授與使用者的許可權，以及使用者所屬的群組。

``` syntax
<xs:simpleType name="privilegeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="SeCreateTokenPrivilege"
         />
        <xs:enumeration
            value="SeAssignPrimaryTokenPrivilege"
         />
        <xs:enumeration
            value="SeLockMemoryPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseQuotaPrivilege"
         />
        <xs:enumeration
            value="SeUnsolicitedInputPrivilege"
         />
        <xs:enumeration
            value="SeMachineAccountPrivilege"
         />
        <xs:enumeration
            value="SeTcbPrivilege"
         />
        <xs:enumeration
            value="SeSecurityPrivilege"
         />
        <xs:enumeration
            value="SeTakeOwnershipPrivilege"
         />
        <xs:enumeration
            value="SeLoadDriverPrivilege"
         />
        <xs:enumeration
            value="SeSystemProfilePrivilege"
         />
        <xs:enumeration
            value="SeSystemtimePrivilege"
         />
        <xs:enumeration
            value="SeProfileSingleProcessPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseBasePriorityPrivilege"
         />
        <xs:enumeration
            value="SeCreatePagefilePrivilege"
         />
        <xs:enumeration
            value="SeCreatePermanentPrivilege"
         />
        <xs:enumeration
            value="SeBackupPrivilege"
         />
        <xs:enumeration
            value="SeRestorePrivilege"
         />
        <xs:enumeration
            value="SeShutdownPrivilege"
         />
        <xs:enumeration
            value="SeDebugPrivilege"
         />
        <xs:enumeration
            value="SeAuditPrivilege"
         />
        <xs:enumeration
            value="SeSystemEnvironmentPrivilege"
         />
        <xs:enumeration
            value="SeChangeNotifyPrivilege"
         />
        <xs:enumeration
            value="SeRemoteShutdownPrivilege"
         />
        <xs:enumeration
            value="SeUndockPrivilege"
         />
        <xs:enumeration
            value="SeSyncAgentPrivilege"
         />
        <xs:enumeration
            value="SeEnableDelegationPrivilege"
         />
        <xs:enumeration
            value="SeManageVolumePrivilege"
         />
        <xs:enumeration
            value="SeImpersonatePrivilege"
         />
        <xs:enumeration
            value="SeCreateGlobalPrivilege"
         />
        <xs:enumeration
            value="SeTrustedCredManAccessPrivilege"
         />
        <xs:enumeration
            value="SeRelabelPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseWorkingSetPrivilege"
         />
        <xs:enumeration
            value="SeTimeZonePrivilege"
         />
        <xs:enumeration
            value="SeCreateSymbolicLinkPrivilege"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**PrivilegeType** 簡單類型會定義下列值。



| 值                           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SeCreateTokenPrivilege          | 建立主要權杖所需。 使用者權限：建立 token 物件。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeAssignPrimaryTokenPrivilege   | 指派進程主要權杖的必要項。 使用者權限：取代進程層級的 token。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeLockMemoryPrivilege           | 鎖定記憶體中的實體頁面所需。 使用者權限：鎖定記憶體中的分頁。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeIncreaseQuotaPrivilege        | 需要增加指派給處理常式的配額。 使用者權限：調整進程的記憶體配額。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeUnsolicitedInputPrivilege     | 從終端機裝置讀取未經要求的輸入時需要。 使用者權限：不適用。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SeMachineAccountPrivilege       | 建立電腦帳戶所需。 使用者權限：將工作站新增到網域。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeTcbPrivilege                  | 此許可權會將其持有者識別為受信任電腦基礎的一部分。 某些受信任的受保護子系統被授與此許可權。 使用者權限：作為作業系統的一部分。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SeSecurityPrivilege             | 需要執行一些安全性相關的功能，例如控制和查看審核訊息。 此許可權會將其持有者識別為安全性操作員。 使用者權限：管理審核和安全性記錄。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeTakeOwnershipPrivilege        | 取得物件擁有權而不授與任意存取權的必要項。 此許可權允許將 [擁有者] 值設定為 [擁有者] 可合法指派為物件之擁有者的值。 使用者權限：取得檔案或其他物件的擁有權。 <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| SeLoadDriverPrivilege           | 需要載入或卸載設備磁碟機。 使用者權限：載入和卸載設備磁碟機。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemProfilePrivilege        | 需要收集整個系統的程式碼剖析資訊。 使用者權限：配置檔案系統效能。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemtimePrivilege           | 修改系統時間所需。 使用者權限：變更系統時間。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeProfileSingleProcessPrivilege | 需要收集單一進程的程式碼剖析資訊。 使用者權限：設定檔單一進程。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseBasePriorityPrivilege | 需要提高進程的基本優先權。 使用者權限：提高排程優先權。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeCreatePagefilePrivilege       | 建立分頁檔案所需。 使用者權限：建立分頁檔。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| SeCreatePermanentPrivilege      | 建立永久物件時所需。 使用者權限：建立永久共用物件。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SeBackupPrivilege               | 執行備份作業所需。 此許可權可讓系統將所有讀取存取控制授與任何檔案，而不論 (ACL) 為檔案指定的存取控制清單。 除了讀取以外的任何存取要求仍會以 ACL 進行評估。 RegSaveKey 和 RegSaveKeyExfunctions 都需要此許可權。 如果保留此許可權，則會授與下列存取權限：讀取 \_ 控制、存取 \_ 系統 \_ 安全性、檔案 \_ 一般 \_ 讀取、 \_ 檔案往返。 使用者權限：備份檔案和目錄。 <br/>                                                                                                                                     |
| SeRestorePrivilege              | 執行還原作業所需。 無論為檔案指定的 ACL 為何，此許可權都會讓系統將所有寫入存取控制授與任何檔案。 寫入以外的任何存取要求仍會以 ACL 進行評估。 此外，此許可權可讓您將任何有效的使用者或群組安全性識別元 (SID) 做為檔案的擁有者。 RegLoadKey 函式需要此許可權。 如果保留此許可權，則會授與下列存取權限：寫入 \_ DAC、寫入 \_ 擁有者、存取 \_ 系統 \_ 安全性、檔案 \_ 一般 \_ 寫入、檔案新增檔案、檔案 \_ \_ \_ 新增 \_ 子目錄、刪除。 使用者權限：還原檔案和目錄。 <br/> |
| SeShutdownPrivilege             | 關閉本機系統的必要參數。 使用者權限：關閉系統。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeDebugPrivilege                | 需要對其他帳戶所擁有之進程的記憶體進行 debug 和調整。 使用者權限：偵錯工具。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeAuditPrivilege                | 產生 audit 記錄檔專案的必要專案。 授與此許可權以保護伺服器。 使用者權限：產生安全性審核。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SeSystemEnvironmentPrivilege    | 需要修改使用這種記憶體類型之系統的靜態 RAM 來儲存設定資訊。 使用者權限：修改固件環境值。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeChangeNotifyPrivilege         | 需要接收檔案或目錄變更的通知。 此許可權也會導致系統略過所有的遍歷存取檢查。 預設會針對所有使用者啟用。 使用者權限：略過遍歷檢查。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeRemoteShutdownPrivilege       | 需要使用網路要求關閉系統。 使用者權限：強制從遠端系統關機。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SeUndockPrivilege               | 卸載膝上型電腦的必要。 使用者權限：從銜接站移除電腦。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeSyncAgentPrivilege            | 網域控制站在使用 LDAP 目錄同步處理服務時所需。 此許可權可讓持有者讀取目錄中的所有物件和屬性，不論物件和屬性的保護為何。 依預設，它會指派給網域控制站上的系統管理員和 LocalSystem 帳戶。 使用者權限：同步目錄服務資料。 <br/>                                                                                                                                                                                                                                                                                |
| SeEnableDelegationPrivilege     | 將使用者和電腦帳戶標示為受信任以進行委派時，需要此參數。 使用者權限：啟用受信任的電腦和使用者帳戶以進行委派。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeManageVolumePrivilege         | 啟用磁片區管理許可權的必要元件。 使用者權限：管理磁片區上的檔案。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeImpersonatePrivilege          | 需要模擬。 使用者權限：在驗證之後模擬用戶端。 WindowsXP/2000：不支援此許可權。 <br/> 請注意，從 Windows Server 2003、Windows XP SP2 和 Windows 2000 加裝 SP4 開始支援此值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateGlobalPrivilege         | 在終端機服務會話期間，必須在全域命名空間中建立指名的檔案對應物件。 系統管理員、服務和本機系統帳戶預設會啟用此許可權。 使用者權限：建立全域物件。 WindowsXP/2000：不支援此許可權。 <br/> 請注意，從 Windows Server 2003、Windows XP SP2 和 Windows 2000 加裝 SP4 開始支援此值。<br/>                                                                                                                                                                                                                                        |
| SeTrustedCredManAccessPrivilege | 以信任的呼叫端存取認證管理員所需。 使用者權限：存取認證管理員作為受信任的呼叫者。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeRelabelPrivilege              | 修改物件的強制完整性層級所需。 使用者權限：修改物件標籤。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseWorkingSetPrivilege   | 配置更多記憶體給在使用者的環境中執行的應用程式所需。 使用者權限：提高進程的工作集。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SeTimeZonePrivilege             | 需要調整與電腦內部時鐘相關聯的時區。 使用者權限：變更時區。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateSymbolicLinkPrivilege   | 建立符號連結所需。 使用者權限：建立符號連結。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 





