---
title: 使用指標的規則
description: 將您的程式碼移植到適用于32和64位 Microsoft Windows 的程式碼很簡單。 您只需要遵循一些有關轉換指標的簡單規則，並在您的程式碼中使用新的資料類型。 指標操作的規則如下所示。
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- 使用指標64位 Windows 程式設計的規則
- 指標操作 64-位 Windows 程式設計
- 轉換指標64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103933683"
---
# <a name="rules-for-using-pointers"></a><span data-ttu-id="ef3b2-108">使用指標的規則</span><span class="sxs-lookup"><span data-stu-id="ef3b2-108">Rules for Using Pointers</span></span>

<span data-ttu-id="ef3b2-109">將您的程式碼移植到適用于32和64位 Microsoft Windows 的程式碼很簡單。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-109">Porting your code to compile for both 32- and 64-bit Microsoft Windows is straightforward.</span></span> <span data-ttu-id="ef3b2-110">您只需要遵循一些有關轉換指標的簡單規則，並在您的程式碼中使用新的資料類型。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-110">You need only follow a few simple rules about casting pointers, and use the new data types in your code.</span></span> <span data-ttu-id="ef3b2-111">指標操作的規則如下所示。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-111">The rules for pointer manipulation are as follows.</span></span>

1.  <span data-ttu-id="ef3b2-112">請勿將指標轉換成 **int**、 **long**、 **ULONG** 或 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-112">Do not cast pointers to **int**, **long**, **ULONG**, or **DWORD**.</span></span>

    <span data-ttu-id="ef3b2-113">如果您必須轉換指標以測試部分位、設定或清除位，或以其他方式操作其內容，請使用 **UINT \_ PTR** 或 **INT \_ ptr** 類型。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-113">If you must cast a pointer to test some bits, set or clear bits, or otherwise manipulate its contents, use the **UINT\_PTR** or **INT\_PTR** type.</span></span> <span data-ttu-id="ef3b2-114">這些型別是一種整數類資料類型，可調整為32和64位 Windows (的指標大小，例如， **ULONG** （32）位 windows，以及 \_ 64 位 windows) 的 int64。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-114">These types are integral types that scale to the size of a pointer for both 32- and 64-bit Windows (for example, **ULONG** for 32-bit Windows and \_int64 for 64-bit Windows).</span></span> <span data-ttu-id="ef3b2-115">例如，假設您正在移植下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="ef3b2-115">For example, assume you are porting the following code:</span></span>

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    <span data-ttu-id="ef3b2-116">作為移植程式的一部分，您可以變更程式碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ef3b2-116">As a part of the porting process, you would change the code as follows:</span></span>

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    <span data-ttu-id="ef3b2-117">如果有適當的 (，請使用 **UINT \_ Ptr** 和 **INT \_ ptr** ，如果您不確定是否需要，則在) 的情況下使用它們就不會有任何傷害。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-117">Use **UINT\_PTR** and **INT\_PTR** where appropriate (and if you are uncertain whether they are required, there is no harm in using them just in case).</span></span> <span data-ttu-id="ef3b2-118">請勿將指標轉換為 **ULONG**、 **LONG**、 **INT**、 **UINT** 或 **DWORD** 類型。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-118">Do not cast your pointers to the types **ULONG**, **LONG**, **INT**, **UINT**, or **DWORD**.</span></span>

    <span data-ttu-id="ef3b2-119">請注意，**控制碼** 定義為 **void \***，因此將句 **柄** 值 typecasting 為 **ULONG** 值以測試、設定或清除低序位2位是64位 Windows 上的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-119">Note that **HANDLE** is defined as a **void\***, so typecasting a **HANDLE** value to a **ULONG** value to test, set, or clear the low-order 2 bits is an error on 64-bit Windows.</span></span>

2.  <span data-ttu-id="ef3b2-120">使用 **PtrToLong** 或 **PtrToUlong** 函式來截斷指標。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-120">Use the **PtrToLong** or **PtrToUlong** function to truncate pointers.</span></span>

    <span data-ttu-id="ef3b2-121">如果您必須截斷32位值的指標，請使用 (在 Basetsd 中定義的 **PtrToLong** 或 **PtrToUlong** 函數) 。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-121">If you must truncate a pointer to a 32-bit value, use the **PtrToLong** or **PtrToUlong** function (defined in Basetsd.h).</span></span> <span data-ttu-id="ef3b2-122">這些函數會在呼叫期間停用指標截斷警告。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-122">These functions disable the pointer truncation warning for the duration of the call.</span></span>

    <span data-ttu-id="ef3b2-123">請小心使用這些函數。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-123">Use these functions carefully.</span></span> <span data-ttu-id="ef3b2-124">當您使用這些函式的其中一個來轉換指標變數之後，請不要再使用它做為指標。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-124">After you convert a pointer variable using one of these functions, never use it as a pointer again.</span></span> <span data-ttu-id="ef3b2-125">這些函式會截斷位址的前32位，通常是存取指標最初參考的記憶體所需的部分。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-125">These functions truncate the upper 32 bits of an address, which are usually needed to access the memory originally referenced by pointer.</span></span> <span data-ttu-id="ef3b2-126">使用這些函式而不謹慎考慮將會產生脆弱的程式碼。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-126">Using these functions without careful consideration will result in fragile code.</span></span>

3.  <span data-ttu-id="ef3b2-127">\_在程式碼中使用可以編譯為64位程式碼的指標32值時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-127">Be careful when using POINTER\_32 values in code that may be compiled as 64-bit code.</span></span> <span data-ttu-id="ef3b2-128">當指標指派給64位程式碼中的原生指標，而不是以零擴充指標時，編譯器將會簽署並擴充指標。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-128">The compiler will sign-extend the pointer when it is assigned to a native pointer in 64-bit code, not zero-extend the pointer.</span></span>
4.  <span data-ttu-id="ef3b2-129">\_在程式碼中使用可以編譯為32位程式碼的指標64值時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-129">Be careful when using POINTER\_64 values in code that may be compiled as 32-bit code.</span></span> <span data-ttu-id="ef3b2-130">編譯器會在32位程式碼中簽署並擴充指標，而不是以零擴充指標。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-130">The compiler will sign-extend the pointer in 32-bit code, not zero-extend the pointer.</span></span>
5.  <span data-ttu-id="ef3b2-131">請小心使用 OUT 參數。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-131">Be careful using OUT parameters.</span></span>

    <span data-ttu-id="ef3b2-132">例如，假設您有定義如下的函數：</span><span class="sxs-lookup"><span data-stu-id="ef3b2-132">For example, suppose you have a function defined as follows:</span></span>

    `void func( OUT PULONG *PointerToUlong );`

    <span data-ttu-id="ef3b2-133">請勿呼叫此函數，如下所示。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-133">Do not call this function as follows.</span></span>

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    <span data-ttu-id="ef3b2-134">請改用下列呼叫。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-134">Instead, use the following call.</span></span>

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    <span data-ttu-id="ef3b2-135">Typecasting &ul to **PULONG \*** 可以防止編譯器錯誤，但函式會將64位指標值寫入 &ul 的記憶體中。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-135">Typecasting &ul to **PULONG\*** prevents a compiler error, but the function will write a 64-bit pointer value into the memory at &ul.</span></span> <span data-ttu-id="ef3b2-136">這段程式碼適用于32位的 Windows，但會導致64位 Windows 的資料損毀，而這會是很微妙、難以發現的損毀。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-136">This code works on 32-bit Windows, but will cause data corruption on 64-bit Windows and it will be subtle, hard-to-find corruption.</span></span> <span data-ttu-id="ef3b2-137">最下面的程式程式碼：不使用 C 程式碼玩訣竅，簡單明瞭。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-137">The bottom line: Do not play tricks with the C code—straightforward and simple is better.</span></span>

6.  <span data-ttu-id="ef3b2-138">使用多型介面時請小心。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-138">Be careful with polymorphic interfaces.</span></span>

    <span data-ttu-id="ef3b2-139">請勿建立接受多型資料之 **DWORD** 參數的函數。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-139">Do not create functions that accept **DWORD** parameters for polymorphic data.</span></span> <span data-ttu-id="ef3b2-140">如果資料可以是指標或整數值，請使用 UINT \_ PTR 或 **PVOID** 類型。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-140">If the data can be a pointer or an integral value, use the UINT\_PTR or **PVOID** type.</span></span>

    <span data-ttu-id="ef3b2-141">例如，請勿建立接受型別為 **DWORD** 值之例外狀況參數陣列的函式。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-141">For example, do not create a function that accepts an array of exception parameters typed as **DWORD** values.</span></span> <span data-ttu-id="ef3b2-142">陣列應為 **DWORD \_ PTR** 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-142">The array should be an array of **DWORD\_PTR** values.</span></span> <span data-ttu-id="ef3b2-143">因此，陣列元素可以保留位址或32位整數值。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-143">Therefore, the array elements can hold addresses or 32-bit integral values.</span></span> <span data-ttu-id="ef3b2-144"> (一般規則是，如果原始型別是 **DWORD** ，而且必須是指標寬度，請將它轉換成 **DWORD \_ 指標** 值。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-144">(The general rule is that if the original type is **DWORD** and it needs to be pointer width, convert it to a **DWORD\_PTR** value.</span></span> <span data-ttu-id="ef3b2-145">這就是為什麼有對應的指標精確度型別。 ) 如果您的程式碼使用 **DWORD**、 **ULONG** 或其他32位類型的多型方法， (也就是說，您真的希望參數或結構成員保留位址) ，請使用 **UINT \_ PTR** 來取代目前的型別。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-145">That is why there are corresponding pointer-precision types.) If you have code that uses **DWORD**, **ULONG**, or other 32-bit types in a polymorphic way (that is, you really want the parameter or structure member to hold an address), use **UINT\_PTR** in place of the current type.</span></span>

7.  <span data-ttu-id="ef3b2-146">使用新的視窗類別函數。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-146">Use the new window class functions.</span></span>

    <span data-ttu-id="ef3b2-147">如果您有包含指標的視窗或類別私用資料，您的程式碼將需要使用下列新函數：</span><span class="sxs-lookup"><span data-stu-id="ef3b2-147">If you have window or class private data that contains pointers, your code will need to use the following new functions:</span></span>

    -   [<span data-ttu-id="ef3b2-148">**GetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="ef3b2-148">**GetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [<span data-ttu-id="ef3b2-149">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="ef3b2-149">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [<span data-ttu-id="ef3b2-150">**SetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="ef3b2-150">**SetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [<span data-ttu-id="ef3b2-151">**SetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="ef3b2-151">**SetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    <span data-ttu-id="ef3b2-152">這些函式可用於 32-和64位的 Windows，但它們在64位的 Windows 上是必要的。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-152">These functions can be used on both 32- and 64-bit Windows, but they are required on 64-bit Windows.</span></span> <span data-ttu-id="ef3b2-153">立即使用這些功能來準備轉換。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-153">Prepare for the transition by using these functions now.</span></span>

    <span data-ttu-id="ef3b2-154">此外，您必須使用64位 Windows 上的新函數，來存取類別私用資料中的指標或控制碼。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-154">Additionally, you must access pointers or handles in class private data using the new functions on 64-bit Windows.</span></span> <span data-ttu-id="ef3b2-155">為了協助您找出這些情況，在64位編譯期間，Winuser 中不會定義下列索引：</span><span class="sxs-lookup"><span data-stu-id="ef3b2-155">To aid you in finding these cases, the following indexes are not defined in Winuser.h during a 64-bit compile:</span></span>

    -   <span data-ttu-id="ef3b2-156">GWL \_ WNDPROC</span><span class="sxs-lookup"><span data-stu-id="ef3b2-156">GWL\_WNDPROC</span></span>
    -   <span data-ttu-id="ef3b2-157">GWL \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef3b2-157">GWL\_HINSTANCE</span></span>
    -   <span data-ttu-id="ef3b2-158">GWL \_ HWDPARENT</span><span class="sxs-lookup"><span data-stu-id="ef3b2-158">GWL\_HWDPARENT</span></span>
    -   <span data-ttu-id="ef3b2-159">GWL \_ USERDATA</span><span class="sxs-lookup"><span data-stu-id="ef3b2-159">GWL\_USERDATA</span></span>

    <span data-ttu-id="ef3b2-160">相反地，Winuser 會定義下列新的索引：</span><span class="sxs-lookup"><span data-stu-id="ef3b2-160">Instead, Winuser.h defines the following new indexes:</span></span>

    -   <span data-ttu-id="ef3b2-161">GWLP \_ WNDPROC</span><span class="sxs-lookup"><span data-stu-id="ef3b2-161">GWLP\_WNDPROC</span></span>
    -   <span data-ttu-id="ef3b2-162">GWLP \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef3b2-162">GWLP\_HINSTANCE</span></span>
    -   <span data-ttu-id="ef3b2-163">GWLP \_ HWNDPARENT</span><span class="sxs-lookup"><span data-stu-id="ef3b2-163">GWLP\_HWNDPARENT</span></span>
    -   <span data-ttu-id="ef3b2-164">GWLP \_ USERDATA</span><span class="sxs-lookup"><span data-stu-id="ef3b2-164">GWLP\_USERDATA</span></span>
    -   <span data-ttu-id="ef3b2-165">GWLP \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="ef3b2-165">GWLP\_ID</span></span>

    <span data-ttu-id="ef3b2-166">例如，下列程式碼不會進行編譯：</span><span class="sxs-lookup"><span data-stu-id="ef3b2-166">For example, the following code does not compile:</span></span>

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    <span data-ttu-id="ef3b2-167">其應如下變更：</span><span class="sxs-lookup"><span data-stu-id="ef3b2-167">It should be changed as follows:</span></span>

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    <span data-ttu-id="ef3b2-168">設定 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **cbWndExtra** 成員時，請務必為指標保留足夠的空間。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-168">When setting the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure, be sure to reserve enough space for pointers.</span></span> <span data-ttu-id="ef3b2-169">例如，如果您目前為指標值保留 sizeof (DWORD) 個位元組，請保留 sizeof (DWORD \_ PTR) 位元組。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-169">For example, if you are currently reserving sizeof(DWORD) bytes for a pointer value, reserve sizeof(DWORD\_PTR) bytes.</span></span>

8.  <span data-ttu-id="ef3b2-170">使用 **欄位 \_ 位移** 存取所有視窗和類別資料。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-170">Access all window and class data using **FIELD\_OFFSET**.</span></span>

    <span data-ttu-id="ef3b2-171">使用硬式編碼的位移來存取視窗資料是很常見的。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-171">It is common to access window data using hard-coded offsets.</span></span> <span data-ttu-id="ef3b2-172">這項技術無法移植到64位的 Windows。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-172">This technique is not portable to 64-bit Windows.</span></span> <span data-ttu-id="ef3b2-173">若要讓您的程式碼可移植，請使用 **欄位 \_ 位移** 宏來存取視窗和類別資料。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-173">To make your code portable, access your window and class data using the **FIELD\_OFFSET** macro.</span></span> <span data-ttu-id="ef3b2-174">請勿假設第二個指標的位移為4。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-174">Do not assume that the second pointer has an offset of 4.</span></span>

9.  <span data-ttu-id="ef3b2-175">**LPARAM**、 **WPARAM** 和 **LRESULT** 類型會變更平臺的大小。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-175">The **LPARAM**, **WPARAM**, and **LRESULT** types change size with the platform.</span></span>

    <span data-ttu-id="ef3b2-176">編譯64位程式碼時，這些類型會擴充至64位，因為它們通常會保留指標或整數類型。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-176">When compiling 64-bit code, these types expand to 64 bits, because they typically hold pointers or integral types.</span></span> <span data-ttu-id="ef3b2-177">請勿將這些值與 **DWORD**、 **ULONG**、 **UINT**、 **int**、 **int** 或 **long** 值混合。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-177">Do not mix these values with **DWORD**, **ULONG**, **UINT**, **INT**, **int**, or **long** values.</span></span> <span data-ttu-id="ef3b2-178">檢查您如何使用這些類型，並確保不會不慎截斷值。</span><span class="sxs-lookup"><span data-stu-id="ef3b2-178">Examine how you use these types and ensure that you do not inadvertently truncate values.</span></span>

 

 