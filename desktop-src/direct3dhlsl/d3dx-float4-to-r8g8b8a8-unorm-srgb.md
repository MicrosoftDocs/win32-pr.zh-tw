---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB 函式
description: 將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB。
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f61e484675b94e1089436ce0b3bd564b3103a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323284"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a><span data-ttu-id="2482f-104">D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM \_ SRGB 函數</span><span class="sxs-lookup"><span data-stu-id="2482f-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="2482f-105">將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB。</span><span class="sxs-lookup"><span data-stu-id="2482f-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="2482f-106">語法</span><span class="sxs-lookup"><span data-stu-id="2482f-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="2482f-107">參數</span><span class="sxs-lookup"><span data-stu-id="2482f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2482f-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="2482f-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="2482f-109">要封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="2482f-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2482f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2482f-110">Return value</span></span>

<span data-ttu-id="2482f-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="2482f-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2482f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2482f-112">Requirements</span></span>



| <span data-ttu-id="2482f-113">需求</span><span class="sxs-lookup"><span data-stu-id="2482f-113">Requirement</span></span> | <span data-ttu-id="2482f-114">值</span><span class="sxs-lookup"><span data-stu-id="2482f-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2482f-115">標頭</span><span class="sxs-lookup"><span data-stu-id="2482f-115">Header</span></span><br/> | <dl> <span data-ttu-id="2482f-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="2482f-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2482f-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="2482f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2482f-118">函式</span><span class="sxs-lookup"><span data-stu-id="2482f-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="2482f-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="2482f-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





