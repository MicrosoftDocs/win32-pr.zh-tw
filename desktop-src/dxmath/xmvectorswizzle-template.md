---
description: Swizzles 向量。
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: 'XMVectorSwizzle template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994892"
---
# <a name="xmvectorswizzle-template"></a><span data-ttu-id="c9e24-103">XMVectorSwizzle 範本</span><span class="sxs-lookup"><span data-stu-id="c9e24-103">XMVectorSwizzle template</span></span>

<span data-ttu-id="c9e24-104">Swizzles 向量。</span><span class="sxs-lookup"><span data-stu-id="c9e24-104">Swizzles a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e24-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9e24-105">Syntax</span></span>

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="c9e24-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9e24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9e24-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="c9e24-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="c9e24-108">\[在 \] 向量中 swizzle。</span><span class="sxs-lookup"><span data-stu-id="c9e24-108">\[in\] Vector to swizzle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9e24-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9e24-109">Return Value</span></span>

<span data-ttu-id="c9e24-110">傳回 swizzled [**XMVECTOR**](xmvector-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="c9e24-110">Returns the swizzled [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9e24-111">備註</span><span class="sxs-lookup"><span data-stu-id="c9e24-111">Remarks</span></span>

<span data-ttu-id="c9e24-112">此函式是 [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle)的範本版本，其中 *Swizzle \** 引數是範本值。</span><span class="sxs-lookup"><span data-stu-id="c9e24-112">This function is a template version of [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) where the *Swizzle\** arguments are template values.</span></span>

<span data-ttu-id="c9e24-113">`XM_SWIZZLE_X`、 `XM_SWIZZLE_Y` 、 `XM_SWIZZLE_Z` 和 `XM_SWIZZLE_W` 都是分別評估為0、1、2和3的常數，以搭配使用 `XMVectorSwizzle` 。</span><span class="sxs-lookup"><span data-stu-id="c9e24-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y`, `XM_SWIZZLE_Z`, and `XM_SWIZZLE_W` are constants which evaluate to 0, 1, 2, and 3 respectively for use with `XMVectorSwizzle`.</span></span> <span data-ttu-id="c9e24-114">這與 `XM_PERMUTE_0X` 、 `XM_PERMUTE_0Y` 、和相同 `XM_PERMUTE_0Z` `XM_PERMUTE_0W` 。</span><span class="sxs-lookup"><span data-stu-id="c9e24-114">This is identical to `XM_PERMUTE_0X`, `XM_PERMUTE_0Y`, `XM_PERMUTE_0Z`, and `XM_PERMUTE_0W`.</span></span>

> [!Note]  
> <span data-ttu-id="c9e24-115">`XMVectorSwizzle`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。</span><span class="sxs-lookup"><span data-stu-id="c9e24-115">The `XMVectorSwizzle` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="c9e24-116">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="c9e24-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="c9e24-117">平台需求</span><span class="sxs-lookup"><span data-stu-id="c9e24-117">Platform Requirements</span></span>

<span data-ttu-id="c9e24-118">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="c9e24-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="c9e24-119">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="c9e24-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9e24-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9e24-120">Requirements</span></span>



| <span data-ttu-id="c9e24-121">需求</span><span class="sxs-lookup"><span data-stu-id="c9e24-121">Requirement</span></span> | <span data-ttu-id="c9e24-122">值</span><span class="sxs-lookup"><span data-stu-id="c9e24-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e24-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c9e24-123">Header</span></span><br/> | <dl> <span data-ttu-id="c9e24-124"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9e24-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9e24-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9e24-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9e24-126">DirectXMath 程式庫範本函數</span><span class="sxs-lookup"><span data-stu-id="c9e24-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="c9e24-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="c9e24-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> </dl>

 

 
