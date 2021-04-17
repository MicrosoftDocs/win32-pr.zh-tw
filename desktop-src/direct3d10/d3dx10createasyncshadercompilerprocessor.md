---
description: 編譯著色器，並以非同步方式建立資料處理器。
ms.assetid: 842db48b-51a7-4f32-8ea6-44247f2619b0
title: D3DX10CreateAsyncShaderCompilerProcessor 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 2a1cd663827cc32b868c9c6c9b74fbc3c21b8ee6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386442"
---
# <a name="d3dx10createasyncshadercompilerprocessor-function"></a><span data-ttu-id="9bf11-103">D3DX10CreateAsyncShaderCompilerProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="9bf11-103">D3DX10CreateAsyncShaderCompilerProcessor function</span></span>

<span data-ttu-id="9bf11-104">編譯著色器，並以非同步方式建立資料處理器。</span><span class="sxs-lookup"><span data-stu-id="9bf11-104">Compile a shader and create a data processor asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf11-105">語法</span><span class="sxs-lookup"><span data-stu-id="9bf11-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="9bf11-106">參數</span><span class="sxs-lookup"><span data-stu-id="9bf11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bf11-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9bf11-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf11-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bf11-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bf11-109">包含著色器檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="9bf11-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="9bf11-110">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9bf11-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf11-111">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="9bf11-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="9bf11-112">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="9bf11-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="9bf11-113">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9bf11-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf11-114">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9bf11-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="9bf11-115">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) ;將此設為 **Null** ，以指定沒有包含檔。</span><span class="sxs-lookup"><span data-stu-id="9bf11-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="9bf11-116">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9bf11-116">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf11-117">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bf11-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bf11-118">著色器的進入點函數名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf11-118">Name of the entry point function for the shader.</span></span>

</dd> <dt>

<span data-ttu-id="9bf11-119">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9bf11-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf11-120">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bf11-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bf11-121">指定 [著色器設定檔](../direct3dhlsl/dx-graphics-hlsl-models.md) 或著色器模型的字串。</span><span class="sxs-lookup"><span data-stu-id="9bf11-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="9bf11-122">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9bf11-122">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf11-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bf11-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bf11-124">HLSL 編譯選項 (參閱 [著色器旗標](d3d10-graphics-reference-effect-constants.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9bf11-124">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9bf11-125">*ppCompiledShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9bf11-125">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf11-126">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9bf11-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9bf11-127">已編譯著色器之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="9bf11-127">Address of a pointer to the compiled shader.</span></span> <span data-ttu-id="9bf11-128">請參閱 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)。</span><span class="sxs-lookup"><span data-stu-id="9bf11-128">See [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="9bf11-129">*ppErrorBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9bf11-129">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf11-130">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9bf11-130">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9bf11-131">包含編譯錯誤之緩衝區的指標位址 (查看 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="9bf11-131">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="9bf11-132">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9bf11-132">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf11-133">類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9bf11-133">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="9bf11-134">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9bf11-134">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bf11-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="9bf11-135">Return value</span></span>

<span data-ttu-id="9bf11-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9bf11-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9bf11-137">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9bf11-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf11-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bf11-138">Requirements</span></span>



| <span data-ttu-id="9bf11-139">需求</span><span class="sxs-lookup"><span data-stu-id="9bf11-139">Requirement</span></span> | <span data-ttu-id="9bf11-140">值</span><span class="sxs-lookup"><span data-stu-id="9bf11-140">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf11-141">標頭</span><span class="sxs-lookup"><span data-stu-id="9bf11-141">Header</span></span><br/> | <dl> <span data-ttu-id="9bf11-142"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="9bf11-142"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bf11-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bf11-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf11-144">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="9bf11-144">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
