---
description: 從記憶體中的效果建立效果集區。
ms.assetid: 634bcb23-a73f-4493-b805-e2aa5420fa2a
title: D3DX10CreateEffectPoolFromMemory 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 7dc93b7e73f336e75432debfe9bde6659ea4707c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981999"
---
# <a name="d3dx10createeffectpoolfrommemory-function"></a><span data-ttu-id="868f6-103">D3DX10CreateEffectPoolFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="868f6-103">D3DX10CreateEffectPoolFromMemory function</span></span>

<span data-ttu-id="868f6-104">從記憶體中的效果建立效果集區。</span><span class="sxs-lookup"><span data-stu-id="868f6-104">Create an effect pool from an effect in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="868f6-105">語法</span><span class="sxs-lookup"><span data-stu-id="868f6-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="868f6-106">參數</span><span class="sxs-lookup"><span data-stu-id="868f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="868f6-107">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="868f6-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="868f6-109">效果的指標。</span><span class="sxs-lookup"><span data-stu-id="868f6-109">A pointer to the effect.</span></span>

</dd> <dt>

<span data-ttu-id="868f6-110">*DataLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-111">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="868f6-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="868f6-112">效果的大小。</span><span class="sxs-lookup"><span data-stu-id="868f6-112">The size of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="868f6-113">*pSrcFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-114">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="868f6-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="868f6-115">效果檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="868f6-115">The name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="868f6-116">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-117">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="868f6-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="868f6-118">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="868f6-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="868f6-119">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-120">類型： **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="868f6-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="868f6-121">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) 。</span><span class="sxs-lookup"><span data-stu-id="868f6-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="868f6-122">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="868f6-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="868f6-123">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-124">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="868f6-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="868f6-125">指定 [著色器設定檔](../direct3dhlsl/dx-graphics-hlsl-models.md)或著色器模型的字串。</span><span class="sxs-lookup"><span data-stu-id="868f6-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="868f6-126">*HLSLFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-127">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="868f6-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="868f6-128">HLSL 編譯選項 (參閱 [D3D10 \_ 著色器常數](d3d10-shader.md)) 。</span><span class="sxs-lookup"><span data-stu-id="868f6-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="868f6-129">*FXFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-130">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="868f6-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="868f6-131">效果編譯選項 (查看 [編譯和效果旗標](d3d10-graphics-reference-effect-constants.md)) 。</span><span class="sxs-lookup"><span data-stu-id="868f6-131">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="868f6-132">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-133">類型： **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="868f6-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="868f6-134">裝置的指標 (查看將使用這些資源的 [**ID3D10Device 介面**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="868f6-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="868f6-135">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="868f6-135">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-136">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="868f6-136">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="868f6-137">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="868f6-137">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="868f6-138">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="868f6-138">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="868f6-139">*ppEffectPool* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="868f6-139">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-140">類型： **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="868f6-140">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="868f6-141">效果集區指標的位址 (查看 [**ID3D10EffectPool 介面**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) 。</span><span class="sxs-lookup"><span data-stu-id="868f6-141">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="868f6-142">*ppErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="868f6-142">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-143">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="868f6-143">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="868f6-144">記憶體指標的位址 (查看包含效果編譯錯誤（如果有的話）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="868f6-144">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="868f6-145">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="868f6-145">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="868f6-146">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="868f6-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="868f6-147">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="868f6-147">A pointer to the return value.</span></span> <span data-ttu-id="868f6-148">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="868f6-148">May be **NULL**.</span></span> <span data-ttu-id="868f6-149">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="868f6-149">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="868f6-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="868f6-150">Return value</span></span>

<span data-ttu-id="868f6-151">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="868f6-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="868f6-152">傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="868f6-152">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="868f6-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="868f6-153">Requirements</span></span>



| <span data-ttu-id="868f6-154">需求</span><span class="sxs-lookup"><span data-stu-id="868f6-154">Requirement</span></span> | <span data-ttu-id="868f6-155">值</span><span class="sxs-lookup"><span data-stu-id="868f6-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="868f6-156">標頭</span><span class="sxs-lookup"><span data-stu-id="868f6-156">Header</span></span><br/> | <dl> <span data-ttu-id="868f6-157"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="868f6-157"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="868f6-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="868f6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868f6-159">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="868f6-159">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
