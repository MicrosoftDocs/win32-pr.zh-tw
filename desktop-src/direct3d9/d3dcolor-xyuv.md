---
description: 使用 (y、u、v) 值來初始化色彩。
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: 'D3DCOLOR_XYUV 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853971"
---
# <a name="d3dcolor_xyuv-macro"></a><span data-ttu-id="6c2c1-103">D3DCOLOR \_ XYUV 宏</span><span class="sxs-lookup"><span data-stu-id="6c2c1-103">D3DCOLOR\_XYUV macro</span></span>

<span data-ttu-id="6c2c1-104">使用 (y、u、v) 值來初始化色彩。</span><span class="sxs-lookup"><span data-stu-id="6c2c1-104">Initializes a color with the (y, u, v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c2c1-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c2c1-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="6c2c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c2c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c2c1-107">*y*</span><span class="sxs-lookup"><span data-stu-id="6c2c1-107">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="6c2c1-108">色彩的亮度成分。</span><span class="sxs-lookup"><span data-stu-id="6c2c1-108">Luminance component of the color.</span></span> <span data-ttu-id="6c2c1-109">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="6c2c1-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="6c2c1-110">*u*</span><span class="sxs-lookup"><span data-stu-id="6c2c1-110">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="6c2c1-111">色彩的藍色亮度。</span><span class="sxs-lookup"><span data-stu-id="6c2c1-111">Blue brightness of the color.</span></span> <span data-ttu-id="6c2c1-112">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="6c2c1-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="6c2c1-113">*V*</span><span class="sxs-lookup"><span data-stu-id="6c2c1-113">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="6c2c1-114">色彩的紅色亮度。</span><span class="sxs-lookup"><span data-stu-id="6c2c1-114">Red brightness of the color.</span></span> <span data-ttu-id="6c2c1-115">這個值必須介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="6c2c1-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c2c1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c2c1-116">Return value</span></span>

<span data-ttu-id="6c2c1-117">傳回對應至提供的 (y，u，v) 值的 [**D3DCOLOR**](d3dcolor.md) 值。</span><span class="sxs-lookup"><span data-stu-id="6c2c1-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied (y, u, v) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c2c1-118">備註</span><span class="sxs-lookup"><span data-stu-id="6c2c1-118">Remarks</span></span>

<span data-ttu-id="6c2c1-119">您可以使用下列方程式來轉換成亮度和色彩差異，以將 RGB 色彩縮減為每圖元16位：</span><span class="sxs-lookup"><span data-stu-id="6c2c1-119">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="6c2c1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c2c1-120">Requirements</span></span>



| <span data-ttu-id="6c2c1-121">需求</span><span class="sxs-lookup"><span data-stu-id="6c2c1-121">Requirement</span></span> | <span data-ttu-id="6c2c1-122">值</span><span class="sxs-lookup"><span data-stu-id="6c2c1-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c2c1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6c2c1-123">Header</span></span><br/> | <dl> <span data-ttu-id="6c2c1-124"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c2c1-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c2c1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c2c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2c1-126">巨集</span><span class="sxs-lookup"><span data-stu-id="6c2c1-126">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="6c2c1-127">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="6c2c1-127">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="6c2c1-128">**D3DCOLOR \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="6c2c1-128">**D3DCOLOR\_AYUV**</span></span>](d3dcolor-ayuv.md)
</dt> </dl>

 

 




