---
title: def-vs
description: 定義頂點著色器常數。
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186090"
---
# <a name="def---vs"></a><span data-ttu-id="ee07d-103">def-vs</span><span class="sxs-lookup"><span data-stu-id="ee07d-103">def - vs</span></span>

<span data-ttu-id="ee07d-104">定義頂點著色器常數。</span><span class="sxs-lookup"><span data-stu-id="ee07d-104">Defines vertex shader constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee07d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee07d-105">Syntax</span></span>



| <span data-ttu-id="ee07d-106">def dst、float1、float2、float3、float4</span><span class="sxs-lookup"><span data-stu-id="ee07d-106">def dst, float1, float2, float3, float4</span></span> |
|-----------------------------------------|



 

<span data-ttu-id="ee07d-107">其中</span><span class="sxs-lookup"><span data-stu-id="ee07d-107">where</span></span>

-   <span data-ttu-id="ee07d-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="ee07d-108">dst is the destination register.</span></span>
-   <span data-ttu-id="ee07d-109">float1、float2、float3、float4 是四個浮點數。</span><span class="sxs-lookup"><span data-stu-id="ee07d-109">float1, float2, float3, float4 are four floating point numbers.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee07d-110">備註</span><span class="sxs-lookup"><span data-stu-id="ee07d-110">Remarks</span></span>



| <span data-ttu-id="ee07d-111">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="ee07d-111">Vertex shader versions</span></span> | <span data-ttu-id="ee07d-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="ee07d-112">1\_1</span></span> | <span data-ttu-id="ee07d-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ee07d-113">2\_0</span></span> | <span data-ttu-id="ee07d-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ee07d-114">2\_x</span></span> | <span data-ttu-id="ee07d-115">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ee07d-115">2\_sw</span></span> | <span data-ttu-id="ee07d-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ee07d-116">3\_0</span></span> | <span data-ttu-id="ee07d-117">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ee07d-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ee07d-118">def</span><span class="sxs-lookup"><span data-stu-id="ee07d-118">def</span></span>                    | <span data-ttu-id="ee07d-119">x</span><span class="sxs-lookup"><span data-stu-id="ee07d-119">x</span></span>    | <span data-ttu-id="ee07d-120">x</span><span class="sxs-lookup"><span data-stu-id="ee07d-120">x</span></span>    | <span data-ttu-id="ee07d-121">x</span><span class="sxs-lookup"><span data-stu-id="ee07d-121">x</span></span>    | <span data-ttu-id="ee07d-122">x</span><span class="sxs-lookup"><span data-stu-id="ee07d-122">x</span></span>     | <span data-ttu-id="ee07d-123">x</span><span class="sxs-lookup"><span data-stu-id="ee07d-123">x</span></span>    | <span data-ttu-id="ee07d-124">x</span><span class="sxs-lookup"><span data-stu-id="ee07d-124">x</span></span>     |



 

<span data-ttu-id="ee07d-125">Def 指令會定義著色器常數，其值會在著色器設定為裝置時載入。</span><span class="sxs-lookup"><span data-stu-id="ee07d-125">The def instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="ee07d-126">這些都稱為立即常數。</span><span class="sxs-lookup"><span data-stu-id="ee07d-126">These are called immediate constants.</span></span> <span data-ttu-id="ee07d-127">立即的常數優先于 API 方法 SetVertexShaderConstantF 所設定的常數。</span><span class="sxs-lookup"><span data-stu-id="ee07d-127">Immediate constants take precedence over constants set by API methods SetVertexShaderConstantF.</span></span>

<span data-ttu-id="ee07d-128">有兩種方式可以設定著色器中的常數。</span><span class="sxs-lookup"><span data-stu-id="ee07d-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="ee07d-129">使用 def-vs，直接在著色器內定義常數。</span><span class="sxs-lookup"><span data-stu-id="ee07d-129">Use def - vs to define the constant directly inside a shader.</span></span>

    <span data-ttu-id="ee07d-130">def-vs 只能定義浮點數常數。</span><span class="sxs-lookup"><span data-stu-id="ee07d-130">def - vs can only define floating-point constants.</span></span>

2.  <span data-ttu-id="ee07d-131">使用 API 方法來設定常數。</span><span class="sxs-lookup"><span data-stu-id="ee07d-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="ee07d-132">使用 [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) 設定浮點數常數。</span><span class="sxs-lookup"><span data-stu-id="ee07d-132">Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) to set a floating-point constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee07d-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee07d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee07d-134">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="ee07d-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="ee07d-135">defi-vs</span><span class="sxs-lookup"><span data-stu-id="ee07d-135">defi - vs</span></span>](defi---vs.md)
</dt> <dt>

[<span data-ttu-id="ee07d-136">defb-vs</span><span class="sxs-lookup"><span data-stu-id="ee07d-136">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 