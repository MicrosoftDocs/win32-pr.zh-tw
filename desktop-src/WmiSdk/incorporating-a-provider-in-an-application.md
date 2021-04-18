---
description: 描述如何在應用程式中包含 WMI COM 提供者作為元件，而不是在內部處理 WMI。 所謂的低耦合提供者，這是建議的 WMI COM 提供者類型，可針對 Windows 2000 和更新版本的作業系統建立。
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: 將提供者併入應用程式中
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571141"
---
# <a name="incorporating-a-provider-in-an-application"></a><span data-ttu-id="816a0-104">將提供者併入應用程式中</span><span class="sxs-lookup"><span data-stu-id="816a0-104">Incorporating a Provider in an Application</span></span>

<span data-ttu-id="816a0-105">在建立要檢測的應用程式時，最佳作法是將提供者納入為應用程式本身內的元件。</span><span class="sxs-lookup"><span data-stu-id="816a0-105">When creating an application that is to be instrumented, the best practice is to include the provider as a component within the application itself.</span></span> <span data-ttu-id="816a0-106">這種作法可讓 Windows Management Instrumentation (WMI) 直接與服務提供者互動，而不是間接透過程式 API 來與服務提供者互動。</span><span class="sxs-lookup"><span data-stu-id="816a0-106">This practice permits Windows Management Instrumentation (WMI) to interact with the service provider directly instead of indirectly through the program API.</span></span> <span data-ttu-id="816a0-107">將提供者與 WMI 分離也會讓應用程式控制提供者存留期，而不是 WMI。</span><span class="sxs-lookup"><span data-stu-id="816a0-107">Decoupling the provider from WMI also puts the application in control of the provider lifespan, instead of WMI.</span></span> <span data-ttu-id="816a0-108">如需撰寫在 WMI 進程中執行的提供者的詳細資訊，請參閱 [撰寫提供者以將資料提供給 wmi](supplying-data-to-wmi-by-writing-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="816a0-108">For more information about writing a provider that runs in the WMI process, see [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).</span></span> <span data-ttu-id="816a0-109">如需有關主控提供者之模型和安全性設定的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="816a0-109">For more information about hosting model and security settings for the provider, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="816a0-110">下圖說明 WMI、低耦合提供者和應用程式之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="816a0-110">The following diagram illustrates the relationship between WMI, a decoupled provider, and an application.</span></span>

![wmi、低耦合提供者和應用程式之間的關聯性](images/decoupledprov.png)

<span data-ttu-id="816a0-112">如需有關低耦合提供者方法的詳細資訊，請參閱 [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) 和 [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider)。</span><span class="sxs-lookup"><span data-stu-id="816a0-112">For more information about decoupled provider methods, see [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) and [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span></span>

> [!Note]  
> <span data-ttu-id="816a0-113">低耦合提供者支援實例、方法、事件提供者和事件取用者。</span><span class="sxs-lookup"><span data-stu-id="816a0-113">The decoupled provider supports instance, method, event providers, and event consumers.</span></span> <span data-ttu-id="816a0-114">它不支援類別和屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="816a0-114">It does not support class and property providers.</span></span> <span data-ttu-id="816a0-115">如需詳細資訊，請參閱 [撰寫類別提供者](writing-a-class-provider.md) 和 [撰寫屬性提供者](writing-a-property-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="816a0-115">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Property Provider](writing-a-property-provider.md).</span></span>

 

<span data-ttu-id="816a0-116">本主題中的程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="816a0-116">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="816a0-117">下列程式會使用 c + + 程式碼範例，說明如何在應用程式中納入低耦合提供者。</span><span class="sxs-lookup"><span data-stu-id="816a0-117">The following procedure uses C++ code examples to describe how to incorporate a decoupled provider in your application.</span></span> <span data-ttu-id="816a0-118">應用程式的初始化方法會執行下列步驟，讓 WMI 僅與已註冊的低耦合提供者互動。</span><span class="sxs-lookup"><span data-stu-id="816a0-118">The initialization method of the application performs the following steps so that WMI only interacts with a registered decoupled provider.</span></span>

<span data-ttu-id="816a0-119">**在 c + + 應用程式中執行低耦合提供者**</span><span class="sxs-lookup"><span data-stu-id="816a0-119">**To implement a decoupled provider in a C++ application**</span></span>

1.  <span data-ttu-id="816a0-120">初始化 COM 程式庫以供呼叫執行緒使用。</span><span class="sxs-lookup"><span data-stu-id="816a0-120">Initialize the COM library for use by the calling thread.</span></span>

    <span data-ttu-id="816a0-121">下列程式碼範例顯示如何初始化 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="816a0-121">The following code example shows how to initialize the COM library.</span></span>

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  <span data-ttu-id="816a0-122">設定預設進程安全性層級。</span><span class="sxs-lookup"><span data-stu-id="816a0-122">Set the default process security level.</span></span>

    <span data-ttu-id="816a0-123">此層級會建立其他程式存取用戶端進程資訊所需的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="816a0-123">This level establishes the security level required of other processes to access the client process' information.</span></span> <span data-ttu-id="816a0-124">驗證層級應為 RPC \_ C \_ 驗證 \_ 層級的 \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="816a0-124">The authentication level should be RPC\_C\_AUTHN\_LEVEL\_DEFAULT.</span></span> <span data-ttu-id="816a0-125">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="816a0-125">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="816a0-126">下列程式碼範例顯示如何設定預設的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="816a0-126">The following code example shows how to set the default security level.</span></span>

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  <span data-ttu-id="816a0-127">註冊低耦合提供者註冊機構。</span><span class="sxs-lookup"><span data-stu-id="816a0-127">Register the decoupled provider registrar.</span></span>

    <span data-ttu-id="816a0-128">下列程式碼範例顯示如何註冊低耦合提供者註冊機構。</span><span class="sxs-lookup"><span data-stu-id="816a0-128">The following code example shows how to register the decoupled provider registrar.</span></span>

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  <span data-ttu-id="816a0-129">註冊分離事件提供者。</span><span class="sxs-lookup"><span data-stu-id="816a0-129">Register the decoupled event provider.</span></span>

    <span data-ttu-id="816a0-130">下列程式碼範例示範如何註冊分離事件提供者。</span><span class="sxs-lookup"><span data-stu-id="816a0-130">The following code example shows how to register the decoupled event provider.</span></span>

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  <span data-ttu-id="816a0-131">對提供者功能所需的 [WMI 進行呼叫](making-calls-to-wmi.md) 。</span><span class="sxs-lookup"><span data-stu-id="816a0-131">Make the [calls to WMI](making-calls-to-wmi.md) required by the provider's functionality.</span></span> <span data-ttu-id="816a0-132">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="816a0-132">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="816a0-133">如需提供者服務腳本或應用程式的資料要求的詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="816a0-133">For more information if the provider services a request for data from a script or application, see [Impersonating a Client](impersonating-a-client.md).</span></span>

<span data-ttu-id="816a0-134">在終止之前，應用程式必須先清除。</span><span class="sxs-lookup"><span data-stu-id="816a0-134">Just prior to terminating, the application must clean up after itself.</span></span> <span data-ttu-id="816a0-135">下列程式說明如何取消註冊低耦合提供者，讓 WMI 不會嘗試查詢資訊。</span><span class="sxs-lookup"><span data-stu-id="816a0-135">The following procedure describes how to unregister the decoupled provider so that WMI does not attempt to query it for information.</span></span>

<span data-ttu-id="816a0-136">下列程式說明如何取消註冊低耦合提供者。</span><span class="sxs-lookup"><span data-stu-id="816a0-136">The following procedure describes how to unregister the decoupled provider.</span></span>

<span data-ttu-id="816a0-137">**取消註冊低耦合提供者**</span><span class="sxs-lookup"><span data-stu-id="816a0-137">**To unregister the decoupled provider**</span></span>

1.  <span data-ttu-id="816a0-138">取消註冊並釋放註冊機構。</span><span class="sxs-lookup"><span data-stu-id="816a0-138">Unregister and release the registrar.</span></span>

    <span data-ttu-id="816a0-139">下列程式碼範例示範如何取消註冊和釋放註冊機構。</span><span class="sxs-lookup"><span data-stu-id="816a0-139">The following code example shows how to unregister and release the registrar.</span></span>

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  <span data-ttu-id="816a0-140">取消註冊並釋放事件提供者。</span><span class="sxs-lookup"><span data-stu-id="816a0-140">Unregister and release the event provider.</span></span>

    <span data-ttu-id="816a0-141">下列程式碼範例示範如何取消登錄和釋放事件提供者。</span><span class="sxs-lookup"><span data-stu-id="816a0-141">The following code example shows how to unregister and release the event provider.</span></span>

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  <span data-ttu-id="816a0-142">清除 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="816a0-142">Clean up the COM server.</span></span>

    <span data-ttu-id="816a0-143">下列程式碼範例示範如何將 COM 程式庫解除初始化。</span><span class="sxs-lookup"><span data-stu-id="816a0-143">The following code example shows how to uninitialize the COM library.</span></span>

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a><span data-ttu-id="816a0-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="816a0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="816a0-145">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="816a0-145">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="816a0-146">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="816a0-146">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="816a0-147">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="816a0-147">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> </dl>

 

 



