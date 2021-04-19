---
description: 建立適用于效果的非同步資料處理器。
ms.assetid: 90a0dcd1-e495-4068-9f28-e2645370b984
title: D3DX10CreateAsyncEffectCompilerProcessor 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 9e1e5716228537d505adc4f48179ec7027b57198
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993891"
---
# <a name="d3dx10createasynceffectcompilerprocessor-function"></a><span data-ttu-id="9974d-103">D3DX10CreateAsyncEffectCompilerProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="9974d-103">D3DX10CreateAsyncEffectCompilerProcessor function</span></span>

<span data-ttu-id="9974d-104">建立適用于效果的非同步資料處理器。</span><span class="sxs-lookup"><span data-stu-id="9974d-104">Create an asynchronous-data processor for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="9974d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9974d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="9974d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9974d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9974d-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9974d-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9974d-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9974d-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9974d-109">包含效果檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="9974d-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="9974d-110">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9974d-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9974d-111">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="9974d-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="9974d-112">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="9974d-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="9974d-113">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9974d-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9974d-114">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9974d-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="9974d-115">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) 。</span><span class="sxs-lookup"><span data-stu-id="9974d-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="9974d-116">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9974d-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9974d-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9974d-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9974d-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9974d-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9974d-119">[HLSL 編譯選項](d3d10-graphics-reference-effect-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9974d-119">[HLSL compile options](d3d10-graphics-reference-effect-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="9974d-120">*FXFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9974d-120">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9974d-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9974d-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9974d-122">) 的[效果編譯選項](d3d10-graphics-reference-effect-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9974d-122">[Effect compile options](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9974d-123">*ppCompiledShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9974d-123">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9974d-124">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9974d-124">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9974d-125">緩衝區指標的位址 (請參閱包含已編譯效果的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="9974d-125">Address of a pointer to buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="9974d-126">*ppErrorBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9974d-126">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9974d-127">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9974d-127">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9974d-128">緩衝區指標的位址 (查看包含編譯錯誤的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="9974d-128">Address of a pointer to a buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="9974d-129">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9974d-129">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9974d-130">類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9974d-130">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="9974d-131">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9974d-131">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9974d-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="9974d-132">Return value</span></span>

<span data-ttu-id="9974d-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9974d-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9974d-134">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9974d-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9974d-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="9974d-135">Requirements</span></span>



| <span data-ttu-id="9974d-136">需求</span><span class="sxs-lookup"><span data-stu-id="9974d-136">Requirement</span></span> | <span data-ttu-id="9974d-137">值</span><span class="sxs-lookup"><span data-stu-id="9974d-137">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9974d-138">標頭</span><span class="sxs-lookup"><span data-stu-id="9974d-138">Header</span></span><br/> | <dl> <span data-ttu-id="9974d-139"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="9974d-139"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9974d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9974d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9974d-141">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="9974d-141">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
