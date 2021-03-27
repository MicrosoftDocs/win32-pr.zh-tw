---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM 函式
description: 解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM 著色器資料至 XMFLOAT4。 |D3DX_FLOAT4_to_R8G8B8A8_UNORM 函式
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696827"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a><span data-ttu-id="02dfb-105">D3DX \_ FLOAT4 \_ to \_ R8G8B8A8 \_ UNORM function</span><span class="sxs-lookup"><span data-stu-id="02dfb-105">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM function</span></span>

<span data-ttu-id="02dfb-106">解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM 著色器資料至 XMFLOAT4。</span><span class="sxs-lookup"><span data-stu-id="02dfb-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="02dfb-107">語法</span><span class="sxs-lookup"><span data-stu-id="02dfb-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="02dfb-108">參數</span><span class="sxs-lookup"><span data-stu-id="02dfb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02dfb-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="02dfb-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="02dfb-110">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="02dfb-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02dfb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="02dfb-111">Return value</span></span>

<span data-ttu-id="02dfb-112">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="02dfb-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="02dfb-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="02dfb-113">Requirements</span></span>



| <span data-ttu-id="02dfb-114">需求</span><span class="sxs-lookup"><span data-stu-id="02dfb-114">Requirement</span></span> | <span data-ttu-id="02dfb-115">值</span><span class="sxs-lookup"><span data-stu-id="02dfb-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02dfb-116">標頭</span><span class="sxs-lookup"><span data-stu-id="02dfb-116">Header</span></span><br/> | <dl> <span data-ttu-id="02dfb-117"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="02dfb-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02dfb-118">請參閱</span><span class="sxs-lookup"><span data-stu-id="02dfb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02dfb-119">函式</span><span class="sxs-lookup"><span data-stu-id="02dfb-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="02dfb-120">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="02dfb-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





