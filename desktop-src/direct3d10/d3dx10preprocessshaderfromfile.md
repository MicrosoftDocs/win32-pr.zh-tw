---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 D3DPreprocess API。 在不編譯的情況下，從檔案建立著色器。
ms.assetid: 9f609aa5-5ee7-45fb-9693-69de130b6cc0
title: D3DX10PreprocessShaderFromFile 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e6222febd378b262d9fb9e87a6224968c2d04038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974875"
---
# <a name="d3dx10preprocessshaderfromfile-function"></a><span data-ttu-id="609c4-104">D3DX10PreprocessShaderFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="609c4-104">D3DX10PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="609c4-105">我們建議您不要使用此舊版函式，而是使用 [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API。</span><span class="sxs-lookup"><span data-stu-id="609c4-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="609c4-106">在不編譯的情況下，從檔案建立著色器。</span><span class="sxs-lookup"><span data-stu-id="609c4-106">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="609c4-107">語法</span><span class="sxs-lookup"><span data-stu-id="609c4-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="609c4-108">參數</span><span class="sxs-lookup"><span data-stu-id="609c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="609c4-109">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="609c4-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="609c4-110">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="609c4-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="609c4-111">著色器檔案名。</span><span class="sxs-lookup"><span data-stu-id="609c4-111">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="609c4-112">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="609c4-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="609c4-113">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="609c4-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="609c4-114">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="609c4-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="609c4-115">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="609c4-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="609c4-116">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="609c4-116">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="609c4-117">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) ;將此設為 **Null** ，以指定沒有包含檔。</span><span class="sxs-lookup"><span data-stu-id="609c4-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="609c4-118">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="609c4-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="609c4-119">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="609c4-119">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="609c4-120">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="609c4-120">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="609c4-121">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="609c4-121">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="609c4-122">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="609c4-122">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="609c4-123">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="609c4-123">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="609c4-124">記憶體指標 (查看包含未編譯著色器的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="609c4-124">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="609c4-125">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="609c4-125">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="609c4-126">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="609c4-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="609c4-127">記憶體指標的位址 (查看包含效果建立錯誤（如果有發生）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="609c4-127">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="609c4-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="609c4-128">Return value</span></span>

<span data-ttu-id="609c4-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="609c4-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="609c4-130">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="609c4-130">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="609c4-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="609c4-131">Requirements</span></span>



| <span data-ttu-id="609c4-132">需求</span><span class="sxs-lookup"><span data-stu-id="609c4-132">Requirement</span></span> | <span data-ttu-id="609c4-133">值</span><span class="sxs-lookup"><span data-stu-id="609c4-133">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="609c4-134">標頭</span><span class="sxs-lookup"><span data-stu-id="609c4-134">Header</span></span><br/> | <dl> <span data-ttu-id="609c4-135"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="609c4-135"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="609c4-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="609c4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="609c4-137">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="609c4-137">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
