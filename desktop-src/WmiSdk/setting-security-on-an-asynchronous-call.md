---
description: 非同步呼叫會帶來嚴重的安全性風險，因為對接收器的回呼可能不是原始應用程式或腳本的非同步呼叫結果。
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: 在非同步呼叫上設定安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996980"
---
# <a name="setting-security-on-an-asynchronous-call"></a><span data-ttu-id="72fc3-103">在非同步呼叫上設定安全性</span><span class="sxs-lookup"><span data-stu-id="72fc3-103">Setting Security on an Asynchronous Call</span></span>

<span data-ttu-id="72fc3-104">非同步呼叫會帶來嚴重的安全性風險，因為對 [*接收器*](gloss-s.md) 的回呼可能不是原始應用程式或腳本的非同步呼叫結果。</span><span class="sxs-lookup"><span data-stu-id="72fc3-104">Asynchronous calls present serious security risks because a callback to the [*sink*](gloss-s.md) may not be a result of the asynchronous call by the original application or script.</span></span> <span data-ttu-id="72fc3-105">遠端連線中的安全性是以遠端電腦上用戶端與提供者之間的通訊加密為基礎。</span><span class="sxs-lookup"><span data-stu-id="72fc3-105">Security in remote connections is based on encryption of the communication between the client and the provider on the remote computer.</span></span> <span data-ttu-id="72fc3-106">在 c + + 中，您可以透過 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)呼叫中的驗證層級參數設定加密。</span><span class="sxs-lookup"><span data-stu-id="72fc3-106">In C++ you can set encryption through the authentication level parameter in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="72fc3-107">在腳本中，請在 [**SWbemSecurity**](swbemsecurity.md)物件上設定 *AuthenticationLevel* 。</span><span class="sxs-lookup"><span data-stu-id="72fc3-107">In scripting, set the *AuthenticationLevel* in the moniker connection or on an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="72fc3-108">如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="72fc3-108">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="72fc3-109">非同步呼叫的安全性風險存在，因為 WMI 會降低回呼的驗證層級，直到回呼成功為止。</span><span class="sxs-lookup"><span data-stu-id="72fc3-109">The security risks for asynchronous calls exist because WMI lowers the authentication level on a callback until the callback succeeds.</span></span> <span data-ttu-id="72fc3-110">在連出的非同步呼叫上，用戶端可以設定與 WMI 的連線上的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="72fc3-110">On an outgoing asynchronous call, the client can set the authentication level on the connection to WMI.</span></span> <span data-ttu-id="72fc3-111">WMI 會抓取用戶端呼叫上的安全性設定，並嘗試使用相同的驗證層級回撥。</span><span class="sxs-lookup"><span data-stu-id="72fc3-111">WMI retrieves the security settings on the client call and attempts to call back with the same authentication level.</span></span> <span data-ttu-id="72fc3-112">回呼一律會在 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權** 等級起始。</span><span class="sxs-lookup"><span data-stu-id="72fc3-112">The callback is always initiated at the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** level.</span></span> <span data-ttu-id="72fc3-113">如果回呼失敗，WMI 會將驗證層級減少到回呼可以成功的層級（如有必要）至 **RPC \_ C \_ 驗證 \_ 層級 \_ 無**。</span><span class="sxs-lookup"><span data-stu-id="72fc3-113">If the callback fails, WMI lowers the authentication level to a level where the callback can succeed, if necessary, to **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span> <span data-ttu-id="72fc3-114">在本機系統（驗證服務不是 Kerberos）內的呼叫內容中，永遠會在 **RPC \_ C \_ 驗證 \_ 層級 \_** 傳回回呼。</span><span class="sxs-lookup"><span data-stu-id="72fc3-114">In the context of calls within the local system where the authentication service is not Kerberos, the callback is always returned at **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span>

<span data-ttu-id="72fc3-115">最小驗證層級為腳本) 的 **RPC \_ C \_ 驗證 \_ 層級 \_ PKT** (**wbemAuthenticationLevelPkt**。</span><span class="sxs-lookup"><span data-stu-id="72fc3-115">The minimum authentication level is **RPC\_C\_AUTHN\_LEVEL\_PKT** (**wbemAuthenticationLevelPkt** for scripting).</span></span> <span data-ttu-id="72fc3-116">不過，您可以指定較高的層級，例如 **RPC \_ C \_ 驗證 \_ Level \_ PKT \_ 隱私權** (**wbemAuthenticationLevelPktPrivacy**) 。</span><span class="sxs-lookup"><span data-stu-id="72fc3-116">However, you can specify a higher level, such as **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="72fc3-117">建議用戶端應用程式或腳本將驗證層級設定為 **RPC \_ C \_ 驗證 \_ level \_ DEFAULT** (**wbemAuthenticationLevelDefault**) 這可讓驗證等級與伺服器所指定的層級進行協調。</span><span class="sxs-lookup"><span data-stu-id="72fc3-117">It is recommended that client applications or scripts set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** (**wbemAuthenticationLevelDefault**) which allows the authentication level to be negotiated to the level specified by the server.</span></span>

<span data-ttu-id="72fc3-118">**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** 登錄值控制 WMI 是否會檢查回呼中可接受的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="72fc3-118">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level in callbacks.</span></span> <span data-ttu-id="72fc3-119">這是保護在腳本或 Visual Basic 中進行的非同步呼叫之接收安全性的唯一機制。</span><span class="sxs-lookup"><span data-stu-id="72fc3-119">This is the only mechanism for protecting sink security for asynchronous calls made in scripting or Visual Basic.</span></span> <span data-ttu-id="72fc3-120">依預設，此登錄機碼設定為零。</span><span class="sxs-lookup"><span data-stu-id="72fc3-120">By default, this registry key is set to zero.</span></span> <span data-ttu-id="72fc3-121">如果登錄機碼為零，則 WMI 不會驗證驗證層級。</span><span class="sxs-lookup"><span data-stu-id="72fc3-121">If the registry key is zero then WMI does not verify authentication levels.</span></span> <span data-ttu-id="72fc3-122">若要保護腳本中的非同步呼叫，請將登錄機碼設定為1。</span><span class="sxs-lookup"><span data-stu-id="72fc3-122">To secure asynchronous calls in scripting, set the registry key to 1.</span></span> <span data-ttu-id="72fc3-123">C + + 用戶端可以呼叫 [**IWbemUnsecuredApartment：： CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) 來控制接收的存取。</span><span class="sxs-lookup"><span data-stu-id="72fc3-123">C++ clients can call [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) to control access to the sink.</span></span> <span data-ttu-id="72fc3-124">預設會在任何位置建立這個值。</span><span class="sxs-lookup"><span data-stu-id="72fc3-124">The value is created anywhere by default.</span></span>

<span data-ttu-id="72fc3-125">下列主題提供設定非同步呼叫安全性的範例：</span><span class="sxs-lookup"><span data-stu-id="72fc3-125">The following topics provide examples of setting asynchronous call security:</span></span>

-   [<span data-ttu-id="72fc3-126">在 VBScript 中設定非同步呼叫的安全性</span><span class="sxs-lookup"><span data-stu-id="72fc3-126">Setting Security on an Asynchronous Call in VBScript</span></span>](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   <span data-ttu-id="72fc3-127">設定 c + + 中的非同步呼叫安全性</span><span class="sxs-lookup"><span data-stu-id="72fc3-127">Setting Asynchronous Call Security in C++</span></span>

## <a name="setting-asynchronous-call-security-in-c"></a><span data-ttu-id="72fc3-128">設定 c + + 中的非同步呼叫安全性</span><span class="sxs-lookup"><span data-stu-id="72fc3-128">Setting Asynchronous Call Security in C++</span></span>

<span data-ttu-id="72fc3-129">[**IWbemUnsecuredApartment：： CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub)方法類似于 [**IUnsecuredApartment：： CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub)方法，會在個別的進程中建立接收，Unsecapp.exe 來接收回呼。</span><span class="sxs-lookup"><span data-stu-id="72fc3-129">The [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) method is similar to [**IUnsecuredApartment::CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) method and creates a sink in a separate process, Unsecapp.exe, to receive callbacks.</span></span> <span data-ttu-id="72fc3-130">但是， **CreateSinkStub** 方法具有 *>dwflag* 參數，可指定個別進程處理存取控制的方式。</span><span class="sxs-lookup"><span data-stu-id="72fc3-130">However, the **CreateSinkStub** method has a *dwFlag* parameter that specifies how the separate process handles access control.</span></span>

<span data-ttu-id="72fc3-131">*>dwflag* 參數會為 Unsecapp.exe 指定下列其中一個動作：</span><span class="sxs-lookup"><span data-stu-id="72fc3-131">The *dwFlag* parameter specifies one of the following actions for Unsecapp.exe:</span></span>

-   <span data-ttu-id="72fc3-132">使用登錄機碼設定來判斷是否要檢查存取權。</span><span class="sxs-lookup"><span data-stu-id="72fc3-132">Use the registry key setting to determine whether or not to check access.</span></span>
-   <span data-ttu-id="72fc3-133">略過登錄機碼，並一律檢查存取權。</span><span class="sxs-lookup"><span data-stu-id="72fc3-133">Ignore the registry key and always check access.</span></span>
-   <span data-ttu-id="72fc3-134">略過登錄機碼，而且絕不檢查存取權。</span><span class="sxs-lookup"><span data-stu-id="72fc3-134">Ignore the registry key and never check access.</span></span>

<span data-ttu-id="72fc3-135">本主題中的程式碼範例需要下列 \# include 語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="72fc3-135">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="72fc3-136">下列程式描述如何使用 [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment)執行非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="72fc3-136">The following procedure describes how to perform an asynchronous call with [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span></span>

<span data-ttu-id="72fc3-137">**使用 IWbemUnsecuredApartment 執行非同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="72fc3-137">**To perform an asynchronous call with IWbemUnsecuredApartment**</span></span>

1.  <span data-ttu-id="72fc3-138">使用對 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來建立專用的進程。</span><span class="sxs-lookup"><span data-stu-id="72fc3-138">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="72fc3-139">下列程式碼範例會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立專用的進程。</span><span class="sxs-lookup"><span data-stu-id="72fc3-139">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
                     (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="72fc3-140">將接收器物件具現化。</span><span class="sxs-lookup"><span data-stu-id="72fc3-140">Instantiate the sink object.</span></span>

    <span data-ttu-id="72fc3-141">下列程式碼範例會建立新的接收物件。</span><span class="sxs-lookup"><span data-stu-id="72fc3-141">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="72fc3-142">建立接收的存根。</span><span class="sxs-lookup"><span data-stu-id="72fc3-142">Create a stub for the sink.</span></span>

    <span data-ttu-id="72fc3-143">存根是從接收產生的包裝函式函數。</span><span class="sxs-lookup"><span data-stu-id="72fc3-143">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="72fc3-144">下列程式碼範例會建立接收器的存根。</span><span class="sxs-lookup"><span data-stu-id="72fc3-144">The following code example creates a stub for the sink.</span></span>

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  <span data-ttu-id="72fc3-145">釋放接收器物件指標。</span><span class="sxs-lookup"><span data-stu-id="72fc3-145">Release the sink object pointer.</span></span>

    <span data-ttu-id="72fc3-146">您可以釋放物件指標，因為存根現在擁有指標。</span><span class="sxs-lookup"><span data-stu-id="72fc3-146">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="72fc3-147">下列程式碼範例會釋放物件指標。</span><span class="sxs-lookup"><span data-stu-id="72fc3-147">The following code example releases the object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

5.  <span data-ttu-id="72fc3-148">在任何非同步呼叫中使用存根。</span><span class="sxs-lookup"><span data-stu-id="72fc3-148">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="72fc3-149">完成呼叫時，釋放本機參考計數。</span><span class="sxs-lookup"><span data-stu-id="72fc3-149">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="72fc3-150">下列程式碼範例會在非同步呼叫中使用存根。</span><span class="sxs-lookup"><span data-stu-id="72fc3-150">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="72fc3-151">有時您可能必須在進行呼叫後取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="72fc3-151">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="72fc3-152">如果您需要取消呼叫，請使用原先發出呼叫的相同指標取消呼叫。</span><span class="sxs-lookup"><span data-stu-id="72fc3-152">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="72fc3-153">下列程式碼範例說明如何取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="72fc3-153">The following code example describes how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  <span data-ttu-id="72fc3-154">當您使用非同步呼叫完成時，請釋放本機參考計數。</span><span class="sxs-lookup"><span data-stu-id="72fc3-154">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="72fc3-155">請務必在確認非同步呼叫不需要取消之後，才釋放 *pStubSink* 指標。</span><span class="sxs-lookup"><span data-stu-id="72fc3-155">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not must be canceled.</span></span> <span data-ttu-id="72fc3-156">此外，在 WMI 釋放 *pSink* 接收器指標之後，請勿釋放 *pStubSink* 。</span><span class="sxs-lookup"><span data-stu-id="72fc3-156">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="72fc3-157">在 *pSink* 之後釋放 *pStubSink* 會建立迴圈參考計數，讓接收和存根永遠留在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="72fc3-157">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="72fc3-158">相反地，釋放指標的可能位置是在 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 呼叫中，由 WMI 發出，以報告原始非同步呼叫已完成。</span><span class="sxs-lookup"><span data-stu-id="72fc3-158">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

7.  <span data-ttu-id="72fc3-159">完成時，透過呼叫 [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)將 COM 解除初始化。</span><span class="sxs-lookup"><span data-stu-id="72fc3-159">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="72fc3-160">下列程式碼範例顯示如何在 *pUnsecApp* 指標上呼叫 [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="72fc3-160">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

<span data-ttu-id="72fc3-161">如需 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數和參數的詳細資訊，請參閱 [COM](../cossdk/component-services-portal.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="72fc3-161">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation.</span></span>

 

 
