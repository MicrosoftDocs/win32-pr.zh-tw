---
description: 本總覽說明使用 [DirectXMath] 程式庫將現有程式碼遷移至程式庫所需的變更。
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: 從「設備」數學程式庫進行程式碼遷移
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c446165d3d0b6b7303424959f96ddf48bc75b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512688"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="61d1a-103">從「設備」數學程式庫進行程式碼遷移</span><span class="sxs-lookup"><span data-stu-id="61d1a-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="61d1a-104">本總覽說明使用 [DirectXMath] 程式庫將現有程式碼遷移至程式庫所需的變更。</span><span class="sxs-lookup"><span data-stu-id="61d1a-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

-   [<span data-ttu-id="61d1a-105">標頭變更</span><span class="sxs-lookup"><span data-stu-id="61d1a-105">Header Changes</span></span>](#header-changes)
-   [<span data-ttu-id="61d1a-106">常數變更</span><span class="sxs-lookup"><span data-stu-id="61d1a-106">Constant Changes</span></span>](#constant-changes)
-   [<span data-ttu-id="61d1a-107">命名空間</span><span class="sxs-lookup"><span data-stu-id="61d1a-107">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="61d1a-108">部分載入</span><span class="sxs-lookup"><span data-stu-id="61d1a-108">Partial Loads</span></span>](#partial-loads)
-   [<span data-ttu-id="61d1a-109">移除 Xbox 360 的特定類型</span><span class="sxs-lookup"><span data-stu-id="61d1a-109">Removal of Xbox 360 Specific Types</span></span>](#removal-of-xbox-360-specific-types)
-   [<span data-ttu-id="61d1a-110">ARM-霓虹燈內建函式</span><span class="sxs-lookup"><span data-stu-id="61d1a-110">ARM-NEON Intrinsics</span></span>](#arm-neon-intrinsics)
-   [<span data-ttu-id="61d1a-111">置換</span><span class="sxs-lookup"><span data-stu-id="61d1a-111">Permute</span></span>](#permute)
-   [<span data-ttu-id="61d1a-112">範本表單</span><span class="sxs-lookup"><span data-stu-id="61d1a-112">Template Forms</span></span>](#template-forms)
-   [<span data-ttu-id="61d1a-113">消除函式</span><span class="sxs-lookup"><span data-stu-id="61d1a-113">Eliminated Functions</span></span>](#eliminated-functions)
-   [<span data-ttu-id="61d1a-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="61d1a-114">Related topics</span></span>](#related-topics)

## <a name="header-changes"></a><span data-ttu-id="61d1a-115">標頭變更</span><span class="sxs-lookup"><span data-stu-id="61d1a-115">Header Changes</span></span>

<span data-ttu-id="61d1a-116">DirectXMath 程式庫會使用一組新的標頭。</span><span class="sxs-lookup"><span data-stu-id="61d1a-116">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="61d1a-117">以 DirectXMath 取代 xnamath .h 標頭，並為「GPU 已封裝」類型新增 DirectXPackedVector。</span><span class="sxs-lookup"><span data-stu-id="61d1a-117">Replace the xnamath.h header with DirectXMath.h and add DirectXPackedVector.h for the “GPU packed” types.</span></span>

<span data-ttu-id="61d1a-118">Xnacollision 中 DirectX SDK 碰撞範例中的周框類型現在是 DirectXCollision 中 DirectXMath 程式庫的一部分。</span><span class="sxs-lookup"><span data-stu-id="61d1a-118">The bounding types from the DirectX SDK Collision sample in xnacollision.h is now part of the DirectXMath library in DirectXCollision.h.</span></span> <span data-ttu-id="61d1a-119">這些已修改為使用 c + + 類別，而不是 C 樣式的 API。</span><span class="sxs-lookup"><span data-stu-id="61d1a-119">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="61d1a-120">常數變更</span><span class="sxs-lookup"><span data-stu-id="61d1a-120">Constant Changes</span></span>

<span data-ttu-id="61d1a-121">XNAMATH \_ 版本 (200、201、202、203、204等) 已取代為 DIRECXTMATH \_ 版本 (300、301、302、303等) 。</span><span class="sxs-lookup"><span data-stu-id="61d1a-121">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!Note]  
> <span data-ttu-id="61d1a-122">DirectXMath 3.00 和3.02 隨附 Windows SDK 的初步版本。</span><span class="sxs-lookup"><span data-stu-id="61d1a-122">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="61d1a-123">DirectXMath 3.03 是 Windows 8 SDK 的最終版本。</span><span class="sxs-lookup"><span data-stu-id="61d1a-123">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

 

## <a name="namespaces"></a><span data-ttu-id="61d1a-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="61d1a-124">Namespaces</span></span>

<span data-ttu-id="61d1a-125">DirectXMath 程式庫會使用 c + + 命名空間來組織類型。</span><span class="sxs-lookup"><span data-stu-id="61d1a-125">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="61d1a-126">只有全域命名空間才會使用未使用的運算。</span><span class="sxs-lookup"><span data-stu-id="61d1a-126">XNA Math used only the global namespace.</span></span> <span data-ttu-id="61d1a-127">DirectXMath 型別在具有「DirectX」或「DirectX：:P ackedVector」命名空間中的常見情況。</span><span class="sxs-lookup"><span data-stu-id="61d1a-127">The DirectXMath types in common with XNA Math are in the “DirectX” or the “DirectX::PackedVector” namespace.</span></span>

<span data-ttu-id="61d1a-128">在 c + + 原始程式檔中，簡單的解決方案是加入 ' using ' 語句：</span><span class="sxs-lookup"><span data-stu-id="61d1a-128">In C++ source files, a simple solution is to add ‘using’ statements:</span></span>


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



<span data-ttu-id="61d1a-129">若為標頭，則不會將它視為「最佳做法」來加入 using 語句。</span><span class="sxs-lookup"><span data-stu-id="61d1a-129">For headers, it is not considered ‘best practice’ to add using statements.</span></span> <span data-ttu-id="61d1a-130">請改為新增完整命名空間：</span><span class="sxs-lookup"><span data-stu-id="61d1a-130">Instead, add fully qualified namespaces:</span></span>


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a><span data-ttu-id="61d1a-131">部分載入</span><span class="sxs-lookup"><span data-stu-id="61d1a-131">Partial Loads</span></span>

<span data-ttu-id="61d1a-132">針對載入小於4個 XMVECTOR 專案的各種函式，未定義的「未定義」專案會保留未定義的其他元素。</span><span class="sxs-lookup"><span data-stu-id="61d1a-132">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="61d1a-133">DirectXMath 一律會以0填滿這些額外的元素。</span><span class="sxs-lookup"><span data-stu-id="61d1a-133">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="61d1a-134">移除 Xbox 360 的特定類型</span><span class="sxs-lookup"><span data-stu-id="61d1a-134">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="61d1a-135">DirectXMath 中無法使用下列未使用的數學程式庫類型、函數和常數。</span><span class="sxs-lookup"><span data-stu-id="61d1a-135">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="61d1a-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="61d1a-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="61d1a-137">XMLoadHenDN3 () 、XMLoadHenD3 () 、XMLoadUHenDN3 () 、XMLoadUHenD3 () 、XMLoadDHenN3 () 、XMLoadDHen3 () 、XMLoadUDHenN3 () 、XMLoadUDHen3 () </span><span class="sxs-lookup"><span data-stu-id="61d1a-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="61d1a-138">XMStoreHenDN3 () 、XMStoreHenD3 () 、XMStoreUHenDN3 () 、XMStoreUHenD3 () 、XMStoreDHenN3 () 、XMStoreDHen3 () 、XMStoreUDHenN3 () 、XMStoreUDHen3 () </span><span class="sxs-lookup"><span data-stu-id="61d1a-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="61d1a-139">g \_ XMMaskHenD3、g \_ XMMaskDHen3、g \_ XMAddUHenD3、g \_ XMAddHenD3、g \_ XMAddDHen、g \_ XMMulHenD3、g \_ XMMulDHen3、g \_ XMXorHenD3、g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="61d1a-139">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="61d1a-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="61d1a-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="61d1a-141">XMLoadXIcoN4 () 、XMLoadXIco4 () 、XMLoadIcoN4 () 、XMLoadIco4 () 、XMLoadUIcoN4 () 、XMLoadUIco4 () </span><span class="sxs-lookup"><span data-stu-id="61d1a-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="61d1a-142">XMStoreXIcoN4 () 、XMStoreXIco4 () 、XMStoreIcoN4 () 、XMStoreIco4 () 、XMStoreUIcoN4 () 、XMStoreUIco4 () </span><span class="sxs-lookup"><span data-stu-id="61d1a-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="61d1a-143">g \_ XMMaskIco4、g \_ XMXorXIco4、g \_ XMXorIco4、g \_ XMAddXIco4、g \_ XMAddUIco4、g \_ XMAddIco4、g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="61d1a-143">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="61d1a-144">\_\_vector4i 已被取代。</span><span class="sxs-lookup"><span data-stu-id="61d1a-144">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="61d1a-145">請改用 [**XMVECTORI32**](xmvectori32-data-type.md) 或 [**XMVECTORU32**](xmvectoru32-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="61d1a-145">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="61d1a-146">下列函數和類型已被取代，因為它們只 Xbox 360： XMLoadDecN4、XMStoreDecN4、XMDECN4、XMLoadDec4、XMStoreDec4、XMDEC4、XMLoadXDec4、XMStoreXDec4、XMXDEC4。</span><span class="sxs-lookup"><span data-stu-id="61d1a-146">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="61d1a-147">ARM-霓虹燈內建函式</span><span class="sxs-lookup"><span data-stu-id="61d1a-147">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="61d1a-148">使用此程式碼宣告向量常數，將會針對 SSE 和無內建的未處理數學進行編譯，但使用 ARM 的 DirectXMath 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="61d1a-148">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



<span data-ttu-id="61d1a-149">一般而言，我們不建議使用這種方法來初始化 [**XMVECTOR**](xmvector-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="61d1a-149">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="61d1a-150">但是，如果您想要向量常數， [**XMVECTORF32**](xmvectorf32-data-type.md) 類別支援這種初始化樣式，並會自動傳回 **XMVECTOR** 型別，因此您可以在大部分的相同內容中使用 **XMVECTORF32** 。</span><span class="sxs-lookup"><span data-stu-id="61d1a-150">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="61d1a-151">**XMVECTORF32** 類別的任何寫入作業都需要明確參考. v **XMVECTOR** 成員。</span><span class="sxs-lookup"><span data-stu-id="61d1a-151">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="61d1a-152">置換</span><span class="sxs-lookup"><span data-stu-id="61d1a-152">Permute</span></span>

<span data-ttu-id="61d1a-153">在一般向量置換中，「執行程式數學程式庫」具有下列形式：</span><span class="sxs-lookup"><span data-stu-id="61d1a-153">The XNA Math library had the following form for general vector permute:</span></span>


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



<span data-ttu-id="61d1a-154">若為 DirectXMath， **XMVectorPermuteControl** 已被刪除，而 XM \_ 置換 \_ 0x。</span><span class="sxs-lookup"><span data-stu-id="61d1a-154">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="61d1a-155">\_置換 \_ 1Z 常數已重新定義為簡單的0-7 索引。</span><span class="sxs-lookup"><span data-stu-id="61d1a-155">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="61d1a-156">以下是 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)的新簽章：</span><span class="sxs-lookup"><span data-stu-id="61d1a-156">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



<span data-ttu-id="61d1a-157">這個函式不會使用控制字組，而是直接採用4個索引做為參數，也就是使用新的 XM SWIZZLE X 來使其類似于 [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) 函式 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="61d1a-157">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="61d1a-158">\_SWIZZLE \_ ，W 常數定義為簡單的0-3 索引。</span><span class="sxs-lookup"><span data-stu-id="61d1a-158">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> <span data-ttu-id="61d1a-159">針對常數值，有更有效率的方式來執行置換。</span><span class="sxs-lookup"><span data-stu-id="61d1a-159">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="61d1a-160">使用 **範本** 表單，而不是使用 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)的函式形式：</span><span class="sxs-lookup"><span data-stu-id="61d1a-160">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="template-forms"></a><span data-ttu-id="61d1a-161">範本表單</span><span class="sxs-lookup"><span data-stu-id="61d1a-161">Template Forms</span></span>
>
> <span data-ttu-id="61d1a-162">一般情況下，使用範本形式的函式形式的下列函式會更有效率，而且可讓程式庫透過範本特製化來執行平臺特定的優化。</span><span class="sxs-lookup"><span data-stu-id="61d1a-162">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
>     XMVECTOR XMVectorSwizzle(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateLeft(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateRight(FXMVECTOR V)
>
> template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
>     XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="eliminated-functions"></a><span data-ttu-id="61d1a-163">消除函式</span><span class="sxs-lookup"><span data-stu-id="61d1a-163">Eliminated Functions</span></span>
>
> 
>
> | <span data-ttu-id="61d1a-164">刪除函式</span><span class="sxs-lookup"><span data-stu-id="61d1a-164">Eliminated Function</span></span>        | <span data-ttu-id="61d1a-165">取代</span><span class="sxs-lookup"><span data-stu-id="61d1a-165">Replacement</span></span>                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | <span data-ttu-id="61d1a-166">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="61d1a-166">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="61d1a-167">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="61d1a-167">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | <span data-ttu-id="61d1a-168">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="61d1a-168">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="61d1a-169">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="61d1a-169">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | <span data-ttu-id="61d1a-170">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="61d1a-170">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="61d1a-171">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="61d1a-171">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | <span data-ttu-id="61d1a-172">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="61d1a-172">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="61d1a-173">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="61d1a-173">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | <span data-ttu-id="61d1a-174">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="61d1a-174">XMStoreInt4NC</span></span>              | [<span data-ttu-id="61d1a-175">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="61d1a-175">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | <span data-ttu-id="61d1a-176">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="61d1a-176">XMVector2InBoundsR</span></span>         | <span data-ttu-id="61d1a-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) 嗎？</span><span class="sxs-lookup"><span data-stu-id="61d1a-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="61d1a-178">[XM \_CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) ：0</span><span class="sxs-lookup"><span data-stu-id="61d1a-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="61d1a-179">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="61d1a-179">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="61d1a-180">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="61d1a-180">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | <span data-ttu-id="61d1a-181">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="61d1a-181">XMVector3InBoundsR</span></span>         | <span data-ttu-id="61d1a-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) 嗎？</span><span class="sxs-lookup"><span data-stu-id="61d1a-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="61d1a-183">[XM \_CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) ：0</span><span class="sxs-lookup"><span data-stu-id="61d1a-183">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="61d1a-184">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="61d1a-184">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="61d1a-185">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="61d1a-185">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | <span data-ttu-id="61d1a-186">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="61d1a-186">XMVector4InBoundsR</span></span>         | <span data-ttu-id="61d1a-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) 嗎？</span><span class="sxs-lookup"><span data-stu-id="61d1a-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="61d1a-188">[XM \_CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) ：0</span><span class="sxs-lookup"><span data-stu-id="61d1a-188">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="61d1a-189">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="61d1a-189">XMVectorCosHEst</span></span>            | [<span data-ttu-id="61d1a-190">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="61d1a-190">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | <span data-ttu-id="61d1a-191">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="61d1a-191">XMVectorExpEst</span></span>             | [<span data-ttu-id="61d1a-192">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="61d1a-192">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | <span data-ttu-id="61d1a-193">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="61d1a-193">XMVectorLogEst</span></span>             | [<span data-ttu-id="61d1a-194">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="61d1a-194">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | <span data-ttu-id="61d1a-195">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="61d1a-195">XMVectorPowEst</span></span>             | [<span data-ttu-id="61d1a-196">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="61d1a-196">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | <span data-ttu-id="61d1a-197">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="61d1a-197">XMVectorSinHEst</span></span>            | [<span data-ttu-id="61d1a-198">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="61d1a-198">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | <span data-ttu-id="61d1a-199">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="61d1a-199">XMVectorTanHEst</span></span>            | [<span data-ttu-id="61d1a-200">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="61d1a-200">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a><span data-ttu-id="61d1a-201">相關主題</span><span class="sxs-lookup"><span data-stu-id="61d1a-201">Related topics</span></span>
>
> <dl> <dt>

[<span data-ttu-id="61d1a-202">DirectXMath 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="61d1a-202">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
