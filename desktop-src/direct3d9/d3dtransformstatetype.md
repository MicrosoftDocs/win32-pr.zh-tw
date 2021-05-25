---
description: 定義描述轉換狀態值的常數。
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: 'D3DTRANSFORMSTATETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 022aa20fab0739b32aa75eb5f4bc575c0a8ad853
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342993"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="0f221-103">D3DTRANSFORMSTATETYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="0f221-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="0f221-104">定義描述轉換狀態值的常數。</span><span class="sxs-lookup"><span data-stu-id="0f221-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f221-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f221-105">Syntax</span></span>


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="0f221-106">常數</span><span class="sxs-lookup"><span data-stu-id="0f221-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0f221-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS \_ 視圖**</span><span class="sxs-lookup"><span data-stu-id="0f221-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-108">識別要設定為視圖轉換矩陣的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="0f221-109">預設值為 **Null** (標識矩陣) 。</span><span class="sxs-lookup"><span data-stu-id="0f221-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="0f221-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS \_ 投射**</span><span class="sxs-lookup"><span data-stu-id="0f221-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-111">識別要設定為投影轉換矩陣的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="0f221-112">預設值為 **Null** (標識矩陣) 。</span><span class="sxs-lookup"><span data-stu-id="0f221-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="0f221-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**</span><span class="sxs-lookup"><span data-stu-id="0f221-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-114">識別要為指定的材質階段設定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0f221-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ >texture1**</span><span class="sxs-lookup"><span data-stu-id="0f221-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-116">識別要為指定的材質階段設定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0f221-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**</span><span class="sxs-lookup"><span data-stu-id="0f221-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-118">識別要為指定的材質階段設定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0f221-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**</span><span class="sxs-lookup"><span data-stu-id="0f221-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-120">識別要為指定的材質階段設定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0f221-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**</span><span class="sxs-lookup"><span data-stu-id="0f221-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-122">識別要為指定的材質階段設定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0f221-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="0f221-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-124">識別要為指定的材質階段設定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0f221-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="0f221-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-126">識別要為指定的材質階段設定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0f221-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="0f221-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-128">識別要為指定的材質階段設定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0f221-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0f221-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0f221-130">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="0f221-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0f221-131">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="0f221-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0f221-132">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="0f221-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f221-133">備註</span><span class="sxs-lookup"><span data-stu-id="0f221-133">Remarks</span></span>

<span data-ttu-id="0f221-134">範圍256到511的轉換狀態是保留來儲存最多256世界矩陣，可使用 D3DTS \_ WORLDMATRIX 和 D3DTS 世界宏來編制索引 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0f221-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="0f221-135">巨集</span><span class="sxs-lookup"><span data-stu-id="0f221-135">Macros</span></span>                                                  | <span data-ttu-id="0f221-136">Description</span><span class="sxs-lookup"><span data-stu-id="0f221-136">Description</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f221-137">**D3DTS \_ 世界**</span><span class="sxs-lookup"><span data-stu-id="0f221-137">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="0f221-138">相當於 D3DTS \_ WORLDMATRIX (0) 。</span><span class="sxs-lookup"><span data-stu-id="0f221-138">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="0f221-139">[**D3DTS \_WORLDMATRIX**](d3dts-worldmatrix.md) (索引) </span><span class="sxs-lookup"><span data-stu-id="0f221-139">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="0f221-140">識別要為位於索引的世界矩陣設定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="0f221-140">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="0f221-141">多個世界矩陣只用于頂點混色。</span><span class="sxs-lookup"><span data-stu-id="0f221-141">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="0f221-142">否則只 \_ 會使用 D3DTS WORLD。</span><span class="sxs-lookup"><span data-stu-id="0f221-142">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0f221-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f221-143">Requirements</span></span>



| <span data-ttu-id="0f221-144">需求</span><span class="sxs-lookup"><span data-stu-id="0f221-144">Requirement</span></span> | <span data-ttu-id="0f221-145">值</span><span class="sxs-lookup"><span data-stu-id="0f221-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f221-146">標頭</span><span class="sxs-lookup"><span data-stu-id="0f221-146">Header</span></span><br/> | <dl> <span data-ttu-id="0f221-147"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f221-147"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f221-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f221-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f221-149">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="0f221-149">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0f221-150">**IDirect3DDevice9::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="0f221-150">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="0f221-151">**IDirect3DDevice9::MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="0f221-151">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="0f221-152">**IDirect3DDevice9::SetTransform**</span><span class="sxs-lookup"><span data-stu-id="0f221-152">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="0f221-153">**D3DTS \_ 世界**</span><span class="sxs-lookup"><span data-stu-id="0f221-153">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="0f221-154">**D3DTS \_ WORLDn**</span><span class="sxs-lookup"><span data-stu-id="0f221-154">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="0f221-155">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="0f221-155">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
