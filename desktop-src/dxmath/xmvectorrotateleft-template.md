---
description: 將向量向左旋轉指定的32位元素數目。
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: 'XMVectorRotateLeft template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000412"
---
# <a name="xmvectorrotateleft-template"></a><span data-ttu-id="dc9f4-103">XMVectorRotateLeft 範本</span><span class="sxs-lookup"><span data-stu-id="dc9f4-103">XMVectorRotateLeft template</span></span>

<span data-ttu-id="dc9f4-104">將向量向左旋轉指定的32位元素數目。</span><span class="sxs-lookup"><span data-stu-id="dc9f4-104">Rotates the vector left by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9f4-105">語法</span><span class="sxs-lookup"><span data-stu-id="dc9f4-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="dc9f4-106">參數</span><span class="sxs-lookup"><span data-stu-id="dc9f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc9f4-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="dc9f4-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="dc9f4-108">\[\]以向量向左旋轉。</span><span class="sxs-lookup"><span data-stu-id="dc9f4-108">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc9f4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc9f4-109">Return Value</span></span>

<span data-ttu-id="dc9f4-110">傳迴旋轉的 [**XMVECTOR**](xmvector-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="dc9f4-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dc9f4-111">備註</span><span class="sxs-lookup"><span data-stu-id="dc9f4-111">Remarks</span></span>

<span data-ttu-id="dc9f4-112">此函式是範本版本的 [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) ，其中 *Elements* 引數是範本值。</span><span class="sxs-lookup"><span data-stu-id="dc9f4-112">This function is a template version of [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="dc9f4-113">`XMVectorRotateLeft`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。</span><span class="sxs-lookup"><span data-stu-id="dc9f4-113">The `XMVectorRotateLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="dc9f4-114">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="dc9f4-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="dc9f4-115">平台需求</span><span class="sxs-lookup"><span data-stu-id="dc9f4-115">Platform Requirements</span></span>

<span data-ttu-id="dc9f4-116">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="dc9f4-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="dc9f4-117">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="dc9f4-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc9f4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc9f4-118">Requirements</span></span>



| <span data-ttu-id="dc9f4-119">需求</span><span class="sxs-lookup"><span data-stu-id="dc9f4-119">Requirement</span></span> | <span data-ttu-id="dc9f4-120">值</span><span class="sxs-lookup"><span data-stu-id="dc9f4-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9f4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="dc9f4-121">Header</span></span><br/> | <dl> <span data-ttu-id="dc9f4-122"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc9f4-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc9f4-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc9f4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9f4-124">DirectXMath 程式庫範本函數</span><span class="sxs-lookup"><span data-stu-id="dc9f4-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="dc9f4-125">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="dc9f4-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="dc9f4-126">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="dc9f4-126">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="dc9f4-127">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="dc9f4-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
