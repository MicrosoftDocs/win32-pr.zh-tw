---
description: 本總覽說明使用 [DirectXMath] 程式庫將現有程式碼遷移至程式庫所需的變更。
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: 從「設備」數學程式庫進行程式碼遷移
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549960"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="a71b2-103">從「設備」數學程式庫進行程式碼遷移</span><span class="sxs-lookup"><span data-stu-id="a71b2-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="a71b2-104">本總覽說明使用 [DirectXMath] 程式庫將現有程式碼遷移至程式庫所需的變更。</span><span class="sxs-lookup"><span data-stu-id="a71b2-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

## <a name="header-changes"></a><span data-ttu-id="a71b2-105">標頭變更</span><span class="sxs-lookup"><span data-stu-id="a71b2-105">Header Changes</span></span>

<span data-ttu-id="a71b2-106">DirectXMath 程式庫會使用一組新的標頭。</span><span class="sxs-lookup"><span data-stu-id="a71b2-106">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="a71b2-107">將 `xnamath.h` 標頭取代為 `DirectXMath.h` ，並 `DirectXPackedVector.h` 為 *GPU 封裝* 類型新增。</span><span class="sxs-lookup"><span data-stu-id="a71b2-107">Replace the `xnamath.h` header with `DirectXMath.h`, and add `DirectXPackedVector.h` for the *GPU packed* types.</span></span>

<span data-ttu-id="a71b2-108">中的 DirectX SDK 衝突範例中的周框類型 `xnacollision.h` 現在是中 DirectXMath 程式庫的一部分 `DirectXCollision.h` 。</span><span class="sxs-lookup"><span data-stu-id="a71b2-108">The bounding types from the DirectX SDK Collision sample in `xnacollision.h` is now part of the DirectXMath library in `DirectXCollision.h`.</span></span> <span data-ttu-id="a71b2-109">這些已修改為使用 c + + 類別，而不是 C 樣式的 API。</span><span class="sxs-lookup"><span data-stu-id="a71b2-109">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="a71b2-110">常數變更</span><span class="sxs-lookup"><span data-stu-id="a71b2-110">Constant Changes</span></span>

<span data-ttu-id="a71b2-111">XNAMATH \_ 版本 (200、201、202、203、204等) 已取代為 DIRECXTMATH \_ 版本 (300、301、302、303等) 。</span><span class="sxs-lookup"><span data-stu-id="a71b2-111">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!NOTE]  
> <span data-ttu-id="a71b2-112">DirectXMath 3.00 和3.02 隨附 Windows SDK 的初步版本。</span><span class="sxs-lookup"><span data-stu-id="a71b2-112">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="a71b2-113">DirectXMath 3.03 是 Windows 8 SDK 的最終版本。</span><span class="sxs-lookup"><span data-stu-id="a71b2-113">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

## <a name="namespaces"></a><span data-ttu-id="a71b2-114">命名空間</span><span class="sxs-lookup"><span data-stu-id="a71b2-114">Namespaces</span></span>

<span data-ttu-id="a71b2-115">DirectXMath 程式庫會使用 c + + 命名空間來組織類型。</span><span class="sxs-lookup"><span data-stu-id="a71b2-115">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="a71b2-116">只有全域命名空間才會使用未使用的運算。</span><span class="sxs-lookup"><span data-stu-id="a71b2-116">XNA Math used only the global namespace.</span></span> <span data-ttu-id="a71b2-117">DirectXMath 類型在 **directx** 或 **Directx：:P ackedvector** 命名空間中是常見的。</span><span class="sxs-lookup"><span data-stu-id="a71b2-117">The DirectXMath types in common with XNA Math are in the **DirectX** or the **DirectX::PackedVector** namespace.</span></span>

<span data-ttu-id="a71b2-118">在 c + + 原始程式檔中，簡單的解決方案是加入 `using` 語句。</span><span class="sxs-lookup"><span data-stu-id="a71b2-118">In C++ source files, a simple solution is to add `using` statements.</span></span>

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

<span data-ttu-id="a71b2-119">如果是標頭，則不會被視為加入 using 語句的最佳作法。</span><span class="sxs-lookup"><span data-stu-id="a71b2-119">For headers, it is not considered best practice to add using statements.</span></span> <span data-ttu-id="a71b2-120">請改為新增完整命名空間。</span><span class="sxs-lookup"><span data-stu-id="a71b2-120">Instead, add fully-qualified namespaces.</span></span>

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a><span data-ttu-id="a71b2-121">部分載入</span><span class="sxs-lookup"><span data-stu-id="a71b2-121">Partial Loads</span></span>

<span data-ttu-id="a71b2-122">針對載入小於4個 XMVECTOR 專案的各種函式，未定義的「未定義」專案會保留未定義的其他元素。</span><span class="sxs-lookup"><span data-stu-id="a71b2-122">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="a71b2-123">DirectXMath 一律會以0填滿這些額外的元素。</span><span class="sxs-lookup"><span data-stu-id="a71b2-123">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="a71b2-124">移除 Xbox 360 的特定類型</span><span class="sxs-lookup"><span data-stu-id="a71b2-124">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="a71b2-125">DirectXMath 中無法使用下列未使用的數學程式庫類型、函數和常數。</span><span class="sxs-lookup"><span data-stu-id="a71b2-125">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="a71b2-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="a71b2-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="a71b2-127">XMLoadHenDN3 () 、XMLoadHenD3 () 、XMLoadUHenDN3 () 、XMLoadUHenD3 () 、XMLoadDHenN3 () 、XMLoadDHen3 () 、XMLoadUDHenN3 () 、XMLoadUDHen3 () </span><span class="sxs-lookup"><span data-stu-id="a71b2-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="a71b2-128">XMStoreHenDN3 () 、XMStoreHenD3 () 、XMStoreUHenDN3 () 、XMStoreUHenD3 () 、XMStoreDHenN3 () 、XMStoreDHen3 () 、XMStoreUDHenN3 () 、XMStoreUDHen3 () </span><span class="sxs-lookup"><span data-stu-id="a71b2-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="a71b2-129">g \_ XMMaskHenD3、g \_ XMMaskDHen3、g \_ XMAddUHenD3、g \_ XMAddHenD3、g \_ XMAddDHen、g \_ XMMulHenD3、g \_ XMMulDHen3、g \_ XMXorHenD3、g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="a71b2-129">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="a71b2-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="a71b2-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="a71b2-131">XMLoadXIcoN4 () 、XMLoadXIco4 () 、XMLoadIcoN4 () 、XMLoadIco4 () 、XMLoadUIcoN4 () 、XMLoadUIco4 () </span><span class="sxs-lookup"><span data-stu-id="a71b2-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="a71b2-132">XMStoreXIcoN4 () 、XMStoreXIco4 () 、XMStoreIcoN4 () 、XMStoreIco4 () 、XMStoreUIcoN4 () 、XMStoreUIco4 () </span><span class="sxs-lookup"><span data-stu-id="a71b2-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="a71b2-133">g \_ XMMaskIco4、g \_ XMXorXIco4、g \_ XMXorIco4、g \_ XMAddXIco4、g \_ XMAddUIco4、g \_ XMAddIco4、g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="a71b2-133">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="a71b2-134">\_\_vector4i 已被取代。</span><span class="sxs-lookup"><span data-stu-id="a71b2-134">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="a71b2-135">請改用 [**XMVECTORI32**](xmvectori32-data-type.md) 或 [**XMVECTORU32**](xmvectoru32-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="a71b2-135">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="a71b2-136">下列函數和類型已被取代，因為它們只 Xbox 360： XMLoadDecN4、XMStoreDecN4、XMDECN4、XMLoadDec4、XMStoreDec4、XMDEC4、XMLoadXDec4、XMStoreXDec4、XMXDEC4。</span><span class="sxs-lookup"><span data-stu-id="a71b2-136">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="a71b2-137">ARM-霓虹燈內建函式</span><span class="sxs-lookup"><span data-stu-id="a71b2-137">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="a71b2-138">使用此程式碼宣告向量常數，將會針對 SSE 和無內建的未處理數學進行編譯，但使用 ARM 的 DirectXMath 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a71b2-138">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

<span data-ttu-id="a71b2-139">一般而言，我們不建議使用這種方法來初始化 [**XMVECTOR**](xmvector-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="a71b2-139">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="a71b2-140">但是，如果您想要向量常數， [**XMVECTORF32**](xmvectorf32-data-type.md) 類別支援這種初始化樣式，並會自動傳回 **XMVECTOR** 型別，因此您可以在大部分的相同內容中使用 **XMVECTORF32** 。</span><span class="sxs-lookup"><span data-stu-id="a71b2-140">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="a71b2-141">**XMVECTORF32** 類別的任何寫入作業都需要明確參考. v **XMVECTOR** 成員。</span><span class="sxs-lookup"><span data-stu-id="a71b2-141">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="a71b2-142">置換</span><span class="sxs-lookup"><span data-stu-id="a71b2-142">Permute</span></span>

<span data-ttu-id="a71b2-143">在一般向量置換中，「執行程式數學程式庫」具有下列形式：</span><span class="sxs-lookup"><span data-stu-id="a71b2-143">The XNA Math library had the following form for general vector permute:</span></span>

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

<span data-ttu-id="a71b2-144">若為 DirectXMath， **XMVectorPermuteControl** 已被刪除，而 XM \_ 置換 \_ 0x。</span><span class="sxs-lookup"><span data-stu-id="a71b2-144">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="a71b2-145">\_置換 \_ 1Z 常數已重新定義為簡單的0-7 索引。</span><span class="sxs-lookup"><span data-stu-id="a71b2-145">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="a71b2-146">以下是 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)的新簽章：</span><span class="sxs-lookup"><span data-stu-id="a71b2-146">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

<span data-ttu-id="a71b2-147">這個函式不會使用控制字組，而是直接採用4個索引做為參數，也就是使用新的 XM SWIZZLE X 來使其類似于 [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) 函式 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="a71b2-147">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="a71b2-148">\_SWIZZLE \_ ，W 常數定義為簡單的0-3 索引。</span><span class="sxs-lookup"><span data-stu-id="a71b2-148">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> <span data-ttu-id="a71b2-149">針對常數值，有更有效率的方式來執行置換。</span><span class="sxs-lookup"><span data-stu-id="a71b2-149">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="a71b2-150">使用 **範本** 表單，而不是使用 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)的函式形式：</span><span class="sxs-lookup"><span data-stu-id="a71b2-150">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a><span data-ttu-id="a71b2-151">範本表單</span><span class="sxs-lookup"><span data-stu-id="a71b2-151">Template Forms</span></span>

<span data-ttu-id="a71b2-152">一般情況下，使用範本形式的函式形式的下列函式會更有效率，而且可讓程式庫透過範本特製化來執行平臺特定的優化。</span><span class="sxs-lookup"><span data-stu-id="a71b2-152">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a><span data-ttu-id="a71b2-153">消除函式</span><span class="sxs-lookup"><span data-stu-id="a71b2-153">Eliminated Functions</span></span>

| <span data-ttu-id="a71b2-154">刪除函式</span><span class="sxs-lookup"><span data-stu-id="a71b2-154">Eliminated Function</span></span>        | <span data-ttu-id="a71b2-155">取代</span><span class="sxs-lookup"><span data-stu-id="a71b2-155">Replacement</span></span>                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a71b2-156">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="a71b2-156">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="a71b2-157">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="a71b2-157">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| <span data-ttu-id="a71b2-158">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="a71b2-158">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="a71b2-159">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="a71b2-159">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| <span data-ttu-id="a71b2-160">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="a71b2-160">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="a71b2-161">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="a71b2-161">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| <span data-ttu-id="a71b2-162">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="a71b2-162">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="a71b2-163">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="a71b2-163">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| <span data-ttu-id="a71b2-164">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="a71b2-164">XMStoreInt4NC</span></span>              | [<span data-ttu-id="a71b2-165">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="a71b2-165">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| <span data-ttu-id="a71b2-166">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="a71b2-166">XMVector2InBoundsR</span></span>         | <span data-ttu-id="a71b2-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) 嗎？</span><span class="sxs-lookup"><span data-stu-id="a71b2-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="a71b2-168">[XM \_CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) ：0</span><span class="sxs-lookup"><span data-stu-id="a71b2-168">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="a71b2-169">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="a71b2-169">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="a71b2-170">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="a71b2-170">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| <span data-ttu-id="a71b2-171">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="a71b2-171">XMVector3InBoundsR</span></span>         | <span data-ttu-id="a71b2-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) 嗎？</span><span class="sxs-lookup"><span data-stu-id="a71b2-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="a71b2-173">[XM \_CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) ：0</span><span class="sxs-lookup"><span data-stu-id="a71b2-173">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="a71b2-174">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="a71b2-174">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="a71b2-175">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="a71b2-175">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| <span data-ttu-id="a71b2-176">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="a71b2-176">XMVector4InBoundsR</span></span>         | <span data-ttu-id="a71b2-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) 嗎？</span><span class="sxs-lookup"><span data-stu-id="a71b2-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="a71b2-178">[XM \_CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) ：0</span><span class="sxs-lookup"><span data-stu-id="a71b2-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="a71b2-179">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="a71b2-179">XMVectorCosHEst</span></span>            | [<span data-ttu-id="a71b2-180">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="a71b2-180">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| <span data-ttu-id="a71b2-181">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="a71b2-181">XMVectorExpEst</span></span>             | [<span data-ttu-id="a71b2-182">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="a71b2-182">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| <span data-ttu-id="a71b2-183">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="a71b2-183">XMVectorLogEst</span></span>             | [<span data-ttu-id="a71b2-184">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="a71b2-184">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| <span data-ttu-id="a71b2-185">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="a71b2-185">XMVectorPowEst</span></span>             | [<span data-ttu-id="a71b2-186">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="a71b2-186">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| <span data-ttu-id="a71b2-187">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="a71b2-187">XMVectorSinHEst</span></span>            | [<span data-ttu-id="a71b2-188">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="a71b2-188">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| <span data-ttu-id="a71b2-189">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="a71b2-189">XMVectorTanHEst</span></span>            | [<span data-ttu-id="a71b2-190">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="a71b2-190">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a><span data-ttu-id="a71b2-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="a71b2-191">Related topics</span></span>

[<span data-ttu-id="a71b2-192">DirectXMath 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="a71b2-192">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
