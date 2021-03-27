---
title: D3DX_FLOAT2_to_R16G16_SNORM 函式
description: 將指定的 XMFLOAT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ SNORM。
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- D3DX_FLOAT2_to_R16G16_SNORM 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946132"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a><span data-ttu-id="f9801-104">D3DX \_ FLOAT2 \_ to \_ R16G16 \_ SNORM function</span><span class="sxs-lookup"><span data-stu-id="f9801-104">D3DX\_FLOAT2\_to\_R16G16\_SNORM function</span></span>

<span data-ttu-id="f9801-105">將指定的 XMFLOAT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ SNORM。</span><span class="sxs-lookup"><span data-stu-id="f9801-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9801-106">語法</span><span class="sxs-lookup"><span data-stu-id="f9801-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="f9801-107">參數</span><span class="sxs-lookup"><span data-stu-id="f9801-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9801-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="f9801-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="f9801-109">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="f9801-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9801-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9801-110">Return value</span></span>

<span data-ttu-id="f9801-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="f9801-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9801-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9801-112">Requirements</span></span>



| <span data-ttu-id="f9801-113">需求</span><span class="sxs-lookup"><span data-stu-id="f9801-113">Requirement</span></span> | <span data-ttu-id="f9801-114">值</span><span class="sxs-lookup"><span data-stu-id="f9801-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9801-115">標頭</span><span class="sxs-lookup"><span data-stu-id="f9801-115">Header</span></span><br/> | <dl> <span data-ttu-id="f9801-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="f9801-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9801-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="f9801-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9801-118">函式</span><span class="sxs-lookup"><span data-stu-id="f9801-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="f9801-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="f9801-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





