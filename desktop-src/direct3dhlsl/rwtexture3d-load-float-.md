---
title: RWTexture3D：： Load (int) 函數
description: 讀取紋理資料。 |RWTexture3D：： Load (int) 函數
ms.assetid: 93C4FFFF-8695-4BAF-BAE4-A2704332E6A9
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
ms.openlocfilehash: 70f001cbea05f21a96bfbf1b5bdbf43a1d7da07d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322216"
---
# <a name="rwtexture3dloadint-function"></a><span data-ttu-id="8cb26-105">RWTexture3D：： Load (int) 函數</span><span class="sxs-lookup"><span data-stu-id="8cb26-105">RWTexture3D::Load(int) function</span></span>

<span data-ttu-id="8cb26-106">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="8cb26-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cb26-107">語法</span><span class="sxs-lookup"><span data-stu-id="8cb26-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="8cb26-108">參數</span><span class="sxs-lookup"><span data-stu-id="8cb26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cb26-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8cb26-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb26-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="8cb26-110">Type: **int**</span></span>

<span data-ttu-id="8cb26-111">材質的位置。</span><span class="sxs-lookup"><span data-stu-id="8cb26-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cb26-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cb26-112">Return value</span></span>

<span data-ttu-id="8cb26-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="8cb26-113">Type:</span></span>

<span data-ttu-id="8cb26-114">傳回型別符合 [**RWTexture3D**](sm5-object-rwtexture3d.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="8cb26-114">The return type matches the type in the declaration for the [**RWTexture3D**](sm5-object-rwtexture3d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cb26-115">備註</span><span class="sxs-lookup"><span data-stu-id="8cb26-115">Remarks</span></span>

<span data-ttu-id="8cb26-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="8cb26-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8cb26-117">頂點</span><span class="sxs-lookup"><span data-stu-id="8cb26-117">Vertex</span></span> | <span data-ttu-id="8cb26-118">船體</span><span class="sxs-lookup"><span data-stu-id="8cb26-118">Hull</span></span> | <span data-ttu-id="8cb26-119">網域</span><span class="sxs-lookup"><span data-stu-id="8cb26-119">Domain</span></span> | <span data-ttu-id="8cb26-120">幾何</span><span class="sxs-lookup"><span data-stu-id="8cb26-120">Geometry</span></span> | <span data-ttu-id="8cb26-121">像素</span><span class="sxs-lookup"><span data-stu-id="8cb26-121">Pixel</span></span> | <span data-ttu-id="8cb26-122">計算</span><span class="sxs-lookup"><span data-stu-id="8cb26-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8cb26-123">x</span><span class="sxs-lookup"><span data-stu-id="8cb26-123">x</span></span>     | <span data-ttu-id="8cb26-124">x</span><span class="sxs-lookup"><span data-stu-id="8cb26-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8cb26-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cb26-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb26-126">載入方法</span><span class="sxs-lookup"><span data-stu-id="8cb26-126">Load methods</span></span>](rwtexture3d-load.md)
</dt> </dl>

 

 




