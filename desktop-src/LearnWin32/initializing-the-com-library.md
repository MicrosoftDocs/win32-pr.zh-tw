---
title: 初始化 COM 程式庫
description: 初始化 COM 程式庫
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968494"
---
# <a name="initializing-the-com-library"></a><span data-ttu-id="268a6-103">初始化 COM 程式庫</span><span class="sxs-lookup"><span data-stu-id="268a6-103">Initializing the COM Library</span></span>

<span data-ttu-id="268a6-104">任何使用 COM 的 Windows 程式都必須藉由呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 函數來初始化 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="268a6-104">Any Windows program that uses COM must initialize the COM library by calling the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span> <span data-ttu-id="268a6-105">使用 COM 介面的每個執行緒都必須對此函式進行個別呼叫。</span><span class="sxs-lookup"><span data-stu-id="268a6-105">Each thread that uses a COM interface must make a separate call to this function.</span></span> <span data-ttu-id="268a6-106">**CoInitializeEx** 具有下列簽章：</span><span class="sxs-lookup"><span data-stu-id="268a6-106">**CoInitializeEx** has the following signature:</span></span>


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



<span data-ttu-id="268a6-107">第一個參數是保留的，而且必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="268a6-107">The first parameter is reserved and must be **NULL**.</span></span> <span data-ttu-id="268a6-108">第二個參數指定您的程式將使用的執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="268a6-108">The second parameter specifies the threading model that your program will use.</span></span> <span data-ttu-id="268a6-109">COM 支援兩種不同的執行緒模型，也就是 *單元執行緒* 和 *多執行緒*。</span><span class="sxs-lookup"><span data-stu-id="268a6-109">COM supports two different threading models, *apartment threaded* and *multithreaded*.</span></span> <span data-ttu-id="268a6-110">如果您指定了單元執行緒，則會進行下列保證：</span><span class="sxs-lookup"><span data-stu-id="268a6-110">If you specify apartment threading, you are making the following guarantees:</span></span>

-   <span data-ttu-id="268a6-111">您將從單一執行緒存取每個 COM 物件;您不會在多個執行緒之間共用 COM 介面指標。</span><span class="sxs-lookup"><span data-stu-id="268a6-111">You will access each COM object from a single thread; you will not share COM interface pointers between multiple threads.</span></span>
-   <span data-ttu-id="268a6-112">執行緒將會有訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="268a6-112">The thread will have a message loop.</span></span> <span data-ttu-id="268a6-113"> (查看模組1中的 [視窗訊息](window-messages.md) 。 ) </span><span class="sxs-lookup"><span data-stu-id="268a6-113">(See [Window Messages](window-messages.md) in Module 1.)</span></span>

<span data-ttu-id="268a6-114">如果其中一個條件約束不是 true，請使用多執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="268a6-114">If either of these constraints is not true, use the multithreaded model.</span></span> <span data-ttu-id="268a6-115">若要指定執行緒模型，請在 *dwCoInit* 參數中設定下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="268a6-115">To specify the threading model, set one of the following flags in the *dwCoInit* parameter.</span></span>



| <span data-ttu-id="268a6-116">旗標</span><span class="sxs-lookup"><span data-stu-id="268a6-116">Flag</span></span>                          | <span data-ttu-id="268a6-117">描述</span><span class="sxs-lookup"><span data-stu-id="268a6-117">Description</span></span>         |
|-------------------------------|---------------------|
| <span data-ttu-id="268a6-118">**COINIT \_ APARTMENTTHREADED**</span><span class="sxs-lookup"><span data-stu-id="268a6-118">**COINIT\_APARTMENTTHREADED**</span></span> | <span data-ttu-id="268a6-119">單元執行緒。</span><span class="sxs-lookup"><span data-stu-id="268a6-119">Apartment threaded.</span></span> |
| <span data-ttu-id="268a6-120">**COINIT \_ 多執行緒**</span><span class="sxs-lookup"><span data-stu-id="268a6-120">**COINIT\_MULTITHREADED**</span></span>     | <span data-ttu-id="268a6-121">多執行緒。</span><span class="sxs-lookup"><span data-stu-id="268a6-121">Multithreaded.</span></span>      |



 

<span data-ttu-id="268a6-122">您必須只設定這些旗標的其中一個。</span><span class="sxs-lookup"><span data-stu-id="268a6-122">You must set exactly one of these flags.</span></span> <span data-ttu-id="268a6-123">一般來說，建立視窗的執行緒應該使用 **COINIT \_ APARTMENTTHREADED** 旗標，而其他執行緒則應該使用 **COINIT \_ 多執行緒**。</span><span class="sxs-lookup"><span data-stu-id="268a6-123">Generally, a thread that creates a window should use the **COINIT\_APARTMENTTHREADED** flag, and other threads should use **COINIT\_MULTITHREADED**.</span></span> <span data-ttu-id="268a6-124">不過，某些 COM 元件需要特定的執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="268a6-124">However, some COM components require a particular threading model.</span></span> <span data-ttu-id="268a6-125">MSDN 檔應該會在這種情況下告訴您。</span><span class="sxs-lookup"><span data-stu-id="268a6-125">The MSDN documentation should tell you when that is the case.</span></span>

> [!Note]  
> <span data-ttu-id="268a6-126">實際上，即使您指定了單元執行緒，還是可以使用稱為 *封送處理* 的技巧，線上程之間共用介面。</span><span class="sxs-lookup"><span data-stu-id="268a6-126">Actually, even if you specify apartment threading, it is still possible to share interfaces between threads, by using a technique called *marshaling*.</span></span> <span data-ttu-id="268a6-127">封送處理已超出此課程模組的範圍。</span><span class="sxs-lookup"><span data-stu-id="268a6-127">Marshaling is beyond the scope of this module.</span></span> <span data-ttu-id="268a6-128">重點是使用單元執行緒時，您絕不能只將介面指標複製到另一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="268a6-128">The important point is that with apartment threading, you must never simply copy an interface pointer to another thread.</span></span> <span data-ttu-id="268a6-129">如需 COM 執行緒模型的詳細資訊，請參閱 [進程、執行緒和單元](/windows/desktop/com/processes--threads--and-apartments)。</span><span class="sxs-lookup"><span data-stu-id="268a6-129">For more information about the COM threading models, see [Processes, Threads, and Apartments](/windows/desktop/com/processes--threads--and-apartments).</span></span>

 

<span data-ttu-id="268a6-130">除了已提及的旗標之外，最好在 *dwCoInit* 參數中設定 **COINIT \_ DISABLE \_ OLE1DDE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="268a6-130">In addition to the flags already mentioned, it is a good idea to set the **COINIT\_DISABLE\_OLE1DDE** flag in the *dwCoInit* parameter.</span></span> <span data-ttu-id="268a6-131">設定此旗標可避免 (OLE) 1.0 （淘汰的技術）與物件連結和內嵌相關聯的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="268a6-131">Setting this flag avoids some overhead associated with Object Linking and Embedding (OLE) 1.0, an obsolete technology.</span></span>

<span data-ttu-id="268a6-132">以下是您初始化 COM 以進行單元執行緒的方式：</span><span class="sxs-lookup"><span data-stu-id="268a6-132">Here is how you would initialize COM for apartment threading:</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



<span data-ttu-id="268a6-133">**HRESULT** 傳回型別包含錯誤或成功碼。</span><span class="sxs-lookup"><span data-stu-id="268a6-133">The **HRESULT** return type contains an error or success code.</span></span> <span data-ttu-id="268a6-134">在下一節中，我們將探討 COM 錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="268a6-134">We'll look at COM error handling in the next section.</span></span>

## <a name="uninitializing-the-com-library"></a><span data-ttu-id="268a6-135">將 COM 程式庫取消初始化</span><span class="sxs-lookup"><span data-stu-id="268a6-135">Uninitializing the COM Library</span></span>

<span data-ttu-id="268a6-136">針對每次成功呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)，您必須線上程結束之前呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) 。</span><span class="sxs-lookup"><span data-stu-id="268a6-136">For every successful call to [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), you must call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) before the thread exits.</span></span> <span data-ttu-id="268a6-137">此函數不接受任何參數，而且沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="268a6-137">This function takes no parameters and has no return value.</span></span>


```C++
CoUninitialize();
```



## <a name="next"></a><span data-ttu-id="268a6-138">下一個</span><span class="sxs-lookup"><span data-stu-id="268a6-138">Next</span></span>

[<span data-ttu-id="268a6-139">COM 中的錯誤碼</span><span class="sxs-lookup"><span data-stu-id="268a6-139">Error Codes in COM</span></span>](error-codes-in-com.md)

 

 