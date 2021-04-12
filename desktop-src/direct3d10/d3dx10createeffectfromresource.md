---
description: 從資源建立效果。
ms.assetid: 239a3b14-9eea-4a0f-96b5-3959b7be3e19
title: D3DX10CreateEffectFromResource 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6c5f7b7805e126f02c2658ddce6ec5029978de53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323016"
---
# <a name="d3dx10createeffectfromresource-function"></a><span data-ttu-id="e4d10-103">D3DX10CreateEffectFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="e4d10-103">D3DX10CreateEffectFromResource function</span></span>

<span data-ttu-id="e4d10-104">從資源建立效果。</span><span class="sxs-lookup"><span data-stu-id="e4d10-104">Create an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d10-105">語法</span><span class="sxs-lookup"><span data-stu-id="e4d10-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="e4d10-106">參數</span><span class="sxs-lookup"><span data-stu-id="e4d10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d10-107">*hModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-108">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4d10-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4d10-109">包含效果的資源模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="e4d10-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="e4d10-110">您可以使用 [GetModuleHandle 函數](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 HMODULE。</span><span class="sxs-lookup"><span data-stu-id="e4d10-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-111">*pResourceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-112">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4d10-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4d10-113">HModule 中資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d10-113">Name of the resource in hModule.</span></span> <span data-ttu-id="e4d10-114">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="e4d10-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e4d10-115">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="e4d10-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-116">*pSrcFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-117">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4d10-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4d10-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e4d10-118">Optional.</span></span> <span data-ttu-id="e4d10-119">效果檔案名，只用于錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e4d10-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="e4d10-120">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e4d10-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-121">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-122">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="e4d10-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="e4d10-123">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="e4d10-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-124">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-125">類型： **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="e4d10-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="e4d10-126">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) 。</span><span class="sxs-lookup"><span data-stu-id="e4d10-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="e4d10-127">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e4d10-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-128">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-129">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4d10-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4d10-130">指定 [著色器設定檔](../direct3dhlsl/dx-graphics-hlsl-models.md)或著色器模型的字串。</span><span class="sxs-lookup"><span data-stu-id="e4d10-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-131">*HLSLFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-132">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4d10-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4d10-133">HLSL 編譯選項 (參閱 [D3D10 \_ 著色器常數](d3d10-shader.md)) 。</span><span class="sxs-lookup"><span data-stu-id="e4d10-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-134">*FXFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-135">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4d10-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4d10-136">效果編譯選項 (查看 [編譯和效果旗標](d3d10-graphics-reference-effect-constants.md)) 。</span><span class="sxs-lookup"><span data-stu-id="e4d10-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-137">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-138">類型： **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="e4d10-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="e4d10-139">裝置的指標 (查看將使用這些資源的 [**ID3D10Device 介面**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="e4d10-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-140">*pEffectPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-140">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-141">類型： **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="e4d10-141">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="e4d10-142">效果集區的指標 (查看 [**ID3D10EffectPool 介面**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) ，以便在效果之間共用變數。</span><span class="sxs-lookup"><span data-stu-id="e4d10-142">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-143">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-144">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4d10-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="e4d10-145">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="e4d10-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="e4d10-146">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="e4d10-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-147">*ppEffect* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-147">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-148">類型： **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="e4d10-148">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="e4d10-149">效果的指標位址 (查看所建立的 [**ID3D10Effect 介面**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) 。</span><span class="sxs-lookup"><span data-stu-id="e4d10-149">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-150">*ppErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-150">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-151">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e4d10-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e4d10-152">記憶體指標的位址 (查看包含效果編譯錯誤（如果有的話）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="e4d10-152">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="e4d10-153">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e4d10-153">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d10-154">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="e4d10-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="e4d10-155">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="e4d10-155">A pointer to the return value.</span></span> <span data-ttu-id="e4d10-156">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e4d10-156">May be **NULL**.</span></span> <span data-ttu-id="e4d10-157">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="e4d10-157">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4d10-158">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4d10-158">Return value</span></span>

<span data-ttu-id="e4d10-159">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4d10-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4d10-160">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e4d10-160">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d10-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4d10-161">Requirements</span></span>



| <span data-ttu-id="e4d10-162">需求</span><span class="sxs-lookup"><span data-stu-id="e4d10-162">Requirement</span></span> | <span data-ttu-id="e4d10-163">值</span><span class="sxs-lookup"><span data-stu-id="e4d10-163">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d10-164">標頭</span><span class="sxs-lookup"><span data-stu-id="e4d10-164">Header</span></span><br/> | <dl> <span data-ttu-id="e4d10-165"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4d10-165"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4d10-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4d10-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d10-167">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="e4d10-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
