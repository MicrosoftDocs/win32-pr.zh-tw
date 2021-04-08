---
title: 建立裝置搜尋工具
description: 下列範例示範如何在 c + +、Visual Basic 和 VBScript 中建立裝置搜尋工具物件的實例。
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a12fc7e269f2c0ce5b577fe2f49b6d13fe3b5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840531"
---
# <a name="creating-the-device-finder"></a>建立裝置搜尋工具

下列範例示範如何在 c + +、Visual Basic 和 VBScript 中建立裝置搜尋工具物件的實例。 指令碼語言使用 (ProgID) [**UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 的程式設計識別碼來識別裝置搜尋工具類別。 C + + 程式碼使用類別識別碼。

## <a name="c-example"></a>C + + 範例


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



如這個 c + + 範例所示，裝置搜尋工具物件會公開預設介面 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)。 這個介面的方法會根據以 UPnP 為基礎之裝置的有效搜尋準則來執行搜尋。 這個介面具備自動化功能，因此可以透過腳本來呼叫其方法。

## <a name="vbscript-example"></a>VBScript 範例


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




