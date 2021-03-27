---
title: 位置註冊
description: 此頂點著色器輸出暫存器包含每個頂點的位置資料。
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673591"
---
# <a name="position-register"></a><span data-ttu-id="92381-103">位置註冊</span><span class="sxs-lookup"><span data-stu-id="92381-103">Position Register</span></span>

<span data-ttu-id="92381-104">此頂點著色器輸出暫存器包含每個頂點的位置資料。</span><span class="sxs-lookup"><span data-stu-id="92381-104">This vertex shader output register contains per-vertex position data.</span></span>



| <span data-ttu-id="92381-105">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="92381-105">Vertex shader versions</span></span> | <span data-ttu-id="92381-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="92381-106">1\_1</span></span> | <span data-ttu-id="92381-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="92381-107">2\_0</span></span> | <span data-ttu-id="92381-108">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="92381-108">2\_sw</span></span> | <span data-ttu-id="92381-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="92381-109">2\_x</span></span> | <span data-ttu-id="92381-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="92381-110">3\_0</span></span> | <span data-ttu-id="92381-111">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="92381-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="92381-112">位置註冊</span><span class="sxs-lookup"><span data-stu-id="92381-112">Position Register</span></span>      | <span data-ttu-id="92381-113">x</span><span class="sxs-lookup"><span data-stu-id="92381-113">x</span></span>    | <span data-ttu-id="92381-114">x</span><span class="sxs-lookup"><span data-stu-id="92381-114">x</span></span>    | <span data-ttu-id="92381-115">x</span><span class="sxs-lookup"><span data-stu-id="92381-115">x</span></span>     | <span data-ttu-id="92381-116">x</span><span class="sxs-lookup"><span data-stu-id="92381-116">x</span></span>    | <span data-ttu-id="92381-117">x</span><span class="sxs-lookup"><span data-stu-id="92381-117">x</span></span>    | <span data-ttu-id="92381-118">x</span><span class="sxs-lookup"><span data-stu-id="92381-118">x</span></span>     |



 

<span data-ttu-id="92381-119">暫存器包含的屬性會決定每個註冊的行為。</span><span class="sxs-lookup"><span data-stu-id="92381-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="92381-120">屬性</span><span class="sxs-lookup"><span data-stu-id="92381-120">Property</span></span>        | <span data-ttu-id="92381-121">描述</span><span class="sxs-lookup"><span data-stu-id="92381-121">Description</span></span> |
|-----------------|-------------|
| <span data-ttu-id="92381-122">Name</span><span class="sxs-lookup"><span data-stu-id="92381-122">Name</span></span>            | <span data-ttu-id="92381-123">oPos</span><span class="sxs-lookup"><span data-stu-id="92381-123">oPos</span></span>        |
| <span data-ttu-id="92381-124">Count</span><span class="sxs-lookup"><span data-stu-id="92381-124">Count</span></span>           | <span data-ttu-id="92381-125">1個向量</span><span class="sxs-lookup"><span data-stu-id="92381-125">1 vector</span></span>    |
| <span data-ttu-id="92381-126">I/o 許可權</span><span class="sxs-lookup"><span data-stu-id="92381-126">I/O permissions</span></span> | <span data-ttu-id="92381-127">唯寫。</span><span class="sxs-lookup"><span data-stu-id="92381-127">Write-only.</span></span> |



 

<span data-ttu-id="92381-128">值是同質剪切空間中的位置。</span><span class="sxs-lookup"><span data-stu-id="92381-128">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="92381-129">這個值必須由頂點著色器撰寫。</span><span class="sxs-lookup"><span data-stu-id="92381-129">This value must be written by the vertex shader.</span></span>

<span data-ttu-id="92381-130">範例</span><span class="sxs-lookup"><span data-stu-id="92381-130">Example</span></span>


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a><span data-ttu-id="92381-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="92381-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92381-132">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="92381-132">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




