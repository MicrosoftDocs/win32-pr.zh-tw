---
description: 將向量向左移位指定數目的32位元素，並使用第二個向量的元素來填滿空的元素。
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: 'XMVectorShiftLeft template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982651"
---
# <a name="xmvectorshiftleft-template"></a><span data-ttu-id="15e4f-103">XMVectorShiftLeft 範本</span><span class="sxs-lookup"><span data-stu-id="15e4f-103">XMVectorShiftLeft template</span></span>

<span data-ttu-id="15e4f-104">將向量向左移位指定數目的32位元素，並使用第二個向量的元素來填滿空的元素。</span><span class="sxs-lookup"><span data-stu-id="15e4f-104">Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e4f-105">語法</span><span class="sxs-lookup"><span data-stu-id="15e4f-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="15e4f-106">參數</span><span class="sxs-lookup"><span data-stu-id="15e4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15e4f-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="15e4f-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="15e4f-108">\[\]以向量向左移。</span><span class="sxs-lookup"><span data-stu-id="15e4f-108">\[in\] Vector to shift left.</span></span>

</dd> <dt>

<span data-ttu-id="15e4f-109"><span id="V2"></span><span id="v2"></span>*2*</span><span class="sxs-lookup"><span data-stu-id="15e4f-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="15e4f-110">\[在中， \] 用來在左移左方元件之後，用來填入該元件的。</span><span class="sxs-lookup"><span data-stu-id="15e4f-110">\[in\] Vector used to fill in the vacated components of V1 after it is shifted left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15e4f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="15e4f-111">Return Value</span></span>

<span data-ttu-id="15e4f-112">傳回移位並填滿 [**XMVECTOR**](xmvector-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="15e4f-112">Returns the shifted and filled in [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="15e4f-113">備註</span><span class="sxs-lookup"><span data-stu-id="15e4f-113">Remarks</span></span>

<span data-ttu-id="15e4f-114">此函式是範本版本的 [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) ，其中 *Elements* 引數是範本值。</span><span class="sxs-lookup"><span data-stu-id="15e4f-114">This function is a template version of [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="15e4f-115">`XMVectorShiftLeft`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。</span><span class="sxs-lookup"><span data-stu-id="15e4f-115">The `XMVectorShiftLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="15e4f-116">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="15e4f-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="15e4f-117">平台需求</span><span class="sxs-lookup"><span data-stu-id="15e4f-117">Platform Requirements</span></span>

<span data-ttu-id="15e4f-118">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="15e4f-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="15e4f-119">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="15e4f-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e4f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="15e4f-120">Requirements</span></span>



| <span data-ttu-id="15e4f-121">需求</span><span class="sxs-lookup"><span data-stu-id="15e4f-121">Requirement</span></span> | <span data-ttu-id="15e4f-122">值</span><span class="sxs-lookup"><span data-stu-id="15e4f-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="15e4f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="15e4f-123">Header</span></span><br/> | <dl> <span data-ttu-id="15e4f-124"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="15e4f-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15e4f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15e4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e4f-126">DirectXMath 程式庫範本函數</span><span class="sxs-lookup"><span data-stu-id="15e4f-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="15e4f-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="15e4f-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="15e4f-128">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="15e4f-128">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="15e4f-129">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="15e4f-129">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> </dl>

 

 
