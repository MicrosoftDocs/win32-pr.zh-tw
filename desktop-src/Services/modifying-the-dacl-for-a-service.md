---
description: 服務控制程式可以建立或修改與服務相關聯的 DACL 以控制存取。
ms.assetid: 24bfb2b5-34be-4d38-a690-90d29f5d4f9c
title: 修改服務的 DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d814f6bc81b6d6a207bebf0e9b88c0bb672cdfbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851492"
---
# <a name="modifying-the-dacl-for-a-service"></a><span data-ttu-id="8c7d7-103">修改服務的 DACL</span><span class="sxs-lookup"><span data-stu-id="8c7d7-103">Modifying the DACL for a Service</span></span>

<span data-ttu-id="8c7d7-104">[服務控制程式](service-control-programs.md)可以建立或修改與服務相關聯的 DACL 以控制存取。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-104">A [service control program](service-control-programs.md) can create or modify the DACL associated with a service to control access.</span></span> <span data-ttu-id="8c7d7-105">若要取得與服務物件相關聯的 DACL，請使用 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 函數。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-105">To retrieve the DACL associated with a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span> <span data-ttu-id="8c7d7-106">若要設定 DACL，請使用 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函數。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-106">To set the DACL, use the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="8c7d7-107">對服務物件相關聯之 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 所做的任何變更都是持續性，直到從系統移除服務為止。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-107">Any changes made to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with the service object are persistent until the service is removed from the system.</span></span>

<span data-ttu-id="8c7d7-108">下列範例會為服務建立及設定新的 DACL。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-108">The following example creates and sets a new DACL for the service.</span></span> <span data-ttu-id="8c7d7-109">程式碼會將一個存取控制專案 (ACE) 合併到服務的現有 DACL。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-109">The code merges one access control entry (ACE) to the existing DACL for the service.</span></span> <span data-ttu-id="8c7d7-110">新的 ACE 會授與來賓帳戶對指定服務的啟動、停止、刪除和讀取 \_ 控制存取權。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-110">The new ACE grants the Guest account start, stop, delete, and READ\_CONTROL access to the specified service.</span></span> <span data-ttu-id="8c7d7-111">傳遞給 [**BuildExplicitAccessWithName**](/windows/desktop/api/aclapi/nf-aclapi-buildexplicitaccesswithnamea)函數的 *accesspermissions.list* 參數可以修改服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-111">Access to the service can be modified by the *AccessPermissions* parameter passed to the [**BuildExplicitAccessWithName**](/windows/desktop/api/aclapi/nf-aclapi-buildexplicitaccesswithnamea) function.</span></span>

<span data-ttu-id="8c7d7-112">SzSvcName 變數是包含服務名稱的全域變數。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-112">The szSvcName variable is a global variable that contains the name of the service.</span></span> <span data-ttu-id="8c7d7-113">如需設定此變數的完整範例，請參閱 [SvcControl .cpp](svccontrol-cpp.md)。</span><span class="sxs-lookup"><span data-stu-id="8c7d7-113">For the complete example that sets this variable, see [SvcControl.cpp](svccontrol-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Updates the service DACL to grant start, stop, delete, and read
//   control access to the Guest account.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoUpdateSvcDacl()
{
    EXPLICIT_ACCESS      ea;
    SECURITY_DESCRIPTOR  sd;
    PSECURITY_DESCRIPTOR psd            = NULL;
    PACL                 pacl           = NULL;
    PACL                 pNewAcl        = NULL;
    BOOL                 bDaclPresent   = FALSE;
    BOOL                 bDaclDefaulted = FALSE;
    DWORD                dwError        = 0;
    DWORD                dwSize         = 0;
    DWORD                dwBytesNeeded  = 0;

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

    // Get a handle to the service

    schService = OpenService( 
        schSCManager,              // SCManager database 
        szSvcName,                 // name of service 
        READ_CONTROL | WRITE_DAC); // access
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Get the current security descriptor.

    if (!QueryServiceObjectSecurity(schService,
        DACL_SECURITY_INFORMATION, 
        &psd,           // using NULL does not work on all versions
        0, 
        &dwBytesNeeded))
    {
        if (GetLastError() == ERROR_INSUFFICIENT_BUFFER)
        {
            dwSize = dwBytesNeeded;
            psd = (PSECURITY_DESCRIPTOR)HeapAlloc(GetProcessHeap(),
                    HEAP_ZERO_MEMORY, dwSize);
            if (psd == NULL)
            {
                // Note: HeapAlloc does not support GetLastError.
                printf("HeapAlloc failed\n");
                goto dacl_cleanup;
            }
  
            if (!QueryServiceObjectSecurity(schService,
                DACL_SECURITY_INFORMATION, psd, dwSize, &dwBytesNeeded))
            {
                printf("QueryServiceObjectSecurity failed (%d)\n", GetLastError());
                goto dacl_cleanup;
            }
        }
        else 
        {
            printf("QueryServiceObjectSecurity failed (%d)\n", GetLastError());
            goto dacl_cleanup;
        }
    }

    // Get the DACL.

    if (!GetSecurityDescriptorDacl(psd, &bDaclPresent, &pacl,
                                   &bDaclDefaulted))
    {
        printf("GetSecurityDescriptorDacl failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Build the ACE.

    BuildExplicitAccessWithName(&ea, TEXT("GUEST"),
        SERVICE_START | SERVICE_STOP | READ_CONTROL | DELETE,
        SET_ACCESS, NO_INHERITANCE);

    dwError = SetEntriesInAcl(1, &ea, pacl, &pNewAcl);
    if (dwError != ERROR_SUCCESS)
    {
        printf("SetEntriesInAcl failed(%d)\n", dwError);
        goto dacl_cleanup;
    }

    // Initialize a new security descriptor.

    if (!InitializeSecurityDescriptor(&sd, 
        SECURITY_DESCRIPTOR_REVISION))
    {
        printf("InitializeSecurityDescriptor failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Set the new DACL in the security descriptor.

    if (!SetSecurityDescriptorDacl(&sd, TRUE, pNewAcl, FALSE))
    {
        printf("SetSecurityDescriptorDacl failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Set the new DACL for the service object.

    if (!SetServiceObjectSecurity(schService, 
        DACL_SECURITY_INFORMATION, &sd))
    {
        printf("SetServiceObjectSecurity failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }
    else printf("Service DACL updated successfully\n");

dacl_cleanup:
    CloseServiceHandle(schSCManager);
    CloseServiceHandle(schService);

    if(NULL != pNewAcl)
        LocalFree((HLOCAL)pNewAcl);
    if(NULL != psd)
        HeapFree(GetProcessHeap(), 0, (LPVOID)psd);
}
```



## <a name="related-topics"></a><span data-ttu-id="8c7d7-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c7d7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c7d7-115">完整的服務範例</span><span class="sxs-lookup"><span data-stu-id="8c7d7-115">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
