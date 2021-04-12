---
title: 撰寫自訂代理
description: 撰寫自訂代理
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316513"
---
# <a name="writing-a-custom-surrogate"></a><span data-ttu-id="c3350-103">撰寫自訂代理</span><span class="sxs-lookup"><span data-stu-id="c3350-103">Writing a Custom Surrogate</span></span>

<span data-ttu-id="c3350-104">雖然系統提供的代理程式在大部分的情況下都是不夠的，但在某些情況下，撰寫自訂代理可能是值得的。</span><span class="sxs-lookup"><span data-stu-id="c3350-104">While the system-supplied surrogate will be more than adequate for most situations, there are some cases where writing a custom surrogate could be worthwhile.</span></span> <span data-ttu-id="c3350-105">下列是一些範例：</span><span class="sxs-lookup"><span data-stu-id="c3350-105">Following are some examples:</span></span>

-   <span data-ttu-id="c3350-106">自訂代理可以提供某些優化或不存在於系統代理中的語義。</span><span class="sxs-lookup"><span data-stu-id="c3350-106">A custom surrogate could provide some optimizations or semantics not present in the system surrogate.</span></span>
-   <span data-ttu-id="c3350-107">如果同進程 DLL 包含的程式碼相依于與用戶端相同的進程，則 DLL 伺服器在系統代理中執行時將無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c3350-107">If an in-process DLL contains code that depends on being in the same process as the client, the DLL server will not function correctly if it is running in the system surrogate.</span></span> <span data-ttu-id="c3350-108">自訂代理可以針對特定的 DLL 量身訂做，以處理此情況。</span><span class="sxs-lookup"><span data-stu-id="c3350-108">A custom surrogate could be tailored to a specific DLL to deal with this.</span></span>
-   <span data-ttu-id="c3350-109">系統代理支援混合執行緒模型，讓它可以載入可用和單元模型 Dll。</span><span class="sxs-lookup"><span data-stu-id="c3350-109">The system surrogate supports a mixed-threading model so that it can load both free and apartment model DLLs.</span></span> <span data-ttu-id="c3350-110">自訂代理可能會基於效率的原因而量身訂做，或針對允許載入的 DLL 類型接受命令列引數。</span><span class="sxs-lookup"><span data-stu-id="c3350-110">A custom surrogate might be tailored to load only apartment DLLs for reasons of efficiency or to accept a command-line argument for the type of DLL it is allowed to load.</span></span>
-   <span data-ttu-id="c3350-111">自訂代理可能會採用系統代理不需要的額外命令列參數。</span><span class="sxs-lookup"><span data-stu-id="c3350-111">A custom surrogate could take extra command-line parameters that the system surrogate does not.</span></span>
-   <span data-ttu-id="c3350-112">系統代理會呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，並告知它使用登錄中的 [AppID](appid-key.md) 機碼下找到的任何現有安全性設定。</span><span class="sxs-lookup"><span data-stu-id="c3350-112">The system surrogate calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and tells it to use any existing security settings found under the [AppID](appid-key.md) key in the registry.</span></span> <span data-ttu-id="c3350-113">自訂代理可能會使用另一個安全性內容。</span><span class="sxs-lookup"><span data-stu-id="c3350-113">A custom surrogate could use another security context.</span></span>
-   <span data-ttu-id="c3350-114">無法遠端 (的介面（例如最新的 OCXs) ）將無法搭配系統代理使用。</span><span class="sxs-lookup"><span data-stu-id="c3350-114">Interfaces that aren't remotable (such as those for recent OCXs) will not work with the system surrogate.</span></span> <span data-ttu-id="c3350-115">自訂代理可以使用本身的實作為包裝 DLL 的介面，並使用 proxy/stub Dll 和可遠端執行的 IDL 定義，讓介面可進行遠端處理。</span><span class="sxs-lookup"><span data-stu-id="c3350-115">A custom surrogate could wrap the DLL's interfaces with its own implementation and use proxy/stub DLLs with a remotable IDL definition that would allow the interface to be remoted.</span></span>

<span data-ttu-id="c3350-116">主要的代理執行緒通常應該執行下列設定步驟：</span><span class="sxs-lookup"><span data-stu-id="c3350-116">The main surrogate thread should typically perform the following setup steps:</span></span>

1.  <span data-ttu-id="c3350-117">呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 以初始化執行緒，並設定執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="c3350-117">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the thread and set the threading model.</span></span>
2.  <span data-ttu-id="c3350-118">如果您想要在伺服器中執行的 DLL 伺服器能夠使用 **appid** 登錄機碼中的安全性設定，請使用 EOAC AppID 功能來呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) \_ 。</span><span class="sxs-lookup"><span data-stu-id="c3350-118">If you want the DLL servers that are to run in the server to be able to use the security settings in the **AppID** registry key, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) with the EOAC\_APPID capability.</span></span> <span data-ttu-id="c3350-119">否則，將會使用舊版安全性設定。</span><span class="sxs-lookup"><span data-stu-id="c3350-119">Otherwise, legacy security settings will be used.</span></span>
3.  <span data-ttu-id="c3350-120">呼叫 [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) ，將代理介面註冊至 COM。</span><span class="sxs-lookup"><span data-stu-id="c3350-120">Call [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) to register the surrogate interface to COM.</span></span>
4.  <span data-ttu-id="c3350-121">針對要求的 CLSID 呼叫 [**ISurrogate：： LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) 。</span><span class="sxs-lookup"><span data-stu-id="c3350-121">Call [**ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) for the requested CLSID.</span></span>
5.  <span data-ttu-id="c3350-122">將主執行緒放在迴圈中，以定期呼叫 [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) 。</span><span class="sxs-lookup"><span data-stu-id="c3350-122">Put main thread in a loop to call [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodically.</span></span>
6.  <span data-ttu-id="c3350-123">當 COM 呼叫 [**ISurrogate：： FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate)時，請撤銷所有的 class factory 並結束。</span><span class="sxs-lookup"><span data-stu-id="c3350-123">When COM calls [**ISurrogate::FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revoke all class factories and exit.</span></span>

<span data-ttu-id="c3350-124">代理進程必須執行 [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) 介面。</span><span class="sxs-lookup"><span data-stu-id="c3350-124">A surrogate process must implement the [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) interface.</span></span> <span data-ttu-id="c3350-125">當新的代理程式啟動時，以及呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)之後，應該註冊這個介面。</span><span class="sxs-lookup"><span data-stu-id="c3350-125">This interface should be registered when a new surrogate is started and after calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span> <span data-ttu-id="c3350-126">如上述步驟所示， **ISurrogate** 介面有兩個 COM 呼叫的方法： [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)，以動態方式將新的 DLL 伺服器載入至現有的代理程式。和 [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate)，以釋放代理。</span><span class="sxs-lookup"><span data-stu-id="c3350-126">As indicated in the preceding steps, the **ISurrogate** interface has two methods that COM calls: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), to dynamically load new DLL servers into existing surrogates; and [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), to free the surrogate.</span></span>

<span data-ttu-id="c3350-127">[**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)的執行（使用載入要求的 COM 呼叫）必須先建立支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)、 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)和 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)的 class factory 物件，然後呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)將物件註冊為所要求 CLSID 的 class factory。</span><span class="sxs-lookup"><span data-stu-id="c3350-127">The implementation of [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), which COM calls with a load request, must first create a class factory object that supports [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), and then call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) to register the object as the class factory for the requested CLSID.</span></span>

<span data-ttu-id="c3350-128">代理程式所註冊的 class factory 並非由 DLL 伺服器所執行的實際 class factory，而是由支援 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 和 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)的代理程式所執行的泛型 class factory。</span><span class="sxs-lookup"><span data-stu-id="c3350-128">The class factory registered by the surrogate process is not the actual class factory implemented by the DLL server but is a generic class factory implemented by the surrogate process that supports [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span></span> <span data-ttu-id="c3350-129">由於它是代理的 class factory，而不是所註冊的 DLL 伺服器，因此代理的 class factory 必須使用 real class factory 來為已註冊的 CLSID 建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="c3350-129">Because it is the surrogate's class factory, rather than that of the DLL server that is being registered, the surrogate's class factory will need to use the real class factory to create an instance of the object for the registered CLSID.</span></span> <span data-ttu-id="c3350-130">代理的 [**IClassFactory：： CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) 看起來應該如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="c3350-130">The surrogate's [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) should look something like the following example:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::CreateInstance(
  IUnknown* pUnkOuter, 
  REFIID iid, 
  void** ppv)
{
    void* pcf;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, IID_IClassFactory, &pcf);
    if ( FAILED(hr) )
        return hr;
    hr = ((IClassFactory*)pcf)->CreateInstance(pUnkOuter, iid, ppv);
    ((IClassFactory*)pcf)->Release();
    return hr;
}
 
```



<span data-ttu-id="c3350-131">代理的 class factory 也必須支援 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ，因為呼叫 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 可以向註冊的 class factory 要求任何介面，而不只是 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)。</span><span class="sxs-lookup"><span data-stu-id="c3350-131">The surrogate's class factory must also support [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) because a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) can request any interface from the registered class factory, not just [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="c3350-132">此外，因為泛型類別 factory 僅支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 和 **IClassFactory**，所以必須將其他介面的要求導向至真正的物件。</span><span class="sxs-lookup"><span data-stu-id="c3350-132">Further, since the generic class factory supports only [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and **IClassFactory**, requests for other interfaces must be directed to the real object.</span></span> <span data-ttu-id="c3350-133">因此，應該會有一個 [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) 方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c3350-133">Thus, there should be a [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) method which should be similar to the following:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::MarshalInterface(
  IStream *pStm,  
  REFIID riid, void *pv, 
  WORD dwDestContext, 
  void *pvDestContext, 
  DWORD mshlflags )
{   
    void * pCF = NULL;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, riid, &pCF);
    if ( FAILED(hr) )
        return hr;   
    hr = CoMarshalInterface(pStm, riid, (IUnknown*)pCF, dwDestContext, pvDestContext,  mshlflags);
    ((IUnknown*)pCF)->Release();
    return S_OK;
 
```



<span data-ttu-id="c3350-134">裝載 DLL 伺服器的代理必須使用 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)的呼叫，將 dll 伺服器的類別物件) 發行 (s。</span><span class="sxs-lookup"><span data-stu-id="c3350-134">The surrogate that houses a DLL server must publish the DLL server's class object(s) with a call to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span></span> <span data-ttu-id="c3350-135">DLL 代理程式的所有 class factory 都應該註冊為 REGCLS \_ 代理。</span><span class="sxs-lookup"><span data-stu-id="c3350-135">All class factories for DLL surrogates should be registered as REGCLS\_SURROGATE.</span></span> <span data-ttu-id="c3350-136">REGCLS \_ SINGLUSE 和 REGCLS \_ MULTIPLEUSE 不能用於載入至代理程式的 DLL 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c3350-136">REGCLS\_SINGLUSE and REGCLS\_MULTIPLEUSE should not be used for DLL servers loaded into surrogates.</span></span>

<span data-ttu-id="c3350-137">遵循這些指導方針，以便在需要時建立代理程式，應確保適當的行為。</span><span class="sxs-lookup"><span data-stu-id="c3350-137">Following these guidelines for creating a surrogate process when it is necessary to do so should ensure proper behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3350-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3350-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3350-139">DLL 代理</span><span class="sxs-lookup"><span data-stu-id="c3350-139">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 