---
title: 'abort 函數 (Corecrt \_ terminate. h) '
description: 將錯誤訊息提交至資訊佇列，並終止目前正在執行的繪圖或分派呼叫。
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- abort 函式 HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974729"
---
# <a name="abort-function"></a><span data-ttu-id="dfbf4-104">abort 函式</span><span class="sxs-lookup"><span data-stu-id="dfbf4-104">abort function</span></span>

<span data-ttu-id="dfbf4-105">將錯誤訊息提交至資訊佇列，並終止目前正在執行的繪圖或分派呼叫。</span><span class="sxs-lookup"><span data-stu-id="dfbf4-105">Submits an error message to the information queue and terminates the current draw or dispatch call being executed.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfbf4-106">語法</span><span class="sxs-lookup"><span data-stu-id="dfbf4-106">Syntax</span></span>

``` syntax
void abort(
    
);
```

## <a name="parameters"></a><span data-ttu-id="dfbf4-107">參數</span><span class="sxs-lookup"><span data-stu-id="dfbf4-107">Parameters</span></span>

<dl> <dt>

 
</dt> <dd>

<span data-ttu-id="dfbf4-108">None</span><span class="sxs-lookup"><span data-stu-id="dfbf4-108">None</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfbf4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="dfbf4-109">Return value</span></span>

<span data-ttu-id="dfbf4-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="dfbf4-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfbf4-111">備註</span><span class="sxs-lookup"><span data-stu-id="dfbf4-111">Remarks</span></span>

<span data-ttu-id="dfbf4-112">此作業不會在不支援的 rasterizers 上執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="dfbf4-112">This operation does nothing on rasterizers that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="dfbf4-113">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="dfbf4-113">Minimum Shader Model</span></span>

<span data-ttu-id="dfbf4-114">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="dfbf4-114">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dfbf4-115">著色器模型</span><span class="sxs-lookup"><span data-stu-id="dfbf4-115">Shader Model</span></span>                                                        | <span data-ttu-id="dfbf4-116">支援</span><span class="sxs-lookup"><span data-stu-id="dfbf4-116">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="dfbf4-117">著色器模型 4 (DirectX HLSL) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="dfbf4-117">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dfbf4-118">是</span><span class="sxs-lookup"><span data-stu-id="dfbf4-118">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="dfbf4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfbf4-119">Requirements</span></span>



| <span data-ttu-id="dfbf4-120">需求</span><span class="sxs-lookup"><span data-stu-id="dfbf4-120">Requirement</span></span> | <span data-ttu-id="dfbf4-121">值</span><span class="sxs-lookup"><span data-stu-id="dfbf4-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbf4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="dfbf4-122">Header</span></span><br/> | <dl> <span data-ttu-id="dfbf4-123"><dt>Corecrt \_ terminate。h</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf4-123"><dt>Corecrt\_terminate.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfbf4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfbf4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfbf4-125">內建函式</span><span class="sxs-lookup"><span data-stu-id="dfbf4-125">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





