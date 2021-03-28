---
title: D3DX_FLOAT_to_SRGB 函式
description: 將 FLOAT 值轉換成 SRGB。
ms.assetid: 734a0837-98da-45ba-bb0b-1e930ba78a7d
keywords:
- D3DX_FLOAT_to_SRGB 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71afb0c4e601be70c1ec04bd7bcd5e76c6cc573
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992359"
---
# <a name="d3dx_float_to_srgb-function"></a><span data-ttu-id="9fd54-104">\_將 FLOAT D3DX \_ 至 \_ SRGB 函數</span><span class="sxs-lookup"><span data-stu-id="9fd54-104">D3DX\_FLOAT\_to\_SRGB function</span></span>

<span data-ttu-id="9fd54-105">將 FLOAT 值轉換成 SRGB。</span><span class="sxs-lookup"><span data-stu-id="9fd54-105">Converts a FLOAT value to an SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd54-106">語法</span><span class="sxs-lookup"><span data-stu-id="9fd54-106">Syntax</span></span>

``` syntax
FLOAT D3DX_FLOAT_to_SRGB(
   FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="9fd54-107">參數</span><span class="sxs-lookup"><span data-stu-id="9fd54-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fd54-108">*瓦爾*</span><span class="sxs-lookup"><span data-stu-id="9fd54-108">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd54-109">要轉換的 FLOAT 值。</span><span class="sxs-lookup"><span data-stu-id="9fd54-109">FLOAT value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fd54-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fd54-110">Return value</span></span>

<span data-ttu-id="9fd54-111">已轉換的 SRGB 值。</span><span class="sxs-lookup"><span data-stu-id="9fd54-111">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fd54-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fd54-112">Requirements</span></span>



| <span data-ttu-id="9fd54-113">需求</span><span class="sxs-lookup"><span data-stu-id="9fd54-113">Requirement</span></span> | <span data-ttu-id="9fd54-114">值</span><span class="sxs-lookup"><span data-stu-id="9fd54-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd54-115">標頭</span><span class="sxs-lookup"><span data-stu-id="9fd54-115">Header</span></span><br/> | <dl> <span data-ttu-id="9fd54-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="9fd54-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd54-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="9fd54-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd54-118">函式</span><span class="sxs-lookup"><span data-stu-id="9fd54-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="9fd54-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="9fd54-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





