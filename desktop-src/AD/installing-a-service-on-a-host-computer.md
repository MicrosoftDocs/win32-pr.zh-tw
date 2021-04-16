---
title: 在主機電腦上安裝服務
description: 下列程式碼範例顯示在主機電腦上安裝啟用目錄的服務的基本步驟。
ms.assetid: 35a3b261-d499-4154-a022-1e33a9ef7ba8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d687bbbfadb4d1ccb789e9d5f1051ebfbb4484d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462849"
---
# <a name="installing-a-service-on-a-host-computer"></a>在主機電腦上安裝服務

下列程式碼範例顯示在主機電腦上安裝啟用目錄的服務的基本步驟。 它會執行下列作業：

1.  呼叫 [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) 函式，在本機電腦上 (SCM) 開啟服務控制管理員的控制碼。
2.  呼叫 [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) 函式，以便在 SCM 資料庫中安裝服務。 此呼叫會指定服務的登入帳戶和密碼，以及服務的可執行檔和服務的其他相關資訊。 如果指定的登入帳戶無效， **CreateService** 就會失敗。 但是， **CreateService** 不會檢查密碼的有效性。 此外，它也不會驗證帳戶是否在本機電腦上具有「以服務方式登入」許可權。 如需詳細資訊，請參閱 [主機電腦上的授與以服務方式登入許可權](granting-logon-as-service-right-on-the-host-computer.md)。
3.  呼叫服務的 **ScpCreate** 副程式，在目錄中建立服務連接點物件 (SCP) ，以發佈此服務實例的位置。 如需詳細資訊，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。 此常式也會將服務的系結資訊儲存在 SCP 中、在 SCP 上設定 ACE，讓服務可以在執行時間存取它、在本機登錄中快取 SCP 的辨別名稱，並傳回新 SCP 的分辨名稱。
4.  呼叫服務的 **SpnCompose** 副程式，以使用服務的類別字串和 SCP 的分辨名稱來撰寫服務主體名稱 (SPN) 。 如需詳細資訊，請參閱 [使用 SCP 撰寫服務的 spn](composing-the-spns-for-a-service-with-an-scp.md)。 SPN 可唯一識別此服務的實例。
5.  呼叫服務的 **SpnRegister** 副程式，以在與服務的登入帳戶相關聯的帳戶物件上註冊 SPN。 如需詳細資訊，請參閱 [註冊服務的 spn](registering-the-spns-for-a-service.md)。 註冊 SPN 可讓用戶端應用程式驗證服務。

無論登入帳戶是本機或網域使用者帳戶或 LocalSystem 帳戶，這個程式碼範例都能正常運作。 如果是網域使用者帳戶， *szServiceAccountSAM* 參數會包含帳戶的網域使用者名稱，而 *szServiceAccountDN* 參數則會包含目錄中使用者帳戶物件的分辨名稱。 ****\\**** 如果是 LocalSystem 帳戶， *szServiceAccountSAM* 和 *szPassword* 是 **Null**，而 *szServiceAccountSN* 是目錄中本機電腦帳戶物件的分辨名稱。 如果 *szServiceAccountSAM* 指定本機使用者帳戶 (名稱格式為 "。 \\*UserName*") ，程式碼範例會略過 SPN 註冊，因為本機使用者帳戶不支援相互驗證。

請注意，預設的安全性設定只允許網域系統管理員執行此程式碼。

此外，請注意，此程式碼範例（如所撰寫）必須在要安裝服務的電腦上執行。 因此，它通常位於服務安裝程式碼（如果有的話）中的個別安裝可執行檔，可延伸架構、延伸 UI 或設定群組原則。 這些作業會安裝整個樹系的服務元件，而此程式碼會在單一電腦上安裝服務。


```C++
void InstallServiceOnLocalComputer(
            LPTSTR szServiceAccountDN,  // Distinguished name of logon account.
            LPTSTR szServiceAccountSAM, // SAM name of logon account.
            LPTSTR szPassword)          // Password of logon account.
{
SC_HANDLE   schService = NULL;
SC_HANDLE   schSCManager = NULL;
TCHAR szPath[512];
LPTSTR lpFilePart;
TCHAR szDNofSCP[MAX_PATH];
TCHAR szServiceClass[]=TEXT("ADSockAuth");
 
DWORD dwStatus;
TCHAR **pspn=NULL;
ULONG ulSpn=1;
 
// Get the full path of the service's executable.
// The code example assumes that the executable is in the current directory.
dwStatus = GetFullPathName(TEXT("service.exe"), 512, szPath, &lpFilePart);
if (dwStatus == 0) {
    _tprintf(TEXT("Unable to install %s - %s\n"), 
            TEXT(SZSERVICEDISPLAYNAME), GetLastErrorText(szErr, 256));
    return;
}
_tprintf(TEXT("path of service.exe: %s\n"), szPath);
 
// Open the Service Control Manager on the local computer.
schSCManager = OpenSCManager(
                NULL,                   // Computer (NULL == local)
                NULL,                   // Database (NULL == default)
                SC_MANAGER_ALL_ACCESS   // Access required
                );
if (! schSCManager) {
    _tprintf(TEXT("OpenSCManager failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
        
// Install the service in the SCM database.
schService = CreateService(
            schSCManager,               // SCManager database
            TEXT(SZSERVICENAME),        // Name of service
            TEXT(SZSERVICEDISPLAYNAME), // Name to display
            SERVICE_ALL_ACCESS,         // Desired access
            SERVICE_WIN32_OWN_PROCESS,  // Service type
            SERVICE_DEMAND_START,       // Start type
            SERVICE_ERROR_NORMAL,       // Error control type
            szPath,                     // Service binary
            NULL,                       // No load ordering group
            NULL,                       // No tag identifier
            TEXT(SZDEPENDENCIES),       // Dependencies
            szServiceAccountSAM,        // Service account
            szPassword);                // Account password
if (! schService) {
    _tprintf(TEXT("CreateService failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
 
_tprintf(TEXT("%s installed.\n"), TEXT(SZSERVICEDISPLAYNAME) );
 
// Create the service's Service Connection Point (SCP).
dwStatus = ScpCreate(
        2000,                 // Service default port number
        szServiceClass,       // Specifies the service class string
        szServiceAccountSAM,  // SAM name of logon account for ACE
        szDNofSCP             // Buffer returns the DN of the SCP
        );
if (dwStatus != 0) {
    _tprintf(TEXT("ScpCreate failed: %d\n"), dwStatus );
    DeleteService(schService);
    goto cleanup;
}
 
// Compose and register a service principal name for this service.
// This is performed on the install path because this requires elevated
// privileges for updating the directory.
// If a local account of the format ".\user name", skip the SPN.
if ( szServiceAccountSAM[0] == '.' ) 
{
    _tprintf(TEXT("Do not register SPN for a local account.\n"));
    goto cleanup;
}
 
dwStatus = SpnCompose(
        &pspn,            // Receives pointer to the SPN array.
        &ulSpn,           // Receives number of SPNs returned.
        szDNofSCP,        // Input: DN of the SCP.
        szServiceClass);  // Input: the service's class string.
 
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
        szServiceAccountDN,  // Account on which SPNs are registered.
        pspn,                // Array of SPNs to register.
        ulSpn,               // Number of SPNs in array.
        DS_SPN_ADD_SPN_OP);  // Operation code: Add SPNs.
 
if (dwStatus != NO_ERROR) 
{
    _tprintf(TEXT("Failed to compose SPN: Error was %X\n"), 
                  dwStatus);
    DeleteService(schService);
    ScpDelete(szDNofSCP, szServiceClass, szServiceAccountDN);
    goto cleanup;
}
 
cleanup:
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (schService)
    CloseServiceHandle(schService);
DsFreeSpnArray(ulSpn, pspn);
return;
}
```



如需上述程式碼範例的詳細資訊，請參閱 [使用 SCP 撰寫服務的 spn](composing-the-spns-for-a-service-with-an-scp.md) ，以及 [註冊服務的 spn](registering-the-spns-for-a-service.md)。

 

 