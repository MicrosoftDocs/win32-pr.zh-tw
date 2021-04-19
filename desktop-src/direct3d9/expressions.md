---
description: 運算式是在等號右邊使用的數學或邏輯語句。 有許多類型的運算式。
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: " (Direct3D 9) 的運算式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991584"
---
# <a name="expressions-direct3d-9"></a><span data-ttu-id="753f8-104"> (Direct3D 9) 的運算式</span><span class="sxs-lookup"><span data-stu-id="753f8-104">Expressions (Direct3D 9)</span></span>

<span data-ttu-id="753f8-105">運算式是在等號右邊使用的數學或邏輯語句。</span><span class="sxs-lookup"><span data-stu-id="753f8-105">Expressions are mathematical or logical statements that are used on the right hand side of an equals sign.</span></span> <span data-ttu-id="753f8-106">有許多類型的運算式。</span><span class="sxs-lookup"><span data-stu-id="753f8-106">There are many types of expressions.</span></span>

## <a name="expressions"></a><span data-ttu-id="753f8-107">運算式</span><span class="sxs-lookup"><span data-stu-id="753f8-107">Expressions</span></span>

1.  <span data-ttu-id="753f8-108">變數參考</span><span class="sxs-lookup"><span data-stu-id="753f8-108">Variable Reference</span></span>
    ```
    ( variable ) or<variable >
    ```

    

2.  <span data-ttu-id="753f8-109">數值純量</span><span class="sxs-lookup"><span data-stu-id="753f8-109">Numeric Scalar</span></span>
    ```
    scalar 
    ```

    

3.  <span data-ttu-id="753f8-110">數值運算式</span><span class="sxs-lookup"><span data-stu-id="753f8-110">Numeric Expression</span></span>

    ```
    ( numeric expression )
    ```

    

    <span data-ttu-id="753f8-111">此處支援所有標準數值 HLL 運算式。</span><span class="sxs-lookup"><span data-stu-id="753f8-111">All standard numeric HLL expressions are supported here.</span></span>

4.  <span data-ttu-id="753f8-112">建構函式</span><span class="sxs-lookup"><span data-stu-id="753f8-112">Constructor</span></span>
    ```
    type ( constructor arguments )
    ```

    

5.  <span data-ttu-id="753f8-113">初始化運算式清單</span><span class="sxs-lookup"><span data-stu-id="753f8-113">List of Initializers</span></span>

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    <span data-ttu-id="753f8-114">純量值必須是常值純量值。</span><span class="sxs-lookup"><span data-stu-id="753f8-114">The scalars must be literal scalar values.</span></span>

    <span data-ttu-id="753f8-115">初始化運算式的數目必須與等號左邊的變數 (狀態) 相容。</span><span class="sxs-lookup"><span data-stu-id="753f8-115">The number of initializers must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

6.  <span data-ttu-id="753f8-116">OR 運算式</span><span class="sxs-lookup"><span data-stu-id="753f8-116">OR Expression</span></span>

    ```
    token [ | token ... ]
    ```

    

    <span data-ttu-id="753f8-117">標記必須與等號左邊的變數 (狀態) 相容。</span><span class="sxs-lookup"><span data-stu-id="753f8-117">The tokens must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

    <span data-ttu-id="753f8-118">標記不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="753f8-118">The tokens are not case sensitive.</span></span>

7.  <span data-ttu-id="753f8-119">NULL</span><span class="sxs-lookup"><span data-stu-id="753f8-119">NULL</span></span>

    ```
    NULL
    ```

    

    <span data-ttu-id="753f8-120">Null 只能指派給著色器、取樣器或紋理物件。</span><span class="sxs-lookup"><span data-stu-id="753f8-120">NULL can only be assigned to a shader, sampler, or a texture object.</span></span>

8.  <span data-ttu-id="753f8-121">元件區塊</span><span class="sxs-lookup"><span data-stu-id="753f8-121">Assembly Block</span></span>

    ```
    asm { code }
    ```

    

    <span data-ttu-id="753f8-122">必須將 PS 元件區塊指派給無效狀態。</span><span class="sxs-lookup"><span data-stu-id="753f8-122">PS Assembly Blocks must be assigned to the PIXELSHADER state.</span></span>

    <span data-ttu-id="753f8-123">必須將 VS 元件區塊指派給 VERTEXSHADER 狀態。</span><span class="sxs-lookup"><span data-stu-id="753f8-123">VS Assembly Blocks must be assigned to the VERTEXSHADER state.</span></span>

9.  <span data-ttu-id="753f8-124">取樣器狀態欄塊</span><span class="sxs-lookup"><span data-stu-id="753f8-124">Sampler State Block</span></span>

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    <span data-ttu-id="753f8-125">取樣器狀態欄塊是未索引的取樣器階段狀態或材質指派的順序。</span><span class="sxs-lookup"><span data-stu-id="753f8-125">Sampler state blocks are sequences of un-indexed sampler stage state or texture assignments.</span></span>

    <span data-ttu-id="753f8-126">取樣器狀態欄塊必須指派給取樣器效果狀態。</span><span class="sxs-lookup"><span data-stu-id="753f8-126">Sampler state blocks must be assigned to the SAMPLER effect state.</span></span>

10. <span data-ttu-id="753f8-127">效果狀態狀態欄塊</span><span class="sxs-lookup"><span data-stu-id="753f8-127">Effect State State Block</span></span>

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    <span data-ttu-id="753f8-128">狀態欄塊是一般狀態的序列。</span><span class="sxs-lookup"><span data-stu-id="753f8-128">State blocks are sequences of general state.</span></span> <span data-ttu-id="753f8-129">狀態欄塊可以進行嵌套，但不能包含迴圈參考。</span><span class="sxs-lookup"><span data-stu-id="753f8-129">State blocks can be nested, but cannot contain circular references.</span></span>

    <span data-ttu-id="753f8-130">必須將狀態欄塊指派給 STATEBLOCK 效果狀態。</span><span class="sxs-lookup"><span data-stu-id="753f8-130">State blocks must be assigned to the STATEBLOCK effect state.</span></span>

11. <span data-ttu-id="753f8-131">HLSL 編譯</span><span class="sxs-lookup"><span data-stu-id="753f8-131">HLSL Compile</span></span>

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    <span data-ttu-id="753f8-132">頂點著色器與 \_ m \_ n 目標表示 D3DVS \_ 版本 (m，n) 頂點著色器版本。</span><span class="sxs-lookup"><span data-stu-id="753f8-132">The vertex shader vs\_m\_n target indicates D3DVS\_VERSION(m, n) vertex shader version.</span></span> <span data-ttu-id="753f8-133">圖元著色器 ps \_ m \_ n 目標表示 D3DPS \_ 版 (m，n) 圖元著色器版本。</span><span class="sxs-lookup"><span data-stu-id="753f8-133">The pixel shader ps\_m\_n target indicates D3DPS\_VERSION(m, n) pixel shader version.</span></span>

    <span data-ttu-id="753f8-134">頂點著色器高階語言編譯運算式只能指派給 VERTEXSHADER 效果狀態。</span><span class="sxs-lookup"><span data-stu-id="753f8-134">Vertex shader high-level language compile expressions can only be assigned to the VERTEXSHADER effect state.</span></span> <span data-ttu-id="753f8-135">圖元著色器高階語言編譯運算式只能指派給無效效果狀態。</span><span class="sxs-lookup"><span data-stu-id="753f8-135">Pixel shader high-level language compile expressions can only be assigned to the PIXELSHADER effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="753f8-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="753f8-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="753f8-137">效果格式</span><span class="sxs-lookup"><span data-stu-id="753f8-137">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



