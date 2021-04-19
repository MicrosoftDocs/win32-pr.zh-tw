---
description: 從效果檔案建立效果集區。
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: D3DX10CreateEffectPoolFromFile 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 418ea287b9bbf2021f3b2e5379b209cf87745a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982000"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a><span data-ttu-id="87ffe-103">D3DX10CreateEffectPoolFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="87ffe-103">D3DX10CreateEffectPoolFromFile function</span></span>

<span data-ttu-id="87ffe-104">從效果檔案建立效果集區。</span><span class="sxs-lookup"><span data-stu-id="87ffe-104">Create an effect pool from an effect file.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ffe-105">語法</span><span class="sxs-lookup"><span data-stu-id="87ffe-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
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



## <a name="parameters"></a><span data-ttu-id="87ffe-106">參數</span><span class="sxs-lookup"><span data-stu-id="87ffe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ffe-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87ffe-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87ffe-109">效果檔案名。</span><span class="sxs-lookup"><span data-stu-id="87ffe-109">The effect filename.</span></span> <span data-ttu-id="87ffe-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="87ffe-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="87ffe-111">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="87ffe-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-112">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-113">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="87ffe-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="87ffe-114">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="87ffe-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-115">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-116">類型： **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="87ffe-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="87ffe-117">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) 。</span><span class="sxs-lookup"><span data-stu-id="87ffe-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="87ffe-118">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="87ffe-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-119">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-120">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87ffe-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87ffe-121">指定 [著色器設定檔](../direct3dhlsl/dx-graphics-hlsl-models.md)或著色器模型的字串。</span><span class="sxs-lookup"><span data-stu-id="87ffe-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-122">*HLSLFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87ffe-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87ffe-124">HLSL 編譯選項 (參閱 [D3D10 \_ 著色器常數](d3d10-shader.md)) 。</span><span class="sxs-lookup"><span data-stu-id="87ffe-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-125">*FXFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87ffe-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87ffe-127">效果編譯選項 (查看 [編譯和效果旗標](d3d10-graphics-reference-effect-constants.md)) 。</span><span class="sxs-lookup"><span data-stu-id="87ffe-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-128">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-129">類型： **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="87ffe-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="87ffe-130">裝置的指標 (查看將使用這些資源的 [**ID3D10Device 介面**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="87ffe-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-131">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-131">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-132">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="87ffe-132">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="87ffe-133">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="87ffe-133">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="87ffe-134">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="87ffe-134">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-135">*ppEffectPool* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-135">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-136">類型： **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="87ffe-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="87ffe-137">效果集區指標的位址 (查看 [**ID3D10EffectPool 介面**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) 。</span><span class="sxs-lookup"><span data-stu-id="87ffe-137">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-138">*ppErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-138">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-139">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="87ffe-139">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="87ffe-140">記憶體指標的位址 (查看包含效果編譯錯誤（如果有的話）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="87ffe-140">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="87ffe-141">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="87ffe-141">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87ffe-142">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="87ffe-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="87ffe-143">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="87ffe-143">A pointer to the return value.</span></span> <span data-ttu-id="87ffe-144">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="87ffe-144">May be **NULL**.</span></span> <span data-ttu-id="87ffe-145">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="87ffe-145">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ffe-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="87ffe-146">Return value</span></span>

<span data-ttu-id="87ffe-147">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87ffe-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87ffe-148">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="87ffe-148">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87ffe-149">備註</span><span class="sxs-lookup"><span data-stu-id="87ffe-149">Remarks</span></span>

<span data-ttu-id="87ffe-150">此範例會從 [BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)中所使用的效果建立效果集區。</span><span class="sxs-lookup"><span data-stu-id="87ffe-150">This example creates an effect pool from the effect used in the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a><span data-ttu-id="87ffe-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="87ffe-151">Requirements</span></span>



| <span data-ttu-id="87ffe-152">需求</span><span class="sxs-lookup"><span data-stu-id="87ffe-152">Requirement</span></span> | <span data-ttu-id="87ffe-153">值</span><span class="sxs-lookup"><span data-stu-id="87ffe-153">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ffe-154">標頭</span><span class="sxs-lookup"><span data-stu-id="87ffe-154">Header</span></span><br/> | <dl> <span data-ttu-id="87ffe-155"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="87ffe-155"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ffe-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87ffe-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ffe-157">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="87ffe-157">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
