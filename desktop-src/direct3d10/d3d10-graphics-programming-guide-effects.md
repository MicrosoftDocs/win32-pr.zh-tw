---
description: DirectX 效果是管線狀態的集合，由以 HLSL 撰寫的運算式所設定，以及某些特定于效果架構的語法。
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: " (Direct3D 10) 的效果"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e08d0c79a6f7f52982a74d5127da70d7b82f84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970541"
---
# <a name="effects-direct3d-10"></a><span data-ttu-id="527b8-103"> (Direct3D 10) 的效果</span><span class="sxs-lookup"><span data-stu-id="527b8-103">Effects (Direct3D 10)</span></span>

<span data-ttu-id="527b8-104">DirectX 效果是管線狀態的集合，由以 [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) 撰寫的運算式所設定，以及某些特定于效果架構的語法。</span><span class="sxs-lookup"><span data-stu-id="527b8-104">A DirectX effect is a collection of pipeline state, set by expressions written in [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) and some syntax that is specific to the effect framework.</span></span> <span data-ttu-id="527b8-105">編譯效果之後，請使用效果架構 Api 來呈現。</span><span class="sxs-lookup"><span data-stu-id="527b8-105">After compiling an effect, use the effect framework APIs to render.</span></span> <span data-ttu-id="527b8-106">效果功能的範圍可以像是頂點著色器一樣簡單，也就是轉換幾何和圖元著色器以輸出純色、轉換成需要多個行程的轉譯技術、使用圖形管線的每個階段，以及操作著色器狀態以及未與可程式化著色器相關聯的管線狀態。</span><span class="sxs-lookup"><span data-stu-id="527b8-106">Effect functionality can range from something as simple as a vertex shader that transforms geometry and a pixel shader that outputs a solid color, to a rendering technique that requires multiple passes, uses every stage of the graphics pipeline, and manipulates shader state as well as the pipeline state not associated with the programmable shaders.</span></span>

<span data-ttu-id="527b8-107">第一個步驟是將您想要控制的狀態組織成一個效果。</span><span class="sxs-lookup"><span data-stu-id="527b8-107">The first step is to organize the state you want to control in an effect.</span></span> <span data-ttu-id="527b8-108">這包括著色器狀態 (頂點、幾何和圖元著色器) 、著色器所使用的材質和取樣器狀態，以及其他無法程式化的管線狀態。</span><span class="sxs-lookup"><span data-stu-id="527b8-108">This includes shader state (vertex, geometry and pixel shaders), texture and sampler state used by the shaders, and other non-programmable pipeline state.</span></span> <span data-ttu-id="527b8-109">您可以在記憶體中以文字字串的形式建立效果，但一般來說，大小夠大，因為在效果檔案中儲存效果的狀態， (一個以 fx 副檔名) 結尾的文字檔。</span><span class="sxs-lookup"><span data-stu-id="527b8-109">You can create an effect in memory as a text string, but typically, the size gets large enough that it is handy to store effect state in an effect file (a text file that ends in a .fx extension).</span></span> <span data-ttu-id="527b8-110">若要使用效果，您必須將它編譯 (以檢查 HLSL 語法以及效果架構語法) 、透過 API 呼叫初始化效果狀態，以及修改轉譯迴圈來呼叫轉譯 Api。</span><span class="sxs-lookup"><span data-stu-id="527b8-110">To use an effect, you must compile it (to check HLSL syntax as well as effect framework syntax), initialize effect state through API calls, and modify your render loop to call the rendering APIs.</span></span>

-   [<span data-ttu-id="527b8-111">組織效果中的狀態</span><span class="sxs-lookup"><span data-stu-id="527b8-111">Organizing State in an Effect</span></span>](d3d10-graphics-programming-guide-effects-organize.md)
-   [<span data-ttu-id="527b8-112">效果系統介面</span><span class="sxs-lookup"><span data-stu-id="527b8-112">Effect System Interfaces</span></span>](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [<span data-ttu-id="527b8-113">專用介面</span><span class="sxs-lookup"><span data-stu-id="527b8-113">Specializing Interfaces</span></span>](d3d10-graphics-reference-effect-specializing.md)
-   [<span data-ttu-id="527b8-114">呈現效果</span><span class="sxs-lookup"><span data-stu-id="527b8-114">Rendering an Effect</span></span>](d3d10-graphics-programming-guide-effects-render.md)

<span data-ttu-id="527b8-115">效果會將特定效果所需的所有轉譯狀態封裝到稱為技術的單一轉譯函數中。</span><span class="sxs-lookup"><span data-stu-id="527b8-115">An effect encapsulates all of the render state required by a particular effect into a single rendering function called a technique.</span></span> <span data-ttu-id="527b8-116">Pass 是技術的子集合，其中包含呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="527b8-116">A pass is a sub-set of a technique, that contains render state.</span></span> <span data-ttu-id="527b8-117">若要執行多重傳遞轉譯效果，請在技術內執行一或多個階段。</span><span class="sxs-lookup"><span data-stu-id="527b8-117">To implement a multiple pass rendering effect, implement one or more passes within a technique.</span></span> <span data-ttu-id="527b8-118">例如，假設您想要使用一組深度/樣板緩衝區來轉譯某些幾何，然後在其上方繪製一些 sprite。</span><span class="sxs-lookup"><span data-stu-id="527b8-118">For example, say you wanted to render some geometry with one set of depth/stencil buffers, and then draw some sprites on top of that.</span></span> <span data-ttu-id="527b8-119">您可以在第一個階段中執行幾何轉譯，並在第二個階段中執行 sprite 繪製。</span><span class="sxs-lookup"><span data-stu-id="527b8-119">You could implement the geometry rendering in the first pass, and the sprite drawing in the second pass.</span></span> <span data-ttu-id="527b8-120">若要轉譯效果，您只需在轉譯迴圈中轉譯這兩個階段。</span><span class="sxs-lookup"><span data-stu-id="527b8-120">To render the effect, you simply render both passes in your render loop.</span></span> <span data-ttu-id="527b8-121">您可以在效果中執行任何數目的技巧。</span><span class="sxs-lookup"><span data-stu-id="527b8-121">You can implement any number of techniques in an effect.</span></span> <span data-ttu-id="527b8-122">當然，技術的數目愈大，結果的編譯時間就愈大。</span><span class="sxs-lookup"><span data-stu-id="527b8-122">Of course, the greater the number of techniques, the greater the compile time for the effect.</span></span> <span data-ttu-id="527b8-123">利用這項功能的其中一種方法，就是使用專為在不同硬體上執行而設計的技術來建立效果。</span><span class="sxs-lookup"><span data-stu-id="527b8-123">One way to exploit this functionality is to create effects with techniques that are designed to run on different hardware.</span></span> <span data-ttu-id="527b8-124">這可讓應用程式根據偵測到的硬體功能，適當地將效能降級。</span><span class="sxs-lookup"><span data-stu-id="527b8-124">This allows an application to gracefully downgrade performance based on the hardware capabilities detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="527b8-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="527b8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="527b8-126">Direct3D 10 程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="527b8-126">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
