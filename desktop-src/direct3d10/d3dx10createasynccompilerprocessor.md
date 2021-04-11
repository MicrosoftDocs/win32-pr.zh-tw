---
description: 建立著色器的非同步資料處理器。
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: D3DX10CreateAsyncCompilerProcessor 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fa6a558efd56917832da3280df2aad4ac400def
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196219"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a><span data-ttu-id="940a6-103">D3DX10CreateAsyncCompilerProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="940a6-103">D3DX10CreateAsyncCompilerProcessor function</span></span>

<span data-ttu-id="940a6-104">建立著色器的非同步資料處理器。</span><span class="sxs-lookup"><span data-stu-id="940a6-104">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="940a6-105">語法</span><span class="sxs-lookup"><span data-stu-id="940a6-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="940a6-106">參數</span><span class="sxs-lookup"><span data-stu-id="940a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940a6-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="940a6-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="940a6-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="940a6-109">包含著色器檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="940a6-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="940a6-110">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="940a6-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-111">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="940a6-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="940a6-112">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="940a6-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="940a6-113">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="940a6-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-114">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="940a6-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="940a6-115">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) 。</span><span class="sxs-lookup"><span data-stu-id="940a6-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="940a6-116">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="940a6-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="940a6-117">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="940a6-117">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-118">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="940a6-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="940a6-119">著色器開始執行的著色器輸入點函式名稱。</span><span class="sxs-lookup"><span data-stu-id="940a6-119">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="940a6-120">當您編譯效果時， **D3DX10CreateAsyncCompilerProcessor** 會忽略 *pFunctionName*;建議您將 *pFunctionName* 設定為 **null** ，因為如果所呼叫的函式不會使用它，則將指標參數設定為 **null** ，是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="940a6-120">When you compile an effect, **D3DX10CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="940a6-121">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="940a6-121">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-122">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="940a6-122">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="940a6-123">指定 [著色器設定檔](../direct3dhlsl/dx-graphics-hlsl-models.md) 或著色器模型的字串。</span><span class="sxs-lookup"><span data-stu-id="940a6-123">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="940a6-124">*Flags1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="940a6-124">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-125">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="940a6-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="940a6-126">[著色器編譯旗標](d3d10-shader.md)。</span><span class="sxs-lookup"><span data-stu-id="940a6-126">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="940a6-127">*Flags2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="940a6-127">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-128">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="940a6-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="940a6-129">[效果編譯旗標](d3d10-graphics-reference-effect-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="940a6-129">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="940a6-130">當您編譯著色器而非效果檔案時， **D3DX10CreateAsyncCompilerProcessor** 會忽略 *Flags2*;我們建議您將 *Flags2* 設定為零，因為如果所呼叫的函式不會使用它，則將指標參數設定為 **Null** ，是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="940a6-130">When you compile a shader and not an effect file, **D3DX10CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="940a6-131">*ppCompiledShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="940a6-131">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-132">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="940a6-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="940a6-133">已編譯效果之指標的位址 (參閱 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="940a6-133">Address of a pointer to the compiled effect (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="940a6-134">*ppErrorBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="940a6-134">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-135">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="940a6-135">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="940a6-136">編譯錯誤之指標的位址 (參閱 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="940a6-136">Address of a pointer to compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="940a6-137">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="940a6-137">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="940a6-138">類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="940a6-138">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="940a6-139">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="940a6-139">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940a6-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="940a6-140">Return value</span></span>

<span data-ttu-id="940a6-141">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="940a6-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="940a6-142">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="940a6-142">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="940a6-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="940a6-143">Requirements</span></span>



| <span data-ttu-id="940a6-144">需求</span><span class="sxs-lookup"><span data-stu-id="940a6-144">Requirement</span></span> | <span data-ttu-id="940a6-145">值</span><span class="sxs-lookup"><span data-stu-id="940a6-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="940a6-146">標頭</span><span class="sxs-lookup"><span data-stu-id="940a6-146">Header</span></span><br/> | <dl> <span data-ttu-id="940a6-147"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="940a6-147"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="940a6-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="940a6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940a6-149">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="940a6-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
