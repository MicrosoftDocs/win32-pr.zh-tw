---
title: vs
description: 此指示會指定著色器版本號碼。 此指示適用于所有著色器版本。
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373895"
---
# <a name="vs"></a><span data-ttu-id="48500-104">vs</span><span class="sxs-lookup"><span data-stu-id="48500-104">vs</span></span>

<span data-ttu-id="48500-105">此指示會指定著色器版本號碼。</span><span class="sxs-lookup"><span data-stu-id="48500-105">This instruction specifies the shader version number.</span></span> <span data-ttu-id="48500-106">此指示適用于所有著色器版本。</span><span class="sxs-lookup"><span data-stu-id="48500-106">This instruction works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="48500-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="48500-107">Syntax</span></span>


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="48500-108">輸入引數</span><span class="sxs-lookup"><span data-stu-id="48500-108">Input Arguments</span></span>

<span data-ttu-id="48500-109">輸入引數包含單一的主要版本號碼，其具有單一的子版本號碼。</span><span class="sxs-lookup"><span data-stu-id="48500-109">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="48500-110">下表列出允許的組合。</span><span class="sxs-lookup"><span data-stu-id="48500-110">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="48500-111">主要版本</span><span class="sxs-lookup"><span data-stu-id="48500-111">Main versions</span></span> | <span data-ttu-id="48500-112">次要版本</span><span class="sxs-lookup"><span data-stu-id="48500-112">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="48500-113">1</span><span class="sxs-lookup"><span data-stu-id="48500-113">1</span></span>             | <span data-ttu-id="48500-114">1</span><span class="sxs-lookup"><span data-stu-id="48500-114">1</span></span>                              |
| <span data-ttu-id="48500-115">2</span><span class="sxs-lookup"><span data-stu-id="48500-115">2</span></span>             | <span data-ttu-id="48500-116">0、sw (software) 、x (擴充) </span><span class="sxs-lookup"><span data-stu-id="48500-116">0, sw (software), x (extended)</span></span> |
| <span data-ttu-id="48500-117">3</span><span class="sxs-lookup"><span data-stu-id="48500-117">3</span></span>             | <span data-ttu-id="48500-118">0、sw (軟體) </span><span class="sxs-lookup"><span data-stu-id="48500-118">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="48500-119">備註</span><span class="sxs-lookup"><span data-stu-id="48500-119">Remarks</span></span>



| <span data-ttu-id="48500-120">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="48500-120">Vertex shader versions</span></span> | <span data-ttu-id="48500-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="48500-121">1\_1</span></span> | <span data-ttu-id="48500-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48500-122">2\_0</span></span> | <span data-ttu-id="48500-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="48500-123">2\_x</span></span> | <span data-ttu-id="48500-124">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="48500-124">2\_sw</span></span> | <span data-ttu-id="48500-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48500-125">3\_0</span></span> | <span data-ttu-id="48500-126">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="48500-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="48500-127">vs</span><span class="sxs-lookup"><span data-stu-id="48500-127">vs</span></span>                     | <span data-ttu-id="48500-128">x</span><span class="sxs-lookup"><span data-stu-id="48500-128">x</span></span>    | <span data-ttu-id="48500-129">x</span><span class="sxs-lookup"><span data-stu-id="48500-129">x</span></span>    | <span data-ttu-id="48500-130">x</span><span class="sxs-lookup"><span data-stu-id="48500-130">x</span></span>    | <span data-ttu-id="48500-131">x</span><span class="sxs-lookup"><span data-stu-id="48500-131">x</span></span>     | <span data-ttu-id="48500-132">x</span><span class="sxs-lookup"><span data-stu-id="48500-132">x</span></span>    | <span data-ttu-id="48500-133">x</span><span class="sxs-lookup"><span data-stu-id="48500-133">x</span></span>     |



 

<span data-ttu-id="48500-134">此指令必須是頂點著色器中的第一個非批註指令。</span><span class="sxs-lookup"><span data-stu-id="48500-134">This instruction must be the first non-comment instruction in a vertex shader.</span></span>

<span data-ttu-id="48500-135">所有頂點著色器版本都支援此指令。</span><span class="sxs-lookup"><span data-stu-id="48500-135">This instruction is supported in all vertex shader versions.</span></span>

<span data-ttu-id="48500-136">硬體加速版本的軟體 (版本號碼) 的無軟體版本 \_ ，可以處理具有硬體 accelearation 或使用軟體頂點處理的頂點。</span><span class="sxs-lookup"><span data-stu-id="48500-136">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="48500-137">軟體版本 (版本 \_ 號碼中的 sw 版，) 只使用軟體處理頂點。</span><span class="sxs-lookup"><span data-stu-id="48500-137">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="48500-138">範例</span><span class="sxs-lookup"><span data-stu-id="48500-138">Examples</span></span>

<span data-ttu-id="48500-139">這個部分範例會宣告第1版 \_ 頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="48500-139">This partial example declares a version 1\_1 vertex shader.</span></span>


```
vs_1_1
```



<span data-ttu-id="48500-140">這個部分範例會宣告第2版軟體端點著色器。</span><span class="sxs-lookup"><span data-stu-id="48500-140">This partial example declares a version 2 software vertex shader.</span></span>


```
vs_2_sw
```



## <a name="related-topics"></a><span data-ttu-id="48500-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="48500-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48500-142">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="48500-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




