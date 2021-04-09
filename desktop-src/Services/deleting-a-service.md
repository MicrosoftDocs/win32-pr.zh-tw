---
description: 服務設定程式會使用 OpenService 函數來取得已安裝之服務物件的控制碼。 然後，程式可以使用 DeleteService 函式中的服務物件控制碼，從 SCM 資料庫中刪除該服務。
ms.assetid: 3bfe4d42-a8a0-4613-9b0f-a80eef54b622
title: 刪除服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b1e0e95e0ea943487a0d3fa513afa2c0563d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944938"
---
# <a name="deleting-a-service"></a><span data-ttu-id="1fff2-104">刪除服務</span><span class="sxs-lookup"><span data-stu-id="1fff2-104">Deleting a Service</span></span>

<span data-ttu-id="1fff2-105">[服務設定程式](service-configuration-programs.md)會使用 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)函數來取得已安裝之服務物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1fff2-105">A [service configuration program](service-configuration-programs.md) uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function to get a handle to an installed service object.</span></span> <span data-ttu-id="1fff2-106">然後，程式可以使用 [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) 函式中的服務物件控制碼，從 SCM 資料庫中刪除該服務。</span><span class="sxs-lookup"><span data-stu-id="1fff2-106">The program can then use the service object handle in the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service from the SCM database.</span></span>

<span data-ttu-id="1fff2-107">下列範例中的 DoDeleteSvc 函式會示範如何從 SCM 資料庫刪除服務。</span><span class="sxs-lookup"><span data-stu-id="1fff2-107">The DoDeleteSvc function in the following example shows how to delete a service from the SCM database.</span></span> <span data-ttu-id="1fff2-108">SzSvcName 變數是全域變數，其中包含要刪除之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fff2-108">The szSvcName variable is a global variable that contains the name of the service to be deleted.</span></span> <span data-ttu-id="1fff2-109">如需設定此變數的完整範例，請參閱 [SvcConfig .cpp](svcconfig-cpp.md)。</span><span class="sxs-lookup"><span data-stu-id="1fff2-109">For the complete example that sets this variable, see [SvcConfig.cpp](svcconfig-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Deletes a service from the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoDeleteSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    SERVICE_STATUS ssStatus; 

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

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,       // SCM database 
        szSvcName,          // name of service 
        DELETE);            // need delete access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }

    // Delete the service.
 
    if (! DeleteService(schService) ) 
    {
        printf("DeleteService failed (%d)\n", GetLastError()); 
    }
    else printf("Service deleted successfully\n"); 
 
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="1fff2-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="1fff2-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fff2-111">服務安裝、移除和列舉</span><span class="sxs-lookup"><span data-stu-id="1fff2-111">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> <dt>

[<span data-ttu-id="1fff2-112">完整的服務範例</span><span class="sxs-lookup"><span data-stu-id="1fff2-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



