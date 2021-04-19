---
description: 從包含一或多個函式的效果編譯著色器。
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'ID3DXEffectCompiler：： CompileShader 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 375646202e102623053c179398329ad2286e6c1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986111"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="fc9fb-103">ID3DXEffectCompiler：： CompileShader 方法</span><span class="sxs-lookup"><span data-stu-id="fc9fb-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="fc9fb-104">從包含一或多個函式的效果編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc9fb-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc9fb-105">Syntax</span></span>


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="fc9fb-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc9fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc9fb-107">*hFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc9fb-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc9fb-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fc9fb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fc9fb-109">要編譯之函數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="fc9fb-110">此值不得為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-110">This value must not be **NULL**.</span></span> <span data-ttu-id="fc9fb-111">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc9fb-112">*pTarget* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc9fb-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc9fb-113">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc9fb-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc9fb-114">著色器設定檔的指標，此設定檔可決定著色器指令集。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="fc9fb-115">如需可用的配置檔案清單，請參閱 [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) 或 [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) 。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="fc9fb-116">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="fc9fb-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc9fb-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc9fb-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc9fb-118">不同旗標所識別的編譯選項。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-118">Compile options identified by various flags.</span></span> <span data-ttu-id="fc9fb-119">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="fc9fb-120">如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="fc9fb-121">*ppShader* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="fc9fb-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fc9fb-122">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc9fb-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="fc9fb-123">包含已編譯著色器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="fc9fb-124">編譯器著色器是 Dword 的陣列。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="fc9fb-125">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc9fb-126">*ppErrorMsgs* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="fc9fb-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fc9fb-127">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc9fb-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="fc9fb-128">包含至少發生第一個編譯錯誤訊息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="fc9fb-129">這包括對編譯器錯誤和高階語言編譯錯誤的影響。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="fc9fb-130">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc9fb-131">*ppConstantTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fc9fb-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc9fb-132">類型： **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc9fb-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="fc9fb-133">傳回 [**ID3DXConstantTable**](id3dxconstanttable.md) 介面，這個介面可以用來存取著色器常數。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="fc9fb-134">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-134">This value can be **NULL**.</span></span> <span data-ttu-id="fc9fb-135">如果您將應用程式編譯為大型位址感知 (也就是說，您可以使用/LARGEADDRESSAWARE 連結器選項來處理大於 2 GB 的位址) ，您無法使用此參數，而且必須將它設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="fc9fb-136">相反地，您必須使用 [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) 函式來取出內嵌于著色器中的著色器常數資料表。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="fc9fb-137">在這個 **D3DXGetShaderConstantTableEx** 呼叫中，您必須將 **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** 旗標傳遞給 *Flags* 參數，以指定最多可存取 4 GB 的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc9fb-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc9fb-138">Return value</span></span>

<span data-ttu-id="fc9fb-139">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc9fb-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc9fb-140">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="fc9fb-141">如果引數無效，此方法將會傳回 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="fc9fb-142">如果方法失敗，傳回值將會是 E \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc9fb-143">備註</span><span class="sxs-lookup"><span data-stu-id="fc9fb-143">Remarks</span></span>

<span data-ttu-id="fc9fb-144">您可以針對頂點著色器、圖元著色器和紋理填滿功能指定目標。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



|                       |                                                                       |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="fc9fb-145">頂點著色器目標</span><span class="sxs-lookup"><span data-stu-id="fc9fb-145">Vertex shader targets</span></span> | <span data-ttu-id="fc9fb-146">vs \_ 1 \_ 1、vs \_ 2 \_ 0、vs \_ 2 \_ sw、vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fc9fb-146">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="fc9fb-147">圖元著色器目標</span><span class="sxs-lookup"><span data-stu-id="fc9fb-147">Pixel shader targets</span></span>  | <span data-ttu-id="fc9fb-148">ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4、ps \_ 2 \_ 0、ps \_ 2 \_ sw、ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fc9fb-148">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="fc9fb-149">紋理填滿目標</span><span class="sxs-lookup"><span data-stu-id="fc9fb-149">Texture fill targets</span></span>  | <span data-ttu-id="fc9fb-150">德克薩斯州 \_ 0，德克薩斯州 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fc9fb-150">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="fc9fb-151">這個方法會從以類似 C 的語言撰寫的函式編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-151">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="fc9fb-152">如需詳細資訊，請參閱 [HLSL](../direct3dhlsl/dx-graphics-hlsl.md)。</span><span class="sxs-lookup"><span data-stu-id="fc9fb-152">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc9fb-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc9fb-153">Requirements</span></span>



| <span data-ttu-id="fc9fb-154">需求</span><span class="sxs-lookup"><span data-stu-id="fc9fb-154">Requirement</span></span> | <span data-ttu-id="fc9fb-155">值</span><span class="sxs-lookup"><span data-stu-id="fc9fb-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9fb-156">標頭</span><span class="sxs-lookup"><span data-stu-id="fc9fb-156">Header</span></span><br/>  | <dl> <span data-ttu-id="fc9fb-157"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc9fb-157"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="fc9fb-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc9fb-158">Library</span></span><br/> | <dl> <span data-ttu-id="fc9fb-159"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc9fb-159"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fc9fb-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc9fb-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc9fb-161">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="fc9fb-161">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="fc9fb-162">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="fc9fb-162">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
