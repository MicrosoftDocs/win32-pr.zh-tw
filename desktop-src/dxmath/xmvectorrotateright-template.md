---
description: 將向量向右旋轉指定的32位元素數目。
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: 'XMVectorRotateRight template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990830"
---
# <a name="xmvectorrotateright-template"></a><span data-ttu-id="5fc93-103">XMVectorRotateRight 範本</span><span class="sxs-lookup"><span data-stu-id="5fc93-103">XMVectorRotateRight template</span></span>

<span data-ttu-id="5fc93-104">將向量向右旋轉指定的32位元素數目。</span><span class="sxs-lookup"><span data-stu-id="5fc93-104">Rotates the vector right by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc93-105">語法</span><span class="sxs-lookup"><span data-stu-id="5fc93-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="5fc93-106">參數</span><span class="sxs-lookup"><span data-stu-id="5fc93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc93-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="5fc93-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="5fc93-108">\[\]以向量向右旋轉。</span><span class="sxs-lookup"><span data-stu-id="5fc93-108">\[in\] Vector to rotate right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc93-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fc93-109">Return Value</span></span>

<span data-ttu-id="5fc93-110">傳迴旋轉的 [**XMVECTOR**](xmvector-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5fc93-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc93-111">備註</span><span class="sxs-lookup"><span data-stu-id="5fc93-111">Remarks</span></span>

<span data-ttu-id="5fc93-112">此函式是範本版本的 [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) ，其中 *Elements* 引數是範本值。</span><span class="sxs-lookup"><span data-stu-id="5fc93-112">This function is a template version of [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="5fc93-113">`XMVectorRotateRight`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。</span><span class="sxs-lookup"><span data-stu-id="5fc93-113">The `XMVectorRotateRight` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="5fc93-114">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="5fc93-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="5fc93-115">平台需求</span><span class="sxs-lookup"><span data-stu-id="5fc93-115">Platform Requirements</span></span>

<span data-ttu-id="5fc93-116">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="5fc93-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="5fc93-117">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="5fc93-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc93-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fc93-118">Requirements</span></span>



| <span data-ttu-id="5fc93-119">需求</span><span class="sxs-lookup"><span data-stu-id="5fc93-119">Requirement</span></span> | <span data-ttu-id="5fc93-120">值</span><span class="sxs-lookup"><span data-stu-id="5fc93-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc93-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5fc93-121">Header</span></span><br/> | <dl> <span data-ttu-id="5fc93-122"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="5fc93-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc93-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fc93-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc93-124">DirectXMath 程式庫範本函數</span><span class="sxs-lookup"><span data-stu-id="5fc93-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="5fc93-125">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="5fc93-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="5fc93-126">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="5fc93-126">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="5fc93-127">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="5fc93-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
