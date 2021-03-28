---
title: RWTexture1DArray：： Load (int) 函數
description: 讀取紋理資料。 |RWTexture1DArray：： Load (int) 函數
ms.assetid: 8A9ABE4A-C9FA-4092-8C2B-24E55645CA64
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
ms.openlocfilehash: 4eb0dcbfe7a465756f865b90d2a39f65784bcd8a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973993"
---
# <a name="rwtexture1darrayloadint-function"></a><span data-ttu-id="e0cc0-105">RWTexture1DArray：： Load (int) 函數</span><span class="sxs-lookup"><span data-stu-id="e0cc0-105">RWTexture1DArray::Load(int) function</span></span>

<span data-ttu-id="e0cc0-106">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="e0cc0-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0cc0-107">語法</span><span class="sxs-lookup"><span data-stu-id="e0cc0-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="e0cc0-108">參數</span><span class="sxs-lookup"><span data-stu-id="e0cc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0cc0-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0cc0-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cc0-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="e0cc0-110">Type: **int**</span></span>

<span data-ttu-id="e0cc0-111">材質的位置。</span><span class="sxs-lookup"><span data-stu-id="e0cc0-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0cc0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0cc0-112">Return value</span></span>

<span data-ttu-id="e0cc0-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="e0cc0-113">Type:</span></span>

<span data-ttu-id="e0cc0-114">傳回型別符合 [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="e0cc0-114">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0cc0-115">備註</span><span class="sxs-lookup"><span data-stu-id="e0cc0-115">Remarks</span></span>

<span data-ttu-id="e0cc0-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="e0cc0-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e0cc0-117">頂點</span><span class="sxs-lookup"><span data-stu-id="e0cc0-117">Vertex</span></span> | <span data-ttu-id="e0cc0-118">船體</span><span class="sxs-lookup"><span data-stu-id="e0cc0-118">Hull</span></span> | <span data-ttu-id="e0cc0-119">網域</span><span class="sxs-lookup"><span data-stu-id="e0cc0-119">Domain</span></span> | <span data-ttu-id="e0cc0-120">幾何</span><span class="sxs-lookup"><span data-stu-id="e0cc0-120">Geometry</span></span> | <span data-ttu-id="e0cc0-121">像素</span><span class="sxs-lookup"><span data-stu-id="e0cc0-121">Pixel</span></span> | <span data-ttu-id="e0cc0-122">計算</span><span class="sxs-lookup"><span data-stu-id="e0cc0-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e0cc0-123">x</span><span class="sxs-lookup"><span data-stu-id="e0cc0-123">x</span></span>     | <span data-ttu-id="e0cc0-124">x</span><span class="sxs-lookup"><span data-stu-id="e0cc0-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e0cc0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0cc0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0cc0-126">載入方法</span><span class="sxs-lookup"><span data-stu-id="e0cc0-126">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 




