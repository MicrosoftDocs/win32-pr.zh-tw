---
description: 在 c + + 中，傳回值的類型通常是 HRESULT。
ms.assetid: 7abf1b3e-b94b-4846-a813-5eab5b34324c
title: C + + 中的傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7a5417019468945054f24701636fcece1d3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192739"
---
# <a name="return-values-in-c"></a><span data-ttu-id="2e5c3-103">C + + 中的傳回值</span><span class="sxs-lookup"><span data-stu-id="2e5c3-103">Return Values in C++</span></span>

<span data-ttu-id="2e5c3-104">在 c + + 中，傳回值的類型通常是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="2e5c3-104">In C++, the return value is typically of type **HRESULT**.</span></span> <span data-ttu-id="2e5c3-105">這是來自此傳回值，可以判斷方法是否成功，如果不是，則錯誤是什麼。</span><span class="sxs-lookup"><span data-stu-id="2e5c3-105">It is from this return value that it can be determined whether the method succeeded or not, and if not, what the error was.</span></span> <span data-ttu-id="2e5c3-106">\_當方法成功完成時，憑證服務通常會傳回 **HRESULT** 的「確定」。</span><span class="sxs-lookup"><span data-stu-id="2e5c3-106">Certificate Services typically returns S\_OK for the **HRESULT** when the method has completed successfully.</span></span> <span data-ttu-id="2e5c3-107">需要傳回的程式設計值會透過方法中的 "out" 參數傳回。</span><span class="sxs-lookup"><span data-stu-id="2e5c3-107">Programmatic values that need to be returned are returned through "out" parameters in the method.</span></span> <span data-ttu-id="2e5c3-108">下列範例顯示 c + + 方法呼叫，以抓取要求屬性：</span><span class="sxs-lookup"><span data-stu-id="2e5c3-108">The following example shows a C++ method call to retrieve a request property:</span></span>


```C++
BSTR      bstrPropName = NULL;
VARIANT   varProp;
HRESULT   hr;

VariantInit(&varProp);

bstrPropName = SysAllocString(L"RequestID");
if (NULL == bstrPropName)
{
    printf("Failed SysAllocString\n");
    // Take application-specific error action.
    exit(1);
}

// Retrieve the request property.
// pCertServerPolicy is a pointer to a previously
// instantiated ICertServerPolicy object.
hr = pCertServerPolicy->GetRequestProperty(bstrPropName,
                                           PROPTYPE_LONG,
                                           &varProp);
if (S_OK != hr)
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    // Take application-specific error action.
    // ...
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear(&varProp);
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
```



<span data-ttu-id="2e5c3-109">在上述的程式碼片段中，成功或失敗會傳回給 **HRESULT** 變數 *hr*。</span><span class="sxs-lookup"><span data-stu-id="2e5c3-109">In the preceding code fragment, success or failure is returned to the **HRESULT** variable, *hr*.</span></span> <span data-ttu-id="2e5c3-110">在程式碼中檢查 **HRESULT** 變數是否成功， \[ 條件 (S \_ OK！ = hr) \] 。</span><span class="sxs-lookup"><span data-stu-id="2e5c3-110">It is imperative to check the **HRESULT** variable for success \[handled in the code by the condition (S\_OK != hr)\].</span></span> <span data-ttu-id="2e5c3-111">如果方法順利完成，就會在 **VARIANT** *varProp* 參數中傳回 request 屬性值。</span><span class="sxs-lookup"><span data-stu-id="2e5c3-111">If the method completed successfully, the request property value is returned in the **VARIANT** *varProp* parameter.</span></span>

 

 



