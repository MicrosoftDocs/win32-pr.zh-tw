---
title: defb-ps
description: 定義布林值常數值，此值應該會在著色器設定為裝置時載入。
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682826"
---
# <a name="defb---ps"></a><span data-ttu-id="e9d9a-103">defb-ps</span><span class="sxs-lookup"><span data-stu-id="e9d9a-103">defb - ps</span></span>

<span data-ttu-id="e9d9a-104">定義布林值常數值，此值應該會在著色器設定為裝置時載入。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-104">Defines a boolean constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d9a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9d9a-105">Syntax</span></span>



| <span data-ttu-id="e9d9a-106">defb dest，booleanValue</span><span class="sxs-lookup"><span data-stu-id="e9d9a-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="e9d9a-107">其中</span><span class="sxs-lookup"><span data-stu-id="e9d9a-107">where</span></span>

-   <span data-ttu-id="e9d9a-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e9d9a-109">booleanValue 是單一布林值，也就是 true 或 false。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-109">booleanValue is a single boolean value, either true or false.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9d9a-110">備註</span><span class="sxs-lookup"><span data-stu-id="e9d9a-110">Remarks</span></span>



| <span data-ttu-id="e9d9a-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="e9d9a-111">Pixel shader versions</span></span> | <span data-ttu-id="e9d9a-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e9d9a-112">1\_1</span></span> | <span data-ttu-id="e9d9a-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="e9d9a-113">1\_2</span></span> | <span data-ttu-id="e9d9a-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e9d9a-114">1\_3</span></span> | <span data-ttu-id="e9d9a-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="e9d9a-115">1\_4</span></span> | <span data-ttu-id="e9d9a-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e9d9a-116">2\_0</span></span> | <span data-ttu-id="e9d9a-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e9d9a-117">2\_x</span></span> | <span data-ttu-id="e9d9a-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e9d9a-118">2\_sw</span></span> | <span data-ttu-id="e9d9a-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e9d9a-119">3\_0</span></span> | <span data-ttu-id="e9d9a-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e9d9a-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e9d9a-121">defb</span><span class="sxs-lookup"><span data-stu-id="e9d9a-121">defb</span></span>                  |      |      |      |      |      | <span data-ttu-id="e9d9a-122">x</span><span class="sxs-lookup"><span data-stu-id="e9d9a-122">x</span></span>    | <span data-ttu-id="e9d9a-123">x</span><span class="sxs-lookup"><span data-stu-id="e9d9a-123">x</span></span>     | <span data-ttu-id="e9d9a-124">x</span><span class="sxs-lookup"><span data-stu-id="e9d9a-124">x</span></span>    | <span data-ttu-id="e9d9a-125">x</span><span class="sxs-lookup"><span data-stu-id="e9d9a-125">x</span></span>     |



 

<span data-ttu-id="e9d9a-126">Defb 指令會定義布林著色器常數，其值會在著色器設定為裝置時載入。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-126">The defb instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="e9d9a-127">這些都稱為立即常數。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-127">These are called immediate constants.</span></span> <span data-ttu-id="e9d9a-128">立即的常數優先于 API 方法 SetPixelShaderConstantB 所設定的常數。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-128">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="e9d9a-129">有兩種方式可以設定著色器中的 booleanconstant。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-129">There are two ways to set a booleanconstant in a shader.</span></span>

1.  <span data-ttu-id="e9d9a-130">您可以使用 defb，直接在著色器內定義常數。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-130">Use defb to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="e9d9a-131">使用 API 方法來設定常數。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="e9d9a-132">使用 [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) 設定布林值常數。</span><span class="sxs-lookup"><span data-stu-id="e9d9a-132">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9d9a-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9d9a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9d9a-134">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="e9d9a-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="e9d9a-135">def-ps</span><span class="sxs-lookup"><span data-stu-id="e9d9a-135">def - ps</span></span>](def---ps.md)
</dt> <dt>

[<span data-ttu-id="e9d9a-136">defi-ps</span><span class="sxs-lookup"><span data-stu-id="e9d9a-136">defi - ps</span></span>](defi---ps.md)
</dt> </dl>

 

 