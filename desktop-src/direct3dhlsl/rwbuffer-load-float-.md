---
title: RWBuffer：： Load (int) 函數
description: 讀取緩衝區資料。 |RWBuffer：： Load (int) 函數
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
keywords:
- Load function HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 561f055990bbca683bf9c55b5805b8d3c55b3272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696410"
---
# <a name="rwbufferloadint-function"></a><span data-ttu-id="1761f-105">RWBuffer：： Load (int) 函數</span><span class="sxs-lookup"><span data-stu-id="1761f-105">RWBuffer::Load(int) function</span></span>

<span data-ttu-id="1761f-106">讀取緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="1761f-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1761f-107">語法</span><span class="sxs-lookup"><span data-stu-id="1761f-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="1761f-108">參數</span><span class="sxs-lookup"><span data-stu-id="1761f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1761f-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1761f-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1761f-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="1761f-110">Type: **int**</span></span>

<span data-ttu-id="1761f-111">緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="1761f-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1761f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1761f-112">Return value</span></span>

<span data-ttu-id="1761f-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="1761f-113">Type:</span></span>

<span data-ttu-id="1761f-114">傳回型別符合 [**RWBuffer**](sm5-object-rwbuffer.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="1761f-114">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1761f-115">備註</span><span class="sxs-lookup"><span data-stu-id="1761f-115">Remarks</span></span>

<span data-ttu-id="1761f-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="1761f-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1761f-117">頂點</span><span class="sxs-lookup"><span data-stu-id="1761f-117">Vertex</span></span> | <span data-ttu-id="1761f-118">船體</span><span class="sxs-lookup"><span data-stu-id="1761f-118">Hull</span></span> | <span data-ttu-id="1761f-119">網域</span><span class="sxs-lookup"><span data-stu-id="1761f-119">Domain</span></span> | <span data-ttu-id="1761f-120">幾何</span><span class="sxs-lookup"><span data-stu-id="1761f-120">Geometry</span></span> | <span data-ttu-id="1761f-121">像素</span><span class="sxs-lookup"><span data-stu-id="1761f-121">Pixel</span></span> | <span data-ttu-id="1761f-122">計算</span><span class="sxs-lookup"><span data-stu-id="1761f-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1761f-123">x</span><span class="sxs-lookup"><span data-stu-id="1761f-123">x</span></span>      | <span data-ttu-id="1761f-124">x</span><span class="sxs-lookup"><span data-stu-id="1761f-124">x</span></span>    | <span data-ttu-id="1761f-125">x</span><span class="sxs-lookup"><span data-stu-id="1761f-125">x</span></span>      | <span data-ttu-id="1761f-126">x</span><span class="sxs-lookup"><span data-stu-id="1761f-126">x</span></span>        | <span data-ttu-id="1761f-127">x</span><span class="sxs-lookup"><span data-stu-id="1761f-127">x</span></span>     | <span data-ttu-id="1761f-128">x</span><span class="sxs-lookup"><span data-stu-id="1761f-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1761f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1761f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1761f-130">載入方法</span><span class="sxs-lookup"><span data-stu-id="1761f-130">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 




