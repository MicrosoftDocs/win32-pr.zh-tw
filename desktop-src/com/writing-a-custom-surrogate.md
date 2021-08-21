---
title: 撰寫自訂代理
description: 撰寫自訂代理
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c6098f4d0e9d99be86956bacce413e7e8a4b864a91212d6c2a1a257d9c1db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047656"
---
# <a name="writing-a-custom-surrogate"></a>撰寫自訂代理

雖然系統提供的代理程式在大部分的情況下都是不夠的，但在某些情況下，撰寫自訂代理可能是值得的。 下列是一些範例：

-   自訂代理可以提供某些優化或不存在於系統代理中的語義。
-   如果同進程 DLL 包含的程式碼相依于與用戶端相同的進程，則 DLL 伺服器在系統代理中執行時將無法正常運作。 自訂代理可以針對特定的 DLL 量身訂做，以處理此情況。
-   系統代理支援混合執行緒模型，讓它可以載入可用和單元模型 Dll。 自訂代理可能會基於效率的原因而量身訂做，或針對允許載入的 DLL 類型接受命令列引數。
-   自訂代理可能會採用系統代理不需要的額外命令列參數。
-   系統代理會呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，並告知它使用登錄中的 [AppID](appid-key.md) 機碼下找到的任何現有安全性設定。 自訂代理可能會使用另一個安全性內容。
-   無法遠端 (的介面（例如最新的 OCXs) ）將無法搭配系統代理使用。 自訂代理可以使用本身的實作為包裝 DLL 的介面，並使用 proxy/stub Dll 和可遠端執行的 IDL 定義，讓介面可進行遠端處理。

主要的代理執行緒通常應該執行下列設定步驟：

1.  呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 以初始化執行緒，並設定執行緒模型。
2.  如果您想要在伺服器中執行的 DLL 伺服器能夠使用 **appid** 登錄機碼中的安全性設定，請使用 EOAC AppID 功能來呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) \_ 。 否則，將會使用舊版安全性設定。
3.  呼叫 [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) ，將代理介面註冊至 COM。
4.  針對要求的 CLSID 呼叫 [**ISurrogate：： LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) 。
5.  將主執行緒放在迴圈中，以定期呼叫 [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) 。
6.  當 COM 呼叫 [**ISurrogate：： FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate)時，請撤銷所有的 class factory 並結束。

代理進程必須執行 [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) 介面。 當新的代理程式啟動時，以及呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)之後，應該註冊這個介面。 如上述步驟所示， **ISurrogate** 介面有兩個 COM 呼叫的方法： [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)，以動態方式將新的 DLL 伺服器載入至現有的代理程式。和 [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate)，以釋放代理。

[**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)的執行（使用載入要求的 COM 呼叫）必須先建立支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)、 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)和 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)的 class factory 物件，然後呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)將物件註冊為所要求 CLSID 的 class factory。

代理程式所註冊的 class factory 並非由 DLL 伺服器所執行的實際 class factory，而是由支援 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 和 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)的代理程式所執行的泛型 class factory。 由於它是代理的 class factory，而不是所註冊的 DLL 伺服器，因此代理的 class factory 必須使用 real class factory 來為已註冊的 CLSID 建立物件的實例。 代理的 [**IClassFactory：： CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) 看起來應該如下列範例所示：


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



代理的 class factory 也必須支援 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ，因為呼叫 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 可以向註冊的 class factory 要求任何介面，而不只是 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)。 此外，因為泛型類別 factory 僅支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 和 **IClassFactory**，所以必須將其他介面的要求導向至真正的物件。 因此，應該會有一個 [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) 方法，如下所示：


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



裝載 DLL 伺服器的代理必須使用 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)的呼叫，將 dll 伺服器的類別物件) 發行 (s。 DLL 代理程式的所有 class factory 都應該註冊為 REGCLS \_ 代理。 REGCLS \_ SINGLUSE 和 REGCLS \_ MULTIPLEUSE 不能用於載入至代理程式的 DLL 伺服器。

遵循這些指導方針，以便在需要時建立代理程式，應確保適當的行為。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DLL 代理](dll-surrogates.md)
</dt> </dl>

 

 