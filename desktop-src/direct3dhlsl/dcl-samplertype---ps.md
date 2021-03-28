---
title: 'dcl_samplerType (sm2、sm3-ps asm) '
description: 宣告圖元著色器取樣器。
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022855"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="3f706-103">dcl \_ samplerType (sm2、sm3-ps asm) </span><span class="sxs-lookup"><span data-stu-id="3f706-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="3f706-104">宣告圖元著色器取樣器。</span><span class="sxs-lookup"><span data-stu-id="3f706-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f706-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f706-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="3f706-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="3f706-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="3f706-107">其中：</span><span class="sxs-lookup"><span data-stu-id="3f706-107">where:</span></span>

-   <span data-ttu-id="3f706-108">\_samplerType 會定義取樣器資料類型。</span><span class="sxs-lookup"><span data-stu-id="3f706-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="3f706-109">這會決定取樣時，每個材質座標需要多少座標。</span><span class="sxs-lookup"><span data-stu-id="3f706-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="3f706-110">會定義下列紋理座標維度。</span><span class="sxs-lookup"><span data-stu-id="3f706-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="3f706-111">\_二 維和</span><span class="sxs-lookup"><span data-stu-id="3f706-111">\_2d</span></span>
    -   <span data-ttu-id="3f706-112">\_立方體</span><span class="sxs-lookup"><span data-stu-id="3f706-112">\_cube</span></span>
    -   <span data-ttu-id="3f706-113">\_體積</span><span class="sxs-lookup"><span data-stu-id="3f706-113">\_volume</span></span>
-   <span data-ttu-id="3f706-114">s \# 會識別一個取樣器，其中 s 是取樣器的縮寫，而 \# 是取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="3f706-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="3f706-115">取樣器是虛擬暫存器，因為您無法直接讀取或寫入它們。</span><span class="sxs-lookup"><span data-stu-id="3f706-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f706-116">備註</span><span class="sxs-lookup"><span data-stu-id="3f706-116">Remarks</span></span>



| <span data-ttu-id="3f706-117">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="3f706-117">Pixel shader versions</span></span> | <span data-ttu-id="3f706-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="3f706-118">1\_1</span></span> | <span data-ttu-id="3f706-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="3f706-119">1\_2</span></span> | <span data-ttu-id="3f706-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3f706-120">1\_3</span></span> | <span data-ttu-id="3f706-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="3f706-121">1\_4</span></span> | <span data-ttu-id="3f706-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f706-122">2\_0</span></span> | <span data-ttu-id="3f706-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3f706-123">2\_x</span></span> | <span data-ttu-id="3f706-124">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3f706-124">2\_sw</span></span> | <span data-ttu-id="3f706-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f706-125">3\_0</span></span> | <span data-ttu-id="3f706-126">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3f706-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3f706-127">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="3f706-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="3f706-128">x</span><span class="sxs-lookup"><span data-stu-id="3f706-128">x</span></span>    | <span data-ttu-id="3f706-129">x</span><span class="sxs-lookup"><span data-stu-id="3f706-129">x</span></span>    | <span data-ttu-id="3f706-130">x</span><span class="sxs-lookup"><span data-stu-id="3f706-130">x</span></span>     | <span data-ttu-id="3f706-131">x</span><span class="sxs-lookup"><span data-stu-id="3f706-131">x</span></span>    | <span data-ttu-id="3f706-132">x</span><span class="sxs-lookup"><span data-stu-id="3f706-132">x</span></span>     |



 

<span data-ttu-id="3f706-133">所有 \_ 的 dcl samplerType 指令都必須出現在第一個可執行指令之前。</span><span class="sxs-lookup"><span data-stu-id="3f706-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="3f706-134">範例</span><span class="sxs-lookup"><span data-stu-id="3f706-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="3f706-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="3f706-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f706-136">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="3f706-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




