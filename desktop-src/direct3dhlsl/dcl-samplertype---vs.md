---
title: 'dcl_samplerType (sm3-vs asm) '
description: 宣告頂點著色器取樣器。
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129866"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="97942-103">dcl \_ samplerType (sm3-vs asm) </span><span class="sxs-lookup"><span data-stu-id="97942-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="97942-104">宣告頂點著色器取樣器。</span><span class="sxs-lookup"><span data-stu-id="97942-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="97942-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97942-105">Syntax</span></span>

<span data-ttu-id="97942-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="97942-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="97942-107">其中：</span><span class="sxs-lookup"><span data-stu-id="97942-107">where:</span></span>

-   <span data-ttu-id="97942-108">\_samplerType 會定義取樣器資料類型。</span><span class="sxs-lookup"><span data-stu-id="97942-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="97942-109">這會決定取樣時，每個材質座標需要多少座標。</span><span class="sxs-lookup"><span data-stu-id="97942-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="97942-110">會定義下列紋理座標維度。</span><span class="sxs-lookup"><span data-stu-id="97942-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="97942-111">\_二 維和</span><span class="sxs-lookup"><span data-stu-id="97942-111">\_2d</span></span>
    -   <span data-ttu-id="97942-112">\_立方體</span><span class="sxs-lookup"><span data-stu-id="97942-112">\_cube</span></span>
    -   <span data-ttu-id="97942-113">\_體積</span><span class="sxs-lookup"><span data-stu-id="97942-113">\_volume</span></span>
-   <span data-ttu-id="97942-114">s \# 會識別一個取樣器，其中 s 是取樣器的縮寫，而 \# 是取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="97942-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="97942-115">[ (Direct3D 9 asm-vs) ](dx9-graphics-reference-asm-vs-registers-sampler.md)s 的取樣器是虛擬暫存器，因為您無法直接讀取或寫入它們。</span><span class="sxs-lookup"><span data-stu-id="97942-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="97942-116">備註</span><span class="sxs-lookup"><span data-stu-id="97942-116">Remarks</span></span>



| <span data-ttu-id="97942-117">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="97942-117">Vertex shader versions</span></span> | <span data-ttu-id="97942-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="97942-118">1\_1</span></span> | <span data-ttu-id="97942-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97942-119">2\_0</span></span> | <span data-ttu-id="97942-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="97942-120">2\_x</span></span> | <span data-ttu-id="97942-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="97942-121">2\_sw</span></span> | <span data-ttu-id="97942-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97942-122">3\_0</span></span> | <span data-ttu-id="97942-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="97942-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="97942-124">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="97942-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="97942-125">x</span><span class="sxs-lookup"><span data-stu-id="97942-125">x</span></span>    | <span data-ttu-id="97942-126">x</span><span class="sxs-lookup"><span data-stu-id="97942-126">x</span></span>     |



 

<span data-ttu-id="97942-127">所有 \_ 的 dcl samplerType 指令都必須出現在第一個可執行指令之前。</span><span class="sxs-lookup"><span data-stu-id="97942-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97942-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="97942-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97942-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="97942-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




