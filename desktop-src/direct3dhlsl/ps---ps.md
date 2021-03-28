---
title: ps
description: 此指示會指定著色器版本號碼，並可在所有著色器版本上運作。
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990819"
---
# <a name="ps"></a><span data-ttu-id="18521-103">ps</span><span class="sxs-lookup"><span data-stu-id="18521-103">ps</span></span>

<span data-ttu-id="18521-104">此指示會指定著色器版本號碼，並可在所有著色器版本上運作。</span><span class="sxs-lookup"><span data-stu-id="18521-104">This instruction specifies the shader version number and works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="18521-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18521-105">Syntax</span></span>


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="18521-106">輸入引數</span><span class="sxs-lookup"><span data-stu-id="18521-106">Input Arguments</span></span>

<span data-ttu-id="18521-107">輸入引數包含單一的主要版本號碼，其具有單一的子版本號碼。</span><span class="sxs-lookup"><span data-stu-id="18521-107">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="18521-108">下表列出允許的組合。</span><span class="sxs-lookup"><span data-stu-id="18521-108">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="18521-109">主要版本</span><span class="sxs-lookup"><span data-stu-id="18521-109">Main versions</span></span> | <span data-ttu-id="18521-110">次要版本</span><span class="sxs-lookup"><span data-stu-id="18521-110">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="18521-111">1</span><span class="sxs-lookup"><span data-stu-id="18521-111">1</span></span>             | <span data-ttu-id="18521-112">1、2、3、4</span><span class="sxs-lookup"><span data-stu-id="18521-112">1, 2, 3, 4</span></span>                     |
| <span data-ttu-id="18521-113">2</span><span class="sxs-lookup"><span data-stu-id="18521-113">2</span></span>             | <span data-ttu-id="18521-114">0、x (擴充) 、軟體 (軟體) </span><span class="sxs-lookup"><span data-stu-id="18521-114">0, x (extended), sw (software)</span></span> |
| <span data-ttu-id="18521-115">3</span><span class="sxs-lookup"><span data-stu-id="18521-115">3</span></span>             | <span data-ttu-id="18521-116">0、sw (軟體) </span><span class="sxs-lookup"><span data-stu-id="18521-116">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="18521-117">備註</span><span class="sxs-lookup"><span data-stu-id="18521-117">Remarks</span></span>



| <span data-ttu-id="18521-118">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="18521-118">Pixel shader versions</span></span> | <span data-ttu-id="18521-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="18521-119">1\_1</span></span> | <span data-ttu-id="18521-120">1\_2</span><span class="sxs-lookup"><span data-stu-id="18521-120">1\_2</span></span> | <span data-ttu-id="18521-121">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="18521-121">1\_3</span></span> | <span data-ttu-id="18521-122">1\_4</span><span class="sxs-lookup"><span data-stu-id="18521-122">1\_4</span></span> | <span data-ttu-id="18521-123">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="18521-123">2\_0</span></span> | <span data-ttu-id="18521-124">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="18521-124">2\_x</span></span> | <span data-ttu-id="18521-125">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="18521-125">2\_sw</span></span> | <span data-ttu-id="18521-126">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="18521-126">3\_0</span></span> | <span data-ttu-id="18521-127">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="18521-127">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="18521-128">ps</span><span class="sxs-lookup"><span data-stu-id="18521-128">ps</span></span>                    | <span data-ttu-id="18521-129">x</span><span class="sxs-lookup"><span data-stu-id="18521-129">x</span></span>    | <span data-ttu-id="18521-130">x</span><span class="sxs-lookup"><span data-stu-id="18521-130">x</span></span>    | <span data-ttu-id="18521-131">x</span><span class="sxs-lookup"><span data-stu-id="18521-131">x</span></span>    | <span data-ttu-id="18521-132">x</span><span class="sxs-lookup"><span data-stu-id="18521-132">x</span></span>    | <span data-ttu-id="18521-133">x</span><span class="sxs-lookup"><span data-stu-id="18521-133">x</span></span>    | <span data-ttu-id="18521-134">x</span><span class="sxs-lookup"><span data-stu-id="18521-134">x</span></span>    | <span data-ttu-id="18521-135">x</span><span class="sxs-lookup"><span data-stu-id="18521-135">x</span></span>     | <span data-ttu-id="18521-136">x</span><span class="sxs-lookup"><span data-stu-id="18521-136">x</span></span>    | <span data-ttu-id="18521-137">x</span><span class="sxs-lookup"><span data-stu-id="18521-137">x</span></span>     |



 

<span data-ttu-id="18521-138">此指令必須是圖元著色器中的第一個非批註指令。</span><span class="sxs-lookup"><span data-stu-id="18521-138">This instruction must be the first non-comment instruction in a pixel shader.</span></span>

<span data-ttu-id="18521-139">硬體加速版本的軟體 (版本號碼) 的無軟體版本 \_ ，可以處理具有硬體 accelearation 或使用軟體頂點處理的頂點。</span><span class="sxs-lookup"><span data-stu-id="18521-139">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="18521-140">軟體版本 (版本 \_ 號碼中的 sw 版，) 只使用軟體處理頂點。</span><span class="sxs-lookup"><span data-stu-id="18521-140">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="18521-141">範例</span><span class="sxs-lookup"><span data-stu-id="18521-141">Examples</span></span>

<span data-ttu-id="18521-142">這個部分範例會宣告第1版的 \_ 圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="18521-142">This partial example declares a version 1\_1 pixel shader.</span></span>


```
ps_1_1
```



<span data-ttu-id="18521-143">這個部分範例會宣告第1版的 \_ 圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="18521-143">This partial example declares a version 1\_4 pixel shader.</span></span>


```
ps_1_4
```



## <a name="related-topics"></a><span data-ttu-id="18521-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="18521-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18521-145">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="18521-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




