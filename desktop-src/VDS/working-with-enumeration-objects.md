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
# <a name="working-with-enumeration-objects"></a>使用列舉物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

接下來的程式碼範例會示範呼叫端如何使用 [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) 介面來處理列舉物件。 請注意，列舉物件所傳回的資訊是靜態的。 您必須重新查詢物件，才能看到新的設定變更。

**GetControllerById** 函式會採用 [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)介面（由 *pSubsystem* 參數指定），並查詢子系統中的控制器，然後逐一查看傳回的列舉，以使用符合 *PCONTROLLERID* 參數所指定之 guid 的 guid 來搜尋控制器。 如果找到相符的控制器， *ppController* 參數會傳回該控制器以及 S \_ OK **HRESULT**。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VDS](using-vds.md)
</dt> <dt>

[Helper 物件](helper-objects.md)
</dt> <dt>

[**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject)
</dt> <dt>

[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)
</dt> </dl>

 

 
