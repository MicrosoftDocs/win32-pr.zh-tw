---
title: D3DX_FLOAT4_to_R8G8B8A8_SNORM 函式
description: 將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM。
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194835ef126a3441dc2b842784dfa841ae1d7d6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323288"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a><span data-ttu-id="733a8-104">D3DX \_ FLOAT4 \_ to \_ R8G8B8A8 \_ SNORM function</span><span class="sxs-lookup"><span data-stu-id="733a8-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM function</span></span>

<span data-ttu-id="733a8-105">將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM。</span><span class="sxs-lookup"><span data-stu-id="733a8-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="733a8-106">語法</span><span class="sxs-lookup"><span data-stu-id="733a8-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="733a8-107">參數</span><span class="sxs-lookup"><span data-stu-id="733a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733a8-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="733a8-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="733a8-109">要封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="733a8-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733a8-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="733a8-110">Return value</span></span>

<span data-ttu-id="733a8-111">封裝的著色器資料。</span><span class="sxs-lookup"><span data-stu-id="733a8-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="733a8-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="733a8-112">Requirements</span></span>



| <span data-ttu-id="733a8-113">需求</span><span class="sxs-lookup"><span data-stu-id="733a8-113">Requirement</span></span> | <span data-ttu-id="733a8-114">值</span><span class="sxs-lookup"><span data-stu-id="733a8-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="733a8-115">標頭</span><span class="sxs-lookup"><span data-stu-id="733a8-115">Header</span></span><br/> | <dl> <span data-ttu-id="733a8-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="733a8-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733a8-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="733a8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733a8-118">函式</span><span class="sxs-lookup"><span data-stu-id="733a8-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="733a8-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="733a8-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





