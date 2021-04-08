---
description: 取消註冊篩選
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: 取消註冊篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d161b7d1f169b84ba43ac734bf01708a37eb700a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850348"
---
# <a name="unregistering-a-filter"></a>取消註冊篩選

若要取消註冊篩選準則，請執行 **DllUnregisterServer** 函數。 在此函式中，呼叫具有值 **FALSE** 的 DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md)函式。 如果您在註冊篩選時呼叫 **IFilterMapper2：： RegisterFilter** ，請在這裡呼叫 [**IFilterMapper2：： UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) 方法。

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



 

 



