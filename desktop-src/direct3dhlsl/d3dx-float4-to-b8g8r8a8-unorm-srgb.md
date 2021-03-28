---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB 函式
description: 將指定的 XMFLOAT4 封裝成 DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB UINT。
ms.assetid: 2fc36f19-44ce-43ba-9d9f-e8061f94a207
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c20292e1038d31c6d853eb8ae62f7e764e722a6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196384"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a><span data-ttu-id="7af4e-104">D3DX \_ FLOAT4 \_ 到 \_ B8G8R8A8 \_ UNORM \_ SRGB 函數</span><span class="sxs-lookup"><span data-stu-id="7af4e-104">D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="7af4e-105">將指定的 XMFLOAT4 封裝成 DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB UINT。</span><span class="sxs-lookup"><span data-stu-id="7af4e-105">Packs the given XMFLOAT4 into a DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af4e-106">語法</span><span class="sxs-lookup"><span data-stu-id="7af4e-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="7af4e-107">參數</span><span class="sxs-lookup"><span data-stu-id="7af4e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af4e-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="7af4e-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="7af4e-109">解壓縮的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="7af4e-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af4e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7af4e-110">Return value</span></span>

<span data-ttu-id="7af4e-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="7af4e-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af4e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7af4e-112">Requirements</span></span>



| <span data-ttu-id="7af4e-113">需求</span><span class="sxs-lookup"><span data-stu-id="7af4e-113">Requirement</span></span> | <span data-ttu-id="7af4e-114">值</span><span class="sxs-lookup"><span data-stu-id="7af4e-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af4e-115">標頭</span><span class="sxs-lookup"><span data-stu-id="7af4e-115">Header</span></span><br/> | <dl> <span data-ttu-id="7af4e-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="7af4e-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7af4e-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="7af4e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af4e-118">函式</span><span class="sxs-lookup"><span data-stu-id="7af4e-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="7af4e-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="7af4e-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





