---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB 函式
description: 將指定的 XMFLOAT3 重新封裝回 DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB。
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74dd5fbc1329d884968d76039061fceb22aafbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992175"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a><span data-ttu-id="2bdb5-104">D3DX \_ FLOAT3 \_ 到 \_ B8G8R8X8 \_ UNORM \_ SRGB 函數</span><span class="sxs-lookup"><span data-stu-id="2bdb5-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="2bdb5-105">將指定的 XMFLOAT3 重新封裝回 DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB。</span><span class="sxs-lookup"><span data-stu-id="2bdb5-105">Packs the given XMFLOAT3 back into a DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bdb5-106">語法</span><span class="sxs-lookup"><span data-stu-id="2bdb5-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="2bdb5-107">參數</span><span class="sxs-lookup"><span data-stu-id="2bdb5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bdb5-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="2bdb5-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="2bdb5-109">要封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="2bdb5-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bdb5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bdb5-110">Return value</span></span>

<span data-ttu-id="2bdb5-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="2bdb5-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bdb5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bdb5-112">Requirements</span></span>



| <span data-ttu-id="2bdb5-113">需求</span><span class="sxs-lookup"><span data-stu-id="2bdb5-113">Requirement</span></span> | <span data-ttu-id="2bdb5-114">值</span><span class="sxs-lookup"><span data-stu-id="2bdb5-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bdb5-115">標頭</span><span class="sxs-lookup"><span data-stu-id="2bdb5-115">Header</span></span><br/> | <dl> <span data-ttu-id="2bdb5-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="2bdb5-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bdb5-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="2bdb5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bdb5-118">函式</span><span class="sxs-lookup"><span data-stu-id="2bdb5-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="2bdb5-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="2bdb5-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





