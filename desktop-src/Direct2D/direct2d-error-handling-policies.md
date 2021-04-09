---
title: Direct2D 錯誤處理原則
description: 本主題說明 Direct2D 錯誤處理原則。 包含以下幾節。
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D，錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933523"
---
# <a name="direct2d-error-handling-policies"></a><span data-ttu-id="f9383-105">Direct2D 錯誤處理原則</span><span class="sxs-lookup"><span data-stu-id="f9383-105">Direct2D Error Handling Policies</span></span>

<span data-ttu-id="f9383-106">本主題說明 Direct2D 錯誤處理原則。</span><span class="sxs-lookup"><span data-stu-id="f9383-106">This topic describes the Direct2D error handling policies.</span></span> <span data-ttu-id="f9383-107">包含以下幾節。</span><span class="sxs-lookup"><span data-stu-id="f9383-107">It contains the following sections.</span></span>

-   [<span data-ttu-id="f9383-108">使用 HRESULT</span><span class="sxs-lookup"><span data-stu-id="f9383-108">Use of HRESULT</span></span>](#use-of-hresult)
-   [<span data-ttu-id="f9383-109">批次函數的傳回值</span><span class="sxs-lookup"><span data-stu-id="f9383-109">Return Value of Batched Functions</span></span>](#return-value-of-batched-functions)
-   [<span data-ttu-id="f9383-110">輸入無效</span><span class="sxs-lookup"><span data-stu-id="f9383-110">Invalid Input</span></span>](#invalid-input)
    -   [<span data-ttu-id="f9383-111">Output 指標</span><span class="sxs-lookup"><span data-stu-id="f9383-111">Output Pointer</span></span>](#output-pointer)
    -   [<span data-ttu-id="f9383-112">必要參數</span><span class="sxs-lookup"><span data-stu-id="f9383-112">Required Parameter</span></span>](#required-parameter)
-   [<span data-ttu-id="f9383-113">NaN 和排序不正確的輸入矩形</span><span class="sxs-lookup"><span data-stu-id="f9383-113">NaN and Poorly Ordered Input RECTs</span></span>](#nan-and-poorly-ordered-input-rects)
    -   [<span data-ttu-id="f9383-114">NaN 作為輸入</span><span class="sxs-lookup"><span data-stu-id="f9383-114">NaN as Input</span></span>](#nan-as-input)
    -   [<span data-ttu-id="f9383-115">排序不正確的輸入矩形</span><span class="sxs-lookup"><span data-stu-id="f9383-115">Poorly Ordered Input RECTs</span></span>](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a><span data-ttu-id="f9383-116">使用 HRESULT</span><span class="sxs-lookup"><span data-stu-id="f9383-116">Use of HRESULT</span></span>

<span data-ttu-id="f9383-117">如果函式未批次處理，而且可能有運行時失敗，則應該傳回 **HRESULT** 以表示失敗。</span><span class="sxs-lookup"><span data-stu-id="f9383-117">If a function is not batched and can have a run-time failure, it should return **HRESULT** to indicate a failure.</span></span> <span data-ttu-id="f9383-118">執行時間失敗是在設計階段無法避免的任何失敗，例如記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="f9383-118">A run-time failure is any failure that cannot be avoided at design time, such as out of memory.</span></span>

## <a name="return-value-of-batched-functions"></a><span data-ttu-id="f9383-119">批次函數的傳回值</span><span class="sxs-lookup"><span data-stu-id="f9383-119">Return Value of Batched Functions</span></span>

<span data-ttu-id="f9383-120">Direct2D 中的批次函式是在呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) 時，以單一單位處理的函式。</span><span class="sxs-lookup"><span data-stu-id="f9383-120">Batched functions in Direct2D are the functions that are processed as a single unit when [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) is called.</span></span> <span data-ttu-id="f9383-121">它們是 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 和 **EndDraw** 之間的繪圖命令，或 [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)上的命令。</span><span class="sxs-lookup"><span data-stu-id="f9383-121">They are the drawing commands between [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw** or commands on [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="f9383-122">針對這些函式，會在批次完成時回報錯誤。</span><span class="sxs-lookup"><span data-stu-id="f9383-122">For these functions, errors are reported at the time the batch is completed.</span></span> <span data-ttu-id="f9383-123">在 **EndDraw** 以繪製命令之後，以及在 **關閉** **GeometrySink** 之後，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f9383-123">The error is returned after **EndDraw** for drawing commands, and after **Close** for **GeometrySink**.</span></span>

<span data-ttu-id="f9383-124">如果已設定錯誤狀態，RenderTargets 停止繪圖，但是應用程式可以呼叫 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 來重設錯誤狀態並繼續繪製。</span><span class="sxs-lookup"><span data-stu-id="f9383-124">RenderTargets stop drawing if an error state is set, but an application can call [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) to reset the error state and resume drawing.</span></span>

<span data-ttu-id="f9383-125">**Get** 和 **Set** 函數沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="f9383-125">**Get** and **Set** functions have no return value.</span></span> <span data-ttu-id="f9383-126">但是，如果 **Set** 函數有不正確輸入，debug 層會產生訊息。</span><span class="sxs-lookup"><span data-stu-id="f9383-126">However, if a **Set** function has an invalid input, the debug layer generates a message.</span></span> <span data-ttu-id="f9383-127">在此情況下，不會設定任何錯誤狀態，且 **set** 函數不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="f9383-127">In this case, no error state is set and the **Set** function does nothing.</span></span>

## <a name="invalid-input"></a><span data-ttu-id="f9383-128">輸入無效</span><span class="sxs-lookup"><span data-stu-id="f9383-128">Invalid Input</span></span>

<span data-ttu-id="f9383-129">Direct2D 會在指標無效或 **為 Null** 時，取值會導致存取違規的輸出指標和必要參數。</span><span class="sxs-lookup"><span data-stu-id="f9383-129">Direct2D dereferences output pointers and required parameters which result in access violations when the pointers are invalid or **NULL**.</span></span>

### <a name="output-pointer"></a><span data-ttu-id="f9383-130">Output 指標</span><span class="sxs-lookup"><span data-stu-id="f9383-130">Output Pointer</span></span>

<span data-ttu-id="f9383-131">Direct2D 會在輸入函式時，對輸出指標進行取值，並立即將其指派給 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f9383-131">Direct2D dereferences an output pointer and assigns it to **NULL** immediately upon entering the function.</span></span> <span data-ttu-id="f9383-132">如果呼叫端傳入 **Null** 做為傳回值的指標，這會造成存取違規。</span><span class="sxs-lookup"><span data-stu-id="f9383-132">This causes an access violation if a caller passes in **NULL** as the pointer to the return value.</span></span> <span data-ttu-id="f9383-133">這項原則也適用于指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="f9383-133">This policy also applies to arrays of pointers.</span></span> <span data-ttu-id="f9383-134">針對其他輸出參數（例如結構），會在稍後進行取值，而且會導致存取違規。</span><span class="sxs-lookup"><span data-stu-id="f9383-134">For other output parameters, such as a struct, the dereference happens later and also results in an access violation.</span></span> <span data-ttu-id="f9383-135">不過，有一些方法會有選擇性的輸出指標 (也就是 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)、 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) 不會造成存取違規。</span><span class="sxs-lookup"><span data-stu-id="f9383-135">However, there are some methods that have optional output pointers (that is, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) that will not cause an access violation.</span></span>

### <a name="required-parameter"></a><span data-ttu-id="f9383-136">必要參數</span><span class="sxs-lookup"><span data-stu-id="f9383-136">Required Parameter</span></span>

<span data-ttu-id="f9383-137">如果將 **Null** 傳遞給任何需要有效值的函式，則函式會提早對錯誤指標進行取值，而導致存取違規。</span><span class="sxs-lookup"><span data-stu-id="f9383-137">If **NULL** is passed to any function requiring a valid value, the function dereferences the bad pointer early resulting in an access violation.</span></span> <span data-ttu-id="f9383-138">對於選擇性的輸入參數， **Null** 是有效的值，會產生一些合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="f9383-138">For optional input parameters, **NULL** is a valid value that results in some reasonable default.</span></span>

## <a name="nan-and-poorly-ordered-input-rects"></a><span data-ttu-id="f9383-139">NaN 和排序不正確的輸入矩形</span><span class="sxs-lookup"><span data-stu-id="f9383-139">NaN and Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="f9383-140">在 Direct2D 中，會將 NaN 視為有效的輸入，且排序不正確的輸入矩形。</span><span class="sxs-lookup"><span data-stu-id="f9383-140">In Direct2D, NaN is considered a valid input and poorly ordered input RECTs are sorted.</span></span>

### <a name="nan-as-input"></a><span data-ttu-id="f9383-141">NaN 作為輸入</span><span class="sxs-lookup"><span data-stu-id="f9383-141">NaN as Input</span></span>

<span data-ttu-id="f9383-142">NaN 會被視為有效的輸入，不過它通常會導致包含 NaN 未繪製的基本類型。</span><span class="sxs-lookup"><span data-stu-id="f9383-142">NaN is considered a valid input, though it typically results in the primitive that contains the NaN not drawing.</span></span> <span data-ttu-id="f9383-143">Direct2D API 不會提供 NaN 的明確篩選來驗證輸入。</span><span class="sxs-lookup"><span data-stu-id="f9383-143">The Direct2D API does not provide explicit filtering of NaN to validate input.</span></span>

### <a name="poorly-ordered-input-rects"></a><span data-ttu-id="f9383-144">排序不正確的輸入矩形</span><span class="sxs-lookup"><span data-stu-id="f9383-144">Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="f9383-145">排序不正確的輸入矩形會進行排序，以便正確地指定頂端、左方和右下角。</span><span class="sxs-lookup"><span data-stu-id="f9383-145">Poorly ordered input RECTs are sorted so that the top, left and bottom, right corners are correctly specified.</span></span> <span data-ttu-id="f9383-146">針對輸出，空的矩形看起來像這樣： {無限大、無限大、FloatMax、FloatMax}。</span><span class="sxs-lookup"><span data-stu-id="f9383-146">For output, empty rectangles look like this: {Infinity, Infinity, FloatMax, FloatMax}.</span></span>

 

 