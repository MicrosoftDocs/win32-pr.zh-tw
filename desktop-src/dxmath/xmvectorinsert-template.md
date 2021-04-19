---
description: 將向量旋轉指定的32位元件數目，並將該結果的選取元素插入另一個向量。
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: 'XMVectorInsert template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990661"
---
# <a name="xmvectorinsert-template"></a><span data-ttu-id="0e2f1-103">XMVectorInsert 範本</span><span class="sxs-lookup"><span data-stu-id="0e2f1-103">XMVectorInsert template</span></span>

<span data-ttu-id="0e2f1-104">將向量旋轉指定的32位元件數目，並將該結果的選取元素插入另一個向量。</span><span class="sxs-lookup"><span data-stu-id="0e2f1-104">Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e2f1-105">語法</span><span class="sxs-lookup"><span data-stu-id="0e2f1-105">Syntax</span></span>

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a><span data-ttu-id="0e2f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="0e2f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e2f1-107"><span id="VD"></span><span id="vd"></span>*Vd*</span><span class="sxs-lookup"><span data-stu-id="0e2f1-107"><span id="VD"></span><span id="vd"></span>*VD*</span></span>
</dt> <dd>

<span data-ttu-id="0e2f1-108">\[\]要插入的向量。</span><span class="sxs-lookup"><span data-stu-id="0e2f1-108">\[in\] Vector to insert into.</span></span>

</dd> <dt>

<span data-ttu-id="0e2f1-109"><span id="VS"></span><span id="vs"></span>*與*</span><span class="sxs-lookup"><span data-stu-id="0e2f1-109"><span id="VS"></span><span id="vs"></span>*VS*</span></span>
</dt> <dd>

<span data-ttu-id="0e2f1-110">\[\]以向量向左旋轉。</span><span class="sxs-lookup"><span data-stu-id="0e2f1-110">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e2f1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e2f1-111">Return Value</span></span>

<span data-ttu-id="0e2f1-112">傳迴旋轉和插入所產生的 [**XMVECTOR**](xmvector-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="0e2f1-112">Returns the [**XMVECTOR**](xmvector-data-type.md) that results from the rotation and insertion.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e2f1-113">備註</span><span class="sxs-lookup"><span data-stu-id="0e2f1-113">Remarks</span></span>

<span data-ttu-id="0e2f1-114">此函數是 [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert)的範本版本，其中 *Select \** 引數是範本值。</span><span class="sxs-lookup"><span data-stu-id="0e2f1-114">This function is a template version of [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) where the *Select\** arguments are template values.</span></span>

<span data-ttu-id="0e2f1-115">為了達到最佳效能， `XMVectorInsert` 應該將的結果指派回 *VD*。</span><span class="sxs-lookup"><span data-stu-id="0e2f1-115">For best performance, the result of `XMVectorInsert` should be assigned back to *VD*.</span></span>

> [!Note]  
> <span data-ttu-id="0e2f1-116">`XMVectorInsert`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。</span><span class="sxs-lookup"><span data-stu-id="0e2f1-116">The `XMVectorInsert` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="0e2f1-117">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="0e2f1-117">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="0e2f1-118">平台需求</span><span class="sxs-lookup"><span data-stu-id="0e2f1-118">Platform Requirements</span></span>

<span data-ttu-id="0e2f1-119">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="0e2f1-119">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="0e2f1-120">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="0e2f1-120">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e2f1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e2f1-121">Requirements</span></span>



| <span data-ttu-id="0e2f1-122">需求</span><span class="sxs-lookup"><span data-stu-id="0e2f1-122">Requirement</span></span> | <span data-ttu-id="0e2f1-123">值</span><span class="sxs-lookup"><span data-stu-id="0e2f1-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e2f1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0e2f1-124">Header</span></span><br/> | <dl> <span data-ttu-id="0e2f1-125"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e2f1-125"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e2f1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e2f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e2f1-127">DirectXMath 程式庫範本函數</span><span class="sxs-lookup"><span data-stu-id="0e2f1-127">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="0e2f1-128">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="0e2f1-128">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="0e2f1-129">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="0e2f1-129">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="0e2f1-130">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="0e2f1-130">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="0e2f1-131">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="0e2f1-131">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
