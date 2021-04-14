---
title: 標籤-ps
description: 將下一個指令標示為具有標籤索引。 |標籤-ps
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992011"
---
# <a name="label---ps"></a><span data-ttu-id="6f6e9-104">標籤-ps</span><span class="sxs-lookup"><span data-stu-id="6f6e9-104">label - ps</span></span>

<span data-ttu-id="6f6e9-105">將下一個指令標示為具有標籤索引。</span><span class="sxs-lookup"><span data-stu-id="6f6e9-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6e9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f6e9-106">Syntax</span></span>



| <span data-ttu-id="6f6e9-107">標籤 l\#</span><span class="sxs-lookup"><span data-stu-id="6f6e9-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="6f6e9-108">其中會 \# 識別標籤號碼。</span><span class="sxs-lookup"><span data-stu-id="6f6e9-108">where \# identifies the label number.</span></span>

<span data-ttu-id="6f6e9-109">若是 ps \_ 2 \_ x，標籤編號必須介於0到15之間。</span><span class="sxs-lookup"><span data-stu-id="6f6e9-109">For ps\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="6f6e9-110">針對 ps \_ 2 \_ sw、ps \_ 3 \_ 0 和 ps \_ 3 \_ sw，標籤編號必須介於0到2047之間。</span><span class="sxs-lookup"><span data-stu-id="6f6e9-110">For ps\_2\_sw, ps\_3\_0, and ps\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f6e9-111">備註</span><span class="sxs-lookup"><span data-stu-id="6f6e9-111">Remarks</span></span>



| <span data-ttu-id="6f6e9-112">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="6f6e9-112">Pixel shader versions</span></span> | <span data-ttu-id="6f6e9-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="6f6e9-113">1\_1</span></span> | <span data-ttu-id="6f6e9-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="6f6e9-114">1\_2</span></span> | <span data-ttu-id="6f6e9-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6f6e9-115">1\_3</span></span> | <span data-ttu-id="6f6e9-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="6f6e9-116">1\_4</span></span> | <span data-ttu-id="6f6e9-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6f6e9-117">2\_0</span></span> | <span data-ttu-id="6f6e9-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6f6e9-118">2\_x</span></span> | <span data-ttu-id="6f6e9-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6f6e9-119">2\_sw</span></span> | <span data-ttu-id="6f6e9-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6f6e9-120">3\_0</span></span> | <span data-ttu-id="6f6e9-121">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6f6e9-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6f6e9-122">label</span><span class="sxs-lookup"><span data-stu-id="6f6e9-122">label</span></span>                 |      |      |      |      |      | <span data-ttu-id="6f6e9-123">x</span><span class="sxs-lookup"><span data-stu-id="6f6e9-123">x</span></span>    | <span data-ttu-id="6f6e9-124">x</span><span class="sxs-lookup"><span data-stu-id="6f6e9-124">x</span></span>     | <span data-ttu-id="6f6e9-125">x</span><span class="sxs-lookup"><span data-stu-id="6f6e9-125">x</span></span>    | <span data-ttu-id="6f6e9-126">x</span><span class="sxs-lookup"><span data-stu-id="6f6e9-126">x</span></span>     |



 

<span data-ttu-id="6f6e9-127">此指令會定義位於下一個著色器指令的標籤。</span><span class="sxs-lookup"><span data-stu-id="6f6e9-127">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="6f6e9-128">標籤指令只能直接存在於 [ret](ret---ps.md) 指令之後， (定義上一個副程式或主要程式) 的結尾。</span><span class="sxs-lookup"><span data-stu-id="6f6e9-128">The label instruction can only be present directly after a [ret](ret---ps.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f6e9-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="6f6e9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f6e9-130">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="6f6e9-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




