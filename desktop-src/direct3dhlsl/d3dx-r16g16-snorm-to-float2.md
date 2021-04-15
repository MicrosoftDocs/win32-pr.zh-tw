---
title: D3DX_R16G16_SNORM_to_FLOAT2 函式
description: 解壓縮 DXGI \_ FORMAT \_ R16G16 \_ SNORM 著色器資料至 XMFLOAT2。
ms.assetid: b54df555-b71f-46cd-8be7-34de785d15e2
keywords:
- D3DX_R16G16_SNORM_to_FLOAT2 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3d45f486d2c44e2cbe319e920ab4bdec764fd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992206"
---
# <a name="d3dx_r16g16_snorm_to_float2-function"></a><span data-ttu-id="3c76c-104">D3DX \_ R16G16 \_ SNORM \_ to \_ FLOAT2 function</span><span class="sxs-lookup"><span data-stu-id="3c76c-104">D3DX\_R16G16\_SNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="3c76c-105">解壓縮 DXGI \_ FORMAT \_ R16G16 \_ SNORM 著色器資料至 XMFLOAT2。</span><span class="sxs-lookup"><span data-stu-id="3c76c-105">Unpacks DXGI\_FORMAT\_R16G16\_SNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c76c-106">語法</span><span class="sxs-lookup"><span data-stu-id="3c76c-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="3c76c-107">參數</span><span class="sxs-lookup"><span data-stu-id="3c76c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c76c-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="3c76c-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="3c76c-109">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="3c76c-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c76c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c76c-110">Return value</span></span>

<span data-ttu-id="3c76c-111">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="3c76c-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c76c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c76c-112">Requirements</span></span>



| <span data-ttu-id="3c76c-113">需求</span><span class="sxs-lookup"><span data-stu-id="3c76c-113">Requirement</span></span> | <span data-ttu-id="3c76c-114">值</span><span class="sxs-lookup"><span data-stu-id="3c76c-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c76c-115">標頭</span><span class="sxs-lookup"><span data-stu-id="3c76c-115">Header</span></span><br/> | <dl> <span data-ttu-id="3c76c-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="3c76c-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c76c-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="3c76c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c76c-118">函式</span><span class="sxs-lookup"><span data-stu-id="3c76c-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="3c76c-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="3c76c-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





