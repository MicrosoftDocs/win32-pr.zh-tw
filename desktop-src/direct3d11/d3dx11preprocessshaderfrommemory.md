---
title: 'D3DX11PreprocessShaderFromMemory 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用 D3DPreprocess API。 在不編譯的情況下，從記憶體建立著色器。
ms.assetid: 3c646914-9334-44fe-a8a0-b84d0dc1a16e
keywords:
- D3DX11PreprocessShaderFromMemory 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a94633270fe0f4e462e60915de862be8693daa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992266"
---
# <a name="d3dx11preprocessshaderfrommemory-function"></a><span data-ttu-id="d399b-106">D3DX11PreprocessShaderFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="d399b-106">D3DX11PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="d399b-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d399b-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="d399b-108">我們建議您不要使用此函式，而是使用 [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API。</span><span class="sxs-lookup"><span data-stu-id="d399b-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="d399b-109">在不編譯的情況下，從記憶體建立著色器。</span><span class="sxs-lookup"><span data-stu-id="d399b-109">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="d399b-110">語法</span><span class="sxs-lookup"><span data-stu-id="d399b-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="d399b-111">參數</span><span class="sxs-lookup"><span data-stu-id="d399b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d399b-112">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d399b-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d399b-113">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d399b-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d399b-114">包含著色器之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="d399b-114">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="d399b-115">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d399b-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d399b-116">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d399b-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d399b-117">著色器的大小。</span><span class="sxs-lookup"><span data-stu-id="d399b-117">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="d399b-118">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d399b-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d399b-119">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d399b-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d399b-120">著色器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d399b-120">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="d399b-121">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d399b-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d399b-122">Type： **CONST D3D11 \_ 著色 \_ 器 \* 宏**</span><span class="sxs-lookup"><span data-stu-id="d399b-122">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="d399b-123">以 Null 結束的著色器宏陣列;將此設為 **Null** ，以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="d399b-123">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="d399b-124">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d399b-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d399b-125">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d399b-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="d399b-126">包含介面的指標;將此設為 **Null** ，以指定沒有包含檔。</span><span class="sxs-lookup"><span data-stu-id="d399b-126">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="d399b-127">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d399b-127">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d399b-128">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="d399b-128">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="d399b-129">執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d399b-129">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="d399b-130">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="d399b-130">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="d399b-131">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d399b-131">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d399b-132">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d399b-132">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d399b-133">記憶體的指標，其中包含未編譯的著色器。</span><span class="sxs-lookup"><span data-stu-id="d399b-133">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="d399b-134">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d399b-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d399b-135">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d399b-135">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d399b-136">記憶體指標的位址，其中包含效果建立錯誤（如果有發生的話）。</span><span class="sxs-lookup"><span data-stu-id="d399b-136">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d399b-137">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d399b-137">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d399b-138">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="d399b-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="d399b-139">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="d399b-139">A pointer to the return value.</span></span> <span data-ttu-id="d399b-140">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d399b-140">May be **NULL**.</span></span> <span data-ttu-id="d399b-141">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="d399b-141">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d399b-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="d399b-142">Return value</span></span>

<span data-ttu-id="d399b-143">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d399b-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d399b-144">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d399b-144">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d399b-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="d399b-145">Requirements</span></span>



| <span data-ttu-id="d399b-146">需求</span><span class="sxs-lookup"><span data-stu-id="d399b-146">Requirement</span></span> | <span data-ttu-id="d399b-147">值</span><span class="sxs-lookup"><span data-stu-id="d399b-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d399b-148">標頭</span><span class="sxs-lookup"><span data-stu-id="d399b-148">Header</span></span><br/>  | <dl> <span data-ttu-id="d399b-149"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="d399b-149"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="d399b-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="d399b-150">Library</span></span><br/> | <dl> <span data-ttu-id="d399b-151"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d399b-151"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d399b-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d399b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d399b-153">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="d399b-153">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

