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
ms.openlocfilehash: 3e8d1d72fccd5c4ad47d21d05ee46013860a7743
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343623"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="4ca32-103">ID3DXEffectCompiler：： CompileShader 方法</span><span class="sxs-lookup"><span data-stu-id="4ca32-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="4ca32-104">從包含一或多個函式的效果編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="4ca32-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca32-105">語法</span><span class="sxs-lookup"><span data-stu-id="4ca32-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4ca32-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ca32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ca32-107">*hFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ca32-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca32-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4ca32-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4ca32-109">要編譯之函數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ca32-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="4ca32-110">此值不得為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4ca32-110">This value must not be **NULL**.</span></span> <span data-ttu-id="4ca32-111">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="4ca32-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ca32-112">*pTarget* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ca32-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca32-113">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ca32-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ca32-114">著色器設定檔的指標，此設定檔可決定著色器指令集。</span><span class="sxs-lookup"><span data-stu-id="4ca32-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="4ca32-115">如需可用的配置檔案清單，請參閱 [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) 或 [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) 。</span><span class="sxs-lookup"><span data-stu-id="4ca32-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="4ca32-116">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4ca32-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca32-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ca32-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ca32-118">不同旗標所識別的編譯選項。</span><span class="sxs-lookup"><span data-stu-id="4ca32-118">Compile options identified by various flags.</span></span> <span data-ttu-id="4ca32-119">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="4ca32-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="4ca32-120">如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="4ca32-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="4ca32-121">*ppShader* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4ca32-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca32-122">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ca32-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4ca32-123">包含已編譯著色器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4ca32-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="4ca32-124">編譯器著色器是 Dword 的陣列。</span><span class="sxs-lookup"><span data-stu-id="4ca32-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="4ca32-125">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="4ca32-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ca32-126">*ppErrorMsgs* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4ca32-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca32-127">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ca32-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4ca32-128">包含至少發生第一個編譯錯誤訊息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4ca32-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="4ca32-129">這包括對編譯器錯誤和高階語言編譯錯誤的影響。</span><span class="sxs-lookup"><span data-stu-id="4ca32-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="4ca32-130">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="4ca32-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ca32-131">*ppConstantTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4ca32-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca32-132">類型： **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ca32-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="4ca32-133">傳回 [**ID3DXConstantTable**](id3dxconstanttable.md) 介面，這個介面可以用來存取著色器常數。</span><span class="sxs-lookup"><span data-stu-id="4ca32-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="4ca32-134">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4ca32-134">This value can be **NULL**.</span></span> <span data-ttu-id="4ca32-135">如果您將應用程式編譯為大型位址感知 (也就是說，您可以使用/LARGEADDRESSAWARE 連結器選項來處理大於 2 GB 的位址) ，您無法使用此參數，而且必須將它設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4ca32-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="4ca32-136">相反地，您必須使用 [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) 函式來取出內嵌于著色器中的著色器常數資料表。</span><span class="sxs-lookup"><span data-stu-id="4ca32-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="4ca32-137">在這個 **D3DXGetShaderConstantTableEx** 呼叫中，您必須將 **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** 旗標傳遞給 *Flags* 參數，以指定最多可存取 4 GB 的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="4ca32-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ca32-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ca32-138">Return value</span></span>

<span data-ttu-id="4ca32-139">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ca32-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ca32-140">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4ca32-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="4ca32-141">如果引數無效，此方法將會傳回 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="4ca32-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="4ca32-142">如果方法失敗，傳回值將會是 E \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="4ca32-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca32-143">備註</span><span class="sxs-lookup"><span data-stu-id="4ca32-143">Remarks</span></span>

<span data-ttu-id="4ca32-144">您可以針對頂點著色器、圖元著色器和紋理填滿功能指定目標。</span><span class="sxs-lookup"><span data-stu-id="4ca32-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



| <span data-ttu-id="4ca32-145">Targets</span><span class="sxs-lookup"><span data-stu-id="4ca32-145">Targets</span></span>                      | <span data-ttu-id="4ca32-146">函式</span><span class="sxs-lookup"><span data-stu-id="4ca32-146">Functions</span></span>                                                                      |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="4ca32-147">頂點著色器目標</span><span class="sxs-lookup"><span data-stu-id="4ca32-147">Vertex shader targets</span></span> | <span data-ttu-id="4ca32-148">vs \_ 1 \_ 1、vs \_ 2 \_ 0、vs \_ 2 \_ sw、vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4ca32-148">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="4ca32-149">圖元著色器目標</span><span class="sxs-lookup"><span data-stu-id="4ca32-149">Pixel shader targets</span></span>  | <span data-ttu-id="4ca32-150">ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4、ps \_ 2 \_ 0、ps \_ 2 \_ sw、ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4ca32-150">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="4ca32-151">紋理填滿目標</span><span class="sxs-lookup"><span data-stu-id="4ca32-151">Texture fill targets</span></span>  | <span data-ttu-id="4ca32-152">德克薩斯州 \_ 0，德克薩斯州 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4ca32-152">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="4ca32-153">這個方法會從以類似 C 的語言撰寫的函式編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="4ca32-153">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="4ca32-154">如需詳細資訊，請參閱 [HLSL](../direct3dhlsl/dx-graphics-hlsl.md)。</span><span class="sxs-lookup"><span data-stu-id="4ca32-154">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca32-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ca32-155">Requirements</span></span>



| <span data-ttu-id="4ca32-156">需求</span><span class="sxs-lookup"><span data-stu-id="4ca32-156">Requirement</span></span> | <span data-ttu-id="4ca32-157">值</span><span class="sxs-lookup"><span data-stu-id="4ca32-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca32-158">標頭</span><span class="sxs-lookup"><span data-stu-id="4ca32-158">Header</span></span><br/>  | <dl> <span data-ttu-id="4ca32-159"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ca32-159"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4ca32-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ca32-160">Library</span></span><br/> | <dl> <span data-ttu-id="4ca32-161"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ca32-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4ca32-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ca32-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca32-163">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="4ca32-163">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="4ca32-164">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="4ca32-164">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
