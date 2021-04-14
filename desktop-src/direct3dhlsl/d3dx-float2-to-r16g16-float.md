---
title: D3DX_FLOAT2_to_R16G16_FLOAT 函式
description: 將指定的 XMFLOAT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ FLOAT。
ms.assetid: 8d03fac3-68f0-4c85-afaa-ff2cb76f1b73
keywords:
- D3DX_FLOAT2_to_R16G16_FLOAT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 849eb4dde5ab11e98675a1581519aabbeeb1e8da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992130"
---
# <a name="d3dx_float2_to_r16g16_float-function"></a><span data-ttu-id="e2447-104">D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ FLOAT 函數</span><span class="sxs-lookup"><span data-stu-id="e2447-104">D3DX\_FLOAT2\_to\_R16G16\_FLOAT function</span></span>

<span data-ttu-id="e2447-105">將指定的 XMFLOAT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="e2447-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2447-106">語法</span><span class="sxs-lookup"><span data-stu-id="e2447-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_FLOAT(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="e2447-107">參數</span><span class="sxs-lookup"><span data-stu-id="e2447-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2447-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="e2447-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="e2447-109">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="e2447-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2447-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2447-110">Return value</span></span>

<span data-ttu-id="e2447-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="e2447-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2447-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2447-112">Requirements</span></span>



| <span data-ttu-id="e2447-113">需求</span><span class="sxs-lookup"><span data-stu-id="e2447-113">Requirement</span></span> | <span data-ttu-id="e2447-114">值</span><span class="sxs-lookup"><span data-stu-id="e2447-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2447-115">標頭</span><span class="sxs-lookup"><span data-stu-id="e2447-115">Header</span></span><br/> | <dl> <span data-ttu-id="e2447-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="e2447-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2447-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="e2447-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2447-118">函式</span><span class="sxs-lookup"><span data-stu-id="e2447-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e2447-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="e2447-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





