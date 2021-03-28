---
title: RWTexture2D：： Load (int) 函數
description: 讀取紋理資料。 |RWTexture2D：： Load (int) 函數
ms.assetid: AEBB9C78-BE4B-4121-93CC-EE03B9925CF0
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
ms.openlocfilehash: ab5f8d755ad4af3127a0c238defc9f1c422061bc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992006"
---
# <a name="rwtexture2dloadint-function"></a><span data-ttu-id="5b206-105">RWTexture2D：： Load (int) 函數</span><span class="sxs-lookup"><span data-stu-id="5b206-105">RWTexture2D::Load(int) function</span></span>

<span data-ttu-id="5b206-106">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="5b206-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b206-107">語法</span><span class="sxs-lookup"><span data-stu-id="5b206-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="5b206-108">參數</span><span class="sxs-lookup"><span data-stu-id="5b206-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b206-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b206-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b206-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="5b206-110">Type: **int**</span></span>

<span data-ttu-id="5b206-111">材質的位置。</span><span class="sxs-lookup"><span data-stu-id="5b206-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b206-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b206-112">Return value</span></span>

<span data-ttu-id="5b206-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="5b206-113">Type:</span></span>

<span data-ttu-id="5b206-114">傳回型別符合 [**RWTexture2D**](sm5-object-rwtexture2d.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="5b206-114">The return type matches the type in the declaration for the [**RWTexture2D**](sm5-object-rwtexture2d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b206-115">備註</span><span class="sxs-lookup"><span data-stu-id="5b206-115">Remarks</span></span>

<span data-ttu-id="5b206-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="5b206-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5b206-117">頂點</span><span class="sxs-lookup"><span data-stu-id="5b206-117">Vertex</span></span> | <span data-ttu-id="5b206-118">船體</span><span class="sxs-lookup"><span data-stu-id="5b206-118">Hull</span></span> | <span data-ttu-id="5b206-119">網域</span><span class="sxs-lookup"><span data-stu-id="5b206-119">Domain</span></span> | <span data-ttu-id="5b206-120">幾何</span><span class="sxs-lookup"><span data-stu-id="5b206-120">Geometry</span></span> | <span data-ttu-id="5b206-121">像素</span><span class="sxs-lookup"><span data-stu-id="5b206-121">Pixel</span></span> | <span data-ttu-id="5b206-122">計算</span><span class="sxs-lookup"><span data-stu-id="5b206-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5b206-123">x</span><span class="sxs-lookup"><span data-stu-id="5b206-123">x</span></span>     | <span data-ttu-id="5b206-124">x</span><span class="sxs-lookup"><span data-stu-id="5b206-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5b206-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b206-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b206-126">載入方法</span><span class="sxs-lookup"><span data-stu-id="5b206-126">Load methods</span></span>](rwtexture2d-load.md)
</dt> </dl>

 

 




