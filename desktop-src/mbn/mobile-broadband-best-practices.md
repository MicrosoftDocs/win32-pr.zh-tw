---
description: 使用行動寬頻 API 時，您應該使用下列最佳作法集合，以達到最佳的可能效能。
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: 行動寬頻 API 最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399c2ebc40a357eac9686bc3c2c9f471e3b853f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191445"
---
# <a name="mobile-broadband-api-best-practices"></a><span data-ttu-id="247b8-103">行動寬頻 API 最佳作法</span><span class="sxs-lookup"><span data-stu-id="247b8-103">Mobile Broadband API Best Practices</span></span>

<span data-ttu-id="247b8-104">使用行動寬頻 API 時，您應該使用下列最佳作法集合，以達到最佳的可能效能。</span><span class="sxs-lookup"><span data-stu-id="247b8-104">When working with the Mobile Broadband API the following set of best practices should be used in order to achieve the best possible performance.</span></span>

## <a name="do-not-cache-functional-objects"></a><span data-ttu-id="247b8-105">不要快取功能物件</span><span class="sxs-lookup"><span data-stu-id="247b8-105">Do Not Cache Functional Objects</span></span>

<span data-ttu-id="247b8-106">函數物件（例如 [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface)和其他專案）是使用對應的管理員物件上的列舉方法，從 IMbnInterfaceManager 的管理員物件（例如 [](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager)）取得。</span><span class="sxs-lookup"><span data-stu-id="247b8-106">Functional objects, such as [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) and others, are obtained from manager objects, like [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), using the enumeration method on the corresponding manager object.</span></span> <span data-ttu-id="247b8-107">請勿快取這些功能物件，因為快取的功能物件包含過時的資料。</span><span class="sxs-lookup"><span data-stu-id="247b8-107">Do not cache these functional objects, since cached functional objects contain stale data.</span></span> <span data-ttu-id="247b8-108">在這些功能物件上執行的同步作業會傳回相同的資料，直到再次取得功能物件為止。</span><span class="sxs-lookup"><span data-stu-id="247b8-108">The synchronous operations performed on these functional objects will return the same data until the functional objects are obtained again.</span></span>

<span data-ttu-id="247b8-109">請改為使用對應的管理員物件上的列舉方法，快取管理員物件並從管理員物件取得功能物件，以取得最新的資料。</span><span class="sxs-lookup"><span data-stu-id="247b8-109">Instead, cache the manager objects and obtain the functional objects from manager object using the enumeration method on the corresponding manager object again to get the latest data.</span></span>

<span data-ttu-id="247b8-110">下列程式碼範例示範快取管理員物件的正確方式。</span><span class="sxs-lookup"><span data-stu-id="247b8-110">The following code example demonstrates the proper way to cache manager objects.</span></span>


```C++
#include <atlbase.h>
#include "mbnapi.h"
#include <tchar.h>

int main()
{
    HRESULT hr = E_FAIL;
    int returnVal = 0;

    do
    {
        hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);    
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;

        //Do the below once(cache the manager objects)
        hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        SAFEARRAY *psa = NULL;

        //Do the below each time(do not cache functional objects)
        hr = g_InterfaceMgr->GetInterfaces(&psa);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        LONG lLower;
        LONG lUpper;

        hr = SafeArrayGetLBound(psa, 1, &lLower);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        hr = SafeArrayGetUBound(psa, 1, &lUpper);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterface>  pInf = NULL;
        MBN_READY_STATE readyState;

        for (LONG l = lLower; l <= lUpper; l++)
        {
            hr = SafeArrayGetElement(psa, &l, (void*)(&pInf));
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            hr = pInf->GetReadyState(&readyState);
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            _tprintf(_T("Ready State = %d"), readyState); 
        }

        if (FAILED(hr))
        {
            break;
        }
    } while (FALSE);


    CoUninitialize();
    return returnVal;
}
```



## <a name="handle-all-notifications"></a><span data-ttu-id="247b8-111">處理所有通知</span><span class="sxs-lookup"><span data-stu-id="247b8-111">Handle All Notifications</span></span>

<span data-ttu-id="247b8-112">遵循並處理所有通知，即使您的應用程式不會觸發它們也是一樣。</span><span class="sxs-lookup"><span data-stu-id="247b8-112">Follow and handle all notifications, even if they are not triggered by your application.</span></span> <span data-ttu-id="247b8-113">這是讓 UI 與裝置的實際狀態保持同步的必要項。</span><span class="sxs-lookup"><span data-stu-id="247b8-113">This is required to keep the UI in sync with the actual state of the device.</span></span>

<span data-ttu-id="247b8-114">電腦上可以有一個以上的連線管理員正在執行。</span><span class="sxs-lookup"><span data-stu-id="247b8-114">There can be more than one connection manager running on a computer.</span></span> <span data-ttu-id="247b8-115">Windows 7 提供的原生視圖可用網路介面 UI 是連線管理員。</span><span class="sxs-lookup"><span data-stu-id="247b8-115">The native View Available Network Interface UI provided by Windows 7 is a connection manager.</span></span> <span data-ttu-id="247b8-116">任何其他連接管理員都必須回應所有通知，以保持同步 Windows 原生 UI。</span><span class="sxs-lookup"><span data-stu-id="247b8-116">Any other connection managers need to respond to all notifications to remain in sync the Windows native UI.</span></span> <span data-ttu-id="247b8-117">使用者可以選擇在其中一個連線管理員上執行某些作業，這可能會導致行動寬頻裝置的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="247b8-117">A user may opt to perform some operation on one of the connection managers which may result in a state change of the Mobile Broadband device.</span></span> <span data-ttu-id="247b8-118">不過，其他連接管理員必須保持更新狀態，才能正確地指出裝置的修改狀態。</span><span class="sxs-lookup"><span data-stu-id="247b8-118">However, other connection managers need to remain updated in order to properly indicate the modified state of the device.</span></span>

<span data-ttu-id="247b8-119">例如，使用其中一個連線管理員執行連接，會將裝置的狀態從 [可用] 變更為 [已連線]。</span><span class="sxs-lookup"><span data-stu-id="247b8-119">For example, performing a connect using one of the connection managers will change the state of the device from available to connected.</span></span> <span data-ttu-id="247b8-120">未起始此動作的連接管理員應該會看到這種變更。</span><span class="sxs-lookup"><span data-stu-id="247b8-120">This change should be visible to the connection managers that didn’t initiate this action.</span></span> <span data-ttu-id="247b8-121">所有具有指出裝置線上狀態之 UI 的連線管理員，都必須接聽並處理連接狀態通知，才能正確地更新其使用者介面。</span><span class="sxs-lookup"><span data-stu-id="247b8-121">All connection managers that have UI that indicates the connection state of the device, need to listen to and handle the connection state notifications in order to properly update their user interface.</span></span>

## <a name="sending-and-receiving-bytes"></a><span data-ttu-id="247b8-122">傳送和接收位元組</span><span class="sxs-lookup"><span data-stu-id="247b8-122">Sending And Receiving Bytes</span></span>

<span data-ttu-id="247b8-123">使用 IP Helper 函式 [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) 和 [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) 來傳送和接收位元組。</span><span class="sxs-lookup"><span data-stu-id="247b8-123">Use the IP Helper functions [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) and [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) to send and receive bytes.</span></span>

## <a name="using-the-pin-unblock-api"></a><span data-ttu-id="247b8-124">使用 Pin 解鎖 API</span><span class="sxs-lookup"><span data-stu-id="247b8-124">Using The Pin Unblock API</span></span>

<span data-ttu-id="247b8-125">呼叫用戶端應用程式必須提高許可權，才能成功叫用 [**IMbnPin：：解除封鎖**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock)。</span><span class="sxs-lookup"><span data-stu-id="247b8-125">A calling client application must be elevated in order to successfully to invoke [**IMbnPin::Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span></span> <span data-ttu-id="247b8-126">此方法是行動寬頻 API 中唯一需要系統管理員或 NCO 許可權的部分。</span><span class="sxs-lookup"><span data-stu-id="247b8-126">This method is the only portion of the Mobile Broadband API that requires administrator or NCO privileges.</span></span> <span data-ttu-id="247b8-127">如需詳細資訊，請參閱 [Network Configuration Operators 群組的描述]( https://support.microsoft.com/kb/297938/en-us) 。</span><span class="sxs-lookup"><span data-stu-id="247b8-127">See [A Description of the Network Configuration Operators Group]( https://support.microsoft.com/kb/297938/en-us) for more information.</span></span>

## <a name="working-with-safearrays"></a><span data-ttu-id="247b8-128">使用 Safearray</span><span class="sxs-lookup"><span data-stu-id="247b8-128">Working With SafeArrays</span></span>

-   <span data-ttu-id="247b8-129">請先使用 ZeroMemory () ，然後再存取 SafeArray 中的任何元素。</span><span class="sxs-lookup"><span data-stu-id="247b8-129">Use ZeroMemory() before accessing any elements in a SafeArray.</span></span>

-   <span data-ttu-id="247b8-130">請勿檢查 SafeArray 的索引。</span><span class="sxs-lookup"><span data-stu-id="247b8-130">Don’t check on the indexes of a SafeArray.</span></span> <span data-ttu-id="247b8-131">它們可能是負數。</span><span class="sxs-lookup"><span data-stu-id="247b8-131">They may be negative.</span></span>

<span data-ttu-id="247b8-132">下列程式碼範例示範如何適當地處理 SafeArray。</span><span class="sxs-lookup"><span data-stu-id="247b8-132">The following code example shows how to properly handle a SafeArray.</span></span>


```C++
#include <atlbase.h>
#include "mbnapi.h"

void CreateVisibleProviderList(LPCWSTR interfaceID)
{
    CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;
    SAFEARRAY *visibleProviders = NULL;
    long visibleLower = 0;
    long visibleUpper = 0;
    MBN_PROVIDER *pProvider = NULL;
    CComPtr<IMbnInterface> pInterface = NULL;

    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
    
    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = g_InterfaceMgr->GetInterface(interfaceID, & pInterface);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    ULONG age;

    hr = pInterface->GetVisibleProviders(&age, &visibleProviders);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetLBound(visibleProviders, 1, &visibleLower);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetUBound(visibleProviders, 1, &visibleUpper);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    //don't check on the indexes of safearray to be positive
    if (visibleLower > visibleUpper) 
    {
        // There are no visible providers in this case.
        hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
        goto ERROR_0;
    }

    DWORD size = (visibleUpper - visibleLower + 1) * sizeof(BOOL);
    DBG_UNREFERENCED_LOCAL_VARIABLE(size); 
    
    pProvider = (MBN_PROVIDER *)CoTaskMemAlloc(sizeof(MBN_PROVIDER));
    if (!pProvider) 
    {
        hr = E_OUTOFMEMORY;
        goto ERROR_0;
    }

    for (LONG vIndex = visibleLower; vIndex <= visibleUpper; vIndex++) 
    {
        //use zeromemory before accessing any elements in a safearray
        ZeroMemory(pProvider, sizeof(MBN_PROVIDER));
        hr = SafeArrayGetElement(visibleProviders, &vIndex, (void *)pProvider);
        if (FAILED(hr)) 
        {
            continue;
        }
    }

ERROR_0:
    if (visibleProviders) 
    {
        SafeArrayDestroy(visibleProviders);
        visibleProviders = NULL;
    }

    CoUninitialize();
}
```



 

 
