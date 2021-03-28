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
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990826"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="bce98-103">dcl \_ samplerType (sm3-vs asm) </span><span class="sxs-lookup"><span data-stu-id="bce98-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="bce98-104">宣告頂點著色器取樣器。</span><span class="sxs-lookup"><span data-stu-id="bce98-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce98-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bce98-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="bce98-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="bce98-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="bce98-107">其中：</span><span class="sxs-lookup"><span data-stu-id="bce98-107">where:</span></span>

-   <span data-ttu-id="bce98-108">\_samplerType 會定義取樣器資料類型。</span><span class="sxs-lookup"><span data-stu-id="bce98-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="bce98-109">這會決定取樣時，每個材質座標需要多少座標。</span><span class="sxs-lookup"><span data-stu-id="bce98-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="bce98-110">會定義下列紋理座標維度。</span><span class="sxs-lookup"><span data-stu-id="bce98-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="bce98-111">\_二 維和</span><span class="sxs-lookup"><span data-stu-id="bce98-111">\_2d</span></span>
    -   <span data-ttu-id="bce98-112">\_立方體</span><span class="sxs-lookup"><span data-stu-id="bce98-112">\_cube</span></span>
    -   <span data-ttu-id="bce98-113">\_體積</span><span class="sxs-lookup"><span data-stu-id="bce98-113">\_volume</span></span>
-   <span data-ttu-id="bce98-114">s \# 會識別一個取樣器，其中 s 是取樣器的縮寫，而 \# 是取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="bce98-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="bce98-115">[ (Direct3D 9 asm-vs) ](dx9-graphics-reference-asm-vs-registers-sampler.md)s 的取樣器是虛擬暫存器，因為您無法直接讀取或寫入它們。</span><span class="sxs-lookup"><span data-stu-id="bce98-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="bce98-116">備註</span><span class="sxs-lookup"><span data-stu-id="bce98-116">Remarks</span></span>



| <span data-ttu-id="bce98-117">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="bce98-117">Vertex shader versions</span></span> | <span data-ttu-id="bce98-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="bce98-118">1\_1</span></span> | <span data-ttu-id="bce98-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bce98-119">2\_0</span></span> | <span data-ttu-id="bce98-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bce98-120">2\_x</span></span> | <span data-ttu-id="bce98-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="bce98-121">2\_sw</span></span> | <span data-ttu-id="bce98-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bce98-122">3\_0</span></span> | <span data-ttu-id="bce98-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="bce98-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="bce98-124">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="bce98-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="bce98-125">x</span><span class="sxs-lookup"><span data-stu-id="bce98-125">x</span></span>    | <span data-ttu-id="bce98-126">x</span><span class="sxs-lookup"><span data-stu-id="bce98-126">x</span></span>     |



 

<span data-ttu-id="bce98-127">所有 \_ 的 dcl samplerType 指令都必須出現在第一個可執行指令之前。</span><span class="sxs-lookup"><span data-stu-id="bce98-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bce98-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="bce98-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce98-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="bce98-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




