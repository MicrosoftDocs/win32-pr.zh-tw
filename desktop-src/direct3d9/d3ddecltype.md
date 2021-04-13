---
description: 定義頂點宣告資料類型。
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: 'D3DDECLTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322728"
---
# <a name="d3ddecltype-enumeration"></a><span data-ttu-id="d7c72-103">D3DDECLTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="d7c72-103">D3DDECLTYPE enumeration</span></span>

<span data-ttu-id="d7c72-104">定義頂點宣告資料類型。</span><span class="sxs-lookup"><span data-stu-id="d7c72-104">Defines a vertex declaration data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7c72-105">Syntax</span></span>


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a><span data-ttu-id="d7c72-106">常數</span><span class="sxs-lookup"><span data-stu-id="d7c72-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d7c72-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**</span><span class="sxs-lookup"><span data-stu-id="d7c72-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE\_FLOAT1**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-108">一個元件 float 展開至 (浮點數、0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-108">One-component float expanded to (float, 0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="d7c72-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE\_FLOAT2**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-110">雙元件 float 展開至 (浮點數、浮點數、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-110">Two-component float expanded to (float, float, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="d7c72-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE\_FLOAT3**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-112">將三個元件 float 展開至 (float、float、float、1) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-112">Three-component float expanded to (float, float, float, 1).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="d7c72-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-114">四個元件 float 展開至 (浮點數、浮點數、浮點數) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-114">Four-component float expanded to (float, float, float, float).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="d7c72-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE\_D3DCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-116">四個元件、已封裝、不帶正負號的位元組對應至0到1個範圍。</span><span class="sxs-lookup"><span data-stu-id="d7c72-116">Four-component, packed, unsigned bytes mapped to 0 to 1 range.</span></span> <span data-ttu-id="d7c72-117">輸入是 [**D3DCOLOR**](d3dcolor.md) ，並已展開為 RGBA 順序。</span><span class="sxs-lookup"><span data-stu-id="d7c72-117">Input is a [**D3DCOLOR**](d3dcolor.md) and is expanded to RGBA order.</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**</span><span class="sxs-lookup"><span data-stu-id="d7c72-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE\_UBYTE4**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-119">四個元件、不帶正負號的位元組。</span><span class="sxs-lookup"><span data-stu-id="d7c72-119">Four-component, unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**</span><span class="sxs-lookup"><span data-stu-id="d7c72-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE\_SHORT2**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-121">雙元件的帶正負號的簡短擴充至 (值、值、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-121">Two-component, signed short expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**</span><span class="sxs-lookup"><span data-stu-id="d7c72-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE\_SHORT4**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-123">四個元件的帶正負號的簡短擴充至 (值、值、值、值) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-123">Four-component, signed short expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**</span><span class="sxs-lookup"><span data-stu-id="d7c72-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE\_UBYTE4N**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-125">四個元件的位元組，其中每個位元組都以正規化方式除以 255.0 f。</span><span class="sxs-lookup"><span data-stu-id="d7c72-125">Four-component byte with each byte normalized by dividing with 255.0f.</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**</span><span class="sxs-lookup"><span data-stu-id="d7c72-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE\_SHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-127">正規化的兩個元件（帶正負號）會展開為 (第一個簡短/32767.0、第二個簡短/32767.0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-127">Normalized, two-component, signed short, expanded to (first short/32767.0, second short/32767.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**</span><span class="sxs-lookup"><span data-stu-id="d7c72-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE\_SHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-129">正規化，四個元件的帶正負號的簡短，展開為 (first short/32767.0，第二個 short/32767.0，第三個簡短/32767.0，第四個 short/32767.0) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-129">Normalized, four-component, signed short, expanded to (first short/32767.0, second short/32767.0, third short/32767.0, fourth short/32767.0).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**</span><span class="sxs-lookup"><span data-stu-id="d7c72-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE\_USHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-131">正規化、雙元件、不帶正負號的簡短、展開為 (first short/65535.0、short short/65535.0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-131">Normalized, two-component, unsigned short, expanded to (first short/65535.0, short short/65535.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**</span><span class="sxs-lookup"><span data-stu-id="d7c72-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE\_USHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-133">正規化、四個元件、不帶正負號的簡短、展開為 (first short/65535.0、second short/65535.0、第三個簡短/65535.0、第四個 short/65535.0) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-133">Normalized, four-component, unsigned short, expanded to (first short/65535.0, second short/65535.0, third short/65535.0, fourth short/65535.0).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**</span><span class="sxs-lookup"><span data-stu-id="d7c72-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE\_UDEC3**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-135">將三個元件、不帶正負號的 10 10 10 格式擴充為 (值、值、值、1) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-135">Three-component, unsigned, 10 10 10 format expanded to (value, value, value, 1).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**</span><span class="sxs-lookup"><span data-stu-id="d7c72-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE\_DEC3N**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-137">三個元件、帶正負號的 10 10 10 格式正規化和展開為 (v \[ 0 \] /511.0、v \[ 1 \] /511.0、v \[ 2 \] /511.0、1) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-137">Three-component, signed, 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d7c72-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE\_FLOAT16\_2**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-139">雙元件、16位、浮點數展開至 (值、值、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-139">Two-component, 16-bit, floating point expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="d7c72-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE\_FLOAT16\_4**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-141">四個元件、16位、浮點數展開至 (值、值、值、值) 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-141">Four-component, 16-bit, floating point expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="d7c72-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**\_未使用 D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="d7c72-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="d7c72-143">宣告中的類型欄位未使用。</span><span class="sxs-lookup"><span data-stu-id="d7c72-143">Type field in the declaration is unused.</span></span> <span data-ttu-id="d7c72-144">這是設計來與 D3DDECLMETHOD \_ UV 和 D3DDECLMETHOD LOOKUPPRESAMPLED 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d7c72-144">This is designed for use with D3DDECLMETHOD\_UV and D3DDECLMETHOD\_LOOKUPPRESAMPLED.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7c72-145">備註</span><span class="sxs-lookup"><span data-stu-id="d7c72-145">Remarks</span></span>

<span data-ttu-id="d7c72-146">頂點資料是使用 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 結構的陣列來宣告。</span><span class="sxs-lookup"><span data-stu-id="d7c72-146">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="d7c72-147">陣列中的每個元素都包含一個頂點宣告資料類型。</span><span class="sxs-lookup"><span data-stu-id="d7c72-147">Each element in the array contains a vertex declaration data type.</span></span>

<span data-ttu-id="d7c72-148">使用 DirectX Cap 檢視器工具 (DXCapsViewer.exe) 來查看裝置支援的類型。</span><span class="sxs-lookup"><span data-stu-id="d7c72-148">Use the DirectX Caps Viewer Tool (DXCapsViewer.exe) to see which types are supported on your device.</span></span> <span data-ttu-id="d7c72-149">您可以從 DirectX SDK 取得此工具，並瞭解其相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d7c72-149">You can get this tool and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="d7c72-150">如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="d7c72-150">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c72-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7c72-151">Requirements</span></span>



| <span data-ttu-id="d7c72-152">需求</span><span class="sxs-lookup"><span data-stu-id="d7c72-152">Requirement</span></span> | <span data-ttu-id="d7c72-153">值</span><span class="sxs-lookup"><span data-stu-id="d7c72-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c72-154">標頭</span><span class="sxs-lookup"><span data-stu-id="d7c72-154">Header</span></span><br/> | <dl> <span data-ttu-id="d7c72-155"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7c72-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c72-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7c72-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c72-157">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="d7c72-157">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d7c72-158">**D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="d7c72-158">**D3DDECLMETHOD**</span></span>](./d3ddeclmethod.md)
</dt> </dl>

 

 
