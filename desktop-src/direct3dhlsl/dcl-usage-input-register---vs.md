---
title: 'dcl_usage 輸入 (sm1、sm2、sm3-vs asm) '
description: 宣告頂點專案使用方式與頂點著色器輸入暫存器的使用方式索引之間的關聯。
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463353"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="d7d2c-103">dcl \_ 使用方式輸入 (sm1、sm2、sm3-vs asm) </span><span class="sxs-lookup"><span data-stu-id="d7d2c-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="d7d2c-104">宣告頂點專案使用方式與頂點著色器輸入暫存器的使用方式索引之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d2c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7d2c-105">Syntax</span></span>



|                                |
|--------------------------------|
| <span data-ttu-id="d7d2c-106">dcl \_ 使用方式 \[ 使用方式 \_ 索引 \] v\#</span><span class="sxs-lookup"><span data-stu-id="d7d2c-106">dcl\_usage\[usage\_index\] v\#</span></span> |



 

<span data-ttu-id="d7d2c-107">其中：</span><span class="sxs-lookup"><span data-stu-id="d7d2c-107">Where:</span></span>

-   <span data-ttu-id="d7d2c-108">dcl \_ 使用方式會識別如何使用註冊資料。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="d7d2c-109">這與沒有 D3DDECLUSAGE 前置詞的 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) 成員具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="d7d2c-110">使用方式 \_ 索引是介於0到15之間的選擇性整數索引。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="d7d2c-111">它會修改使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-111">It modifies the usage data.</span></span> <span data-ttu-id="d7d2c-112">索引符合頂點宣告中的使用方式索引。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="d7d2c-113">請參閱 [ (Direct3D 9) 的頂點 ](/windows/desktop/direct3d9/vertex-declaration)宣告。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="d7d2c-114">索引會附加至使用值 (\_ ) 不含空格的使用值。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="d7d2c-115">如果未提供，則會假設為0。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="d7d2c-116">v \# 是 [輸入](dx9-graphics-reference-asm-vs-registers-input.md)暫存器。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d2c-117">備註</span><span class="sxs-lookup"><span data-stu-id="d7d2c-117">Remarks</span></span>



| <span data-ttu-id="d7d2c-118">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="d7d2c-118">Vertex shader versions</span></span> | <span data-ttu-id="d7d2c-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="d7d2c-119">1\_1</span></span> | <span data-ttu-id="d7d2c-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7d2c-120">2\_0</span></span> | <span data-ttu-id="d7d2c-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d7d2c-121">2\_x</span></span> | <span data-ttu-id="d7d2c-122">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d7d2c-122">2\_sw</span></span> | <span data-ttu-id="d7d2c-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7d2c-123">3\_0</span></span> | <span data-ttu-id="d7d2c-124">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d7d2c-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d7d2c-125">dcl \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="d7d2c-125">dcl\_usage</span></span>             | <span data-ttu-id="d7d2c-126">x</span><span class="sxs-lookup"><span data-stu-id="d7d2c-126">x</span></span>    | <span data-ttu-id="d7d2c-127">x</span><span class="sxs-lookup"><span data-stu-id="d7d2c-127">x</span></span>    | <span data-ttu-id="d7d2c-128">x</span><span class="sxs-lookup"><span data-stu-id="d7d2c-128">x</span></span>    | <span data-ttu-id="d7d2c-129">x</span><span class="sxs-lookup"><span data-stu-id="d7d2c-129">x</span></span>     | <span data-ttu-id="d7d2c-130">x</span><span class="sxs-lookup"><span data-stu-id="d7d2c-130">x</span></span>    | <span data-ttu-id="d7d2c-131">x</span><span class="sxs-lookup"><span data-stu-id="d7d2c-131">x</span></span>     |



 

<span data-ttu-id="d7d2c-132">所有 \_ 的 dcl 使用方式指令都必須出現在第一個可執行指令之前。</span><span class="sxs-lookup"><span data-stu-id="d7d2c-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7d2c-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7d2c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7d2c-134">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="d7d2c-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 