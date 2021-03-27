---
title: D3DX_IsNan 函式
description: 判斷值是否為 NaN (不是) 的數位。
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- D3DX_IsNan 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aac82ebfb145bc11aac8d4ab509a4260767a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946230"
---
# <a name="d3dx_isnan-function"></a><span data-ttu-id="a563e-104">D3DX \_ IsNan 函式</span><span class="sxs-lookup"><span data-stu-id="a563e-104">D3DX\_IsNan function</span></span>

<span data-ttu-id="a563e-105">判斷值是否為 NaN (不是) 的數位。</span><span class="sxs-lookup"><span data-stu-id="a563e-105">Determines if the value is a NaN (Not a Number).</span></span>

## <a name="syntax"></a><span data-ttu-id="a563e-106">語法</span><span class="sxs-lookup"><span data-stu-id="a563e-106">Syntax</span></span>

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="a563e-107">參數</span><span class="sxs-lookup"><span data-stu-id="a563e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a563e-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="a563e-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="a563e-109">指定值。</span><span class="sxs-lookup"><span data-stu-id="a563e-109">The specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a563e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a563e-110">Return value</span></span>

<span data-ttu-id="a563e-111">如果是 NaN，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="a563e-111">true if a NaN; otherwise false.</span></span>

## <a name="requirements"></a><span data-ttu-id="a563e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a563e-112">Requirements</span></span>



| <span data-ttu-id="a563e-113">需求</span><span class="sxs-lookup"><span data-stu-id="a563e-113">Requirement</span></span> | <span data-ttu-id="a563e-114">值</span><span class="sxs-lookup"><span data-stu-id="a563e-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a563e-115">標頭</span><span class="sxs-lookup"><span data-stu-id="a563e-115">Header</span></span><br/> | <dl> <span data-ttu-id="a563e-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="a563e-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a563e-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="a563e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a563e-118">函式</span><span class="sxs-lookup"><span data-stu-id="a563e-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="a563e-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="a563e-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





