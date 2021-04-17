---
description: 使用提供的紅色、綠色和藍色值，初始化色彩。
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: 'D3DCOLOR_XRGB 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386435"
---
# <a name="d3dcolor_xrgb-macro"></a><span data-ttu-id="b3a52-103">D3DCOLOR \_ XRGB 宏</span><span class="sxs-lookup"><span data-stu-id="b3a52-103">D3DCOLOR\_XRGB macro</span></span>

<span data-ttu-id="b3a52-104">使用提供的紅色、綠色和藍色值，初始化色彩。</span><span class="sxs-lookup"><span data-stu-id="b3a52-104">Initializes a color with the supplied red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a52-105">語法</span><span class="sxs-lookup"><span data-stu-id="b3a52-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="b3a52-106">參數</span><span class="sxs-lookup"><span data-stu-id="b3a52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a52-107">*r*</span><span class="sxs-lookup"><span data-stu-id="b3a52-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a52-108">色彩的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="b3a52-108">Red component of the color.</span></span> <span data-ttu-id="b3a52-109">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="b3a52-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="b3a52-110">*G*</span><span class="sxs-lookup"><span data-stu-id="b3a52-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a52-111">色彩的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="b3a52-111">Green component of the color.</span></span> <span data-ttu-id="b3a52-112">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="b3a52-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="b3a52-113">*b*</span><span class="sxs-lookup"><span data-stu-id="b3a52-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a52-114">色彩的藍色元件。</span><span class="sxs-lookup"><span data-stu-id="b3a52-114">Blue component of the color.</span></span> <span data-ttu-id="b3a52-115">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="b3a52-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3a52-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3a52-116">Return value</span></span>

<span data-ttu-id="b3a52-117">傳回對應至所提供 RGB 值的 [**D3DCOLOR**](d3dcolor.md) 值。</span><span class="sxs-lookup"><span data-stu-id="b3a52-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a52-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3a52-118">Requirements</span></span>



| <span data-ttu-id="b3a52-119">需求</span><span class="sxs-lookup"><span data-stu-id="b3a52-119">Requirement</span></span> | <span data-ttu-id="b3a52-120">值</span><span class="sxs-lookup"><span data-stu-id="b3a52-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a52-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b3a52-121">Header</span></span><br/> | <dl> <span data-ttu-id="b3a52-122"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="b3a52-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3a52-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3a52-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a52-124">巨集</span><span class="sxs-lookup"><span data-stu-id="b3a52-124">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="b3a52-125">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="b3a52-125">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="b3a52-126">**D3DCOLOR \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="b3a52-126">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> </dl>

 

 




