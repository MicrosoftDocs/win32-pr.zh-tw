---
title: StructuredBuffer：： Load (int) 函數
description: 讀取緩衝區資料。 |StructuredBuffer：： Load (int) 函數
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
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
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974321"
---
# <a name="structuredbufferloadint-function"></a><span data-ttu-id="b64c7-105">StructuredBuffer：： Load (int) 函數</span><span class="sxs-lookup"><span data-stu-id="b64c7-105">StructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="b64c7-106">讀取緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="b64c7-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b64c7-107">語法</span><span class="sxs-lookup"><span data-stu-id="b64c7-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="b64c7-108">參數</span><span class="sxs-lookup"><span data-stu-id="b64c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64c7-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b64c7-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b64c7-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="b64c7-110">Type: **int**</span></span>

<span data-ttu-id="b64c7-111">緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="b64c7-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64c7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b64c7-112">Return value</span></span>

<span data-ttu-id="b64c7-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="b64c7-113">Type:</span></span>

<span data-ttu-id="b64c7-114">傳回型別符合 [**StructuredBuffer**](sm5-object-structuredbuffer.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="b64c7-114">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b64c7-115">備註</span><span class="sxs-lookup"><span data-stu-id="b64c7-115">Remarks</span></span>

<span data-ttu-id="b64c7-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b64c7-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b64c7-117">頂點</span><span class="sxs-lookup"><span data-stu-id="b64c7-117">Vertex</span></span> | <span data-ttu-id="b64c7-118">船體</span><span class="sxs-lookup"><span data-stu-id="b64c7-118">Hull</span></span> | <span data-ttu-id="b64c7-119">網域</span><span class="sxs-lookup"><span data-stu-id="b64c7-119">Domain</span></span> | <span data-ttu-id="b64c7-120">幾何</span><span class="sxs-lookup"><span data-stu-id="b64c7-120">Geometry</span></span> | <span data-ttu-id="b64c7-121">像素</span><span class="sxs-lookup"><span data-stu-id="b64c7-121">Pixel</span></span> | <span data-ttu-id="b64c7-122">計算</span><span class="sxs-lookup"><span data-stu-id="b64c7-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b64c7-123">x</span><span class="sxs-lookup"><span data-stu-id="b64c7-123">x</span></span>     | <span data-ttu-id="b64c7-124">x</span><span class="sxs-lookup"><span data-stu-id="b64c7-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b64c7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b64c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64c7-126">載入方法</span><span class="sxs-lookup"><span data-stu-id="b64c7-126">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 




