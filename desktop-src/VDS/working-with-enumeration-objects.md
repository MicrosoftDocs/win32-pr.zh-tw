---
description: 使用列舉物件
ms.assetid: cb99e9fd-613c-4e38-9e0f-e1a23b72aa07
title: 使用列舉物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df90548ef060d537faff206e45e0cf74630cdfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979194"
---
# <a name="working-with-enumeration-objects"></a><span data-ttu-id="7ecee-103">使用列舉物件</span><span class="sxs-lookup"><span data-stu-id="7ecee-103">Working with Enumeration Objects</span></span>

<span data-ttu-id="7ecee-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="7ecee-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="7ecee-105">接下來的程式碼範例會示範呼叫端如何使用 [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) 介面來處理列舉物件。</span><span class="sxs-lookup"><span data-stu-id="7ecee-105">The code example that follows demonstrates how a caller works with enumeration objects using the [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) interface.</span></span> <span data-ttu-id="7ecee-106">請注意，列舉物件所傳回的資訊是靜態的。</span><span class="sxs-lookup"><span data-stu-id="7ecee-106">Note that the information that is returned by a enumeration object is static.</span></span> <span data-ttu-id="7ecee-107">您必須重新查詢物件，才能看到新的設定變更。</span><span class="sxs-lookup"><span data-stu-id="7ecee-107">You must query the object again to see new configuration changes.</span></span>

<span data-ttu-id="7ecee-108">**GetControllerById** 函式會採用 [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)介面（由 *pSubsystem* 參數指定），並查詢子系統中的控制器，然後逐一查看傳回的列舉，以使用符合 *PCONTROLLERID* 參數所指定之 guid 的 guid 來搜尋控制器。</span><span class="sxs-lookup"><span data-stu-id="7ecee-108">The **GetControllerById** function takes an [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) interface, specified by the *pSubsystem* parameter, and queries for the controllers in the subsystem, then iterates through the returned enumeration searching for a controller with a GUID that matches the GUID that is specified by the *pControllerId* parameter.</span></span> <span data-ttu-id="7ecee-109">如果找到相符的控制器， *ppController* 參數會傳回該控制器以及 S \_ OK **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="7ecee-109">If a matching controller is found, it is returned by the *ppController* parameter along with an S\_OK **HRESULT**.</span></span>


```C++
//
// Simple macro to release non-null interfaces.
//
#include <windows.h>
#include "vds.h"
#include <stdio.h>

#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

HRESULT GetControllerById(
         IN IVdsSubSystem       *pSubsystem,
         IN CONST VDS_OBJECT_ID *pControllerId,
         OUT IVdsController     **ppController)
{
    VDS_CONTROLLER_PROP vdsControllerProperties;
    IEnumVdsObject      *pEnumController = NULL;
    IVdsController      *pController     = NULL;
    IUnknown            *pUnknown        = NULL;
    HRESULT             hResult          = S_OK;
    ULONG               ulFetched        = 0;
    BOOL                bDone            = FALSE;

    ZeroMemory(&vdsControllerProperties, sizeof(VDS_CONTROLLER_PROP));

    // Query for the enumeration of controllers belonging
    // to the given subsystem.
    hResult = pSubsystem->QueryControllers(&pEnumController);

    if (SUCCEEDED(hResult) && (!pEnumController)) 
    {
        hResult = E_UNEXPECTED; // Errant provider, 
        // returned S_OK 
        // with a NULL pointer.
    }

    if (SUCCEEDED(hResult)) 
    {
        // Enumerate through all the controllers this subsystem 
        // contains to find the controller of interest.
        while (!bDone) 
        {
            ulFetched = 0;
            hResult = pEnumController->Next(1, &pUnknown, &ulFetched);

            if (hResult == S_FALSE) 
            {
                hResult = E_INVALIDARG;
                break;
            }

            if (SUCCEEDED(hResult) && (!pUnknown)) 
            {
                hResult = E_UNEXPECTED; // Errant provider, 
                // returned S_OK with
                // a NULL pointer 
            }

            // Use an IVdsController interface to get the controller 
            // properties and check for the desired GUID.
            if (SUCCEEDED(hResult)) 
            {
                hResult = pUnknown->QueryInterface(IID_IVdsController,  
                    (void **) &pController);
            }

            if (SUCCEEDED(hResult) && (!pController)) 
            {
                hResult = E_UNEXPECTED; // Errant provider, 
                // returned S_OK 
                // with a NULL pointer
            }

            if (SUCCEEDED(hResult)) 
            {
                hResult = pController->  
                GetProperties( &vdsControllerProperties);
            }

            if (SUCCEEDED(hResult) 
                && IsEqualGUID(*pControllerId, vdsControllerProperties.id)) 
            {
                bDone = TRUE;
            } 
            else 
            {
                _SafeRelease(pController);
            }

            _SafeRelease(pUnknown);

            //Free the strings in the properties structure.
            if (NULL != vdsControllerProperties.pwszIdentification) 
            {
                CoTaskMemFree(vdsControllerProperties.pwszIdentification);
            }

            ZeroMemory(&vdsControllerProperties, sizeof(VDS_CONTROLLER_PROP));
        }
    }

    if (SUCCEEDED(hResult)) 
    {
        *ppController = pController;
    }

    _SafeRelease(pEnumController);
    return hResult;
}
```



## <a name="related-topics"></a><span data-ttu-id="7ecee-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="7ecee-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ecee-111">使用 VDS</span><span class="sxs-lookup"><span data-stu-id="7ecee-111">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="7ecee-112">Helper 物件</span><span class="sxs-lookup"><span data-stu-id="7ecee-112">Helper Objects</span></span>](helper-objects.md)
</dt> <dt>

[<span data-ttu-id="7ecee-113">**IEnumVdsObject**</span><span class="sxs-lookup"><span data-stu-id="7ecee-113">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject)
</dt> <dt>

[<span data-ttu-id="7ecee-114">**IVdsSubSystem**</span><span class="sxs-lookup"><span data-stu-id="7ecee-114">**IVdsSubSystem**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)
</dt> </dl>

 

 
