---
description: Permutes 兩個向量的元件來建立新的向量。
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: 'XMVectorPermute template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990831"
---
# <a name="xmvectorpermute-template"></a><span data-ttu-id="7af22-103">XMVectorPermute 範本</span><span class="sxs-lookup"><span data-stu-id="7af22-103">XMVectorPermute template</span></span>

<span data-ttu-id="7af22-104">Permutes 兩個向量的元件來建立新的向量。</span><span class="sxs-lookup"><span data-stu-id="7af22-104">Permutes the components of two vectors to create a new vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af22-105">語法</span><span class="sxs-lookup"><span data-stu-id="7af22-105">Syntax</span></span>

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="7af22-106">參數</span><span class="sxs-lookup"><span data-stu-id="7af22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af22-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="7af22-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="7af22-108">\[\]第一個向量。</span><span class="sxs-lookup"><span data-stu-id="7af22-108">\[in\] First vector.</span></span>

</dd> <dt>

<span data-ttu-id="7af22-109"><span id="V2"></span><span id="v2"></span>*2*</span><span class="sxs-lookup"><span data-stu-id="7af22-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="7af22-110">\[\]第二個向量。</span><span class="sxs-lookup"><span data-stu-id="7af22-110">\[in\] Second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af22-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7af22-111">Return Value</span></span>

<span data-ttu-id="7af22-112">傳回合並來源向量所產生的排列向量。</span><span class="sxs-lookup"><span data-stu-id="7af22-112">Returns the permuted vector that resulted from combining the source vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af22-113">備註</span><span class="sxs-lookup"><span data-stu-id="7af22-113">Remarks</span></span>

<span data-ttu-id="7af22-114">如果所有4個索引只參考單一向量 (也就是它們全都在0-3 範圍內，或在 4-7) 的所有範圍內，請改用 [**XMVectorSwizzle**](xmvectorswizzle-template.md) 來提升效能。</span><span class="sxs-lookup"><span data-stu-id="7af22-114">If all 4 indices reference only a single vector (i.e. they are all in the range 0-3 or all in the range 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) instead for better performance.</span></span>

<span data-ttu-id="7af22-115">請注意，程式庫會在某些平臺上使用範本特製化，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="7af22-115">Note the library makes use of template specializations on some platforms to improve performance.</span></span> <span data-ttu-id="7af22-116">並非每個可能的鏡像案例都是針對這些特殊情況所執行，因此最好是 permutes，其中產生之向量的 X 元素來自 V1 參數，而不是 V2 參數。</span><span class="sxs-lookup"><span data-stu-id="7af22-116">Not every possible mirror case is implemented for these special cases, so prefer permutes where the X element of the resulting vector comes from the V1 parameter rather than the V2 parameter.</span></span> <span data-ttu-id="7af22-117">例如，偏好使用 `XMVectorPermute<0,1,4,5>(A,B);` to `XMVectorPermute(4,5,0,1)(B,A);` 。</span><span class="sxs-lookup"><span data-stu-id="7af22-117">For example, prefer using `XMVectorPermute<0,1,4,5>(A,B);` to `XMVectorPermute(4,5,0,1)(B,A);`.</span></span>

<span data-ttu-id="7af22-118">此函式是 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)的範本版本，其中 *置換 \** 引數是範本值。</span><span class="sxs-lookup"><span data-stu-id="7af22-118">This function is a template version of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) where the *Permute\** arguments are template values.</span></span>

<span data-ttu-id="7af22-119">提供 [了 \_ XM \_ 置換](ovw-xnamath-reference-constants.md)常數作為 *PermuteX*、*PermuteY*、*PermuteZ* 和 *PermuteW* 的輸入值使用。</span><span class="sxs-lookup"><span data-stu-id="7af22-119">The [XM\_PERMUTE\_](ovw-xnamath-reference-constants.md) constants are provided to use as input values for *PermuteX*,*PermuteY*,*PermuteZ*, and *PermuteW*.</span></span>

> [!Note]  
> <span data-ttu-id="7af22-120">`XMVectorPermute`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。</span><span class="sxs-lookup"><span data-stu-id="7af22-120">The `XMVectorPermute` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="7af22-121">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="7af22-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="7af22-122">平台需求</span><span class="sxs-lookup"><span data-stu-id="7af22-122">Platform Requirements</span></span>

<span data-ttu-id="7af22-123">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="7af22-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="7af22-124">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="7af22-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af22-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7af22-125">Requirements</span></span>



| <span data-ttu-id="7af22-126">需求</span><span class="sxs-lookup"><span data-stu-id="7af22-126">Requirement</span></span> | <span data-ttu-id="7af22-127">值</span><span class="sxs-lookup"><span data-stu-id="7af22-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af22-128">標頭</span><span class="sxs-lookup"><span data-stu-id="7af22-128">Header</span></span><br/> | <dl> <span data-ttu-id="7af22-129"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="7af22-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7af22-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7af22-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af22-131">DirectXMath 程式庫範本函數</span><span class="sxs-lookup"><span data-stu-id="7af22-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="7af22-132">**XMVectorSwizzle**</span><span class="sxs-lookup"><span data-stu-id="7af22-132">**XMVectorSwizzle**</span></span>](xmvectorswizzle-template.md)
</dt> </dl>

 

 
