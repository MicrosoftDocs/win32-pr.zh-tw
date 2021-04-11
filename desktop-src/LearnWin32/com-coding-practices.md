---
title: COM 編碼作法
description: 本主題說明讓您的 COM 程式碼更有效率且更穩固的方式。
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104093436"
---
# <a name="com-coding-practices"></a><span data-ttu-id="f51e7-103">COM 編碼作法</span><span class="sxs-lookup"><span data-stu-id="f51e7-103">COM Coding Practices</span></span>

<span data-ttu-id="f51e7-104">本主題說明讓您的 COM 程式碼更有效率且更穩固的方式。</span><span class="sxs-lookup"><span data-stu-id="f51e7-104">This topic describes ways to make your COM code more effective and robust.</span></span>

-   [<span data-ttu-id="f51e7-105">\_ \_ Uuidof 運算子</span><span class="sxs-lookup"><span data-stu-id="f51e7-105">The \_\_uuidof Operator</span></span>](/windows)
-   [<span data-ttu-id="f51e7-106">IID \_ PPV \_ ARGS 宏</span><span class="sxs-lookup"><span data-stu-id="f51e7-106">The IID\_PPV\_ARGS Macro</span></span>](/windows)
-   [<span data-ttu-id="f51e7-107">SafeRelease 模式</span><span class="sxs-lookup"><span data-stu-id="f51e7-107">The SafeRelease Pattern</span></span>](#the-saferelease-pattern)
-   [<span data-ttu-id="f51e7-108">COM 智慧型指標</span><span class="sxs-lookup"><span data-stu-id="f51e7-108">COM Smart Pointers</span></span>](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a><span data-ttu-id="f51e7-109">\_ \_ Uuidof 運算子</span><span class="sxs-lookup"><span data-stu-id="f51e7-109">The \_\_uuidof Operator</span></span>

<span data-ttu-id="f51e7-110">當您建立程式時，可能會收到類似下列的連結器錯誤：</span><span class="sxs-lookup"><span data-stu-id="f51e7-110">When you build your program, you might get linker errors similar to the following:</span></span>

`unresolved external symbol "struct _GUID const IID_IDrawable"`

<span data-ttu-id="f51e7-111">此錯誤表示 GUID 常數是使用外部連結 (**extern**) 宣告，而連結器找不到常數的定義。</span><span class="sxs-lookup"><span data-stu-id="f51e7-111">This error means that a GUID constant was declared with external linkage (**extern**), and the linker could not find the definition of the constant.</span></span> <span data-ttu-id="f51e7-112">GUID 常數的值通常會從靜態程式庫檔案匯出。</span><span class="sxs-lookup"><span data-stu-id="f51e7-112">The value of a GUID constant is usually exported from a static library file.</span></span> <span data-ttu-id="f51e7-113">如果您使用 Microsoft Visual C++，則可以避免使用 **\_ \_ uuidof** 運算子連結靜態程式庫的需求。</span><span class="sxs-lookup"><span data-stu-id="f51e7-113">If you are using Microsoft Visual C++, you can avoid the need to link a static library by using the **\_\_uuidof** operator.</span></span> <span data-ttu-id="f51e7-114">此運算子是 Microsoft 語言擴充功能。</span><span class="sxs-lookup"><span data-stu-id="f51e7-114">This operator is a Microsoft language extension.</span></span> <span data-ttu-id="f51e7-115">它會從運算式傳回 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="f51e7-115">It returns a GUID value from an expression.</span></span> <span data-ttu-id="f51e7-116">運算式可以是介面型別名稱、類別名稱或介面指標。</span><span class="sxs-lookup"><span data-stu-id="f51e7-116">The expression can be an interface type name, a class name, or an interface pointer.</span></span> <span data-ttu-id="f51e7-117">使用 **\_ \_ uuidof**，您可以建立一般專案對話方塊物件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f51e7-117">Using **\_\_uuidof**, you can create the Common Item Dialog object as follows:</span></span>


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



<span data-ttu-id="f51e7-118">編譯器會從標頭中解壓縮 GUID 值，因此不需要任何程式庫匯出。</span><span class="sxs-lookup"><span data-stu-id="f51e7-118">The compiler extracts the GUID value from the header, so no library export is necessary.</span></span>

> [!Note]  
> <span data-ttu-id="f51e7-119">GUID 值是藉由 `__declspec(uuid( ... ))` 在標頭中宣告來與型別名稱相關聯。</span><span class="sxs-lookup"><span data-stu-id="f51e7-119">The GUID value is associated with the type name by declaring `__declspec(uuid( ... ))` in the header.</span></span> <span data-ttu-id="f51e7-120">如需詳細資訊，請參閱 Visual C++ 檔中的 **\_ \_ declspec** 檔。</span><span class="sxs-lookup"><span data-stu-id="f51e7-120">For more information, see the documentation for **\_\_declspec** in the Visual C++ documentation.</span></span>

 

## <a name="the-iid_ppv_args-macro"></a><span data-ttu-id="f51e7-121">IID \_ PPV \_ ARGS 宏</span><span class="sxs-lookup"><span data-stu-id="f51e7-121">The IID\_PPV\_ARGS Macro</span></span>

<span data-ttu-id="f51e7-122">我們看到 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)和 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))都需要將最後一個參數強迫回 **void \* \*** 型別。</span><span class="sxs-lookup"><span data-stu-id="f51e7-122">We saw that both [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) require coercing the final parameter to a **void\*\*** type.</span></span> <span data-ttu-id="f51e7-123">這會造成類型不符的可能性。</span><span class="sxs-lookup"><span data-stu-id="f51e7-123">This creates the potential for a type mismatch.</span></span> <span data-ttu-id="f51e7-124">請考慮下列程式碼片段：</span><span class="sxs-lookup"><span data-stu-id="f51e7-124">Consider the following code fragment:</span></span>


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



<span data-ttu-id="f51e7-125">此程式碼會要求 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 介面，但會傳入 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 指標。</span><span class="sxs-lookup"><span data-stu-id="f51e7-125">This code asks for the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface, but passes in an [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer.</span></span> <span data-ttu-id="f51e7-126">**重新解譯 \_ cast** 運算式會規避 c + + 類型系統，因此編譯器不會攔截這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="f51e7-126">The **reinterpret\_cast** expression circumvents the C++ type system, so the compiler will not catch this error.</span></span> <span data-ttu-id="f51e7-127">在最佳情況下，如果物件不會執行要求的介面，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="f51e7-127">In the best case, if the object does not implement the requested interface, the call simply fails.</span></span> <span data-ttu-id="f51e7-128">在最糟的情況下，函式會成功，而且您會有不相符的指標。</span><span class="sxs-lookup"><span data-stu-id="f51e7-128">In the worst case, the function succeeds and you have a mismatched pointer.</span></span> <span data-ttu-id="f51e7-129">換句話說，指標類型與記憶體中的實際 vtable 不相符。</span><span class="sxs-lookup"><span data-stu-id="f51e7-129">In other words, the pointer type does not match the actual vtable in memory.</span></span> <span data-ttu-id="f51e7-130">如您所見，此時不會有任何好處。</span><span class="sxs-lookup"><span data-stu-id="f51e7-130">As you can imagine, nothing good can happen at that point.</span></span>

> [!Note]  
> <span data-ttu-id="f51e7-131">*Vtable* (虛擬方法資料表) 是函數指標的資料表。</span><span class="sxs-lookup"><span data-stu-id="f51e7-131">A *vtable* (virtual method table) is a table of function pointers.</span></span> <span data-ttu-id="f51e7-132">Vtable 是 COM 如何在執行時間將方法呼叫系結至其實作為。</span><span class="sxs-lookup"><span data-stu-id="f51e7-132">The vtable is how COM binds a method call to its implementation at run time.</span></span> <span data-ttu-id="f51e7-133">剛好，vtable 是大部分 c + + 編譯器如何執行虛擬方法的方式。</span><span class="sxs-lookup"><span data-stu-id="f51e7-133">Not coincidentally, vtables are how most C++ compilers implement virtual methods.</span></span>

 

<span data-ttu-id="f51e7-134">[**IID \_ PPV \_ ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args)宏可協助避免此錯誤類別。</span><span class="sxs-lookup"><span data-stu-id="f51e7-134">The [**IID\_PPV\_ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) macro helps to avoid this class of error.</span></span> <span data-ttu-id="f51e7-135">若要使用這個宏，請取代下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="f51e7-135">To use this macro, replace the following code:</span></span>


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



<span data-ttu-id="f51e7-136">取代為這個：</span><span class="sxs-lookup"><span data-stu-id="f51e7-136">with this:</span></span>


```C++
IID_PPV_ARGS(&pFileOpen)
```



<span data-ttu-id="f51e7-137">宏會自動插入 `__uuidof(IFileOpenDialog)` 介面識別碼，因此保證會符合指標類型。</span><span class="sxs-lookup"><span data-stu-id="f51e7-137">The macro automatically inserts `__uuidof(IFileOpenDialog)` for the interface identifier, so it is guaranteed to match the pointer type.</span></span> <span data-ttu-id="f51e7-138">以下是修改過的 (和正確的) 程式碼：</span><span class="sxs-lookup"><span data-stu-id="f51e7-138">Here is the modified (and correct) code:</span></span>


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



<span data-ttu-id="f51e7-139">您可以搭配使用相同的宏與 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))：</span><span class="sxs-lookup"><span data-stu-id="f51e7-139">You can use the same macro with [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a><span data-ttu-id="f51e7-140">SafeRelease 模式</span><span class="sxs-lookup"><span data-stu-id="f51e7-140">The SafeRelease Pattern</span></span>

<span data-ttu-id="f51e7-141">參考計數是在程式設計中的其中一項作業，基本上是很簡單，但也很繁瑣，讓您很容易出錯。</span><span class="sxs-lookup"><span data-stu-id="f51e7-141">Reference counting is one of those things in programming that is basically easy, but is also tedious, which makes it easy to get wrong.</span></span> <span data-ttu-id="f51e7-142">一般錯誤包含：</span><span class="sxs-lookup"><span data-stu-id="f51e7-142">Typical errors include:</span></span>

-   <span data-ttu-id="f51e7-143">當您完成使用介面指標時，無法釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="f51e7-143">Failing to release an interface pointer when you are done using it.</span></span> <span data-ttu-id="f51e7-144">這個 bug 類別會導致您的程式流失記憶體和其他資源，因為物件並未損毀。</span><span class="sxs-lookup"><span data-stu-id="f51e7-144">This class of bug will cause your program to leak memory and other resources, because objects are not destroyed.</span></span>
-   <span data-ttu-id="f51e7-145">呼叫具有無效指標的 [**版本**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="f51e7-145">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with an invalid pointer.</span></span> <span data-ttu-id="f51e7-146">例如，如果從未建立物件，就會發生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="f51e7-146">For example, this error can happen if the object was never created.</span></span> <span data-ttu-id="f51e7-147">這類 bug 可能會導致您的程式損毀。</span><span class="sxs-lookup"><span data-stu-id="f51e7-147">This category of bug will probably cause your program to crash.</span></span>
-   <span data-ttu-id="f51e7-148">呼叫 [**發行**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 之後的介面指標。</span><span class="sxs-lookup"><span data-stu-id="f51e7-148">Dereferencing an interface pointer after [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) is called.</span></span> <span data-ttu-id="f51e7-149">這個 bug 可能會導致您的程式損毀。</span><span class="sxs-lookup"><span data-stu-id="f51e7-149">This bug may cause your program to crash.</span></span> <span data-ttu-id="f51e7-150">更糟的是，它可能會導致您的程式在一段時間後損毀，因此難以追蹤原始錯誤。</span><span class="sxs-lookup"><span data-stu-id="f51e7-150">Worse, it may cause your program to crash at a random later time, making it hard to track down the original error.</span></span>

<span data-ttu-id="f51e7-151">避免這些錯誤的其中一種方式，是透過安全釋放指標的函式來呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="f51e7-151">One way to avoid these bugs is to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) through a function that safely releases the pointer.</span></span> <span data-ttu-id="f51e7-152">下列程式碼顯示執行此動作的函式：</span><span class="sxs-lookup"><span data-stu-id="f51e7-152">The following code shows a function that does this:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



<span data-ttu-id="f51e7-153">此函式會採用 COM 介面指標做為參數，並執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="f51e7-153">This function takes a COM interface pointer as a parameter and does the following:</span></span>

1.  <span data-ttu-id="f51e7-154">檢查指標是否為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f51e7-154">Checks whether the pointer is **NULL**.</span></span>
2.  <span data-ttu-id="f51e7-155">如果指標不是 **Null**，則呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="f51e7-155">Calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) if the pointer is not **NULL**.</span></span>
3.  <span data-ttu-id="f51e7-156">將指標設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f51e7-156">Sets the pointer to **NULL**.</span></span>

<span data-ttu-id="f51e7-157">以下是如何使用的範例 `SafeRelease` ：</span><span class="sxs-lookup"><span data-stu-id="f51e7-157">Here is an example of how to use `SafeRelease`:</span></span>


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



<span data-ttu-id="f51e7-158">如果 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 成功，則為 `SafeRelease` 釋放指標的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f51e7-158">If [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) succeeds, the call to `SafeRelease` releases the pointer.</span></span> <span data-ttu-id="f51e7-159">如果 **CoCreateInstance** 失敗， *PFileOpen* 會維持 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f51e7-159">If **CoCreateInstance** fails, *pFileOpen* remains **NULL**.</span></span> <span data-ttu-id="f51e7-160">此函式會 `SafeRelease` 檢查這一點，並略過 [**發行**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f51e7-160">The `SafeRelease` function checks for this and skips the call to [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span>

<span data-ttu-id="f51e7-161">也可以安全地 `SafeRelease` 在相同的指標上呼叫一次以上，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f51e7-161">It is also safe to call `SafeRelease` more than once on the same pointer, as shown here:</span></span>


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a><span data-ttu-id="f51e7-162">COM 智慧型指標</span><span class="sxs-lookup"><span data-stu-id="f51e7-162">COM Smart Pointers</span></span>

<span data-ttu-id="f51e7-163">函式 `SafeRelease` 很有用，但您需要記住兩件事：</span><span class="sxs-lookup"><span data-stu-id="f51e7-163">The `SafeRelease` function is useful, but it requires you to remember two things:</span></span>

-   <span data-ttu-id="f51e7-164">將每個介面指標初始化為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f51e7-164">Initialize every interface pointer to **NULL**.</span></span>
-   <span data-ttu-id="f51e7-165">`SafeRelease`在每個指標超出範圍之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="f51e7-165">Call `SafeRelease` before each pointer goes out of scope.</span></span>

<span data-ttu-id="f51e7-166">如果您是 c + + 程式設計人員，您可能會認為您不需要記住這其中一項。</span><span class="sxs-lookup"><span data-stu-id="f51e7-166">As a C++ programmer, you are probably thinking that you shouldn't have to remember either of these things.</span></span> <span data-ttu-id="f51e7-167">畢竟，c + + 具有函式和析構函數。</span><span class="sxs-lookup"><span data-stu-id="f51e7-167">After all, that's why C++ has constructors and destructors.</span></span> <span data-ttu-id="f51e7-168">要有一個包裝基礎介面指標的類別，並自動初始化和釋放指標，是很好的作法。</span><span class="sxs-lookup"><span data-stu-id="f51e7-168">It would be nice to have a class that wraps the underlying interface pointer and automatically initializes and releases the pointer.</span></span> <span data-ttu-id="f51e7-169">換句話說，我們需要像這樣的內容：</span><span class="sxs-lookup"><span data-stu-id="f51e7-169">In other words, we want something like this:</span></span>


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



<span data-ttu-id="f51e7-170">此處所示的類別定義不完整，而且無法使用，如下所示。</span><span class="sxs-lookup"><span data-stu-id="f51e7-170">The class definition shown here is incomplete, and is not usable as shown.</span></span> <span data-ttu-id="f51e7-171">您至少需要定義複製的函式、指派運算子，以及存取基礎 COM 指標的方式。</span><span class="sxs-lookup"><span data-stu-id="f51e7-171">At a minimum, you would need to define a copy constructor, an assignment operator, and a way to access the underlying COM pointer.</span></span> <span data-ttu-id="f51e7-172">幸運的是，您不需要執行這項工作，因為 Microsoft Visual Studio 已經提供智慧型指標類別做為 Active Template Library (ATL) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f51e7-172">Fortunately, you don't need to do any of this work, because Microsoft Visual Studio already provides a smart pointer class as part of the Active Template Library (ATL).</span></span>

<span data-ttu-id="f51e7-173">ATL 智慧型指標類別的名稱是 **CComPtr**。</span><span class="sxs-lookup"><span data-stu-id="f51e7-173">The ATL smart pointer class is named **CComPtr**.</span></span> <span data-ttu-id="f51e7-174"> (也有一個 **CComQIPtr** 類別，這並不在此討論 ) 。此處的 [開啟對話方塊](example--the-open-dialog-box.md) 範例已重寫為使用 **CComPtr**。</span><span class="sxs-lookup"><span data-stu-id="f51e7-174">(There is also a **CComQIPtr** class, which is not discussed here.) Here is the [Open Dialog Box](example--the-open-dialog-box.md) example rewritten to use **CComPtr**.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="f51e7-175">這段程式碼與原始範例之間的主要差異在於，這個版本不會明確地呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)。</span><span class="sxs-lookup"><span data-stu-id="f51e7-175">The main difference between this code and the original example is that this version does not explicitly call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="f51e7-176">當 **CComPtr** 實例超出範圍時，此函式會在基礎指標上呼叫 **Release** 。</span><span class="sxs-lookup"><span data-stu-id="f51e7-176">When the **CComPtr** instance goes out of scope, the destructor calls **Release** on the underlying pointer.</span></span>

<span data-ttu-id="f51e7-177">**CComPtr** 是類別範本。</span><span class="sxs-lookup"><span data-stu-id="f51e7-177">**CComPtr** is a class template.</span></span> <span data-ttu-id="f51e7-178">範本引數是 COM 介面型別。</span><span class="sxs-lookup"><span data-stu-id="f51e7-178">The template argument is the COM interface type.</span></span> <span data-ttu-id="f51e7-179">就內部而言， **CComPtr** 會保存該型別的指標。</span><span class="sxs-lookup"><span data-stu-id="f51e7-179">Internally, **CComPtr** holds a pointer of that type.</span></span> <span data-ttu-id="f51e7-180">**CComPtr** 會覆寫 **運算子-> ()** 和 **運算子& ()** 讓類別的行為就像基礎指標。</span><span class="sxs-lookup"><span data-stu-id="f51e7-180">**CComPtr** overrides **operator->()** and **operator&()** so that the class acts like the underlying pointer.</span></span> <span data-ttu-id="f51e7-181">例如，下列程式碼相當於直接呼叫 **IFileOpenDialog：： Show** 方法：</span><span class="sxs-lookup"><span data-stu-id="f51e7-181">For example, the following code is equivalent to calling the **IFileOpenDialog::Show** method directly:</span></span>


```C++
hr = pFileOpen->Show(NULL);
```



<span data-ttu-id="f51e7-182">**CComPtr** 也會定義 **CComPtr：： CoCreateInstance** 方法，它會使用一些預設參數值來呼叫 COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。</span><span class="sxs-lookup"><span data-stu-id="f51e7-182">**CComPtr** also defines a **CComPtr::CoCreateInstance** method, which calls the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function with some default parameter values.</span></span> <span data-ttu-id="f51e7-183">唯一必要的參數是類別識別碼，如下一個範例所示：</span><span class="sxs-lookup"><span data-stu-id="f51e7-183">The only required parameter is the class identifier, as the next example shows:</span></span>


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



<span data-ttu-id="f51e7-184">**CComPtr：： CoCreateInstance** 方法純粹是為了方便起見而提供;如果您想要的話，還是可以呼叫 COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)函數。</span><span class="sxs-lookup"><span data-stu-id="f51e7-184">The **CComPtr::CoCreateInstance** method is provided purely as a convenience; you can still call the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, if you prefer.</span></span>

## <a name="next"></a><span data-ttu-id="f51e7-185">下一個</span><span class="sxs-lookup"><span data-stu-id="f51e7-185">Next</span></span>

[<span data-ttu-id="f51e7-186">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="f51e7-186">Error Handling in COM</span></span>](error-handling-in-com.md)

 

 