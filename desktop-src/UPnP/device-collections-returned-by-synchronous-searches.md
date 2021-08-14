---
title: 同步搜尋所傳回的裝置集合
description: 裝置集合是包含一或多個裝置物件的物件。 裝置集合會公開 IUPnPDevices 介面，這個介面會提供方法和屬性來進行集合和解壓縮個別的裝置物件。
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94901dd2f3988327c32d7c21799ff4db7647e76fd987247e903501bd8937851a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755524"
---
# <a name="device-collections-returned-by-synchronous-searches"></a>同步搜尋所傳回的裝置集合

裝置集合是包含一或多個裝置物件的物件。 裝置集合會公開 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) 介面，這個介面會提供方法和屬性來進行集合和解壓縮個別的裝置物件。

## <a name="vbscript-example"></a>VBScript 範例

VBScript 應用程式可以透過兩種方式存取集合中的物件。 首先，他們可以依序使用 for .。。 每個。。。下一個迴圈，如下列範例所示：


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



在此範例中，會假設裝置變數已初始化為先前搜尋的結果。 迴圈會逐步執行集合中的裝置物件，並依次指派變數 deviceObj 每個裝置物件的值。 迴圈的主體可以包含處理裝置物件的程式碼。

## <a name="c-example"></a>C + + 範例

下列範例顯示存取裝置物件集合中的物件所需的 c + + 程式碼。 **TraverseCollection** 所顯示的函式會接收 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)介面的指標做為輸入參數。 此介面指標可由裝置搜尋工具物件的 [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) 方法或其他 **尋找** 方法傳回。


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



第一個步驟是使用 [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum)屬性來要求集合的新枚舉器。 這會傳回一個枚舉器作為 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。 範例程式碼會叫用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 然後，範例程式碼會叫用 [**IEnumVARIANT：： Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) 方法，將列舉值設定為集合的開頭。 最後，範例程式碼會叫用 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) 方法以遍歷集合。 集合中的裝置物件包含在 **VARIANT** 結構內。 這些結構包含裝置物件上的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面指標。 為了取得 [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)介面，範例程式碼會在 **IDispatch** 介面上叫用 **QueryInterface** 。

 

 