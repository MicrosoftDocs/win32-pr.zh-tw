---
title: 從您的延伸模組取得 ADSI 介面
description: 延伸模組通常需要從它所系結的目錄物件取得資料。
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- 擴充功能 ADSI，從您的延伸模組取得 ADSI 介面
- ADSI ADSI，範例程式碼 C/c + +，從您的延伸模組取得 ADSI 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eeff55f2e382ce2816f59ee53dbd78033b79c
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106984945"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a><span data-ttu-id="dcf3f-105">從您的延伸模組取得 ADSI 介面</span><span class="sxs-lookup"><span data-stu-id="dcf3f-105">Getting ADSI Interfaces From Your Extension</span></span>

<span data-ttu-id="dcf3f-106">延伸模組通常需要從它所系結的目錄物件取得資料。</span><span class="sxs-lookup"><span data-stu-id="dcf3f-106">An extension often needs to get data from the directory object it binds to.</span></span> <span data-ttu-id="dcf3f-107">例如， **電腦** 物件的延伸模組可能會想要從目錄取得目前物件的 **dnsHostName** 。</span><span class="sxs-lookup"><span data-stu-id="dcf3f-107">For example, an extension for a **computer** object may want to get the **dnsHostName** of the current object from the directory.</span></span> <span data-ttu-id="dcf3f-108">您可以在匯總工具的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面上發出 **QueryInterface** 呼叫，輕鬆達成這個目的。</span><span class="sxs-lookup"><span data-stu-id="dcf3f-108">This can be easily achieved by issuing a **QueryInterface** call on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the aggregator.</span></span>


```C++
HRESULT hr;
IADs *pADs; ' ADSI Interface to get/set attributes.
 
hr = m_pOuterUnk->QueryInterface(IID_IADs,(void**)&pADs);
 
if ( SUCCEEDED(hr) )
{
    VARIANT var;
    VariantInit(&var);
    hr  = pADs ->Get(_bstr_t("dnsHostName"), &var);
    if ( SUCCEEDED(hr) )
    { 
        printf("%S\n", V_BSTR(&var));
    }
    VariantClear(&var);
    pADs->Release();
}
```



<span data-ttu-id="dcf3f-109">您應該在使用介面之後立即加以釋放。</span><span class="sxs-lookup"><span data-stu-id="dcf3f-109">You should release the interface immediately after using it.</span></span> <span data-ttu-id="dcf3f-110">如果延伸模組具有匯總工具的開啟參考，則您已建立迴圈參考，且匯總工具無法釋放延伸模組。</span><span class="sxs-lookup"><span data-stu-id="dcf3f-110">If the extension has an open reference to the aggregator, you have created a circular reference and the aggregator cannot release the extension.</span></span> <span data-ttu-id="dcf3f-111">因此，無法釋放匯總工具，且結果會在您的應用程式中造成記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="dcf3f-111">Therefore, the aggregator cannot be released and the result is memory leaks in your application.</span></span>

 

 