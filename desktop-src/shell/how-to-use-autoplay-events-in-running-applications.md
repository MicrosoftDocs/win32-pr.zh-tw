---
description: IHWEventHandler 介面可在執行中的物件資料表中註冊 (的 ROT) ，以便執行的應用程式可以存取自動播放事件。
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: 如何在執行中的應用程式中使用自動播放事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab30fa020b5501f8832a5b350ad409934ecbb4258d75adf147e908c699516474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714813"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a>如何在執行中的應用程式中使用自動播放事件

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)介面可在執行中的物件資料表中註冊 (的 ROT) ，以便執行的應用程式可以存取自動播放事件。

下列指示說明如何在執行中的應用程式中使用自動播放事件。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

建立可實 [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) 介面的新元件。

### <a name="step-2"></a>步驟 2:

使用 **處理常式** 索引鍵下特定處理常式專案的 InitCmdLine 值，初始化新元件。

這是必要步驟，因為自動播放不會呼叫 Initialize 方法。

### <a name="step-3"></a>步驟 3：

呼叫 [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) 函式，以取得代表您的元件和您想要呼叫的事件處理常式的標記。

### <a name="step-4"></a>步驟 4：

使用 *ppmoniker* 參數在 ROT 中註冊您的元件。

## <a name="remarks"></a>備註

> [!Note]  
> [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會造成安全性風險。 如需如何正確載入具有不同 Windows 版本之 Dll 的相關資訊，請參閱 **LoadLibrary** 檔。

```cpp
typedef HRESULT (*CREATEHARDWAREEVENTMONIKER)(REFCLSID clsid, LPCWSTR pszEventHandler, IMoniker **ppmoniker);

HRESULT RegisterComponent(IUnknown* punk, DWORD* dpwToken)
{
    HRESULT hr = E_FAIL;
    HINSTANCE hinstShSvcs = LoadLibrary(TEXT("shsvcs.dll"));
    
    if (hinstShSvcs)
    {   
        CREATEHARDWAREEVENTMONIKER fct = (CREATEHARDWAREEVENTMONIKER)GetProcAddress(hinstShSvcs, "CreateHardwareEventMoniker");
        if (fct)
        {
            IMoniker* pmoniker;
            
            hr = fct(CLSID_App, TEXT("VideoCameraArrival"), &pmoniker);

            if (SUCCEEDED(hr))
            {
                IRunningObjectTable *prot;
                    
                if (SUCCEEDED(GetRunningObjectTable(0, &prot)))
                {
                    hr = prot->Register(ROTFLAGS_ALLOWANYCLIENT | ROTFLAGS_REGISTRATIONKEEPSALIVE, punk, pmoniker, &_dwRegisterROT);
                    prot->Release();
                }
                pmoniker->Release();
            }
            CoRegisterClassObject(CLSID_App, static_cast<IClassFactory *>(this), CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE, &_dwRegisterClass;
        }
        FreeLibrary(hinstShSvcs);
    }
    return hr;
}
```

呼叫 [**IRunningObjectTable：： Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) 需要元件在登錄中具有下列 **AppID** 資訊。

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="related-topics"></a>相關主題

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[**CreateHardwareEventMoniker**](createhardwareeventmoniker.md)
