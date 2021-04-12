---
description: 您可以使用效果來儲存資訊，或使用一組狀態來呈現。
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: 轉譯 (Direct3D 10) 的效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187652"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="b41f2-103">轉譯 (Direct3D 10) 的效果</span><span class="sxs-lookup"><span data-stu-id="b41f2-103">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="b41f2-104">您可以使用效果來儲存資訊，或使用一組狀態來呈現。</span><span class="sxs-lookup"><span data-stu-id="b41f2-104">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="b41f2-105">每項技術都會指定頂點著色器、幾何著色器、圖元著色器、著色器狀態、取樣器和材質狀態，以及其他管線狀態。</span><span class="sxs-lookup"><span data-stu-id="b41f2-105">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="b41f2-106">因此，當您將狀態組織成某個效果之後，您可以藉由建立和轉譯效果，來封裝該狀態所產生的轉譯效果。</span><span class="sxs-lookup"><span data-stu-id="b41f2-106">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="b41f2-107">有幾個步驟可準備轉譯的效果。</span><span class="sxs-lookup"><span data-stu-id="b41f2-107">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="b41f2-108">第一個是編譯，它會根據 HLSL 語言語法和效果架構規則來檢查 HLSL，例如程式碼。</span><span class="sxs-lookup"><span data-stu-id="b41f2-108">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="b41f2-109">您可以使用 API 呼叫來編譯應用程式的效果，也可以使用效果編譯器公用程式來離線編譯效果。</span><span class="sxs-lookup"><span data-stu-id="b41f2-109">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="b41f2-110">成功編譯效果之後，請呼叫不同 (但非常類似的) 組 Api 來建立它。</span><span class="sxs-lookup"><span data-stu-id="b41f2-110">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="b41f2-111">建立效果之後，有兩個剩餘的步驟可以使用它。</span><span class="sxs-lookup"><span data-stu-id="b41f2-111">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="b41f2-112">首先，您必須使用數個設定狀態的方法，將效果狀態值初始化 (的效果變數值) 。</span><span class="sxs-lookup"><span data-stu-id="b41f2-112">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="b41f2-113">針對某些變數，您可以在建立效果時完成這項操作;每次您的應用程式呼叫轉譯迴圈時，都必須更新其他專案。</span><span class="sxs-lookup"><span data-stu-id="b41f2-113">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="b41f2-114">設定效果變數後，您可以指示執行時間藉由套用技術來呈現影響。</span><span class="sxs-lookup"><span data-stu-id="b41f2-114">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="b41f2-115">以下將詳細討論這些主題。</span><span class="sxs-lookup"><span data-stu-id="b41f2-115">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="b41f2-116">編譯效果 (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b41f2-116">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="b41f2-117"> (Direct3D 10 建立效果) </span><span class="sxs-lookup"><span data-stu-id="b41f2-117">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="b41f2-118">設定效果狀態 (Direct3D 10) </span><span class="sxs-lookup"><span data-stu-id="b41f2-118">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="b41f2-119">將技術套用 (Direct3D 10) </span><span class="sxs-lookup"><span data-stu-id="b41f2-119">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="b41f2-120">當然，使用效果會有 [效能考慮](d3d10-graphics-programming-guide-effects-performance.md) 。</span><span class="sxs-lookup"><span data-stu-id="b41f2-120">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="b41f2-121">如果您不是使用效果，則這些考慮大致相同。</span><span class="sxs-lookup"><span data-stu-id="b41f2-121">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="b41f2-122">例如，將狀態變更的數量降到最低，或組織需要依頻率更新的變數。</span><span class="sxs-lookup"><span data-stu-id="b41f2-122">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="b41f2-123">這些策略可用來將需要從 CPU 傳送到 GPU 的資料量降到最低，因此可將可能的同步處理問題降至最低。</span><span class="sxs-lookup"><span data-stu-id="b41f2-123">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b41f2-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="b41f2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b41f2-125"> (Direct3D 10) 的效果 </span><span class="sxs-lookup"><span data-stu-id="b41f2-125">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



