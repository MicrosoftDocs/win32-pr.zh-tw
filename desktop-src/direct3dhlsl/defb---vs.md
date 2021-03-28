---
title: defb-vs
description: 定義布林值常數值，此值應該會在著色器設定為裝置時，隨時載入。
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933264"
---
# <a name="defb---vs"></a><span data-ttu-id="2a2d2-103">defb-vs</span><span class="sxs-lookup"><span data-stu-id="2a2d2-103">defb - vs</span></span>

<span data-ttu-id="2a2d2-104">定義布林值常數值，此值應該會在著色器設定為裝置時，隨時載入。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-104">Defines a Boolean constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a2d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a2d2-105">Syntax</span></span>



| <span data-ttu-id="2a2d2-106">defb dest，booleanValue</span><span class="sxs-lookup"><span data-stu-id="2a2d2-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="2a2d2-107">其中</span><span class="sxs-lookup"><span data-stu-id="2a2d2-107">where</span></span>

-   <span data-ttu-id="2a2d2-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-108">dst is the destination register.</span></span>
-   <span data-ttu-id="2a2d2-109">booleanValue 是布林值，也就是 True 或 False。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-109">booleanValue is a boolean value, either True or False.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a2d2-110">備註</span><span class="sxs-lookup"><span data-stu-id="2a2d2-110">Remarks</span></span>



| <span data-ttu-id="2a2d2-111">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="2a2d2-111">Vertex shader versions</span></span> | <span data-ttu-id="2a2d2-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="2a2d2-112">1\_1</span></span> | <span data-ttu-id="2a2d2-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2a2d2-113">2\_0</span></span> | <span data-ttu-id="2a2d2-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2a2d2-114">2\_x</span></span> | <span data-ttu-id="2a2d2-115">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2a2d2-115">2\_sw</span></span> | <span data-ttu-id="2a2d2-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2a2d2-116">3\_0</span></span> | <span data-ttu-id="2a2d2-117">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2a2d2-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2a2d2-118">defb</span><span class="sxs-lookup"><span data-stu-id="2a2d2-118">defb</span></span>                   |      | <span data-ttu-id="2a2d2-119">x</span><span class="sxs-lookup"><span data-stu-id="2a2d2-119">x</span></span>    | <span data-ttu-id="2a2d2-120">x</span><span class="sxs-lookup"><span data-stu-id="2a2d2-120">x</span></span>    | <span data-ttu-id="2a2d2-121">x</span><span class="sxs-lookup"><span data-stu-id="2a2d2-121">x</span></span>     | <span data-ttu-id="2a2d2-122">x</span><span class="sxs-lookup"><span data-stu-id="2a2d2-122">x</span></span>    | <span data-ttu-id="2a2d2-123">x</span><span class="sxs-lookup"><span data-stu-id="2a2d2-123">x</span></span>     |



 

<span data-ttu-id="2a2d2-124">Defb-vs 指令會定義布林著色器常數，其值會在著色器設定為裝置時載入。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-124">The defb - vs instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="2a2d2-125">這些都稱為立即常數。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-125">These are called immediate constants.</span></span> <span data-ttu-id="2a2d2-126">立即的常數優先于 API 方法 SetVertexShaderConstantB 所設定的常數。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-126">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantB.</span></span>

<span data-ttu-id="2a2d2-127">有兩種方式可以設定著色器中的布林值常數。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-127">There are two ways to set a boolean constant in a shader.</span></span>

1.  <span data-ttu-id="2a2d2-128">使用 defb-vs，直接在著色器內定義常數。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-128">Use defb - vs to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="2a2d2-129">使用 API 方法來設定常數。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-129">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="2a2d2-130">使用 [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) 設定布林值常數。</span><span class="sxs-lookup"><span data-stu-id="2a2d2-130">Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a2d2-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a2d2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a2d2-132">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="2a2d2-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="2a2d2-133">def-vs</span><span class="sxs-lookup"><span data-stu-id="2a2d2-133">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="2a2d2-134">defi-vs</span><span class="sxs-lookup"><span data-stu-id="2a2d2-134">defi - vs</span></span>](defi---vs.md)
</dt> </dl>

 

 