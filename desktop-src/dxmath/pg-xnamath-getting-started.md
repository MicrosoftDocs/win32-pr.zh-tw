---
title: '開始 (DirectXMath) '
description: DirectXMath 程式庫會針對單精確度浮點數向量（ (2D、3D 和 4D) 或矩陣 (3 ×3和4× 4) ），來實作為算術和線性代數運算的最佳和可移植介面。
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e599acfc498e28b33acfc5bbbba2bea5669d2a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321384"
---
# <a name="getting-started-directxmath"></a><span data-ttu-id="50f88-103">開始 (DirectXMath) </span><span class="sxs-lookup"><span data-stu-id="50f88-103">Getting started (DirectXMath)</span></span>

<span data-ttu-id="50f88-104">DirectXMath 程式庫會針對單精確度浮點數向量（ (2D、3D 和 4D) 或矩陣 (3 ×3和4× 4) ），來實作為算術和線性代數運算的最佳和可移植介面。</span><span class="sxs-lookup"><span data-stu-id="50f88-104">The DirectXMath Library implements an optimal and portable interface for arithmetic and linear algebra operations on single-precision floating-point vectors (2D, 3D, and 4D) or matrices (3×3 and 4×4).</span></span> <span data-ttu-id="50f88-105">程式庫對整數向量作業的支援有限。</span><span class="sxs-lookup"><span data-stu-id="50f88-105">The library has some limited support for integer vector operations.</span></span> <span data-ttu-id="50f88-106">圖形程式會廣泛地使用這些作業來呈現和動畫。</span><span class="sxs-lookup"><span data-stu-id="50f88-106">These operations are used extensively in rendering and animation by graphics programs.</span></span> <span data-ttu-id="50f88-107">不支援雙精確度向量 (包括長、短路或 bytes) ，以及只有有限的整數向量運算。</span><span class="sxs-lookup"><span data-stu-id="50f88-107">There is no support for double-precision vectors (including longs, shorts, or bytes), and only limited integer vector operations.</span></span>

<span data-ttu-id="50f88-108">此程式庫可在各種不同的 Windows 平臺上使用。</span><span class="sxs-lookup"><span data-stu-id="50f88-108">The library is available on a variety of Windows platforms.</span></span> <span data-ttu-id="50f88-109">因為此程式庫提供了先前無法使用的功能，所以這個版本會取代下列程式庫：</span><span class="sxs-lookup"><span data-stu-id="50f88-109">Because the library provides functionality not available previously, this version supersedes the following libraries:</span></span>

-   <span data-ttu-id="50f88-110">Xboxmath .h 標頭所提供的 Xbox 數學程式庫</span><span class="sxs-lookup"><span data-stu-id="50f88-110">Xbox Math library provided by the Xboxmath.h header</span></span>
-   <span data-ttu-id="50f88-111">D3DX 9 Dll 提供的 D3DX 9 程式庫</span><span class="sxs-lookup"><span data-stu-id="50f88-111">D3DX 9 library provided by the D3DX 9 DLLs</span></span>
-   <span data-ttu-id="50f88-112">透過 D3DX 10 Dll 提供的 D3DX 10 數學程式庫</span><span class="sxs-lookup"><span data-stu-id="50f88-112">D3DX 10 math library provided through the D3DX 10 DLLs</span></span>
-   <span data-ttu-id="50f88-113">DirectX SDK 和 Xbox 360 XDK 中的 xnamath. h 標頭所提供的不帶數學程式庫</span><span class="sxs-lookup"><span data-stu-id="50f88-113">XNA Math library provided by the xnamath.h header in the DirectX SDK and Xbox 360 XDK</span></span>

<span data-ttu-id="50f88-114">這些章節概述開始使用的基本概念。</span><span class="sxs-lookup"><span data-stu-id="50f88-114">These sections outline the basics of getting started.</span></span>

-   [<span data-ttu-id="50f88-115">下載</span><span class="sxs-lookup"><span data-stu-id="50f88-115">Download</span></span>](#download)
-   [<span data-ttu-id="50f88-116">執行時間系統需求</span><span class="sxs-lookup"><span data-stu-id="50f88-116">Run-Time System Requirements</span></span>](#run-time-system-requirements)
-   [<span data-ttu-id="50f88-117">設計總覽</span><span class="sxs-lookup"><span data-stu-id="50f88-117">Design Overview</span></span>](#design-overview)
-   [<span data-ttu-id="50f88-118">矩陣慣例</span><span class="sxs-lookup"><span data-stu-id="50f88-118">Matrix convention</span></span>](#matrix-convention)
-   [<span data-ttu-id="50f88-119">基本使用方式</span><span class="sxs-lookup"><span data-stu-id="50f88-119">Basic Usage</span></span>](#basic-usage)
-   [<span data-ttu-id="50f88-120">類型使用指導方針</span><span class="sxs-lookup"><span data-stu-id="50f88-120">Type Usage Guidelines</span></span>](#type-usage-guidelines)
-   [<span data-ttu-id="50f88-121">建立向量</span><span class="sxs-lookup"><span data-stu-id="50f88-121">Creating Vectors</span></span>](#creating-vectors)
    -   [<span data-ttu-id="50f88-122">常數向量</span><span class="sxs-lookup"><span data-stu-id="50f88-122">CONSTANT VECTORS</span></span>](#constant-vectors)
    -   [<span data-ttu-id="50f88-123">變數中的向量</span><span class="sxs-lookup"><span data-stu-id="50f88-123">VECTORS FROM VARIABLES</span></span>](#vectors-from-variables)
    -   [<span data-ttu-id="50f88-124">向量的向量</span><span class="sxs-lookup"><span data-stu-id="50f88-124">VECTORS FROM VECTORS</span></span>](#vectors-from-vectors)
    -   [<span data-ttu-id="50f88-125">記憶體中的向量</span><span class="sxs-lookup"><span data-stu-id="50f88-125">VECTORS FROM MEMORY</span></span>](#vectors-from-memory)
-   [<span data-ttu-id="50f88-126">從向量解壓縮元件</span><span class="sxs-lookup"><span data-stu-id="50f88-126">Extracting Components from Vectors</span></span>](#extracting-components-from-vectors)
-   [<span data-ttu-id="50f88-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="50f88-127">Related topics</span></span>](#related-topics)

## <a name="download"></a><span data-ttu-id="50f88-128">下載</span><span class="sxs-lookup"><span data-stu-id="50f88-128">Download</span></span>

<span data-ttu-id="50f88-129">DirectXMath 程式庫包含在 Windows SDK 中。</span><span class="sxs-lookup"><span data-stu-id="50f88-129">The DirectXMath library is included in the Windows SDK.</span></span> <span data-ttu-id="50f88-130">或者，您也可以從 [GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath)下載。</span><span class="sxs-lookup"><span data-stu-id="50f88-130">Alternatively you can download it from [GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath).</span></span> <span data-ttu-id="50f88-131">此網站也包含相關的範例專案。</span><span class="sxs-lookup"><span data-stu-id="50f88-131">This site also contains related sample projects.</span></span>

## <a name="run-time-system-requirements"></a><span data-ttu-id="50f88-132">Run-Time 系統需求</span><span class="sxs-lookup"><span data-stu-id="50f88-132">Run-Time System Requirements</span></span>

<span data-ttu-id="50f88-133">DirectXMath 程式庫會在向量作業可用時，使用特製化的處理器指令。</span><span class="sxs-lookup"><span data-stu-id="50f88-133">The DirectXMath Library uses specialized processor instructions for vector operations when they are available.</span></span> <span data-ttu-id="50f88-134">若要避免程式產生「未知的指令例外狀況」錯誤，請先呼叫 [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) ，然後再使用 DirectXMath 程式庫來檢查處理器支援。</span><span class="sxs-lookup"><span data-stu-id="50f88-134">To avoid having a program generate "unknown instruction exception" faults, check for processor support by calling [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) before using the DirectXMath Library.</span></span>

<span data-ttu-id="50f88-135">以下是基本的 DirectXMath 程式庫執行時間支援需求：</span><span class="sxs-lookup"><span data-stu-id="50f88-135">These are the basic DirectXMath Library run-time support requirements:</span></span>

-   <span data-ttu-id="50f88-136">Windows (x86/x64) 平臺上的預設編譯需要 SSE/SSE2 指令支援。</span><span class="sxs-lookup"><span data-stu-id="50f88-136">Default compilation on a Windows (x86/x64) platform requires SSE/SSE2 instruction support.</span></span>
-   <span data-ttu-id="50f88-137">Windows RT 平臺上的預設編譯需要 ARM-霓虹燈指令支援。</span><span class="sxs-lookup"><span data-stu-id="50f88-137">Default compliation on a Windows RT platform requires ARM-NEON instruction support.</span></span>
-   <span data-ttu-id="50f88-138">使用 XM 進行編譯時， [**\_ \_ 未定義任何 \_ 內建函式 \_**](ovw-xnamath-reference-directives.md) ，只需要標準的浮點運算支援。</span><span class="sxs-lookup"><span data-stu-id="50f88-138">Compilation with [**\_XM\_NO\_INTRINSICS\_**](ovw-xnamath-reference-directives.md) defined requires only standard floating-point operation support.</span></span>

> [!Note]  
> <span data-ttu-id="50f88-139">當您呼叫 [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport)時，請包含 <的>，然後再包含 <DirectXMath. h>。</span><span class="sxs-lookup"><span data-stu-id="50f88-139">When you call [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport), include <windows.h> before you include <DirectXMath.h>.</span></span> <span data-ttu-id="50f88-140">這是程式庫中唯一需要 <windows. h> 中之內容的函式，因此您不需要在使用 <DirectXMath 的每個模組中包含 <的 windows. h>。</span><span class="sxs-lookup"><span data-stu-id="50f88-140">This is the only function in the library that requires any content from <windows.h> so you aren't required to include <windows.h> in every module that uses <DirectXMath.h>.</span></span>

 

## <a name="design-overview"></a><span data-ttu-id="50f88-141">設計概觀</span><span class="sxs-lookup"><span data-stu-id="50f88-141">Design Overview</span></span>

<span data-ttu-id="50f88-142">DirectXMath 程式庫主要支援 c + + 程式設計語言。</span><span class="sxs-lookup"><span data-stu-id="50f88-142">The DirectXMath Library primarily supports the C++ programming language.</span></span> <span data-ttu-id="50f88-143">此程式庫是使用 DirectXMath \* . .inl、DirectXPackedVector. .inl 和 DirectXCollision. .inl 中的內嵌常式來執行。</span><span class="sxs-lookup"><span data-stu-id="50f88-143">The library is implemented using inline routines in the header files, DirectXMath\*.inl, DirectXPackedVector.inl and DirectXCollision.inl.</span></span> <span data-ttu-id="50f88-144">這項實行會使用高效能編譯器內建函式。</span><span class="sxs-lookup"><span data-stu-id="50f88-144">This implementation makes use of high-performance compiler intrinsics.</span></span>

<span data-ttu-id="50f88-145">DirectXMath 程式庫提供：</span><span class="sxs-lookup"><span data-stu-id="50f88-145">The DirectXMath Library provides:</span></span>

-   <span data-ttu-id="50f88-146">使用 SSE/SSE2 內建函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="50f88-146">An implementation using SSE/SSE2 intrinsics.</span></span>
-   <span data-ttu-id="50f88-147">沒有內建函式的執行。</span><span class="sxs-lookup"><span data-stu-id="50f88-147">An implementation without intrinsics.</span></span>
-   <span data-ttu-id="50f88-148">使用 ARM 霓虹燈內建函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="50f88-148">An implementation using ARM-NEON intrinsics.</span></span>

<span data-ttu-id="50f88-149">因為程式庫是使用標頭檔來傳遞，所以請使用原始程式碼針對您自己的應用程式自訂和優化。</span><span class="sxs-lookup"><span data-stu-id="50f88-149">Because the library is delivered using header files, use the source code to customize and optimize for your own app.</span></span>

## <a name="matrix-convention"></a><span data-ttu-id="50f88-150">矩陣慣例</span><span class="sxs-lookup"><span data-stu-id="50f88-150">Matrix convention</span></span>

<span data-ttu-id="50f88-151">DirectXMath 使用資料列主要矩陣、資料列向量和預先相乘。</span><span class="sxs-lookup"><span data-stu-id="50f88-151">DirectXMath uses row-major matrices, row vectors, and pre-multiplication.</span></span> <span data-ttu-id="50f88-152">Handedness 取決於 (RH 與 LH) 所使用的函式版本，否則函數會使用左手或右手的視圖座標。</span><span class="sxs-lookup"><span data-stu-id="50f88-152">Handedness is determined by which function version is used (RH vs. LH), otherwise the function works with either left-handed or right-handed view coordinates.</span></span>

<span data-ttu-id="50f88-153">為了進行參考，Direct3D 先前使用了左方座標系統、資料列主要矩陣、資料列向量和預先相乘。</span><span class="sxs-lookup"><span data-stu-id="50f88-153">For reference, Direct3D has historically used left-handed coordinate system, row-major matrices, row vectors, and pre-multiplication.</span></span> <span data-ttu-id="50f88-154">新式 Direct3D 並不具有左方和右手方座標的強大需求，而且通常會 HLSL 著色器預設為使用資料行主要矩陣。</span><span class="sxs-lookup"><span data-stu-id="50f88-154">Modern Direct3D does not have a strong requirement for left vs. right-handed coordinates, and typically HLSL shaders default to consuming column-major matrices.</span></span> <span data-ttu-id="50f88-155">如需詳細資料，請參閱 [HLSL 矩陣順序](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-155">See [HLSL Matrix Ordering](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math) for details.</span></span>

## <a name="basic-usage"></a><span data-ttu-id="50f88-156">基本使用方式</span><span class="sxs-lookup"><span data-stu-id="50f88-156">Basic Usage</span></span>

<span data-ttu-id="50f88-157">若要使用 DirectXMath 程式庫函式，請包含 DirectXMath .h、DirectXPackedVector .h、DirectXColors .h 及/或 DirectXCollision .h 標頭。</span><span class="sxs-lookup"><span data-stu-id="50f88-157">To use DirectXMath Library functions, include the DirectXMath.h, DirectXPackedVector.h, DirectXColors.h, and/or DirectXCollision.h headers.</span></span> <span data-ttu-id="50f88-158">您可以在 Windows Store 應用程式的 Windows 軟體開發套件中找到這些標頭。</span><span class="sxs-lookup"><span data-stu-id="50f88-158">The headers are found in the Windows Software Development Kit for Windows Store apps.</span></span>

## <a name="type-usage-guidelines"></a><span data-ttu-id="50f88-159">類型使用指導方針</span><span class="sxs-lookup"><span data-stu-id="50f88-159">Type Usage Guidelines</span></span>

<span data-ttu-id="50f88-160">[**XMVECTOR**](xmvector-data-type.md)和 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)類型是 DirectXMath 程式庫的工作馬。</span><span class="sxs-lookup"><span data-stu-id="50f88-160">The [**XMVECTOR**](xmvector-data-type.md) and [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) types are the work horses for the DirectXMath Library.</span></span> <span data-ttu-id="50f88-161">每個作業都會耗用或產生這些類型的資料。</span><span class="sxs-lookup"><span data-stu-id="50f88-161">Every operation consumes or produces data of these types.</span></span> <span data-ttu-id="50f88-162">使用程式庫是使用程式庫的關鍵。</span><span class="sxs-lookup"><span data-stu-id="50f88-162">Working with them is key to using the library.</span></span> <span data-ttu-id="50f88-163">不過，由於 DirectXMath 會使用 SIMD 指令集，因此這些資料類型會受到一些限制。</span><span class="sxs-lookup"><span data-stu-id="50f88-163">However, since DirectXMath makes use of the SIMD instruction sets, these data types are subject to a number of restrictions.</span></span> <span data-ttu-id="50f88-164">如果您想要充分利用 DirectXMath 函式，請務必瞭解這些限制。</span><span class="sxs-lookup"><span data-stu-id="50f88-164">It is critical that you understand these restrictions if you want to make good use of the DirectXMath functions.</span></span>

<span data-ttu-id="50f88-165">您應該將 [**XMVECTOR**](xmvector-data-type.md) 視為 SIMD 硬體登錄的 proxy，以及 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 為四個 simd 硬體暫存器邏輯群組的 proxy。</span><span class="sxs-lookup"><span data-stu-id="50f88-165">You should think of [**XMVECTOR**](xmvector-data-type.md) as a proxy for a SIMD hardware register, and [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) as a proxy for a logical grouping of four SIMD hardware registers.</span></span> <span data-ttu-id="50f88-166">這些類型會標注，表示它們需要16位元組對齊才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="50f88-166">These types are annotated to indicate they require 16-byte alignment to work correctly.</span></span> <span data-ttu-id="50f88-167">編譯器會在做為區域變數時，自動將它們放置在堆疊上，或在當做全域變數使用時，將它們放在資料區段中。</span><span class="sxs-lookup"><span data-stu-id="50f88-167">The compiler will automatically place them correctly on the stack when they are used as a local variable, or place them in the data segment when they are used as a global variable.</span></span> <span data-ttu-id="50f88-168">有了適當的慣例，也可以安全地將它們當作參數傳遞給函式 (如需詳細資訊) ，請參閱 [呼叫慣例](pg-xnamath-internals.md) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-168">With proper conventions, they can also be passed safely as parameters to a function (see [Calling Conventions](pg-xnamath-internals.md) for details).</span></span>

<span data-ttu-id="50f88-169">不過，堆積的配置更為複雜。</span><span class="sxs-lookup"><span data-stu-id="50f88-169">Allocations from the heap, however, are more complicated.</span></span> <span data-ttu-id="50f88-170">因此，每當您使用 [**XMVECTOR**](xmvector-data-type.md) 或 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 做為類別或結構的成員，以從堆積配置時，您就必須特別小心。</span><span class="sxs-lookup"><span data-stu-id="50f88-170">As such, you need to be careful whenever you use either [**XMVECTOR**](xmvector-data-type.md) or [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) as a member of a class or structure to be allocated from the heap.</span></span> <span data-ttu-id="50f88-171">在 Windows x64 上，所有堆積配置都已對齊16位元組，但針對 Windows x86，則只會對齊8個位元組。</span><span class="sxs-lookup"><span data-stu-id="50f88-171">On Windows x64, all heap allocations are 16-byte aligned, but for Windows x86, they are only 8-byte aligned.</span></span> <span data-ttu-id="50f88-172">有一些選項可從堆積配置16位元組對齊的結構 (請參閱 [適當地對齊](pg-xnamath-optimizing.md) 配置) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-172">There are options for allocating structures from the heap with 16-byte alignment (see [Properly Align Allocations](pg-xnamath-optimizing.md)).</span></span> <span data-ttu-id="50f88-173">針對 c + + 程式，您可以使用 operator new/delete/new/delete 多載 \[ \] \[ \] (全域或特定類別) ，視需要強制執行最佳對齊。</span><span class="sxs-lookup"><span data-stu-id="50f88-173">For C++ programs, you can use operator new/delete/new\[\]/delete\[\] overloads (either globally or class-specific) to enforce optimal alignment if desired.</span></span>

> [!Note]  
> <span data-ttu-id="50f88-174">替代方法是在 c + + 類別中直接藉由多載新的/刪除來強制對齊，您可以使用 [pImpl 的用法](https://en.wikipedia.org/wiki/Opaque_pointer)。</span><span class="sxs-lookup"><span data-stu-id="50f88-174">As an alternative to enforcing alignment in your C++ class directly by overloading new/delete, you can use the [pImpl idiom](https://en.wikipedia.org/wiki/Opaque_pointer).</span></span> <span data-ttu-id="50f88-175">如果您確定您的 **Impl** 類別透過內部 [**\_ 對齊的 \_ malloc**](/cpp/c-runtime-library/reference/aligned-malloc)對齊，您就可以在內部執行中自由使用對齊的類型。</span><span class="sxs-lookup"><span data-stu-id="50f88-175">If you ensure your **Impl** class is aligned via [**\_aligned\_malloc**](/cpp/c-runtime-library/reference/aligned-malloc) internally, you can then freely use aligned types within the internal implementation.</span></span> <span data-ttu-id="50f88-176">當 ' public ' 類別是 Windows 執行階段 ref 類別，或要與 [**std：： shared \_ ptr<>**](/cpp/standard-library/shared-ptr-class)搭配使用時，這會是很好的選項，否則可能會中斷密切對齊。</span><span class="sxs-lookup"><span data-stu-id="50f88-176">This is a good option when the 'public' class is a Windows Runtime ref class or intended for use with [**std::shared\_ptr<>**](/cpp/standard-library/shared-ptr-class), which can otherwise disrupt careful alignment.</span></span>

 

<span data-ttu-id="50f88-177">不過，通常更容易且更精簡，以避免直接在類別或結構中使用 [**XMVECTOR**](xmvector-data-type.md) 或 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-177">However, often it is easier and more compact to avoid using [**XMVECTOR**](xmvector-data-type.md) or [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) directly in a class or structure.</span></span> <span data-ttu-id="50f88-178">相反地，請使用 [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)、 [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)、 [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3)、 [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)等作為結構的成員。</span><span class="sxs-lookup"><span data-stu-id="50f88-178">Instead, make use of the [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3), [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4), [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3), [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4), and so on, as members of your structure.</span></span> <span data-ttu-id="50f88-179">此外，您可以使用 [向量載入](ovw-xnamath-reference-functions-load.md) 和 [向量儲存](ovw-xnamath-reference-functions-storage.md) 函式，將資料有效率地移至 **XMVECTOR** 或 **XMMATRIX** 區域變數，執行計算並儲存結果。</span><span class="sxs-lookup"><span data-stu-id="50f88-179">Further, you can use the [Vector Loading](ovw-xnamath-reference-functions-load.md) and [Vector Storage](ovw-xnamath-reference-functions-storage.md) functions to move the data efficiently into **XMVECTOR** or **XMMATRIX** local variables, perform computations, and store the results.</span></span> <span data-ttu-id="50f88-180">另外還有串流處理函式 ([**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)、 [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)等，在這些資料類型的陣列上有效率地直接操作的) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-180">There are also streaming functions ([**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream), [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream), and so on) that efficiently operate directly on arrays of these data types.</span></span>

## <a name="creating-vectors"></a><span data-ttu-id="50f88-181">建立向量</span><span class="sxs-lookup"><span data-stu-id="50f88-181">Creating Vectors</span></span>

### <a name="constant-vectors"></a><span data-ttu-id="50f88-182">常數向量</span><span class="sxs-lookup"><span data-stu-id="50f88-182">CONSTANT VECTORS</span></span>

<span data-ttu-id="50f88-183">許多作業都需要在向量計算中使用常數，而且有數種方式可以載入具有所需值的 [**XMVECTOR**](xmvector-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-183">Many operations require the use of constants in vector computations, and there are a number of ways to load an [**XMVECTOR**](xmvector-data-type.md) with the desired values.</span></span>

-   <span data-ttu-id="50f88-184">如果將純量常數載入至 [**XMVECTOR**](xmvector-data-type.md)的所有元素，請使用 [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) 或 [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint)。</span><span class="sxs-lookup"><span data-stu-id="50f88-184">If loading a scalar constant into all elements of an [**XMVECTOR**](xmvector-data-type.md), use [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) or [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).</span></span>
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   <span data-ttu-id="50f88-185">如果使用具有不同固定值的向量常數作為 [**XMVECTOR**](xmvector-data-type.md)，請使用 [**XMVECTORF32**](xmvectorf32-data-type.md)、 [**XMVECTORU32**](xmvectoru32-data-type.md)、 **XMVECTORI32** 或 [**XMVECTORU8**](xmvectoru8-data-type.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="50f88-185">If using a vector constant with different fixed values as an [**XMVECTOR**](xmvector-data-type.md), use the [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32**, or [**XMVECTORU8**](xmvectoru8-data-type.md) structures.</span></span> <span data-ttu-id="50f88-186">然後您可以直接參考您傳遞 **XMVECTOR** 值的任何位置。</span><span class="sxs-lookup"><span data-stu-id="50f88-186">These can be then referenced directly anywhere you would pass an **XMVECTOR** value.</span></span>
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > <span data-ttu-id="50f88-187">請勿直接使用具有 [**XMVECTOR**](xmvector-data-type.md) (的初始化運算式清單，也就是 XMVECTOR v = {1.0 f，2.0 f，3.0 f，4.0 f} ) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-187">Do not use initializer lists directly with [**XMVECTOR**](xmvector-data-type.md) (that is, XMVECTOR v = { 1.0f, 2.0f, 3.0f, 4.0f }).</span></span> <span data-ttu-id="50f88-188">這類程式碼的效率不佳，而且在 DirectXMath 支援的所有平臺上都無法移植。</span><span class="sxs-lookup"><span data-stu-id="50f88-188">Such code is inefficient and is not portable across all platforms that are supported by DirectXMath.</span></span>

     

-   <span data-ttu-id="50f88-189">DirectXMath 包含數個預先定義的全域常數，可讓您在程式碼中使用 (g \_ XMOne、g \_ XMOne3、g \_ XMTwo、g \_ XMOneHalf、g \_ XMHalfPi、g \_ XMPi 等) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-189">DirectXMath includes a number of pre-defined global constants you can make use of in your code (g\_XMOne, g\_XMOne3, g\_XMTwo, g\_XMOneHalf, g\_XMHalfPi, g\_XMPi, and so on).</span></span> <span data-ttu-id="50f88-190">在 DirectXMath. h 標頭中搜尋 **XMGLOBALCONSTANT** 值。</span><span class="sxs-lookup"><span data-stu-id="50f88-190">Search the DirectXMath.h header for the **XMGLOBALCONSTANT** values.</span></span>
-   <span data-ttu-id="50f88-191">常見 RGB 色彩有一組向量常數 (紅色、綠色、藍色、黃色等) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-191">There are a set of vector constants for common RGB colors (Red, Green, Blue, Yellow, and so on).</span></span> <span data-ttu-id="50f88-192">如需這些向量常數的詳細資訊，請參閱 DirectXColors .h 和 DirectX：： Colors 命名空間。</span><span class="sxs-lookup"><span data-stu-id="50f88-192">For more info about these vector constants, see DirectXColors.h and the DirectX::Colors namespace.</span></span>

### <a name="vectors-from-variables"></a><span data-ttu-id="50f88-193">變數中的向量</span><span class="sxs-lookup"><span data-stu-id="50f88-193">VECTORS FROM VARIABLES</span></span>

-   <span data-ttu-id="50f88-194">如果從單一純量變數建立向量，請參閱 [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) 和 [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint)。</span><span class="sxs-lookup"><span data-stu-id="50f88-194">If creating a vector from a single scalar variable, see [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) and [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).</span></span>
    ```
    XMVECTOR v = XMVectorReplicate( f  );
    ```

    

-   <span data-ttu-id="50f88-195">如果從四個純量變數建立向量，請參閱 [**XMVectorSet**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) 和 [**XMVectorSetInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint)。</span><span class="sxs-lookup"><span data-stu-id="50f88-195">If creating a vector from four scalar variables, see [**XMVectorSet**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) and [**XMVectorSetInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint).</span></span>
    ```
    XMVECTOR v = XMVectorSet( fx, fy, fz, fw );
    ```

    

### <a name="vectors-from-vectors"></a><span data-ttu-id="50f88-196">向量的向量</span><span class="sxs-lookup"><span data-stu-id="50f88-196">VECTORS FROM VECTORS</span></span>

-   <span data-ttu-id="50f88-197">如果從另一個向量建立向量，並將特定的元件設定為變數，您可以考慮使用 [向量存取子函數](ovw-xnamath-reference-functions-accessors.md)。</span><span class="sxs-lookup"><span data-stu-id="50f88-197">If creating a vector from another vector with a specific component set to a variable, you can consider using [Vector Accessor Functions](ovw-xnamath-reference-functions-accessors.md).</span></span>
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   <span data-ttu-id="50f88-198">如果從另一個已複寫單一元件的向量建立向量，請使用 [**XMVectorSplatX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx)、 [**XMVectorSplatY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty)、 [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)和 [**XMVectorSplatW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw)。</span><span class="sxs-lookup"><span data-stu-id="50f88-198">If creating a vector from another vector with a single component replicated, use [**XMVectorSplatX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx), [**XMVectorSplatY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty), [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz), and [**XMVectorSplatW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw).</span></span>
    ```
    XMVECTOR vz = XMVectorSplatZ( v );
    ```

    

-   <span data-ttu-id="50f88-199">如果從另一個向量或不同向量（具有重新排序的元件）建立向量，請參閱 [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) 和 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)。</span><span class="sxs-lookup"><span data-stu-id="50f88-199">If creating a vector from another vector or pair of vectors with reordered components, see [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) and [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute).</span></span>
    ```
    XMVECTOR v2 = XMVectorSwizzle<XM_SWIZZLE_Z, XM_SWIZZLE_Y, XM_SWIZZLE_W, XM_SWIZZLE_X>( v1 );

    XMVECTOR v3 = XMVectorPermute<XM_PERMUTE_0W, XM_PERMUTE_1X, XM_PERMUTE_0X, XM_PERMUTE_1Z>( v1, v2 );
    ```

    

### <a name="vectors-from-memory"></a><span data-ttu-id="50f88-200">記憶體中的向量</span><span class="sxs-lookup"><span data-stu-id="50f88-200">VECTORS FROM MEMORY</span></span>

-   <span data-ttu-id="50f88-201">若要從記憶體載入單一 float 值，請參閱 [**XMVectorReplicatePtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr)、 [**XMVectorReplicateIntPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr)、 [**XMLoadFloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat)和 [**XMLoadInt**](/windows/win32/api/directxmath/nf-directxmath-xmloadint)。</span><span class="sxs-lookup"><span data-stu-id="50f88-201">For loading a single float value from memory, see [**XMVectorReplicatePtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr), [**XMVectorReplicateIntPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr), [**XMLoadFloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat), and [**XMLoadInt**](/windows/win32/api/directxmath/nf-directxmath-xmloadint).</span></span>
-   <span data-ttu-id="50f88-202">載入 float 陣列的常見方式是： [**XMLoadFloat2**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2)、 [**XMLoadFloat3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3)、 [**XMLoadFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4)、 [**XMLoadFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3)、 [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3)和 [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4)。</span><span class="sxs-lookup"><span data-stu-id="50f88-202">Common ways to load float arrays are: [**XMLoadFloat2**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2), [**XMLoadFloat3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3), [**XMLoadFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4), [**XMLoadFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3), [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3), and [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4).</span></span>
-   <span data-ttu-id="50f88-203">DirectXMath 包含一組豐富的型別和相關的負載，以及用來處理各種資料結構和常見 GPU 格式的存放區。</span><span class="sxs-lookup"><span data-stu-id="50f88-203">DirectXMath includes a rich set of types and related loads and stores for handling various data-structures and common GPU formats.</span></span> <span data-ttu-id="50f88-204">請參閱 [向量載入](ovw-xnamath-reference-functions-load.md) 和 [向量存放區](ovw-xnamath-reference-functions-storage.md)。</span><span class="sxs-lookup"><span data-stu-id="50f88-204">See [Vector Load](ovw-xnamath-reference-functions-load.md) and [Vector Store](ovw-xnamath-reference-functions-storage.md).</span></span>

## <a name="extracting-components-from-vectors"></a><span data-ttu-id="50f88-205">從向量解壓縮元件</span><span class="sxs-lookup"><span data-stu-id="50f88-205">Extracting Components from Vectors</span></span>

<span data-ttu-id="50f88-206">當資料載入 SIMD 暫存器，並在解壓縮結果之前完整處理時，SIMD 處理最有效率。</span><span class="sxs-lookup"><span data-stu-id="50f88-206">SIMD processing is most efficient when data is loaded into the SIMD registers and fully processed before extracting the results.</span></span> <span data-ttu-id="50f88-207">純量和向量表單之間的轉換效率不佳，因此我們建議您只在必要時才這樣做。</span><span class="sxs-lookup"><span data-stu-id="50f88-207">Conversion between scalar and vector forms is inefficient, so we recommend that you do it only when required.</span></span> <span data-ttu-id="50f88-208">基於這個理由，DirectXMath 程式庫中產生純量值的函式會以向量形式傳回，其中純量結果會在產生的向量之間複寫， (也就是， [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot)、 [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length)等) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-208">For this reason, functions in the DirectXMath library that produce a scalar value are returned in a vector form where the scalar result is replicated across the resulting vector (that is, [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot), [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length), and so on).</span></span> <span data-ttu-id="50f88-209">但是，當您需要純量值時，以下是一些如何做的選擇：</span><span class="sxs-lookup"><span data-stu-id="50f88-209">However, when you need scalar values, here are a few choices on how to go about it:</span></span>

-   <span data-ttu-id="50f88-210">如果計算單一純量答案，則適用 [向量存取](ovw-xnamath-reference-functions-accessors.md) 子函式的用法如下：</span><span class="sxs-lookup"><span data-stu-id="50f88-210">If a single scalar answer is computed, use of the [Vector Accessor Functions](ovw-xnamath-reference-functions-accessors.md) is appropriate:</span></span>
    ```
    float f = XMVectorGetX( v );
    ```

    

-   <span data-ttu-id="50f88-211">如果需要將向量的多個元件解壓縮，請考慮將向量儲存在記憶體結構中，然後將它讀回。</span><span class="sxs-lookup"><span data-stu-id="50f88-211">If multiple components of the vector are required to be extracted, consider storing the vector in a memory structure and reading it back.</span></span> <span data-ttu-id="50f88-212">例如：</span><span class="sxs-lookup"><span data-stu-id="50f88-212">For example:</span></span>
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   <span data-ttu-id="50f88-213">向量處理最有效率的形式是使用記憶體對記憶體串流，其中會使用 [向量載入](ovw-xnamath-reference-functions-load.md) 函式從記憶體載入輸入資料 () 、完整地以 SIMD 形式處理，然後寫入記憶體 () 使用 [向量存放函數](ovw-xnamath-reference-functions-storage.md) 。</span><span class="sxs-lookup"><span data-stu-id="50f88-213">The most efficient form of vector processing is to use memory-to-memory streaming where the input data is loaded from memory (using [Vector Load Functions](ovw-xnamath-reference-functions-load.md)), processed fully in SIMD form, and then written to memory (using [Vector Store Functions](ovw-xnamath-reference-functions-storage.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="50f88-214">相關主題</span><span class="sxs-lookup"><span data-stu-id="50f88-214">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50f88-215">DirectXMath 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="50f88-215">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>

 

 