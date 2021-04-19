---
description: Windows 安全性模型可讓您控制服務控制管理員 (SCM) 和服務物件的存取權。
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: 服務安全性與存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978139"
---
# <a name="service-security-and-access-rights"></a>服務安全性與存取權限

Windows 安全性模型可讓您控制服務控制管理員 (SCM) 和服務物件的存取權。 下列各節提供詳細資訊：

-   [服務控制管理員的存取權限](#access-rights-for-the-service-control-manager)
-   [服務的存取權限](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a>服務控制管理員的存取權限

以下是 SCM 的特定存取權限。



| 存取權限                                   | Description                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SC \_管理員 \_ 所有 \_ 存取** (0xF003F)          | 除了此資料表中的所有存取權限之外，還包含 **\_ \_ 所需的標準許可權**。                                                                                                                                                                                                                                                                                 |
| **SC \_MANAGER \_ 建立 \_ 服務** (0x0002)       | 需要呼叫 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函式來建立服務物件，並將它加入至資料庫。                                                                                                                                                                                                                                              |
| **SC \_MANAGER \_ CONNECT** (0x0001)               | 連接至服務控制管理員所需。                                                                                                                                                                                                                                                                                                                      |
| **SC \_管理員 \_ 列舉 \_ 服務** (0x0004)    | 需要呼叫 [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) 或 [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) 函式，以列出資料庫中的服務。<br/> 在建立或刪除任何服務時，呼叫 [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) 函式以接收通知的必要項。<br/> |
| **SC \_管理員 \_ 鎖定** (0x0008)                  | 需要呼叫 [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) 函數，才能取得資料庫的鎖定。                                                                                                                                                                                                                                                      |
| **SC \_MANAGER \_ 修改 \_ 開機 \_** 設定 (0x0020)  | 需要呼叫 [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) 函數。                                                                                                                                                                                                                                                                                  |
| **SC \_管理員 \_ 查詢 \_ 鎖定 \_ 狀態** (0x0010)   | 需要呼叫 [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) 函數，才能取得資料庫的鎖定狀態資訊。                                                                                                                                                                                                                         |



 

以下是 SCM 的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。



<table>
<thead>
<tr class="header">
<th>存取權限</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SC_MANAGER_CREATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_LOCK</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_ALL</strong></td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

具有正確存取權限的進程可以開啟可在 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)、 [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)和 [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) 函式中使用之 SCM 的控制碼。 只有具備系統管理員許可權的進程才能開啟 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 和 [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) 函式可使用的 SCM 控制碼。

系統會建立 SCM 的安全描述項。 若要取得或設定 SCM 的安全描述項，請使用 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 和 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函數搭配 SCManager 物件的控制碼。

**Windows Server 2003 和 WINDOWS XP：** 與大部分其他安全物件不同的是，無法修改 SCM 的安全描述項。 此行為已從 Windows Server 2003 Service Pack 1 (SP1) 變更。

系統會授與下列存取權限。



<table>
<thead>
<tr class="header">
<th>帳戶</th>
<th>存取權限</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>遠端驗證的使用者</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>本機驗證的使用者 (包括 LocalService 和 NetworkService) </td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>系統管理員</td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

請注意，透過網路驗證的遠端使用者（而不是以互動方式登入）可以連接到 SCM，但無法執行需要其他存取權限的作業。 若要執行這些作業，使用者必須以互動方式登入，或服務必須使用其中一個服務帳戶。

**Windows Server 2003 和 WINDOWS XP：** 遠端驗證的使用者會被授與 **sc \_ manager \_ CONNECT**、 **sc \_ manager \_ 列舉 \_ 服務**、 **sc \_ manager \_ 查詢 \_ 鎖定 \_ 狀態**，以及 **標準 \_ 許可權 \_ 讀取** 存取權限。 從 Windows Server 2003 （含 SP1）開始，這些存取權限受限於上表所述

當進程使用 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式來開啟已安裝服務之資料庫的控制碼時，它可以要求存取權限。 在授與所要求的存取權限之前，系統會針對 SCM 的安全描述項執行安全性檢查。

## <a name="access-rights-for-a-service"></a>服務的存取權限

以下是服務的特定存取權限。



| 存取權限                                | Description                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **服務 \_所有 \_ 存取** (0xF01FF)           | 除了此資料表中的所有存取權限之外，還包含 **\_ \_ 所需的標準許可權** 。                                                                                                                                                                                                                                                                                              |
| **服務 \_變更 \_ CONFIG** (0x0002)         | 需要呼叫 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 或 [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) 函式來變更服務設定。 因為這會授與呼叫者變更系統所執行之可執行檔的許可權，所以只能授與系統管理員。                                                              |
| **服務 \_列舉相依 \_ 項** (0x0008)  | 需要呼叫 [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) 函式，以列舉相依于服務的所有服務。                                                                                                                                                                                                                                         |
| **服務 \_查閱 (0x0080**)            | 需要呼叫 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函式，才能要求服務立即報告其狀態。                                                                                                                                                                                                                                                          |
| **服務 \_暫停 \_ 繼續** (0x0040)        | 需要呼叫 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函式來暫停或繼續服務。                                                                                                                                                                                                                                                                             |
| **服務 \_查詢 \_** 設定 (0x0001)          | 需要呼叫 [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) 和 [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) 函數才能查詢服務設定。                                                                                                                                                                                                           |
| **服務 \_查詢 \_ 狀態** (0x0004)          | 需要呼叫 [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) 或 [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) 函式，才能向服務控制管理員要求服務的狀態。<br/> 當服務變更狀態時，需要呼叫 [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) 函式來接收通知。<br/> |
| **服務 \_開始** (0x0010)                  | 呼叫 [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) 函式來啟動服務時所需。                                                                                                                                                                                                                                                                                             |
| **服務 \_停止** (0x0020)                   | 需要呼叫 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函式來停止服務。                                                                                                                                                                                                                                                                                          |
| **服務 \_使用者 \_ 定義 \_ 控制項** (0x0100)  | 呼叫 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函式來指定使用者定義的控制項程式碼時，需要用到。                                                                                                                                                                                                                                                                       |



 

以下是服務的 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) 。



| 存取權限                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **存取 \_ 系統 \_ 安全性** | 呼叫 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 或 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函式以存取 SACL 的必要參數。 取得此存取權的正確方式是在呼叫端的目前存取權杖中啟用「 **SE \_ 安全性 \_ 名稱**」[**許可權**](/windows/desktop/SecAuthZ/privileges)、開啟 **存取 \_ 系統 \_ 安全性** 存取的控制碼，然後停用該許可權。 |
| **刪除**   (0x10000)        | 呼叫 [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) 函數來刪除服務的必要參數。                                                                                                                                                                                                                                                                                                                                                  |
| **讀取 \_控制**  (0x20000)     | 呼叫 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 函數來查詢服務物件的安全描述項時，需要此項。                                                                                                                                                                                                                                                                                  |
| **寫入 \_DAC**  (0x40000)     | 需要呼叫 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函式，才能修改服務物件安全描述項的 **Dacl** 成員。                                                                                                                                                                                                                                                                   |
| **寫入 \_擁有** 者 (0x80000)    | 需要呼叫 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函式，才能修改服務物件安全描述項的 **擁有** 者和 **群組** 成員。                                                                                                                                                                                                                                                   |



 

以下是服務的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。



<table>
<thead>
<tr class="header">
<th>存取權限</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SERVICE_CHANGE_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

當 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函數安裝服務時，SCM 會建立服務物件的安全描述項。 服務物件的預設安全描述項會授與下列存取權。



<table>
<thead>
<tr class="header">
<th>帳戶</th>
<th>存取權限</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>遠端驗證的使用者</td>
<td>預設不會授與。<strong>Windows Server 2003 SP1： SERVICE_USER_DEFINED_CONTROL</strong><br/> <strong>Windows Server 2003 和 WINDOWS XP：</strong> 遠端驗證使用者的存取權限與本機驗證使用者的存取權限相同。<br/></td>
</tr>
<tr class="even">
<td>本機驗證的使用者 (包括 LocalService 和 NetworkService) </td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>系統管理員</td>
<td><dl> <strong>DELETE</strong><br />
<strong>READ_CONTROL</strong><br />
<strong>SERVICE_ALL_ACCESS</strong><br />
<strong>WRITE_DAC</strong><br />
<strong>WRITE_OWNER</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

若要執行任何作業，使用者必須以互動方式登入，或服務必須使用其中一個服務帳戶。

若要取得或設定服務物件的安全描述項，請使用 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 和 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函數。 如需詳細資訊，請參閱 [修改服務的 DACL](modifying-the-dacl-for-a-service.md)。

當進程使用 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) 函式時，系統會根據服務物件的安全描述項來檢查要求的存取權限。

授與不受信任使用者的特定存取權限 (例如 **服務 \_ 變更 \_** 設定或 **服務 \_ 停止**) 可讓他們干擾您的服務執行，而且可能會允許他們在 LocalSystem 帳戶下執行應用程式。

呼叫 [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) 函式時，如果呼叫端沒有服務的 **服務 \_ 查詢 \_ 狀態** 存取權，則會從傳回給用戶端的服務清單中，以無訊息方式省略服務。

 

