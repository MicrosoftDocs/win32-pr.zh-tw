---
title: 使用 Win32 和 c + +) 開始 COM (中的錯誤處理
description: 使用 Win32 和 c + +) 開始 COM (中的錯誤處理
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cf89170087469fa6ef8587fb5377e6374f6a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103916"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a><span data-ttu-id="d0bf0-103">使用 Win32 和 c + +) 開始 COM (中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="d0bf0-103">Error Handling in COM (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="d0bf0-104">COM 會使用 **HRESULT** 值來指出方法或函式呼叫的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-104">COM uses **HRESULT** values to indicate the success or failure of a method or function call.</span></span> <span data-ttu-id="d0bf0-105">各種 SDK 標頭會定義各種 **HRESULT** 常數。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-105">Various SDK headers define various **HRESULT** constants.</span></span> <span data-ttu-id="d0bf0-106">Winerror.h 中會定義一組通用的全系統程式碼。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-106">A common set of system-wide codes is defined in WinError.h.</span></span> <span data-ttu-id="d0bf0-107">下表顯示其中一些全系統的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-107">The following table shows some of those system-wide return codes.</span></span>



| <span data-ttu-id="d0bf0-108">常數</span><span class="sxs-lookup"><span data-stu-id="d0bf0-108">Constant</span></span>            | <span data-ttu-id="d0bf0-109">數值</span><span class="sxs-lookup"><span data-stu-id="d0bf0-109">Numeric value</span></span> | <span data-ttu-id="d0bf0-110">Description</span><span class="sxs-lookup"><span data-stu-id="d0bf0-110">Description</span></span>                                          |
|---------------------|---------------|------------------------------------------------------|
| <span data-ttu-id="d0bf0-111">**E \_ ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-111">**E\_ACCESSDENIED**</span></span> | <span data-ttu-id="d0bf0-112">0x80070005</span><span class="sxs-lookup"><span data-stu-id="d0bf0-112">0x80070005</span></span>    | <span data-ttu-id="d0bf0-113">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-113">Access denied.</span></span>                                       |
| <span data-ttu-id="d0bf0-114">**E \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-114">**E\_FAIL**</span></span>         | <span data-ttu-id="d0bf0-115">0x80004005</span><span class="sxs-lookup"><span data-stu-id="d0bf0-115">0x80004005</span></span>    | <span data-ttu-id="d0bf0-116">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-116">Unspecified error.</span></span>                                   |
| <span data-ttu-id="d0bf0-117">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-117">**E\_INVALIDARG**</span></span>   | <span data-ttu-id="d0bf0-118">0x80070057</span><span class="sxs-lookup"><span data-stu-id="d0bf0-118">0x80070057</span></span>    | <span data-ttu-id="d0bf0-119">參數值無效。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-119">Invalid parameter value.</span></span>                             |
| <span data-ttu-id="d0bf0-120">**E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-120">**E\_OUTOFMEMORY**</span></span>  | <span data-ttu-id="d0bf0-121">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="d0bf0-121">0x8007000E</span></span>    | <span data-ttu-id="d0bf0-122">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-122">Out of memory.</span></span>                                       |
| <span data-ttu-id="d0bf0-123">**E \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-123">**E\_POINTER**</span></span>      | <span data-ttu-id="d0bf0-124">且顯示0x80004003</span><span class="sxs-lookup"><span data-stu-id="d0bf0-124">0x80004003</span></span>    | <span data-ttu-id="d0bf0-125">指標值未正確傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-125">**NULL** was passed incorrectly for a pointer value.</span></span> |
| <span data-ttu-id="d0bf0-126">**E 未 \_ 預期**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-126">**E\_UNEXPECTED**</span></span>   | <span data-ttu-id="d0bf0-127">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="d0bf0-127">0x8000FFFF</span></span>    | <span data-ttu-id="d0bf0-128">未預期的情況。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-128">Unexpected condition.</span></span>                                |
| <span data-ttu-id="d0bf0-129">**S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-129">**S\_OK**</span></span>           | <span data-ttu-id="d0bf0-130">0x0</span><span class="sxs-lookup"><span data-stu-id="d0bf0-130">0x0</span></span>           | <span data-ttu-id="d0bf0-131">成功。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-131">Success.</span></span>                                             |
| <span data-ttu-id="d0bf0-132">**S \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-132">**S\_FALSE**</span></span>        | <span data-ttu-id="d0bf0-133">0x1</span><span class="sxs-lookup"><span data-stu-id="d0bf0-133">0x1</span></span>           | <span data-ttu-id="d0bf0-134">成功。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-134">Success.</span></span>                                             |



 

<span data-ttu-id="d0bf0-135">前置詞為 "E" 的所有常數 \_ 都是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-135">All of the constants with the prefix "E\_" are error codes.</span></span> <span data-ttu-id="d0bf0-136">常數 **S \_ OK** 和 **S \_ FALSE** 都是成功的代碼。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-136">The constants **S\_OK** and **S\_FALSE** are both success codes.</span></span> <span data-ttu-id="d0bf0-137">可能是99% 的 COM 方法 **會 \_ 在成功時傳回** ，但不讓這項事實誤導您。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-137">Probably 99% of COM methods return **S\_OK** when they succeed; but do not let this fact mislead you.</span></span> <span data-ttu-id="d0bf0-138">方法可能會傳回其他成功的程式碼，因此請一律使用 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) 或 [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) 的宏來測試錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-138">A method might return other success codes, so always test for errors by using the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) or [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="d0bf0-139">下列範例程式碼顯示錯誤的方式，以及測試函數呼叫是否成功的正確方式。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-139">The following example code shows the wrong way and the right way to test for the success of a function call.</span></span>


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



<span data-ttu-id="d0bf0-140">成功碼 **\_ 為 FALSE** ，則值得提及。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-140">The success code **S\_FALSE** deserves mention.</span></span> <span data-ttu-id="d0bf0-141">某些方法會 **使用 \_ FALSE** 來平均表示非失敗的負條件。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-141">Some methods use **S\_FALSE** to mean, roughly, a negative condition that is not a failure.</span></span> <span data-ttu-id="d0bf0-142">它也可以表示「無作業」—方法成功，但不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-142">It can also indicate a "no-op"—the method succeeded, but had no effect.</span></span> <span data-ttu-id="d0bf0-143">例如，如果您從相同的執行緒呼叫第二次， [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 函式會傳回 **S \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-143">For example, the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function returns **S\_FALSE** if you call it a second time from the same thread.</span></span> <span data-ttu-id="d0bf0-144">如果您需要區分程式碼中的 **\_ [確定] 和 [** **\_ FALSE** ]，您應該直接測試值，但仍使用 [ [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) ] 或 [ [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) ] 來處理其餘的案例，如下列範例程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-144">If you need to differentiate between **S\_OK** and **S\_FALSE** in your code, you should test the value directly, but still use [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) or [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) to handle the remaining cases, as shown in the following example code.</span></span>


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



<span data-ttu-id="d0bf0-145">某些 **HRESULT** 值專屬於特定的 Windows 功能或子系統。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-145">Some **HRESULT** values are specific to a particular feature or subsystem of Windows.</span></span> <span data-ttu-id="d0bf0-146">例如，Direct2D 圖形 API 會定義錯誤碼 **D2DERR \_ 不支援的 \_ 圖元 \_ 格式**，這表示程式使用的像素格式不受支援。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-146">For example, the Direct2D graphics API defines the error code **D2DERR\_UNSUPPORTED\_PIXEL\_FORMAT**, which means that the program used an unsupported pixel format.</span></span> <span data-ttu-id="d0bf0-147">MSDN 檔通常會提供方法可能會傳回的特定錯誤碼清單。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-147">MSDN documentation often gives a list of specific error codes that a method might return.</span></span> <span data-ttu-id="d0bf0-148">不過，您不應該將這些清單視為具有決定性。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-148">However, you should not consider these lists to be definitive.</span></span> <span data-ttu-id="d0bf0-149">方法一律會傳回檔中未列出的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-149">A method can always return an **HRESULT** value that is not listed in the documentation.</span></span> <span data-ttu-id="d0bf0-150">同樣地，請使用 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) 和 [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) 的宏。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-150">Again, use the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macros.</span></span> <span data-ttu-id="d0bf0-151">如果您測試特定的錯誤碼，也請包含預設案例。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-151">If you test for a specific error code, include a default case as well.</span></span>


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a><span data-ttu-id="d0bf0-152">錯誤處理模式</span><span class="sxs-lookup"><span data-stu-id="d0bf0-152">Patterns for Error Handling</span></span>

<span data-ttu-id="d0bf0-153">本節探討以結構化方式處理 COM 錯誤的一些模式。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-153">This section looks at some patterns for handling COM errors in a structured way.</span></span> <span data-ttu-id="d0bf0-154">每個模式都有優缺點。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-154">Each pattern has advantages and disadvantages.</span></span> <span data-ttu-id="d0bf0-155">在某些程度上，選擇是一種感受。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-155">To some extent, the choice is a matter of taste.</span></span> <span data-ttu-id="d0bf0-156">如果您使用現有的專案，它可能已經有 proscribe 特定樣式的編碼方針。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-156">If you work on an existing project, it might already have coding guidelines that proscribe a particular style.</span></span> <span data-ttu-id="d0bf0-157">無論您採用哪種模式，健全的程式碼都將遵守下列規則。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-157">Regardless of which pattern you adopt, robust code will obey the following rules.</span></span>

-   <span data-ttu-id="d0bf0-158">針對傳回 **HRESULT** 的每個方法或函式，請先檢查傳回值再繼續。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-158">For every method or function that returns an **HRESULT**, check the return value before proceeding.</span></span>
-   <span data-ttu-id="d0bf0-159">使用之後釋放資源。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-159">Release resources after they are used.</span></span>
-   <span data-ttu-id="d0bf0-160">請勿嘗試存取無效或未初始化的資源，例如 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-160">Do not attempt to access invalid or uninitialized resources, such as **NULL** pointers.</span></span>
-   <span data-ttu-id="d0bf0-161">在您釋放資源之後，請勿嘗試使用它。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-161">Do not try to use a resource after you release it.</span></span>

<span data-ttu-id="d0bf0-162">考慮這些規則，以下是處理錯誤的四種模式。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-162">With these rules in mind, here are four patterns for handling errors.</span></span>

-   [<span data-ttu-id="d0bf0-163">嵌套的 ifs</span><span class="sxs-lookup"><span data-stu-id="d0bf0-163">Nested ifs</span></span>](#nested-ifs)
-   [<span data-ttu-id="d0bf0-164">串聯式 ifs</span><span class="sxs-lookup"><span data-stu-id="d0bf0-164">Cascading ifs</span></span>](#cascading-ifs)
-   [<span data-ttu-id="d0bf0-165">失敗時跳</span><span class="sxs-lookup"><span data-stu-id="d0bf0-165">Jump on Fail</span></span>](#jump-on-fail)
-   [<span data-ttu-id="d0bf0-166">失敗時擲回</span><span class="sxs-lookup"><span data-stu-id="d0bf0-166">Throw on Fail</span></span>](#throw-on-fail)

### <a name="nested-ifs"></a><span data-ttu-id="d0bf0-167">嵌套的 ifs</span><span class="sxs-lookup"><span data-stu-id="d0bf0-167">Nested ifs</span></span>

<span data-ttu-id="d0bf0-168">在傳回 **HRESULT** 的每次呼叫之後，請使用 **if** 語句來測試是否成功。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-168">After every call that returns an **HRESULT**, use an **if** statement to test for success.</span></span> <span data-ttu-id="d0bf0-169">然後，將下一個方法呼叫放在 **if** 語句的範圍內。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-169">Then, put the next method call within the scope of the **if** statement.</span></span> <span data-ttu-id="d0bf0-170">如 **有需要** ，可以將更多語句嵌套至語句。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-170">More **if** statements can be nested as deeply as needed.</span></span> <span data-ttu-id="d0bf0-171">此課程模組中先前的程式碼範例已使用此模式，但在此會再次出現：</span><span class="sxs-lookup"><span data-stu-id="d0bf0-171">The previous code examples in this module have all used this pattern, but here it is again:</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



<span data-ttu-id="d0bf0-172">優點</span><span class="sxs-lookup"><span data-stu-id="d0bf0-172">Advantages</span></span>

-   <span data-ttu-id="d0bf0-173">變數可以用基本的範圍宣告。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-173">Variables can be declared with minimal scope.</span></span> <span data-ttu-id="d0bf0-174">例如，在使用 *pItem* 之前，不會宣告。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-174">For example, *pItem* is not declared until it is used.</span></span>
-   <span data-ttu-id="d0bf0-175">在每個 **if** 語句中，特定的非變異值為 True：所有先前的呼叫都已成功，且所有取得的資源仍有效。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-175">Within each **if** statement, certain invariants are true: All previous calls have succeeded, and all acquired resources are still valid.</span></span> <span data-ttu-id="d0bf0-176">在上述範例中，當程式到達最內層的 **if** 語句時， *pItem* 和 *pFileOpen* 都已知有效。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-176">In the previous example, when the program reaches the innermost **if** statement, both *pItem* and *pFileOpen* are known to be valid.</span></span>
-   <span data-ttu-id="d0bf0-177">您可以明確地釋放介面指標和其他資源。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-177">It is clear when to release interface pointers and other resources.</span></span> <span data-ttu-id="d0bf0-178">您會在 **if** 語句的結尾釋放資源，緊接在取得資源的呼叫之後。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-178">You release a resource at the end of the **if** statement that immediately follows the call that acquired the resource.</span></span>

<span data-ttu-id="d0bf0-179">缺點</span><span class="sxs-lookup"><span data-stu-id="d0bf0-179">Disadvantages</span></span>

-   <span data-ttu-id="d0bf0-180">有些人發現深層的嵌套難以閱讀。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-180">Some people find deep nesting hard to read.</span></span>
-   <span data-ttu-id="d0bf0-181">錯誤處理與其他分支和迴圈語句混合在一起。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-181">Error handling is mixed in with other branching and looping statements.</span></span> <span data-ttu-id="d0bf0-182">這可能會使整體程式邏輯更難追蹤。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-182">This can make the overall program logic harder to follow.</span></span>

### <a name="cascading-ifs"></a><span data-ttu-id="d0bf0-183">串聯式 ifs</span><span class="sxs-lookup"><span data-stu-id="d0bf0-183">Cascading ifs</span></span>

<span data-ttu-id="d0bf0-184">在每個方法呼叫之後，請使用 **if** 語句來測試是否成功。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-184">After each method call, use an **if** statement to test for success.</span></span> <span data-ttu-id="d0bf0-185">如果方法成功，請將下一個方法呼叫放在 **if** 區塊內。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-185">If the method succeeds, place the next method call inside the **if** block.</span></span> <span data-ttu-id="d0bf0-186">但是，請將每個後續 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded)的測試放在先前的 **if** 區塊之後，而不是進一步嵌套 **if** 語句。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-186">But instead of nesting further **if** statements, place each subsequent [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) test after the previous **if** block.</span></span> <span data-ttu-id="d0bf0-187">如果有任何方法失敗，則所有其餘 **成功** 的測試都只會失敗，直到到達函式的底部為止。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-187">If any method fails, all the remaining **SUCCEEDED** tests simply fail until the bottom of the function is reached.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="d0bf0-188">在此模式中，您會在函式的最一端釋放資源。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-188">In this pattern, you release resources at the very end of the function.</span></span> <span data-ttu-id="d0bf0-189">如果發生錯誤，當函式結束時，某些指標可能會無效。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-189">If an error occurs, some pointers might be invalid when the function exits.</span></span> <span data-ttu-id="d0bf0-190">在不正確指標上呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 將會使程式 (或更糟的) 而損毀，因此您必須將所有指標初始化為 **null** ，並檢查它們是否為 **null** ，然後再釋放它們。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-190">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on an invalid pointer will crash the program (or worse), so you must initialize all pointers to **NULL** and check whether they are **NULL** before releasing them.</span></span> <span data-ttu-id="d0bf0-191">此範例使用函式 `SafeRelease` ; 智慧型指標也是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-191">This example uses the `SafeRelease` function; smart pointers are also a good choice.</span></span>

<span data-ttu-id="d0bf0-192">如果您使用此模式，您必須小心使用迴圈結構。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-192">If you use this pattern, you must be careful with loop constructs.</span></span> <span data-ttu-id="d0bf0-193">在迴圈中，如果有任何呼叫失敗，請中斷迴圈。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-193">Inside a loop, break from the loop if any call fails.</span></span>

<span data-ttu-id="d0bf0-194">優點</span><span class="sxs-lookup"><span data-stu-id="d0bf0-194">Advantages</span></span>

-   <span data-ttu-id="d0bf0-195">這個模式所建立的嵌套小於「nested ifs」模式。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-195">This pattern creates less nesting than the "nested ifs" pattern.</span></span>
-   <span data-ttu-id="d0bf0-196">您可以更輕鬆地查看整體控制流程。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-196">Overall control flow is easier to see.</span></span>
-   <span data-ttu-id="d0bf0-197">資源會在程式碼中的某個時間點釋放。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-197">Resources are released at one point in the code.</span></span>

<span data-ttu-id="d0bf0-198">缺點</span><span class="sxs-lookup"><span data-stu-id="d0bf0-198">Disadvantages</span></span>

-   <span data-ttu-id="d0bf0-199">所有變數都必須在函式頂端宣告和初始化。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-199">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="d0bf0-200">如果呼叫失敗，函式會進行多個不必要的錯誤檢查，而不是立即結束函式。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-200">If a call fails, the function makes multiple unneeded error checks, instead of exiting the function immediately.</span></span>
-   <span data-ttu-id="d0bf0-201">因為控制流程會在失敗之後繼續執行函式，所以您必須在函式主體中小心，不要存取不正確資源。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-201">Because the flow of control continues through the function after a failure, you must be careful throughout the body of the function not to access invalid resources.</span></span>
-   <span data-ttu-id="d0bf0-202">迴圈內的錯誤需要特殊大小寫。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-202">Errors inside a loop require a special case.</span></span>

### <a name="jump-on-fail"></a><span data-ttu-id="d0bf0-203">失敗時跳</span><span class="sxs-lookup"><span data-stu-id="d0bf0-203">Jump on Fail</span></span>

<span data-ttu-id="d0bf0-204">在每個方法呼叫之後，測試失敗 (不是成功的) 。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-204">After each method call, test for failure (not success).</span></span> <span data-ttu-id="d0bf0-205">失敗時，跳至接近函式底部的標籤。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-205">On failure, jump to a label near the bottom of the function.</span></span> <span data-ttu-id="d0bf0-206">在標籤之後，但在結束函式之前，釋放資源。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-206">After the label, but before exiting the function, release resources.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="d0bf0-207">優點</span><span class="sxs-lookup"><span data-stu-id="d0bf0-207">Advantages</span></span>

-   <span data-ttu-id="d0bf0-208">您可以輕鬆看到整個控制流程。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-208">The overall control flow is easy to see.</span></span>
-   <span data-ttu-id="d0bf0-209">檢查 [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) 之後，在程式碼中的每個點，如果您沒有跳到標籤，就保證所有先前的呼叫都已成功。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-209">At every point in the code after a [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) check, if you have not jumped to the label, it is guaranteed that all the previous calls have succeeded.</span></span>
-   <span data-ttu-id="d0bf0-210">資源會在程式碼中的一個位置釋放。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-210">Resources are released at one place in the code.</span></span>

<span data-ttu-id="d0bf0-211">缺點</span><span class="sxs-lookup"><span data-stu-id="d0bf0-211">Disadvantages</span></span>

-   <span data-ttu-id="d0bf0-212">所有變數都必須在函式頂端宣告和初始化。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-212">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="d0bf0-213">某些程式設計人員不想在其程式碼中使用 **goto** 。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-213">Some programmers do not like to use **goto** in their code.</span></span> <span data-ttu-id="d0bf0-214"> (不過，請注意， **這種用法是高度** 結構化的：程式碼永遠不會跳到目前的函式呼叫之外。 ) </span><span class="sxs-lookup"><span data-stu-id="d0bf0-214">(However, it should be noted that this use of **goto** is highly structured; the code never jumps outside the current function call.)</span></span>
-   <span data-ttu-id="d0bf0-215">**goto** 語句會略過初始化運算式。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-215">**goto** statements skip initializers.</span></span>

### <a name="throw-on-fail"></a><span data-ttu-id="d0bf0-216">失敗時擲回</span><span class="sxs-lookup"><span data-stu-id="d0bf0-216">Throw on Fail</span></span>

<span data-ttu-id="d0bf0-217">您可以在方法失敗時擲回例外狀況，而不是跳至標籤。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-217">Rather than jump to a label, you can throw an exception when a method fails.</span></span> <span data-ttu-id="d0bf0-218">如果您用來撰寫例外狀況安全的程式碼，這可能會產生更慣用的 c + + 樣式。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-218">This can produce a more idiomatic style of C++ if you are used to writing exception-safe code.</span></span>


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



<span data-ttu-id="d0bf0-219">請注意，此範例會使用 **CComPtr** 類別來管理介面指標。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-219">Notice that this example uses the **CComPtr** class to manage interface pointers.</span></span> <span data-ttu-id="d0bf0-220">一般而言，如果您的程式碼擲回例外狀況，您應該遵循 RAII (資源取得是) 模式的初始化。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-220">Generally, if your code throws exceptions, you should follow the RAII (Resource Acquisition is Initialization) pattern.</span></span> <span data-ttu-id="d0bf0-221">也就是說，每個資源都應該由其可保證正確釋放資源的物件來管理。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-221">That is, every resource should be managed by an object whose destructor guarantees that the resource is correctly released.</span></span> <span data-ttu-id="d0bf0-222">如果擲回例外狀況，就一定會叫用此函式。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-222">If an exception is thrown, the destructor is guaranteed to be invoked.</span></span> <span data-ttu-id="d0bf0-223">否則，您的程式可能會洩漏資源。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-223">Otherwise, your program might leak resources.</span></span>

<span data-ttu-id="d0bf0-224">優點</span><span class="sxs-lookup"><span data-stu-id="d0bf0-224">Advantages</span></span>

-   <span data-ttu-id="d0bf0-225">與使用例外狀況處理的現有程式碼相容。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-225">Compatible with existing code that uses exception handling.</span></span>
-   <span data-ttu-id="d0bf0-226">與擲回例外狀況的 c + + 程式庫相容，例如標準範本程式庫 (STL) 。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-226">Compatible with C++ libraries that throw exceptions, such as the Standard Template Library (STL).</span></span>

<span data-ttu-id="d0bf0-227">缺點</span><span class="sxs-lookup"><span data-stu-id="d0bf0-227">Disadvantages</span></span>

-   <span data-ttu-id="d0bf0-228">需要 c + + 物件來管理資源，例如記憶體或檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-228">Requires C++ objects to manage resources such as memory or file handles.</span></span>
-   <span data-ttu-id="d0bf0-229">需要充分瞭解如何撰寫例外狀況安全程式碼。</span><span class="sxs-lookup"><span data-stu-id="d0bf0-229">Requires a good understanding of how to write exception-safe code.</span></span>

## <a name="next"></a><span data-ttu-id="d0bf0-230">下一個</span><span class="sxs-lookup"><span data-stu-id="d0bf0-230">Next</span></span>

[<span data-ttu-id="d0bf0-231">模組3。Windows 圖形</span><span class="sxs-lookup"><span data-stu-id="d0bf0-231">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)

 

 
