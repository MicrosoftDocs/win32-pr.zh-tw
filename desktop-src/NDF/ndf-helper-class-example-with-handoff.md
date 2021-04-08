---
title: 具有遞交的 NDF Helper 類別延伸
description: 此協助程式類別對於第一個範例中所編碼的 SimpleFileHelperClass 具有低健康情況的相依性。
ms.assetid: b59cd855-c68a-4f5c-b145-ceac395ddcc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b799b795fcf23cbddf268056e23db433566c8a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932206"
---
# <a name="ndf-helper-class-extension-with-handoff"></a><span data-ttu-id="10aab-103">具有遞交的 NDF Helper 類別延伸</span><span class="sxs-lookup"><span data-stu-id="10aab-103">NDF Helper Class Extension with Handoff</span></span>

<span data-ttu-id="10aab-104">此協助程式類別對於第一個範例中所編碼的 SimpleFileHelperClass 具有低健康情況的相依性。</span><span class="sxs-lookup"><span data-stu-id="10aab-104">This Helper Class has a low-health dependency on the SimpleFileHelperClass coded in the first example.</span></span>

<span data-ttu-id="10aab-105">第二個遞交 helper 類別是簡單的傳遞 helper 類別，不會執行任何診斷本身。</span><span class="sxs-lookup"><span data-stu-id="10aab-105">The second handoff helper class is a simple pass-through helper class which does not perform any diagnosis itself.</span></span> <span data-ttu-id="10aab-106">相反地，它一律會為 SimpleFileHelperClass 產生較低的健康情況假設。</span><span class="sxs-lookup"><span data-stu-id="10aab-106">Instead, it always generates lower health hypothesis for the SimpleFileHelperClass.</span></span> <span data-ttu-id="10aab-107">這在作為預留位置，以供未來在此協助程式類別中新增診斷功能時，是很有用的。</span><span class="sxs-lookup"><span data-stu-id="10aab-107">This is useful in serving as a placeholder for future addition of diagnostics capability in this helper class.</span></span> <span data-ttu-id="10aab-108">「遞交協助程式」類別會執行兩個方法。</span><span class="sxs-lookup"><span data-stu-id="10aab-108">The handoff helper class implements two methods.</span></span>

<span data-ttu-id="10aab-109">LowHealth 方法是用來將診斷狀態設定為 DS \_ 不定。</span><span class="sxs-lookup"><span data-stu-id="10aab-109">The LowHealth method is used to set the Diagnosis Status to DS\_INDETERMINATE.</span></span> <span data-ttu-id="10aab-110">這會讓 NDF 呼叫 GetLowerHypotheses。</span><span class="sxs-lookup"><span data-stu-id="10aab-110">This makes NDF call GetLowerHypotheses.</span></span>


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::LowHealth( 
    /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
    /* [string][out] */ LPWSTR *ppwszDescription,
    /* [out] */ long *pDeferredTime,
    /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    *pStatus = DS_INDETERMINATE;
    return S_OK;
}

```



<span data-ttu-id="10aab-111">接下來，會執行 GetLowerHypotheses，告訴 NDF 要診斷哪一個 Helper 類別。</span><span class="sxs-lookup"><span data-stu-id="10aab-111">Next, GetLowerHypotheses is implemented to tell NDF which Helper Class to diagnose.</span></span>


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::GetLowerHypotheses( 
ULONG *Count,
HYPOTHESIS **Hypotheses)
{
    HRESULT hr = S_OK;
    HYPOTHESIS *pHypothesis=NULL;
    HELPER_ATTRIBUTE *pAttr=NULL;

    pHypothesis = (PHYPOTHESIS)CoTaskMemAlloc(sizeof(HYPOTHESIS));
    if (pHypothesis == NULL)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pHypothesis, sizeof(HYPOTHESIS));

    pAttr = (PHELPER_ATTRIBUTE)CoTaskMemAlloc(sizeof(HELPER_ATTRIBUTE));
    if (pAttr  == NULL)
    {
       hr = E_OUTOFMEMORY;
       goto Error;
    }
    SecureZeroMemory(pAttr, sizeof(HELPER_ATTRIBUTE));

    //set the helper class name to hand off to
    hr = StringCchCopyWithAlloc(&pHypothesis->pwszClassName, MAX_PATH,
                 L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    //populate the attribute
    //set the attribute name
    hr = StringCchCopyWithAlloc(&pAttr->pwszName, MAX_PATH, L"filename");
    if (FAILED(hr))
    {
        goto Error;  
    }

    //set attribute data
    pAttr->type = AT_STRING;
    hr = StringCchCopyWithAlloc(&pAttr->PWStr, MAX_PATH, m_pwszTestFile);
    if (FAILED(hr))
    {
        goto Error;
    }

    //set the attributes to the hypothesis  
    pHypothesis->celt = 1; //number of attributes
    pHypothesis->rgAttributes=pAttr;

    //pass data back
    *pcelt = 1; //one hypothesis
    *pprgHypotheses = pHypothesis;

    return S_OK;

Error:

    if (pAttr)
    {
        if (pAttr->PWStr) 
            CoTaskMemFree(pAttr->PWStr);
        if (pAttr->pwszName) 
            CoTaskMemFree(pAttr->pwszName);
    }

    if (pHypothesis)
    {
        if (pHypothesis->pwszClassName) 
            CoTaskMemFree(pHypothesis->pwszClassName);
        CoTaskMemFree(pHypothesis);
    }
    return hr;
}

```



 

 




