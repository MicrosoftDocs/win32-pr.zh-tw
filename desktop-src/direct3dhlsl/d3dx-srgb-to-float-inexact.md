---
title: D3DX_SRGB_to_FLOAT_inexact 函式
description: 將 SRGB 值轉換為 FLOAT。 |D3DX_SRGB_to_FLOAT_inexact 函式
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974516"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a><span data-ttu-id="5e423-105">D3DX \_ SRGB \_ 至 \_ FLOAT 不 \_ 精確函式</span><span class="sxs-lookup"><span data-stu-id="5e423-105">D3DX\_SRGB\_to\_FLOAT\_inexact function</span></span>

<span data-ttu-id="5e423-106">將 SRGB 值轉換為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="5e423-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e423-107">語法</span><span class="sxs-lookup"><span data-stu-id="5e423-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="5e423-108">參數</span><span class="sxs-lookup"><span data-stu-id="5e423-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e423-109">*瓦爾*</span><span class="sxs-lookup"><span data-stu-id="5e423-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="5e423-110">要轉換的 SRGB 值。</span><span class="sxs-lookup"><span data-stu-id="5e423-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e423-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e423-111">Return value</span></span>

<span data-ttu-id="5e423-112">已轉換的 SRGB 值。</span><span class="sxs-lookup"><span data-stu-id="5e423-112">The converted SRGB value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e423-113">備註</span><span class="sxs-lookup"><span data-stu-id="5e423-113">Remarks</span></span>

<span data-ttu-id="5e423-114">這個函式的有效位數沒有足夠的精確度可提供確切的答案。</span><span class="sxs-lookup"><span data-stu-id="5e423-114">This function doesn't have a high enough precision to give the exact answer.</span></span> <span data-ttu-id="5e423-115">替代函式 [**D3DX \_ SRGB \_ 至 \_ float**](d3dx-srgb-to-float.md) 使用查閱資料表來提供精確的 SRGB 至 float 轉換。</span><span class="sxs-lookup"><span data-stu-id="5e423-115">The alternative function [**D3DX\_SRGB\_to\_FLOAT**](d3dx-srgb-to-float.md) uses a lookup table to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e423-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e423-116">Requirements</span></span>



| <span data-ttu-id="5e423-117">需求</span><span class="sxs-lookup"><span data-stu-id="5e423-117">Requirement</span></span> | <span data-ttu-id="5e423-118">值</span><span class="sxs-lookup"><span data-stu-id="5e423-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e423-119">標頭</span><span class="sxs-lookup"><span data-stu-id="5e423-119">Header</span></span><br/> | <dl> <span data-ttu-id="5e423-120"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="5e423-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e423-121">請參閱</span><span class="sxs-lookup"><span data-stu-id="5e423-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e423-122">函式</span><span class="sxs-lookup"><span data-stu-id="5e423-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5e423-123">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="5e423-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





