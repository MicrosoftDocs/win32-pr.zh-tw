---
description: 使用 (a、y、u、v) 值來初始化色彩。
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: 'D3DCOLOR_AYUV 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976468"
---
# <a name="d3dcolor_ayuv-macro"></a><span data-ttu-id="b9eba-103">D3DCOLOR \_ AYUV 宏</span><span class="sxs-lookup"><span data-stu-id="b9eba-103">D3DCOLOR\_AYUV macro</span></span>

<span data-ttu-id="b9eba-104">使用 (a、y、u、v) 值來初始化色彩。</span><span class="sxs-lookup"><span data-stu-id="b9eba-104">Initializes a color using the (a,y,u,v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9eba-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9eba-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="b9eba-106">參數</span><span class="sxs-lookup"><span data-stu-id="b9eba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9eba-107">*的*</span><span class="sxs-lookup"><span data-stu-id="b9eba-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="b9eba-108">色彩的 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="b9eba-108">Alpha component of the color.</span></span> <span data-ttu-id="b9eba-109">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="b9eba-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="b9eba-110">*y*</span><span class="sxs-lookup"><span data-stu-id="b9eba-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="b9eba-111">色彩的亮度成分。</span><span class="sxs-lookup"><span data-stu-id="b9eba-111">Luminance component of the color.</span></span> <span data-ttu-id="b9eba-112">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="b9eba-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="b9eba-113">*u*</span><span class="sxs-lookup"><span data-stu-id="b9eba-113">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="b9eba-114">色彩的藍色亮度。</span><span class="sxs-lookup"><span data-stu-id="b9eba-114">Blue brightness of the color.</span></span> <span data-ttu-id="b9eba-115">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="b9eba-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="b9eba-116">*V*</span><span class="sxs-lookup"><span data-stu-id="b9eba-116">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="b9eba-117">色彩的紅色亮度。</span><span class="sxs-lookup"><span data-stu-id="b9eba-117">Red brightness of the color.</span></span> <span data-ttu-id="b9eba-118">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="b9eba-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9eba-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9eba-119">Return value</span></span>

<span data-ttu-id="b9eba-120">傳回對應至提供之 ARGB 值的 [D3DCOLOR](d3dcolor.md) 值。</span><span class="sxs-lookup"><span data-stu-id="b9eba-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9eba-121">備註</span><span class="sxs-lookup"><span data-stu-id="b9eba-121">Remarks</span></span>

<span data-ttu-id="b9eba-122">您可以使用下列方程式來轉換成亮度和色彩差異，以將 RGB 色彩縮減為每圖元16位：</span><span class="sxs-lookup"><span data-stu-id="b9eba-122">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="b9eba-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9eba-123">Requirements</span></span>



| <span data-ttu-id="b9eba-124">需求</span><span class="sxs-lookup"><span data-stu-id="b9eba-124">Requirement</span></span> | <span data-ttu-id="b9eba-125">值</span><span class="sxs-lookup"><span data-stu-id="b9eba-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9eba-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b9eba-126">Header</span></span><br/> | <dl> <span data-ttu-id="b9eba-127"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9eba-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9eba-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9eba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9eba-129">巨集</span><span class="sxs-lookup"><span data-stu-id="b9eba-129">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="b9eba-130">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="b9eba-130">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="b9eba-131">**D3DCOLOR \_ XYUV**</span><span class="sxs-lookup"><span data-stu-id="b9eba-131">**D3DCOLOR\_XYUV**</span></span>](d3dcolor-xyuv.md)
</dt> </dl>

 

 




