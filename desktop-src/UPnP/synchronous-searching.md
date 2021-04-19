---
title: 同步搜尋
description: 裝置搜尋工具物件可啟用同步和非同步搜尋。 同步搜尋已完成，而且只有在找到所有可用的裝置之後，才會將控制權交還給呼叫的應用程式。
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1890829dfe8386cd79627dde039264dc81e473c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969870"
---
# <a name="synchronous-searching"></a>同步搜尋

裝置搜尋工具物件可啟用同步和非同步搜尋。 同步搜尋已完成，而且只有在找到所有可用的裝置之後，才會將控制權交還給呼叫的應用程式。 若要執行同步搜尋，請使用 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 介面的其中一個同步搜尋方法。

> [!Note]  
> 同步搜尋至少需要九秒的時間才會返回。 延遲的原因是因為必須多次傳送初始的 UDP 搜尋訊息。 這是程度基礎網路通訊協定的重複帳戶。 同步搜尋最適合命令列介面。 不建議針對圖形化使用者介面使用它們。

 

[**IUPnPDeviceFinder：： FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype)方法會依裝置或服務類型來搜尋。 這個方法會採用類型 URI 做為輸入參數，並傳回裝置物件的集合。 裝置物件代表個別裝置。

下列範例示範如何在 VBScript 中執行裝置的同步搜尋。 每個腳本都會使用 [**IUPnPDeviceFinder：： FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype)，以 media player 裝置類型 (服務識別碼) 的類型 URI 進行呼叫， *urn：架構-upnp-org： device： mediaplayer. v 1.00.00*。 方法會傳回對應到所找到媒體播放機裝置的裝置物件集合。 如需從集合解壓縮個別裝置物件的詳細資訊，請參閱 [同步搜尋所傳回的裝置集合](device-collections-returned-by-synchronous-searches.md)。

## <a name="search-for-devices-by-type-in-vbscript"></a>在 VBScript 中依類型搜尋裝置


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>在 c + + 中依類型搜尋裝置

下列範例示範如何使用 c + + 進行媒體播放機裝置的同步搜尋。 函數會接受 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 介面的指標作為輸入，並傳回 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) 介面指標。

此範例會先配置一個 **BSTR** 來代表裝置類型 URI，然後將它傳遞給 [**IUPnPDeviceFinder：： FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) 方法。 它也會將本機 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) 指標的位址傳遞到緩衝區中，方法接著會在該緩衝區中儲存找到的裝置集合。 如果函式呼叫成功，則會將指標傳回至這個集合。


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




