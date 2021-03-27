---
title: D3DX_Saturate_FLOAT 函式
description: 抓取給定浮點數的飽和值。
ms.assetid: 659df450-3535-44eb-b867-89529369f903
keywords:
- D3DX_Saturate_FLOAT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_Saturate_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3deabf5140d4f3f3bdfc2d6cce52f32385987ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854027"
---
# <a name="d3dx_saturate_float-function"></a><span data-ttu-id="57168-104">D3DX \_ 飽和 \_ FLOAT 函數</span><span class="sxs-lookup"><span data-stu-id="57168-104">D3DX\_Saturate\_FLOAT function</span></span>

<span data-ttu-id="57168-105">抓取給定浮點數的飽和值。</span><span class="sxs-lookup"><span data-stu-id="57168-105">Retrieves the saturated value of the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="57168-106">語法</span><span class="sxs-lookup"><span data-stu-id="57168-106">Syntax</span></span>

``` syntax
FLOAT D3DX_Saturate_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="57168-107">參數</span><span class="sxs-lookup"><span data-stu-id="57168-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57168-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="57168-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="57168-109">要使其飽和的值。</span><span class="sxs-lookup"><span data-stu-id="57168-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57168-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="57168-110">Return value</span></span>

<span data-ttu-id="57168-111">飽和值。</span><span class="sxs-lookup"><span data-stu-id="57168-111">The saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="57168-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="57168-112">Requirements</span></span>



| <span data-ttu-id="57168-113">需求</span><span class="sxs-lookup"><span data-stu-id="57168-113">Requirement</span></span> | <span data-ttu-id="57168-114">值</span><span class="sxs-lookup"><span data-stu-id="57168-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57168-115">標頭</span><span class="sxs-lookup"><span data-stu-id="57168-115">Header</span></span><br/> | <dl> <span data-ttu-id="57168-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="57168-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57168-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="57168-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57168-118">函式</span><span class="sxs-lookup"><span data-stu-id="57168-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="57168-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="57168-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





