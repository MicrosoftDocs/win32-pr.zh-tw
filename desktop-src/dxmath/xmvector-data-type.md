---
description: 用來代表 4 32 位浮點數或整陣列件向量的可移植型別，每個都能以最佳方式對齊，並對應至硬體向量暫存器。
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: 'XMVECTOR 資料類型 (DirectXMath .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992377"
---
# <a name="xmvector-data-type"></a><span data-ttu-id="f270a-103">XMVECTOR 資料類型</span><span class="sxs-lookup"><span data-stu-id="f270a-103">XMVECTOR Data Type</span></span>

<span data-ttu-id="f270a-104">用來代表 4 32 位浮點數或整陣列件向量的可移植型別，每個都能以最佳方式對齊，並對應至硬體向量暫存器。</span><span class="sxs-lookup"><span data-stu-id="f270a-104">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f270a-105">備註</span><span class="sxs-lookup"><span data-stu-id="f270a-105">Remarks</span></span>

<span data-ttu-id="f270a-106">如需在 c + + 中進行程式設計時可使用的其他功能（例如，如函式和運算子）的清單， `XMVECTOR` 請參閱 [XMVECTOR 延伸](ovw-xmvector-extensions.md)模組。</span><span class="sxs-lookup"><span data-stu-id="f270a-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTOR` when programming in C++, see [XMVECTOR Extensions](ovw-xmvector-extensions.md).</span></span>

<span data-ttu-id="f270a-107">在 DirectXMath 程式庫中，為了完全支援可攜性和優化，其 `XMVECTOR` 設計是不透明的型別。</span><span class="sxs-lookup"><span data-stu-id="f270a-107">In the DirectXMath Library, to fully support portability and optimization, `XMVECTOR` is, by design, an opaque type.</span></span> <span data-ttu-id="f270a-108">的實際執行 `XMVECTOR` 相依于平臺。</span><span class="sxs-lookup"><span data-stu-id="f270a-108">The actual implementation of `XMVECTOR` is platform dependent.</span></span>

<span data-ttu-id="f270a-109">一般情況下，程式碼不應該依賴任何特定平臺的特定執行方式的細節 `XMVECTOR` 。</span><span class="sxs-lookup"><span data-stu-id="f270a-109">In general, code should not rely on the specifics of any given platform specific implementation of `XMVECTOR`.</span></span> <span data-ttu-id="f270a-110">平臺特定的執行具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="f270a-110">Platform-specific implementations have these characteristics:</span></span>

-   <span data-ttu-id="f270a-111">它們不是可移植的。</span><span class="sxs-lookup"><span data-stu-id="f270a-111">They are not portable.</span></span>
-   <span data-ttu-id="f270a-112">它們可能會在版本之間變更。</span><span class="sxs-lookup"><span data-stu-id="f270a-112">They may change between releases.</span></span>
-   <span data-ttu-id="f270a-113">Injudicious 使用的實作為詳細資料可能很理想。</span><span class="sxs-lookup"><span data-stu-id="f270a-113">Injudicious use of implementation details may be suboptimal.</span></span>

<span data-ttu-id="f270a-114">開發人員應該使用 DirectXMath 程式庫的 [存取](ovw-xnamath-reference-functions-accessors.md)子、 [載入](ovw-xnamath-reference-functions-load.md)和 [儲存](ovw-xnamath-reference-functions-storage.md) 函式來取得和設定向量，以及使用 [DirectXMath 程式庫4d 向量函數](ovw-xnamath-reference-functions-vector4.md) 來操作它們。</span><span class="sxs-lookup"><span data-stu-id="f270a-114">Developers should use DirectXMath Library's [accessor](ovw-xnamath-reference-functions-accessors.md), [load](ovw-xnamath-reference-functions-load.md), and [store](ovw-xnamath-reference-functions-storage.md) functions to get and set the vectors, and the [DirectXMath Library 4D Vector Functions](ovw-xnamath-reference-functions-vector4.md) to manipulate them.</span></span>

<span data-ttu-id="f270a-115">針對需要如何在不同平臺上執行之詳細資訊的專案 `XMVECTOR` ，請參閱連結 [庫內部](pg-xnamath-internals.md)。</span><span class="sxs-lookup"><span data-stu-id="f270a-115">For projects that need detailed information about how to implement `XMVECTOR` on different platforms, see [Library Internals](pg-xnamath-internals.md).</span></span>

### <a name="compiler-aliases"></a><span data-ttu-id="f270a-116">編譯器別名</span><span class="sxs-lookup"><span data-stu-id="f270a-116">Compiler Aliases</span></span>

<span data-ttu-id="f270a-117">DirectXMath .h 標頭檔會使用物件的別名 `XMVECTOR` ，特別是 **CXMVECTOR** 和 **FXMVECTOR**。</span><span class="sxs-lookup"><span data-stu-id="f270a-117">The DirectXMath.h header file uses aliases to the `XMVECTOR` object, specifically **CXMVECTOR** and **FXMVECTOR**.</span></span> <span data-ttu-id="f270a-118">標頭會使用這些別名，以符合不同編譯器的最佳內嵌呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="f270a-118">The header uses these aliases to comply with the optimal in-line calling conventions of different compilers.</span></span> <span data-ttu-id="f270a-119">大部分使用 DirectXMath 的專案，都足以將這些類型視為的確切別名 `XMVECTOR` 。</span><span class="sxs-lookup"><span data-stu-id="f270a-119">For most projects that use DirectXMath it is sufficient to treat these types as an exact alias to `XMVECTOR`.</span></span>

<span data-ttu-id="f270a-120">例如：</span><span class="sxs-lookup"><span data-stu-id="f270a-120">For example:</span></span>


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



<span data-ttu-id="f270a-121">針對需要不同平臺如何處理其呼叫慣例之詳細資訊的專案，請參閱連結 [庫內部](pg-xnamath-internals.md)。</span><span class="sxs-lookup"><span data-stu-id="f270a-121">For projects that need detailed information about how different platforms handle their calling conventions, see [Library Internals](pg-xnamath-internals.md).</span></span>

<span data-ttu-id="f270a-122">針對 XNAMATH 2.x， `XMVECTOR` 資料類型具有. x、. y、. z、. 和. w 元素成員，這通常會造成效能不佳。</span><span class="sxs-lookup"><span data-stu-id="f270a-122">For XNAMATH 2.x, the `XMVECTOR` data type has .x, .y, .z, .and .w element members, which generally cause poor performance.</span></span> <span data-ttu-id="f270a-123">使用 XM \_ STRICT \_ VECTOR4 型別可讓您加入宣告不透明資料類型的 DirectXMath 定義。</span><span class="sxs-lookup"><span data-stu-id="f270a-123">The use of the XM\_STRICT\_VECTOR4 type provides an opt-in of the DirectXMath definition of an opaque data type.</span></span>

<span data-ttu-id="f270a-124">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="f270a-124">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="f270a-125">平台需求</span><span class="sxs-lookup"><span data-stu-id="f270a-125">Platform Requirements</span></span>

<span data-ttu-id="f270a-126">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="f270a-126">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="f270a-127">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="f270a-127">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="f270a-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="f270a-128">Requirements</span></span>



| <span data-ttu-id="f270a-129">需求</span><span class="sxs-lookup"><span data-stu-id="f270a-129">Requirement</span></span> | <span data-ttu-id="f270a-130">值</span><span class="sxs-lookup"><span data-stu-id="f270a-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f270a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f270a-131">Header</span></span><br/> | <dl> <span data-ttu-id="f270a-132"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="f270a-132"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f270a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f270a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f270a-134">DirectXMath 程式庫類型</span><span class="sxs-lookup"><span data-stu-id="f270a-134">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="f270a-135">**XMVECTORI32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="f270a-135">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="f270a-136">**XMVECTORF32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="f270a-136">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="f270a-137">**XMVECTORU32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="f270a-137">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="f270a-138">**XMVECTORU8 資料類型**</span><span class="sxs-lookup"><span data-stu-id="f270a-138">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="f270a-139">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="f270a-139">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 




