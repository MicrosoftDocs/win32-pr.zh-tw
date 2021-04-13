---
title: Buffer：： Operator 函數
description: 傳回唯讀的資源變數。 |Buffer：： Operator 函數
ms.assetid: 6a9e1176-439b-4565-9c7e-957d7c4045f0
keywords:
- Operator 函數直接寫入
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b811dd2409a00bb07f0b2441f6d57d4bd122f50
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386348"
---
# <a name="bufferoperator--function"></a><span data-ttu-id="2f777-105">Buffer：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="2f777-105">Buffer::Operator  function</span></span>

<span data-ttu-id="2f777-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="2f777-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f777-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f777-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="2f777-108">參數</span><span class="sxs-lookup"><span data-stu-id="2f777-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f777-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f777-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f777-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="2f777-110">Type: **uint**</span></span>

<span data-ttu-id="2f777-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="2f777-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f777-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f777-112">Return value</span></span>

<span data-ttu-id="2f777-113">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="2f777-113">Type: **R**</span></span>

<span data-ttu-id="2f777-114">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="2f777-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f777-115">備註</span><span class="sxs-lookup"><span data-stu-id="2f777-115">Remarks</span></span>

<span data-ttu-id="2f777-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="2f777-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2f777-117">頂點</span><span class="sxs-lookup"><span data-stu-id="2f777-117">Vertex</span></span> | <span data-ttu-id="2f777-118">船體</span><span class="sxs-lookup"><span data-stu-id="2f777-118">Hull</span></span> | <span data-ttu-id="2f777-119">網域</span><span class="sxs-lookup"><span data-stu-id="2f777-119">Domain</span></span> | <span data-ttu-id="2f777-120">幾何</span><span class="sxs-lookup"><span data-stu-id="2f777-120">Geometry</span></span> | <span data-ttu-id="2f777-121">像素</span><span class="sxs-lookup"><span data-stu-id="2f777-121">Pixel</span></span> | <span data-ttu-id="2f777-122">計算</span><span class="sxs-lookup"><span data-stu-id="2f777-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2f777-123">x</span><span class="sxs-lookup"><span data-stu-id="2f777-123">x</span></span>     | <span data-ttu-id="2f777-124">x</span><span class="sxs-lookup"><span data-stu-id="2f777-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2f777-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f777-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f777-126">Buffer</span><span class="sxs-lookup"><span data-stu-id="2f777-126">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="2f777-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2f777-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




