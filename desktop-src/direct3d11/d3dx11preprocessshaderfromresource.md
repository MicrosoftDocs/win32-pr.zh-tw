---
title: 'D3DX11PreprocessShaderFromResource 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用 D3DPreprocess API。 從資源建立著色器，而不進行編譯。
ms.assetid: 13362ad6-f02e-4899-8962-4f7d4750ff69
keywords:
- D3DX11PreprocessShaderFromResource 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645d872e983cabbcd81aab05a59ee8f1f83cc403
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992263"
---
# <a name="d3dx11preprocessshaderfromresource-function"></a><span data-ttu-id="9a07f-106">D3DX11PreprocessShaderFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="9a07f-106">D3DX11PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="9a07f-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9a07f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="9a07f-108">我們建議您不要使用此函式，而是使用 [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API。</span><span class="sxs-lookup"><span data-stu-id="9a07f-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="9a07f-109">從資源建立著色器，而不進行編譯。</span><span class="sxs-lookup"><span data-stu-id="9a07f-109">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a07f-110">語法</span><span class="sxs-lookup"><span data-stu-id="9a07f-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="9a07f-111">參數</span><span class="sxs-lookup"><span data-stu-id="9a07f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a07f-112">*hModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a07f-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a07f-113">類型： **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a07f-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a07f-114">包含著色器之資源模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9a07f-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="9a07f-115">您可以使用 [GetModuleHandle 函數](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 HMODULE。</span><span class="sxs-lookup"><span data-stu-id="9a07f-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="9a07f-116">*pResourceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a07f-116">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a07f-117">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a07f-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a07f-118">包含著色器的端 hModule 資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9a07f-118">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="9a07f-119">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="9a07f-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="9a07f-120">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="9a07f-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="9a07f-121">*pSrcFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a07f-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a07f-122">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a07f-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a07f-123">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9a07f-123">Optional.</span></span> <span data-ttu-id="9a07f-124">效果檔案名，只用于錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="9a07f-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="9a07f-125">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9a07f-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9a07f-126">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a07f-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a07f-127">Type： **CONST D3D11 \_ 著色 \_ 器 \* 宏**</span><span class="sxs-lookup"><span data-stu-id="9a07f-127">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="9a07f-128">以 Null 結束的著色器宏陣列;將此設為 **Null** ，以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="9a07f-128">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="9a07f-129">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a07f-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a07f-130">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9a07f-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="9a07f-131">包含介面的指標;將此設為 **Null** ，以指定沒有包含檔。</span><span class="sxs-lookup"><span data-stu-id="9a07f-131">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="9a07f-132">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a07f-132">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a07f-133">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a07f-133">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="9a07f-134">執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9a07f-134">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="9a07f-135">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="9a07f-135">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="9a07f-136">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9a07f-136">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a07f-137">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9a07f-137">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9a07f-138">記憶體的指標，其中包含未編譯的著色器。</span><span class="sxs-lookup"><span data-stu-id="9a07f-138">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="9a07f-139">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9a07f-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a07f-140">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9a07f-140">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9a07f-141">記憶體指標的位址，其中包含效果建立錯誤（如果有發生的話）。</span><span class="sxs-lookup"><span data-stu-id="9a07f-141">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9a07f-142">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9a07f-142">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a07f-143">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="9a07f-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="9a07f-144">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="9a07f-144">A pointer to the return value.</span></span> <span data-ttu-id="9a07f-145">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9a07f-145">May be **NULL**.</span></span> <span data-ttu-id="9a07f-146">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="9a07f-146">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a07f-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a07f-147">Return value</span></span>

<span data-ttu-id="9a07f-148">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a07f-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a07f-149">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9a07f-149">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a07f-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a07f-150">Requirements</span></span>



| <span data-ttu-id="9a07f-151">需求</span><span class="sxs-lookup"><span data-stu-id="9a07f-151">Requirement</span></span> | <span data-ttu-id="9a07f-152">值</span><span class="sxs-lookup"><span data-stu-id="9a07f-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a07f-153">標頭</span><span class="sxs-lookup"><span data-stu-id="9a07f-153">Header</span></span><br/>  | <dl> <span data-ttu-id="9a07f-154"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a07f-154"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="9a07f-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a07f-155">Library</span></span><br/> | <dl> <span data-ttu-id="9a07f-156"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a07f-156"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9a07f-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a07f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a07f-158">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="9a07f-158">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

