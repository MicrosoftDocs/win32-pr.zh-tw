---
title: D3DX_INT_to_FLOAT 函式
description: 將 INT 值轉換為 FLOAT。
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- D3DX_INT_to_FLOAT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974695"
---
# <a name="d3dx_int_to_float-function"></a><span data-ttu-id="5a48a-104">D3DX \_ INT \_ 至 \_ FLOAT 函數</span><span class="sxs-lookup"><span data-stu-id="5a48a-104">D3DX\_INT\_to\_FLOAT function</span></span>

<span data-ttu-id="5a48a-105">將 INT 值轉換為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="5a48a-105">Converts a INT value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a48a-106">語法</span><span class="sxs-lookup"><span data-stu-id="5a48a-106">Syntax</span></span>

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="5a48a-107">參數</span><span class="sxs-lookup"><span data-stu-id="5a48a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a48a-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="5a48a-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="5a48a-109">V 值。</span><span class="sxs-lookup"><span data-stu-id="5a48a-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="5a48a-110">*\_調整*</span><span class="sxs-lookup"><span data-stu-id="5a48a-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="5a48a-111">比例值。</span><span class="sxs-lookup"><span data-stu-id="5a48a-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a48a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a48a-112">Return value</span></span>

<span data-ttu-id="5a48a-113">已轉換的 int 值。</span><span class="sxs-lookup"><span data-stu-id="5a48a-113">The converted int value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a48a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a48a-114">Requirements</span></span>



| <span data-ttu-id="5a48a-115">需求</span><span class="sxs-lookup"><span data-stu-id="5a48a-115">Requirement</span></span> | <span data-ttu-id="5a48a-116">值</span><span class="sxs-lookup"><span data-stu-id="5a48a-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a48a-117">標頭</span><span class="sxs-lookup"><span data-stu-id="5a48a-117">Header</span></span><br/> | <dl> <span data-ttu-id="5a48a-118"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="5a48a-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a48a-119">請參閱</span><span class="sxs-lookup"><span data-stu-id="5a48a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a48a-120">函式</span><span class="sxs-lookup"><span data-stu-id="5a48a-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5a48a-121">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="5a48a-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





