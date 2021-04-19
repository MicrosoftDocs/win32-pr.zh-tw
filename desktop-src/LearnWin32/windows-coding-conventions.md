---
title: Windows 編碼慣例
description: 如果您是 Windows 程式設計的新手，則在第一次看到 Windows 程式時，可能會令人不安。
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966237"
---
# <a name="windows-coding-conventions"></a><span data-ttu-id="f06c6-103">Windows 編碼慣例</span><span class="sxs-lookup"><span data-stu-id="f06c6-103">Windows Coding Conventions</span></span>

<span data-ttu-id="f06c6-104">如果您是 Windows 程式設計的新手，則在第一次看到 Windows 程式時，可能會令人不安。</span><span class="sxs-lookup"><span data-stu-id="f06c6-104">If you are new to Windows programming, it can be disconcerting when you first see a Windows program.</span></span> <span data-ttu-id="f06c6-105">程式碼會填入奇怪的型別定義，例如 **DWORD \_ PTR** 和 **LPRECT**，而變數的名稱像是 *hWnd* 和 *pwsz* (稱為匈牙利文標記法) 。</span><span class="sxs-lookup"><span data-stu-id="f06c6-105">The code is filled with strange type definitions like **DWORD\_PTR** and **LPRECT**, and variables have names like *hWnd* and *pwsz* (called Hungarian notation).</span></span> <span data-ttu-id="f06c6-106">值得花一點時間學習一些 Windows 程式碼撰寫慣例。</span><span class="sxs-lookup"><span data-stu-id="f06c6-106">It's worth taking a moment to learn some of the Windows coding conventions.</span></span>

<span data-ttu-id="f06c6-107">大部分的 Windows Api 都是由函數或元件物件模型 (COM) 介面所組成。</span><span class="sxs-lookup"><span data-stu-id="f06c6-107">The vast majority of Windows APIs consist of either functions or Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="f06c6-108">許多 Windows Api 都是以 c + + 類別的形式提供。</span><span class="sxs-lookup"><span data-stu-id="f06c6-108">Very few Windows APIs are provided as C++ classes.</span></span> <span data-ttu-id="f06c6-109"> (有個值得注意的例外狀況是 GDI + （2-d 圖形 Api 的其中一個）。 ) </span><span class="sxs-lookup"><span data-stu-id="f06c6-109">(A notable exception is GDI+, one of the 2-D graphics APIs.)</span></span>

## <a name="typedefs"></a><span data-ttu-id="f06c6-110">Typedefs</span><span class="sxs-lookup"><span data-stu-id="f06c6-110">Typedefs</span></span>

<span data-ttu-id="f06c6-111">Windows 標頭包含許多 typedef。</span><span class="sxs-lookup"><span data-stu-id="f06c6-111">The Windows headers contain a lot of typedefs.</span></span> <span data-ttu-id="f06c6-112">其中許多都是在標頭檔 WinDef 中定義。</span><span class="sxs-lookup"><span data-stu-id="f06c6-112">Many of these are defined in the header file WinDef.h.</span></span> <span data-ttu-id="f06c6-113">以下是您經常會遇到的部分。</span><span class="sxs-lookup"><span data-stu-id="f06c6-113">Here are some that you will encounter often.</span></span>

### <a name="integer-types"></a><span data-ttu-id="f06c6-114">整數類型</span><span class="sxs-lookup"><span data-stu-id="f06c6-114">Integer types</span></span>



| <span data-ttu-id="f06c6-115">資料類型</span><span class="sxs-lookup"><span data-stu-id="f06c6-115">Data type</span></span>     | <span data-ttu-id="f06c6-116">大小</span><span class="sxs-lookup"><span data-stu-id="f06c6-116">Size</span></span>    | <span data-ttu-id="f06c6-117">簽署？</span><span class="sxs-lookup"><span data-stu-id="f06c6-117">Signed?</span></span>  |
|---------------|---------|----------|
| <span data-ttu-id="f06c6-118">**BYTE**</span><span class="sxs-lookup"><span data-stu-id="f06c6-118">**BYTE**</span></span>      | <span data-ttu-id="f06c6-119">8 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-119">8 bits</span></span>  | <span data-ttu-id="f06c6-120">不帶正負號</span><span class="sxs-lookup"><span data-stu-id="f06c6-120">Unsigned</span></span> |
| <span data-ttu-id="f06c6-121">**Dword**</span><span class="sxs-lookup"><span data-stu-id="f06c6-121">**DWORD**</span></span>     | <span data-ttu-id="f06c6-122">32 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-122">32 bits</span></span> | <span data-ttu-id="f06c6-123">不帶正負號</span><span class="sxs-lookup"><span data-stu-id="f06c6-123">Unsigned</span></span> |
| <span data-ttu-id="f06c6-124">**時會**</span><span class="sxs-lookup"><span data-stu-id="f06c6-124">**INT32**</span></span>     | <span data-ttu-id="f06c6-125">32 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-125">32 bits</span></span> | <span data-ttu-id="f06c6-126">簽署人</span><span class="sxs-lookup"><span data-stu-id="f06c6-126">Signed</span></span>   |
| <span data-ttu-id="f06c6-127">**INT64**</span><span class="sxs-lookup"><span data-stu-id="f06c6-127">**INT64**</span></span>     | <span data-ttu-id="f06c6-128">64 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-128">64 bits</span></span> | <span data-ttu-id="f06c6-129">簽署人</span><span class="sxs-lookup"><span data-stu-id="f06c6-129">Signed</span></span>   |
| <span data-ttu-id="f06c6-130">**LONG**</span><span class="sxs-lookup"><span data-stu-id="f06c6-130">**LONG**</span></span>      | <span data-ttu-id="f06c6-131">32 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-131">32 bits</span></span> | <span data-ttu-id="f06c6-132">簽署人</span><span class="sxs-lookup"><span data-stu-id="f06c6-132">Signed</span></span>   |
| <span data-ttu-id="f06c6-133">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="f06c6-133">**LONGLONG**</span></span>  | <span data-ttu-id="f06c6-134">64 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-134">64 bits</span></span> | <span data-ttu-id="f06c6-135">簽署人</span><span class="sxs-lookup"><span data-stu-id="f06c6-135">Signed</span></span>   |
| <span data-ttu-id="f06c6-136">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f06c6-136">**UINT32**</span></span>    | <span data-ttu-id="f06c6-137">32 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-137">32 bits</span></span> | <span data-ttu-id="f06c6-138">不帶正負號</span><span class="sxs-lookup"><span data-stu-id="f06c6-138">Unsigned</span></span> |
| <span data-ttu-id="f06c6-139">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f06c6-139">**UINT64**</span></span>    | <span data-ttu-id="f06c6-140">64 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-140">64 bits</span></span> | <span data-ttu-id="f06c6-141">不帶正負號</span><span class="sxs-lookup"><span data-stu-id="f06c6-141">Unsigned</span></span> |
| <span data-ttu-id="f06c6-142">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="f06c6-142">**ULONG**</span></span>     | <span data-ttu-id="f06c6-143">32 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-143">32 bits</span></span> | <span data-ttu-id="f06c6-144">不帶正負號</span><span class="sxs-lookup"><span data-stu-id="f06c6-144">Unsigned</span></span> |
| <span data-ttu-id="f06c6-145">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="f06c6-145">**ULONGLONG**</span></span> | <span data-ttu-id="f06c6-146">64 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-146">64 bits</span></span> | <span data-ttu-id="f06c6-147">不帶正負號</span><span class="sxs-lookup"><span data-stu-id="f06c6-147">Unsigned</span></span> |
| <span data-ttu-id="f06c6-148">**WORD**</span><span class="sxs-lookup"><span data-stu-id="f06c6-148">**WORD**</span></span>      | <span data-ttu-id="f06c6-149">16 位元</span><span class="sxs-lookup"><span data-stu-id="f06c6-149">16 bits</span></span> | <span data-ttu-id="f06c6-150">不帶正負號</span><span class="sxs-lookup"><span data-stu-id="f06c6-150">Unsigned</span></span> |



 

<span data-ttu-id="f06c6-151">如您所見，這些 typedef 中有一定數量的多餘。</span><span class="sxs-lookup"><span data-stu-id="f06c6-151">As you can see, there is a certain amount of redundancy in these typedefs.</span></span> <span data-ttu-id="f06c6-152">這部分重迭只是因為 Windows Api 的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="f06c6-152">Some of this overlap is simply due to the history of the Windows APIs.</span></span> <span data-ttu-id="f06c6-153">此處所列的類型具有固定的大小，在32位和64應用程式中的大小都相同。</span><span class="sxs-lookup"><span data-stu-id="f06c6-153">The types listed here have fixed size, and the sizes are the same in both 32-bit and 64-applications.</span></span> <span data-ttu-id="f06c6-154">例如， **DWORD** 類型一律為32位寬。</span><span class="sxs-lookup"><span data-stu-id="f06c6-154">For example, the **DWORD** type is always 32 bits wide.</span></span>

### <a name="boolean-type"></a><span data-ttu-id="f06c6-155">布林類型</span><span class="sxs-lookup"><span data-stu-id="f06c6-155">Boolean Type</span></span>

<span data-ttu-id="f06c6-156">**BOOL** 是布林值內容中所使用之整數值的 typedef。</span><span class="sxs-lookup"><span data-stu-id="f06c6-156">**BOOL** is a typedef for an integer value that is used in a Boolean context.</span></span> <span data-ttu-id="f06c6-157">標頭檔 WinDef 也會定義兩個搭配 **BOOL** 使用的值。</span><span class="sxs-lookup"><span data-stu-id="f06c6-157">The header file WinDef.h also defines two values for use with **BOOL**.</span></span>


```C++
#define FALSE    0 
#define TRUE     1
```



<span data-ttu-id="f06c6-158">不過，儘管這個定義為 **TRUE**，但傳回 **BOOL** 類型的大部分函式都可以傳回任何非零值以表示布林值。</span><span class="sxs-lookup"><span data-stu-id="f06c6-158">Despite this definition of **TRUE**, however, most functions that return a **BOOL** type can return any non-zero value to indicate Boolean truth.</span></span> <span data-ttu-id="f06c6-159">因此，您應該一律撰寫下列內容：</span><span class="sxs-lookup"><span data-stu-id="f06c6-159">Therefore, you should always write this:</span></span>


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



<span data-ttu-id="f06c6-160">而不是：</span><span class="sxs-lookup"><span data-stu-id="f06c6-160">and not this:</span></span>


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



<span data-ttu-id="f06c6-161">請注意， **BOOL** 是整數型別，而且無法與 c + + **BOOL** 型別互換。</span><span class="sxs-lookup"><span data-stu-id="f06c6-161">Be aware that **BOOL** is an integer type and is not interchangeable with the C++ **bool** type.</span></span>

### <a name="pointer-types"></a><span data-ttu-id="f06c6-162">指標類型</span><span class="sxs-lookup"><span data-stu-id="f06c6-162">Pointer Types</span></span>

<span data-ttu-id="f06c6-163">Windows 定義許多形式的表單 *指標到 X* 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="f06c6-163">Windows defines many data types of the form *pointer-to-X*.</span></span> <span data-ttu-id="f06c6-164">這些通常會在名稱中使用前置詞 *P* 或 *LP* 。</span><span class="sxs-lookup"><span data-stu-id="f06c6-164">These usually have the prefix *P-* or *LP-* in the name.</span></span> <span data-ttu-id="f06c6-165">例如， **LPRECT** [**是矩形的指標，其中**](/previous-versions//dd162897(v=vs.85)) **rect** 是描述矩形的結構。</span><span class="sxs-lookup"><span data-stu-id="f06c6-165">For example, **LPRECT** is a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)), where **RECT** is a structure that describes a rectangle.</span></span> <span data-ttu-id="f06c6-166">下列變數宣告是相等的。</span><span class="sxs-lookup"><span data-stu-id="f06c6-166">The following variable declarations are equivalent.</span></span>


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



<span data-ttu-id="f06c6-167">在過去， *P* 代表「指標」，而 *LP* 代表「長指標」。</span><span class="sxs-lookup"><span data-stu-id="f06c6-167">Historically, *P* stands for "pointer" and *LP* stands for "long pointer".</span></span> <span data-ttu-id="f06c6-168">長指標 (也稱為 *遠指標*) 是從16位 Windows holdover 的指標，當需要這些指標來處理目前區段之外的記憶體範圍時。</span><span class="sxs-lookup"><span data-stu-id="f06c6-168">Long pointers (also called *far pointers*) are a holdover from 16-bit Windows, when they were needed to address memory ranges outside the current segment.</span></span> <span data-ttu-id="f06c6-169">已保留 *LP* 前置詞，可讓您更輕鬆地將16位程式碼移植到32位 Windows。</span><span class="sxs-lookup"><span data-stu-id="f06c6-169">The *LP* prefix was preserved to make it easier to port 16-bit code to 32-bit Windows.</span></span> <span data-ttu-id="f06c6-170">今天沒有任何差別，指標就是指標。</span><span class="sxs-lookup"><span data-stu-id="f06c6-170">Today there is no distinction — a pointer is a pointer.</span></span>

### <a name="pointer-precision-types"></a><span data-ttu-id="f06c6-171">指標精確度類型</span><span class="sxs-lookup"><span data-stu-id="f06c6-171">Pointer Precision Types</span></span>

<span data-ttu-id="f06c6-172">下列資料類型一律是指標的大小，也就是32位應用程式中的32位寬，以及64位應用程式中的64位寬。</span><span class="sxs-lookup"><span data-stu-id="f06c6-172">The following data types are always the size of a pointer—that is, 32 bits wide in 32-bit applications, and 64 bits wide in 64-bit applications.</span></span> <span data-ttu-id="f06c6-173">大小是在編譯時期決定。</span><span class="sxs-lookup"><span data-stu-id="f06c6-173">The size is determined at compile time.</span></span> <span data-ttu-id="f06c6-174">當32位應用程式在64位的 Windows 上執行時，這些資料類型仍然是4個位元組寬。</span><span class="sxs-lookup"><span data-stu-id="f06c6-174">When a 32-bit application runs on 64-bit Windows, these data types are still 4 bytes wide.</span></span> <span data-ttu-id="f06c6-175"> (64 位應用程式無法在32位的 Windows 上執行，因此不會發生反向的情況。 ) </span><span class="sxs-lookup"><span data-stu-id="f06c6-175">(A 64-bit application cannot run on 32-bit Windows, so the reverse situation does not occur.)</span></span>

-   <span data-ttu-id="f06c6-176">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="f06c6-176">**DWORD\_PTR**</span></span>
-   <span data-ttu-id="f06c6-177">**INT \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="f06c6-177">**INT\_PTR**</span></span>
-   <span data-ttu-id="f06c6-178">**長 \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="f06c6-178">**LONG\_PTR**</span></span>
-   <span data-ttu-id="f06c6-179">**ULONG \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="f06c6-179">**ULONG\_PTR**</span></span>
-   <span data-ttu-id="f06c6-180">**UINT \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="f06c6-180">**UINT\_PTR**</span></span>

<span data-ttu-id="f06c6-181">這些類型會在整數可能轉換成指標的情況下使用。</span><span class="sxs-lookup"><span data-stu-id="f06c6-181">These types are used in situations where an integer might be cast to a pointer.</span></span> <span data-ttu-id="f06c6-182">它們也可用來定義指標算術的變數，以及定義迴圈計數器，以逐一查看記憶體緩衝區中的完整位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="f06c6-182">They are also used to define variables for pointer arithmetic and to define loop counters that iterate over the full range of bytes in memory buffers.</span></span> <span data-ttu-id="f06c6-183">更常見的情況是，它們會出現在現有32位值在64位 Windows 上擴充至64位的位置。</span><span class="sxs-lookup"><span data-stu-id="f06c6-183">More generally, they appear in places where an existing 32-bit value was expanded to 64 bits on 64-bit Windows.</span></span>

## <a name="hungarian-notation"></a><span data-ttu-id="f06c6-184">匈牙利文標記法</span><span class="sxs-lookup"><span data-stu-id="f06c6-184">Hungarian Notation</span></span>

<span data-ttu-id="f06c6-185">*匈牙利文標記法* 是將前置詞新增至變數名稱的做法，以提供變數的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f06c6-185">*Hungarian notation* is the practice of adding prefixes to the names of variables, to give additional information about the variable.</span></span> <span data-ttu-id="f06c6-186"> (標記法的發明者（Charles Simonyi）是匈牙利文，因此其名稱) 。</span><span class="sxs-lookup"><span data-stu-id="f06c6-186">(The notation's inventor, Charles Simonyi, was Hungarian, hence its name).</span></span>

<span data-ttu-id="f06c6-187">在其原始形式中，匈牙利文標記法會提供變數的相關 *語義* 資訊，告訴您預期的用途。</span><span class="sxs-lookup"><span data-stu-id="f06c6-187">In its original form, Hungarian notation gives *semantic* information about a variable, telling you the intended use.</span></span> <span data-ttu-id="f06c6-188">例如， *i* 表示索引， *cb* 表示以位元組為單位的大小 ( 「位元組計數」 ) ，以及 *rw* 和資料行 *的平均資料* 列和資料行數目。</span><span class="sxs-lookup"><span data-stu-id="f06c6-188">For example, *i* means an index, *cb* means a size in bytes ("count of bytes"), and *rw* and *col* mean row and column numbers.</span></span> <span data-ttu-id="f06c6-189">這些前置詞的設計目的是為了避免在錯誤的內容中意外使用變數。</span><span class="sxs-lookup"><span data-stu-id="f06c6-189">These prefixes are designed to avoid the accidental use of a variable in the wrong context.</span></span> <span data-ttu-id="f06c6-190">例如，如果您看到運算式 `rwPosition +  cbTable` ，您會知道將資料列編號加入至大小，這在程式碼中幾乎肯定是錯誤的</span><span class="sxs-lookup"><span data-stu-id="f06c6-190">For example, if you saw the expression `rwPosition +  cbTable`, you would know that a row number is being added to a size, which is almost certainly a bug in the code</span></span>

<span data-ttu-id="f06c6-191">比較常見的匈牙利文標記法會使用前置詞來提供 *類型* 資訊，例如 *dw* for **DWORD** 和 *w* for **WORD**。</span><span class="sxs-lookup"><span data-stu-id="f06c6-191">A more common form of Hungarian notation uses prefixes to give *type* information—for example, *dw* for **DWORD** and *w* for **WORD**.</span></span>

<span data-ttu-id="f06c6-192">如果您在網路上搜尋「匈牙利文標記法」，您會發現有關匈牙利文標記法是否正確或不正確的許多意見。</span><span class="sxs-lookup"><span data-stu-id="f06c6-192">If you search the Web for "Hungarian notation," you will find a lot of opinions about whether Hungarian notation is good or bad.</span></span> <span data-ttu-id="f06c6-193">某些程式設計人員對於匈牙利文標記法的不喜歡。</span><span class="sxs-lookup"><span data-stu-id="f06c6-193">Some programmers have an intense dislike for Hungarian notation.</span></span> <span data-ttu-id="f06c6-194">其他人覺得很有用。</span><span class="sxs-lookup"><span data-stu-id="f06c6-194">Others find it helpful.</span></span> <span data-ttu-id="f06c6-195">無論如何，MSDN 上的許多程式碼範例都使用匈牙利文標記法，但您不需要記住首碼來瞭解程式碼。</span><span class="sxs-lookup"><span data-stu-id="f06c6-195">Regardless, many of the code examples on MSDN use Hungarian notation, but you don't need to memorize the prefixes to understand the code.</span></span>

## <a name="next"></a><span data-ttu-id="f06c6-196">下一個</span><span class="sxs-lookup"><span data-stu-id="f06c6-196">Next</span></span>

[<span data-ttu-id="f06c6-197">使用字串</span><span class="sxs-lookup"><span data-stu-id="f06c6-197">Working with Strings</span></span>](working-with-strings.md)

 

 