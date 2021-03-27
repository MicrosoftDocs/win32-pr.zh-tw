---
description: IHWEventHandler 介面可在執行中的物件資料表中註冊 (的 ROT) ，以便執行的應用程式可以存取自動播放事件。
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: 如何在執行中的應用程式中使用自動播放事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51795a3992bdb40dde833bb3e352905efaa2be63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944182"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a><span data-ttu-id="b7005-103">如何在執行中的應用程式中使用自動播放事件</span><span class="sxs-lookup"><span data-stu-id="b7005-103">How to Use AutoPlay Events in Running Applications</span></span>

<span data-ttu-id="b7005-104">[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)介面可在執行中的物件資料表中註冊 (的 ROT) ，以便執行的應用程式可以存取自動播放事件。</span><span class="sxs-lookup"><span data-stu-id="b7005-104">The [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface can be registered in the running object table (ROT) so that running applications have access to AutoPlay events.</span></span>

<span data-ttu-id="b7005-105">下列指示說明如何在執行中的應用程式中使用自動播放事件。</span><span class="sxs-lookup"><span data-stu-id="b7005-105">The following instructions describe how to use AutoPlay events in running applications.</span></span>

## <a name="instructions"></a><span data-ttu-id="b7005-106">指示</span><span class="sxs-lookup"><span data-stu-id="b7005-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="b7005-107">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="b7005-107">Step 1:</span></span>

<span data-ttu-id="b7005-108">建立可實 [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) 介面的新元件。</span><span class="sxs-lookup"><span data-stu-id="b7005-108">Create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="b7005-109">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="b7005-109">Step 2:</span></span>

<span data-ttu-id="b7005-110">使用 **處理常式** 索引鍵下特定處理常式專案的 InitCmdLine 值，初始化新元件。</span><span class="sxs-lookup"><span data-stu-id="b7005-110">Initialize the new component with the InitCmdLine value from the particular handler's entry under the **Handlers** key.</span></span>

<span data-ttu-id="b7005-111">這是必要步驟，因為自動播放不會呼叫 Initialize 方法。</span><span class="sxs-lookup"><span data-stu-id="b7005-111">This step is required because Autoplay does not call the Initialize method.</span></span>

### <a name="step-3"></a><span data-ttu-id="b7005-112">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="b7005-112">Step 3:</span></span>

<span data-ttu-id="b7005-113">呼叫 [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) 函式，以取得代表您的元件和您想要呼叫的事件處理常式的標記。</span><span class="sxs-lookup"><span data-stu-id="b7005-113">Call the [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) function to get a moniker that represents your component and the event handler that you want to call.</span></span>

### <a name="step-4"></a><span data-ttu-id="b7005-114">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="b7005-114">Step 4:</span></span>

<span data-ttu-id="b7005-115">使用 *ppmoniker* 參數在 ROT 中註冊您的元件。</span><span class="sxs-lookup"><span data-stu-id="b7005-115">Use the *ppmoniker* parameter to register your component in the ROT.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7005-116">備註</span><span class="sxs-lookup"><span data-stu-id="b7005-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7005-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會造成安全性風險。</span><span class="sxs-lookup"><span data-stu-id="b7005-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) can pose security risks.</span></span> <span data-ttu-id="b7005-118">請參閱 **LoadLibrary** 檔，以取得如何使用不同版本的 Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b7005-118">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

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

<span data-ttu-id="b7005-119">呼叫 [**IRunningObjectTable：： Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) 需要元件在登錄中具有下列 **AppID** 資訊。</span><span class="sxs-lookup"><span data-stu-id="b7005-119">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that the component have the following **AppID** information in the registry.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b7005-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7005-120">Related topics</span></span>

[<span data-ttu-id="b7005-121">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="b7005-121">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[<span data-ttu-id="b7005-122">**CreateHardwareEventMoniker**</span><span class="sxs-lookup"><span data-stu-id="b7005-122">**CreateHardwareEventMoniker**</span></span>](createhardwareeventmoniker.md)
