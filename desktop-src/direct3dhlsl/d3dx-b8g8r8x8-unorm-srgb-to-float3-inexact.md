---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact 函式
description: 解壓縮 DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT3。 |D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact 函式
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974452"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a><span data-ttu-id="56563-105">D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ to \_ FLOAT3 不 \_ 精確的函式</span><span class="sxs-lookup"><span data-stu-id="56563-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact function</span></span>

<span data-ttu-id="56563-106">解壓縮 DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT3。</span><span class="sxs-lookup"><span data-stu-id="56563-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="56563-107">語法</span><span class="sxs-lookup"><span data-stu-id="56563-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="56563-108">參數</span><span class="sxs-lookup"><span data-stu-id="56563-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56563-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="56563-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="56563-110">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="56563-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56563-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="56563-111">Return value</span></span>

<span data-ttu-id="56563-112">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="56563-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="56563-113">備註</span><span class="sxs-lookup"><span data-stu-id="56563-113">Remarks</span></span>

<span data-ttu-id="56563-114">此函式會使用沒有足夠精確度的著色器指令來提供確切的答案。</span><span class="sxs-lookup"><span data-stu-id="56563-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="56563-115">替代函式 [**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ to \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) 會使用儲存在著色器中的查閱資料表，提供確切的 SRGB 給 float 轉換。</span><span class="sxs-lookup"><span data-stu-id="56563-115">The alternative function [**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="56563-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="56563-116">Requirements</span></span>



| <span data-ttu-id="56563-117">需求</span><span class="sxs-lookup"><span data-stu-id="56563-117">Requirement</span></span> | <span data-ttu-id="56563-118">值</span><span class="sxs-lookup"><span data-stu-id="56563-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56563-119">標頭</span><span class="sxs-lookup"><span data-stu-id="56563-119">Header</span></span><br/> | <dl> <span data-ttu-id="56563-120"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="56563-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56563-121">請參閱</span><span class="sxs-lookup"><span data-stu-id="56563-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56563-122">函式</span><span class="sxs-lookup"><span data-stu-id="56563-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="56563-123">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="56563-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





