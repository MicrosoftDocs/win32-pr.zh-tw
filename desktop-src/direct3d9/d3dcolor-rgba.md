---
description: 使用提供的紅色、綠色、藍色和 Alpha 值，初始化色彩。
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: 'D3DCOLOR_RGBA 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988581"
---
# <a name="d3dcolor_rgba-macro"></a><span data-ttu-id="164c4-103">D3DCOLOR \_ RGBA 宏</span><span class="sxs-lookup"><span data-stu-id="164c4-103">D3DCOLOR\_RGBA macro</span></span>

<span data-ttu-id="164c4-104">使用提供的紅色、綠色、藍色和 Alpha 值，初始化色彩。</span><span class="sxs-lookup"><span data-stu-id="164c4-104">Initializes a color with the supplied red, green, blue, and alpha values.</span></span>

## <a name="syntax"></a><span data-ttu-id="164c4-105">語法</span><span class="sxs-lookup"><span data-stu-id="164c4-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a><span data-ttu-id="164c4-106">參數</span><span class="sxs-lookup"><span data-stu-id="164c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="164c4-107">*r*</span><span class="sxs-lookup"><span data-stu-id="164c4-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="164c4-108">色彩的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="164c4-108">Red component of the color.</span></span> <span data-ttu-id="164c4-109">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="164c4-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="164c4-110">*G*</span><span class="sxs-lookup"><span data-stu-id="164c4-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="164c4-111">色彩的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="164c4-111">Green component of the color.</span></span> <span data-ttu-id="164c4-112">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="164c4-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="164c4-113">*b*</span><span class="sxs-lookup"><span data-stu-id="164c4-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="164c4-114">色彩的藍色元件。</span><span class="sxs-lookup"><span data-stu-id="164c4-114">Blue component of the color.</span></span> <span data-ttu-id="164c4-115">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="164c4-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="164c4-116">*的*</span><span class="sxs-lookup"><span data-stu-id="164c4-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="164c4-117">色彩的 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="164c4-117">Alpha component of the color.</span></span> <span data-ttu-id="164c4-118">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="164c4-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="164c4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="164c4-119">Return value</span></span>

<span data-ttu-id="164c4-120">傳回對應至提供的 RGBA 值的 [**D3DCOLOR**](d3dcolor.md) 值。</span><span class="sxs-lookup"><span data-stu-id="164c4-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="164c4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="164c4-121">Requirements</span></span>



| <span data-ttu-id="164c4-122">需求</span><span class="sxs-lookup"><span data-stu-id="164c4-122">Requirement</span></span> | <span data-ttu-id="164c4-123">值</span><span class="sxs-lookup"><span data-stu-id="164c4-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="164c4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="164c4-124">Header</span></span><br/> | <dl> <span data-ttu-id="164c4-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="164c4-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="164c4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="164c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="164c4-127">巨集</span><span class="sxs-lookup"><span data-stu-id="164c4-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="164c4-128">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="164c4-128">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="164c4-129">**D3DCOLOR \_ XRGB**</span><span class="sxs-lookup"><span data-stu-id="164c4-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




