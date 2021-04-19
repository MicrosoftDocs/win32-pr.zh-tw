---
description: 從檔案建立效果。
ms.assetid: 1418857e-bda1-4ffb-bbb9-dfa3709313b1
title: D3DX10CreateEffectFromFile 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 60bc52e5b149a2fa69cc4a16f12900b12ab81db8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991487"
---
# <a name="d3dx10createeffectfromfile-function"></a><span data-ttu-id="80306-103">D3DX10CreateEffectFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="80306-103">D3DX10CreateEffectFromFile function</span></span>

<span data-ttu-id="80306-104">從檔案建立效果。</span><span class="sxs-lookup"><span data-stu-id="80306-104">Create an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="80306-105">語法</span><span class="sxs-lookup"><span data-stu-id="80306-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="80306-106">參數</span><span class="sxs-lookup"><span data-stu-id="80306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80306-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80306-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80306-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80306-109">ASCII 效果檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="80306-109">Name of the ASCII effect file.</span></span> <span data-ttu-id="80306-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="80306-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="80306-111">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="80306-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="80306-112">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80306-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-113">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="80306-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="80306-114">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="80306-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="80306-115">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80306-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-116">類型： **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="80306-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="80306-117">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) 。</span><span class="sxs-lookup"><span data-stu-id="80306-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="80306-118">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="80306-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="80306-119">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80306-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-120">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80306-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80306-121">指定 [著色器設定檔](../direct3dhlsl/dx-graphics-hlsl-models.md)或著色器模型的字串。</span><span class="sxs-lookup"><span data-stu-id="80306-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="80306-122">*HLSLFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80306-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80306-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80306-124">HLSL 編譯選項 (參閱 [D3D10 \_ 著色器常數](d3d10-shader.md)) 。</span><span class="sxs-lookup"><span data-stu-id="80306-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="80306-125">*FXFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80306-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80306-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80306-127">效果編譯選項 (查看 [編譯和效果旗標](d3d10-graphics-reference-effect-constants.md)) 。</span><span class="sxs-lookup"><span data-stu-id="80306-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="80306-128">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80306-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-129">類型： **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="80306-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="80306-130">裝置的指標 (查看將使用這些資源的 [**ID3D10Device 介面**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="80306-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="80306-131">*pEffectPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80306-131">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-132">類型： **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="80306-132">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="80306-133">效果集區的指標 (查看 [**ID3D10EffectPool 介面**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) ，以便在效果之間共用變數。</span><span class="sxs-lookup"><span data-stu-id="80306-133">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="80306-134">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80306-134">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-135">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="80306-135">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="80306-136">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="80306-136">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="80306-137">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="80306-137">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="80306-138">*ppEffect* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80306-138">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-139">類型： **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="80306-139">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="80306-140">效果的指標位址 (查看所建立的 [**ID3D10Effect 介面**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) 。</span><span class="sxs-lookup"><span data-stu-id="80306-140">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="80306-141">*ppErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80306-141">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-142">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="80306-142">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="80306-143">記憶體指標的位址 (查看包含效果編譯錯誤（如果有的話）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="80306-143">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="80306-144">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80306-144">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80306-145">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="80306-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="80306-146">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="80306-146">A pointer to the return value.</span></span> <span data-ttu-id="80306-147">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="80306-147">May be **NULL**.</span></span> <span data-ttu-id="80306-148">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="80306-148">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80306-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="80306-149">Return value</span></span>

<span data-ttu-id="80306-150">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80306-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80306-151">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="80306-151">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80306-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="80306-152">Requirements</span></span>



| <span data-ttu-id="80306-153">需求</span><span class="sxs-lookup"><span data-stu-id="80306-153">Requirement</span></span> | <span data-ttu-id="80306-154">值</span><span class="sxs-lookup"><span data-stu-id="80306-154">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80306-155">標頭</span><span class="sxs-lookup"><span data-stu-id="80306-155">Header</span></span><br/> | <dl> <span data-ttu-id="80306-156"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="80306-156"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80306-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80306-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80306-158">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="80306-158">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
