---
title: 管理物件的存留期
description: 瞭解如何管理 AddRef 和發行方法，以控制物件的存留期。
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104566507"
---
# <a name="managing-the-lifetime-of-an-object"></a><span data-ttu-id="6845e-103">管理物件的存留期</span><span class="sxs-lookup"><span data-stu-id="6845e-103">Managing the Lifetime of an Object</span></span>

<span data-ttu-id="6845e-104">我們尚未提及的 COM 介面有一個規則。</span><span class="sxs-lookup"><span data-stu-id="6845e-104">There is a rule for COM interfaces that we have not yet mentioned.</span></span> <span data-ttu-id="6845e-105">每個 COM 介面都必須直接或間接繼承自名為 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)的介面。</span><span class="sxs-lookup"><span data-stu-id="6845e-105">Every COM interface must inherit, directly or indirectly, from an interface named [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="6845e-106">這個介面會提供所有 COM 物件都必須支援的一些基本功能。</span><span class="sxs-lookup"><span data-stu-id="6845e-106">This interface provides some baseline capabilities that all COM objects must support.</span></span>

<span data-ttu-id="6845e-107">[**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面會定義三個方法：</span><span class="sxs-lookup"><span data-stu-id="6845e-107">The [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface defines three methods:</span></span>

-   <span data-ttu-id="6845e-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="6845e-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
-   [<span data-ttu-id="6845e-109">**AddRef**</span><span class="sxs-lookup"><span data-stu-id="6845e-109">**AddRef**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [<span data-ttu-id="6845e-110">**版本**</span><span class="sxs-lookup"><span data-stu-id="6845e-110">**Release**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

<span data-ttu-id="6845e-111">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法可讓程式在執行時間查詢物件的功能。</span><span class="sxs-lookup"><span data-stu-id="6845e-111">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method enables a program to query the capabilities of the object at run time.</span></span> <span data-ttu-id="6845e-112">在下一個主題中，我們將詳細說明如何 [針對介面提出物件](asking-an-object-for-an-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="6845e-112">We'll say more about that in the next topic, [Asking an Object for an Interface](asking-an-object-for-an-interface.md).</span></span> <span data-ttu-id="6845e-113">[**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)方法是用來控制物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="6845e-113">The [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are used to control the lifetime of an object.</span></span> <span data-ttu-id="6845e-114">這是本主題的主題。</span><span class="sxs-lookup"><span data-stu-id="6845e-114">This is the subject of this topic.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="6845e-115">參考計數</span><span class="sxs-lookup"><span data-stu-id="6845e-115">Reference Counting</span></span>

<span data-ttu-id="6845e-116">程式可能會做的任何事，在某個時間點會配置和釋出資源。</span><span class="sxs-lookup"><span data-stu-id="6845e-116">Whatever else a program might do, at some point it will allocate and free resources.</span></span> <span data-ttu-id="6845e-117">配置資源很簡單。</span><span class="sxs-lookup"><span data-stu-id="6845e-117">Allocating a resource is easy.</span></span> <span data-ttu-id="6845e-118">知道何時釋出資源很困難，特別是當資源的存留期超出目前範圍時。</span><span class="sxs-lookup"><span data-stu-id="6845e-118">Knowing when to free the resource is hard, especially if the lifetime of the resource extends beyond the current scope.</span></span> <span data-ttu-id="6845e-119">這個問題對 COM 而言並不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="6845e-119">This problem is not unique to COM.</span></span> <span data-ttu-id="6845e-120">配置堆積記憶體的任何程式都必須解決相同的問題。</span><span class="sxs-lookup"><span data-stu-id="6845e-120">Any program that allocates heap memory must solve the same problem.</span></span> <span data-ttu-id="6845e-121">例如，c + + 會使用自動析構函數，而 c # 和 JAVA 則使用垃圾收集。</span><span class="sxs-lookup"><span data-stu-id="6845e-121">For example, C++ uses automatic destructors, while C# and Java use garbage collection.</span></span> <span data-ttu-id="6845e-122">COM 使用稱為 *參考計數* 的方法。</span><span class="sxs-lookup"><span data-stu-id="6845e-122">COM uses an approach called *reference counting*.</span></span>

<span data-ttu-id="6845e-123">每個 COM 物件都會維護內部計數。</span><span class="sxs-lookup"><span data-stu-id="6845e-123">Every COM object maintains an internal count.</span></span> <span data-ttu-id="6845e-124">這就是所謂的參考計數。</span><span class="sxs-lookup"><span data-stu-id="6845e-124">This is known as the reference count.</span></span> <span data-ttu-id="6845e-125">參考計數會追蹤目前作用中物件的參考數目。</span><span class="sxs-lookup"><span data-stu-id="6845e-125">The reference count tracks how many references to the object are currently active.</span></span> <span data-ttu-id="6845e-126">當參考的數目降至零時，物件就會刪除本身。</span><span class="sxs-lookup"><span data-stu-id="6845e-126">When the number of references drops to zero, the object deletes itself.</span></span> <span data-ttu-id="6845e-127">最後一個部分值得重複：物件會刪除本身。</span><span class="sxs-lookup"><span data-stu-id="6845e-127">The last part is worth repeating: The object deletes itself.</span></span> <span data-ttu-id="6845e-128">程式永遠不會明確刪除物件。</span><span class="sxs-lookup"><span data-stu-id="6845e-128">The program never explicitly deletes the object.</span></span>

<span data-ttu-id="6845e-129">以下是參考計數的規則：</span><span class="sxs-lookup"><span data-stu-id="6845e-129">Here are the rules for reference counting:</span></span>

-   <span data-ttu-id="6845e-130">第一次建立物件時，它的參考計數為1。</span><span class="sxs-lookup"><span data-stu-id="6845e-130">When the object is first created, its reference count is 1.</span></span> <span data-ttu-id="6845e-131">此時，程式具有物件的單一指標。</span><span class="sxs-lookup"><span data-stu-id="6845e-131">At this point, the program has a single pointer to the object.</span></span>
-   <span data-ttu-id="6845e-132">程式可以複製 (複製) 指標來建立新的參考。</span><span class="sxs-lookup"><span data-stu-id="6845e-132">The program can create a new reference by duplicating (copying) the pointer.</span></span> <span data-ttu-id="6845e-133">當您複製指標時，您必須呼叫物件的 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 方法。</span><span class="sxs-lookup"><span data-stu-id="6845e-133">When you copy the pointer, you must call the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method of the object.</span></span> <span data-ttu-id="6845e-134">這個方法會將參考計數遞增一。</span><span class="sxs-lookup"><span data-stu-id="6845e-134">This method increments the reference count by one.</span></span>
-   <span data-ttu-id="6845e-135">當您完成使用物件的指標時，您必須呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)。</span><span class="sxs-lookup"><span data-stu-id="6845e-135">When you are finished using a pointer to the object, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="6845e-136">**發行** 方法會將參考計數遞減一。</span><span class="sxs-lookup"><span data-stu-id="6845e-136">The **Release** method decrements the reference count by one.</span></span> <span data-ttu-id="6845e-137">它也會使指標失效。</span><span class="sxs-lookup"><span data-stu-id="6845e-137">It also invalidates the pointer.</span></span> <span data-ttu-id="6845e-138">呼叫 **Release** 之後，請不要再使用指標。</span><span class="sxs-lookup"><span data-stu-id="6845e-138">Do not use the pointer again after you call **Release**.</span></span> <span data-ttu-id="6845e-139"> (如果您有相同物件的其他指標，您可以繼續使用這些指標。 ) </span><span class="sxs-lookup"><span data-stu-id="6845e-139">(If you have other pointers to the same object, you can continue to use those pointers.)</span></span>
-   <span data-ttu-id="6845e-140">當您使用每個指標呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 時，物件的物件參考計數會到達零，而物件會刪除本身。</span><span class="sxs-lookup"><span data-stu-id="6845e-140">When you have called [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with every pointer, the object reference count of the object reaches zero, and the object deletes itself.</span></span>

<span data-ttu-id="6845e-141">下圖顯示簡單但一般的案例。</span><span class="sxs-lookup"><span data-stu-id="6845e-141">The following diagram shows a simple but typical case.</span></span>

![顯示簡單參考計數案例的圖表。](images/com04.png)

<span data-ttu-id="6845e-143">此程式會建立物件，並將指標 (*p*) 儲存至物件。</span><span class="sxs-lookup"><span data-stu-id="6845e-143">The program creates an object and stores a pointer (*p*) to the object.</span></span> <span data-ttu-id="6845e-144">此時，參考計數為1。</span><span class="sxs-lookup"><span data-stu-id="6845e-144">At this point, the reference count is 1.</span></span> <span data-ttu-id="6845e-145">當程式完成使用指標時，它會呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)。</span><span class="sxs-lookup"><span data-stu-id="6845e-145">When the program is finished using the pointer, it calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="6845e-146">參考計數會減少為零，而物件會刪除本身。</span><span class="sxs-lookup"><span data-stu-id="6845e-146">The reference count is decremented to zero, and the object deletes itself.</span></span> <span data-ttu-id="6845e-147">現在 *p* 是不正確。</span><span class="sxs-lookup"><span data-stu-id="6845e-147">Now *p* is invalid.</span></span> <span data-ttu-id="6845e-148">將 *p* 用於任何進一步的方法呼叫時，會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="6845e-148">It is an error to use *p* for any further method calls.</span></span>

<span data-ttu-id="6845e-149">下圖顯示更複雜的範例。</span><span class="sxs-lookup"><span data-stu-id="6845e-149">The next diagram shows a more complex example.</span></span>

![顯示參考計數的圖例](images/com05.png)

<span data-ttu-id="6845e-151">在這裡，程式會建立物件，並將指標 *p* 儲存在前面。</span><span class="sxs-lookup"><span data-stu-id="6845e-151">Here, the program creates an object and stores the pointer *p*, as before.</span></span> <span data-ttu-id="6845e-152">接下來，程式會將 *p* 複製到新的變數 *q*。</span><span class="sxs-lookup"><span data-stu-id="6845e-152">Next, the program copies *p* to a new variable, *q*.</span></span> <span data-ttu-id="6845e-153">此時，程式必須呼叫 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 來遞增參考計數。</span><span class="sxs-lookup"><span data-stu-id="6845e-153">At this point, the program must call [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) to increment the reference count.</span></span> <span data-ttu-id="6845e-154">參考計數現在是2，而物件有兩個有效的指標。</span><span class="sxs-lookup"><span data-stu-id="6845e-154">The reference count is now 2, and there are two valid pointers to the object.</span></span> <span data-ttu-id="6845e-155">現在假設程式已使用 *p* 完成。</span><span class="sxs-lookup"><span data-stu-id="6845e-155">Now suppose that the program is finished using *p*.</span></span> <span data-ttu-id="6845e-156">此程式會呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)，參考計數會變成1，而 *p* 不再有效。</span><span class="sxs-lookup"><span data-stu-id="6845e-156">The program calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), the reference count goes to 1, and *p* is no longer valid.</span></span> <span data-ttu-id="6845e-157">但 *q* 仍有效。</span><span class="sxs-lookup"><span data-stu-id="6845e-157">However, *q* is still valid.</span></span> <span data-ttu-id="6845e-158">之後，程式就會使用 *q* 完成。</span><span class="sxs-lookup"><span data-stu-id="6845e-158">Later, the program finishes using *q*.</span></span> <span data-ttu-id="6845e-159">因此，它會再次呼叫 **發行** 。</span><span class="sxs-lookup"><span data-stu-id="6845e-159">Therefore, it calls **Release** again.</span></span> <span data-ttu-id="6845e-160">參考計數會變成零，而物件會刪除本身。</span><span class="sxs-lookup"><span data-stu-id="6845e-160">The reference count goes to zero, and the object deletes itself.</span></span>

<span data-ttu-id="6845e-161">您可能會想知道程式會複製 *p* 的原因。</span><span class="sxs-lookup"><span data-stu-id="6845e-161">You might wonder why the program would copy *p*.</span></span> <span data-ttu-id="6845e-162">有兩個主要的原因：首先，您可能會想要將指標儲存在資料結構中，例如清單。</span><span class="sxs-lookup"><span data-stu-id="6845e-162">There are two main reasons: First, you might want to store the pointer in a data structure, such as a list.</span></span> <span data-ttu-id="6845e-163">其次，您可能會想要將指標保持在原始變數的目前範圍之外。</span><span class="sxs-lookup"><span data-stu-id="6845e-163">Second, you might want to keep the pointer beyond the current scope of the original variable.</span></span> <span data-ttu-id="6845e-164">因此，您可以將它複製到範圍較廣的新變數。</span><span class="sxs-lookup"><span data-stu-id="6845e-164">Therefore, you would copy it to a new variable with wider scope.</span></span>

<span data-ttu-id="6845e-165">參考計數的其中一個優點是您可以在不同的程式碼區段之間共用指標，而不需要針對不同的程式碼路徑進行協調來刪除物件。</span><span class="sxs-lookup"><span data-stu-id="6845e-165">One advantage of reference counting is that you can share pointers across different sections of code, without the various code paths coordinating to delete the object.</span></span> <span data-ttu-id="6845e-166">相反地，每個程式碼路徑只會在該程式碼路徑使用物件完成時，呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="6845e-166">Instead, each code path merely calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when that code path is done using the object.</span></span> <span data-ttu-id="6845e-167">物件會在正確的時間處理本身的刪除。</span><span class="sxs-lookup"><span data-stu-id="6845e-167">The object handles deleting itself at the correct time.</span></span>

## <a name="example"></a><span data-ttu-id="6845e-168">範例</span><span class="sxs-lookup"><span data-stu-id="6845e-168">Example</span></span>

<span data-ttu-id="6845e-169">以下是再次 [開啟對話方塊範例](example--the-open-dialog-box.md) 中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="6845e-169">Here is the code from the [Open dialog box example](example--the-open-dialog-box.md) again.</span></span>

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

<span data-ttu-id="6845e-170">參考計數會在此程式碼的兩個位置進行。</span><span class="sxs-lookup"><span data-stu-id="6845e-170">Reference counting occurs in two places in this code.</span></span> <span data-ttu-id="6845e-171">首先，如果程式成功建立一般專案對話方塊物件，它必須在 *pFileOpen* 指標上呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="6845e-171">First, if program successfully creates the Common Item Dialog object, it must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pFileOpen* pointer.</span></span>

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

<span data-ttu-id="6845e-172">其次，當 [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)方法傳回 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)介面的指標時，程式必須在 *pItem* 指標上呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="6845e-172">Second, when the [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method returns a pointer to the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, the program must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pItem* pointer.</span></span>

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

<span data-ttu-id="6845e-173">請注意，在這兩種情況下， [**釋放**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 呼叫是指標超出範圍之前所發生的最後一件事。</span><span class="sxs-lookup"><span data-stu-id="6845e-173">Notice that in both cases, the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call is the last thing that happens before the pointer goes out of scope.</span></span> <span data-ttu-id="6845e-174">另外也請注意，只有在您測試 **HRESULT** 是否成功之後，才會呼叫此 **版本**。</span><span class="sxs-lookup"><span data-stu-id="6845e-174">Also notice that **Release** is called only after you test the **HRESULT** for success.</span></span> <span data-ttu-id="6845e-175">例如，如果對 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 的呼叫失敗， *pFileOpen* 指標就會無效。</span><span class="sxs-lookup"><span data-stu-id="6845e-175">For example, if the call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails, the *pFileOpen* pointer is not valid.</span></span> <span data-ttu-id="6845e-176">因此，在指標上呼叫 **Release** 會是錯誤。</span><span class="sxs-lookup"><span data-stu-id="6845e-176">Therefore, it would be an error to call **Release** on the pointer.</span></span>

## <a name="next"></a><span data-ttu-id="6845e-177">下一個</span><span class="sxs-lookup"><span data-stu-id="6845e-177">Next</span></span>

[<span data-ttu-id="6845e-178">要求物件提供介面</span><span class="sxs-lookup"><span data-stu-id="6845e-178">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)