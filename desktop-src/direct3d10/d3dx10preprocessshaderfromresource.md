---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 D3DPreprocess API。 從資源建立著色器，而不進行編譯。
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: D3DX10PreprocessShaderFromResource 函式 (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 81a9f272cb0769d4313a4375f98bdc25b9e403e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386530"
---
# <a name="d3dx10preprocessshaderfromresource-function"></a><span data-ttu-id="44d3d-104">D3DX10PreprocessShaderFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="44d3d-104">D3DX10PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="44d3d-105">我們建議您不要使用此舊版函式，而是使用 [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API。</span><span class="sxs-lookup"><span data-stu-id="44d3d-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="44d3d-106">從資源建立著色器，而不進行編譯。</span><span class="sxs-lookup"><span data-stu-id="44d3d-106">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d3d-107">語法</span><span class="sxs-lookup"><span data-stu-id="44d3d-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="44d3d-108">參數</span><span class="sxs-lookup"><span data-stu-id="44d3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d3d-109">*hModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44d3d-109">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d3d-110">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44d3d-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44d3d-111">包含著色器之資源模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="44d3d-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="44d3d-112">您可以使用 [GetModuleHandle 函數](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 HMODULE。</span><span class="sxs-lookup"><span data-stu-id="44d3d-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="44d3d-113">*pResourceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44d3d-113">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d3d-114">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44d3d-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44d3d-115">包含著色器的端 hModule 資源名稱。</span><span class="sxs-lookup"><span data-stu-id="44d3d-115">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="44d3d-116">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="44d3d-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="44d3d-117">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="44d3d-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="44d3d-118">*pSrcFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44d3d-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d3d-119">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44d3d-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44d3d-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="44d3d-120">Optional.</span></span> <span data-ttu-id="44d3d-121">效果檔案名，只用于錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="44d3d-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="44d3d-122">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="44d3d-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="44d3d-123">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44d3d-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d3d-124">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="44d3d-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="44d3d-125">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="44d3d-125">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="44d3d-126">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44d3d-126">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d3d-127">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="44d3d-127">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="44d3d-128">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) ;將此設為 **Null** ，以指定沒有包含檔。</span><span class="sxs-lookup"><span data-stu-id="44d3d-128">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="44d3d-129">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44d3d-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d3d-130">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="44d3d-130">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="44d3d-131">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="44d3d-131">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="44d3d-132">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="44d3d-132">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="44d3d-133">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="44d3d-133">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44d3d-134">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="44d3d-134">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="44d3d-135">記憶體指標 (查看包含未編譯著色器的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="44d3d-135">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="44d3d-136">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="44d3d-136">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44d3d-137">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="44d3d-137">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="44d3d-138">記憶體指標的位址 (查看包含效果建立錯誤（如果有發生）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="44d3d-138">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d3d-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="44d3d-139">Return value</span></span>

<span data-ttu-id="44d3d-140">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44d3d-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44d3d-141">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="44d3d-141">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44d3d-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="44d3d-142">Requirements</span></span>



| <span data-ttu-id="44d3d-143">需求</span><span class="sxs-lookup"><span data-stu-id="44d3d-143">Requirement</span></span> | <span data-ttu-id="44d3d-144">值</span><span class="sxs-lookup"><span data-stu-id="44d3d-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44d3d-145">標頭</span><span class="sxs-lookup"><span data-stu-id="44d3d-145">Header</span></span><br/>  | <dl> <span data-ttu-id="44d3d-146"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="44d3d-146"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="44d3d-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="44d3d-147">Library</span></span><br/> | <dl> <span data-ttu-id="44d3d-148"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="44d3d-148"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d3d-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44d3d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d3d-150">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="44d3d-150">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
