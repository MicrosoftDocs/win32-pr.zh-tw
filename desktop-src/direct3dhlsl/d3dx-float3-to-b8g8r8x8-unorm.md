---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM 函式
description: 將指定的 XMFLOAT3 封裝成 DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM UINT。
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d922264c62526b79aec5d3e36bb477e6a62987
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992207"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a><span data-ttu-id="13a8d-104">D3DX \_ FLOAT3 \_ to \_ B8G8R8X8 \_ UNORM function</span><span class="sxs-lookup"><span data-stu-id="13a8d-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM function</span></span>

<span data-ttu-id="13a8d-105">將指定的 XMFLOAT3 封裝成 DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM UINT。</span><span class="sxs-lookup"><span data-stu-id="13a8d-105">Packs the given XMFLOAT3 into a DXGI\_FORMAT\_B8G8R8X8\_UNORM UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a8d-106">語法</span><span class="sxs-lookup"><span data-stu-id="13a8d-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="13a8d-107">參數</span><span class="sxs-lookup"><span data-stu-id="13a8d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a8d-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="13a8d-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="13a8d-109">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="13a8d-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a8d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="13a8d-110">Return value</span></span>

<span data-ttu-id="13a8d-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="13a8d-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a8d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="13a8d-112">Requirements</span></span>



| <span data-ttu-id="13a8d-113">需求</span><span class="sxs-lookup"><span data-stu-id="13a8d-113">Requirement</span></span> | <span data-ttu-id="13a8d-114">值</span><span class="sxs-lookup"><span data-stu-id="13a8d-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a8d-115">標頭</span><span class="sxs-lookup"><span data-stu-id="13a8d-115">Header</span></span><br/> | <dl> <span data-ttu-id="13a8d-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="13a8d-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a8d-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="13a8d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a8d-118">函式</span><span class="sxs-lookup"><span data-stu-id="13a8d-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="13a8d-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="13a8d-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





