---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 D3DPreprocess API。 在不編譯的情況下，從記憶體建立著色器。
ms.assetid: 099bc010-1269-4833-8a96-a7c78ed48206
title: D3DX10PreprocessShaderFromMemory 函式 (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d06e46a5cd6b86420543b380f74273be032c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696759"
---
# <a name="d3dx10preprocessshaderfrommemory-function"></a><span data-ttu-id="3cda0-104">D3DX10PreprocessShaderFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="3cda0-104">D3DX10PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="3cda0-105">我們建議您不要使用此舊版函式，而是使用 [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API。</span><span class="sxs-lookup"><span data-stu-id="3cda0-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="3cda0-106">在不編譯的情況下，從記憶體建立著色器。</span><span class="sxs-lookup"><span data-stu-id="3cda0-106">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cda0-107">語法</span><span class="sxs-lookup"><span data-stu-id="3cda0-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="3cda0-108">參數</span><span class="sxs-lookup"><span data-stu-id="3cda0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cda0-109">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cda0-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cda0-110">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3cda0-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3cda0-111">包含著色器之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="3cda0-111">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="3cda0-112">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cda0-112">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cda0-113">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3cda0-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3cda0-114">著色器的大小。</span><span class="sxs-lookup"><span data-stu-id="3cda0-114">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="3cda0-115">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cda0-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cda0-116">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3cda0-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3cda0-117">著色器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cda0-117">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="3cda0-118">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cda0-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cda0-119">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="3cda0-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="3cda0-120">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="3cda0-120">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="3cda0-121">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cda0-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cda0-122">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3cda0-122">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="3cda0-123">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) ;將此設為 **Null** ，以指定沒有包含檔。</span><span class="sxs-lookup"><span data-stu-id="3cda0-123">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="3cda0-124">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cda0-124">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cda0-125">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="3cda0-125">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="3cda0-126">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="3cda0-126">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="3cda0-127">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="3cda0-127">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="3cda0-128">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3cda0-128">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cda0-129">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3cda0-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3cda0-130">記憶體指標 (查看包含未編譯著色器的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="3cda0-130">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="3cda0-131">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3cda0-131">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cda0-132">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3cda0-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3cda0-133">記憶體指標的位址 (查看包含效果建立錯誤（如果有發生）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="3cda0-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cda0-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cda0-134">Return value</span></span>

<span data-ttu-id="3cda0-135">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3cda0-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3cda0-136">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3cda0-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cda0-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cda0-137">Requirements</span></span>



| <span data-ttu-id="3cda0-138">需求</span><span class="sxs-lookup"><span data-stu-id="3cda0-138">Requirement</span></span> | <span data-ttu-id="3cda0-139">值</span><span class="sxs-lookup"><span data-stu-id="3cda0-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cda0-140">標頭</span><span class="sxs-lookup"><span data-stu-id="3cda0-140">Header</span></span><br/>  | <dl> <span data-ttu-id="3cda0-141"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cda0-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3cda0-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="3cda0-142">Library</span></span><br/> | <dl> <span data-ttu-id="3cda0-143"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cda0-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cda0-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cda0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cda0-145">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="3cda0-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
