---
description: 服務設定程式會使用 CreateService 函式，在 SCM 資料庫中安裝服務。
ms.assetid: b94bf94e-1b07-4686-be5c-306e7cf13f39
title: 安裝服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e72953b2d3fc3ce549f614a035c9614c4d895a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972614"
---
# <a name="installing-a-service"></a>安裝服務

[服務設定程式](service-configuration-programs.md)會使用 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)函式，在 SCM 資料庫中安裝服務。

下列範例中的 SvcInstall 函數示範如何從服務程式本身安裝服務。 如需完整範例，請參閱 [.svc .cpp](svc-cpp.md)。


```C++
//
// Purpose: 
//   Installs a service in the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID SvcInstall()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    TCHAR szPath[MAX_PATH];

    if( !GetModuleFileName( "", szPath, MAX_PATH ) )
    {
        printf("Cannot install service (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Create the service

    schService = CreateService( 
        schSCManager,              // SCM database 
        SVCNAME,                   // name of service 
        SVCNAME,                   // service name to display 
        SERVICE_ALL_ACCESS,        // desired access 
        SERVICE_WIN32_OWN_PROCESS, // service type 
        SERVICE_DEMAND_START,      // start type 
        SERVICE_ERROR_NORMAL,      // error control type 
        szPath,                    // path to service's binary 
        NULL,                      // no load ordering group 
        NULL,                      // no tag identifier 
        NULL,                      // no dependencies 
        NULL,                      // LocalSystem account 
        NULL);                     // no password 
 
    if (schService == NULL) 
    {
        printf("CreateService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }
    else printf("Service installed successfully\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[服務安裝、移除和列舉](service-installation-removal-and-enumeration.md)
</dt> <dt>

[完整的服務範例](the-complete-service-sample.md)
</dt> </dl>

 

 



