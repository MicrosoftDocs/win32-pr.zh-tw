---
description: 定義頂點著色器的取樣器紋理類型。
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: 'D3DSAMPLER_TEXTURE_TYPE 列舉 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386426"
---
# <a name="d3dsampler_texture_type-enumeration"></a><span data-ttu-id="ea4f7-103">D3DSAMPLER \_ 紋理 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="ea4f7-103">D3DSAMPLER\_TEXTURE\_TYPE enumeration</span></span>

<span data-ttu-id="ea4f7-104">定義頂點著色器的取樣器紋理類型。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-104">Defines the sampler texture types for vertex shaders.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea4f7-105">Syntax</span></span>


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ea4f7-106">常數</span><span class="sxs-lookup"><span data-stu-id="ea4f7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ea4f7-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="ea4f7-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ea4f7-108">未初始化的值。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-108">Uninitialized value.</span></span> <span data-ttu-id="ea4f7-109">這個元素的值是 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-109">The value of this element is 0 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="ea4f7-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2d**</span><span class="sxs-lookup"><span data-stu-id="ea4f7-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT\_2D**</span></span>
</dt> <dd>

<span data-ttu-id="ea4f7-111">宣告2D 材質。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-111">Declaring a 2D texture.</span></span> <span data-ttu-id="ea4f7-112">此元素的值為 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-112">The value of this element is 2 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="ea4f7-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT \_ CUBE**</span><span class="sxs-lookup"><span data-stu-id="ea4f7-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT\_CUBE**</span></span>
</dt> <dd>

<span data-ttu-id="ea4f7-114">宣告 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-114">Declaring a cube texture.</span></span> <span data-ttu-id="ea4f7-115">此元素的值為 3 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-115">The value of this element is 3 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="ea4f7-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT \_ 磁片區**</span><span class="sxs-lookup"><span data-stu-id="ea4f7-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="ea4f7-117">宣告磁片區材質。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-117">Declaring a volume texture.</span></span> <span data-ttu-id="ea4f7-118">此元素的值為 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-118">The value of this element is 4 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="ea4f7-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ea4f7-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ea4f7-120">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ea4f7-121">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ea4f7-122">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="ea4f7-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea4f7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea4f7-123">Requirements</span></span>



| <span data-ttu-id="ea4f7-124">需求</span><span class="sxs-lookup"><span data-stu-id="ea4f7-124">Requirement</span></span> | <span data-ttu-id="ea4f7-125">值</span><span class="sxs-lookup"><span data-stu-id="ea4f7-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4f7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ea4f7-126">Header</span></span><br/> | <dl> <span data-ttu-id="ea4f7-127"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea4f7-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4f7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea4f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4f7-129">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="ea4f7-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




