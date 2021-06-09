---
description: 本主題說明 DirectXMath 程式庫的優化考慮和策略。
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: 使用 DirectXMath 程式庫進行程式碼優化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15369ab36e199eb1a204cc4b761dc637f114f2a1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827252"
---
# <a name="code-optimization-with-the-directxmath-library"></a><span data-ttu-id="bc81a-103">使用 DirectXMath 程式庫進行程式碼優化</span><span class="sxs-lookup"><span data-stu-id="bc81a-103">Code Optimization with the DirectXMath Library</span></span>

<span data-ttu-id="bc81a-104">本主題說明 DirectXMath 程式庫的優化考慮和策略。</span><span class="sxs-lookup"><span data-stu-id="bc81a-104">This topic describes optimization considerations and strategies with the DirectXMath Library.</span></span>

-   [<span data-ttu-id="bc81a-105">謹慎使用存取子</span><span class="sxs-lookup"><span data-stu-id="bc81a-105">Use accessors sparingly</span></span>](#use-accessors-sparingly)
-   [<span data-ttu-id="bc81a-106">使用正確的編譯設定</span><span class="sxs-lookup"><span data-stu-id="bc81a-106">Use correct compilation settings</span></span>](#use-correct-compilation-settings)
-   [<span data-ttu-id="bc81a-107">適當時使用 Est 函數</span><span class="sxs-lookup"><span data-stu-id="bc81a-107">Use Est functions when appropriate</span></span>](#use-est-functions-when-appropriate)
-   [<span data-ttu-id="bc81a-108">使用對齊的資料類型和作業</span><span class="sxs-lookup"><span data-stu-id="bc81a-108">Use Aligned Data Types and Operations</span></span>](#use-aligned-data-types-and-operations)
-   [<span data-ttu-id="bc81a-109">適當地對齊配置</span><span class="sxs-lookup"><span data-stu-id="bc81a-109">Properly Align Allocations</span></span>](#properly-align-allocations)
-   [<span data-ttu-id="bc81a-110">盡可能避免運算子多載</span><span class="sxs-lookup"><span data-stu-id="bc81a-110">Avoid Operator Overloads When Possible</span></span>](#avoid-operator-overloads-when-possible)
-   [<span data-ttu-id="bc81a-111">非正規數</span><span class="sxs-lookup"><span data-stu-id="bc81a-111">Denormals</span></span>](#denormals)
-   [<span data-ttu-id="bc81a-112">利用整數浮點數類雙重特性</span><span class="sxs-lookup"><span data-stu-id="bc81a-112">Take Advantage of the Integer Floating Point Duality</span></span>](#take-advantage-of-the-integer-floating-point-duality)
-   [<span data-ttu-id="bc81a-113">偏好範本表單</span><span class="sxs-lookup"><span data-stu-id="bc81a-113">Prefer Template Forms</span></span>](#prefer-template-forms)
-   [<span data-ttu-id="bc81a-114">搭配使用 DirectXMath 與 Direct3D</span><span class="sxs-lookup"><span data-stu-id="bc81a-114">Using DirectXMath with Direct3D</span></span>](#using-directxmath-with-direct3d)
-   [<span data-ttu-id="bc81a-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc81a-115">Related topics</span></span>](#related-topics)

## <a name="use-accessors-sparingly"></a><span data-ttu-id="bc81a-116">謹慎使用存取子</span><span class="sxs-lookup"><span data-stu-id="bc81a-116">Use accessors sparingly</span></span>

<span data-ttu-id="bc81a-117">以向量為基礎的作業會使用 SIMD 指令集，而這些指令集會利用特殊暫存器。</span><span class="sxs-lookup"><span data-stu-id="bc81a-117">Vector-based operations use the SIMD instruction sets and these make use of special registers.</span></span> <span data-ttu-id="bc81a-118">存取個別元件需要從 SIMD 暫存器移動到純量專案，然後再重新進行。</span><span class="sxs-lookup"><span data-stu-id="bc81a-118">Accessing individual components requires moving from the SIMD registers to the scalar ones and back again.</span></span>

<span data-ttu-id="bc81a-119">可能的話，您可以更有效率地一次初始化 [**XMVECTOR**](xmvector-data-type.md) 的所有元件，而不是使用一連串個別的向量存取子。</span><span class="sxs-lookup"><span data-stu-id="bc81a-119">When possible, it is more efficient to initialize all of the components of an [**XMVECTOR**](xmvector-data-type.md) at one time, instead of using a series of individual vector accessors.</span></span>

## <a name="use-correct-compilation-settings"></a><span data-ttu-id="bc81a-120">使用正確的編譯設定</span><span class="sxs-lookup"><span data-stu-id="bc81a-120">Use correct compilation settings</span></span>

<span data-ttu-id="bc81a-121">若為 Windows x86 目標，請啟用/arch： SSE2。</span><span class="sxs-lookup"><span data-stu-id="bc81a-121">For Windows x86 targets, enable /arch:SSE2.</span></span> <span data-ttu-id="bc81a-122">針對所有 Windows 目標，啟用/fp： fast。</span><span class="sxs-lookup"><span data-stu-id="bc81a-122">For all Windows targets, enable /fp:fast.</span></span>

<span data-ttu-id="bc81a-123">根據預設，針對 Window x86 目標的 DirectXMath 程式庫進行編譯時，是使用 \_ \_ 已定義的 SSE SSE \_ 內建函式來完成 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc81a-123">By default, compilation against the DirectXMath Library for Window x86 targets is done with \_XM\_SSE\_INTRINSICS\_ defined.</span></span> <span data-ttu-id="bc81a-124">這表示所有 DirectXMath 功能都會使用 SSE2 指令。</span><span class="sxs-lookup"><span data-stu-id="bc81a-124">This means that all DirectXMath functionality will make use of SSE2 instructions.</span></span> <span data-ttu-id="bc81a-125">不過，其他程式碼則不是如此。</span><span class="sxs-lookup"><span data-stu-id="bc81a-125">However, the same is not true for other code.</span></span>

<span data-ttu-id="bc81a-126">DirectXMath 之外的程式碼是使用編譯器預設值進行處理。</span><span class="sxs-lookup"><span data-stu-id="bc81a-126">Code outside of DirectXMath is handled using compiler defaults.</span></span> <span data-ttu-id="bc81a-127">如果沒有這個參數，所產生的程式碼通常可能會使用較不有效率的 x87 程式碼。</span><span class="sxs-lookup"><span data-stu-id="bc81a-127">Without this switch, the generated code may often use the less efficient x87 code.</span></span>

<span data-ttu-id="bc81a-128">強烈建議您一律使用最新的可用編譯器版本。</span><span class="sxs-lookup"><span data-stu-id="bc81a-128">We highly recommend that you always use the latest available version of the compiler.</span></span>

## <a name="use-est-functions-when-appropriate"></a><span data-ttu-id="bc81a-129">適當時使用 Est 函數</span><span class="sxs-lookup"><span data-stu-id="bc81a-129">Use Est functions when appropriate</span></span>

<span data-ttu-id="bc81a-130">許多函式都有對等的估計函數，以 Est 結尾。</span><span class="sxs-lookup"><span data-stu-id="bc81a-130">Many functions have an equivalent estimation function ending in Est.</span></span> <span data-ttu-id="bc81a-131">這些函式會以更佳的效能來提高效能。</span><span class="sxs-lookup"><span data-stu-id="bc81a-131">These functions trade some accuracy for improved performance.</span></span> <span data-ttu-id="bc81a-132">Est 函式適用于不重要的計算，可能會犧牲精確度以加快速度。</span><span class="sxs-lookup"><span data-stu-id="bc81a-132">Est functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.</span></span> <span data-ttu-id="bc81a-133">確切的遺失精確度和速度增加的數量取決於平臺。</span><span class="sxs-lookup"><span data-stu-id="bc81a-133">The exact amount of lost accuracy and speed increase are platform dependent.</span></span>

<span data-ttu-id="bc81a-134">例如， [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) 函式可用來取代 [**XMVector3AngleBetweenNormals**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals) 函數。</span><span class="sxs-lookup"><span data-stu-id="bc81a-134">For example, the [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) function could be used in place of the [**XMVector3AngleBetweenNormals**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals) function.</span></span>

## <a name="use-aligned-data-types-and-operations"></a><span data-ttu-id="bc81a-135">使用對齊的資料類型和作業</span><span class="sxs-lookup"><span data-stu-id="bc81a-135">Use Aligned Data Types and Operations</span></span>

<span data-ttu-id="bc81a-136">SIMD 指令集在支援 SSE2 的 windows 版本上，通常會有對齊和未對齊的記憶體作業版本。</span><span class="sxs-lookup"><span data-stu-id="bc81a-136">The SIMD instruction sets on versions of windows supporting SSE2 typically have aligned and unaligned versions of memory operations.</span></span> <span data-ttu-id="bc81a-137">您可以更快速地使用對齊的作業，而且應該盡可能進行建議。</span><span class="sxs-lookup"><span data-stu-id="bc81a-137">The use of the aligned operations is faster, and should be preferred wherever possible.</span></span>

<span data-ttu-id="bc81a-138">DirectXMath 程式庫透過 variant 向量類型、結構和函式提供存取對齊和未對齊的功能。</span><span class="sxs-lookup"><span data-stu-id="bc81a-138">The DirectXMath Library provides access aligned and unaligned functionality through variant vector types, structure, and functions.</span></span> <span data-ttu-id="bc81a-139">這些變數會以名稱結尾的 "A" 表示。</span><span class="sxs-lookup"><span data-stu-id="bc81a-139">These variants are indicated by an "A" at the end of the name.</span></span>

<span data-ttu-id="bc81a-140">例如，有一個未對齊的 [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) 結構和對齊的 [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) 結構，分別由 [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) 和 [**XMStoreFloat4A**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="bc81a-140">For example, there are an unaligned [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) structure and an aligned [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) structure, which are used by the [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) and [**XMStoreFloat4A**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) functions respectively.</span></span>

## <a name="properly-align-allocations"></a><span data-ttu-id="bc81a-141">適當地對齊配置</span><span class="sxs-lookup"><span data-stu-id="bc81a-141">Properly Align Allocations</span></span>

<span data-ttu-id="bc81a-142">DirectXMath 程式庫基礎的 [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) 內建函式的對齊版本，會比未對齊的程式更快。</span><span class="sxs-lookup"><span data-stu-id="bc81a-142">The aligned versions of the [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) intrinsics underlying the DirectXMath Library are faster than the unaligned.</span></span>

<span data-ttu-id="bc81a-143">基於這個理由，使用 [**XMVECTOR**](xmvector-data-type.md) 和 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 物件的 DirectXMath 作業會假設這些物件已對齊16位元組。</span><span class="sxs-lookup"><span data-stu-id="bc81a-143">For this reason, DirectXMath operations using [**XMVECTOR**](xmvector-data-type.md) and [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) objects assume those objects are 16-byte aligned.</span></span> <span data-ttu-id="bc81a-144">這是自動進行堆疊型配置，如果程式碼是使用建議的 Windows (針對 DirectXMath 程式庫進行編譯，請參閱 [使用正確的編譯設定](#use-correct-compilation-settings)) 編譯器設定。</span><span class="sxs-lookup"><span data-stu-id="bc81a-144">This is automatic for stack based allocations, if code is compiled against the DirectXMath Library using the recommended Windows (see [Use Correct Compilation Settings](#use-correct-compilation-settings)) compiler settings.</span></span> <span data-ttu-id="bc81a-145">不過，請務必確保包含 **XMVECTOR** 和 **XMMATRIX** 物件的堆積配置，或轉換成這些類型，以符合這些對齊需求。</span><span class="sxs-lookup"><span data-stu-id="bc81a-145">However, it is important to ensure that heap-allocation containing **XMVECTOR** and **XMMATRIX** objects, or casts to these types, meet these alignment requirements.</span></span>

<span data-ttu-id="bc81a-146">雖然64位的 Windows 記憶體配置已對齊16位元組，但根據預設，在配置的 Windows 記憶體32位版本中，只會對齊8個位元組。</span><span class="sxs-lookup"><span data-stu-id="bc81a-146">While 64-bit Windows memory allocations are 16-byte aligned, by default on 32 bit versions of Windows memory allocated is only 8-byte aligned.</span></span> <span data-ttu-id="bc81a-147">如需控制記憶體對齊的詳細資訊，請參閱[ \_ 對齊的 \_ malloc](https://docs.microsoft.com/cpp/c-runtime-library/reference/aligned-malloc)。</span><span class="sxs-lookup"><span data-stu-id="bc81a-147">For information on controlling memory alignment, see [\_aligned\_malloc](https://docs.microsoft.com/cpp/c-runtime-library/reference/aligned-malloc).</span></span>

<span data-ttu-id="bc81a-148">使用對齊的 DirectXMath 類型搭配標準範本庫 (STL) 時，您必須提供自訂配置器，以確保16位元組的對齊。</span><span class="sxs-lookup"><span data-stu-id="bc81a-148">When using aligned DirectXMath types with the Standard Template Library (STL), you will need to provide a custom allocator that ensures the 16-byte alignment.</span></span> <span data-ttu-id="bc81a-149">如需撰寫自訂配置器的範例，請參閱 Visual C++ Team [blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) (而不是使用 malloc/free，您會想要 \_ \_ \_ \_ 在您的實施) 中使用對齊的 malloc 並保持可用。</span><span class="sxs-lookup"><span data-stu-id="bc81a-149">See the Visual C++ Team [blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) for an example of writing a custom allocator (instead of malloc/free you'll want to use \_aligned\_malloc and \_aligned\_free in your implementation).</span></span>

> [!Note]  
> <span data-ttu-id="bc81a-150">某些 STL 範本會修改提供的型別對齊。</span><span class="sxs-lookup"><span data-stu-id="bc81a-150">Some STL templates modify the provided type's alignment.</span></span> <span data-ttu-id="bc81a-151">例如， [讓 \_ 共用<>](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) 新增一些內部追蹤資訊，而這些資訊不一定會與所提供使用者類型的對齊，而導致資料成員未對齊。</span><span class="sxs-lookup"><span data-stu-id="bc81a-151">For example, [make\_shared<>](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) adds some internal tracking information which may or may not respect the alignment of the provided user type, resulting in unaligned data members.</span></span> <span data-ttu-id="bc81a-152">在此情況下，您需要使用未對齊的類型，而不是對齊類型。</span><span class="sxs-lookup"><span data-stu-id="bc81a-152">In this case, you need to use unaligned types instead of aligned types.</span></span> <span data-ttu-id="bc81a-153">如果您衍生自現有的類別（包括許多 Windows 執行階段物件），您也可以修改類別或結構的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="bc81a-153">If you derive from existing classes, including many Windows Runtime objects, you can also modify the alignment of a class or structure.</span></span>

 

## <a name="avoid-operator-overloads-when-possible"></a><span data-ttu-id="bc81a-154">盡可能避免運算子多載</span><span class="sxs-lookup"><span data-stu-id="bc81a-154">Avoid Operator Overloads When Possible</span></span>

<span data-ttu-id="bc81a-155">為了方便起見， [**XMVECTOR**](xmvector-data-type.md) 和 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 之類的一些類型具有一般算數運算的運算子多載。</span><span class="sxs-lookup"><span data-stu-id="bc81a-155">As a convenience feature, a number of types such as [**XMVECTOR**](xmvector-data-type.md) and [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) have operator overloads for common arithmetic operations.</span></span> <span data-ttu-id="bc81a-156">這類運算子多載通常會建立許多暫存物件。</span><span class="sxs-lookup"><span data-stu-id="bc81a-156">Such operator overloads tend to create numerous temporary objects.</span></span> <span data-ttu-id="bc81a-157">建議您避免在效能敏感的程式碼中執行這些運算子多載。</span><span class="sxs-lookup"><span data-stu-id="bc81a-157">We recommend that you avoid these operator overloads in performance sensitive code.</span></span>

## <a name="denormals"></a><span data-ttu-id="bc81a-158">非正規數</span><span class="sxs-lookup"><span data-stu-id="bc81a-158">Denormals</span></span>

<span data-ttu-id="bc81a-159">為了支援接近0的計算，IEEE 754 浮點數標準包含漸進下溢的支援。</span><span class="sxs-lookup"><span data-stu-id="bc81a-159">To support computations close to 0, the IEEE 754 float-point standard includes support for gradual underflow.</span></span> <span data-ttu-id="bc81a-160">逐漸下溢是透過使用反正規化值來實行，而許多硬體實作為處理 denormals 時的速度很慢。</span><span class="sxs-lookup"><span data-stu-id="bc81a-160">Gradual underflow is implemented through the use of denormalized values, and many hardware implementations are slow when handling denormals.</span></span> <span data-ttu-id="bc81a-161">要考慮的優化是針對 DirectXMath 所使用的向量作業停用 denormals 處理。</span><span class="sxs-lookup"><span data-stu-id="bc81a-161">An optimization to consider is to disable the handling of denormals for the vector operations used by DirectXMath.</span></span>

<span data-ttu-id="bc81a-162">變更 denormals 的處理是藉由線上程上使用[ \_ controlfp \_ ](/cpp/c-runtime-library/reference/controlfp-s)的常式來完成，而且可能會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="bc81a-162">Changing the handling of denormals is done by using the [\_controlfp\_s](/cpp/c-runtime-library/reference/controlfp-s) routine on a pre-thread basis, and can result in performance improvements.</span></span> <span data-ttu-id="bc81a-163">使用此程式碼來變更 denormals 的處理：</span><span class="sxs-lookup"><span data-stu-id="bc81a-163">Use this code to change the handling of denormals:</span></span>


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> <span data-ttu-id="bc81a-164">在64位版本的 Windows 上， [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) 指令是用於所有計算，而不只是向量作業。</span><span class="sxs-lookup"><span data-stu-id="bc81a-164">On 64-bit versions of Windows, [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) instructions are used for all computations, not just the vector operations.</span></span> <span data-ttu-id="bc81a-165">變更 denormal 處理會影響程式中的所有浮點運算，而不只是 DirectXMath 所使用的向量作業。</span><span class="sxs-lookup"><span data-stu-id="bc81a-165">Changing the denormal handling affects all floating-point computations in your program, not just the vector operations used by DirectXMath.</span></span>

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a><span data-ttu-id="bc81a-166">利用整數浮點數類雙重特性</span><span class="sxs-lookup"><span data-stu-id="bc81a-166">Take Advantage of the Integer Floating Point Duality</span></span>

<span data-ttu-id="bc81a-167">DirectXMath 支援以四個單精確度浮點數或 4 32 位 (帶正負號或不帶正負號) 值的向量。</span><span class="sxs-lookup"><span data-stu-id="bc81a-167">DirectXMath supports vectors of 4 single-precision floating-point or four 32-bit (signed or unsigned) values.</span></span>

<span data-ttu-id="bc81a-168">由於用來實 DirectXMath 程式庫的指令集會讓您將相同的資料視為多個不同的類型（例如，將相同的向量視為浮點數和整數資料），因此可以達成特定的優化功能。</span><span class="sxs-lookup"><span data-stu-id="bc81a-168">Because the instruction sets used to implement the DirectXMath Library have the ability to treat the same data as multiple different types-for example, treat the same vector as floating-point and integer data-certain optimizations can be achieved.</span></span> <span data-ttu-id="bc81a-169">您可以使用整數向量初始化常式和位運算運算子來取得這些優化，以操作浮點值。</span><span class="sxs-lookup"><span data-stu-id="bc81a-169">You can get these optimizations by using the integer vector initialization routines and bit-wise operators to manipulate floating-point values.</span></span>

<span data-ttu-id="bc81a-170">DirectXMath 程式庫所使用之單精確度浮點數的二進位格式，完全符合 IEEE 764 標準：</span><span class="sxs-lookup"><span data-stu-id="bc81a-170">The binary format of single-precision floating-point numbers used by the DirectXMath Library completely conforms to the IEEE 764 standard:</span></span>

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

<span data-ttu-id="bc81a-171">使用 IEEE 764 單一精確度浮點數時，請務必記住，某些標記法具有特殊意義 (也就是說，它們不符合上述描述) 。</span><span class="sxs-lookup"><span data-stu-id="bc81a-171">When working with the IEEE 764 single precision floating-point number, it is important to keep in mind, that some representations have special meaning (that is, they do not conform to the preceding description).</span></span> <span data-ttu-id="bc81a-172">範例包括：</span><span class="sxs-lookup"><span data-stu-id="bc81a-172">Examples include:</span></span>

-   <span data-ttu-id="bc81a-173">正零為0</span><span class="sxs-lookup"><span data-stu-id="bc81a-173">Positive zero is 0</span></span>
-   <span data-ttu-id="bc81a-174">負零是0x80000000</span><span class="sxs-lookup"><span data-stu-id="bc81a-174">Negative zero is 0x80000000</span></span>
-   <span data-ttu-id="bc81a-175">Q \_ NAN 為07FC0000</span><span class="sxs-lookup"><span data-stu-id="bc81a-175">Q\_NAN is 07FC0000</span></span>
-   <span data-ttu-id="bc81a-176">+ INF 0x7F800000</span><span class="sxs-lookup"><span data-stu-id="bc81a-176">+INF is 0x7F800000</span></span>
-   <span data-ttu-id="bc81a-177">-INF 0xFF800000</span><span class="sxs-lookup"><span data-stu-id="bc81a-177">-INF is 0xFF800000</span></span>

## <a name="prefer-template-forms"></a><span data-ttu-id="bc81a-178">偏好範本表單</span><span class="sxs-lookup"><span data-stu-id="bc81a-178">Prefer Template Forms</span></span>

<span data-ttu-id="bc81a-179">[**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle)、 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)、 [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert)、 [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft)、 [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)和 [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright)的範本形式存在。</span><span class="sxs-lookup"><span data-stu-id="bc81a-179">Template form exists for [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle), [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert), [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft), [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft), and [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright).</span></span> <span data-ttu-id="bc81a-180">使用這些取代一般的函式表單，可讓編譯器建立更多提升企業效率的實作為。</span><span class="sxs-lookup"><span data-stu-id="bc81a-180">Using these instead of the general function form allows the compiler to create much more efficent implementations.</span></span> <span data-ttu-id="bc81a-181">對於 [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))，這通常會折迭為一或兩個 \_ mm \_ 隨機的 \_ ps 值。</span><span class="sxs-lookup"><span data-stu-id="bc81a-181">For [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)), this often collapses down to one or two \_mm\_shuffle\_ps values.</span></span> <span data-ttu-id="bc81a-182">針對 ARM-霓虹燈， **XMVectorSwizzle** 範本可以利用一些特殊案例，而不是更一般的 VTBL swizzle/置換。</span><span class="sxs-lookup"><span data-stu-id="bc81a-182">For ARM-NEON, the **XMVectorSwizzle** template can utilize a number of special cases rather than the more general VTBL swizzle/permute.</span></span>

## <a name="using-directxmath-with-direct3d"></a><span data-ttu-id="bc81a-183">搭配使用 DirectXMath 與 Direct3D</span><span class="sxs-lookup"><span data-stu-id="bc81a-183">Using DirectXMath with Direct3D</span></span>

<span data-ttu-id="bc81a-184">DirectXMath 的常見用途是執行與 Direct3D 搭配使用的圖形計算。</span><span class="sxs-lookup"><span data-stu-id="bc81a-184">A common use for DirectXMath is to perform graphics computations for use with Direct3D.</span></span> <span data-ttu-id="bc81a-185">使用 Direct3D 2.x 和 Direct3D 11. x，您可以透過下列直接方式來使用 DirectXMath 程式庫：</span><span class="sxs-lookup"><span data-stu-id="bc81a-185">With Direct3D 10.x and Direct3D 11.x, you can use the DirectXMath library in these direct ways:</span></span>

-   <span data-ttu-id="bc81a-186">在 [**>id3d11devicecoNtext：： ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview)或 [**ID3D10Device：： ClearRenderTargetView**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview)方法的呼叫中，直接在 *ColorRGBA* 參數中使用色彩命名空間 [常數](ovw-xnamath-reference-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="bc81a-186">Use the Colors namespace [constants](ovw-xnamath-reference-constants.md) directly in the *ColorRGBA* parameter in a call to the [**ID3D11DeviceContext::ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) or [**ID3D10Device::ClearRenderTargetView**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) method.</span></span> <span data-ttu-id="bc81a-187">針對 Direct3D 9，您必須轉換成 [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)型別，以在 [**IDirect3DDevice9：： Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)方法的呼叫中使用它做為 *Color* 參數。</span><span class="sxs-lookup"><span data-stu-id="bc81a-187">For Direct3D 9, you must convert to the [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) type to use it as the *Color* parameter in a call to the [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) method.</span></span>
-   <span data-ttu-id="bc81a-188">使用 [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**XMVECTOR**](xmvector-data-type.md)和 [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)型別來設定常數緩衝區結構，以供 HLSL [**float4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md)或 [**矩陣**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4 類型參考。</span><span class="sxs-lookup"><span data-stu-id="bc81a-188">Use the [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)/[**XMVECTOR**](xmvector-data-type.md) and [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)/[**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) types to setup constant buffer structures for reference by HLSL [**float4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md) or [**matrix**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4 types.</span></span>
    > [!Note]  
    > <span data-ttu-id="bc81a-189">[**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) /[**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)類型是以資料列為主的格式。</span><span class="sxs-lookup"><span data-stu-id="bc81a-189">[**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)/[**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) types are in row-major format.</span></span> <span data-ttu-id="bc81a-190">因此，如果您使用/Zpr 編譯器參數 ([**D3DCOMPILE \_ PACK 矩陣資料 \_ 行 \_ \_ 主要**](../direct3dhlsl/d3dcompile-constants.md) 編譯旗標) 或在 \_ HLSL 中宣告矩陣類型時省略 row 主要 [關鍵字](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md) ，則當您將矩陣設定為常數緩衝區時，就必須將它變換。</span><span class="sxs-lookup"><span data-stu-id="bc81a-190">Therefore, if you use the /Zpr compiler switch (the [**D3DCOMPILE\_PACK\_MATRIX\_COLUMN\_MAJOR**](../direct3dhlsl/d3dcompile-constants.md) compile flag) or omit the row\_major [keyword](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md) when you declare the matrix type in HLSL, you must transpose the matrix when you set it into the constant buffer.</span></span>

     

-   <span data-ttu-id="bc81a-191">使用 Direct3D 2.x 和 Direct3D 11. x，您可以假設 Map 方法所傳回的指標 (例如， **.pdata** 成員 ([**D3D10 \_ 對應 \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d)中的 [**>id3d11devicecoNtext：： map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) 。**.Pdata**、 [**D3D10 \_ 對應的 \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d)。**.Pdata**，或 [**D3D11 \_ 對應的 \_ SUBRESOURCE**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource)。如果您使用 [功能層級](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)10 \_ 0 或更高版本，或每次使用 [**D3D11 \_ 使用量 \_ 暫存**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage)資源，.pdata) 會對齊16位元組。</span><span class="sxs-lookup"><span data-stu-id="bc81a-191">With Direct3D 10.x and Direct3D 11.x, you can assume that the pointer returned by the Map method (for example, [**ID3D11DeviceContext::Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) in the **pData** member ([**D3D10\_MAPPED\_TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d).**pData**, [**D3D10\_MAPPED\_TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**pData**, or [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) is 16-byte aligned if you use [feature level](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 10\_0 or higher or whenever you use [**D3D11\_USAGE\_STAGING**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc81a-192">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc81a-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc81a-193">DirectXMath 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="bc81a-193">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
