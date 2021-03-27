---
title: 輸入暫存器
description: 輸入暫存器
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932358"
---
# <a name="input-register"></a><span data-ttu-id="5c80a-103">輸入暫存器</span><span class="sxs-lookup"><span data-stu-id="5c80a-103">Input Register</span></span>

<span data-ttu-id="5c80a-104">頂點著色器輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="5c80a-104">Vertex shader input register.</span></span>

<span data-ttu-id="5c80a-105">使用一或多個輸入頂點資料流程的每個頂點 (的資料) 會在執行頂點著色器之前載入至頂點輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="5c80a-105">Data from each vertex (using one or more input vertex streams) is loaded into the vertex input registers before the vertex shader is run.</span></span> <span data-ttu-id="5c80a-106">輸入暫存器由 16 4-元件浮點向量所組成，指定為 v0 到 v15。</span><span class="sxs-lookup"><span data-stu-id="5c80a-106">The input registers consist of 16 four-component floating-point vectors, designated as v0 through v15.</span></span> <span data-ttu-id="5c80a-107">這些暫存器是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5c80a-107">These registers are read-only.</span></span> <span data-ttu-id="5c80a-108">輸入暫存器會透過頂點宣告系結至頂點資料。</span><span class="sxs-lookup"><span data-stu-id="5c80a-108">An input register is bound to vertex data through a vertex declaration.</span></span>

<span data-ttu-id="5c80a-109">下列暫存器屬性會控制每個註冊的行為：</span><span class="sxs-lookup"><span data-stu-id="5c80a-109">The following register properties control how each register behaves:</span></span>



| <span data-ttu-id="5c80a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5c80a-110">Property</span></span>        | <span data-ttu-id="5c80a-111">描述</span><span class="sxs-lookup"><span data-stu-id="5c80a-111">Description</span></span>                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c80a-112">Name</span><span class="sxs-lookup"><span data-stu-id="5c80a-112">Name</span></span>            | <span data-ttu-id="5c80a-113">v \[ n \] -n 是選擇性的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="5c80a-113">v\[n\] - n is an optional register number.</span></span> <span data-ttu-id="5c80a-114">如果省略，則預設值為0。</span><span class="sxs-lookup"><span data-stu-id="5c80a-114">0 is the default value used, if it is omitted.</span></span>     |
| <span data-ttu-id="5c80a-115">Count</span><span class="sxs-lookup"><span data-stu-id="5c80a-115">Count</span></span>           | <span data-ttu-id="5c80a-116">最多16個暫存器，v0-v15。</span><span class="sxs-lookup"><span data-stu-id="5c80a-116">A maximum of 16 registers, v0 - v15.</span></span>                                                          |
| <span data-ttu-id="5c80a-117">I/o 許可權</span><span class="sxs-lookup"><span data-stu-id="5c80a-117">I/O permissions</span></span> | <span data-ttu-id="5c80a-118">唯讀。</span><span class="sxs-lookup"><span data-stu-id="5c80a-118">Read-only.</span></span> <span data-ttu-id="5c80a-119">此暫存器無法由 API 或在著色器中寫入。</span><span class="sxs-lookup"><span data-stu-id="5c80a-119">This register cannot be written by the API or within the shader.</span></span>                   |
| <span data-ttu-id="5c80a-120">讀取埠</span><span class="sxs-lookup"><span data-stu-id="5c80a-120">Read ports</span></span>      | <span data-ttu-id="5c80a-121">1. 這是在單一指令內可以讀取暫存器的次數。</span><span class="sxs-lookup"><span data-stu-id="5c80a-121">1. This is the number of times a register can be read within a single instruction.</span></span> <span data-ttu-id="5c80a-122">請參閱下文。</span><span class="sxs-lookup"><span data-stu-id="5c80a-122">See below.</span></span> |



 

<span data-ttu-id="5c80a-123">任何單一指令都只能存取一個頂點輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="5c80a-123">Any single instruction can access only one vertex input register.</span></span> <span data-ttu-id="5c80a-124">不過，指令中的每個來源都可以獨立地 swizzle，並在該向量被讀取時對其進行否定。</span><span class="sxs-lookup"><span data-stu-id="5c80a-124">However, each source in the instruction can independently swizzle and negate that vector as it is read.</span></span>

## <a name="example"></a><span data-ttu-id="5c80a-125">範例</span><span class="sxs-lookup"><span data-stu-id="5c80a-125">Example</span></span>

<span data-ttu-id="5c80a-126">以下範例使用頂點宣告來系結2D 頂點位置資料，以註冊 v0。</span><span class="sxs-lookup"><span data-stu-id="5c80a-126">Here is an example using a vertex declaration to bind 2D vertex position data to register v0.</span></span>

<span data-ttu-id="5c80a-127">頂點宣告屬於應用程式：</span><span class="sxs-lookup"><span data-stu-id="5c80a-127">The vertex declaration belongs in the application:</span></span>


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



<span data-ttu-id="5c80a-128">以下是對應的頂點著色器宣告：</span><span class="sxs-lookup"><span data-stu-id="5c80a-128">Here is the corresponding vertex shader declaration:</span></span>


```
dcl_position v0
```





| <span data-ttu-id="5c80a-129">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="5c80a-129">Vertex shader versions</span></span> | <span data-ttu-id="5c80a-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="5c80a-130">1\_1</span></span> | <span data-ttu-id="5c80a-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c80a-131">2\_0</span></span> | <span data-ttu-id="5c80a-132">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5c80a-132">2\_sw</span></span> | <span data-ttu-id="5c80a-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5c80a-133">2\_x</span></span> | <span data-ttu-id="5c80a-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c80a-134">3\_0</span></span> | <span data-ttu-id="5c80a-135">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5c80a-135">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="5c80a-136">位置註冊</span><span class="sxs-lookup"><span data-stu-id="5c80a-136">Position Register</span></span>      | <span data-ttu-id="5c80a-137">x</span><span class="sxs-lookup"><span data-stu-id="5c80a-137">x</span></span>    | <span data-ttu-id="5c80a-138">x</span><span class="sxs-lookup"><span data-stu-id="5c80a-138">x</span></span>    | <span data-ttu-id="5c80a-139">x</span><span class="sxs-lookup"><span data-stu-id="5c80a-139">x</span></span>     | <span data-ttu-id="5c80a-140">x</span><span class="sxs-lookup"><span data-stu-id="5c80a-140">x</span></span>    | <span data-ttu-id="5c80a-141">x</span><span class="sxs-lookup"><span data-stu-id="5c80a-141">x</span></span>    | <span data-ttu-id="5c80a-142">x</span><span class="sxs-lookup"><span data-stu-id="5c80a-142">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="5c80a-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c80a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c80a-144">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="5c80a-144">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




