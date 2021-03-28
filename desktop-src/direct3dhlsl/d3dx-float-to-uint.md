---
title: D3DX_FLOAT_to_UINT 函式
description: 將浮點值轉換成 UINT。
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- D3DX_FLOAT_to_UINT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e729ba805d63068844192a134236722288fe8a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322695"
---
# <a name="d3dx_float_to_uint-function"></a><span data-ttu-id="22ee1-104">D3DX \_ FLOAT \_ 到 \_ UINT 函數</span><span class="sxs-lookup"><span data-stu-id="22ee1-104">D3DX\_FLOAT\_to\_UINT function</span></span>

<span data-ttu-id="22ee1-105">將浮點值轉換成 UINT。</span><span class="sxs-lookup"><span data-stu-id="22ee1-105">Converts a FLOAT value to UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ee1-106">語法</span><span class="sxs-lookup"><span data-stu-id="22ee1-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="22ee1-107">參數</span><span class="sxs-lookup"><span data-stu-id="22ee1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ee1-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="22ee1-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="22ee1-109">V 向量。</span><span class="sxs-lookup"><span data-stu-id="22ee1-109">The v vector.</span></span>

</dd> <dt>

<span data-ttu-id="22ee1-110">*\_調整*</span><span class="sxs-lookup"><span data-stu-id="22ee1-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="22ee1-111">比例值。</span><span class="sxs-lookup"><span data-stu-id="22ee1-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22ee1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="22ee1-112">Return value</span></span>

<span data-ttu-id="22ee1-113">轉換的 FLOAT 值</span><span class="sxs-lookup"><span data-stu-id="22ee1-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="22ee1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="22ee1-114">Requirements</span></span>



| <span data-ttu-id="22ee1-115">需求</span><span class="sxs-lookup"><span data-stu-id="22ee1-115">Requirement</span></span> | <span data-ttu-id="22ee1-116">值</span><span class="sxs-lookup"><span data-stu-id="22ee1-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22ee1-117">標頭</span><span class="sxs-lookup"><span data-stu-id="22ee1-117">Header</span></span><br/> | <dl> <span data-ttu-id="22ee1-118"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="22ee1-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22ee1-119">請參閱</span><span class="sxs-lookup"><span data-stu-id="22ee1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ee1-120">函式</span><span class="sxs-lookup"><span data-stu-id="22ee1-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="22ee1-121">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="22ee1-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





