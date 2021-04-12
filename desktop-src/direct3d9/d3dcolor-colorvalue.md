---
description: 使用提供的紅色、綠色、藍色和 Alpha 浮點值，初始化色彩。
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: 'D3DCOLOR_COLORVALUE 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696580"
---
# <a name="d3dcolor_colorvalue-macro"></a><span data-ttu-id="49267-103">D3DCOLOR \_ COLORVALUE 宏</span><span class="sxs-lookup"><span data-stu-id="49267-103">D3DCOLOR\_COLORVALUE macro</span></span>

<span data-ttu-id="49267-104">使用提供的紅色、綠色、藍色和 Alpha 浮點值，初始化色彩。</span><span class="sxs-lookup"><span data-stu-id="49267-104">Initializes a color with the supplied red, green, blue, and alpha floating-point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="49267-105">語法</span><span class="sxs-lookup"><span data-stu-id="49267-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a><span data-ttu-id="49267-106">參數</span><span class="sxs-lookup"><span data-stu-id="49267-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49267-107">*r*</span><span class="sxs-lookup"><span data-stu-id="49267-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="49267-108">色彩的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="49267-108">Red component of the color.</span></span> <span data-ttu-id="49267-109">這個值必須是範圍0.0 到1.0 的浮點值。</span><span class="sxs-lookup"><span data-stu-id="49267-109">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="49267-110">*G*</span><span class="sxs-lookup"><span data-stu-id="49267-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="49267-111">色彩的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="49267-111">Green component of the color.</span></span> <span data-ttu-id="49267-112">這個值必須是範圍0.0 到1.0 的浮點值。</span><span class="sxs-lookup"><span data-stu-id="49267-112">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="49267-113">*b*</span><span class="sxs-lookup"><span data-stu-id="49267-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="49267-114">色彩的藍色元件。</span><span class="sxs-lookup"><span data-stu-id="49267-114">Blue component of the color.</span></span> <span data-ttu-id="49267-115">這個值必須是範圍0.0 到1.0 的浮點值。</span><span class="sxs-lookup"><span data-stu-id="49267-115">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="49267-116">*的*</span><span class="sxs-lookup"><span data-stu-id="49267-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="49267-117">色彩的 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="49267-117">Alpha component of the color.</span></span> <span data-ttu-id="49267-118">這個值必須是範圍0.0 到1.0 的浮點值。</span><span class="sxs-lookup"><span data-stu-id="49267-118">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49267-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="49267-119">Return value</span></span>

<span data-ttu-id="49267-120">傳回對應至提供的 RGBA 值的 [**D3DCOLOR**](d3dcolor.md) 值。</span><span class="sxs-lookup"><span data-stu-id="49267-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="49267-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="49267-121">Requirements</span></span>



| <span data-ttu-id="49267-122">需求</span><span class="sxs-lookup"><span data-stu-id="49267-122">Requirement</span></span> | <span data-ttu-id="49267-123">值</span><span class="sxs-lookup"><span data-stu-id="49267-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49267-124">標頭</span><span class="sxs-lookup"><span data-stu-id="49267-124">Header</span></span><br/> | <dl> <span data-ttu-id="49267-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="49267-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49267-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49267-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49267-127">巨集</span><span class="sxs-lookup"><span data-stu-id="49267-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




