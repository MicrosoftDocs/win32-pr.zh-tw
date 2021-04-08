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
# <a name="unregistering-a-filter"></a><span data-ttu-id="b47f4-103">取消註冊篩選</span><span class="sxs-lookup"><span data-stu-id="b47f4-103">Unregistering a Filter</span></span>

<span data-ttu-id="b47f4-104">若要取消註冊篩選準則，請執行 **DllUnregisterServer** 函數。</span><span class="sxs-lookup"><span data-stu-id="b47f4-104">To unregister a filter, implement the **DllUnregisterServer** function.</span></span> <span data-ttu-id="b47f4-105">在此函式中，呼叫具有值 **FALSE** 的 DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md)函式。</span><span class="sxs-lookup"><span data-stu-id="b47f4-105">Within this function, call the DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function with a value of **FALSE**.</span></span> <span data-ttu-id="b47f4-106">如果您在註冊篩選時呼叫 **IFilterMapper2：： RegisterFilter** ，請在這裡呼叫 [**IFilterMapper2：： UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) 方法。</span><span class="sxs-lookup"><span data-stu-id="b47f4-106">If you called **IFilterMapper2::RegisterFilter** when you registered the filter, call the [**IFilterMapper2::UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) method here.</span></span>

<span data-ttu-id="b47f4-107">下列範例示範如何取消註冊篩選：</span><span class="sxs-lookup"><span data-stu-id="b47f4-107">The following example shows how to unregister a filter:</span></span>


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



 

 



