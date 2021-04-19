---
description: Windows Management Instrumentation (WMI) 可以建立接收，以接收用戶端應用程式在個別進程中的非同步回呼。
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: 降低接收器在個別進程中的安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979808"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a><span data-ttu-id="cf098-103">降低接收器在個別進程中的安全性</span><span class="sxs-lookup"><span data-stu-id="cf098-103">Lowering the Security for a Sink in a Separate Process</span></span>

<span data-ttu-id="cf098-104">Windows Management Instrumentation (WMI) 可以建立接收，以接收用戶端應用程式在個別進程中的非同步回呼。</span><span class="sxs-lookup"><span data-stu-id="cf098-104">Windows Management Instrumentation (WMI) can create the sink to receive asynchronous callbacks for a client application in a separate process.</span></span> <span data-ttu-id="cf098-105">Unsecapp.exe 個別的進程。</span><span class="sxs-lookup"><span data-stu-id="cf098-105">The separate process is Unsecapp.exe.</span></span> <span data-ttu-id="cf098-106">使用 [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) 介面。</span><span class="sxs-lookup"><span data-stu-id="cf098-106">Use the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface.</span></span> <span data-ttu-id="cf098-107">**IWbemUnsecuredApartment** 可讓您控制 Unsecapp.exe 是否驗證接收器的回呼。</span><span class="sxs-lookup"><span data-stu-id="cf098-107">**IWbemUnsecuredApartment** allows you to control whether Unsecapp.exe authenticates callbacks to the sink.</span></span> <span data-ttu-id="cf098-108">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="cf098-108">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="cf098-109">然後，您可以降低該程式的安全性，WMI 可以存取接收器而不受限制。</span><span class="sxs-lookup"><span data-stu-id="cf098-109">You can then lower the security on that process and WMI can access the sink without restriction.</span></span> <span data-ttu-id="cf098-110">為了協助進行這項技術，WMI 提供了 Unsecapp.exe 的流程，可作為個別的進程。</span><span class="sxs-lookup"><span data-stu-id="cf098-110">To assist with this technique WMI provides the Unsecapp.exe process to function as the separate process.</span></span> <span data-ttu-id="cf098-111">您可以使用 [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) 介面的呼叫來裝載 Unsecapp.exe。</span><span class="sxs-lookup"><span data-stu-id="cf098-111">You can host Unsecapp.exe with a call to the [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface.</span></span>

<span data-ttu-id="cf098-112">[**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)介面可讓用戶端應用程式建立個別的專用進程，執行 Unsecapp.exe 來裝載 [**IWbemObjectSink**](iwbemobjectsink.md)的執行。</span><span class="sxs-lookup"><span data-stu-id="cf098-112">The [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface allows a client application to create a separate dedicated process running Unsecapp.exe for hosting a [**IWbemObjectSink**](iwbemobjectsink.md) implementation.</span></span> <span data-ttu-id="cf098-113">專用的進程可以呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，將 WMI 存取權授與專用進程，而不會危及主要進程的安全性。</span><span class="sxs-lookup"><span data-stu-id="cf098-113">The dedicated process can call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to grant WMI access to the dedicated process without compromising the security of the main process.</span></span> <span data-ttu-id="cf098-114">初始化之後，專用進程會扮演主要進程與 WMI 之間的媒介。</span><span class="sxs-lookup"><span data-stu-id="cf098-114">After initialization, the dedicated process acts as an intermediary between the main process and WMI.</span></span>

<span data-ttu-id="cf098-115">下列程式描述如何使用 [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)執行非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="cf098-115">The following procedure describes how to perform an asynchronous call with [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span></span>

<span data-ttu-id="cf098-116">**使用 IUnsecuredApartment 執行非同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="cf098-116">**To perform an asynchronous call with IUnsecuredApartment**</span></span>

1.  <span data-ttu-id="cf098-117">使用對 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來建立專用的進程。</span><span class="sxs-lookup"><span data-stu-id="cf098-117">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="cf098-118">下列程式碼範例會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立專用的進程。</span><span class="sxs-lookup"><span data-stu-id="cf098-118">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="cf098-119">將接收器物件具現化。</span><span class="sxs-lookup"><span data-stu-id="cf098-119">Instantiate the sink object.</span></span>

    <span data-ttu-id="cf098-120">下列程式碼範例會建立新的接收物件。</span><span class="sxs-lookup"><span data-stu-id="cf098-120">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="cf098-121">建立接收的存根。</span><span class="sxs-lookup"><span data-stu-id="cf098-121">Create a stub for the sink.</span></span>

    <span data-ttu-id="cf098-122">存根是從接收產生的包裝函式函數。</span><span class="sxs-lookup"><span data-stu-id="cf098-122">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="cf098-123">下列程式碼範例會呼叫 [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) 來建立接收器的存根。</span><span class="sxs-lookup"><span data-stu-id="cf098-123">The following code example calls [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) to create a stub for the sink.</span></span>

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  <span data-ttu-id="cf098-124">呼叫包裝函式的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，並要求 [**IWbemObjectSink**](iwbemobjectsink.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cf098-124">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the wrapper, and request a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="cf098-125">下列程式碼範例會呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，並要求 [**IWbemObjectSink**](iwbemobjectsink.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cf098-125">The following code example calls [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) and requests a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  <span data-ttu-id="cf098-126">釋放接收器物件指標。</span><span class="sxs-lookup"><span data-stu-id="cf098-126">Release the sink object pointer.</span></span>

    <span data-ttu-id="cf098-127">您可以釋放物件指標，因為存根現在擁有指標。</span><span class="sxs-lookup"><span data-stu-id="cf098-127">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="cf098-128">下列程式碼範例會釋放接收器物件指標。</span><span class="sxs-lookup"><span data-stu-id="cf098-128">The following code example releases the sink object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

6.  <span data-ttu-id="cf098-129">在任何非同步呼叫中使用存根。</span><span class="sxs-lookup"><span data-stu-id="cf098-129">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="cf098-130">完成呼叫時，釋放本機參考計數。</span><span class="sxs-lookup"><span data-stu-id="cf098-130">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="cf098-131">下列程式碼範例會在非同步呼叫中使用存根。</span><span class="sxs-lookup"><span data-stu-id="cf098-131">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="cf098-132">有時您可能必須在進行呼叫後取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="cf098-132">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="cf098-133">如果您需要取消呼叫，請使用原先發出呼叫的相同指標取消呼叫。</span><span class="sxs-lookup"><span data-stu-id="cf098-133">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="cf098-134">下列程式碼範例顯示如何取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="cf098-134">The following code example shows how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  <span data-ttu-id="cf098-135">當您使用非同步呼叫完成時，請釋放本機參考計數。</span><span class="sxs-lookup"><span data-stu-id="cf098-135">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="cf098-136">確認不需要取消非同步呼叫之後，請務必釋放 *pStubSink* 指標。</span><span class="sxs-lookup"><span data-stu-id="cf098-136">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not need to be canceled.</span></span> <span data-ttu-id="cf098-137">此外，在 WMI 釋放 *pSink* 接收器指標之後，請勿釋放 *pStubSink* 。</span><span class="sxs-lookup"><span data-stu-id="cf098-137">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="cf098-138">在 *pSink* 之後釋放 *pStubSink* 會建立迴圈參考計數，讓接收和存根永遠留在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="cf098-138">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="cf098-139">相反地，釋放指標的可能位置是在 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 呼叫中，由 WMI 發出，以報告原始非同步呼叫已完成。</span><span class="sxs-lookup"><span data-stu-id="cf098-139">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

8.  <span data-ttu-id="cf098-140">完成時，透過呼叫 [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)將 COM 解除初始化。</span><span class="sxs-lookup"><span data-stu-id="cf098-140">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="cf098-141">下列程式碼範例顯示如何在 *pUnsecApp* 指標上呼叫 [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="cf098-141">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

    <span data-ttu-id="cf098-142">本主題中的程式碼範例需要下列參考和 \# include 語句，才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="cf098-142">The code examples in this topic require the following reference and \#include statement to correctly compile.</span></span>

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

<span data-ttu-id="cf098-143">如需有關 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函式和參數的詳細資訊，請參閱平臺軟體發展工具組中的 [COM](../cossdk/component-services-portal.md) 檔 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="cf098-143">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation in the Platform Software Development Kit (SDK).</span></span>

 

 
