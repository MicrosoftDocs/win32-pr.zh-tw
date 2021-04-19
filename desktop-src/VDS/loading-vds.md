---
description: 正在載入 VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: 正在載入 VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c66685668641f3036739c57bd7353f72052c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999913"
---
# <a name="loading-vds"></a><span data-ttu-id="fccf4-103">正在載入 VDS</span><span class="sxs-lookup"><span data-stu-id="fccf4-103">Loading VDS</span></span>

<span data-ttu-id="fccf4-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="fccf4-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="fccf4-105">**載入和初始化 VDS**</span><span class="sxs-lookup"><span data-stu-id="fccf4-105">**To load and initialize VDS**</span></span>

1.  <span data-ttu-id="fccf4-106">釋放非 null 的介面。</span><span class="sxs-lookup"><span data-stu-id="fccf4-106">Release non-null interfaces.</span></span>
2.  <span data-ttu-id="fccf4-107">呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)、 [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)或 [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) 函數，以取得服務載入器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="fccf4-107">Call the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex), or [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) function to obtain a pointer to the service loader object.</span></span>

    <span data-ttu-id="fccf4-108">**CLSCTX \_無法 \_** 在此呼叫中指定停用 AAA。</span><span class="sxs-lookup"><span data-stu-id="fccf4-108">**CLSCTX\_DISABLE\_AAA** cannot be specified in this call.</span></span> <span data-ttu-id="fccf4-109">如果呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，就不能在 *dwCapabilities* 參數中指定 **EOAC \_ DISABLE \_ AAA** 。</span><span class="sxs-lookup"><span data-stu-id="fccf4-109">If [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is called, **EOAC\_DISABLE\_AAA** cannot be specified in the *dwCapabilities* parameter.</span></span>

3.  <span data-ttu-id="fccf4-110">呼叫 [**IVdsServiceLoader：： LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) 方法以載入 VDS。</span><span class="sxs-lookup"><span data-stu-id="fccf4-110">Call the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method to load VDS.</span></span>

    <span data-ttu-id="fccf4-111">傳遞 **Null** 做為第一個參數，會在本機主機上載入並初始化 VDS。</span><span class="sxs-lookup"><span data-stu-id="fccf4-111">Passing **NULL** as the first parameter loads and initializes VDS on the local host.</span></span>

4.  <span data-ttu-id="fccf4-112">呼叫 [**IVdsService：： WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) 方法以等候 VDS 初始化完成。</span><span class="sxs-lookup"><span data-stu-id="fccf4-112">Call the [**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) method to wait for VDS initialization to complete.</span></span>

<span data-ttu-id="fccf4-113">下列程式碼範例會初始化服務，以傳回服務物件的指標。</span><span class="sxs-lookup"><span data-stu-id="fccf4-113">The following code example initializes the service that returns a pointer to the service object.</span></span>


```C++
#include "initguid.h"
#include "vds.h"
#include <stdio.h>

#pragma comment( lib, "ole32.lib" )

//
// Simple macro to release non-null interfaces.
//
#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

void __cdecl main(void) 
{
    HRESULT hResult;
    IVdsService *pService = NULL;
    IVdsServiceLoader *pLoader = NULL;

    // For this, you first get a pointer to the VDS Loader
    // Launch the VDS service. 
    //

    hResult = CoInitialize(NULL);

    if (SUCCEEDED(hResult)) 
    {
    
        hResult = CoCreateInstance(CLSID_VdsLoader,
            NULL,
            CLSCTX_LOCAL_SERVER,
            IID_IVdsServiceLoader,
            (void **) &pLoader);

        // 
        // And then load VDS on the local computer.
        //
        if (SUCCEEDED(hResult)) 
        {
            hResult = pLoader->LoadService(NULL, &pService);
        }

        //
        // You're done with the Loader interface at this point.
        //
        _SafeRelease(pLoader); 
        
        if (SUCCEEDED(hResult)) 
        {
            hResult = pService->WaitForServiceReady();
            if (SUCCEEDED(hResult)) 
            {
                //
                // You obtained an interface to the service: pService.
                // This interface can now be used to query for providers 
                // and perform other operations. 
                //
                printf("VDS Service Loaded");
            }

        } 
        else 
        {
            printf("VDS Service failed hr=%x\n",hResult);
        }
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="fccf4-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="fccf4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fccf4-115">使用 VDS</span><span class="sxs-lookup"><span data-stu-id="fccf4-115">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="fccf4-116">**IVdsService::WaitForServiceReady**</span><span class="sxs-lookup"><span data-stu-id="fccf4-116">**IVdsService::WaitForServiceReady**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[<span data-ttu-id="fccf4-117">**IVdsServiceLoader::LoadService**</span><span class="sxs-lookup"><span data-stu-id="fccf4-117">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="fccf4-118">安裝程式和服務物件</span><span class="sxs-lookup"><span data-stu-id="fccf4-118">Setup and Service Objects</span></span>](startup-and-service-objects.md)
</dt> </dl>

 

 
