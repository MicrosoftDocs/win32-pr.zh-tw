---
title: 變更服務使用者帳戶的密碼
description: 如果是以使用者帳戶（而不是 LocalSystem 帳戶）登入的服務實例，則主機電腦上的服務控制管理員 (SCM) 會儲存帳戶密碼，此密碼會在服務啟動時用來登入服務。
ms.assetid: d9cef772-bd85-4103-901e-3cf786b29163
ms.tgt_platform: multiple
keywords:
- 變更服務的使用者帳戶 AD 的密碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf16b018796979d3710825472a5f9abab72cd24
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462924"
---
# <a name="changing-the-password-on-a-services-user-account"></a><span data-ttu-id="d017a-104">變更服務使用者帳戶的密碼</span><span class="sxs-lookup"><span data-stu-id="d017a-104">Changing the Password on a Service's User Account</span></span>

<span data-ttu-id="d017a-105">如果是以使用者帳戶（而不是 LocalSystem 帳戶）登入的服務實例，則主機電腦上的服務控制管理員 (SCM) 會儲存帳戶密碼，此密碼會在服務啟動時用來登入服務。</span><span class="sxs-lookup"><span data-stu-id="d017a-105">For a service instance that logs on with a user account, rather than the LocalSystem account, the Service Control Manager (SCM) on the host computer stores the account password, which it uses to log on the service when the service starts.</span></span> <span data-ttu-id="d017a-106">如同任何使用者帳戶，您必須定期變更密碼以維護安全性。</span><span class="sxs-lookup"><span data-stu-id="d017a-106">As with any user account, you must change the password periodically to maintain security.</span></span> <span data-ttu-id="d017a-107">當您變更服務帳戶的密碼時，請更新 SCM 所儲存的密碼。</span><span class="sxs-lookup"><span data-stu-id="d017a-107">When you change the password on a service account, update the password stored by the SCM.</span></span> <span data-ttu-id="d017a-108">下列程式碼範例示範如何執行這兩項作業。</span><span class="sxs-lookup"><span data-stu-id="d017a-108">The following code example shows how to do both.</span></span>

<span data-ttu-id="d017a-109">程式碼範例會使用 [**IADsUser SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) 來設定帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="d017a-109">The code examples use [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) to set the account password.</span></span> <span data-ttu-id="d017a-110">這個方法會使用帳戶的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="d017a-110">This method uses the distinguished name of the account.</span></span> <span data-ttu-id="d017a-111">然後，此範例會在指定的主機電腦上開啟已安裝服務的控制碼，並使用 [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) 函式來更新 SCM 所快取的密碼。</span><span class="sxs-lookup"><span data-stu-id="d017a-111">Then the sample opens a handle to the installed service on the specified host computer, and uses the [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) function to update the password cached by the SCM.</span></span> <span data-ttu-id="d017a-112">此函數會使用帳戶的 SAM 名稱 ( " <domain> \\ <username> " ) 。</span><span class="sxs-lookup"><span data-stu-id="d017a-112">This function uses the SAM name ("<domain>\\<username>") of the account.</span></span>

> [!Note]  
> <span data-ttu-id="d017a-113">這段程式碼必須由網域系統管理員執行。</span><span class="sxs-lookup"><span data-stu-id="d017a-113">This code must be executed by a domain administrator.</span></span>

 

<span data-ttu-id="d017a-114">對於每個複本都使用不同登入帳戶的可複製服務，您可以藉由列舉服務實例來更新所有複本的密碼。</span><span class="sxs-lookup"><span data-stu-id="d017a-114">For a replicable service in which each replica uses a different logon account, you could update the passwords for all of the replicas by enumerating the service instances.</span></span> <span data-ttu-id="d017a-115">如需詳細資訊和程式碼範例，請參閱 [列舉服務的複本](enumerating-the-replicas-of-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="d017a-115">For more information and a code example, see [Enumerating the Replicas of a Service](enumerating-the-replicas-of-a-service.md).</span></span>


```C++
DWORD UpdateAccountPassword(
    LPTSTR szServerDNS,   // DNS name of host computer
    LPTSTR szAccountDN,   // Distinguished name of service 
                          // logon account
    LPTSTR szServiceName, // Name of the service
    LPTSTR szOldPassword, // Old password
    LPTSTR szNewPassword  // New password
    )
{
SC_HANDLE schService = NULL;
SC_HANDLE schSCManager = NULL;
 
DWORD dwLen = MAX_PATH;
TCHAR szAccountPath[MAX_PATH];
IADsUser *pUser = NULL;
HRESULT hr;
 
DWORD dwStatus = 0;
SC_LOCK sclLock = NULL; 

if( !szServerDNS || 
    !szAccountDN || 
    !szServiceName || 
    !szOldPassword || 
    !szNewPassword)
{
    _tprintf(TEXT("Invalid parameter"));
    goto cleanup;
}
 
// Set the password on the account.
// Use the distinguished name to bind to the account object.
_tcsncpy_s(szAccountPath, TEXT("LDAP://"), MAX_PATH);
_tcscat_s(szAccountPath, 
    szAccountDN, 
    MAX_PATH - _tcslen(szAccountPath));
hr = ADsGetObject(szAccountPath, IID_IADsUser, (void**)&pUser);
if (FAILED(hr)) 
{
    _tprintf(TEXT("Get IADsUser failed - 0x%x\n"), dwStatus = hr);
       goto cleanup;
}
 
// Set the password on the account. 
hr = pUser->ChangePassword(CComBSTR(szOldPassword), 
    CComBSTR(szNewPassword));
if (FAILED(hr)) 
{
    _tprintf(TEXT("ChangePassword failed - 0x%x\n"), 
             dwStatus = hr);
    goto cleanup;
}
 
// Update the account and password in the SCM database.
// Open the Service Control Manager on the specified computer.
schSCManager = OpenSCManager(
                szServerDNS,          // DNS name of host computer
                NULL,                 // database (NULL == default)
                SC_MANAGER_ALL_ACCESS // access required
                        );
if (! schSCManager) 
{
    _tprintf(TEXT("OpenSCManager failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Open a handle to the service instance.
schService = OpenService(schSCManager, 
    szServiceName, 
    SERVICE_ALL_ACCESS);
if (! schService) 
{
    _tprintf(TEXT("OpenService failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Get the SCM database lock before changing the password. 
sclLock = LockServiceDatabase(schSCManager); 
if (sclLock == NULL) {
    _tprintf(TEXT("LockServiceDatabase failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Set the account and password that the service uses at startup.
if (! ChangeServiceConfig( 
        schService,        // Handle of service 
        SERVICE_NO_CHANGE, // Service type: no change 
        SERVICE_NO_CHANGE, // Change service start type 
        SERVICE_NO_CHANGE, // Error control: no change 
        NULL,              // Binary path: no change 
        NULL,              // Load order group: no change 
        NULL,              // Tag ID: no change 
        NULL,              // Dependencies: no change 
        NULL,              // Account name: no change 
        szNewPassword,     // New password 
        NULL) )            // Display name: no change
{
    _tprintf(TEXT("ChangeServiceConfig failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
_tprintf(TEXT("Password changed for service instance on: %s\n"), 
    szServerDNS);

cleanup:
 
if (sclLock)
    UnlockServiceDatabase(sclLock); 
if (schService)
    CloseServiceHandle(schService);
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (pUser)
    pUser->Release();
 
return dwStatus;
}
```



 

 