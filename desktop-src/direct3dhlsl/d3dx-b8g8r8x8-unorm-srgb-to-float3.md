---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 函式
description: 解壓縮 DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT3。 |D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 函式
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277f10bc574e03a7bd608a333cba65f95a3e0b43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992138"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a><span data-ttu-id="c0f93-105">D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ to \_ FLOAT3 function</span><span class="sxs-lookup"><span data-stu-id="c0f93-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3 function</span></span>

<span data-ttu-id="c0f93-106">解壓縮 DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT3。</span><span class="sxs-lookup"><span data-stu-id="c0f93-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f93-107">語法</span><span class="sxs-lookup"><span data-stu-id="c0f93-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="c0f93-108">參數</span><span class="sxs-lookup"><span data-stu-id="c0f93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f93-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="c0f93-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c0f93-110">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="c0f93-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f93-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0f93-111">Return value</span></span>

<span data-ttu-id="c0f93-112">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="c0f93-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f93-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0f93-113">Requirements</span></span>



| <span data-ttu-id="c0f93-114">需求</span><span class="sxs-lookup"><span data-stu-id="c0f93-114">Requirement</span></span> | <span data-ttu-id="c0f93-115">值</span><span class="sxs-lookup"><span data-stu-id="c0f93-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f93-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c0f93-116">Header</span></span><br/> | <dl> <span data-ttu-id="c0f93-117"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="c0f93-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f93-118">請參閱</span><span class="sxs-lookup"><span data-stu-id="c0f93-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f93-119">函式</span><span class="sxs-lookup"><span data-stu-id="c0f93-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c0f93-120">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="c0f93-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





