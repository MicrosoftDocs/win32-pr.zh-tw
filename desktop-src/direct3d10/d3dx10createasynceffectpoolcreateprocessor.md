---
description: 建立記憶體集區的非同步資料處理器。
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: D3DX10CreateAsyncEffectPoolCreateProcessor 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196316"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a><span data-ttu-id="2f636-103">D3DX10CreateAsyncEffectPoolCreateProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="2f636-103">D3DX10CreateAsyncEffectPoolCreateProcessor function</span></span>

<span data-ttu-id="2f636-104">建立記憶體集區的非同步資料處理器。</span><span class="sxs-lookup"><span data-stu-id="2f636-104">Create an asynchronous-data processor for a memory pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f636-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f636-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="2f636-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f636-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f636-107">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f636-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f636-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f636-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f636-109">包含效果檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="2f636-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="2f636-110">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f636-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f636-111">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="2f636-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="2f636-112">著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="2f636-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="2f636-113">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f636-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f636-114">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="2f636-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="2f636-115">包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) ;將此設為 **Null** ，以指定沒有包含檔。</span><span class="sxs-lookup"><span data-stu-id="2f636-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="2f636-116">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f636-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f636-117">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f636-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f636-118">指定 [著色器設定檔](../direct3dhlsl/dx-graphics-hlsl-models.md) 或著色器模型的字串。</span><span class="sxs-lookup"><span data-stu-id="2f636-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="2f636-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2f636-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f636-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f636-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f636-121">HLSL 編譯選項 (參閱 [著色器旗標](d3d10-graphics-reference-effect-constants.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2f636-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2f636-122">*FXFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f636-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f636-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f636-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f636-124">效果編譯選項 (查看 [編譯和效果旗標](d3d10-graphics-reference-effect-constants.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2f636-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2f636-125">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f636-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f636-126">類型： **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="2f636-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="2f636-127">裝置的指標 (查看將使用這些資源的 [**ID3D10Device 介面**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="2f636-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="2f636-128">*ppErrorBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f636-128">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f636-129">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="2f636-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="2f636-130">記憶體指標的位址 (查看包含效果編譯錯誤（如果有的話）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="2f636-130">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="2f636-131">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f636-131">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f636-132">類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2f636-132">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="2f636-133">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2f636-133">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f636-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f636-134">Return value</span></span>

<span data-ttu-id="2f636-135">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f636-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f636-136">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2f636-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f636-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f636-137">Requirements</span></span>



| <span data-ttu-id="2f636-138">需求</span><span class="sxs-lookup"><span data-stu-id="2f636-138">Requirement</span></span> | <span data-ttu-id="2f636-139">值</span><span class="sxs-lookup"><span data-stu-id="2f636-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f636-140">標頭</span><span class="sxs-lookup"><span data-stu-id="2f636-140">Header</span></span><br/> | <dl> <span data-ttu-id="2f636-141"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f636-141"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f636-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f636-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f636-143">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="2f636-143">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
