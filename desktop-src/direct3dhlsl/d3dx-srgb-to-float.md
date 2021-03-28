---
title: D3DX_SRGB_to_FLOAT 函式
description: 將 SRGB 值轉換為 FLOAT。 |D3DX_SRGB_to_FLOAT 函式
ms.assetid: 03e2ea09-3dd7-48cb-81b3-e11f7a9cf0ee
keywords:
- D3DX_SRGB_to_FLOAT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e1b5dc6224a06881e227b82e74436c4820aaf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946131"
---
# <a name="d3dx_srgb_to_float-function"></a><span data-ttu-id="c3335-105">D3DX \_ SRGB \_ 至 \_ FLOAT 函數</span><span class="sxs-lookup"><span data-stu-id="c3335-105">D3DX\_SRGB\_to\_FLOAT function</span></span>

<span data-ttu-id="c3335-106">將 SRGB 值轉換為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="c3335-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3335-107">語法</span><span class="sxs-lookup"><span data-stu-id="c3335-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT(
   UINT val
);
```

## <a name="parameters"></a><span data-ttu-id="c3335-108">參數</span><span class="sxs-lookup"><span data-stu-id="c3335-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3335-109">*瓦爾*</span><span class="sxs-lookup"><span data-stu-id="c3335-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="c3335-110">要轉換的 SRGB 值。</span><span class="sxs-lookup"><span data-stu-id="c3335-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3335-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3335-111">Return value</span></span>

<span data-ttu-id="c3335-112">已轉換的 SRGB 值。</span><span class="sxs-lookup"><span data-stu-id="c3335-112">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3335-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3335-113">Requirements</span></span>



| <span data-ttu-id="c3335-114">需求</span><span class="sxs-lookup"><span data-stu-id="c3335-114">Requirement</span></span> | <span data-ttu-id="c3335-115">值</span><span class="sxs-lookup"><span data-stu-id="c3335-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3335-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c3335-116">Header</span></span><br/> | <dl> <span data-ttu-id="c3335-117"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="c3335-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3335-118">請參閱</span><span class="sxs-lookup"><span data-stu-id="c3335-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3335-119">函式</span><span class="sxs-lookup"><span data-stu-id="c3335-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c3335-120">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="c3335-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





