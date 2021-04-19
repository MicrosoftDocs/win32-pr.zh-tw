---
description: 以非同步方式建立著色器的資料處理器。
ms.assetid: f5521e55-5f20-422d-979e-98b70efd3b13
title: D3DX10CreateAsyncShaderPreprocessProcessor 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderPreprocessProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 14afdb899d99b7c0278d3042fbc9a108f446c692
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975702"
---
# <a name="d3dx10createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="7face-103">D3DX10CreateAsyncShaderPreprocessProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="7face-103">D3DX10CreateAsyncShaderPreprocessProcessor function</span></span>

<span data-ttu-id="7face-104">以非同步方式建立著色器的資料處理器。</span><span class="sxs-lookup"><span data-stu-id="7face-104">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="7face-105">語法</span><span class="sxs-lookup"><span data-stu-id="7face-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="7face-106">參數</span><span class="sxs-lookup"><span data-stu-id="7face-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7face-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7face-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7face-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7face-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7face-109">包含著色器檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="7face-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="7face-110">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7face-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7face-111">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="7face-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="7face-112">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="7face-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="7face-113">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7face-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7face-114">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="7face-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="7face-115">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) ;將此設為 **Null** ，以指定沒有包含檔。</span><span class="sxs-lookup"><span data-stu-id="7face-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="7face-116">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7face-116">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7face-117">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="7face-117">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="7face-118">緩衝區指標的位址，其中包含著色器的 ASCII 文字 (查看 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="7face-118">Address of a pointer to a buffer that contains the ASCII text of the shader (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="7face-119">*ppErrorBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7face-119">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7face-120">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="7face-120">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="7face-121">包含編譯錯誤之緩衝區的指標位址 (查看 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="7face-121">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="7face-122">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7face-122">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7face-123">類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7face-123">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="7face-124">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7face-124">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7face-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="7face-125">Return value</span></span>

<span data-ttu-id="7face-126">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7face-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7face-127">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7face-127">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7face-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="7face-128">Requirements</span></span>



| <span data-ttu-id="7face-129">需求</span><span class="sxs-lookup"><span data-stu-id="7face-129">Requirement</span></span> | <span data-ttu-id="7face-130">值</span><span class="sxs-lookup"><span data-stu-id="7face-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7face-131">標頭</span><span class="sxs-lookup"><span data-stu-id="7face-131">Header</span></span><br/> | <dl> <span data-ttu-id="7face-132"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="7face-132"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7face-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7face-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7face-134">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="7face-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
