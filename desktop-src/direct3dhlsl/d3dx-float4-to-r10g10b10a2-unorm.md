---
title: D3DX_FLOAT4_to_R10G10B10A2_UNORM 函式
description: 將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM。
ms.assetid: 20471435-bb1a-4151-a03a-c334b2a7d944
keywords:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c8d80b8822d03a43e813226c28dde8693397a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974436"
---
# <a name="d3dx_float4_to_r10g10b10a2_unorm-function"></a><span data-ttu-id="c22e9-104">D3DX \_ FLOAT4 \_ to \_ R10G10B10A2 \_ UNORM function</span><span class="sxs-lookup"><span data-stu-id="c22e9-104">D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM function</span></span>

<span data-ttu-id="c22e9-105">將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM。</span><span class="sxs-lookup"><span data-stu-id="c22e9-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R10G10B10A2\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="c22e9-106">語法</span><span class="sxs-lookup"><span data-stu-id="c22e9-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="c22e9-107">參數</span><span class="sxs-lookup"><span data-stu-id="c22e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c22e9-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="c22e9-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c22e9-109">要封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="c22e9-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c22e9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c22e9-110">Return value</span></span>

<span data-ttu-id="c22e9-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="c22e9-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c22e9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c22e9-112">Requirements</span></span>



| <span data-ttu-id="c22e9-113">需求</span><span class="sxs-lookup"><span data-stu-id="c22e9-113">Requirement</span></span> | <span data-ttu-id="c22e9-114">值</span><span class="sxs-lookup"><span data-stu-id="c22e9-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c22e9-115">標頭</span><span class="sxs-lookup"><span data-stu-id="c22e9-115">Header</span></span><br/> | <dl> <span data-ttu-id="c22e9-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="c22e9-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c22e9-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="c22e9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c22e9-118">函式</span><span class="sxs-lookup"><span data-stu-id="c22e9-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c22e9-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="c22e9-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





