---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 函式
description: 解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT4。 |D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 函式
ms.assetid: 67ad1768-aeb9-4c01-ae3e-0cd79476a459
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e373ccb8035b19da7c44ee05a07dd0351ca8f48d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974493"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4-function"></a><span data-ttu-id="4691b-105">D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ to \_ FLOAT4 function</span><span class="sxs-lookup"><span data-stu-id="4691b-105">D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4 function</span></span>

<span data-ttu-id="4691b-106">解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT4。</span><span class="sxs-lookup"><span data-stu-id="4691b-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="4691b-107">語法</span><span class="sxs-lookup"><span data-stu-id="4691b-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="4691b-108">參數</span><span class="sxs-lookup"><span data-stu-id="4691b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4691b-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="4691b-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="4691b-110">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="4691b-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4691b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4691b-111">Return value</span></span>

<span data-ttu-id="4691b-112">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="4691b-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4691b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4691b-113">Requirements</span></span>



| <span data-ttu-id="4691b-114">需求</span><span class="sxs-lookup"><span data-stu-id="4691b-114">Requirement</span></span> | <span data-ttu-id="4691b-115">值</span><span class="sxs-lookup"><span data-stu-id="4691b-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4691b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="4691b-116">Header</span></span><br/> | <dl> <span data-ttu-id="4691b-117"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="4691b-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4691b-118">請參閱</span><span class="sxs-lookup"><span data-stu-id="4691b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4691b-119">函式</span><span class="sxs-lookup"><span data-stu-id="4691b-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4691b-120">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="4691b-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





