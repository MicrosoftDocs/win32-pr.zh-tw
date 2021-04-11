---
description: 託管元件的回呼是讓裝載成為可能的。 不過，您所裝載的元件可能已啟用另一個用來存取本身外掛程式或元件的啟用內容。
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: 使用託管元件的回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef302601985bc7e56a296bc8f494e48e18d785e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112697"
---
# <a name="using-callbacks-from-hosted-components"></a><span data-ttu-id="7aa95-104">使用託管元件的回呼</span><span class="sxs-lookup"><span data-stu-id="7aa95-104">Using Callbacks From Hosted Components</span></span>

<span data-ttu-id="7aa95-105">託管元件的回呼是讓裝載成為可能的。</span><span class="sxs-lookup"><span data-stu-id="7aa95-105">Callbacks from hosted components are what make hosting possible.</span></span> <span data-ttu-id="7aa95-106">不過，您所裝載的元件可能已啟用另一個用來存取本身外掛程式或元件的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="7aa95-106">However, it is possible that the component you are hosting has activated another activation context that it uses to access plug-ins or components of its own.</span></span> <span data-ttu-id="7aa95-107">在此情況下，如果裝載的元件在參考其本身 COM 物件的堆疊上保留啟用內容，則裝載應用程式可能會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來取得它所預期的物件，而改為接收主控元件的物件。</span><span class="sxs-lookup"><span data-stu-id="7aa95-107">In this case, if the hosted component leaves an activation context on the stack that refers to its own COM object, the hosting application might call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get an object that it expects to be its own implementation and instead receive the hosted component's object.</span></span> <span data-ttu-id="7aa95-108">為了避免這項啟用內容繼承，良好的裝載應用程式應該在回呼期間先啟用自己的知名啟用內容。</span><span class="sxs-lookup"><span data-stu-id="7aa95-108">To prevent this inheritance of activation contexts, a good hosting applications should activate its own well-known activation context first during a callback.</span></span>

<span data-ttu-id="7aa95-109">請考慮下列保護主控應用程式程式碼的範例：</span><span class="sxs-lookup"><span data-stu-id="7aa95-109">Consider the following example that protects the hosting application's code:</span></span>

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

<span data-ttu-id="7aa95-110">這可確保在將要求傳遞至 **Funct** 的內部實執行之前，會先設定適當的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="7aa95-110">This ensures that a proper activation context is set before passing the request on to some inner implementation of **Funct**.</span></span> <span data-ttu-id="7aa95-111">您自己的實電腦可以內嵌實際的實值，但先前的方法可透過建立委派的包裝函式，來確保互通性更容易。</span><span class="sxs-lookup"><span data-stu-id="7aa95-111">Your own implementation can have the actual implementation inline, but the preceding method ensures easier interoperability by just creating delegated wrappers.</span></span> <span data-ttu-id="7aa95-112">當公開一般 (非 COM) 回呼時，建議使用類似的方法。</span><span class="sxs-lookup"><span data-stu-id="7aa95-112">It is recommended to use a similar method when exposing normal (non-COM) callbacks.</span></span>

 

 
