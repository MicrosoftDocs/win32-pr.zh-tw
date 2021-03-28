---
title: D3DX_SaturateSigned_FLOAT 函式
description: 從指定的 FLOAT 抓取帶正負號的飽和值。
ms.assetid: 2737ea61-5dbf-4451-bb4f-436e6ea95db6
keywords:
- D3DX_SaturateSigned_FLOAT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_SaturateSigned_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e6ccf5cf941b1abd3577efa5899b8d827e24e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196328"
---
# <a name="d3dx_saturatesigned_float-function"></a><span data-ttu-id="4e19b-104">D3DX \_ SaturateSigned \_ FLOAT 函數</span><span class="sxs-lookup"><span data-stu-id="4e19b-104">D3DX\_SaturateSigned\_FLOAT function</span></span>

<span data-ttu-id="4e19b-105">從指定的 FLOAT 抓取帶正負號的飽和值。</span><span class="sxs-lookup"><span data-stu-id="4e19b-105">Retrieves a signed saturated value from the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e19b-106">語法</span><span class="sxs-lookup"><span data-stu-id="4e19b-106">Syntax</span></span>

``` syntax
 D3DX_SaturateSigned_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="4e19b-107">參數</span><span class="sxs-lookup"><span data-stu-id="4e19b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e19b-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="4e19b-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="4e19b-109">要使其飽和的值。</span><span class="sxs-lookup"><span data-stu-id="4e19b-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e19b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e19b-110">Return value</span></span>

<span data-ttu-id="4e19b-111">帶正負號的飽和值。</span><span class="sxs-lookup"><span data-stu-id="4e19b-111">The signed saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e19b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e19b-112">Requirements</span></span>



| <span data-ttu-id="4e19b-113">需求</span><span class="sxs-lookup"><span data-stu-id="4e19b-113">Requirement</span></span> | <span data-ttu-id="4e19b-114">值</span><span class="sxs-lookup"><span data-stu-id="4e19b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e19b-115">標頭</span><span class="sxs-lookup"><span data-stu-id="4e19b-115">Header</span></span><br/> | <dl> <span data-ttu-id="4e19b-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="4e19b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e19b-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="4e19b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e19b-118">函式</span><span class="sxs-lookup"><span data-stu-id="4e19b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4e19b-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="4e19b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





