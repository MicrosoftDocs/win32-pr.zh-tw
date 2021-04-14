---
description: 使用提供的 Alpha、紅色、綠色及藍色值，初始化色彩。
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: 'D3DCOLOR_ARGB 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322747"
---
# <a name="d3dcolor_argb-macro"></a><span data-ttu-id="a6168-103">D3DCOLOR \_ ARGB 宏</span><span class="sxs-lookup"><span data-stu-id="a6168-103">D3DCOLOR\_ARGB macro</span></span>

<span data-ttu-id="a6168-104">使用提供的 Alpha、紅色、綠色及藍色值，初始化色彩。</span><span class="sxs-lookup"><span data-stu-id="a6168-104">Initializes a color with the supplied alpha, red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6168-105">語法</span><span class="sxs-lookup"><span data-stu-id="a6168-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="a6168-106">參數</span><span class="sxs-lookup"><span data-stu-id="a6168-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6168-107">*的*</span><span class="sxs-lookup"><span data-stu-id="a6168-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="a6168-108">色彩的 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="a6168-108">Alpha component of the color.</span></span> <span data-ttu-id="a6168-109">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="a6168-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a6168-110">*r*</span><span class="sxs-lookup"><span data-stu-id="a6168-110">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="a6168-111">色彩的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="a6168-111">Red component of the color.</span></span> <span data-ttu-id="a6168-112">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="a6168-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a6168-113">*G*</span><span class="sxs-lookup"><span data-stu-id="a6168-113">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="a6168-114">色彩的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="a6168-114">Green component of the color.</span></span> <span data-ttu-id="a6168-115">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="a6168-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a6168-116">*b*</span><span class="sxs-lookup"><span data-stu-id="a6168-116">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="a6168-117">色彩的藍色元件。</span><span class="sxs-lookup"><span data-stu-id="a6168-117">Blue component of the color.</span></span> <span data-ttu-id="a6168-118">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="a6168-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6168-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6168-119">Return value</span></span>

<span data-ttu-id="a6168-120">傳回對應至提供之 ARGB 值的 [D3DCOLOR](d3dcolor.md) 值。</span><span class="sxs-lookup"><span data-stu-id="a6168-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6168-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6168-121">Requirements</span></span>



| <span data-ttu-id="a6168-122">需求</span><span class="sxs-lookup"><span data-stu-id="a6168-122">Requirement</span></span> | <span data-ttu-id="a6168-123">值</span><span class="sxs-lookup"><span data-stu-id="a6168-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6168-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a6168-124">Header</span></span><br/> | <dl> <span data-ttu-id="a6168-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6168-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6168-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6168-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6168-127">巨集</span><span class="sxs-lookup"><span data-stu-id="a6168-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="a6168-128">**D3DCOLOR \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="a6168-128">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> <dt>

[<span data-ttu-id="a6168-129">**D3DCOLOR \_ XRGB**</span><span class="sxs-lookup"><span data-stu-id="a6168-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




