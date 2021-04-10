---
description: 提供者可以從其方法執行中呼叫 WMI 所執行的方法。
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: 對 WMI 進行呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026793"
---
# <a name="making-calls-to-wmi"></a><span data-ttu-id="2c0f2-103">對 WMI 進行呼叫</span><span class="sxs-lookup"><span data-stu-id="2c0f2-103">Making Calls to WMI</span></span>

<span data-ttu-id="2c0f2-104">提供者可以從其方法執行中呼叫 WMI 所執行的方法。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-104">Providers can call methods implemented by WMI from within their method implementations.</span></span> <span data-ttu-id="2c0f2-105">不過，當提供者從其本身的相同方法的執行中呼叫 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 方法的 WMI 時，有一些特殊的考慮。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-105">However, there are special considerations when a provider calls the WMI implementation of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method from within its own implementation of the same method.</span></span> <span data-ttu-id="2c0f2-106">不論提供者是呼叫方法的同步或非同步版本，這些考慮都很重要。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-106">These considerations are important regardless of whether the provider calls the synchronous or asynchronous version of the method.</span></span>

<span data-ttu-id="2c0f2-107">提供者可以實作為的每個 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 方法都有 *pCtx* 參數，也就是 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 介面執行的指標。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-107">Each [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method that a provider can implement has a *pCtx* parameter, a pointer to an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface implementation.</span></span> <span data-ttu-id="2c0f2-108">當 WMI 呼叫提供者時，WMI 會在此參數中傳遞有效的指標。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-108">When WMI calls the provider, WMI passes a valid pointer in this parameter.</span></span> <span data-ttu-id="2c0f2-109">提供者在處理要求時，一律必須在對 WMI 進行的任何呼叫中傳遞此相同指標。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-109">A provider must always pass this same pointer in any calls to WMI that they make while servicing requests.</span></span> <span data-ttu-id="2c0f2-110">如果未正確地設定 *pCtx* ，可能會導致 WMI 啟動無限迴圈。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-110">Neglecting to set *pCtx* appropriately can cause WMI to start an infinite loop.</span></span>

<span data-ttu-id="2c0f2-111">下列程式碼範例顯示從 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)的執行中呼叫 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的 WMI 執行的正確方式。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-111">The following code example shows the correct way to call the WMI implementation of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) from within an implementation of [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



<span data-ttu-id="2c0f2-112">本主題中的 c + + 程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-112">The C++ code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="2c0f2-113">實例、類別和屬性提供者不得發出對 WMI 的任何呼叫，要求在服務讀取要求時修改資料。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-113">Instance, class, and property providers must not issue any calls to WMI requesting the modification of data while servicing a read request.</span></span> <span data-ttu-id="2c0f2-114">這項規則唯一的提供者是推播提供者。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-114">The only providers that are exceptions to this rule are push providers.</span></span> <span data-ttu-id="2c0f2-115">推播提供者是一種類別提供者，可將資料儲存在 WMI 儲存機制中，並依賴 WMI 來處理來自用戶端的要求。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-115">A push provider is a class provider that stores data in the WMI repository and relies on WMI to handle requests from clients.</span></span> <span data-ttu-id="2c0f2-116">當服務讀取要求時，推入提供者可以更新 WMI 儲存機制，但必須在適當的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)呼叫中將 *lFlags* 參數設定為 **WBEM 旗標擁有者 \_ \_ \_ 更新**。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-116">While servicing a read request, a push provider can update the WMI repository, but must set the *lFlags* parameter to **WBEM\_FLAG\_OWNER\_UPDATE** in the appropriate [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call.</span></span>

<span data-ttu-id="2c0f2-117">事件提供者不能在服務呼叫時進行任何類別變更。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-117">Event providers must not make any class changes while servicing a call.</span></span> <span data-ttu-id="2c0f2-118">它們也無法發出任何事件相關的呼叫，例如修改事件篩選。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-118">They also cannot issue any event-related calls, such as modifying an event filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c0f2-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c0f2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c0f2-120">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="2c0f2-120">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="2c0f2-121">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="2c0f2-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="2c0f2-122">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="2c0f2-122">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



