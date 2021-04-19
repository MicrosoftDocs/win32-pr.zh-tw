---
title: 其他考量
description: 移植您的程式碼時，請考慮下列幾點。
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- 移植提示 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "107000640"
---
# <a name="additional-considerations"></a><span data-ttu-id="0c052-104">其他考量</span><span class="sxs-lookup"><span data-stu-id="0c052-104">Additional Considerations</span></span>

<span data-ttu-id="0c052-105">移植您的程式碼時，請考慮下列幾點：</span><span class="sxs-lookup"><span data-stu-id="0c052-105">When porting your code, consider the following points:</span></span>

- <span data-ttu-id="0c052-106">下列假設已不再有效：</span><span class="sxs-lookup"><span data-stu-id="0c052-106">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   <span data-ttu-id="0c052-107">不過，64位編譯器會定義 \_ WIN32 以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="0c052-107">However, the 64-bit compiler defines \_WIN32 for backward compatibility.</span></span>

- <span data-ttu-id="0c052-108">下列假設已不再有效：</span><span class="sxs-lookup"><span data-stu-id="0c052-108">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   <span data-ttu-id="0c052-109">在此情況下，else 子句可代表 \_ WIN32 或 \_ WIN64。</span><span class="sxs-lookup"><span data-stu-id="0c052-109">In this case, the else clause can represent \_WIN32 or \_WIN64.</span></span>

- <span data-ttu-id="0c052-110">請小心使用資料類型對齊。</span><span class="sxs-lookup"><span data-stu-id="0c052-110">Be careful with data-type alignment.</span></span> <span data-ttu-id="0c052-111">**類型 \_ 對齊** 宏會傳回資料類型的對齊需求。</span><span class="sxs-lookup"><span data-stu-id="0c052-111">The **TYPE\_ALIGNMENT** macro returns the alignment requirements of a data type.</span></span> <span data-ttu-id="0c052-112">例如： `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 （x86）、8（Intel Itanium 處理器 `TYPE_ALIGNMENT( UCHAR )` = = 1）</span><span class="sxs-lookup"><span data-stu-id="0c052-112">For example: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 on x86, 8 on Intel Itanium processor`TYPE_ALIGNMENT( UCHAR )` == 1 everywhere</span></span>

    <span data-ttu-id="0c052-113">例如，核心程式代碼目前看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="0c052-113">As an example, kernel code that currently looks like this:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    <span data-ttu-id="0c052-114">可能會變更為：</span><span class="sxs-lookup"><span data-stu-id="0c052-114">should probably be changed to:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    <span data-ttu-id="0c052-115">Intel Itanium 系統已停用核心模式對齊例外狀況的自動修正。</span><span class="sxs-lookup"><span data-stu-id="0c052-115">Automatic fixes of kernel-mode alignment exceptions are disabled for Intel Itanium systems.</span></span>

- <span data-ttu-id="0c052-116">請小心使用 NOT 作業。</span><span class="sxs-lookup"><span data-stu-id="0c052-116">Be careful with NOT operations.</span></span> <span data-ttu-id="0c052-117">請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="0c052-117">Consider the following:</span></span>

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    <span data-ttu-id="0c052-118">問題是 ~ (b-1) 會產生 "0x0000 0000 xxxx"，而不是 "0xFFFF FFFF xxxx"。</span><span class="sxs-lookup"><span data-stu-id="0c052-118">The problem is that ~(b–1) produces "0x0000 0000 xxxx xxxx" and not "0xFFFF FFFF xxxx xxxx".</span></span> <span data-ttu-id="0c052-119">編譯器將不會偵測到此情況。</span><span class="sxs-lookup"><span data-stu-id="0c052-119">The compiler will not detect this.</span></span> <span data-ttu-id="0c052-120">若要修正此問題，請變更程式碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0c052-120">To fix this, change the code as follows:</span></span>

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- <span data-ttu-id="0c052-121">請小心執行未簽署和簽署的作業。</span><span class="sxs-lookup"><span data-stu-id="0c052-121">Be careful performing unsigned and signed operations.</span></span> <span data-ttu-id="0c052-122">請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="0c052-122">Consider the following:</span></span>

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    <span data-ttu-id="0c052-123">結果非預期的大小。</span><span class="sxs-lookup"><span data-stu-id="0c052-123">The result is unexpectedly large.</span></span> <span data-ttu-id="0c052-124">規則是，如果任一運算元未簽署，則結果為未簽署。</span><span class="sxs-lookup"><span data-stu-id="0c052-124">The rule is that if either operand is unsigned, the result is unsigned.</span></span> <span data-ttu-id="0c052-125">在上述範例中，會將轉換成不帶正負號的值（除以 b），並將結果儲存在 c 中。</span><span class="sxs-lookup"><span data-stu-id="0c052-125">In the preceding example, a is converted to an unsigned value, divided by b, and the result stored in c.</span></span> <span data-ttu-id="0c052-126">轉換不需要進行數位操作。</span><span class="sxs-lookup"><span data-stu-id="0c052-126">The conversion involves no numeric manipulation.</span></span>

    <span data-ttu-id="0c052-127">另舉一個範例，請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="0c052-127">As another example, consider the following:</span></span>

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    <span data-ttu-id="0c052-128">發生此問題的原因是 x 不帶正負號，這會使整個運算式不帶正負號。</span><span class="sxs-lookup"><span data-stu-id="0c052-128">The problem arises because x is unsigned, which makes the entire expression unsigned.</span></span> <span data-ttu-id="0c052-129">除非 y 是負值，否則這會正常運作。</span><span class="sxs-lookup"><span data-stu-id="0c052-129">This works fine unless y is negative.</span></span> <span data-ttu-id="0c052-130">在此情況下，會將 y 轉換成不帶正負號的值、使用32位有效位數評估運算式、調整規模，並將其新增至 pVar1。</span><span class="sxs-lookup"><span data-stu-id="0c052-130">In this case, y is converted to an unsigned value, the expression is evaluated using 32-bit precision, scaled, and added to pVar1.</span></span> <span data-ttu-id="0c052-131">32位不帶正負號的負數會變成大型的64位正數，以提供錯誤的結果。</span><span class="sxs-lookup"><span data-stu-id="0c052-131">A 32-bit unsigned negative number becomes a large 64-bit positive number, which gives the wrong result.</span></span> <span data-ttu-id="0c052-132">若要修正這個問題，請將 x 宣告為帶正負號的值，或在運算式中明確地將它轉換為 **LONG** 。</span><span class="sxs-lookup"><span data-stu-id="0c052-132">To fix this problem, declare x as a signed value or explicitly typecast it to **LONG** in the expression.</span></span>

- <span data-ttu-id="0c052-133">進行分次大小配置時請小心。</span><span class="sxs-lookup"><span data-stu-id="0c052-133">Be careful when making piecemeal size allocations.</span></span> <span data-ttu-id="0c052-134">例如：</span><span class="sxs-lookup"><span data-stu-id="0c052-134">For example:</span></span>

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    <span data-ttu-id="0c052-135">下列程式碼是錯誤的，因為編譯器會以額外4個位元組填補結構，以進行8位元組的對齊：</span><span class="sxs-lookup"><span data-stu-id="0c052-135">The following code is wrong because the compiler will pad the structure with an additional 4 bytes to make the 8-byte alignment:</span></span>

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    <span data-ttu-id="0c052-136">下列程式碼是正確的：</span><span class="sxs-lookup"><span data-stu-id="0c052-136">The following code is correct:</span></span>

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- <span data-ttu-id="0c052-137">請勿傳遞給函式 `(HANDLE)0xFFFFFFFF` ，例如 [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)。</span><span class="sxs-lookup"><span data-stu-id="0c052-137">Do not pass `(HANDLE)0xFFFFFFFF` to functions such as [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span></span> <span data-ttu-id="0c052-138">相反地，請使用 **不正確 \_ 控制碼 \_ 值**。</span><span class="sxs-lookup"><span data-stu-id="0c052-138">Instead, use **INVALID\_HANDLE\_VALUE**.</span></span>
- <span data-ttu-id="0c052-139">列印字串時，請使用適當的格式規範。</span><span class="sxs-lookup"><span data-stu-id="0c052-139">Use the proper format specifiers when printing a string.</span></span> <span data-ttu-id="0c052-140">使用% p 以十六進位列印指標。</span><span class="sxs-lookup"><span data-stu-id="0c052-140">Use %p to print pointers in hexadecimal.</span></span> <span data-ttu-id="0c052-141">這是列印指標的最佳選擇。</span><span class="sxs-lookup"><span data-stu-id="0c052-141">This is the best choice for printing pointers.</span></span> <span data-ttu-id="0c052-142">Microsoft Visual C++ 支援% I列印多型資料。</span><span class="sxs-lookup"><span data-stu-id="0c052-142">Microsoft Visual C++ supports %I to print polymorphic data.</span></span> <span data-ttu-id="0c052-143">Visual C++ 也支援% I64 來列印64位的值。</span><span class="sxs-lookup"><span data-stu-id="0c052-143">Visual C++ also supports %I64 to print values that are 64 bits.</span></span>

 

 