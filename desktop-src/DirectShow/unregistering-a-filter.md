---
description: 取消註冊篩選
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: 取消註冊篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e26f2d524ff501fcff1db645c9ccdf1a1c9c80c4056af1af206b996f801207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049678"
---
# <a name="unregistering-a-filter"></a>取消註冊篩選

若要取消註冊篩選準則，請執行 **DllUnregisterServer** 函數。 在此函式中，呼叫值為 **FALSE** 的 DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md)函數。 如果您在註冊篩選時呼叫 **IFilterMapper2：： RegisterFilter** ，請在這裡呼叫 [**IFilterMapper2：： UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) 方法。

下列範例示範如何取消註冊篩選：


```C++
STDAPI DllUnregisterServer()
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
        return hr;
 
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_SomeFilter);

    pFM2->Release();
    return hr;
}
```



 

 



