---
title: 應用程式基本概念
description: 應用程式基本概念
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows Media Format SDK，DRM 應用程式基本概念
- 數位版權管理 (DRM) ，應用程式基本概念
- DRM (數位版權管理) ，應用程式基本概念
- 數位版權管理 (DRM) ，WMDRMStartup 函式
- DRM (數位版權管理) ，WMDRMStartup 函式
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183056"
---
# <a name="application-basics"></a><span data-ttu-id="ab10a-109">應用程式基本概念</span><span class="sxs-lookup"><span data-stu-id="ab10a-109">Application Basics</span></span>

<span data-ttu-id="ab10a-110">您必須針對使用 Windows Media DRM 用戶端擴充 Api 的任何應用程式執行一些額外的處理。</span><span class="sxs-lookup"><span data-stu-id="ab10a-110">There is some extra processing that you must perform for any application that uses the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="ab10a-111">本主題說明簡單應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="ab10a-111">This topic describes the requirements for a simple application.</span></span>

<span data-ttu-id="ab10a-112">首先，您必須藉由呼叫 [**WMDRMStartup**](wmdrmstartup.md) 函式來初始化 WINDOWS Media DRM 用戶端擴充 api。</span><span class="sxs-lookup"><span data-stu-id="ab10a-112">First, you must initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span> <span data-ttu-id="ab10a-113">SDK 的物件是 COM 物件，但您不需要呼叫 **CoIntialize**，因為 **WMDRMStatup** 函數會為您初始化 com。</span><span class="sxs-lookup"><span data-stu-id="ab10a-113">The objects of the SDK are COM objects, but you do not need to call **CoIntialize**, because the **WMDRMStatup** function initializes COM for you.</span></span>

> [!Note]  
> <span data-ttu-id="ab10a-114">Windows Media 格式 SDK 只會使用 COM 的子集，因此，如果您使用 Windows Media DRM 用戶端擴充 API 中以外的 COM 物件，您仍然必須呼叫 **CoInitialize**。</span><span class="sxs-lookup"><span data-stu-id="ab10a-114">The Windows Media Format SDK uses only a subset of COM, so if you use COM objects other than those in the Windows Media DRM Client Extended API, you must still call **CoInitialize**.</span></span>

 

<span data-ttu-id="ab10a-115">Windows Media DRM 用戶端擴充 Api 的所有物件都是使用 helper 函式和方法建立的。</span><span class="sxs-lookup"><span data-stu-id="ab10a-115">All of the objects of the Windows Media DRM Client Extended APIs are created using helper functions and methods.</span></span> <span data-ttu-id="ab10a-116">您永遠不需要呼叫 **CoCreateInstance** 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="ab10a-116">You never need to call **CoCreateInstance** to create an object.</span></span> <span data-ttu-id="ab10a-117">針對使用 SDK 的任何應用程式，要具現化的第一個介面是 [**IWMDRMProvider**](iwmdrmprovider.md)，您可以用它來具現化所有其他基底介面。</span><span class="sxs-lookup"><span data-stu-id="ab10a-117">The first interface to instantiate for any application that uses the SDK is [**IWMDRMProvider**](iwmdrmprovider.md), which you can use to instantiate all of the other base interfaces.</span></span> <span data-ttu-id="ab10a-118">若要取得 **IWMDRMProvider** 的實例，您必須呼叫 [**WMDRMCreateProvider**](wmdrmcreateprovider.md) 或 [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md)。</span><span class="sxs-lookup"><span data-stu-id="ab10a-118">To get an instance of **IWMDRMProvider**, you must call either [**WMDRMCreateProvider**](wmdrmcreateprovider.md) or [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span></span> <span data-ttu-id="ab10a-119">這些函式之間的差異在於， **WMDRMCreateProvider** 會建立一個物件，而這個物件可以接著只建立不支援需要存根程式庫之方法的物件。</span><span class="sxs-lookup"><span data-stu-id="ab10a-119">The difference between these functions is that **WMDRMCreateProvider** creates an object that can in turn create only objects that do not support methods that require the stub library.</span></span>

<span data-ttu-id="ab10a-120">當您擁有 **IWMDRMProvider** 的實例之後，您可以藉由呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)來建立您所需的其他物件。</span><span class="sxs-lookup"><span data-stu-id="ab10a-120">After you have an instance of **IWMDRMProvider**, you can create the other objects that you need by calling [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span>

<span data-ttu-id="ab10a-121">當您準備好要結束應用程式時，您必須藉由呼叫 [**WMDRMShutdown**](wmdrmshutdown.md) 函式來釋出 DRM 子系統資源。</span><span class="sxs-lookup"><span data-stu-id="ab10a-121">When you are ready to exit your application, you must release the DRM subsystem resources by calling the [**WMDRMShutdown**](wmdrmshutdown.md) function.</span></span> <span data-ttu-id="ab10a-122">此函數也會為您關閉 COM。</span><span class="sxs-lookup"><span data-stu-id="ab10a-122">This function also shuts down COM for you.</span></span>

<span data-ttu-id="ab10a-123">下列程式碼範例示範如何初始化並結束使用 Windows Media DRM 用戶端擴充 Api 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ab10a-123">The following code example demonstrates how to initialize and conclude an application that uses the Windows Media DRM Client Extended APIs.</span></span>


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a><span data-ttu-id="ab10a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="ab10a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab10a-125">**開始使用**</span><span class="sxs-lookup"><span data-stu-id="ab10a-125">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




