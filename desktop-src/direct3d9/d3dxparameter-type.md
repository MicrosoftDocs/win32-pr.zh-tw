---
description: 描述列舉所包含的資料。
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: 'D3DXPARAMETER_TYPE 列舉 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322639"
---
# <a name="d3dxparameter_type-enumeration"></a><span data-ttu-id="2f358-103">D3DXPARAMETER \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="2f358-103">D3DXPARAMETER\_TYPE enumeration</span></span>

<span data-ttu-id="2f358-104">描述列舉所包含的資料。</span><span class="sxs-lookup"><span data-stu-id="2f358-104">Describes the data contained by the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f358-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f358-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="2f358-106">常數</span><span class="sxs-lookup"><span data-stu-id="2f358-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2f358-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ VOID**</span><span class="sxs-lookup"><span data-stu-id="2f358-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT\_VOID**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-108">參數是 void 指標。</span><span class="sxs-lookup"><span data-stu-id="2f358-108">Parameter is a void pointer.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="2f358-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-110">參數是布林值。</span><span class="sxs-lookup"><span data-stu-id="2f358-110">Parameter is a Boolean.</span></span> <span data-ttu-id="2f358-111">任何傳入 [**ID3DXConstantTable：： SetBool**](id3dxconstanttable--setbool.md)、 [**ID3DXConstantTable：： SetBoolArray**](id3dxconstanttable--setboolarray.md)、 [**ID3DXConstantTable：： SetValue**](id3dxconstanttable--setvalue.md)、 [**ID3DXConstantTable：： SetVector**](id3dxconstanttable--setvector.md)或 [**ID3DXConstantTable：： SetVectorArray**](id3dxconstanttable--setvectorarray.md) 的非零值，在寫入常數資料表之前，都會對應到 1 (TRUE) 。否則，常數資料表中的值會設定為0。</span><span class="sxs-lookup"><span data-stu-id="2f358-111">Any non-zero value passed into [**ID3DXConstantTable::SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable::SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be mapped to 1 (TRUE) before being written into the constant table; otherwise, the value will be set to 0 in the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ INT**</span><span class="sxs-lookup"><span data-stu-id="2f358-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT\_INT**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-113">參數是整數。</span><span class="sxs-lookup"><span data-stu-id="2f358-113">Parameter is an integer.</span></span> <span data-ttu-id="2f358-114">傳遞至 [**ID3DXConstantTable：： SetValue**](id3dxconstanttable--setvalue.md)、 [**ID3DXConstantTable：： SetVector**](id3dxconstanttable--setvector.md)或 [**ID3DXConstantTable：： SetVectorArray**](id3dxconstanttable--setvectorarray.md) 的任何浮點值，都會在寫入常數資料表之前，) 四捨五入 (為零個小數位數。</span><span class="sxs-lookup"><span data-stu-id="2f358-114">Any floating-point values passed into [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be rounded off (to zero decimal places) before being written into the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ 浮點數**</span><span class="sxs-lookup"><span data-stu-id="2f358-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT\_FLOAT**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-116">參數是浮點數。</span><span class="sxs-lookup"><span data-stu-id="2f358-116">Parameter is a floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="2f358-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-118">參數是字串。</span><span class="sxs-lookup"><span data-stu-id="2f358-118">Parameter is a string.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT \_ 材質**</span><span class="sxs-lookup"><span data-stu-id="2f358-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-120">參數是紋理。</span><span class="sxs-lookup"><span data-stu-id="2f358-120">Parameter is a texture.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**</span><span class="sxs-lookup"><span data-stu-id="2f358-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT\_TEXTURE1D**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-122">參數是1D 紋理。</span><span class="sxs-lookup"><span data-stu-id="2f358-122">Parameter is a 1D texture.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**</span><span class="sxs-lookup"><span data-stu-id="2f358-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT\_TEXTURE2D**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-124">參數是2D 材質。</span><span class="sxs-lookup"><span data-stu-id="2f358-124">Parameter is a 2D texture.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**</span><span class="sxs-lookup"><span data-stu-id="2f358-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT\_TEXTURE3D**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-126">參數是3D 紋理。</span><span class="sxs-lookup"><span data-stu-id="2f358-126">Parameter is a 3D texture.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**</span><span class="sxs-lookup"><span data-stu-id="2f358-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT\_TEXTURECUBE**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-128">參數是 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="2f358-128">Parameter is a cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT \_ 取樣器**</span><span class="sxs-lookup"><span data-stu-id="2f358-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-130">參數是取樣器。</span><span class="sxs-lookup"><span data-stu-id="2f358-130">Parameter is a sampler.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**</span><span class="sxs-lookup"><span data-stu-id="2f358-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT\_SAMPLER1D**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-132">參數是1D 取樣器。</span><span class="sxs-lookup"><span data-stu-id="2f358-132">Parameter is a 1D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**</span><span class="sxs-lookup"><span data-stu-id="2f358-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT\_SAMPLER2D**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-134">參數是2D 取樣器。</span><span class="sxs-lookup"><span data-stu-id="2f358-134">Parameter is a 2D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**</span><span class="sxs-lookup"><span data-stu-id="2f358-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT\_SAMPLER3D**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-136">參數是3D 取樣器。</span><span class="sxs-lookup"><span data-stu-id="2f358-136">Parameter is a 3D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**</span><span class="sxs-lookup"><span data-stu-id="2f358-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT\_SAMPLERCUBE**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-138">參數是 cube 取樣器。</span><span class="sxs-lookup"><span data-stu-id="2f358-138">Parameter is a cube sampler.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="2f358-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT\_PIXELSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-140">參數是圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="2f358-140">Parameter is a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**</span><span class="sxs-lookup"><span data-stu-id="2f358-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT\_VERTEXSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-142">參數是頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="2f358-142">Parameter is a vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="2f358-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT\_PIXELFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-144">參數是圖元著色器片段。</span><span class="sxs-lookup"><span data-stu-id="2f358-144">Parameter is a pixel shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="2f358-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT\_VERTEXFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-146">參數是頂點著色器片段。</span><span class="sxs-lookup"><span data-stu-id="2f358-146">Parameter is a vertex shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**\_不支援 D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="2f358-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT\_UNSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-148">不支援參數。</span><span class="sxs-lookup"><span data-stu-id="2f358-148">Parameter is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2f358-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2f358-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2f358-150">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="2f358-150">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2f358-151">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="2f358-151">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2f358-152">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="2f358-152">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f358-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f358-153">Requirements</span></span>



| <span data-ttu-id="2f358-154">需求</span><span class="sxs-lookup"><span data-stu-id="2f358-154">Requirement</span></span> | <span data-ttu-id="2f358-155">值</span><span class="sxs-lookup"><span data-stu-id="2f358-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f358-156">標頭</span><span class="sxs-lookup"><span data-stu-id="2f358-156">Header</span></span><br/> | <dl> <span data-ttu-id="2f358-157"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f358-157"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f358-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f358-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f358-159">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="2f358-159">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="2f358-160">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="2f358-160">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2f358-161">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="2f358-161">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




