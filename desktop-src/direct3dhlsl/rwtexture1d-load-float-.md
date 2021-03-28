---
title: RWTexture1D：： Load (int) 函數
description: 讀取紋理資料。 |RWTexture1D：： Load (int) 函數
ms.assetid: AA5E324E-A2C0-45C5-92A8-E4DBC4EB684C
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
ms.openlocfilehash: e78cd12502ada91e48df1ce88be6a19fb714327f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322223"
---
# <a name="rwtexture1dloadint-function"></a><span data-ttu-id="fda43-105">RWTexture1D：： Load (int) 函數</span><span class="sxs-lookup"><span data-stu-id="fda43-105">RWTexture1D::Load(int) function</span></span>

<span data-ttu-id="fda43-106">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="fda43-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda43-107">語法</span><span class="sxs-lookup"><span data-stu-id="fda43-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="fda43-108">參數</span><span class="sxs-lookup"><span data-stu-id="fda43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fda43-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fda43-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda43-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="fda43-110">Type: **int**</span></span>

<span data-ttu-id="fda43-111">材質的位置。</span><span class="sxs-lookup"><span data-stu-id="fda43-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fda43-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="fda43-112">Return value</span></span>

<span data-ttu-id="fda43-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="fda43-113">Type:</span></span>

<span data-ttu-id="fda43-114">傳回型別符合 [**RWTexture1D**](sm5-object-rwtexture1d.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="fda43-114">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fda43-115">備註</span><span class="sxs-lookup"><span data-stu-id="fda43-115">Remarks</span></span>

<span data-ttu-id="fda43-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="fda43-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fda43-117">頂點</span><span class="sxs-lookup"><span data-stu-id="fda43-117">Vertex</span></span> | <span data-ttu-id="fda43-118">船體</span><span class="sxs-lookup"><span data-stu-id="fda43-118">Hull</span></span> | <span data-ttu-id="fda43-119">網域</span><span class="sxs-lookup"><span data-stu-id="fda43-119">Domain</span></span> | <span data-ttu-id="fda43-120">幾何</span><span class="sxs-lookup"><span data-stu-id="fda43-120">Geometry</span></span> | <span data-ttu-id="fda43-121">像素</span><span class="sxs-lookup"><span data-stu-id="fda43-121">Pixel</span></span> | <span data-ttu-id="fda43-122">計算</span><span class="sxs-lookup"><span data-stu-id="fda43-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="fda43-123">x</span><span class="sxs-lookup"><span data-stu-id="fda43-123">x</span></span>     | <span data-ttu-id="fda43-124">x</span><span class="sxs-lookup"><span data-stu-id="fda43-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fda43-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fda43-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda43-126">載入方法</span><span class="sxs-lookup"><span data-stu-id="fda43-126">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 




