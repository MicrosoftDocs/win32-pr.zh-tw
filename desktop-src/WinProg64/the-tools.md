---
title: 工具
description: 本主題說明可供您用來讓應用程式64位就緒的工具。 Windows 10 適用于 x64 和 ARM64 型處理器。
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計，工具
- 工具64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372480"
---
# <a name="the-tools"></a><span data-ttu-id="e20a2-106">工具</span><span class="sxs-lookup"><span data-stu-id="e20a2-106">The Tools</span></span>

<span data-ttu-id="e20a2-107">本主題說明可供您用來讓應用程式64位就緒的工具。</span><span class="sxs-lookup"><span data-stu-id="e20a2-107">This topic describes the tools available for you to use in making your application 64-bit ready.</span></span> <span data-ttu-id="e20a2-108">Windows 10 適用于 x64 和 ARM64 型處理器。</span><span class="sxs-lookup"><span data-stu-id="e20a2-108">Windows 10 is available for both x64 and ARM64 based processors.</span></span>

## <a name="include-files"></a><span data-ttu-id="e20a2-109">包含檔案</span><span class="sxs-lookup"><span data-stu-id="e20a2-109">Include Files</span></span>

<span data-ttu-id="e20a2-110">在 32-和64位 Windows 之間，API 元素幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="e20a2-110">The API elements are virtually identical between 32- and 64-bit Windows.</span></span> <span data-ttu-id="e20a2-111">Windows 標頭檔已經過修改，因此可以同時用於32和64位的程式碼。</span><span class="sxs-lookup"><span data-stu-id="e20a2-111">The Windows header files have been modified so that they can be used for both 32- and 64-bit code.</span></span> <span data-ttu-id="e20a2-112">新的64位類型和宏會定義在新的標頭檔 Basetsd 中，該檔案位於 Windows 所包含的標頭檔集中。</span><span class="sxs-lookup"><span data-stu-id="e20a2-112">The new 64-bit types and macros are defined in a new header file, Basetsd.h, which is in the set of header files included by Windows.h.</span></span> <span data-ttu-id="e20a2-113">Basetsd 包含新的資料類型定義，可協助您使原始程式碼與單字大小無關。</span><span class="sxs-lookup"><span data-stu-id="e20a2-113">Basetsd.h includes the new data-type definitions to assist in making source code word-size independent.</span></span>

## <a name="new-data-types"></a><span data-ttu-id="e20a2-114">新的資料類型</span><span class="sxs-lookup"><span data-stu-id="e20a2-114">New Data Types</span></span>

<span data-ttu-id="e20a2-115">Windows 標頭檔包含新的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e20a2-115">The Windows header files contain new data types.</span></span> <span data-ttu-id="e20a2-116">這些類型主要用於與32位資料類型的類型相容性。</span><span class="sxs-lookup"><span data-stu-id="e20a2-116">These types are primarily for type compatibility with the 32-bit data types.</span></span> <span data-ttu-id="e20a2-117">新的型別提供與現有類型完全相同的輸入，同時也提供64位 Windows 的支援。</span><span class="sxs-lookup"><span data-stu-id="e20a2-117">The new types provide exactly the same typing as the existing types, while at the same time providing support for the 64-bit Windows.</span></span> <span data-ttu-id="e20a2-118">如需詳細資訊，請參閱 [新的資料類型](the-new-data-types.md) 或 Basetsd .h 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="e20a2-118">For more information, see [The New Data Types](the-new-data-types.md) or the Basetsd.h header file.</span></span>

## <a name="predefined-macros"></a><span data-ttu-id="e20a2-119">預先定義的巨集</span><span class="sxs-lookup"><span data-stu-id="e20a2-119">Predefined Macros</span></span>

<span data-ttu-id="e20a2-120">編譯器會定義下列宏以識別平臺。</span><span class="sxs-lookup"><span data-stu-id="e20a2-120">The compiler defines the following macros to identify the platform.</span></span>



| <span data-ttu-id="e20a2-121">巨集</span><span class="sxs-lookup"><span data-stu-id="e20a2-121">Macro</span></span>   | <span data-ttu-id="e20a2-122">意義</span><span class="sxs-lookup"><span data-stu-id="e20a2-122">Meaning</span></span>                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e20a2-123">\_WIN64</span><span class="sxs-lookup"><span data-stu-id="e20a2-123">\_WIN64</span></span> | <span data-ttu-id="e20a2-124">64位平臺。</span><span class="sxs-lookup"><span data-stu-id="e20a2-124">A 64-bit platform.</span></span> <span data-ttu-id="e20a2-125">這包括 x64 和 ARM64。</span><span class="sxs-lookup"><span data-stu-id="e20a2-125">This includes both x64 and ARM64.</span></span>                                                        |
| <span data-ttu-id="e20a2-126">\_WIN32</span><span class="sxs-lookup"><span data-stu-id="e20a2-126">\_WIN32</span></span> | <span data-ttu-id="e20a2-127">32位平臺。</span><span class="sxs-lookup"><span data-stu-id="e20a2-127">A 32-bit platform.</span></span> <span data-ttu-id="e20a2-128">64位編譯器也會定義這個值，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="e20a2-128">This value is also defined by the 64-bit compiler for backward compatibility.</span></span><br/> |
| <span data-ttu-id="e20a2-129">\_WIN16</span><span class="sxs-lookup"><span data-stu-id="e20a2-129">\_WIN16</span></span> | <span data-ttu-id="e20a2-130">16位平臺</span><span class="sxs-lookup"><span data-stu-id="e20a2-130">A 16-bit platform</span></span>                                                                                           |



 

<span data-ttu-id="e20a2-131">以下是架構特有的宏。</span><span class="sxs-lookup"><span data-stu-id="e20a2-131">The following macros are specific to the architecture.</span></span>



| <span data-ttu-id="e20a2-132">巨集</span><span class="sxs-lookup"><span data-stu-id="e20a2-132">Macro</span></span>      | <span data-ttu-id="e20a2-133">意義</span><span class="sxs-lookup"><span data-stu-id="e20a2-133">Meaning</span></span>                |
|------------|------------------------|
| <span data-ttu-id="e20a2-134">\_M \_ IA64</span><span class="sxs-lookup"><span data-stu-id="e20a2-134">\_M\_IA64</span></span>  | <span data-ttu-id="e20a2-135">Intel Itanium 平臺</span><span class="sxs-lookup"><span data-stu-id="e20a2-135">Intel Itanium platform</span></span> |
| <span data-ttu-id="e20a2-136">\_M \_ IX86</span><span class="sxs-lookup"><span data-stu-id="e20a2-136">\_M\_IX86</span></span>  | <span data-ttu-id="e20a2-137">x86 平臺</span><span class="sxs-lookup"><span data-stu-id="e20a2-137">x86 platform</span></span>           |
| <span data-ttu-id="e20a2-138">\_M \_ X64</span><span class="sxs-lookup"><span data-stu-id="e20a2-138">\_M\_X64</span></span>   | <span data-ttu-id="e20a2-139">x64 平臺</span><span class="sxs-lookup"><span data-stu-id="e20a2-139">x64 platform</span></span>           |
| <span data-ttu-id="e20a2-140">\_M \_ ARM64</span><span class="sxs-lookup"><span data-stu-id="e20a2-140">\_M\_ARM64</span></span> | <span data-ttu-id="e20a2-141">ARM64 平臺</span><span class="sxs-lookup"><span data-stu-id="e20a2-141">ARM64 platform</span></span>         |



 

<span data-ttu-id="e20a2-142">請勿使用這些宏，但請 \_ 盡可能使用 WIN64、 \_ WIN32 和 WIN16 （但不含架構專屬程式碼） \_ 。</span><span class="sxs-lookup"><span data-stu-id="e20a2-142">Do not use these macros except with architecture-specific code, instead, use \_WIN64, \_WIN32, and \_WIN16 whenever possible.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="e20a2-143">輔助函式</span><span class="sxs-lookup"><span data-stu-id="e20a2-143">Helper Functions</span></span>

<span data-ttu-id="e20a2-144">下列內嵌函式 (在 Basetsd 中定義) 可協助您安全地將值從某個類型轉換成另一個類型。</span><span class="sxs-lookup"><span data-stu-id="e20a2-144">The following inline functions (defined in Basetsd.h) can help you safely convert values from one type to another.</span></span>

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> <span data-ttu-id="e20a2-145">**IntToPtr** sign-擴充 **Int** 值、 **UIntToPtr** 零延伸不 **帶正負** 號的 int 值、 **LongToPtr** sign 擴充 **long** 值， **ULongToPtr** 零延伸不 **帶正負** 號的長整數值。</span><span class="sxs-lookup"><span data-stu-id="e20a2-145">**IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.</span></span>

 

## <a name="64-bit-compiler"></a><span data-ttu-id="e20a2-146">64位編譯器</span><span class="sxs-lookup"><span data-stu-id="e20a2-146">64-bit Compiler</span></span>

<span data-ttu-id="e20a2-147">64位編譯器可以用來識別指標截斷、不當的型別轉換，以及其他64位特定的問題。</span><span class="sxs-lookup"><span data-stu-id="e20a2-147">The 64-bit compilers can be used to identify pointer truncation, improper type casts, and other 64-bit-specific problems.</span></span>

<span data-ttu-id="e20a2-148">當編譯器第一次執行時，可能會產生許多指標截斷或類型不符的警告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e20a2-148">When the compiler is first run, it will probably generate many pointer truncation or type mismatch warnings, such as the following:</span></span>

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

<span data-ttu-id="e20a2-149">使用這些警告作為指南，讓程式碼更健全。</span><span class="sxs-lookup"><span data-stu-id="e20a2-149">Use these warnings as a guide to make the code more robust.</span></span> <span data-ttu-id="e20a2-150">最好的作法是消除所有警告，尤其是指標截斷警告。</span><span class="sxs-lookup"><span data-stu-id="e20a2-150">It is good practice to eliminate all warnings, especially pointer-truncation warnings.</span></span>

## <a name="64-bit-compiler-switches-and-warnings"></a><span data-ttu-id="e20a2-151">64位編譯器參數和警告</span><span class="sxs-lookup"><span data-stu-id="e20a2-151">64-bit Compiler Switches and Warnings</span></span>

<span data-ttu-id="e20a2-152">請注意，此編譯器會啟用 LLP64 資料模型。</span><span class="sxs-lookup"><span data-stu-id="e20a2-152">Note that this compiler enables the LLP64 data model.</span></span>

<span data-ttu-id="e20a2-153">有警告選項可協助移植至 LLP64。</span><span class="sxs-lookup"><span data-stu-id="e20a2-153">There is a warning option to assist porting to LLP64.</span></span> <span data-ttu-id="e20a2-154">-Wp64-W3 參數會啟用下列警告：</span><span class="sxs-lookup"><span data-stu-id="e20a2-154">The -Wp64 -W3 switch enables the following warnings:</span></span>

-   <span data-ttu-id="e20a2-155">C4305：截斷警告。</span><span class="sxs-lookup"><span data-stu-id="e20a2-155">C4305: Truncation warning.</span></span> <span data-ttu-id="e20a2-156">例如，「return」：從「不帶正負號的 int64」到「long」的截斷。</span><span class="sxs-lookup"><span data-stu-id="e20a2-156">For example, "return": truncation from "unsigned int64" to "long."</span></span>
-   <span data-ttu-id="e20a2-157">C4311：截斷警告。</span><span class="sxs-lookup"><span data-stu-id="e20a2-157">C4311: Truncation warning.</span></span> <span data-ttu-id="e20a2-158">例如，"type cast"：從 "int \* \_ ptr64" 到 "int" 的指標截斷。</span><span class="sxs-lookup"><span data-stu-id="e20a2-158">For example, "type cast": pointer truncation from "int\*\_ptr64" to "int."</span></span>
-   <span data-ttu-id="e20a2-159">C4312：轉換成較大大小的警告。</span><span class="sxs-lookup"><span data-stu-id="e20a2-159">C4312: Conversion to bigger-size warning.</span></span> <span data-ttu-id="e20a2-160">例如，「類型轉換」：從 "int" 轉換成 \* \_ 較大大小的 "int ptr64"。</span><span class="sxs-lookup"><span data-stu-id="e20a2-160">For example, "type cast": conversion from "int" to "int\*\_ptr64" of greater size.</span></span>
-   <span data-ttu-id="e20a2-161">C4318：傳遞零長度。</span><span class="sxs-lookup"><span data-stu-id="e20a2-161">C4318: Passing zero length.</span></span> <span data-ttu-id="e20a2-162">例如，將常數零當作長度傳遞給 **memset** 函數。</span><span class="sxs-lookup"><span data-stu-id="e20a2-162">For example, passing constant zero as the length to the **memset** function.</span></span>
-   <span data-ttu-id="e20a2-163">C4319： Not 運算子。</span><span class="sxs-lookup"><span data-stu-id="e20a2-163">C4319: Not operator.</span></span> <span data-ttu-id="e20a2-164">例如，"~"：零將「不帶正負號的 long」延伸至較大的「不帶正負號 \_ 的 int64」。</span><span class="sxs-lookup"><span data-stu-id="e20a2-164">For example, "~": zero extending "unsigned long" to "unsigned \_int64" of greater size.</span></span>
-   <span data-ttu-id="e20a2-165">C4313：呼叫 **printf** 系列的函式，其中包含衝突的轉換類型規範和引數。</span><span class="sxs-lookup"><span data-stu-id="e20a2-165">C4313: Calling the **printf** family of functions with conflicting conversion type specifiers and arguments.</span></span> <span data-ttu-id="e20a2-166">例如，格式字串中的 "printf"： "% p" 與類型 "int64" 的引數2衝突 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e20a2-166">For example, "printf": "%p" in format string conflicts with argument 2 of type "\_int64."</span></span> <span data-ttu-id="e20a2-167">另一個範例是呼叫 printf ( "% x"，指標 \_ 值) ; 這會造成最高32位的截斷。</span><span class="sxs-lookup"><span data-stu-id="e20a2-167">Another example is the call printf("%x", pointer\_value); this causes a truncation of the upper 32 bits.</span></span> <span data-ttu-id="e20a2-168">正確的呼叫是 printf ( "% p"，指標 \_ 值) 。</span><span class="sxs-lookup"><span data-stu-id="e20a2-168">The correct call is printf("%p", pointer\_value).</span></span>
-   <span data-ttu-id="e20a2-169">C4244：與現有的警告 C4242 相同。</span><span class="sxs-lookup"><span data-stu-id="e20a2-169">C4244: Same as the existing warning C4242.</span></span> <span data-ttu-id="e20a2-170">例如，「return」：從「int64」轉換 \_ 成「不帶正負號的整數」可能會遺失資料。</span><span class="sxs-lookup"><span data-stu-id="e20a2-170">For example, "return": conversion from "\_int64" to "unsigned int," possible loss of data.</span></span>

## <a name="64-bit-linker-and-libraries"></a><span data-ttu-id="e20a2-171">64位連結器和程式庫</span><span class="sxs-lookup"><span data-stu-id="e20a2-171">64-bit Linker and Libraries</span></span>

<span data-ttu-id="e20a2-172">若要建立應用程式，請使用 Windows SDK 所提供的連結器和程式庫。</span><span class="sxs-lookup"><span data-stu-id="e20a2-172">To build applications, use the linker and libraries provided by the Windows SDK.</span></span> <span data-ttu-id="e20a2-173">大部分的32位程式庫都有相對應的64位版本，但某些舊版程式庫只有在32位版本中才可使用。</span><span class="sxs-lookup"><span data-stu-id="e20a2-173">Most 32-bit libraries have a corresponding 64-bit version, but certain legacy libraries are available only in 32-bit versions.</span></span> <span data-ttu-id="e20a2-174">當針對64位 Windows 建立應用程式時，呼叫這些程式庫的程式碼將不會連結。</span><span class="sxs-lookup"><span data-stu-id="e20a2-174">Code that calls into these libraries will not link when the application is built for 64-bit Windows.</span></span>

 

 





