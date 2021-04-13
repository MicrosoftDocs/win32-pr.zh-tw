---
title: 在 COM 中建立物件
description: 若要使用 COM 介面，您的程式首先會建立物件的實例，該實例會執行該介面。
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375136"
---
# <a name="creating-an-object-in-com"></a><span data-ttu-id="a4466-103">在 COM 中建立物件</span><span class="sxs-lookup"><span data-stu-id="a4466-103">Creating an Object in COM</span></span>

<span data-ttu-id="a4466-104">執行緒初始化 COM 程式庫之後，就可以安全地讓執行緒使用 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="a4466-104">After a thread has initialized the COM library, it is safe for the thread to use COM interfaces.</span></span> <span data-ttu-id="a4466-105">若要使用 COM 介面，您的程式首先會建立物件的實例，該實例會執行該介面。</span><span class="sxs-lookup"><span data-stu-id="a4466-105">To use a COM interface, your program first creates an instance of an object that implements that interface.</span></span>

<span data-ttu-id="a4466-106">一般情況下，有兩種方式可以建立 COM 物件：</span><span class="sxs-lookup"><span data-stu-id="a4466-106">In general, there are two ways to create a COM object:</span></span>

-   <span data-ttu-id="a4466-107">執行物件的模組可能會提供特別設計的函式，以建立該物件的實例。</span><span class="sxs-lookup"><span data-stu-id="a4466-107">The module that implements the object might provide a function specifically designed to create instances of that object.</span></span>
-   <span data-ttu-id="a4466-108">此外，COM 也提供名為 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的一般建立函數。</span><span class="sxs-lookup"><span data-stu-id="a4466-108">Alternatively, COM provides a generic creation function named [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="a4466-109">例如，從主題的「 `Shape` [什麼是 COM 介面](what-is-a-com-interface-.md)」取得假設的物件。</span><span class="sxs-lookup"><span data-stu-id="a4466-109">For example, take the hypothetical `Shape` object from the topic [What Is a COM Interface?](what-is-a-com-interface-.md).</span></span> <span data-ttu-id="a4466-110">在該範例中， `Shape` 物件會執行名為的介面 `IDrawable` 。</span><span class="sxs-lookup"><span data-stu-id="a4466-110">In that example, the `Shape` object implements an interface named `IDrawable`.</span></span> <span data-ttu-id="a4466-111">執行物件的圖形程式庫 `Shape` 可能會使用下列簽章匯出函式。</span><span class="sxs-lookup"><span data-stu-id="a4466-111">The graphics library that implements the `Shape` object might export a function with the following signature.</span></span>


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



<span data-ttu-id="a4466-112">指定此函式時，您可以建立新的物件，如下所示 `Shape` 。</span><span class="sxs-lookup"><span data-stu-id="a4466-112">Given this function, you could create a new `Shape` object as follows.</span></span>


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="a4466-113">*PpShape* 參數的類型為指標 to `IDrawable` 。</span><span class="sxs-lookup"><span data-stu-id="a4466-113">The *ppShape* parameter is of type pointer-to-pointer-to-`IDrawable`.</span></span> <span data-ttu-id="a4466-114">如果您之前未看到此模式，可能會令人困惑雙重間接取值。</span><span class="sxs-lookup"><span data-stu-id="a4466-114">If you have not seen this pattern before, the double indirection might be puzzling.</span></span>

<span data-ttu-id="a4466-115">請考慮函數的需求 `CreateShape` 。</span><span class="sxs-lookup"><span data-stu-id="a4466-115">Consider the requirements of the `CreateShape` function.</span></span> <span data-ttu-id="a4466-116">函數必須將 `IDrawable` 指標傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="a4466-116">The function must give an `IDrawable` pointer back to the caller.</span></span> <span data-ttu-id="a4466-117">但函數的傳回值已用於錯誤/成功碼。</span><span class="sxs-lookup"><span data-stu-id="a4466-117">But the function's return value is already used for the error/success code.</span></span> <span data-ttu-id="a4466-118">因此，指標必須透過函數的引數傳回。</span><span class="sxs-lookup"><span data-stu-id="a4466-118">Therefore, the pointer must be returned through an argument to the function.</span></span> <span data-ttu-id="a4466-119">呼叫端會將類型的變數傳遞 `IDrawable*` 至函式，而函式會以新指標覆寫此變數 `IDrawable` 。</span><span class="sxs-lookup"><span data-stu-id="a4466-119">The caller will pass a variable of type `IDrawable*` to the function, and the function will overwrite this variable with a new `IDrawable` pointer.</span></span> <span data-ttu-id="a4466-120">在 c + + 中，有兩種方式可讓函式覆寫參數值：以傳址方式傳遞，或依位址傳遞。</span><span class="sxs-lookup"><span data-stu-id="a4466-120">In C++, there are only two ways for a function to overwrite a parameter value: pass by reference, or pass by address.</span></span> <span data-ttu-id="a4466-121">COM 使用後者的傳遞位址。</span><span class="sxs-lookup"><span data-stu-id="a4466-121">COM uses the latter, pass-by-address.</span></span> <span data-ttu-id="a4466-122">指標的位址是指標指標，所以參數型別必須是 `IDrawable**` 。</span><span class="sxs-lookup"><span data-stu-id="a4466-122">And the address of a pointer is a pointer-to-a-pointer, so the parameter type must be `IDrawable**`.</span></span>

<span data-ttu-id="a4466-123">以下的圖表可協助您以視覺化方式呈現進展。</span><span class="sxs-lookup"><span data-stu-id="a4466-123">Here is a diagram to help visualize what's going on.</span></span>

![顯示雙指標間接取值的圖表](images/com03.png)

<span data-ttu-id="a4466-125">`CreateShape`函數會使用 *pShape* (的位址 `&pShape`) 將新的指標值寫入 *pShape*。</span><span class="sxs-lookup"><span data-stu-id="a4466-125">The `CreateShape` function uses the address of *pShape* (`&pShape`) to write a new pointer value to *pShape*.</span></span>

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a><span data-ttu-id="a4466-126">CoCreateInstance：建立物件的一般方式</span><span class="sxs-lookup"><span data-stu-id="a4466-126">CoCreateInstance: A Generic Way to Create Objects</span></span>

<span data-ttu-id="a4466-127">[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)函數提供用來建立物件的一般機制。</span><span class="sxs-lookup"><span data-stu-id="a4466-127">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function provides a generic mechanism for creating objects.</span></span> <span data-ttu-id="a4466-128">若要瞭解 **CoCreateInstance**，請記住，有兩個 COM 物件可以執行相同的介面，而一個物件可執行兩個或多個介面。</span><span class="sxs-lookup"><span data-stu-id="a4466-128">To understand **CoCreateInstance**, keep in mind that two COM objects can implement the same interface, and one object can implement two or more interfaces.</span></span> <span data-ttu-id="a4466-129">因此，建立物件的泛型函數需要兩項資訊。</span><span class="sxs-lookup"><span data-stu-id="a4466-129">Thus, a generic function that creates objects needs two pieces of information.</span></span>

-   <span data-ttu-id="a4466-130">要建立的物件。</span><span class="sxs-lookup"><span data-stu-id="a4466-130">Which object to create.</span></span>
-   <span data-ttu-id="a4466-131">要從物件取得的介面。</span><span class="sxs-lookup"><span data-stu-id="a4466-131">Which interface to get from the object.</span></span>

<span data-ttu-id="a4466-132">但是，我們要如何在呼叫函式時指出這種資訊呢？</span><span class="sxs-lookup"><span data-stu-id="a4466-132">But how do we indicate this information when we call the function?</span></span> <span data-ttu-id="a4466-133">在 COM 中，物件或介面是藉由指派128位數位（稱為 *全域唯一識別碼* (GUID) 來識別）。</span><span class="sxs-lookup"><span data-stu-id="a4466-133">In COM, an object or an interface is identified by assigning it a 128-bit number, called a *globally unique identifier* (GUID).</span></span> <span data-ttu-id="a4466-134">Guid 會以讓它們有效的方式產生。</span><span class="sxs-lookup"><span data-stu-id="a4466-134">GUIDs are generated in a way that makes them effectively unique.</span></span> <span data-ttu-id="a4466-135">Guid 是一種解決方法，可解決如何建立沒有中央登錄授權單位的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4466-135">GUIDs are a solution to the problem of how to create unique identifiers without a central registration authority.</span></span> <span data-ttu-id="a4466-136">Guid 有時也稱為 *通用唯一識別碼* ， (uuid) 。</span><span class="sxs-lookup"><span data-stu-id="a4466-136">GUIDs are sometimes called *universally unique identifiers* (UUIDs).</span></span> <span data-ttu-id="a4466-137">在 COM 之前，它們用於 DCE/RPC (分散式運算環境/遠端程序呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="a4466-137">Prior to COM, they were used in DCE/RPC (Distributed Computing Environment/Remote Procedure Call).</span></span> <span data-ttu-id="a4466-138">有數種演算法可用於建立新的 Guid。</span><span class="sxs-lookup"><span data-stu-id="a4466-138">Several algorithms exist for creating new GUIDs.</span></span> <span data-ttu-id="a4466-139">並非所有這些演算法都能完全保證唯一性，但是不小心建立相同 GUID 值的機率相當小，實際上是零。</span><span class="sxs-lookup"><span data-stu-id="a4466-139">Not all of these algorithms strictly guarantee uniqueness, but the probability of accidentally creating the same GUID value twice is extremely small—effectively zero.</span></span> <span data-ttu-id="a4466-140">Guid 可以用來識別任何類型的實體，而不只是物件和介面。</span><span class="sxs-lookup"><span data-stu-id="a4466-140">GUIDs can be used to identify any sort of entity, not just objects and interfaces.</span></span> <span data-ttu-id="a4466-141">不過，這是我們在此課程模組中唯一關心的用途。</span><span class="sxs-lookup"><span data-stu-id="a4466-141">However, that is the only use that concerns us in this module.</span></span>

<span data-ttu-id="a4466-142">例如，連結 `Shapes` 庫可能會宣告兩個 GUID 常數：</span><span class="sxs-lookup"><span data-stu-id="a4466-142">For example, the `Shapes` library might declare two GUID constants:</span></span>


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



<span data-ttu-id="a4466-143"> (您可以假設這些常數的實際128位數值是在其他地方定義的。 ) 常數 **CLSID \_ 圖形** 可識別 `Shape` 物件，而常數 **IID \_ IDrawable** 則可識別 `IDrawable` 介面。</span><span class="sxs-lookup"><span data-stu-id="a4466-143">(You can assume that the actual 128-bit numeric values for these constants are defined elsewhere.) The constant **CLSID\_Shape** identifies the `Shape` object, while the constant **IID\_IDrawable** identifies the `IDrawable` interface.</span></span> <span data-ttu-id="a4466-144">前置詞 "CLSID" 代表 *類別識別碼*，而前置詞 *IID* 代表 *介面識別碼*。</span><span class="sxs-lookup"><span data-stu-id="a4466-144">The prefix "CLSID" stands for *class identifier*, and the prefix *IID* stands for *interface identifier*.</span></span> <span data-ttu-id="a4466-145">這些是 COM 中的標準命名慣例。</span><span class="sxs-lookup"><span data-stu-id="a4466-145">These are standard naming conventions in COM.</span></span>

<span data-ttu-id="a4466-146">指定這些值之後，您會建立新的實例，如下所示 `Shape` ：</span><span class="sxs-lookup"><span data-stu-id="a4466-146">Given these values, you would create a new `Shape` instance as follows:</span></span>


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="a4466-147">[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)函數有五個參數。</span><span class="sxs-lookup"><span data-stu-id="a4466-147">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function has five parameters.</span></span> <span data-ttu-id="a4466-148">第一個和第四個參數是類別識別碼和介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4466-148">The first and fourth parameters are the class identifier and interface identifier.</span></span> <span data-ttu-id="a4466-149">實際上，這些參數會告訴函式「建立繪圖物件，並提供 IDrawable 介面的指標」。</span><span class="sxs-lookup"><span data-stu-id="a4466-149">In effect, these parameters tell the function, "Create the Shape object, and give me a pointer to the IDrawable interface."</span></span>

<span data-ttu-id="a4466-150">將第二個參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a4466-150">Set the second parameter to **NULL**.</span></span> <span data-ttu-id="a4466-151"> (如需此參數意義的詳細資訊，請參閱 COM 檔集中的主題 [匯總](/windows/desktop/com/aggregation) 。第三個參數 ) 第三個參數會採用一組旗標，其主要目的是要指定物件的 *執行內容* 。</span><span class="sxs-lookup"><span data-stu-id="a4466-151">(For more information about the meaning of this parameter, see the topic [Aggregation](/windows/desktop/com/aggregation) in the COM documentation.) The third parameter takes a set of flags whose main purpose is to specify the *execution context* for the object.</span></span> <span data-ttu-id="a4466-152">執行內容會指定物件是否在與應用程式相同的進程中執行;在同一部電腦的不同處理常式中;或在遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="a4466-152">The execution context specifies whether the object runs in the same process as the application; in a different process on the same computer; or on a remote computer.</span></span> <span data-ttu-id="a4466-153">下表顯示此參數最常用的值。</span><span class="sxs-lookup"><span data-stu-id="a4466-153">The following table shows the most common values for this parameter.</span></span>



| <span data-ttu-id="a4466-154">旗標</span><span class="sxs-lookup"><span data-stu-id="a4466-154">Flag</span></span>                       | <span data-ttu-id="a4466-155">描述</span><span class="sxs-lookup"><span data-stu-id="a4466-155">Description</span></span>                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4466-156">**CLSCTX \_ INPROC \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="a4466-156">**CLSCTX\_INPROC\_SERVER**</span></span> | <span data-ttu-id="a4466-157">相同的進程。</span><span class="sxs-lookup"><span data-stu-id="a4466-157">Same process.</span></span>                                                                                                                                                      |
| <span data-ttu-id="a4466-158">**CLSCTX \_ 本地 \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="a4466-158">**CLSCTX\_LOCAL\_SERVER**</span></span>  | <span data-ttu-id="a4466-159">不同的處理常式，相同的電腦。</span><span class="sxs-lookup"><span data-stu-id="a4466-159">Different process, same computer.</span></span>                                                                                                                                  |
| <span data-ttu-id="a4466-160">**CLSCTX \_ 遠端 \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="a4466-160">**CLSCTX\_REMOTE\_SERVER**</span></span> | <span data-ttu-id="a4466-161">不同的電腦。</span><span class="sxs-lookup"><span data-stu-id="a4466-161">Different computer.</span></span>                                                                                                                                                |
| <span data-ttu-id="a4466-162">**CLSCTX \_ 全部**</span><span class="sxs-lookup"><span data-stu-id="a4466-162">**CLSCTX\_ALL**</span></span>            | <span data-ttu-id="a4466-163">使用物件支援的最有效率選項。</span><span class="sxs-lookup"><span data-stu-id="a4466-163">Use the most efficient option that the object supports.</span></span> <span data-ttu-id="a4466-164">從最有效率到最有效率的等級 (排名是：同進程、跨進程，以及跨電腦。 ) </span><span class="sxs-lookup"><span data-stu-id="a4466-164">(The ranking, from most efficient to least efficient, is: in-process, out-of-process, and cross-computer.)</span></span> |



 

<span data-ttu-id="a4466-165">特定元件的檔可能會告訴您該物件所支援的執行內容。</span><span class="sxs-lookup"><span data-stu-id="a4466-165">The documentation for a particular component might tell you which execution context the object supports.</span></span> <span data-ttu-id="a4466-166">如果不是，請使用 [ **\_ 全部 CLSCTX**]。</span><span class="sxs-lookup"><span data-stu-id="a4466-166">If not, use **CLSCTX\_ALL**.</span></span> <span data-ttu-id="a4466-167">如果您要求物件不支援的執行內容， [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數會傳回錯誤碼 **REGDB \_ E \_ CLASSNOTREG**。</span><span class="sxs-lookup"><span data-stu-id="a4466-167">If you request an execution context that the object does not support, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function returns the error code **REGDB\_E\_CLASSNOTREG**.</span></span> <span data-ttu-id="a4466-168">這個錯誤碼也可以指出 CLSID 沒有對應到使用者電腦上註冊的任何元件。</span><span class="sxs-lookup"><span data-stu-id="a4466-168">This error code can also indicate that the CLSID does not correspond to any component registered on the user's computer.</span></span>

<span data-ttu-id="a4466-169">[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的第五個參數會接收介面指標。</span><span class="sxs-lookup"><span data-stu-id="a4466-169">The fifth parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) receives a pointer to the interface.</span></span> <span data-ttu-id="a4466-170">因為 **CoCreateInstance** 是泛型機制，所以這個參數不能是強型別。</span><span class="sxs-lookup"><span data-stu-id="a4466-170">Because **CoCreateInstance** is a generic mechanism, this parameter cannot be strongly typed.</span></span> <span data-ttu-id="a4466-171">相反地，資料類型為 **void \* \***，而且呼叫端必須將指標的位址強制轉型為 **void \* \*** 型別。</span><span class="sxs-lookup"><span data-stu-id="a4466-171">Instead, the data type is **void\*\***, and the caller must coerce the address of the pointer to a **void\*\*** type.</span></span> <span data-ttu-id="a4466-172">這是在上一個範例中 **重新解譯 \_ 轉換** 的目的。</span><span class="sxs-lookup"><span data-stu-id="a4466-172">That is the purpose of the **reinterpret\_cast** in the previous example.</span></span>

<span data-ttu-id="a4466-173">檢查 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的傳回值是很重要的。</span><span class="sxs-lookup"><span data-stu-id="a4466-173">It is crucial to check the return value of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="a4466-174">如果函式傳回錯誤碼，則 COM 介面指標無效，而嘗試對其進行取值可能會導致您的程式損毀。</span><span class="sxs-lookup"><span data-stu-id="a4466-174">If the function returns an error code, the COM interface pointer is invalid, and attempting to dereference it can cause your program to crash.</span></span>

<span data-ttu-id="a4466-175">就內部而言， [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數會使用各種技術來建立物件。</span><span class="sxs-lookup"><span data-stu-id="a4466-175">Internally, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function uses various techniques to create an object.</span></span> <span data-ttu-id="a4466-176">在最簡單的情況下，它會查閱登錄中的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4466-176">In the simplest case, it looks up the class identifier in the registry.</span></span> <span data-ttu-id="a4466-177">登錄專案會指向用來執行物件的 DLL 或 EXE。</span><span class="sxs-lookup"><span data-stu-id="a4466-177">The registry entry points to a DLL or EXE that implements the object.</span></span> <span data-ttu-id="a4466-178">**CoCreateInstance** 也可以使用 com + 類別目錄中的資訊，或並存的 (SxS) 資訊清單。</span><span class="sxs-lookup"><span data-stu-id="a4466-178">**CoCreateInstance** can also use information from a COM+ catalog or a side-by-side (SxS) manifest.</span></span> <span data-ttu-id="a4466-179">無論何者，詳細資料對呼叫端都是透明的。</span><span class="sxs-lookup"><span data-stu-id="a4466-179">Regardless, the details are transparent to the caller.</span></span> <span data-ttu-id="a4466-180">如需有關 **CoCreateInstance** 內部詳細資料的詳細資訊，請參閱 [COM 用戶端和伺服器](/windows/desktop/com/com-clients-and-servers)。</span><span class="sxs-lookup"><span data-stu-id="a4466-180">For more information about the internal details of **CoCreateInstance**, see [COM Clients and Servers](/windows/desktop/com/com-clients-and-servers).</span></span>

<span data-ttu-id="a4466-181">`Shapes`我們使用的範例有點假設，所以現在讓我們來看看一個實際的 COM 範例：顯示 [**開啟**] 對話方塊，讓使用者選取檔案。</span><span class="sxs-lookup"><span data-stu-id="a4466-181">The `Shapes` example that we have been using is somewhat contrived, so now let's turn to a real-world example of COM in action: displaying the **Open** dialog box for the user to select a file.</span></span>

## <a name="next"></a><span data-ttu-id="a4466-182">下一個</span><span class="sxs-lookup"><span data-stu-id="a4466-182">Next</span></span>

[<span data-ttu-id="a4466-183">範例：開啟對話方塊</span><span class="sxs-lookup"><span data-stu-id="a4466-183">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)

 

 