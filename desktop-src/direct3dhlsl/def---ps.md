---
title: def-ps
description: 定義圖元著色器浮點數常數。
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024034"
---
# <a name="def---ps"></a><span data-ttu-id="ddd7e-103">def-ps</span><span class="sxs-lookup"><span data-stu-id="ddd7e-103">def - ps</span></span>

<span data-ttu-id="ddd7e-104">定義圖元著色器浮點數常數。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-104">Defines pixel shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddd7e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddd7e-105">Syntax</span></span>



| <span data-ttu-id="ddd7e-106">def dst、fVvalue1、fValue2、fValue3、fValue4</span><span class="sxs-lookup"><span data-stu-id="ddd7e-106">def dst, fVvalue1, fValue2, fValue3, fValue4</span></span> |
|----------------------------------------------|



 

<span data-ttu-id="ddd7e-107">其中：</span><span class="sxs-lookup"><span data-stu-id="ddd7e-107">Where:</span></span>

-   <span data-ttu-id="ddd7e-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-108">dst is the destination register.</span></span>
-   <span data-ttu-id="ddd7e-109">fValue1 至 fValue4 是浮點值。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-109">fValue1 to fValue4 are floating-point values..</span></span>

## <a name="remarks"></a><span data-ttu-id="ddd7e-110">備註</span><span class="sxs-lookup"><span data-stu-id="ddd7e-110">Remarks</span></span>



| <span data-ttu-id="ddd7e-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="ddd7e-111">Pixel shader versions</span></span> | <span data-ttu-id="ddd7e-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="ddd7e-112">1\_1</span></span> | <span data-ttu-id="ddd7e-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="ddd7e-113">1\_2</span></span> | <span data-ttu-id="ddd7e-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ddd7e-114">1\_3</span></span> | <span data-ttu-id="ddd7e-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="ddd7e-115">1\_4</span></span> | <span data-ttu-id="ddd7e-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ddd7e-116">2\_0</span></span> | <span data-ttu-id="ddd7e-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-117">2\_x</span></span> | <span data-ttu-id="ddd7e-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ddd7e-118">2\_sw</span></span> | <span data-ttu-id="ddd7e-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ddd7e-119">3\_0</span></span> | <span data-ttu-id="ddd7e-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ddd7e-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ddd7e-121">def</span><span class="sxs-lookup"><span data-stu-id="ddd7e-121">def</span></span>                   | <span data-ttu-id="ddd7e-122">x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-122">x</span></span>    | <span data-ttu-id="ddd7e-123">x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-123">x</span></span>    | <span data-ttu-id="ddd7e-124">x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-124">x</span></span>    | <span data-ttu-id="ddd7e-125">x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-125">x</span></span>    | <span data-ttu-id="ddd7e-126">x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-126">x</span></span>    | <span data-ttu-id="ddd7e-127">x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-127">x</span></span>    | <span data-ttu-id="ddd7e-128">x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-128">x</span></span>     | <span data-ttu-id="ddd7e-129">x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-129">x</span></span>    | <span data-ttu-id="ddd7e-130">x</span><span class="sxs-lookup"><span data-stu-id="ddd7e-130">x</span></span>     |



 

<span data-ttu-id="ddd7e-131">有兩種方式可設定圖元著色器中的浮點數常數。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-131">There are two ways to set a floating-point constant in a pixel shader.</span></span>

1.  <span data-ttu-id="ddd7e-132">您可以使用 def，直接在著色器內定義常數。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-132">Use def to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="ddd7e-133">使用 API 來設定具有 [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)的常數。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-133">Use the API to set a constant with [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="ddd7e-134">def 定義了著色器常數，其值會在著色器設定為裝置時載入。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-134">def defines a shader constant whose value is loaded any time a shader is set to a device.</span></span> <span data-ttu-id="ddd7e-135">這些都稱為立即常數。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-135">These are called immediate constants.</span></span> <span data-ttu-id="ddd7e-136">立即的常數優先于 API 方法所設定的常數。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-136">Immediate constants take precedence over constants set by the API method.</span></span>

-   <span data-ttu-id="ddd7e-137">必須出現在著色器中的第一個算術或定址指令之前。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-137">Must appear before the first arithmetic or addressing instruction in shader.</span></span>
-   <span data-ttu-id="ddd7e-138">可以混合使用 [ (的 sm2、sm3 ps asm) ](dcl---ps.md) 指示 (這是位於著色器) 開頭的另一種指令類型。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-138">Can be intermixed with [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) instructions (which are the other type of instruction that resides at the beginning of a shader).</span></span>
-   <span data-ttu-id="ddd7e-139">dst 註冊必須是 [常數註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-139">dst register must be a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>
-   <span data-ttu-id="ddd7e-140">寫入遮罩必須是 full (預設) 。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-140">Write mask must be full (default).</span></span>
-   <span data-ttu-id="ddd7e-141">如果在著色器中多次定義 [常數](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) 暫存器，則會保存最後一個暫存器。</span><span class="sxs-lookup"><span data-stu-id="ddd7e-141">If a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) is defined multiple times in a shader, the last one persists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddd7e-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="ddd7e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddd7e-143">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="ddd7e-143">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 