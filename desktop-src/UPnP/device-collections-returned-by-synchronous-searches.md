---
title: 同步搜尋所傳回的裝置集合
description: 裝置集合是包含一或多個裝置物件的物件。 裝置集合會公開 IUPnPDevices 介面，這個介面會提供方法和屬性來進行集合和解壓縮個別的裝置物件。
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd581b7c79fe67a825e411d53e8c44c0f3d4326
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093011"
---
# <a name="device-collections-returned-by-synchronous-searches"></a><span data-ttu-id="e15e3-104">同步搜尋所傳回的裝置集合</span><span class="sxs-lookup"><span data-stu-id="e15e3-104">Device Collections Returned By Synchronous Searches</span></span>

<span data-ttu-id="e15e3-105">裝置集合是包含一或多個裝置物件的物件。</span><span class="sxs-lookup"><span data-stu-id="e15e3-105">Device collections are objects that contain one or more Device objects.</span></span> <span data-ttu-id="e15e3-106">裝置集合會公開 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) 介面，這個介面會提供方法和屬性來進行集合和解壓縮個別的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="e15e3-106">A Device collection exposes the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface that provides methods and properties for traversing the collection and extracting individual device objects.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="e15e3-107">VBScript 範例</span><span class="sxs-lookup"><span data-stu-id="e15e3-107">VBScript Example</span></span>

<span data-ttu-id="e15e3-108">VBScript 應用程式可以透過兩種方式存取集合中的物件。</span><span class="sxs-lookup"><span data-stu-id="e15e3-108">VBScript applications can access the objects in the collection in two ways.</span></span> <span data-ttu-id="e15e3-109">首先，他們可以依序使用 for .。。</span><span class="sxs-lookup"><span data-stu-id="e15e3-109">First, they can traverse the elements sequentially using a for …</span></span> <span data-ttu-id="e15e3-110">每個。。。下一個迴圈，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="e15e3-110">each ... next loop as shown in the following example:</span></span>


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



<span data-ttu-id="e15e3-111">在此範例中，會假設裝置變數已初始化為先前搜尋的結果。</span><span class="sxs-lookup"><span data-stu-id="e15e3-111">In this example, the devices variable is assumed to have been initialized with the result of a prior search.</span></span> <span data-ttu-id="e15e3-112">迴圈會逐步執行集合中的裝置物件，並依次指派變數 deviceObj 每個裝置物件的值。</span><span class="sxs-lookup"><span data-stu-id="e15e3-112">The loop steps through the Device objects in the collection, assigning the variable deviceObj the value of each Device object in turn.</span></span> <span data-ttu-id="e15e3-113">迴圈的主體可以包含處理裝置物件的程式碼。</span><span class="sxs-lookup"><span data-stu-id="e15e3-113">The body of the loop can contain code that processes the Device object.</span></span>

## <a name="c-example"></a><span data-ttu-id="e15e3-114">C + + 範例</span><span class="sxs-lookup"><span data-stu-id="e15e3-114">C++ Example</span></span>

<span data-ttu-id="e15e3-115">下列範例顯示存取裝置物件集合中的物件所需的 c + + 程式碼。</span><span class="sxs-lookup"><span data-stu-id="e15e3-115">The following example shows the C++ code required to access the objects in a collection of device objects.</span></span> <span data-ttu-id="e15e3-116">**TraverseCollection** 所顯示的函式會接收 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)介面的指標做為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="e15e3-116">The function shown, **TraverseCollection**, receives a pointer to the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface as an input parameter.</span></span> <span data-ttu-id="e15e3-117">此介面指標可由裝置搜尋工具物件的 [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) 方法或其他 **尋找** 方法傳回。</span><span class="sxs-lookup"><span data-stu-id="e15e3-117">This interface pointer could be returned by the [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method, or other **Find** methods, of the Device Finder object.</span></span>


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



<span data-ttu-id="e15e3-118">第一個步驟是使用 [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum)屬性來要求集合的新枚舉器。</span><span class="sxs-lookup"><span data-stu-id="e15e3-118">The first step is to request a new enumerator for the collection using the [**\_NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) property.</span></span> <span data-ttu-id="e15e3-119">這會傳回一個枚舉器作為 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。</span><span class="sxs-lookup"><span data-stu-id="e15e3-119">This returns an enumerator as the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e15e3-120">範例程式碼會叫用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="e15e3-120">The sample code invokes [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="e15e3-121">然後，範例程式碼會叫用 [**IEnumVARIANT：： Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) 方法，將列舉值設定為集合的開頭。</span><span class="sxs-lookup"><span data-stu-id="e15e3-121">The sample code then sets the enumerator to the beginning of the collection by invoking the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) method.</span></span> <span data-ttu-id="e15e3-122">最後，範例程式碼會叫用 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) 方法以遍歷集合。</span><span class="sxs-lookup"><span data-stu-id="e15e3-122">Finally, the sample code invokes the [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) method to traverse the collection.</span></span> <span data-ttu-id="e15e3-123">集合中的裝置物件包含在 **VARIANT** 結構內。</span><span class="sxs-lookup"><span data-stu-id="e15e3-123">The device objects in the collection are contained within **VARIANT** structures.</span></span> <span data-ttu-id="e15e3-124">這些結構包含裝置物件上的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="e15e3-124">These structures contain pointers to [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces on the device objects.</span></span> <span data-ttu-id="e15e3-125">為了取得 [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)介面，範例程式碼會在 **IDispatch** 介面上叫用 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="e15e3-125">To obtain the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface, the sample code invokes **QueryInterface** on the **IDispatch** interface.</span></span>

 

 