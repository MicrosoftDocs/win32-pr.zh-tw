---
title: D3DX_FLOAT_to_INT 函式
description: 將浮點值轉換為 INT。
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- D3DX_FLOAT_to_INT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c127ef20cdd21cbc83e466f75844b4f80f47f948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514701"
---
# <a name="d3dx_float_to_int-function"></a><span data-ttu-id="96b8b-104">\_將 FLOAT D3DX \_ 至 \_ INT 函數</span><span class="sxs-lookup"><span data-stu-id="96b8b-104">D3DX\_FLOAT\_to\_INT function</span></span>

<span data-ttu-id="96b8b-105">將浮點值轉換為 INT。</span><span class="sxs-lookup"><span data-stu-id="96b8b-105">Converts a FLOAT value to INT.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b8b-106">語法</span><span class="sxs-lookup"><span data-stu-id="96b8b-106">Syntax</span></span>

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="96b8b-107">參數</span><span class="sxs-lookup"><span data-stu-id="96b8b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b8b-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="96b8b-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="96b8b-109">V 值。</span><span class="sxs-lookup"><span data-stu-id="96b8b-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="96b8b-110">*\_調整*</span><span class="sxs-lookup"><span data-stu-id="96b8b-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="96b8b-111">比例值。</span><span class="sxs-lookup"><span data-stu-id="96b8b-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b8b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="96b8b-112">Return value</span></span>

<span data-ttu-id="96b8b-113">轉換的 FLOAT 值</span><span class="sxs-lookup"><span data-stu-id="96b8b-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="96b8b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="96b8b-114">Requirements</span></span>



| <span data-ttu-id="96b8b-115">需求</span><span class="sxs-lookup"><span data-stu-id="96b8b-115">Requirement</span></span> | <span data-ttu-id="96b8b-116">值</span><span class="sxs-lookup"><span data-stu-id="96b8b-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96b8b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="96b8b-117">Header</span></span><br/> | <dl> <span data-ttu-id="96b8b-118"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="96b8b-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96b8b-119">請參閱</span><span class="sxs-lookup"><span data-stu-id="96b8b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b8b-120">函式</span><span class="sxs-lookup"><span data-stu-id="96b8b-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="96b8b-121">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="96b8b-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





