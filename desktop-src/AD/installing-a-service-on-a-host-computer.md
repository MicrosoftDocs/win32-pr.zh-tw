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
# <a name="installing-a-service-on-a-host-computer"></a><span data-ttu-id="8c4df-103">在主機電腦上安裝服務</span><span class="sxs-lookup"><span data-stu-id="8c4df-103">Installing a Service on a Host Computer</span></span>

<span data-ttu-id="8c4df-104">下列程式碼範例顯示在主機電腦上安裝啟用目錄的服務的基本步驟。</span><span class="sxs-lookup"><span data-stu-id="8c4df-104">The following code example shows the basic steps of installing a directory-enabled service on a host computer.</span></span> <span data-ttu-id="8c4df-105">它會執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="8c4df-105">It performs the following operations:</span></span>

1.  <span data-ttu-id="8c4df-106">呼叫 [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) 函式，在本機電腦上 (SCM) 開啟服務控制管理員的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8c4df-106">Calls the [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) function to open a handle to the service control manager (SCM) on the local computer.</span></span>
2.  <span data-ttu-id="8c4df-107">呼叫 [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) 函式，以便在 SCM 資料庫中安裝服務。</span><span class="sxs-lookup"><span data-stu-id="8c4df-107">Calls the [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) function to install the service in the SCM database.</span></span> <span data-ttu-id="8c4df-108">此呼叫會指定服務的登入帳戶和密碼，以及服務的可執行檔和服務的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c4df-108">This call specifies the service's logon account and password, as well as the service's executable and other information about the service.</span></span> <span data-ttu-id="8c4df-109">如果指定的登入帳戶無效， **CreateService** 就會失敗。</span><span class="sxs-lookup"><span data-stu-id="8c4df-109">**CreateService** fails if the specified logon account is invalid.</span></span> <span data-ttu-id="8c4df-110">但是， **CreateService** 不會檢查密碼的有效性。</span><span class="sxs-lookup"><span data-stu-id="8c4df-110">However, **CreateService** does not check the validity of the password.</span></span> <span data-ttu-id="8c4df-111">此外，它也不會驗證帳戶是否在本機電腦上具有「以服務方式登入」許可權。</span><span class="sxs-lookup"><span data-stu-id="8c4df-111">It also does not verify that the account has the logon as a service right on the local computer.</span></span> <span data-ttu-id="8c4df-112">如需詳細資訊，請參閱 [主機電腦上的授與以服務方式登入許可權](granting-logon-as-service-right-on-the-host-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="8c4df-112">For more information, see [Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md).</span></span>
3.  <span data-ttu-id="8c4df-113">呼叫服務的 **ScpCreate** 副程式，在目錄中建立服務連接點物件 (SCP) ，以發佈此服務實例的位置。</span><span class="sxs-lookup"><span data-stu-id="8c4df-113">Calls the service's **ScpCreate** subroutine that creates a service connection point object (SCP) in the directory to publish the location of this instance of the service.</span></span> <span data-ttu-id="8c4df-114">如需詳細資訊，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。</span><span class="sxs-lookup"><span data-stu-id="8c4df-114">For more information, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="8c4df-115">此常式也會將服務的系結資訊儲存在 SCP 中、在 SCP 上設定 ACE，讓服務可以在執行時間存取它、在本機登錄中快取 SCP 的辨別名稱，並傳回新 SCP 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="8c4df-115">This routine also stores the service's binding information in the SCP, sets an ACE on the SCP so the service can access it at run time, caches the distinguished name of the SCP in the local registry, and returns the distinguished name of the new SCP.</span></span>
4.  <span data-ttu-id="8c4df-116">呼叫服務的 **SpnCompose** 副程式，以使用服務的類別字串和 SCP 的分辨名稱來撰寫服務主體名稱 (SPN) 。</span><span class="sxs-lookup"><span data-stu-id="8c4df-116">Calls the service's **SpnCompose** subroutine that uses the service's class string and the distinguished name of the SCP to compose a service principal name (SPN).</span></span> <span data-ttu-id="8c4df-117">如需詳細資訊，請參閱 [使用 SCP 撰寫服務的 spn](composing-the-spns-for-a-service-with-an-scp.md)。</span><span class="sxs-lookup"><span data-stu-id="8c4df-117">For more information, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="8c4df-118">SPN 可唯一識別此服務的實例。</span><span class="sxs-lookup"><span data-stu-id="8c4df-118">The SPN uniquely identifies this instance of the service.</span></span>
5.  <span data-ttu-id="8c4df-119">呼叫服務的 **SpnRegister** 副程式，以在與服務的登入帳戶相關聯的帳戶物件上註冊 SPN。</span><span class="sxs-lookup"><span data-stu-id="8c4df-119">Calls the service's **SpnRegister** subroutine that registers the SPN on the account object associated with service's logon account.</span></span> <span data-ttu-id="8c4df-120">如需詳細資訊，請參閱 [註冊服務的 spn](registering-the-spns-for-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="8c4df-120">For more information, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span> <span data-ttu-id="8c4df-121">註冊 SPN 可讓用戶端應用程式驗證服務。</span><span class="sxs-lookup"><span data-stu-id="8c4df-121">Registration of the SPN enables client applications to authenticate the service.</span></span>

<span data-ttu-id="8c4df-122">無論登入帳戶是本機或網域使用者帳戶或 LocalSystem 帳戶，這個程式碼範例都能正常運作。</span><span class="sxs-lookup"><span data-stu-id="8c4df-122">This code example works correctly regardless of whether the logon account is a local or domain user account or the LocalSystem account.</span></span> <span data-ttu-id="8c4df-123">如果是網域使用者帳戶， *szServiceAccountSAM* 參數會包含帳戶的網域使用者名稱，而 *szServiceAccountDN* 參數則會包含目錄中使用者帳戶物件的分辨名稱。 \*\*\*\*\\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8c4df-123">For a domain user account, the *szServiceAccountSAM* parameter contains the *Domain ***\\*** UserName* name of the account, and the *szServiceAccountDN* parameter contains the distinguished name of the user account object in the directory.</span></span> <span data-ttu-id="8c4df-124">如果是 LocalSystem 帳戶， *szServiceAccountSAM* 和 *szPassword* 是 **Null**，而 *szServiceAccountSN* 是目錄中本機電腦帳戶物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="8c4df-124">For the LocalSystem account, *szServiceAccountSAM* and *szPassword* are **NULL**, and *szServiceAccountSN* is the distinguished name of the local computer's account object in the directory.</span></span> <span data-ttu-id="8c4df-125">如果 *szServiceAccountSAM* 指定本機使用者帳戶 (名稱格式為 "。 \\*UserName*") ，程式碼範例會略過 SPN 註冊，因為本機使用者帳戶不支援相互驗證。</span><span class="sxs-lookup"><span data-stu-id="8c4df-125">If *szServiceAccountSAM* specifies a local user account (name format is ".\\*UserName*"), the code example skips the SPN registration because mutual authentication is not supported for local user accounts.</span></span>

<span data-ttu-id="8c4df-126">請注意，預設的安全性設定只允許網域系統管理員執行此程式碼。</span><span class="sxs-lookup"><span data-stu-id="8c4df-126">Be aware that the default security configuration allows only domain administrators to execute this code.</span></span>

<span data-ttu-id="8c4df-127">此外，請注意，此程式碼範例（如所撰寫）必須在要安裝服務的電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="8c4df-127">Also, be aware that this code example, as written, must be executed on the computer where the service is being installed.</span></span> <span data-ttu-id="8c4df-128">因此，它通常位於服務安裝程式碼（如果有的話）中的個別安裝可執行檔，可延伸架構、延伸 UI 或設定群組原則。</span><span class="sxs-lookup"><span data-stu-id="8c4df-128">Consequently, it is typically in a separate installation executable from your service installation code, if any, that extends the schema, extends the UI, or sets up group policy.</span></span> <span data-ttu-id="8c4df-129">這些作業會安裝整個樹系的服務元件，而此程式碼會在單一電腦上安裝服務。</span><span class="sxs-lookup"><span data-stu-id="8c4df-129">Those operations install service components for an entire a forest, whereas this code installs the service on a single computer.</span></span>


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



<span data-ttu-id="8c4df-130">如需上述程式碼範例的詳細資訊，請參閱 [使用 SCP 撰寫服務的 spn](composing-the-spns-for-a-service-with-an-scp.md) ，以及 [註冊服務的 spn](registering-the-spns-for-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="8c4df-130">For more information about the previous code example, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md) and [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

 

 