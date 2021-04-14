---
title: 建立全域介面資料表
description: 建立全域介面資料表
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383006"
---
# <a name="creating-the-global-interface-table"></a><span data-ttu-id="d12b8-103">建立全域介面資料表</span><span class="sxs-lookup"><span data-stu-id="d12b8-103">Creating the Global Interface Table</span></span>

<span data-ttu-id="d12b8-104">使用下列呼叫來建立全域介面資料表物件，並取得 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)的指標：</span><span class="sxs-lookup"><span data-stu-id="d12b8-104">Use the following call to create the global interface table object and get a pointer to [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span></span>

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> <span data-ttu-id="d12b8-105">使用上述呼叫來建立全域介面資料表物件時，必須連結至程式庫 uuid。</span><span class="sxs-lookup"><span data-stu-id="d12b8-105">When creating the global interface table object using the preceding call, it is necessary to link to the library uuid.lib.</span></span> <span data-ttu-id="d12b8-106">這將解析外部符號 CLSID \_ StdGlobalInterfaceTable 和 IID \_ IGlobalInterfaceTable。</span><span class="sxs-lookup"><span data-stu-id="d12b8-106">This will resolve the external symbols CLSID\_StdGlobalInterfaceTable and IID\_IGlobalInterfaceTable.</span></span>

 

<span data-ttu-id="d12b8-107">每個進程都有一個全域介面表的單一實例，因此在處理常式中對這個函式的所有呼叫都會傳回相同的實例。</span><span class="sxs-lookup"><span data-stu-id="d12b8-107">There is a single instance of the global interface table per process, so all calls to this function in a process return the same instance.</span></span>

<span data-ttu-id="d12b8-108">呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函式之後，請使用 [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) 方法的呼叫，從它所在的單元註冊介面。</span><span class="sxs-lookup"><span data-stu-id="d12b8-108">After the call to the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, register the interface from the apartment in which it resides with a call to the [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) method.</span></span> <span data-ttu-id="d12b8-109">這個方法會提供識別介面及其位置的 cookie。</span><span class="sxs-lookup"><span data-stu-id="d12b8-109">This method supplies a cookie that identifies the interface and its location.</span></span> <span data-ttu-id="d12b8-110">尋找這個介面指標的一個單元會使用此 cookie 來呼叫 [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) 方法，然後執行會提供指向呼叫的單元介面指標。</span><span class="sxs-lookup"><span data-stu-id="d12b8-110">An apartment seeking a pointer to this interface then calls the [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) method with this cookie, and the implementation then supplies an interface pointer to the calling apartment.</span></span> <span data-ttu-id="d12b8-111">若要撤銷介面的全域註冊，任何一個單元都可以呼叫 [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) 方法。</span><span class="sxs-lookup"><span data-stu-id="d12b8-111">To revoke the interface's global registration, any apartment can call the [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) method.</span></span>

<span data-ttu-id="d12b8-112">使用 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) 的簡單範例是當您想要在單一執行緒的單元中將介面指標傳遞 (STA) 至另一個單元中的背景工作執行緒時。</span><span class="sxs-lookup"><span data-stu-id="d12b8-112">A simple example of using [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) would be when you want to pass an interface pointer on an object in a single-threaded apartment (STA) to a worker thread in another apartment.</span></span> <span data-ttu-id="d12b8-113">**IGlobalInterfaceTable** 可讓您只傳遞 cookie，而不需要將它封送處理為數據流，並將資料流程以執行緒參數形式傳遞給背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="d12b8-113">Rather than having to marshal it into a stream and pass the stream to the worker thread as a thread parameter, **IGlobalInterfaceTable** allows you simply to pass a cookie.</span></span>

<span data-ttu-id="d12b8-114">當您在全域介面資料表中註冊介面時，您會取得可用的 cookie，而不是在每次需要將指標傳遞至另一個單元 (的 nonmethod 參數，而不是傳遞真正的 (指標) ，也就是要傳遞至另一個單元的 [*參數，以透過*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) 或可在您的部門以外存取的同進程記憶體。</span><span class="sxs-lookup"><span data-stu-id="d12b8-114">When you register the interface in the global interface table, you get a cookie that you can use instead of passing the actual pointer (whenever you need to pass the pointer), either to a nonmethod parameter that is going to another apartment (as a parameter to [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) through [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) or to in-process memory accessible outside your apartment.</span></span>

<span data-ttu-id="d12b8-115">需要注意的原因是，使用全域介面會讓程式設計人員管理問題（例如競爭條件和相互排除）產生額外的負擔，這些問題與從多個執行緒同時存取全域狀態相關聯。</span><span class="sxs-lookup"><span data-stu-id="d12b8-115">Care is required because using global interfaces places the extra burden on the programmer of managing problems such as race conditions and mutual exclusion, which are associated with accessing global state from multiple threads simultaneously.</span></span>

<span data-ttu-id="d12b8-116">COM 提供 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) 介面的標準實作為。</span><span class="sxs-lookup"><span data-stu-id="d12b8-116">COM provides a standard implementation of the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="d12b8-117">強烈建議您使用這個標準實作為，因為它提供完整的執行緒安全功能。</span><span class="sxs-lookup"><span data-stu-id="d12b8-117">It is highly recommended that you use this standard implementation because it provides complete thread-safe functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d12b8-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="d12b8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d12b8-119">使用全域介面資料表的時機</span><span class="sxs-lookup"><span data-stu-id="d12b8-119">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 