---
title: 標籤-vs
description: 將下一個指令標示為具有標籤索引。 |標籤-vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992087"
---
# <a name="label---vs"></a><span data-ttu-id="f2bf2-104">標籤-vs</span><span class="sxs-lookup"><span data-stu-id="f2bf2-104">label - vs</span></span>

<span data-ttu-id="f2bf2-105">將下一個指令標示為具有標籤索引。</span><span class="sxs-lookup"><span data-stu-id="f2bf2-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2bf2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2bf2-106">Syntax</span></span>



| <span data-ttu-id="f2bf2-107">標籤 l\#</span><span class="sxs-lookup"><span data-stu-id="f2bf2-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="f2bf2-108">其中會 \# 識別標籤號碼。</span><span class="sxs-lookup"><span data-stu-id="f2bf2-108">where \# identifies the label number.</span></span>

<span data-ttu-id="f2bf2-109">針對 vs \_ 2 \_ 0 和 vs \_ 2 \_ x，標籤編號必須介於0到15之間。</span><span class="sxs-lookup"><span data-stu-id="f2bf2-109">For vs\_2\_0, and vs\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="f2bf2-110">針對 vs \_ 2 \_ sw、vs \_ 3 \_ 0 和 vs \_ 3 \_ sw，標籤編號必須介於0到2047之間。</span><span class="sxs-lookup"><span data-stu-id="f2bf2-110">For vs\_2\_sw, vs\_3\_0 and vs\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2bf2-111">備註</span><span class="sxs-lookup"><span data-stu-id="f2bf2-111">Remarks</span></span>



| <span data-ttu-id="f2bf2-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="f2bf2-112">Vertex shader versions</span></span> | <span data-ttu-id="f2bf2-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="f2bf2-113">1\_1</span></span> | <span data-ttu-id="f2bf2-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f2bf2-114">2\_0</span></span> | <span data-ttu-id="f2bf2-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f2bf2-115">2\_x</span></span> | <span data-ttu-id="f2bf2-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="f2bf2-116">2\_sw</span></span> | <span data-ttu-id="f2bf2-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f2bf2-117">3\_0</span></span> | <span data-ttu-id="f2bf2-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="f2bf2-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f2bf2-119">label</span><span class="sxs-lookup"><span data-stu-id="f2bf2-119">label</span></span>                  |      | <span data-ttu-id="f2bf2-120">x</span><span class="sxs-lookup"><span data-stu-id="f2bf2-120">x</span></span>    | <span data-ttu-id="f2bf2-121">x</span><span class="sxs-lookup"><span data-stu-id="f2bf2-121">x</span></span>    | <span data-ttu-id="f2bf2-122">x</span><span class="sxs-lookup"><span data-stu-id="f2bf2-122">x</span></span>     | <span data-ttu-id="f2bf2-123">x</span><span class="sxs-lookup"><span data-stu-id="f2bf2-123">x</span></span>    | <span data-ttu-id="f2bf2-124">x</span><span class="sxs-lookup"><span data-stu-id="f2bf2-124">x</span></span>     |



 

<span data-ttu-id="f2bf2-125">此指令會定義位於下一個著色器指令的標籤。</span><span class="sxs-lookup"><span data-stu-id="f2bf2-125">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="f2bf2-126">標籤指令只能直接存在於 [ret](ret---vs.md) 指令之後， (定義上一個副程式或主要程式) 的結尾。</span><span class="sxs-lookup"><span data-stu-id="f2bf2-126">The label instruction can only be present directly after a [ret](ret---vs.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2bf2-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2bf2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2bf2-128">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="f2bf2-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




