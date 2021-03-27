---
title: AppendStructuredBuffer：： Append 函數
description: 將值附加至緩衝區的結尾。
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- 附加函式 HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "103932777"
---
# <a name="append-function"></a><span data-ttu-id="a88c4-104">Append 函數</span><span class="sxs-lookup"><span data-stu-id="a88c4-104">Append function</span></span>

<span data-ttu-id="a88c4-105">將值附加至緩衝區的結尾。</span><span class="sxs-lookup"><span data-stu-id="a88c4-105">Appends a value to the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88c4-106">語法</span><span class="sxs-lookup"><span data-stu-id="a88c4-106">Syntax</span></span>

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="a88c4-107">參數</span><span class="sxs-lookup"><span data-stu-id="a88c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a88c4-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a88c4-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88c4-109">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="a88c4-109">Type: **T**</span></span>

<span data-ttu-id="a88c4-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="a88c4-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a88c4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a88c4-111">Return value</span></span>

<span data-ttu-id="a88c4-112">無</span><span class="sxs-lookup"><span data-stu-id="a88c4-112">None</span></span>

## <a name="remarks"></a><span data-ttu-id="a88c4-113">備註</span><span class="sxs-lookup"><span data-stu-id="a88c4-113">Remarks</span></span>

<span data-ttu-id="a88c4-114">T 可以是任何資料類型，包括結構。</span><span class="sxs-lookup"><span data-stu-id="a88c4-114">T can be any data type including structures.</span></span>

<span data-ttu-id="a88c4-115">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="a88c4-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a88c4-116">頂點</span><span class="sxs-lookup"><span data-stu-id="a88c4-116">Vertex</span></span> | <span data-ttu-id="a88c4-117">船體</span><span class="sxs-lookup"><span data-stu-id="a88c4-117">Hull</span></span> | <span data-ttu-id="a88c4-118">網域</span><span class="sxs-lookup"><span data-stu-id="a88c4-118">Domain</span></span> | <span data-ttu-id="a88c4-119">幾何</span><span class="sxs-lookup"><span data-stu-id="a88c4-119">Geometry</span></span> | <span data-ttu-id="a88c4-120">像素</span><span class="sxs-lookup"><span data-stu-id="a88c4-120">Pixel</span></span> | <span data-ttu-id="a88c4-121">計算</span><span class="sxs-lookup"><span data-stu-id="a88c4-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a88c4-122">x</span><span class="sxs-lookup"><span data-stu-id="a88c4-122">x</span></span>      | <span data-ttu-id="a88c4-123">x</span><span class="sxs-lookup"><span data-stu-id="a88c4-123">x</span></span>    | <span data-ttu-id="a88c4-124">x</span><span class="sxs-lookup"><span data-stu-id="a88c4-124">x</span></span>      | <span data-ttu-id="a88c4-125">x</span><span class="sxs-lookup"><span data-stu-id="a88c4-125">x</span></span>        | <span data-ttu-id="a88c4-126">x</span><span class="sxs-lookup"><span data-stu-id="a88c4-126">x</span></span>     | <span data-ttu-id="a88c4-127">x</span><span class="sxs-lookup"><span data-stu-id="a88c4-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a88c4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a88c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88c4-129">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="a88c4-129">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="a88c4-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a88c4-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




