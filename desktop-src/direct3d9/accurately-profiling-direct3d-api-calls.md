---
description: 當您擁有可運作的 Microsoft Direct3D 應用程式，並想要改善其效能之後，通常會使用現成的程式碼剖析工具或某些自訂度量技術來測量執行一或多個應用程式開發介面 (API) 呼叫所需的時間。 如果您已完成這項作業，但正在取得不同于下一個轉譯順序的計時結果，或您正在進行假設而不是實際的實驗結果，下列資訊可能有助於您瞭解原因。
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: 正確分析 Direct3D API 呼叫 (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdb6d60fcc1b3ace4112dbf7028d91e2c9c8b345
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689047"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a><span data-ttu-id="0153b-104">正確分析 Direct3D API 呼叫 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0153b-104">Accurately Profiling Direct3D API Calls (Direct3D 9)</span></span>

-   [<span data-ttu-id="0153b-105">很難正確分析 Direct3D</span><span class="sxs-lookup"><span data-stu-id="0153b-105">Accurately Profiling Direct3D Is Difficult</span></span>](#accurately-profiling-direct3d-is-difficult)
-   [<span data-ttu-id="0153b-106">如何精確地分析 Direct3D 轉譯順序</span><span class="sxs-lookup"><span data-stu-id="0153b-106">How to Accurately Profile a Direct3D Render Sequence</span></span>](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [<span data-ttu-id="0153b-107">分析 Direct3D 狀態變更</span><span class="sxs-lookup"><span data-stu-id="0153b-107">Profiling Direct3D State Changes</span></span>](#profiling-direct3d-state-changes)
-   [<span data-ttu-id="0153b-108">總結</span><span class="sxs-lookup"><span data-stu-id="0153b-108">Summary</span></span>](#summary)
-   [<span data-ttu-id="0153b-109">附錄</span><span class="sxs-lookup"><span data-stu-id="0153b-109">Appendix</span></span>](#appendix)

<span data-ttu-id="0153b-110">當您擁有可運作的 Microsoft Direct3D 應用程式，並想要改善其效能之後，通常會使用現成的程式碼剖析工具或某些自訂度量技術來測量執行一或多個應用程式開發介面 (API) 呼叫所需的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-110">Once you have a functional Microsoft Direct3D application and you want to improve its performance, you generally use an off-the-shelf profiling tool or some custom measurement technique to measure the time it takes to execute one or more application programming interface (API) calls.</span></span> <span data-ttu-id="0153b-111">如果您已完成這項作業，但正在取得不同于下一個轉譯順序的計時結果，或您正在進行假設而不是實際的實驗結果，下列資訊可能有助於您瞭解原因。</span><span class="sxs-lookup"><span data-stu-id="0153b-111">If you have done this but are getting timing results that vary from one render sequence to the next, or you are making hypotheses that do not hold up to actual experiment results, the following information may help you to understand why.</span></span>

<span data-ttu-id="0153b-112">此處提供的資訊是根據您對下列各項的瞭解和經驗所做的假設：</span><span class="sxs-lookup"><span data-stu-id="0153b-112">The information provided here is based upon the assumption that you have knowledge of and experience with the following:</span></span>

-   <span data-ttu-id="0153b-113">C/c + + 程式設計</span><span class="sxs-lookup"><span data-stu-id="0153b-113">C/C++ programming</span></span>
-   <span data-ttu-id="0153b-114">Direct3D API 程式設計</span><span class="sxs-lookup"><span data-stu-id="0153b-114">Direct3D API programming</span></span>
-   <span data-ttu-id="0153b-115">測量 API 時間</span><span class="sxs-lookup"><span data-stu-id="0153b-115">Measuring API timing</span></span>
-   <span data-ttu-id="0153b-116">視訊卡及其軟體驅動程式</span><span class="sxs-lookup"><span data-stu-id="0153b-116">The video card and its software driver</span></span>
-   <span data-ttu-id="0153b-117">先前分析體驗可能的無法解釋結果</span><span class="sxs-lookup"><span data-stu-id="0153b-117">Possible unexplainable results from previous profiling experience</span></span>

## <a name="accurately-profiling-direct3d-is-difficult"></a><span data-ttu-id="0153b-118">很難正確分析 Direct3D</span><span class="sxs-lookup"><span data-stu-id="0153b-118">Accurately Profiling Direct3D Is Difficult</span></span>

<span data-ttu-id="0153b-119">分析工具會報告在每個 API 呼叫中花費的時間量。</span><span class="sxs-lookup"><span data-stu-id="0153b-119">A profiler reports on the amount of time spent in each API call.</span></span> <span data-ttu-id="0153b-120">這樣做的目的是為了改善效能，方法是尋找並微調作用點。</span><span class="sxs-lookup"><span data-stu-id="0153b-120">This is done to improve performance by finding and tuning away hot spots.</span></span> <span data-ttu-id="0153b-121">有不同類型的分析工具和分析技術。</span><span class="sxs-lookup"><span data-stu-id="0153b-121">There are different kinds of profilers and profiling techniques.</span></span>

-   <span data-ttu-id="0153b-122">取樣分析工具處於閒置狀態，喚醒到取樣 (的特定間隔，或是記錄正在執行的函式) 。</span><span class="sxs-lookup"><span data-stu-id="0153b-122">A sampling profiler sits idle much of the time, awakening at specific intervals to sample (or to record) the functions being executed.</span></span> <span data-ttu-id="0153b-123">它會傳回每次呼叫所花費的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="0153b-123">It returns the percentage of time spent in each call.</span></span> <span data-ttu-id="0153b-124">一般情況下，取樣分析工具並不會對應用程式造成極大的衝擊，對應用程式的額外負荷造成最大的影響。</span><span class="sxs-lookup"><span data-stu-id="0153b-124">Generally, a sampling profiler is not very invasive to the application and has minimal impact on the overhead for the application.</span></span>
-   <span data-ttu-id="0153b-125">檢測 profiler 會測量呼叫傳回的實際時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-125">An instrumenting profiler measures the actual time it takes for a call to return.</span></span> <span data-ttu-id="0153b-126">它需要將開始和停止分隔符號編譯成應用程式。</span><span class="sxs-lookup"><span data-stu-id="0153b-126">It requires compiling start and stop delimiters into an application.</span></span> <span data-ttu-id="0153b-127">檢測分析工具相較于取樣分析工具，與應用程式的侵入性更高。</span><span class="sxs-lookup"><span data-stu-id="0153b-127">An instrumenting profiler is comparatively more invasive to an application than a sampling profiler.</span></span>
-   <span data-ttu-id="0153b-128">您也可以搭配高效能計時器使用自訂程式碼剖析技術。</span><span class="sxs-lookup"><span data-stu-id="0153b-128">It is also possible to use a custom profiling technique with a high-performance timer.</span></span> <span data-ttu-id="0153b-129">這會產生與檢測分析工具很類似的結果。</span><span class="sxs-lookup"><span data-stu-id="0153b-129">This produces results very much like an instrumenting profiler.</span></span>

<span data-ttu-id="0153b-130">使用的程式碼剖析工具或程式碼剖析技術，只是產生精確度量的挑戰的一部分。</span><span class="sxs-lookup"><span data-stu-id="0153b-130">The type of profiler or profiling technique used is only part of the challenge of generating accurate measurements.</span></span>

<span data-ttu-id="0153b-131">分析提供可協助您預算效能的解答。</span><span class="sxs-lookup"><span data-stu-id="0153b-131">Profiling gives you answers that help you budget performance.</span></span> <span data-ttu-id="0153b-132">比方說，假設您知道 API 呼叫的平均1000頻率迴圈要執行。</span><span class="sxs-lookup"><span data-stu-id="0153b-132">For instance, suppose you know that an API call averages one thousand clock cycles to execute.</span></span> <span data-ttu-id="0153b-133">您可以判斷提示有關效能的一些結論，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0153b-133">You can assert some conclusions about performance such as the following:</span></span>

-   <span data-ttu-id="0153b-134">2 GHz CPU (，其花了50% 的時間轉譯) 限制為每秒呼叫此 API 1000000 次。</span><span class="sxs-lookup"><span data-stu-id="0153b-134">A 2 GHz CPU (which spends 50 percent of its time rendering) is limited to calling this API 1 million times a second.</span></span>
-   <span data-ttu-id="0153b-135">若要達到每秒30個畫面格，您無法在每個畫面上呼叫此 API 33000 次以上。</span><span class="sxs-lookup"><span data-stu-id="0153b-135">To achieve 30 frames per second, you cannot call this API more than 33,000 times per frame.</span></span>
-   <span data-ttu-id="0153b-136">您只能針對每個畫面轉譯 3.3 K 物件 (假設每個物件的轉譯順序) 有10個 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-136">You can only render 3.3K objects per frame (assuming 10 of these API calls for each object's render sequence).</span></span>

<span data-ttu-id="0153b-137">換句話說，如果您的每個 API 呼叫都有足夠的時間，您可以回答預算問題，例如可透過互動方式轉譯的基本專案數。</span><span class="sxs-lookup"><span data-stu-id="0153b-137">In other words, if you had sufficient time per API call, you could answer a budgeting question such as the number of primitives that can be rendered interactively.</span></span> <span data-ttu-id="0153b-138">但是，檢測分析工具所傳回的原始數位將無法準確回答預算問題。</span><span class="sxs-lookup"><span data-stu-id="0153b-138">But the raw numbers returned by an instrumenting profiler will not accurately answer the budgeting questions.</span></span> <span data-ttu-id="0153b-139">這是因為圖形管線有複雜的設計問題，例如需要執行工作的元件數目、控制工作在元件之間流動方式的處理器數目，以及在執行時間中執行的優化策略，以及設計來讓管線更有效率的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0153b-139">This is because the graphics pipeline has complex design issues such as the number of components that need to do work, the number of processors that control how the work flows between components, and optimization strategies implemented in the runtime and in a driver that are designed to make the pipeline more efficient.</span></span>

### <a name="each-api-call-goes-through-several-components"></a><span data-ttu-id="0153b-140">每個 API 呼叫都會經歷數個元件</span><span class="sxs-lookup"><span data-stu-id="0153b-140">Each API Call Goes through Several Components</span></span>

<span data-ttu-id="0153b-141">每次呼叫都會由數個元件從應用程式處理至視訊卡。</span><span class="sxs-lookup"><span data-stu-id="0153b-141">Each call is processed by several components on its way from the application to the video card.</span></span> <span data-ttu-id="0153b-142">例如，請考慮下列轉譯順序，其中包含兩個繪製單一三角形的呼叫：</span><span class="sxs-lookup"><span data-stu-id="0153b-142">For instance, consider the following render sequence containing two calls for drawing a single triangle:</span></span>


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



<span data-ttu-id="0153b-143">下列概念圖表顯示呼叫必須通過的不同元件。</span><span class="sxs-lookup"><span data-stu-id="0153b-143">The following conceptual diagram shows the different components through which the calls must pass.</span></span>

![api 呼叫經過的圖形元件圖表](images/microbenchmarkinstructionflow2.png)

<span data-ttu-id="0153b-145">應用程式會叫用 Direct3D 來控制場景、處理使用者互動，並決定轉譯的完成方式。</span><span class="sxs-lookup"><span data-stu-id="0153b-145">The application invokes Direct3D which controls the scene, handles user interactions, and determines how rendering is done.</span></span> <span data-ttu-id="0153b-146">所有這項工作都是在轉譯順序中指定，使用 Direct3D API 呼叫傳送到執行時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-146">All of this work is specified in the render sequence, which is sent to the runtime using Direct3D API calls.</span></span> <span data-ttu-id="0153b-147">轉譯順序幾乎是硬體獨立的 (也就是說，API 呼叫與硬體無關，但應用程式知道視訊卡支援哪些功能) 。</span><span class="sxs-lookup"><span data-stu-id="0153b-147">The render sequence is virtually hardware independent (that is, the API calls are hardware independent but an application has knowledge of what features a video card supports).</span></span>

<span data-ttu-id="0153b-148">執行時間會將這些呼叫轉換成與裝置無關的格式。</span><span class="sxs-lookup"><span data-stu-id="0153b-148">The runtime converts these calls into a device-independent format.</span></span> <span data-ttu-id="0153b-149">執行時間會處理應用程式與驅動程式之間的所有通訊，如此一來，應用程式就會根據) 所需的功能，在多個硬體 (上執行。</span><span class="sxs-lookup"><span data-stu-id="0153b-149">The runtime handles all the communication between the application and the driver, so that an application will run on more than one compatible piece of hardware (depending on the features required).</span></span> <span data-ttu-id="0153b-150">測量函式呼叫時，檢測分析工具會測量其花費在函數中的時間，以及函式傳回的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-150">When measuring a function call, an instrumenting profiler measures the time it spent in a function as well as the time for the function to return.</span></span> <span data-ttu-id="0153b-151">檢測分析工具有一項限制，就是它可能不會包含驅動程式將產生的工作傳送至視訊卡的時間，或視訊卡處理工作的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-151">One limitation of an instrumenting profiler is that it may not include the time it takes a driver to send the resulting work to the video card nor the time for the video card to process the work.</span></span> <span data-ttu-id="0153b-152">換句話說，現成的檢測分析工具無法屬性與每個函式呼叫相關聯的所有工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-152">In other words, an off-the-shelf instrumenting profiler fails to attribute all of the work associated with each function call.</span></span>

<span data-ttu-id="0153b-153">軟體驅動程式會使用有關視訊卡的硬體特定知識，將裝置獨立的命令轉換成一連串的視訊卡命令。</span><span class="sxs-lookup"><span data-stu-id="0153b-153">The software driver uses hardware specific knowledge about the video card to convert the device-independent commands into a sequence of video card commands.</span></span> <span data-ttu-id="0153b-154">驅動程式也可以優化傳送至視訊卡的命令順序，以便有效率地在視訊卡上進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="0153b-154">Drivers may also optimize the sequence of commands that are sent to the video card, so that rendering on the video card is done efficiently.</span></span> <span data-ttu-id="0153b-155">這些優化可能會造成程式碼剖析問題，因為完成的工作量不會 (您可能需要瞭解) 的優化。</span><span class="sxs-lookup"><span data-stu-id="0153b-155">These optimizations can cause profiling problems because the amount of work done is not what it appears to be (you may need to understand the optimizations to account for them).</span></span> <span data-ttu-id="0153b-156">驅動程式通常會在視訊卡完成所有命令的處理之前，將控制權傳回給執行時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-156">The driver typically returns control to the runtime before the video card has finished processing all the commands.</span></span>

<span data-ttu-id="0153b-157">視訊卡會藉由合併頂點和索引緩衝區、材質、轉譯狀態資訊和圖形命令的資料，來執行大部分的呈現。</span><span class="sxs-lookup"><span data-stu-id="0153b-157">The video card performs the majority of the rendering by combining data from the vertex and index buffers, textures, render state information, and the graphics commands.</span></span> <span data-ttu-id="0153b-158">當視訊卡完成轉譯時，從轉譯順序建立的工作會完成。</span><span class="sxs-lookup"><span data-stu-id="0153b-158">When the video card finishes rendering, the work created from the render sequence is complete.</span></span>

<span data-ttu-id="0153b-159">每個元件都必須處理每個 Direct3D API 呼叫 (執行時間、驅動程式和視訊卡) 轉譯任何事物。</span><span class="sxs-lookup"><span data-stu-id="0153b-159">Each Direct3D API call must be processed by each component (the runtime, the driver, and the video card) to render anything.</span></span>

### <a name="there-is-more-than-one-processor-controlling-the-components"></a><span data-ttu-id="0153b-160">有一個以上的處理器控制元件</span><span class="sxs-lookup"><span data-stu-id="0153b-160">There Is More than One Processor Controlling the Components</span></span>

<span data-ttu-id="0153b-161">這些元件之間的關聯性更為複雜，因為應用程式、執行時間和驅動程式是由一個處理器所控制，而視訊卡是由不同的處理器控制。</span><span class="sxs-lookup"><span data-stu-id="0153b-161">The relationship between these components is even more complex, because the application, runtime, and the driver are controlled by one processor and the video card is controlled by a separate processor.</span></span> <span data-ttu-id="0153b-162">下圖顯示兩種處理器：中央處理器 (CPU) 和圖形處理單元 (GPU) 。</span><span class="sxs-lookup"><span data-stu-id="0153b-162">The following diagram shows two kinds of processors: a central processing unit (CPU) and a graphics processing unit (GPU).</span></span>

![cpu 和 gpu 及其元件的圖表](images/microbenchmarkprocessors.png)

<span data-ttu-id="0153b-164">電腦系統至少有一個 CPU 和一個 GPU，但可以有一或兩個以上的其中一個。</span><span class="sxs-lookup"><span data-stu-id="0153b-164">PC systems have at least one CPU and one GPU, but can have more than one of either or both.</span></span> <span data-ttu-id="0153b-165">Cpu 位於主機板上，而 Gpu 位於主機板或視訊卡上。</span><span class="sxs-lookup"><span data-stu-id="0153b-165">The CPUs are located on the motherboard, and the GPUs are located either on the motherboard or on the video card.</span></span> <span data-ttu-id="0153b-166">CPU 的速度取決於主機板上的時鐘晶片，GPU 的速度取決於不同的時鐘晶片。</span><span class="sxs-lookup"><span data-stu-id="0153b-166">The speed of the CPU is determined by a clock chip on the motherboard, and the speed of the GPU is determined by a separate clock chip.</span></span> <span data-ttu-id="0153b-167">CPU 時鐘可控制應用程式、執行時間和驅動程式完成工作的速度。</span><span class="sxs-lookup"><span data-stu-id="0153b-167">The CPU clock controls the speed of the work done by the application, the runtime, and the driver.</span></span> <span data-ttu-id="0153b-168">應用程式會透過執行時間和驅動程式，將工作傳送至 GPU。</span><span class="sxs-lookup"><span data-stu-id="0153b-168">The application sends work to the GPU via the runtime and the driver.</span></span>

<span data-ttu-id="0153b-169">CPU 和 GPU 通常會以不同的速度執行，而不受彼此影響。</span><span class="sxs-lookup"><span data-stu-id="0153b-169">The CPU and the GPU generally run at different speeds, independent of one another.</span></span> <span data-ttu-id="0153b-170">當工作可供使用時，GPU 可以立即回應工作 (假設 GPU 已完成處理先前的工作) 。</span><span class="sxs-lookup"><span data-stu-id="0153b-170">The GPU may respond to the work as soon as the work is available (assuming the GPU has finished processing previous work).</span></span> <span data-ttu-id="0153b-171">GPU 工作會與上圖中的曲線所反白顯示的 CPU 工作平行完成。</span><span class="sxs-lookup"><span data-stu-id="0153b-171">The GPU work is done in parallel with the CPU work as highlighted by the curved line in the figure above.</span></span> <span data-ttu-id="0153b-172">分析工具通常會測量 CPU 的效能，而不是 GPU 的效能。</span><span class="sxs-lookup"><span data-stu-id="0153b-172">A profiler generally measures the performance of the CPU, not the GPU.</span></span> <span data-ttu-id="0153b-173">這使得分析變得很困難，因為檢測分析工具所做的測量包括 CPU 時間，但可能不包含 GPU 時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-173">This makes profiling challenging, because the measurements made by an instrumenting profiler include the CPU time but may not include the GPU time.</span></span>

<span data-ttu-id="0153b-174">GPU 的目的是要將 CPU 的處理，從 CPU 載入到專為圖形工作而設計的處理器。</span><span class="sxs-lookup"><span data-stu-id="0153b-174">The purpose of the GPU is to off-load processing from the CPU to a processor specifically designed for graphics work.</span></span> <span data-ttu-id="0153b-175">在新式視訊卡上，GPU 會將管線中的大部分轉換和燈光工作取代為 GPU 的 CPU。</span><span class="sxs-lookup"><span data-stu-id="0153b-175">On modern video cards, the GPU replaces much of the transform and lighting work in the pipeline from the CPU to the GPU.</span></span> <span data-ttu-id="0153b-176">這可大幅減少 CPU 工作負載，讓更多的 CPU 週期可供其他處理使用。</span><span class="sxs-lookup"><span data-stu-id="0153b-176">This greatly reduces the CPU workload, leaving more CPU cycles available for other processing.</span></span> <span data-ttu-id="0153b-177">若要調整圖形應用程式的尖峰效能，您需要測量 CPU 和 GPU 的效能，並在這兩種類型的處理器之間平衡工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-177">To tune a graphical application for peak performance, you need to measure the performance of both the CPU and the GPU, and balance the work between the two types of processors.</span></span>

<span data-ttu-id="0153b-178">本檔未涵蓋與測量 GPU 效能或平衡 CPU 與 GPU 之間的工作相關的主題。</span><span class="sxs-lookup"><span data-stu-id="0153b-178">This document does not cover topics related to measuring the performance of the GPU or balancing the work between the CPU and the GPU.</span></span> <span data-ttu-id="0153b-179">如果您想要進一步瞭解 GPU (或特定視訊卡) 的效能，請造訪廠商的網站，尋找有關 GPU 效能的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0153b-179">If you want to better understand the performance of a GPU (or a particular video card), visit the vendor's web site to look for more information about GPU performance.</span></span> <span data-ttu-id="0153b-180">相反地，這份檔著重于執行時間和驅動程式所完成的工作，方法是將 GPU 工作縮減為可忽略的量。</span><span class="sxs-lookup"><span data-stu-id="0153b-180">Instead, this document focuses on the work done by the runtime and the driver by reducing the GPU work to a negligible amount.</span></span> <span data-ttu-id="0153b-181">這部分是根據發生效能問題的應用程式，通常是 CPU 限制的體驗。</span><span class="sxs-lookup"><span data-stu-id="0153b-181">This is, in part, based on experience that applications experiencing performance problems are generally CPU-limited.</span></span>

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a><span data-ttu-id="0153b-182">執行時間和驅動程式優化可以遮罩 API 度量</span><span class="sxs-lookup"><span data-stu-id="0153b-182">Runtime and Driver Optimizations Can Mask API Measurements</span></span>

<span data-ttu-id="0153b-183">執行時間有內建的效能優化，可能會讓個別呼叫的測量量過高。</span><span class="sxs-lookup"><span data-stu-id="0153b-183">The runtime has a performance optimization built into it that can overwhelm the measurement of an individual call.</span></span> <span data-ttu-id="0153b-184">以下是示範此問題的範例案例。</span><span class="sxs-lookup"><span data-stu-id="0153b-184">Here's an example scenario that demonstrates this problem.</span></span> <span data-ttu-id="0153b-185">請考慮下列轉譯順序：</span><span class="sxs-lookup"><span data-stu-id="0153b-185">Consider the following render sequence:</span></span>


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



<span data-ttu-id="0153b-186">範例1：簡單呈現順序</span><span class="sxs-lookup"><span data-stu-id="0153b-186">Example 1: Simple Render Sequence</span></span>

<span data-ttu-id="0153b-187">查看轉譯順序中兩個呼叫的結果，檢測分析工具可能會傳回類似下列的結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-187">Looking at the results for the two calls in the render sequence, an instrumenting profiler could return results similar to these:</span></span>


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



<span data-ttu-id="0153b-188">分析工具會傳回處理與每個呼叫相關聯之工作所需的 CPU 週期數目 (請記住，由於 GPU 尚未開始處理這些命令) ，因此不會在這些數目中包含 GPU。</span><span class="sxs-lookup"><span data-stu-id="0153b-188">The profiler returns the number of CPU cycles required to process the work associated with each call (remember that the GPU isn't included in these numbers because the GPU hasn't started working on these commands yet).</span></span> <span data-ttu-id="0153b-189">因為 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 需要將近一百萬個週期來處理，所以您可以得出結論，這並不是非常有效率。</span><span class="sxs-lookup"><span data-stu-id="0153b-189">Because [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) required almost a million cycles to process, you could conclude that it is not very efficient.</span></span> <span data-ttu-id="0153b-190">不過，您很快就會看到這項結論不正確的原因，以及您可以如何產生可用於預算的結果。</span><span class="sxs-lookup"><span data-stu-id="0153b-190">However, you'll soon see why this conclusion is incorrect and how you can generate results that can be used for budgeting.</span></span>

### <a name="measuring-state-changes-requires-careful-render-sequences"></a><span data-ttu-id="0153b-191">測量狀態變更需要小心轉譯順序</span><span class="sxs-lookup"><span data-stu-id="0153b-191">Measuring State Changes Requires Careful Render Sequences</span></span>

<span data-ttu-id="0153b-192">IDirect3DDevice9 以外的所有呼叫 [**:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)、 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)或 [**Clear**](/windows/desktop/api) (例如 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)、 [**SetVertexDeclaration**](/windows/desktop/api)和 [**graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) 會產生狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-192">All calls other than [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive), or [**Clear**](/windows/desktop/api) (such as [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), [**SetVertexDeclaration**](/windows/desktop/api), and [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) produce a state change.</span></span> <span data-ttu-id="0153b-193">每個狀態變更都會設定管線狀態，以控制如何完成轉譯。</span><span class="sxs-lookup"><span data-stu-id="0153b-193">Each state change sets pipeline state that controls how rendering will be done.</span></span>

<span data-ttu-id="0153b-194">執行時間及（或）驅動程式中的優化是設計來藉由減少所需的工作量來加速轉譯。</span><span class="sxs-lookup"><span data-stu-id="0153b-194">Optimizations in the runtime and/or the driver are designed to speed up rendering by reducing the amount of work required.</span></span> <span data-ttu-id="0153b-195">以下是一些可能會會污染設定檔平均值的狀態變更優化：</span><span class="sxs-lookup"><span data-stu-id="0153b-195">The following are a couple of state change optimizations that may pollute profile averages:</span></span>

-   <span data-ttu-id="0153b-196">驅動程式 (或執行時間) 可能會將狀態變更儲存為本機狀態。</span><span class="sxs-lookup"><span data-stu-id="0153b-196">A driver (or the runtime) could save a state change as a local state.</span></span> <span data-ttu-id="0153b-197">因為驅動程式可在「延遲」演算法中運作 (將工作延後到絕對必要) ，否則與某些狀態變更相關聯的工作可能會延遲。</span><span class="sxs-lookup"><span data-stu-id="0153b-197">Because the driver could operate in a "lazy" algorithm (postponing work until it is absolutely necessary), work associated with some state changes could get delayed.</span></span>
-   <span data-ttu-id="0153b-198">執行時間 (或驅動程式) 可能會藉由優化來移除狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-198">The runtime (or a driver) may remove state changes by optimizing.</span></span> <span data-ttu-id="0153b-199">其中一個範例可能是移除因為先前已停用光源而停用光源的重複狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-199">An example of this might be to remove a redundant state change that disables lighting because lighting has previously been disabled.</span></span>

<span data-ttu-id="0153b-200">沒有萬無一失的方式可以查看轉譯順序，並結束哪些狀態變更將會設定中途位並延後工作，或只是藉由優化來移除。</span><span class="sxs-lookup"><span data-stu-id="0153b-200">There is no foolproof way to look at a render sequence and conclude which state changes will set a dirty bit and defer work, or will simply be removed by optimization.</span></span> <span data-ttu-id="0153b-201">即使您可以在目前的執行時間或驅動程式中識別優化狀態變更，仍可能會更新未來的執行時間或驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0153b-201">Even if you could identify optimized state changes in today's runtime or driver, tomorrow's runtime or driver is likely to be updated.</span></span> <span data-ttu-id="0153b-202">您也不容易知道先前的狀態為何，因此很難識別多餘的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-202">You also don't readily know what the previous state was so it is difficult to identify redundant state changes.</span></span> <span data-ttu-id="0153b-203">驗證狀態變更成本的唯一方法，就是測量包含狀態變更的呈現順序。</span><span class="sxs-lookup"><span data-stu-id="0153b-203">The only way to verify the cost of a state change is to measure the render sequence that includes the state changes.</span></span>

<span data-ttu-id="0153b-204">如您所見，由於有多個處理器、由多個元件處理的命令，以及元件內建的優化，使程式碼剖析難以預測，因此會造成複雜的問題。</span><span class="sxs-lookup"><span data-stu-id="0153b-204">As you can see, the complications caused by having multiple processors, commands being processed by more than one component, and optimizations built into the components make profiling difficult to predict.</span></span> <span data-ttu-id="0153b-205">在下一節中，將會解決這些分析挑戰。</span><span class="sxs-lookup"><span data-stu-id="0153b-205">In the next section, each of these profiling challenges will be addressed.</span></span> <span data-ttu-id="0153b-206">將會顯示範例 Direct3D 轉譯序列，以及伴隨的測量技術。</span><span class="sxs-lookup"><span data-stu-id="0153b-206">Sample Direct3D render sequences will be shown, with the accompanying measurement techniques.</span></span> <span data-ttu-id="0153b-207">透過這種知識，您將能夠針對個別呼叫產生精確、可重複的度量。</span><span class="sxs-lookup"><span data-stu-id="0153b-207">With this knowledge, you will be able to generate accurate, repeatable measurements on individual calls.</span></span>

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a><span data-ttu-id="0153b-208">如何精確地分析 Direct3D 轉譯順序</span><span class="sxs-lookup"><span data-stu-id="0153b-208">How to Accurately Profile a Direct3D Render Sequence</span></span>

<span data-ttu-id="0153b-209">現在已醒目提示某些程式碼剖析挑戰，本節將為您說明可協助您產生可用於預算的設定檔測量的技巧。</span><span class="sxs-lookup"><span data-stu-id="0153b-209">Now that some of the profiling challenges have been highlighted, this section will show you techniques that will help you generate profile measurements that can be used for budgeting.</span></span> <span data-ttu-id="0153b-210">如果您瞭解 CPU 所控制元件之間的關聯性，以及如何避免執行時間和驅動程式所執行的效能優化，則可以精確、可重複的分析測量措施。</span><span class="sxs-lookup"><span data-stu-id="0153b-210">Accurate, repeatable profiling measurements are possible if you understand the relationship between the components controlled by the CPU, and how to avoid performance optimizations implemented by the runtime and the driver.</span></span>

<span data-ttu-id="0153b-211">若要開始，您必須能夠精確地測量單一 API 呼叫的執行時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-211">To begin, you need to be able to accurately measure the execution time of a single API call.</span></span>

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a><span data-ttu-id="0153b-212">挑選精確的測量工具，例如 QueryPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="0153b-212">Pick an Accurate Measurement Tool Like QueryPerformanceCounter</span></span>

<span data-ttu-id="0153b-213">Microsoft Windows 作業系統包含高解析度計時器，可用來測量高解析度的經過時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-213">The Microsoft Windows operating system includes a high-resolution timer that can be used to measure high-resolution elapsed times.</span></span> <span data-ttu-id="0153b-214">您可以使用 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來傳回其中一個這類計時器的目前值。</span><span class="sxs-lookup"><span data-stu-id="0153b-214">The current value of one such timer can be returned using [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span> <span data-ttu-id="0153b-215">叫用 **QueryPerformanceCounter** 來傳回開始和停止值之後，這兩個值之間的差異可以轉換成實際經過的時間， (秒) 使用 **QueryPerformanceCounter**。</span><span class="sxs-lookup"><span data-stu-id="0153b-215">After invoking **QueryPerformanceCounter** to return start and stop values, the difference between the two values can be converted to the actual elapsed time (in seconds) using **QueryPerformanceCounter**.</span></span>

<span data-ttu-id="0153b-216">使用 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 的優點是它可以在 Windows 中使用，而且很容易使用。</span><span class="sxs-lookup"><span data-stu-id="0153b-216">The advantages of using [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) are that it is available in Windows and it is easy to use.</span></span> <span data-ttu-id="0153b-217">只要使用 **QueryPerformanceCounter** 呼叫來括住呼叫，並儲存開始和停止值即可。</span><span class="sxs-lookup"><span data-stu-id="0153b-217">Simply surround the calls with a **QueryPerformanceCounter** call and save the start and stop values.</span></span> <span data-ttu-id="0153b-218">因此，本文將示範如何使用 **QueryPerformanceCounter** 來分析執行時間，類似于檢測分析工具測量它的方式。</span><span class="sxs-lookup"><span data-stu-id="0153b-218">Therefore, this paper will demonstrate how to use **QueryPerformanceCounter** to profile execution times, similar to the way an instrumenting profiler would measure it.</span></span> <span data-ttu-id="0153b-219">以下範例顯示如何在原始程式碼中內嵌 **QueryPerformanceCounter** ：</span><span class="sxs-lookup"><span data-stu-id="0153b-219">Here's an example that shows how to embed **QueryPerformanceCounter** in your source code:</span></span>


```
  BeginScene();
    ...
    // Start profiling
    LARGE_INTEGER start, stop, freq;
    QueryPerformanceCounter(&start);

    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1); 

    QueryPerformanceCounter(&stop);
    stop.QuadPart -= start.QuadPart;
    QueryPerformanceFrequency(&freq);
    // Stop profiling
    ...
  EndScene();
  Present();
```



<span data-ttu-id="0153b-220">範例2：使用 QPC 執行自訂分析</span><span class="sxs-lookup"><span data-stu-id="0153b-220">Example 2: Custom Profiling Implementation with QPC</span></span>

<span data-ttu-id="0153b-221">開始和停止是兩個大型整數，會保存高效能計時器傳回的開始和停止值。</span><span class="sxs-lookup"><span data-stu-id="0153b-221">start and stop are two large integers that will hold the start and stop values returned by the high-performance timer.</span></span> <span data-ttu-id="0153b-222">請注意，QueryPerformanceCounter (&start) 只會在 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 QueryPerformanceCounter 之前呼叫， (&stop) 是在 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-222">Notice that QueryPerformanceCounter(&start) is called just before [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) and QueryPerformanceCounter(&stop) is called just after [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span> <span data-ttu-id="0153b-223">取得停止值之後，會呼叫 QueryPerformanceFrequency 來傳回頻率，也就是高解析度計時器的頻率。</span><span class="sxs-lookup"><span data-stu-id="0153b-223">After getting the stop value, QueryPerformanceFrequency is called to return freq, which is the frequency of the high-resolution timer.</span></span> <span data-ttu-id="0153b-224">在此假設範例中，假設您取得開始、停止和頻率的下列結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-224">In this hypothetical example, suppose you get the following results for start, stop, and freq:</span></span>



| <span data-ttu-id="0153b-225">區域變數</span><span class="sxs-lookup"><span data-stu-id="0153b-225">Local Variable</span></span> | <span data-ttu-id="0153b-226">刻度數目</span><span class="sxs-lookup"><span data-stu-id="0153b-226">Number of Ticks</span></span> |
|----------------|-----------------|
| <span data-ttu-id="0153b-227">start</span><span class="sxs-lookup"><span data-stu-id="0153b-227">start</span></span>          | <span data-ttu-id="0153b-228">1792998845094</span><span class="sxs-lookup"><span data-stu-id="0153b-228">1792998845094</span></span>   |
| <span data-ttu-id="0153b-229">stop</span><span class="sxs-lookup"><span data-stu-id="0153b-229">stop</span></span>           | <span data-ttu-id="0153b-230">1792998845102</span><span class="sxs-lookup"><span data-stu-id="0153b-230">1792998845102</span></span>   |
| <span data-ttu-id="0153b-231">頻率</span><span class="sxs-lookup"><span data-stu-id="0153b-231">freq</span></span>           | <span data-ttu-id="0153b-232">3579545</span><span class="sxs-lookup"><span data-stu-id="0153b-232">3579545</span></span>         |



 

<span data-ttu-id="0153b-233">您可以將這些值轉換為執行 API 呼叫所需的迴圈次數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0153b-233">You could convert these values to the number of cycles it takes to execute the API calls like this:</span></span>


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



<span data-ttu-id="0153b-234">換句話說，在此 2 GHz 電腦上處理 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 大約需要大約4568個時鐘週期。</span><span class="sxs-lookup"><span data-stu-id="0153b-234">In other words, it takes about 4568 clock cycles to process [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) and [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) on this 2 GHz machine.</span></span> <span data-ttu-id="0153b-235">您可以將這些值轉換為執行所有呼叫所花費的實際時間，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0153b-235">You could convert these values to the actual time it took to execute all the calls like this:</span></span>


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



<span data-ttu-id="0153b-236">使用 QueryPerformanceCounter 時，您必須將開始和停止度量新增至轉譯順序，並使用 QueryPerformanceFrequency 將刻度的 (數目) 轉換為 CPU 週期數目或實際時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-236">Using QueryPerformanceCounter requires that you add start and stop measurements to your render sequence and use QueryPerformanceFrequency to convert the difference (number of ticks) to the number of CPU cycles or to actual time.</span></span> <span data-ttu-id="0153b-237">識別測量技術是開始開發自訂程式碼剖析的好開端。</span><span class="sxs-lookup"><span data-stu-id="0153b-237">Identifying the measurement technique is a good start for developing a custom profiling implementation.</span></span> <span data-ttu-id="0153b-238">但在您開始進行測量並開始進行測量之前，您必須先瞭解如何處理視訊卡。</span><span class="sxs-lookup"><span data-stu-id="0153b-238">But before you jump in and start making measurements, you need to know how to deal with the video card.</span></span>

### <a name="focus-on-cpu-measurements"></a><span data-ttu-id="0153b-239">專注于 CPU 度量</span><span class="sxs-lookup"><span data-stu-id="0153b-239">Focus on CPU Measurements</span></span>

<span data-ttu-id="0153b-240">如先前所述，CPU 和 GPU 會平行運作，以處理 API 呼叫所產生的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-240">As stated earlier, the CPU and the GPU work in parallel to process the work generated by the API calls.</span></span> <span data-ttu-id="0153b-241">真實世界的應用程式需要分析這兩種類型的處理器，以找出您的應用程式是否受 CPU 限制或 GPU 受限。</span><span class="sxs-lookup"><span data-stu-id="0153b-241">A real world application requires profiling both types of processors to find out if your application is CPU-limited or GPU-limited.</span></span> <span data-ttu-id="0153b-242">因為 GPU 效能是廠商專屬的，所以在本文中產生的結果會是很大的挑戰，其中涵蓋各種可用的視訊卡。</span><span class="sxs-lookup"><span data-stu-id="0153b-242">Since GPU performance is vendor specific, it would be very challenging to produce results in this paper that cover the variety of video cards available.</span></span>

<span data-ttu-id="0153b-243">這份檔只會著重在分析 CPU 所執行的工作，方法是使用自訂技術來測量執行時間和驅動程式工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-243">Instead, this paper will focus only on profiling the work performed by the CPU by using a custom technique for measuring the runtime and driver work.</span></span> <span data-ttu-id="0153b-244">GPU 工作將會縮減為不重要的數量，讓 CPU 結果更明顯。</span><span class="sxs-lookup"><span data-stu-id="0153b-244">The GPU work will be reduced to an insignificant amount, so that CPU results are more visible.</span></span> <span data-ttu-id="0153b-245">這種方法的其中一個優點是，這項技術會產生附錄中的結果，讓您能夠與您的度量相互關聯。</span><span class="sxs-lookup"><span data-stu-id="0153b-245">One benefit of this approach is that this technique yields results in the Appendix that you should be able to correlate with your measurements.</span></span> <span data-ttu-id="0153b-246">若要將視訊卡所需的工作減少到無意義的層級，只要將轉譯工作縮減至可能的最小數量即可。</span><span class="sxs-lookup"><span data-stu-id="0153b-246">To reduce the work required by the video card to an insignificant level, simply reduce the rendering work to the least amount possible.</span></span> <span data-ttu-id="0153b-247">這可以透過限制繪製呼叫來呈現單一三角形來完成，而且可以進一步限制，讓每個三角形只包含一個圖元。</span><span class="sxs-lookup"><span data-stu-id="0153b-247">This can be accomplished by limiting draw calls to render a single triangle, and can be further constrained so that each triangle only contains one pixel.</span></span>

<span data-ttu-id="0153b-248">本檔中用於測量 CPU 工作的測量單位，會是 CPU 頻率週期的數目，而不是實際時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-248">The unit of measure used in this paper for measuring CPU work will be the number of CPU clock cycles rather than actual time.</span></span> <span data-ttu-id="0153b-249">CPU 頻率週期的優點是，cpu 延遲的應用程式) 的可攜性 (，與 CPU 速度不同的電腦上實際經過的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-249">CPU clock cycles has the advantage that it is more portable (for CPU-limited applications) than actual elapsed time across machines with different CPU speeds.</span></span> <span data-ttu-id="0153b-250">您可以視需要輕鬆地將其轉換為實際時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-250">This can easily be converted to actual time if desired.</span></span>

<span data-ttu-id="0153b-251">本檔未涵蓋在 CPU 與 GPU 之間平衡工作負載的相關主題。</span><span class="sxs-lookup"><span data-stu-id="0153b-251">This document does not cover topics related to balancing the work load between the CPU and the GPU.</span></span> <span data-ttu-id="0153b-252">請記住，本文的目標不是要測量應用程式的整體效能，而是示範如何精確測量執行時間和驅動程式處理 API 呼叫所需的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-252">Remember, the goal of this paper is not to measure the overall performance of an application, but to show you how to accurately measure the time it takes the runtime and the driver to process API calls.</span></span> <span data-ttu-id="0153b-253">使用這些精確的測量，您就可以將 CPU 的預算工作列入考慮，以瞭解特定的效能案例。</span><span class="sxs-lookup"><span data-stu-id="0153b-253">With these accurate measurements, you can take on the task of budgeting the CPU to understand certain performance scenarios.</span></span>

### <a name="controlling-runtime-and-driver-optimizations"></a><span data-ttu-id="0153b-254">控制執行時間和驅動程式優化</span><span class="sxs-lookup"><span data-stu-id="0153b-254">Controlling Runtime and Driver Optimizations</span></span>

<span data-ttu-id="0153b-255">在識別測量技術的情況下，下一步是瞭解程式碼剖析時所取得的執行時間和驅動程式優化策略。</span><span class="sxs-lookup"><span data-stu-id="0153b-255">With a measurement technique identified, and a strategy for reducing GPU work, the next step is to understand the runtime and driver optimizations that get in the way when you are profiling.</span></span>

<span data-ttu-id="0153b-256">CPU 工作可以分為三個值區：應用程式工作、執行時間運作和驅動程式運作。</span><span class="sxs-lookup"><span data-stu-id="0153b-256">The CPU work can be divided into three buckets: the application work, the runtime work, and the driver work.</span></span> <span data-ttu-id="0153b-257">因為這是在程式設計人員控制項下，所以請略過應用程式的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-257">Ignore the application work since this is under programmer control.</span></span> <span data-ttu-id="0153b-258">從應用程式的觀點來看，執行時間和驅動程式就像黑色方塊一樣，因為應用程式無法控制在其中執行的專案。</span><span class="sxs-lookup"><span data-stu-id="0153b-258">From the application's standpoint, the runtime and the driver are like black boxes, as the application has no control over what is implemented in them.</span></span> <span data-ttu-id="0153b-259">重要的是瞭解可在執行時間和驅動程式中執行的優化技術。</span><span class="sxs-lookup"><span data-stu-id="0153b-259">The key is to understand the optimization techniques that may be implemented in the runtime and the driver.</span></span> <span data-ttu-id="0153b-260">如果您不了解這些優化，很容易就能根據設定檔量值，跳到 CPU 所執行之工作量的錯誤結論。</span><span class="sxs-lookup"><span data-stu-id="0153b-260">If you don't understand these optimizations, it is very easy to jump to the wrong conclusion about the amount of work the CPU is doing based on the profile measurements.</span></span> <span data-ttu-id="0153b-261">尤其是，有兩個主題與所謂的命令緩衝區相關，以及它可以如何進行程式碼剖析。</span><span class="sxs-lookup"><span data-stu-id="0153b-261">In particular, there are two topics related to something called the command buffer and what it can do to obfuscate profiling.</span></span> <span data-ttu-id="0153b-262">這些主題包括：</span><span class="sxs-lookup"><span data-stu-id="0153b-262">These topics are:</span></span>

-   <span data-ttu-id="0153b-263">使用命令緩衝區的執行時間優化。</span><span class="sxs-lookup"><span data-stu-id="0153b-263">Runtime optimization with the Command Buffer.</span></span> <span data-ttu-id="0153b-264">命令緩衝區是執行時間優化，可減少模式轉換的影響。</span><span class="sxs-lookup"><span data-stu-id="0153b-264">The command buffer is a runtime optimization that reduces the impact of a mode transition.</span></span> <span data-ttu-id="0153b-265">若要控制模式轉換的時間，請參閱 [控制命令緩衝區](#controlling-the-command-buffer)。</span><span class="sxs-lookup"><span data-stu-id="0153b-265">To control the timing of the mode transition, see [Controlling the Command Buffer](#controlling-the-command-buffer).</span></span>
-   <span data-ttu-id="0153b-266">否定命令緩衝區的計時效果。</span><span class="sxs-lookup"><span data-stu-id="0153b-266">Negating the timing effects of the Command Buffer.</span></span> <span data-ttu-id="0153b-267">模式轉換的經過時間可能會對分析量測測量造成很大的影響。</span><span class="sxs-lookup"><span data-stu-id="0153b-267">The elapsed time of a mode transition can have a big impact on profiling measurements.</span></span> <span data-ttu-id="0153b-268">這項策略的策略是 [讓轉譯順序比模式轉換更大](#make-the-render-sequence-large-compared-to-the-mode-transition)。</span><span class="sxs-lookup"><span data-stu-id="0153b-268">The strategy for this is to [Make the Render Sequence Large Compared to the Mode Transition](#make-the-render-sequence-large-compared-to-the-mode-transition).</span></span>

### <a name="controlling-the-command-buffer"></a><span data-ttu-id="0153b-269">控制命令緩衝區</span><span class="sxs-lookup"><span data-stu-id="0153b-269">Controlling the Command Buffer</span></span>

<span data-ttu-id="0153b-270">當應用程式進行 API 呼叫時，執行時間會將 API 呼叫轉換為與裝置無關的格式， (我們會呼叫命令) ，並將它儲存在命令緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="0153b-270">When an application makes an API call, the runtime converts the API call to a device-independent format (which we will call a command), and stores it in the command buffer.</span></span> <span data-ttu-id="0153b-271">命令緩衝區會新增至下圖。</span><span class="sxs-lookup"><span data-stu-id="0153b-271">The command buffer is added to the following diagram.</span></span>

![cpu 元件的圖表，包括命令緩衝區](images/microbenchmarkcommandbuffer2.png)

<span data-ttu-id="0153b-273">每次應用程式進行另一個 API 呼叫時，執行時間都會重複此順序，並將另一個命令新增至命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-273">Each time the application makes another API call, the runtime repeats this sequence and adds another command to the command buffer.</span></span> <span data-ttu-id="0153b-274">在某個時間點，執行時間會清空緩衝區 (將命令傳送至驅動程式) 。</span><span class="sxs-lookup"><span data-stu-id="0153b-274">At some point, the runtime empties the buffer (sending the commands to the driver).</span></span> <span data-ttu-id="0153b-275">在 Windows XP 中，清空命令緩衝區會導致模式轉換，因為作業系統會從執行時間 (以使用者模式執行，) 到以核心模式) 執行的驅動程式 (，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="0153b-275">In Windows XP, emptying the command buffer causes a mode transition as the operating system switches from the runtime (running in user mode) to the driver (running in kernel mode), as shown in the following diagram.</span></span>

-   <span data-ttu-id="0153b-276">使用者模式-執行應用程式程式碼的非特殊許可權處理器模式。</span><span class="sxs-lookup"><span data-stu-id="0153b-276">user mode - The non-privileged processor mode that executes application code.</span></span> <span data-ttu-id="0153b-277">使用者模式應用程式無法取得系統資料的存取權（透過系統服務）。</span><span class="sxs-lookup"><span data-stu-id="0153b-277">User-mode applications cannot gain access to system data except through system services.</span></span>
-   <span data-ttu-id="0153b-278">核心模式：以 Windows 為基礎的執行程式碼執行時的特殊許可權處理器模式。</span><span class="sxs-lookup"><span data-stu-id="0153b-278">kernel mode - The privileged processor mode in which Windows-based executive code runs.</span></span> <span data-ttu-id="0153b-279">在核心模式中執行的驅動程式或執行緒可以存取所有系統記憶體、直接存取硬體，以及使用硬體來執行 i/o 的 CPU 指示。</span><span class="sxs-lookup"><span data-stu-id="0153b-279">A driver or thread running in kernel mode has access to all system memory, direct access to hardware, and the CPU instructions to perform I/O with the hardware.</span></span>

![使用者模式和核心模式之間的轉換圖](images/microbenchmarkcommandbuffer3.png)

<span data-ttu-id="0153b-281">每次 CPU 從使用者切換至核心模式時，都會進行轉換 (相反地，) 而且其所需的週期數目很大，相較于個別的 API 呼叫會有很大的影響。</span><span class="sxs-lookup"><span data-stu-id="0153b-281">The transition happens each time the CPU switches from user to kernel mode (and vice versa) and the number of cycles it requires is large compared to an individual API call.</span></span> <span data-ttu-id="0153b-282">如果執行時間在叫用時，將每個 API 呼叫傳送至驅動程式，則每個 API 呼叫都會產生模式轉換的成本。</span><span class="sxs-lookup"><span data-stu-id="0153b-282">If the runtime sent each API call to the driver when it was invoked, every API call would incur the cost of a mode transition.</span></span>

<span data-ttu-id="0153b-283">相反地，命令緩衝區是執行時間優化，其設計目的是要降低模式轉換的有效成本。</span><span class="sxs-lookup"><span data-stu-id="0153b-283">Instead, the command buffer is a runtime optimization designed to reduce the effective cost of the mode transition.</span></span> <span data-ttu-id="0153b-284">命令緩衝區會將許多驅動程式命令排入佇列，以準備單一模式轉換。</span><span class="sxs-lookup"><span data-stu-id="0153b-284">The command buffer queues many driver commands in preparation for a single mode transition.</span></span> <span data-ttu-id="0153b-285">當執行時間將命令新增至命令緩衝區時，控制權會傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="0153b-285">When the runtime adds a command to the command buffer, control is returned to the application.</span></span> <span data-ttu-id="0153b-286">Profiler 無法得知驅動程式命令甚至可能尚未傳送至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0153b-286">A profiler has no way of knowing that the driver commands have probably not even been sent to the driver yet.</span></span> <span data-ttu-id="0153b-287">如此一來，現成檢測分析工具所傳回的數位會造成誤導，因為它會測量執行時間的工作，但不會測量相關聯的驅動程式工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-287">As a result, the numbers returned by an off-the-shelf instrumenting profiler are misleading since it measures the runtime work but not the associated driver work.</span></span>

### <a name="profile-results-without-a-mode-transition"></a><span data-ttu-id="0153b-288">不使用模式轉換剖析結果</span><span class="sxs-lookup"><span data-stu-id="0153b-288">Profile Results without a Mode Transition</span></span>

<span data-ttu-id="0153b-289">使用範例2中的轉譯順序，以下是一些可說明模式轉換大小的一般計時度量。</span><span class="sxs-lookup"><span data-stu-id="0153b-289">Using the render sequence from example 2, here are some typical timing measurements that illustrate the magnitude of a mode transition.</span></span> <span data-ttu-id="0153b-290">假設 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 呼叫不會造成模式轉換，則現成的檢測分析工具可能會傳回類似下列的結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-290">Assuming that [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) and [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) calls do not cause a mode transition, an off-the-shelf instrumenting profiler could return results similar to these:</span></span>


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



<span data-ttu-id="0153b-291">每個數位都是執行時間將這些呼叫新增至命令緩衝區所需的時間量。</span><span class="sxs-lookup"><span data-stu-id="0153b-291">Each of these numbers are the amount of time it takes for the runtime to add these calls to the command buffer.</span></span> <span data-ttu-id="0153b-292">因為沒有模式轉換，所以驅動程式尚未完成任何工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-292">Since there is no mode transition, the driver has not done any work yet.</span></span> <span data-ttu-id="0153b-293">分析工具的結果是正確的，但它們並不會測量轉譯順序最終會造成 CPU 執行的所有工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-293">The profiler results are accurate, but they do not measure all of the work that the render sequence will eventually cause the CPU to perform.</span></span>

### <a name="profile-results-with-a-mode-transition"></a><span data-ttu-id="0153b-294">使用模式轉換剖析結果</span><span class="sxs-lookup"><span data-stu-id="0153b-294">Profile Results with a Mode Transition</span></span>

<span data-ttu-id="0153b-295">現在，請看看發生模式轉換時，相同範例會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="0153b-295">Now, look at what happens for the same example when a mode transition occurs.</span></span> <span data-ttu-id="0153b-296">這次，假設 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 會導致模式轉換。</span><span class="sxs-lookup"><span data-stu-id="0153b-296">This time, assume [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) and [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) cause a mode transition.</span></span> <span data-ttu-id="0153b-297">同樣地，現成的檢測分析工具可能會傳回類似以下的結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-297">Once again, an off-the-shelf instrumenting profiler could return results similar to these:</span></span>


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



<span data-ttu-id="0153b-298">針對 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 所測量的時間大約相同，不過， [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 所花費的時間量會大幅增加，因為模式轉換。</span><span class="sxs-lookup"><span data-stu-id="0153b-298">The time measured for [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) is about the same, however, the dramatic increase in the amount of time spent in [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) is due to the mode transition.</span></span> <span data-ttu-id="0153b-299">以下是發生的情況：</span><span class="sxs-lookup"><span data-stu-id="0153b-299">Here's what is happening:</span></span>

1.  <span data-ttu-id="0153b-300">假設在轉譯順序開始之前，命令緩衝區有一個命令的空間。</span><span class="sxs-lookup"><span data-stu-id="0153b-300">Assume the command buffer has room for one command before our render sequence starts.</span></span>
2.  <span data-ttu-id="0153b-301">[**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 會轉換成與裝置無關的格式，並新增至命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-301">[**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) is converted to a device-independent format and added to the command buffer.</span></span> <span data-ttu-id="0153b-302">在此案例中，此呼叫會填入命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-302">In this scenario, this call fills the command buffer.</span></span>
3.  <span data-ttu-id="0153b-303">執行時間會嘗試將 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 新增至命令緩衝區，但無法將其新增至命令緩衝區，因為它已滿。</span><span class="sxs-lookup"><span data-stu-id="0153b-303">The runtime tries to add [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) to the command buffer but cannot, because it is full.</span></span> <span data-ttu-id="0153b-304">相反地，執行時間會清空命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-304">Instead, the runtime empties the command buffer.</span></span> <span data-ttu-id="0153b-305">這會導致核心模式轉換。</span><span class="sxs-lookup"><span data-stu-id="0153b-305">This causes the kernel-mode transition.</span></span> <span data-ttu-id="0153b-306">假設轉換大約需要5000迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-306">Assume the transition takes about 5000 cycles.</span></span> <span data-ttu-id="0153b-307">這段時間可因應 **DrawPrimitive** 所花費的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-307">This time contributes to time spent in **DrawPrimitive**.</span></span>
4.  <span data-ttu-id="0153b-308">驅動程式接著會處理與從命令緩衝區清空的所有命令相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-308">The driver then processes the work associated with all the commands that were emptied from the command buffer.</span></span> <span data-ttu-id="0153b-309">假設處理近乎填滿命令緩衝區之命令的驅動程式時間大約是935000迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-309">Assume that the driver time to process the commands that nearly filled the command buffer is about 935,000 cycles.</span></span> <span data-ttu-id="0153b-310">假設與 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 相關聯的驅動程式工作大約是2750迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-310">Assume that the driver work associated with [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) is about 2750 cycles.</span></span> <span data-ttu-id="0153b-311">這段時間可因應 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)所花費的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-311">This time contributes to time spent in [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>
5.  <span data-ttu-id="0153b-312">當驅動程式完成其工作時，使用者模式轉換會將控制權傳回到執行時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-312">When the driver finishes its work, the user-mode transition returns control to the runtime.</span></span> <span data-ttu-id="0153b-313">命令緩衝區現在是空的。</span><span class="sxs-lookup"><span data-stu-id="0153b-313">The command buffer is now empty.</span></span> <span data-ttu-id="0153b-314">假設轉換大約需要5000迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-314">Assume the transition takes about 5000 cycles.</span></span>
6.  <span data-ttu-id="0153b-315">轉譯順序的完成方式是轉換 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ，並將它新增至命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-315">The render sequence finishes by converting [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) and adding it to the command buffer.</span></span> <span data-ttu-id="0153b-316">假設這大約需要900迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-316">Assume this takes about 900 cycles.</span></span> <span data-ttu-id="0153b-317">這段時間可因應 **DrawPrimitive** 所花費的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-317">This time contributes to time spent in **DrawPrimitive**.</span></span>

<span data-ttu-id="0153b-318">總結結果之後，您會看到：</span><span class="sxs-lookup"><span data-stu-id="0153b-318">Summarizing the results, you see:</span></span>


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



<span data-ttu-id="0153b-319">就像在沒有模式轉換的情況下進行 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 的測量， (900 迴圈) ，採用模式轉換的 **DrawPrimitive** 測量 (947950 迴圈) 是精確的，但在預算的 CPU 工作方面毫無用處。</span><span class="sxs-lookup"><span data-stu-id="0153b-319">Just like the measurement for [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) without the mode transition (900 cycles), the measurement for **DrawPrimitive** with the mode transition (947,950 cycles) is accurate but useless in terms of budgeting CPU work.</span></span> <span data-ttu-id="0153b-320">結果包含正確的執行時間工作、驅動程式適用于 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)、驅動程式適用于任何之前 **SetTexture** 的命令，以及兩個模式轉換。</span><span class="sxs-lookup"><span data-stu-id="0153b-320">The result contains the correct runtime work, the driver work for [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), the driver work for any commands that preceded **SetTexture**, and two mode transitions.</span></span> <span data-ttu-id="0153b-321">不過，測量結果缺少 **DrawPrimitive** 驅動程式工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-321">However, the measurement is missing the **DrawPrimitive** driver work.</span></span>

<span data-ttu-id="0153b-322">可能會發生模式轉換，以回應任何呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-322">A mode transition could happen in response to any call.</span></span> <span data-ttu-id="0153b-323">這取決於先前在命令緩衝區中的內容。</span><span class="sxs-lookup"><span data-stu-id="0153b-323">It depends on what was previously in the command buffer.</span></span> <span data-ttu-id="0153b-324">您必須控制模式轉換，以瞭解多少 CPU 工作 (執行時間和驅動程式) 與每個呼叫相關聯。</span><span class="sxs-lookup"><span data-stu-id="0153b-324">You need to control the mode transition to understand how much CPU work (runtime and driver) is associated with each call.</span></span> <span data-ttu-id="0153b-325">若要這樣做，您需要一種機制來控制命令緩衝區和模式轉換的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-325">To do that, you need a mechanism for controlling the command buffer and the timing of the mode transition.</span></span>

### <a name="the-query-mechanism"></a><span data-ttu-id="0153b-326">查詢機制</span><span class="sxs-lookup"><span data-stu-id="0153b-326">The Query Mechanism</span></span>

<span data-ttu-id="0153b-327">Microsoft Direct3D 9 中的查詢機制是設計來讓執行時間查詢 GPU 以進行處理，並從 GPU 傳回特定資料。</span><span class="sxs-lookup"><span data-stu-id="0153b-327">The query mechanism in Microsoft Direct3D 9 was designed to allow the runtime to query the GPU for progress and return certain data from the GPU.</span></span> <span data-ttu-id="0153b-328">在分析期間，如果 GPU 工作最小化，使其對效能的影響降到最低，您可以從 GPU 傳回狀態，以協助測量驅動程式工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-328">While profiling, if the GPU work is minimized so that it has a negligible impact on performance, you can return status from the GPU to help measure the driver work.</span></span> <span data-ttu-id="0153b-329">畢竟，當 GPU 看到驅動程式命令之後，驅動程式就會完成。</span><span class="sxs-lookup"><span data-stu-id="0153b-329">After all, the driver work is complete when the GPU has seen the driver commands.</span></span> <span data-ttu-id="0153b-330">此外，您可以 coaxed 查詢機制來控制兩個對分析很重要的命令緩衝區特性：當命令緩衝區清空時，以及緩衝區中有多少工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-330">Additionally, the query mechanism can be coaxed into controlling two command buffer characteristics that are important to profiling: when the command buffer empties and how much work is in the buffer.</span></span>

<span data-ttu-id="0153b-331">以下是使用查詢機制的相同呈現順序：</span><span class="sxs-lookup"><span data-stu-id="0153b-331">Here's the same render sequence using the query mechanism:</span></span>


```
// 1. Create an event query from the current device
IDirect3DQuery9* pEvent;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEvent);

// 2. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 3. Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

// 4. Start profiling
LARGE_INTEGER start, stop;
QueryPerformanceCounter(&start);

// 5. Invoke the API calls to be profiled.
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);

// 6. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 7. Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
    
// 8. End profiling
QueryPerformanceCounter(&stop);
```



<span data-ttu-id="0153b-332">範例3：使用查詢來控制命令緩衝區</span><span class="sxs-lookup"><span data-stu-id="0153b-332">Example 3: Using a Query to Control the Command Buffer</span></span>

<span data-ttu-id="0153b-333">以下是每一行程式碼的詳細說明：</span><span class="sxs-lookup"><span data-stu-id="0153b-333">Here is a more detailed explanation of each of these lines of code:</span></span>

1.  <span data-ttu-id="0153b-334">建立具有 D3DQUERYTYPE 事件的 query 物件來建立事件查詢 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0153b-334">Create an event query by creating a query object with D3DQUERYTYPE\_EVENT.</span></span>
2.  <span data-ttu-id="0153b-335">藉由呼叫 ([**D3DISSUE \_ END**](d3dissue-end.md)) 的 [**問題**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)，將查詢事件標記新增至命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-335">Add a query event marker to the command buffer by calling [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)([**D3DISSUE\_END**](d3dissue-end.md)).</span></span> <span data-ttu-id="0153b-336">此標記會指示驅動程式追蹤 GPU 何時完成執行標記之前的任何命令。</span><span class="sxs-lookup"><span data-stu-id="0153b-336">This marker tells the driver to track when the GPU finishes executing whatever commands preceded the marker.</span></span>
3.  <span data-ttu-id="0153b-337">第一個呼叫會清空命令緩衝區，因為 [**使用**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) [**D3DGETDATA \_ FLUSH 呼叫**](d3dgetdata-flush.md) 會強制清空命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-337">The first call empties the command buffer because calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) with [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md) forces the command buffer to be emptied.</span></span> <span data-ttu-id="0153b-338">每個後續的呼叫都會檢查 GPU，以查看它何時完成處理所有命令緩衝區工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-338">Each subsequent call is checking the GPU to see when it finishes processing all the command-buffer work.</span></span> <span data-ttu-id="0153b-339">在 GPU 閒置之前，此迴圈不會傳回 S \_ 確定。</span><span class="sxs-lookup"><span data-stu-id="0153b-339">This loop does not return S\_OK until the GPU is idle.</span></span>
4.  <span data-ttu-id="0153b-340">範例開始時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-340">Sample the start time.</span></span>
5.  <span data-ttu-id="0153b-341">叫用正在分析的 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-341">Invoke the API calls being profiled.</span></span>
6.  <span data-ttu-id="0153b-342">將第二個查詢事件標記新增至命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-342">Add a second query event marker to the command buffer.</span></span> <span data-ttu-id="0153b-343">此標記將用來追蹤完成的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-343">This marker will be used to track the completion of the calls.</span></span>
7.  <span data-ttu-id="0153b-344">第一個呼叫會清空命令緩衝區，因為 [**使用**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) [**D3DGETDATA \_ FLUSH 呼叫**](d3dgetdata-flush.md) 會強制清空命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-344">The first call empties the command buffer because calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) with [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md) forces the command buffer to be emptied.</span></span> <span data-ttu-id="0153b-345">當 GPU 完成處理所有命令緩衝區工作 **時，[** 操作 \_ ] 會傳回 [確定]，而迴圈會因為 GPU 閒置而結束。</span><span class="sxs-lookup"><span data-stu-id="0153b-345">When the GPU finishes processing all the command-buffer work, **GetData** returns S\_OK, and the loop is exited because the GPU is idle.</span></span>
8.  <span data-ttu-id="0153b-346">取樣停止時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-346">Sample the stop time.</span></span>

<span data-ttu-id="0153b-347">以下是以 QueryPerformanceCounter 和 QueryPerformanceFrequency 測量的結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-347">Here are the results measured with QueryPerformanceCounter and QueryPerformanceFrequency:</span></span>



| <span data-ttu-id="0153b-348">區域變數</span><span class="sxs-lookup"><span data-stu-id="0153b-348">Local Variable</span></span> | <span data-ttu-id="0153b-349">刻度數目</span><span class="sxs-lookup"><span data-stu-id="0153b-349">Number of Ticks</span></span> |
|----------------|-----------------|
| <span data-ttu-id="0153b-350">start</span><span class="sxs-lookup"><span data-stu-id="0153b-350">start</span></span>          | <span data-ttu-id="0153b-351">1792998845060</span><span class="sxs-lookup"><span data-stu-id="0153b-351">1792998845060</span></span>   |
| <span data-ttu-id="0153b-352">stop</span><span class="sxs-lookup"><span data-stu-id="0153b-352">stop</span></span>           | <span data-ttu-id="0153b-353">1792998845090</span><span class="sxs-lookup"><span data-stu-id="0153b-353">1792998845090</span></span>   |
| <span data-ttu-id="0153b-354">頻率</span><span class="sxs-lookup"><span data-stu-id="0153b-354">freq</span></span>           | <span data-ttu-id="0153b-355">3579545</span><span class="sxs-lookup"><span data-stu-id="0153b-355">3579545</span></span>         |



 

<span data-ttu-id="0153b-356">在 2 GHz 電腦上再次將刻度轉換成迴圈一次 () ：</span><span class="sxs-lookup"><span data-stu-id="0153b-356">Converting ticks to cycles once again (on a 2 GHz machine):</span></span>


```
# ticks  = (stop - start) = 1792998845090 - 1792998845060 = 30 ticks
# cycles = CPU speed * number of ticks / QPF
# 16,450 = 2 GHz      * 30             / 3,579,545
```



<span data-ttu-id="0153b-357">以下是每次呼叫的迴圈數細目：</span><span class="sxs-lookup"><span data-stu-id="0153b-357">Here is the breakdown of the number of cycles per call:</span></span>


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
Number of cycles for Issue                : 200
Number of cycles for GetData              : 16,450
```



<span data-ttu-id="0153b-358">查詢機制允許我們控制執行時間和所測量的驅動程式工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-358">The query mechanism has allowed us to control the runtime and the driver work that is being measured.</span></span> <span data-ttu-id="0153b-359">若要瞭解每個數位，以下是回應每個 API 呼叫時所發生的狀況，以及預估的時間：</span><span class="sxs-lookup"><span data-stu-id="0153b-359">To understand each of these numbers, here's what is happening in response to each of the API calls, along with the estimated timings:</span></span>

1.  <span data-ttu-id="0153b-360">第一個呼叫會透過使用 [**D3DGETDATA \_ FLUSH 呼叫**](d3dgetdata-flush.md) [**，來**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)清空命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-360">The first call empties the command buffer by calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) with [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md).</span></span> <span data-ttu-id="0153b-361">當 GPU 完成處理所有命令緩衝區工作 **時，[** 操作 \_ ] 會傳回 [確定]，而迴圈會因為 GPU 閒置而結束。</span><span class="sxs-lookup"><span data-stu-id="0153b-361">When the GPU finishes processing all the command-buffer work, **GetData** returns S\_OK, and the loop is exited because the GPU is idle.</span></span>
2.  <span data-ttu-id="0153b-362">轉譯順序一開始會將 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 轉換成與裝置無關的格式，並將它新增至命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-362">The render sequence starts by converting [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) to a device-independent format and adding it to the command buffer.</span></span> <span data-ttu-id="0153b-363">假設這大約需要100迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-363">Assume this takes about 100 cycles.</span></span>
3.  <span data-ttu-id="0153b-364">[**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 會轉換並新增至命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-364">[**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) is converted and added to the command buffer.</span></span> <span data-ttu-id="0153b-365">假設這大約需要900迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-365">Assume this takes about 900 cycles.</span></span>
4.  <span data-ttu-id="0153b-366">[**問題**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) 會將查詢標記新增至命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-366">[**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) adds a query marker to the command buffer.</span></span> <span data-ttu-id="0153b-367">假設這大約需要200迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-367">Assume this takes about 200 cycles.</span></span>
5.  <span data-ttu-id="0153b-368">[，][**會讓命令**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)緩衝區清空，以強制執行核心模式轉換。</span><span class="sxs-lookup"><span data-stu-id="0153b-368">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) causes the command buffer to be emptied which forces the kernel-mode transition.</span></span> <span data-ttu-id="0153b-369">假設這大約需要5000迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-369">Assume this takes about 5000 cycles.</span></span>
6.  <span data-ttu-id="0153b-370">驅動程式接著會處理與所有四個呼叫相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-370">The driver then processes the work associated with all four calls.</span></span> <span data-ttu-id="0153b-371">假設處理 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 的驅動程式時間大約是2964迴圈， [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 大約是3600迴圈， [**問題**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) 大約是200週期。</span><span class="sxs-lookup"><span data-stu-id="0153b-371">Assume that the driver time to process [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) is about 2964 cycles, [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) is about 3600 cycles, [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) is about 200 cycles.</span></span> <span data-ttu-id="0153b-372">因此，所有四個命令的總驅動程式時間大約是6450迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-372">So the total driver time for all four commands is about 6450 cycles.</span></span>
    > [!Note]  
    > <span data-ttu-id="0153b-373">驅動程式也需要花一點時間來查看 GPU 的狀態。</span><span class="sxs-lookup"><span data-stu-id="0153b-373">The driver also takes a little time to see what the status of the GPU is.</span></span> <span data-ttu-id="0153b-374">因為 GPU 的運作方式很簡單，所以 GPU 應該已經完成。</span><span class="sxs-lookup"><span data-stu-id="0153b-374">Because the GPU work is trivial, the GPU should be done already.</span></span> <span data-ttu-id="0153b-375">[](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 「硬碟」會 \_ 根據 GPU 完成的可能性傳回「確定」。</span><span class="sxs-lookup"><span data-stu-id="0153b-375">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) will return S\_OK based on the likelihood that the GPU is finished.</span></span>

     

7.  <span data-ttu-id="0153b-376">當驅動程式完成其工作時，使用者模式轉換會將控制權傳回到執行時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-376">When the driver finishes its work, the user-mode transition returns control to the runtime.</span></span> <span data-ttu-id="0153b-377">命令緩衝區現在是空的。</span><span class="sxs-lookup"><span data-stu-id="0153b-377">The command buffer is now empty.</span></span> <span data-ttu-id="0153b-378">假設這大約需要5000迴圈。</span><span class="sxs-lookup"><span data-stu-id="0153b-378">Assume this takes about 5000 cycles.</span></span>

<span data-ttu-id="0153b-379">數量 [**值包含：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)</span><span class="sxs-lookup"><span data-stu-id="0153b-379">The numbers for [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) include:</span></span>


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



<span data-ttu-id="0153b-380">與 QueryPerformanceCounter 搭配使用的查詢機制會測量所有的 CPU 工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-380">The query mechanism used in combination with QueryPerformanceCounter measures all of the CPU work.</span></span> <span data-ttu-id="0153b-381">這是透過查詢標記和查詢狀態比較來完成。</span><span class="sxs-lookup"><span data-stu-id="0153b-381">This is done with a combination of query markers, and query status comparisons.</span></span> <span data-ttu-id="0153b-382">新增至命令緩衝區的開始和停止查詢標記是用來控制緩衝區中有多少工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-382">Start and stop query markers added to the command buffer are used to control how much work is in the buffer.</span></span> <span data-ttu-id="0153b-383">等到傳回正確的傳回碼時，才會在清除轉譯順序開始之前完成開始測量，並且在驅動程式完成與命令緩衝區內容相關聯的工作之後，才進行停止測量。</span><span class="sxs-lookup"><span data-stu-id="0153b-383">By waiting until the right return code is returned, the start measurement is made just before a clean render sequence starts, and the stop measurement is made just after the driver has finished the work associated with the command buffer contents.</span></span> <span data-ttu-id="0153b-384">這可有效地捕捉執行時間和驅動程式所完成的 CPU 工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-384">This effectively captures the CPU work done by the runtime as well as the driver.</span></span>

<span data-ttu-id="0153b-385">既然您知道命令緩衝區及其對分析的影響，您應該知道有一些其他條件可能會導致執行時間清空命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-385">Now that you know about the command buffer and the effect it can have on profiling, you should know that there are a few other conditions that can cause the runtime to empty the command buffer.</span></span> <span data-ttu-id="0153b-386">您必須在轉譯順序中監看這些專案。</span><span class="sxs-lookup"><span data-stu-id="0153b-386">You need to watch out for these in your render sequences.</span></span> <span data-ttu-id="0153b-387">其中有些條件是為了回應 API 呼叫，而其他則是為了回應執行時間中的資源變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-387">Some of these conditions are in response to API calls, others are in response to resource changes in the runtime.</span></span> <span data-ttu-id="0153b-388">下列任何一項條件都會導致模式轉換：</span><span class="sxs-lookup"><span data-stu-id="0153b-388">Any of the following conditions will cause a mode transition:</span></span>

-   <span data-ttu-id="0153b-389">當 ([**鎖定**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) 的其中一個鎖定方法時，會在特定條件下使用特定旗標) ，在頂點緩衝區、索引緩衝區或材質 (上呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-389">When one of the lock methods ([**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) is called on a vertex buffer, index buffer, or texture (under certain conditions with certain flags).</span></span>
-   <span data-ttu-id="0153b-390">當裝置或頂點緩衝區、索引緩衝區或材質建立時。</span><span class="sxs-lookup"><span data-stu-id="0153b-390">When a device or vertex buffer, index buffer, or texture is created.</span></span>
-   <span data-ttu-id="0153b-391">當最後一個版本終結裝置或頂點緩衝區、索引緩衝區或紋理時。</span><span class="sxs-lookup"><span data-stu-id="0153b-391">When a device or vertex buffer, index buffer, or texture is destroyed by the last release.</span></span>
-   <span data-ttu-id="0153b-392">當呼叫 [**ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) 時。</span><span class="sxs-lookup"><span data-stu-id="0153b-392">When [**ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) is called.</span></span>
-   <span data-ttu-id="0153b-393">如果 [**有的話**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) ，則會呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-393">When [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) is called.</span></span>
-   <span data-ttu-id="0153b-394">當命令緩衝區填滿時。</span><span class="sxs-lookup"><span data-stu-id="0153b-394">When the command buffer fills up.</span></span>
-   <span data-ttu-id="0153b-395">使用 D3DGETDATA 排 [**清時，會呼叫**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) \_ 。</span><span class="sxs-lookup"><span data-stu-id="0153b-395">When [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) is called with D3DGETDATA\_FLUSH.</span></span>

<span data-ttu-id="0153b-396">請小心在轉譯順序中監看這些條件。</span><span class="sxs-lookup"><span data-stu-id="0153b-396">Be careful to watch for these conditions in your render sequences.</span></span> <span data-ttu-id="0153b-397">每次新增模式轉換時，10000的驅動程式工作週期都會新增至分析測量。</span><span class="sxs-lookup"><span data-stu-id="0153b-397">Every time a mode transition is added, 10,000 cycles of driver work will be added to your profiling measurements.</span></span> <span data-ttu-id="0153b-398">此外，命令緩衝區不會以靜態方式調整大小。</span><span class="sxs-lookup"><span data-stu-id="0153b-398">In addition, the command buffer is not statically sized.</span></span> <span data-ttu-id="0153b-399">執行時間可能會變更緩衝區大小，以回應應用程式所產生的工作量。</span><span class="sxs-lookup"><span data-stu-id="0153b-399">The runtime may change the buffer's size in response to the amount of work that is being generated by the application.</span></span> <span data-ttu-id="0153b-400">這也是另一個相依于轉譯順序的優化。</span><span class="sxs-lookup"><span data-stu-id="0153b-400">This is yet another optimization that is dependent on a render sequence.</span></span>

<span data-ttu-id="0153b-401">因此請小心控制分析期間的模式轉換。</span><span class="sxs-lookup"><span data-stu-id="0153b-401">So be careful to control mode transitions during profiling.</span></span> <span data-ttu-id="0153b-402">查詢機制提供了一種健全的方法來清空命令緩衝區，讓您可以控制模式轉換的時間，以及緩衝區所包含的工作量。</span><span class="sxs-lookup"><span data-stu-id="0153b-402">The query mechanism offers a robust method for emptying the command buffer so that you can control the timing of the mode transition as well as the amount of work the buffer contains.</span></span> <span data-ttu-id="0153b-403">但是，即使這項技術也可以藉由減少模式轉換時間來改善，以使其對測量的結果無關緊要。</span><span class="sxs-lookup"><span data-stu-id="0153b-403">However, even this technique can be improved by reducing the mode transition time to make it insignificant with respect to the measured result.</span></span>

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a><span data-ttu-id="0153b-404">比模式轉換更大的呈現順序</span><span class="sxs-lookup"><span data-stu-id="0153b-404">Make the Render Sequence Large Compared to the Mode Transition</span></span>

<span data-ttu-id="0153b-405">在上述範例中，核心模式切換和使用者模式交換器耗用大約10000週期，與執行時間和驅動程式工作無關。</span><span class="sxs-lookup"><span data-stu-id="0153b-405">In the previous example, the kernel-mode switch and the user-mode switch consume about 10,000 cycles that have nothing to do with runtime and driver work.</span></span> <span data-ttu-id="0153b-406">由於模式轉換是內建在作業系統中，因此無法縮減為零。</span><span class="sxs-lookup"><span data-stu-id="0153b-406">Since the mode transition is built into the operating system, it cannot be reduced to zero.</span></span> <span data-ttu-id="0153b-407">若要讓模式轉換成為無意義的，轉譯序列需要調整，讓驅動程式和執行時間工作的大小比模式切換的順序大。</span><span class="sxs-lookup"><span data-stu-id="0153b-407">To make the mode transition insignificant, the render sequence needs to adjusted so that the driver and runtime work are an order of magnitude larger than the mode switches.</span></span> <span data-ttu-id="0153b-408">您可以嘗試進行減法以移除轉換，但透過更大的轉譯順序成本來攤銷成本會更可靠。</span><span class="sxs-lookup"><span data-stu-id="0153b-408">You could try to do a subtraction to remove the transitions, but amortizing the cost over a much larger render sequence cost is more reliable.</span></span>

<span data-ttu-id="0153b-409">減少模式轉換的策略（直到變成不重要的策略）會將迴圈加入至轉譯順序。</span><span class="sxs-lookup"><span data-stu-id="0153b-409">The strategy for reducing the mode transition until it becomes insignificant is to add a loop to the render sequence.</span></span> <span data-ttu-id="0153b-410">例如，如果新增了迴圈來重複轉譯順序1500次，讓我們看看分析結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-410">For example, let look at the profiling results if a loop is added that will repeat the render sequence 1500 times:</span></span>


```
// Initialize the array with two textures, same size, same format
IDirect3DTexture* texArray[2];

CreateQuery(D3DQUERYTYPE_EVENT, pEvent);
pEvent->Issue(D3DISSUE_END);
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

LARGE_INTEGER start, stop;
// Now start counting because the video card is ready
QueryPerformanceCounter(&start);

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  SetTexture(taxArray[i%2]);
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

pEvent->Issue(D3DISSUE_END);

while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
QueryPerformanceCounter(&stop);
```



<span data-ttu-id="0153b-411">範例4：將迴圈加入至轉譯順序</span><span class="sxs-lookup"><span data-stu-id="0153b-411">Example 4: Add a Loop to the Render Sequence</span></span>

<span data-ttu-id="0153b-412">以下是以 QueryPerformanceCounter 和 QueryPerformanceFrequency 測量的結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-412">Here are the results measured with QueryPerformanceCounter and QueryPerformanceFrequency:</span></span>



| <span data-ttu-id="0153b-413">區域變數</span><span class="sxs-lookup"><span data-stu-id="0153b-413">Local Variable</span></span> | <span data-ttu-id="0153b-414">Tics 數目</span><span class="sxs-lookup"><span data-stu-id="0153b-414">Number of Tics</span></span> |
|----------------|----------------|
| <span data-ttu-id="0153b-415">start</span><span class="sxs-lookup"><span data-stu-id="0153b-415">start</span></span>          | <span data-ttu-id="0153b-416">1792998845000</span><span class="sxs-lookup"><span data-stu-id="0153b-416">1792998845000</span></span>  |
| <span data-ttu-id="0153b-417">stop</span><span class="sxs-lookup"><span data-stu-id="0153b-417">stop</span></span>           | <span data-ttu-id="0153b-418">1792998847084</span><span class="sxs-lookup"><span data-stu-id="0153b-418">1792998847084</span></span>  |
| <span data-ttu-id="0153b-419">頻率</span><span class="sxs-lookup"><span data-stu-id="0153b-419">freq</span></span>           | <span data-ttu-id="0153b-420">3579545</span><span class="sxs-lookup"><span data-stu-id="0153b-420">3579545</span></span>        |



 

<span data-ttu-id="0153b-421">立即使用 QueryPerformanceCounter 量值2840刻度。</span><span class="sxs-lookup"><span data-stu-id="0153b-421">Using QueryPerformanceCounter measures 2,840 ticks now.</span></span> <span data-ttu-id="0153b-422">將刻度轉換成迴圈和我們已經顯示的相同：</span><span class="sxs-lookup"><span data-stu-id="0153b-422">Converting ticks to cycles is the same as we have already shown:</span></span>


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



<span data-ttu-id="0153b-423">換句話說，這 2 GHz 電腦上大約需要6900000個週期，才能處理轉譯迴圈中的1500呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-423">In other words, it takes about 6.9 million cycles on this 2 GHz machine to process the 1500 calls in the render loop.</span></span> <span data-ttu-id="0153b-424">在6900000週期中，模式轉換中的時間量大約是1萬，因此現在設定檔結果幾乎會完全測量與 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-424">Of the 6.9 million cycles, the amount of time in the mode transitions is approximately 10k, so now the profile results are almost entirely measuring work associated with [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) and [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>

<span data-ttu-id="0153b-425">請注意，程式碼範例需要兩個材質的陣列。</span><span class="sxs-lookup"><span data-stu-id="0153b-425">Notice that the code sample requires an array of two textures.</span></span> <span data-ttu-id="0153b-426">為了避免在每次呼叫時都設定相同材質指標的執行時間優化，只要使用兩個材質的陣列，就會移除 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 。</span><span class="sxs-lookup"><span data-stu-id="0153b-426">To avoid a runtime optimization that would remove [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) if it sets the same texture pointer every time it is called, simply use an array of two textures.</span></span> <span data-ttu-id="0153b-427">如此一來，每次執行迴圈時，材質指標就會變更，並執行與 **SetTexture** 相關聯的完整工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-427">That way, each time through the loop, the texture pointer changes, and the full work associated with **SetTexture** is performed.</span></span> <span data-ttu-id="0153b-428">請確定這兩個紋理都有相同的大小和格式，如此一來，材質不會變更其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0153b-428">Be sure that both textures are the same size and format, so that no other state will change when the texture does.</span></span>

<span data-ttu-id="0153b-429">現在您已經有分析 Direct3D 的技巧。</span><span class="sxs-lookup"><span data-stu-id="0153b-429">And now you have a technique for profiling Direct3D.</span></span> <span data-ttu-id="0153b-430">它依賴高效能計數器 (QueryPerformanceCounter) 來記錄 CPU 處理工作所需的滴答數。</span><span class="sxs-lookup"><span data-stu-id="0153b-430">It relies on the high performance counter (QueryPerformanceCounter) to record the number of ticks it takes the CPU to process work.</span></span> <span data-ttu-id="0153b-431">您可以使用查詢機制，小心地將工作控制為與 API 呼叫相關聯的執行時間和驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0153b-431">The work is carefully controlled to be the runtime and driver work associated with API calls using the query mechanism.</span></span> <span data-ttu-id="0153b-432">查詢提供兩種控制方法：先在轉譯順序開始之前清空命令緩衝區，第二個則是在 GPU 工作完成時傳回。</span><span class="sxs-lookup"><span data-stu-id="0153b-432">A query provides two means of control: first to empty the command buffer before the render sequence starts, and secondly to return when the GPU work is finished.</span></span>

<span data-ttu-id="0153b-433">到目前為止，本文已說明如何分析轉譯順序。</span><span class="sxs-lookup"><span data-stu-id="0153b-433">So far, this paper has shown how to profile a render sequence.</span></span> <span data-ttu-id="0153b-434">每個轉譯順序都相當簡單，其中包含單一 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 呼叫和 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-434">Each render sequence has been fairly simple, containing a single [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) call and a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) call.</span></span> <span data-ttu-id="0153b-435">這樣做的目的是要將焦點放在命令緩衝區，並使用查詢機制來控制它。</span><span class="sxs-lookup"><span data-stu-id="0153b-435">This was done to focus on the command buffer and the use of the query mechanism to control it.</span></span> <span data-ttu-id="0153b-436">以下是如何分析任意轉譯序列的簡短摘要：</span><span class="sxs-lookup"><span data-stu-id="0153b-436">Here is a brief summary of how to profile an arbitrary render sequence:</span></span>

-   <span data-ttu-id="0153b-437">使用高效能計數器（例如 QueryPerformanceCounter）來測量處理每個 API 呼叫所需的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-437">Use a high performance counter like QueryPerformanceCounter to measure the time it takes to process each API call.</span></span> <span data-ttu-id="0153b-438">使用 QueryPerformanceFrequency 和 CPU 頻率速率，將此值轉換為每個 API 呼叫的 CPU 週期數目。</span><span class="sxs-lookup"><span data-stu-id="0153b-438">Use QueryPerformanceFrequency and the CPU clock rate to convert this to the number of CPU cycles per API call.</span></span>
-   <span data-ttu-id="0153b-439">藉由轉譯三角形清單來將 GPU 工作的數量降到最低，其中每個三角形都包含一個圖元。</span><span class="sxs-lookup"><span data-stu-id="0153b-439">Minimize the amount of GPU work by rendering triangle lists, where each triangle contains one pixel.</span></span>
-   <span data-ttu-id="0153b-440">在轉譯順序之前，請使用查詢機制來清空命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-440">Use the query mechanism to empty the command buffer before the render sequence.</span></span> <span data-ttu-id="0153b-441">這可保證分析將會捕捉與轉譯順序相關聯的執行時間和驅動程式工作的正確數量。</span><span class="sxs-lookup"><span data-stu-id="0153b-441">This guarantees that profiling will capturing the correct amount of runtime and driver work associated with the render sequence.</span></span>
-   <span data-ttu-id="0153b-442">使用查詢事件標記來控制新增至命令緩衝區的工作量。</span><span class="sxs-lookup"><span data-stu-id="0153b-442">Control the amount of work added to the command buffer with query event markers.</span></span> <span data-ttu-id="0153b-443">這個相同的查詢會偵測 GPU 何時完成其工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-443">This same query detects when the GPU finishes its work.</span></span> <span data-ttu-id="0153b-444">因為 GPU 的工作很簡單，這幾乎相當於測量驅動程式工作完成的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-444">Since the GPU work is trivial, this is virtually equivalent to measuring when the driver work is completed.</span></span>

<span data-ttu-id="0153b-445">所有這些技術都是用來分析狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-445">All of these techniques are used to profile state changes.</span></span> <span data-ttu-id="0153b-446">假設您已閱讀並瞭解如何控制命令緩衝區，並已順利完成 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)的基準測量，您就可以將狀態變更新增至轉譯順序。</span><span class="sxs-lookup"><span data-stu-id="0153b-446">Assuming that you have read and understood how to control the command buffer, and have successfully completed baseline measurements on [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), you are ready to add state changes to your render sequences.</span></span> <span data-ttu-id="0153b-447">將狀態變更新增至轉譯順序時，有一些額外的程式碼剖析挑戰。</span><span class="sxs-lookup"><span data-stu-id="0153b-447">There are a few additional profiling challenges when adding state changes to a render sequence.</span></span> <span data-ttu-id="0153b-448">如果您想要將狀態變更新增至轉譯順序，請務必繼續進行下一節。</span><span class="sxs-lookup"><span data-stu-id="0153b-448">If you intend to add state changes to your render sequences, be sure to continue into the next section.</span></span>

## <a name="profiling-direct3d-state-changes"></a><span data-ttu-id="0153b-449">分析 Direct3D 狀態變更</span><span class="sxs-lookup"><span data-stu-id="0153b-449">Profiling Direct3D State Changes</span></span>

<span data-ttu-id="0153b-450">Direct3D 使用許多轉譯狀態來控制幾乎所有的管線層面。</span><span class="sxs-lookup"><span data-stu-id="0153b-450">Direct3D uses many render states to control almost every aspect of the pipeline.</span></span> <span data-ttu-id="0153b-451">導致狀態變更的 Api 包括繪製基本呼叫以外的任何函數或方法 \* 。</span><span class="sxs-lookup"><span data-stu-id="0153b-451">The APIs that cause state changes include any function or method other than the Draw\*Primitive calls.</span></span>

<span data-ttu-id="0153b-452">狀態變更很棘手，因為您可能無法查看狀態變更的成本，而不會呈現。</span><span class="sxs-lookup"><span data-stu-id="0153b-452">State changes are tricky because you may not be able to see the cost of a state change without rendering.</span></span> <span data-ttu-id="0153b-453">這是延遲演算法的結果，驅動程式和 GPU 會使用這些演算法來延遲工作，直到絕對必須完成為止。</span><span class="sxs-lookup"><span data-stu-id="0153b-453">This is a result of the lazy algorithm that the driver and the GPU use to defer work until it absolutely has to be done.</span></span> <span data-ttu-id="0153b-454">一般而言，您應該遵循下列步驟來測量單一狀態變更：</span><span class="sxs-lookup"><span data-stu-id="0153b-454">In general, you should follow these steps to measure a single state change:</span></span>

1.  <span data-ttu-id="0153b-455">先分析 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 。</span><span class="sxs-lookup"><span data-stu-id="0153b-455">Profile [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) first.</span></span>
2.  <span data-ttu-id="0153b-456">將一項狀態變更新增至轉譯順序，並分析新的序列。</span><span class="sxs-lookup"><span data-stu-id="0153b-456">Add one state change to the render sequence and profile the new sequence.</span></span>
3.  <span data-ttu-id="0153b-457">減去兩個序列之間的差異，以取得狀態變更的成本。</span><span class="sxs-lookup"><span data-stu-id="0153b-457">Subtract the difference between the two sequences to get the cost of the state change.</span></span>

<span data-ttu-id="0153b-458">當然，您已瞭解如何使用查詢機制並將轉譯順序放在迴圈中，以消除模式轉換的成本。</span><span class="sxs-lookup"><span data-stu-id="0153b-458">Naturally, everything you have learned about using the query mechanism and putting the render sequence in a loop to negate the cost of the mode transition still applies.</span></span>

### <a name="profiling-a-simple-state-change"></a><span data-ttu-id="0153b-459">程式碼剖析簡單狀態變更</span><span class="sxs-lookup"><span data-stu-id="0153b-459">Profiling a Simple State Change</span></span>

<span data-ttu-id="0153b-460">從包含 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)的轉譯順序開始，以下是測量新增 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)成本的程式碼序列：</span><span class="sxs-lookup"><span data-stu-id="0153b-460">Starting with a render sequence that contains [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), here is the code sequence for measuring the cost of adding [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture):</span></span>


```
// Get the start counter value as shown in Example 4 

// Initialize a texture array as shown in Example 4
IDirect3DTexture* texArray[2];

// Render sequence loop 
for(int i = 0; i < 1500; i++)
{
  SetTexture(0, texArray[i%2];
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

// Get the stop counter value as shown in Example 4 
```



<span data-ttu-id="0153b-461">範例5：測量一次狀態變更 API 呼叫</span><span class="sxs-lookup"><span data-stu-id="0153b-461">Example 5: Measuring One State Change API Call</span></span>

<span data-ttu-id="0153b-462">請注意，迴圈包含兩個呼叫： [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)。</span><span class="sxs-lookup"><span data-stu-id="0153b-462">Notice that the loop contains two calls, [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) and [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span> <span data-ttu-id="0153b-463">轉譯順序會迴圈1500次，並產生類似以下的結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-463">The render sequence loops 1500 times and generates results similar to these:</span></span>



| <span data-ttu-id="0153b-464">區域變數</span><span class="sxs-lookup"><span data-stu-id="0153b-464">Local Variable</span></span> | <span data-ttu-id="0153b-465">Tics 數目</span><span class="sxs-lookup"><span data-stu-id="0153b-465">Number of Tics</span></span> |
|----------------|----------------|
| <span data-ttu-id="0153b-466">start</span><span class="sxs-lookup"><span data-stu-id="0153b-466">start</span></span>          | <span data-ttu-id="0153b-467">1792998860000</span><span class="sxs-lookup"><span data-stu-id="0153b-467">1792998860000</span></span>  |
| <span data-ttu-id="0153b-468">stop</span><span class="sxs-lookup"><span data-stu-id="0153b-468">stop</span></span>           | <span data-ttu-id="0153b-469">1792998870260</span><span class="sxs-lookup"><span data-stu-id="0153b-469">1792998870260</span></span>  |
| <span data-ttu-id="0153b-470">頻率</span><span class="sxs-lookup"><span data-stu-id="0153b-470">freq</span></span>           | <span data-ttu-id="0153b-471">3579545</span><span class="sxs-lookup"><span data-stu-id="0153b-471">3579545</span></span>        |



 

<span data-ttu-id="0153b-472">再次將刻度轉換成迴圈會產生：</span><span class="sxs-lookup"><span data-stu-id="0153b-472">Converting ticks to cycles once again yields:</span></span>


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



<span data-ttu-id="0153b-473">除以迴圈中的反覆運算次數會產生：</span><span class="sxs-lookup"><span data-stu-id="0153b-473">Dividing by the number of iterations in the loop yields:</span></span>


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



<span data-ttu-id="0153b-474">迴圈的每個反復專案都包含狀態變更和繪製呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-474">Each iteration of the loop contains a state change and a draw call.</span></span> <span data-ttu-id="0153b-475">減去 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 轉譯序列的結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-475">Subtracting out the result of the [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) render sequence leaves:</span></span>


```
3850 - 1100 = 2750 cycles for SetTexture
```



<span data-ttu-id="0153b-476">這是將 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 新增至此轉譯順序的平均迴圈數目。</span><span class="sxs-lookup"><span data-stu-id="0153b-476">This is the average number of cycles to add [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) to this render sequence.</span></span> <span data-ttu-id="0153b-477">同樣的技巧也可以套用至其他狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-477">This same technique can be applied to other state changes.</span></span>

<span data-ttu-id="0153b-478">為什麼 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 稱為簡單狀態變更？</span><span class="sxs-lookup"><span data-stu-id="0153b-478">Why is [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) called a simple state change?</span></span> <span data-ttu-id="0153b-479">由於正在設定的狀態受到限制，因此管線會在每次狀態變更時執行相同數量的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-479">Because the state that is being set is constrained so that the pipeline does the same amount of work each time the state is changed.</span></span> <span data-ttu-id="0153b-480">將兩個材質限制為相同的大小和格式，可確保每個 **SetTexture** 呼叫都有相同數量的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-480">Constraining both textures to the same size and format assures the same amount of work for each **SetTexture** call.</span></span>

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a><span data-ttu-id="0153b-481">分析需要切換的狀態變更</span><span class="sxs-lookup"><span data-stu-id="0153b-481">Profiling a State Change that Needs to Be Toggled</span></span>

<span data-ttu-id="0153b-482">有其他狀態變更會導致圖形管線針對轉譯迴圈的每個反復專案變更圖形管線所執行的工作量。</span><span class="sxs-lookup"><span data-stu-id="0153b-482">There are other state changes that cause the amount of work performed by the graphics pipeline to change for every iteration of the render loop.</span></span> <span data-ttu-id="0153b-483">例如，如果已啟用 z 測試，則只有在針對現有圖元的 z 值測試新圖元的 z 值之後，每個圖元色彩才會更新轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="0153b-483">For example, if z-testing is enabled, each pixel color updates a render target only after the new pixel's z value is tested against the z-value for the existing pixel.</span></span> <span data-ttu-id="0153b-484">如果停用 z 測試，則不會執行每個圖元的測試，而且輸出的寫入速度會更快。</span><span class="sxs-lookup"><span data-stu-id="0153b-484">If z-testing is disabled, this per-pixel test is not done and the output is written much faster.</span></span> <span data-ttu-id="0153b-485">啟用或停用 z 測試狀態會大幅變更 CPU (完成的工作量，以及轉譯期間的 GPU) 。</span><span class="sxs-lookup"><span data-stu-id="0153b-485">Enabling or disabling the z-test state dramatically changes the amount of work done (by the CPU as well as the GPU) during rendering.</span></span>

<span data-ttu-id="0153b-486">[**Graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 需要特定的呈現狀態和狀態值，才能啟用或停用 z 測試。</span><span class="sxs-lookup"><span data-stu-id="0153b-486">[**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) requires a particular render state and a state value to enable or disable z-testing.</span></span> <span data-ttu-id="0153b-487">特定狀態值會在執行時間評估，以判斷需要多少工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-487">The particular state value is evaluated at runtime to determine how much work is necessary.</span></span> <span data-ttu-id="0153b-488">很難在轉譯迴圈中測量這項狀態變更，但仍會預先先決條件管線狀態，使其切換。</span><span class="sxs-lookup"><span data-stu-id="0153b-488">It is difficult to measure this state change in a render loop and still precondition the pipeline state so that it switches.</span></span> <span data-ttu-id="0153b-489">唯一的解決方法是在轉譯順序期間切換狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-489">The only solution is to toggle the state change during the render sequence.</span></span>

<span data-ttu-id="0153b-490">例如，程式碼剖析技術需要重複兩次，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0153b-490">For example, the profiling technique needs to be repeated twice as follows:</span></span>

1.  <span data-ttu-id="0153b-491">從分析 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 轉譯順序開始著手。</span><span class="sxs-lookup"><span data-stu-id="0153b-491">Start by profiling the [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) render sequence.</span></span> <span data-ttu-id="0153b-492">將基準稱為此。</span><span class="sxs-lookup"><span data-stu-id="0153b-492">Call this the baseline.</span></span>
2.  <span data-ttu-id="0153b-493">分析可切換狀態變更的第二個轉譯順序。</span><span class="sxs-lookup"><span data-stu-id="0153b-493">Profile a second render sequence that toggles the state change.</span></span> <span data-ttu-id="0153b-494">轉譯順序迴圈包含：</span><span class="sxs-lookup"><span data-stu-id="0153b-494">The render sequence loop contains:</span></span>
    -   <span data-ttu-id="0153b-495">將狀態變更為 "false" 條件的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-495">A state change to set the state into a "false" condition.</span></span>
    -   <span data-ttu-id="0153b-496">[**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 就像原始順序一樣。</span><span class="sxs-lookup"><span data-stu-id="0153b-496">[**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) just like the original sequence.</span></span>
    -   <span data-ttu-id="0153b-497">將狀態變更為「true」條件的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-497">A state change to set the state into a "true" condition.</span></span>
    -   <span data-ttu-id="0153b-498">第二個 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ，以強制實現第二個狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-498">A second [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) to force the second state change to be realized.</span></span>
3.  <span data-ttu-id="0153b-499">找出這兩個轉譯序列之間的差異。</span><span class="sxs-lookup"><span data-stu-id="0153b-499">Find the difference between the two render sequences.</span></span> <span data-ttu-id="0153b-500">這是透過下列方式完成：</span><span class="sxs-lookup"><span data-stu-id="0153b-500">This is done by:</span></span>
    -   <span data-ttu-id="0153b-501">將基準 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 序列乘以2，因為新序列中有兩個 **DrawPrimitive** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-501">Multiply the baseline [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sequence by 2 because there are two **DrawPrimitive** calls in the new sequence.</span></span>
    -   <span data-ttu-id="0153b-502">從原始序列減去新序列的結果。</span><span class="sxs-lookup"><span data-stu-id="0153b-502">Subtract the result of the new sequence from the original sequence.</span></span>
    -   <span data-ttu-id="0153b-503">將結果除以2，以取得「false」和「true」狀態變更的平均成本。</span><span class="sxs-lookup"><span data-stu-id="0153b-503">Divide the result by 2 to get the average cost of both the "false" and the "true" state change.</span></span>

<span data-ttu-id="0153b-504">使用轉譯順序中所使用的迴圈技術時，需要測量變更管線狀態的成本，方法是將狀態從 "true" 切換為 "false" 條件，反之亦然，則針對轉譯順序中的每個反復專案。</span><span class="sxs-lookup"><span data-stu-id="0153b-504">With the looping technique used in the render sequence, the cost of changing pipeline state needs to be measured by toggling the state from a "true" to a "false" condition and vice versa, for each iteration in the render sequence.</span></span> <span data-ttu-id="0153b-505">"True" 和 "false" 的意義不是常值，這只是表示必須將狀態設定為相反的條件。</span><span class="sxs-lookup"><span data-stu-id="0153b-505">The meaning of "true" and "false" here are not literal, this simply means that the state needs to be set into opposing conditions.</span></span> <span data-ttu-id="0153b-506">這會導致在分析期間測量狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-506">This causes both state changes to be measured during profiling.</span></span> <span data-ttu-id="0153b-507">當然，您已瞭解如何使用查詢機制，並將轉譯順序放在迴圈中，以避免模式轉換的成本仍適用。</span><span class="sxs-lookup"><span data-stu-id="0153b-507">Of course everything you have learned about using the query mechanism and putting the render sequence in a loop to negate the cost of the mode transition still applies.</span></span>

<span data-ttu-id="0153b-508">例如，以下是用來測量切換 z 測試開關成本的程式碼序列：</span><span class="sxs-lookup"><span data-stu-id="0153b-508">For example, here is the code sequence for measuring the cost of toggling z-testing on or off:</span></span>


```
// Get the start counter value as shown in Example 4 

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the "false" condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Set the pipeline state to the "true" condition
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}

// Get the stop counter value as shown in Example 4 
```



<span data-ttu-id="0153b-509">範例5：測量切換狀態變更</span><span class="sxs-lookup"><span data-stu-id="0153b-509">Example 5: Measuring a Toggling State Change</span></span>

<span data-ttu-id="0153b-510">迴圈會執行兩個 [**graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 呼叫來切換狀態。</span><span class="sxs-lookup"><span data-stu-id="0153b-510">The loop toggles the state by executing two [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) calls.</span></span> <span data-ttu-id="0153b-511">第一個 **graphicsdevice** 呼叫會停用 z 測試，而第二個 **graphicsdevice** 則啟用 z 測試。</span><span class="sxs-lookup"><span data-stu-id="0153b-511">The first **SetRenderState** call disables z-testing and the second **SetRenderState** enables z-testing.</span></span> <span data-ttu-id="0153b-512">每個 **graphicsdevice** 後面都會接著 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ，如此一來，與狀態變更相關聯的工作就會由驅動程式處理，而不是只在驅動程式中設定中途的位。</span><span class="sxs-lookup"><span data-stu-id="0153b-512">Each **SetRenderState** is followed by [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) so that the work associated with the state change is processed by the driver instead of only setting a dirty bit in the driver.</span></span>

<span data-ttu-id="0153b-513">這些數位對此轉譯順序而言是合理的：</span><span class="sxs-lookup"><span data-stu-id="0153b-513">These numbers are reasonable for this render sequence:</span></span>



| <span data-ttu-id="0153b-514">區域變數</span><span class="sxs-lookup"><span data-stu-id="0153b-514">Local Variable</span></span> | <span data-ttu-id="0153b-515">刻度數目</span><span class="sxs-lookup"><span data-stu-id="0153b-515">Number of Ticks</span></span> |
|----------------|-----------------|
| <span data-ttu-id="0153b-516">start</span><span class="sxs-lookup"><span data-stu-id="0153b-516">start</span></span>          | <span data-ttu-id="0153b-517">1792998845000</span><span class="sxs-lookup"><span data-stu-id="0153b-517">1792998845000</span></span>   |
| <span data-ttu-id="0153b-518">stop</span><span class="sxs-lookup"><span data-stu-id="0153b-518">stop</span></span>           | <span data-ttu-id="0153b-519">1792998861740</span><span class="sxs-lookup"><span data-stu-id="0153b-519">1792998861740</span></span>   |
| <span data-ttu-id="0153b-520">頻率</span><span class="sxs-lookup"><span data-stu-id="0153b-520">freq</span></span>           | <span data-ttu-id="0153b-521">3579545</span><span class="sxs-lookup"><span data-stu-id="0153b-521">3579545</span></span>         |



 

<span data-ttu-id="0153b-522">再次將刻度轉換成迴圈會產生：</span><span class="sxs-lookup"><span data-stu-id="0153b-522">Converting ticks to cycles once again yields:</span></span>


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



<span data-ttu-id="0153b-523">除以迴圈中的反覆運算次數會產生：</span><span class="sxs-lookup"><span data-stu-id="0153b-523">Dividing by the number of iterations in the loop yields:</span></span>


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



<span data-ttu-id="0153b-524">迴圈的每個反復專案都包含兩個狀態變更和兩個繪製呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-524">Each iteration of the loop contains two state changes and two draw calls.</span></span> <span data-ttu-id="0153b-525">將繪製呼叫減去 (假設1100迴圈) 離開：</span><span class="sxs-lookup"><span data-stu-id="0153b-525">Subtracting out the draw calls (assuming 1100 cycles) leaves:</span></span>


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



<span data-ttu-id="0153b-526">這是兩個狀態變更的平均週期數目，因此每個狀態變更的平均時間為：</span><span class="sxs-lookup"><span data-stu-id="0153b-526">This is the average number of cycles for both state changes so the average time for each state change is:</span></span>


```
4000 / 2  = 2000 cycles for each state change
```



<span data-ttu-id="0153b-527">因此，啟用或停用 z 測試的平均迴圈數目是2000週期。</span><span class="sxs-lookup"><span data-stu-id="0153b-527">Therefore, the average number of cycles to enable or disable z-testing is 2000 cycles.</span></span> <span data-ttu-id="0153b-528">值得注意的是，QueryPerformanceCounter 測量的是 z-啟用一半的時間和 z 停用半時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-528">It is worth noting that QueryPerformanceCounter is measuring z-enable half the time and z-disable half of the time.</span></span> <span data-ttu-id="0153b-529">這項技術實際上會測量兩個狀態變更的平均值。</span><span class="sxs-lookup"><span data-stu-id="0153b-529">This technique actually measures the average of both state changes.</span></span> <span data-ttu-id="0153b-530">換句話說，您會測量切換狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-530">In other words, you are measuring the time to toggle a state.</span></span> <span data-ttu-id="0153b-531">使用這項技術，您就無法得知啟用和停用時間是否相等，因為您已測量兩者的平均值。</span><span class="sxs-lookup"><span data-stu-id="0153b-531">Using this technique, you have no way of knowing if the enable and disable times are equivalent since you have measured the average of both of them.</span></span> <span data-ttu-id="0153b-532">不過，這是合理的數位，可在將切換狀態的預算設為應用程式時使用，而此狀態變更只會切換此狀態來執行此作業。</span><span class="sxs-lookup"><span data-stu-id="0153b-532">Nevertheless, this is a reasonable number to use when budgeting a toggling state as an application that causes this state change can only do so by toggling this state.</span></span>

<span data-ttu-id="0153b-533">現在您可以套用這些技術，並分析所有您想要的狀態變更，對吧？</span><span class="sxs-lookup"><span data-stu-id="0153b-533">So now you can apply these techniques and profile all the state changes you want, right?</span></span> <span data-ttu-id="0153b-534">並不全是。</span><span class="sxs-lookup"><span data-stu-id="0153b-534">Not quite.</span></span> <span data-ttu-id="0153b-535">您仍然需要特別小心，其設計目的是要減少需要完成的工作量。</span><span class="sxs-lookup"><span data-stu-id="0153b-535">You still need to be careful about optimizations that are designed to reduce the amount of work that needs to be done.</span></span> <span data-ttu-id="0153b-536">設計轉譯順序時，您應該注意兩種類型的優化。</span><span class="sxs-lookup"><span data-stu-id="0153b-536">There are two types of optimizations that you should be aware of when designing your render sequences.</span></span>

### <a name="watch-out-for-state-change-optimizations"></a><span data-ttu-id="0153b-537">留意狀態變更優化</span><span class="sxs-lookup"><span data-stu-id="0153b-537">Watch Out for State Change Optimizations</span></span>

<span data-ttu-id="0153b-538">上一節示範如何分析這兩種狀態變更：限制為每個反復專案產生相同工作量的簡單狀態變更，以及會大幅變更已完成工作量的切換狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-538">The previous section show how to profile both kinds of state changes: a simple state change that is constrained to generate the same amount of work for each iteration, and a toggling state change that dramatically changes the amount of work done.</span></span> <span data-ttu-id="0153b-539">如果您採用先前的轉譯順序，並新增另一個狀態變更，會發生什麼事？</span><span class="sxs-lookup"><span data-stu-id="0153b-539">What happens if you take the previous render sequence and add another state change to it?</span></span> <span data-ttu-id="0153b-540">比方說，這個範例會採用 z> 啟用轉譯順序，並對其新增 z func 比較：</span><span class="sxs-lookup"><span data-stu-id="0153b-540">For instance, this example takes the z>-enable render sequence and adds a z-func comparison to it:</span></span>


```
// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZFUNC, D3DCMP_NEVER);

  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZFUNC, D3DCMP_ALWAYS);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}
```



<span data-ttu-id="0153b-541">當寫入至 z 緩衝區時，z-func 狀態會設定比較層級，在目前圖元的 z-值與深度緩衝區) 中圖元的 z 值之間 (之間。</span><span class="sxs-lookup"><span data-stu-id="0153b-541">The z-func state sets the comparison level when writing to the z-buffer (between the z-value of a current pixel with the z-value of a pixel in the depth buffer).</span></span> <span data-ttu-id="0153b-542">D3DCMP \_ 絕對不會關閉 z 測試比較，D3DCMP \_ 一律會設定每次完成 z 測試時所發生的比較。</span><span class="sxs-lookup"><span data-stu-id="0153b-542">D3DCMP\_NEVER turns off the z-testing comparison while D3DCMP\_ALWAYS sets the comparison to happen every time z-testing is done.</span></span>

<span data-ttu-id="0153b-543">使用 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 來分析轉譯順序中的其中一個狀態變更，會產生類似以下的結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-543">Profiling either one of these state changes in a render sequence with [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) generates results similar to these:</span></span>



| <span data-ttu-id="0153b-544">單一狀態變更</span><span class="sxs-lookup"><span data-stu-id="0153b-544">Single State Change</span></span> | <span data-ttu-id="0153b-545">平均週期數</span><span class="sxs-lookup"><span data-stu-id="0153b-545">Average Number of Cycles</span></span> |
|---------------------|--------------------------|
| <span data-ttu-id="0153b-546">\_僅限 D3DRS ZENABLE</span><span class="sxs-lookup"><span data-stu-id="0153b-546">D3DRS\_ZENABLE only</span></span> | <span data-ttu-id="0153b-547">2000</span><span class="sxs-lookup"><span data-stu-id="0153b-547">2000</span></span>                     |



 

<span data-ttu-id="0153b-548">或</span><span class="sxs-lookup"><span data-stu-id="0153b-548">or</span></span>



| <span data-ttu-id="0153b-549">單一狀態變更</span><span class="sxs-lookup"><span data-stu-id="0153b-549">Single State Change</span></span> | <span data-ttu-id="0153b-550">平均週期數</span><span class="sxs-lookup"><span data-stu-id="0153b-550">Average Number of Cycles</span></span> |
|---------------------|--------------------------|
| <span data-ttu-id="0153b-551">\_僅限 D3DRS ZFUNC</span><span class="sxs-lookup"><span data-stu-id="0153b-551">D3DRS\_ZFUNC only</span></span>   | <span data-ttu-id="0153b-552">600</span><span class="sxs-lookup"><span data-stu-id="0153b-552">600</span></span>                      |



 

<span data-ttu-id="0153b-553">但是，如果您 \_ 在相同轉譯順序中同時分析 D3DRS ZENABLE 和 D3DRS \_ ZFUNC，您可能會看到如下所示的結果：</span><span class="sxs-lookup"><span data-stu-id="0153b-553">But, if you profile both D3DRS\_ZENABLE and D3DRS\_ZFUNC in the same render sequence you could see results like these:</span></span>



| <span data-ttu-id="0153b-554">狀態變更</span><span class="sxs-lookup"><span data-stu-id="0153b-554">Both State Changes</span></span>            | <span data-ttu-id="0153b-555">平均週期數</span><span class="sxs-lookup"><span data-stu-id="0153b-555">Average Number of Cycles</span></span> |
|-------------------------------|--------------------------|
| <span data-ttu-id="0153b-556">D3DRS \_ ZENABLE + D3DRS \_ ZFUNC</span><span class="sxs-lookup"><span data-stu-id="0153b-556">D3DRS\_ZENABLE + D3DRS\_ZFUNC</span></span> | <span data-ttu-id="0153b-557">2000</span><span class="sxs-lookup"><span data-stu-id="0153b-557">2000</span></span>                     |



 

<span data-ttu-id="0153b-558">您可能預期結果會是2000和 600 (或 2600) 迴圈的總和，因為驅動程式正在執行所有與設定這兩種轉譯狀態相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-558">You could expect the result to be to be the sum of 2000 and 600 (or 2600) cycles because the driver is doing all the work associated with setting both render states.</span></span> <span data-ttu-id="0153b-559">相反地，平均是2000週期。</span><span class="sxs-lookup"><span data-stu-id="0153b-559">Instead, the average is 2000 cycles.</span></span>

<span data-ttu-id="0153b-560">此結果反映在執行時間、驅動程式或 GPU 中實作為狀態變更優化。</span><span class="sxs-lookup"><span data-stu-id="0153b-560">This result reflects a state change optimization implemented in the runtime, the driver, or the GPU.</span></span> <span data-ttu-id="0153b-561">在此情況下，驅動程式可能會看到第一個 [**graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 並設定變更狀態，以在稍後延遲工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-561">In this case, the driver could see the first [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) and set a dirty state which would postpone the work until later.</span></span> <span data-ttu-id="0153b-562">當驅動程式看到第二個 **graphicsdevice** 時，相同的變更狀態可能是重複設定的，而且相同的工作也會再次延後。</span><span class="sxs-lookup"><span data-stu-id="0153b-562">When the driver sees the second **SetRenderState**, the same dirty state could be redundantly set and the same work would be postponed once again.</span></span> <span data-ttu-id="0153b-563">呼叫 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 時，最後會處理與已變更狀態相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-563">When [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) is called, the work associated with the dirty state is finally processed.</span></span> <span data-ttu-id="0153b-564">驅動程式會執行工作一次，這表示驅動程式會將前兩個狀態變更有效地合併。</span><span class="sxs-lookup"><span data-stu-id="0153b-564">The driver executes the work one time, which means that the first two state changes are effectively consolidated by the driver.</span></span> <span data-ttu-id="0153b-565">同樣地，當呼叫第二個 **DrawPrimitive** 時，驅動程式會將第三個和第四個狀態變更有效地合併為單一狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-565">Similarly, the third and fourth state changes are effectively consolidated by the driver into a single state change when the second **DrawPrimitive** is called.</span></span> <span data-ttu-id="0153b-566">最後的結果是，驅動程式和 GPU 會處理每個繪製呼叫的單一狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-566">The net result is that the driver and the GPU process a single state change for each draw call.</span></span>

<span data-ttu-id="0153b-567">這是與序列相依的驅動程式優化的良好範例。</span><span class="sxs-lookup"><span data-stu-id="0153b-567">This is a good example of a sequence-dependent driver optimization.</span></span> <span data-ttu-id="0153b-568">驅動程式會藉由設定中途狀態進行延遲兩次，然後執行一次工作以清除變更狀態。</span><span class="sxs-lookup"><span data-stu-id="0153b-568">The driver postponed work twice by setting a dirty state, and then performed the work once to clear the dirty state.</span></span> <span data-ttu-id="0153b-569">這是一個很好的範例，可在工作延遲到絕對必要時進行。</span><span class="sxs-lookup"><span data-stu-id="0153b-569">This is a good example of the kind of efficiency improvement that can take place when work is deferred until absolutely necessary.</span></span>

<span data-ttu-id="0153b-570">您如何知道哪些狀態變更會在內部設定變更狀態，因而將工作延後到稍後為止？</span><span class="sxs-lookup"><span data-stu-id="0153b-570">How do you know which state changes set a dirty state internally and therefore postpone work until later?</span></span> <span data-ttu-id="0153b-571">只有透過測試轉譯順序 (或與驅動程式寫入器) 交談。</span><span class="sxs-lookup"><span data-stu-id="0153b-571">Only by testing render sequences (or talking to driver writers).</span></span> <span data-ttu-id="0153b-572">驅動程式會定期更新和改進，因此優化清單不是靜態的。</span><span class="sxs-lookup"><span data-stu-id="0153b-572">Drivers are updated and improved periodically so the list of optimizations is not static.</span></span> <span data-ttu-id="0153b-573">在一組特定的硬體上，有一個絕對知道特定轉譯順序中狀態變更成本的方式，也就是測量它。</span><span class="sxs-lookup"><span data-stu-id="0153b-573">There is only one way to absolutely know what a state change costs in a given render sequence, on a particular set of hardware; and that is to measure it.</span></span>

### <a name="watch-out-for-drawprimitive-optimizations"></a><span data-ttu-id="0153b-574">留意 DrawPrimitive 優化</span><span class="sxs-lookup"><span data-stu-id="0153b-574">Watch Out for DrawPrimitive Optimizations</span></span>

<span data-ttu-id="0153b-575">除了狀態變更優化之外，執行時間會嘗試將驅動程式必須處理的繪圖呼叫數目優化。</span><span class="sxs-lookup"><span data-stu-id="0153b-575">In addition to state change optimizations, the runtime will attempt to optimize the number of draw calls that the driver has to process.</span></span> <span data-ttu-id="0153b-576">例如，請將這些回送回 draw 呼叫：</span><span class="sxs-lookup"><span data-stu-id="0153b-576">For example, consider these back to back draw calls:</span></span>


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



<span data-ttu-id="0153b-577">範例5a：兩個繪製呼叫</span><span class="sxs-lookup"><span data-stu-id="0153b-577">Example 5a: Two Draw Calls</span></span>

<span data-ttu-id="0153b-578">此序列包含兩個繪製呼叫，而執行時間會合並成單一呼叫，相當於：</span><span class="sxs-lookup"><span data-stu-id="0153b-578">This sequence contains two draw calls, which the runtime will consolidate into a single call equivalent to:</span></span>


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



<span data-ttu-id="0153b-579">範例5b：單一串連的繪製呼叫</span><span class="sxs-lookup"><span data-stu-id="0153b-579">Example 5b: A Single Concatenated Draw Call</span></span>

<span data-ttu-id="0153b-580">執行時間會將這兩個特定的繪製呼叫串連成單一呼叫，這會減少驅動程式的50%，因為驅動程式現在只需要處理一次繪製呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-580">The runtime will concatenate both of these particular draw calls into a single call, which reduces the driver work by 50 percent because the driver will now only need to process one draw call.</span></span>

<span data-ttu-id="0153b-581">一般而言，執行時間會串連兩個或多個後端 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 呼叫：</span><span class="sxs-lookup"><span data-stu-id="0153b-581">In general, the runtime will concatenate two or more back-to-back [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) calls when:</span></span>

1.  <span data-ttu-id="0153b-582">基本類型是 (D3DPT TRIANGLELIST) 的三角形清單 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0153b-582">The primitive type is a triangle list (D3DPT\_TRIANGLELIST).</span></span>
2.  <span data-ttu-id="0153b-583">每個後續的 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 呼叫都必須參考頂點緩衝區內的連續頂點。</span><span class="sxs-lookup"><span data-stu-id="0153b-583">Each successive [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) call must reference consecutive vertices within the vertex buffer.</span></span>

<span data-ttu-id="0153b-584">同樣地，串連兩個或多個反向 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 呼叫的正確條件如下：</span><span class="sxs-lookup"><span data-stu-id="0153b-584">Similarly, the right conditions for concatenating two or more back-to-back [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) calls are:</span></span>

1.  <span data-ttu-id="0153b-585">基本類型是 (D3DPT TRIANGLELIST) 的三角形清單 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0153b-585">The primitive type is a triangle list (D3DPT\_TRIANGLELIST).</span></span>
2.  <span data-ttu-id="0153b-586">每個後續的 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 呼叫都必須連續參考索引緩衝區內的連續索引。</span><span class="sxs-lookup"><span data-stu-id="0153b-586">Each successive [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) call must sequential reference consecutive indices within the index buffer.</span></span>
3.  <span data-ttu-id="0153b-587">每個後續的 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 呼叫都必須使用相同的 BaseVertexIndex 值。</span><span class="sxs-lookup"><span data-stu-id="0153b-587">Each successive [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) call must use the same value for BaseVertexIndex.</span></span>

<span data-ttu-id="0153b-588">若要在分析期間防止串連，請修改轉譯順序，讓基本型別不是三角形清單，或修改轉譯順序，如此一來，就不會使用連續頂點 (或索引) 的反向繪製呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-588">To prevent concatenation during profiling, modify the render sequence so that the primitive type is not a triangle list, or modify the render sequence so that there are no back-to-back draw calls that use consecutive vertices (or indices).</span></span> <span data-ttu-id="0153b-589">更具體來說，執行時間也會串連符合下列兩個條件的繪製呼叫：</span><span class="sxs-lookup"><span data-stu-id="0153b-589">More specifically, the runtime will also concatenate draw calls that meet both of the following conditions:</span></span>

-   <span data-ttu-id="0153b-590">當先前的呼叫 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)時，如果下一個繪製呼叫：</span><span class="sxs-lookup"><span data-stu-id="0153b-590">When the previous call is [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), if the next draw call:</span></span>
    -   <span data-ttu-id="0153b-591">使用三角形清單，以及</span><span class="sxs-lookup"><span data-stu-id="0153b-591">uses a triangle list, AND</span></span>
    -   <span data-ttu-id="0153b-592">指定 StartVertex = previous StartVertex + previous PrimitiveCount \* 3</span><span class="sxs-lookup"><span data-stu-id="0153b-592">specifies the StartVertex = previous StartVertex + previous PrimitiveCount \* 3</span></span>
-   <span data-ttu-id="0153b-593">使用 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)時，如果下一次繪製呼叫：</span><span class="sxs-lookup"><span data-stu-id="0153b-593">When using [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive), if the next draw call:</span></span>
    -   <span data-ttu-id="0153b-594">使用三角形清單，以及</span><span class="sxs-lookup"><span data-stu-id="0153b-594">uses a triangle list, AND</span></span>
    -   <span data-ttu-id="0153b-595">指定 StartIndex = 上一個 StartIndex + 先前的 PrimitiveCount \* 3，以及</span><span class="sxs-lookup"><span data-stu-id="0153b-595">specifies the StartIndex = previous StartIndex + previous PrimitiveCount \* 3, AND</span></span>
    -   <span data-ttu-id="0153b-596">指定 BaseVertexIndex = previous BaseVertexIndex</span><span class="sxs-lookup"><span data-stu-id="0153b-596">specifies the BaseVertexIndex = previous BaseVertexIndex</span></span>

<span data-ttu-id="0153b-597">以下是更微妙的繪製呼叫串連範例，在分析時很容易忽略。</span><span class="sxs-lookup"><span data-stu-id="0153b-597">Here is a more subtle example of draw call concatenation that is easy to overlook when you are profiling.</span></span> <span data-ttu-id="0153b-598">假設呈現順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="0153b-598">Assume the render sequence looks like this:</span></span>


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



<span data-ttu-id="0153b-599">範例5c：一個狀態變更和一個繪製呼叫</span><span class="sxs-lookup"><span data-stu-id="0153b-599">Example 5c: One State Change and One Draw Call</span></span>

<span data-ttu-id="0153b-600">迴圈會逐一查看1500三角形、設定材質和繪製每個三角形。</span><span class="sxs-lookup"><span data-stu-id="0153b-600">The loop iterates through 1500 triangles, setting a texture and drawing each triangle.</span></span> <span data-ttu-id="0153b-601">這種轉譯迴圈大約需要2750迴圈來進行 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)的 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)和1100迴圈，如上一節所示。</span><span class="sxs-lookup"><span data-stu-id="0153b-601">This render loop takes approximately 2750 cycles for [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) and 1100 cycles for [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) as shown in previous sections.</span></span> <span data-ttu-id="0153b-602">您可能會認為，在轉譯迴圈外部移動 **SetTexture** 應該會減少驅動程式 1500 2750 週期所完成的工作量 \* ，也就是與呼叫 **SetTexture** 1500 時間相關聯的工作量。</span><span class="sxs-lookup"><span data-stu-id="0153b-602">You might intuitively expect that moving **SetTexture** outside the render loop should reduce the amount of work done by the driver by 1500 \* 2750 cycles, which is the amount of work associated with calling **SetTexture** 1500 times.</span></span> <span data-ttu-id="0153b-603">程式碼片段看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="0153b-603">The code snippet would look like this:</span></span>


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



<span data-ttu-id="0153b-604">範例5d：在迴圈外部具有狀態變更的範例5c</span><span class="sxs-lookup"><span data-stu-id="0153b-604">Example 5d: Example 5c with the State Change Outside the Loop</span></span>

<span data-ttu-id="0153b-605">在轉譯迴圈外部移動 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 可減少與 **SetTexture** 相關聯的工作量，因為它會被呼叫一次，而不是1500次。</span><span class="sxs-lookup"><span data-stu-id="0153b-605">Moving [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) outside the render loop does reduce the amount of work associated with **SetTexture** since it is called once instead of 1500 times.</span></span> <span data-ttu-id="0153b-606">較不明顯的次要效果是， [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 的工作也會從1500呼叫減少為1個呼叫，因為串連繪製呼叫的所有條件都已滿足。</span><span class="sxs-lookup"><span data-stu-id="0153b-606">A less obvious secondary effect is that the work for [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) is also reduced from 1500 calls to 1 call because all of the conditions for concatenating draw calls are satisfied.</span></span> <span data-ttu-id="0153b-607">處理轉譯順序時，執行時間會將1500呼叫處理成單一的驅動程式呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-607">When the render sequence is processed, the runtime will process 1500 calls into a single driver call.</span></span> <span data-ttu-id="0153b-608">藉由移動這一行程式碼，就能大幅降低驅動程式的工作量：</span><span class="sxs-lookup"><span data-stu-id="0153b-608">By moving this one line of code, the amount of driver work has been reduced dramatically:</span></span>


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



<span data-ttu-id="0153b-609">這些結果都是正確的，但在原始問題的內容中非常誤導。</span><span class="sxs-lookup"><span data-stu-id="0153b-609">These results are entirely correct, but are very misleading in the context of the original question.</span></span> <span data-ttu-id="0153b-610">繪製呼叫優化造成大量的驅動程式工作量大幅減少。</span><span class="sxs-lookup"><span data-stu-id="0153b-610">The draw call optimization has caused the amount of driver work to be dramatically reduced.</span></span> <span data-ttu-id="0153b-611">這是執行自訂程式碼剖析時常見的問題。</span><span class="sxs-lookup"><span data-stu-id="0153b-611">This is a common problem when doing custom profiling.</span></span> <span data-ttu-id="0153b-612">從轉譯順序中刪除呼叫時，請小心避免繪製呼叫串連。</span><span class="sxs-lookup"><span data-stu-id="0153b-612">When eliminating calls from a render sequence, be careful to avoid draw call concatenation.</span></span> <span data-ttu-id="0153b-613">事實上，此案例是此執行時間優化可能改善驅動程式效能的強大範例。</span><span class="sxs-lookup"><span data-stu-id="0153b-613">In fact, this scenario is a powerful example of the amount of improvement in driver performance possible by this runtime optimization.</span></span>

<span data-ttu-id="0153b-614">現在您知道如何測量狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0153b-614">So now you know how to measure state changes.</span></span> <span data-ttu-id="0153b-615">從分析 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)開始。</span><span class="sxs-lookup"><span data-stu-id="0153b-615">Start by profiling [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span> <span data-ttu-id="0153b-616">然後，將每個額外的狀態變更新增至順序 (在某些情況下，新增一個呼叫，而在其他情況下，新增兩個呼叫) 並測量兩個序列之間的差異。</span><span class="sxs-lookup"><span data-stu-id="0153b-616">Then add each additional state change to the sequence (in some cases adding one call and in other cases adding two calls) and measure the difference between the two sequences.</span></span> <span data-ttu-id="0153b-617">您可以將結果轉換成刻度或週期或時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-617">You can convert the results to ticks or cycles or time.</span></span> <span data-ttu-id="0153b-618">就像使用 QueryPerformanceCounter 測量轉譯順序一樣，測量個別狀態變更依賴查詢機制來控制命令緩衝區，並將狀態變更放在迴圈中，以將模式轉換的影響降到最低。</span><span class="sxs-lookup"><span data-stu-id="0153b-618">Just like measuring render sequences with QueryPerformanceCounter, measuring individual state changes relies on the query mechanism to control the command buffer, and putting the state changes in a loop to minimize the impact of the mode transitions.</span></span> <span data-ttu-id="0153b-619">這項技術會測量切換狀態的成本，因為分析工具會傳回啟用和停用狀態的平均值。</span><span class="sxs-lookup"><span data-stu-id="0153b-619">This technique measures the cost of toggling a state, since the profiler returns the average of enabling and disabling the state.</span></span>

<span data-ttu-id="0153b-620">有了這項功能，您就可以開始產生任意轉譯順序，並精確地測量相關聯的執行時間和驅動程式工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-620">With this capability, you can start generating arbitrary rendering sequences and accurately measuring the associated runtime and driver work.</span></span> <span data-ttu-id="0153b-621">然後，您可以使用這些數位來回答預算問題，例如「在轉譯順序中有多少以上的呼叫」，同時仍維持合理的畫面播放速率（假設 CPU 有限的案例）。</span><span class="sxs-lookup"><span data-stu-id="0153b-621">The numbers can then be used to answer budgeting questions like "how many more of these calls" can be made in the render sequence while still maintaining a reasonable frame rate, assuming CPU-limited scenarios.</span></span>

## <a name="summary"></a><span data-ttu-id="0153b-622">總結</span><span class="sxs-lookup"><span data-stu-id="0153b-622">Summary</span></span>

<span data-ttu-id="0153b-623">本檔將示範如何控制命令緩衝區，以便能夠正確地分析個別呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-623">This paper demonstrates how to control the command buffer so that individual calls can be accurately profiled.</span></span> <span data-ttu-id="0153b-624">程式碼剖析編號可以依滴答、迴圈或絕對時間產生。</span><span class="sxs-lookup"><span data-stu-id="0153b-624">The profiling numbers can be generated in ticks, cycles, or absolute time.</span></span> <span data-ttu-id="0153b-625">它們代表與每個 API 呼叫相關聯的執行時間和驅動程式工作量。</span><span class="sxs-lookup"><span data-stu-id="0153b-625">They represent the amount of runtime and driver work associated with each API call.</span></span>

<span data-ttu-id="0153b-626">一開始先分析轉譯 \* 順序中的繪製基本呼叫。</span><span class="sxs-lookup"><span data-stu-id="0153b-626">Start by profiling a Draw\*Primitive call in a render sequence.</span></span> <span data-ttu-id="0153b-627">請記住：</span><span class="sxs-lookup"><span data-stu-id="0153b-627">Remember to:</span></span>

1.  <span data-ttu-id="0153b-628">使用 QueryPerformanceCounter 測量每個 API 呼叫的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="0153b-628">Use QueryPerformanceCounter to measure the number of ticks per API call.</span></span> <span data-ttu-id="0153b-629">如果您想要的話，請使用 QueryPerformanceFrequency 將結果轉換為迴圈或時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-629">Use QueryPerformanceFrequency to convert the results to cycles or time if you like.</span></span>
2.  <span data-ttu-id="0153b-630">開始之前，請使用查詢機制清空命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0153b-630">Use the query mechanism to empty the command buffer before starting.</span></span>
3.  <span data-ttu-id="0153b-631">在迴圈中包含轉譯順序，以將模式轉換的影響降至最低。</span><span class="sxs-lookup"><span data-stu-id="0153b-631">Include the render sequence in a loop to minimize the impact of the mode transition.</span></span>
4.  <span data-ttu-id="0153b-632">使用查詢機制來測量 GPU 完成其工作的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-632">Use the query mechanism to measure when the GPU has completed its work.</span></span>
5.  <span data-ttu-id="0153b-633">請留意將對完成的工作量有重大影響的執行時間串連。</span><span class="sxs-lookup"><span data-stu-id="0153b-633">Watch out for runtime concatenation that will have a major impact on the amount of work done.</span></span>

<span data-ttu-id="0153b-634">這可提供您 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 的基準效能，可用於建立。</span><span class="sxs-lookup"><span data-stu-id="0153b-634">This gives you a baseline performance for [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) that can be used to build from.</span></span> <span data-ttu-id="0153b-635">若要分析一個狀態變更，請遵循下列其他秘訣：</span><span class="sxs-lookup"><span data-stu-id="0153b-635">To profile one state change, follow these additional tips:</span></span>

1.  <span data-ttu-id="0153b-636">將狀態變更新增至已知轉譯順序設定檔中的新序列。</span><span class="sxs-lookup"><span data-stu-id="0153b-636">Add the state change to a known render sequence profile the new sequence.</span></span> <span data-ttu-id="0153b-637">由於測試是在迴圈中完成，因此必須將狀態設定為相反的值 (例如啟用和停用實例) 。</span><span class="sxs-lookup"><span data-stu-id="0153b-637">Since the testing is done in a loop, this requires setting the state twice into opposite values (like enable and disable for instance).</span></span>
2.  <span data-ttu-id="0153b-638">比較兩個序列之間的週期時間差異。</span><span class="sxs-lookup"><span data-stu-id="0153b-638">Compare the difference in cycle times between the two sequences.</span></span>
3.  <span data-ttu-id="0153b-639">針對大幅變更管線 (如 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) 的狀態變更，請減少兩個序列之間的差異，以取得狀態變更的時間。</span><span class="sxs-lookup"><span data-stu-id="0153b-639">For state changes that significantly change the pipeline (like [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)), subtract the difference between the two sequences to get the time for state change.</span></span>
4.  <span data-ttu-id="0153b-640">針對大幅變更管線 (的狀態變更，因此需要切換狀態，例如 [**graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) ，請減少轉譯序列和除以2之間的差異。</span><span class="sxs-lookup"><span data-stu-id="0153b-640">For state changes that significantly change the pipeline (and therefore require toggling states like [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)), subtract the difference between the render sequences and divide by 2.</span></span> <span data-ttu-id="0153b-641">這會產生每個狀態變更的平均迴圈數目。</span><span class="sxs-lookup"><span data-stu-id="0153b-641">This will generate the average number of cycles for each state change.</span></span>

<span data-ttu-id="0153b-642">但請小心在分析時造成非預期結果的優化。</span><span class="sxs-lookup"><span data-stu-id="0153b-642">But be careful of optimizations that cause unexpected results when profiling.</span></span> <span data-ttu-id="0153b-643">狀態變更優化可能會設定造成工作延遲的變更狀態。</span><span class="sxs-lookup"><span data-stu-id="0153b-643">State change optimizations may set dirty states which causes work to be deferred.</span></span> <span data-ttu-id="0153b-644">這可能會導致不像預期般直覺的設定檔結果。</span><span class="sxs-lookup"><span data-stu-id="0153b-644">This can cause profile results which are not as intuitive as expected.</span></span> <span data-ttu-id="0153b-645">已串連的繪製呼叫會大幅減少驅動程式工作，這可能會導致誤導的結論。</span><span class="sxs-lookup"><span data-stu-id="0153b-645">Draw calls that are concatenated will dramatically reduce driver work which can lead to misleading conclusions.</span></span> <span data-ttu-id="0153b-646">仔細規劃的轉譯順序可用來防止狀態變更，以及繪製呼叫串連。</span><span class="sxs-lookup"><span data-stu-id="0153b-646">Carefully planned render sequences are used to prevent state change and draw call concatenations from occurring.</span></span> <span data-ttu-id="0153b-647">秘訣是避免在程式碼剖析期間進行優化，讓您產生的數位為合理的預算數位。</span><span class="sxs-lookup"><span data-stu-id="0153b-647">The trick is to prevent the optimizations from happening during profiling so that the numbers you generate are reasonable budgeting numbers.</span></span>

> [!Note]  
> <span data-ttu-id="0153b-648">在沒有查詢機制的情況下，在應用程式中複製此程式碼剖析策略比較困難。</span><span class="sxs-lookup"><span data-stu-id="0153b-648">Duplicating this profiling strategy in an application without the query mechanism is more difficult.</span></span> <span data-ttu-id="0153b-649">在 Direct3D 9 之前，唯一可預測的命令緩衝區方法是鎖定使用中的介面 (例如轉譯目標) 等候，直到 GPU 閒置為止。</span><span class="sxs-lookup"><span data-stu-id="0153b-649">Prior to Direct3D 9 the only predictable way to empty the command buffer is to lock an active surface (such as a render target) to wait until the GPU is idle.</span></span> <span data-ttu-id="0153b-650">這是因為鎖定介面會強制執行時間清空命令緩衝區，以防緩衝區中的任何轉譯命令都應該在鎖定之前更新介面，以及等待 GPU 完成。</span><span class="sxs-lookup"><span data-stu-id="0153b-650">This is because locking a surface forces the runtime to empty the command buffer in case there are any rendering commands in the buffer that should update the surface before it gets locked, in addition to waiting for the GPU to finish.</span></span> <span data-ttu-id="0153b-651">這項技術可正常運作，但使用 Direct3D 9 所引進的查詢機制更內斂。</span><span class="sxs-lookup"><span data-stu-id="0153b-651">This technique is functional, although it is more obtrusive that using the query mechanism introduced in Direct3D 9.</span></span>

 

## <a name="appendix"></a><span data-ttu-id="0153b-652">附錄</span><span class="sxs-lookup"><span data-stu-id="0153b-652">Appendix</span></span>

<span data-ttu-id="0153b-653">這份表格中的數位是與每個狀態變更相關聯的執行時間和驅動程式工作量的範圍。</span><span class="sxs-lookup"><span data-stu-id="0153b-653">The numbers in this table are a range of approximations for the amount of runtime and driver work associated with each of these state changes.</span></span> <span data-ttu-id="0153b-654">近似值是根據使用紙張中所示技術在驅動程式上進行的實際度量。</span><span class="sxs-lookup"><span data-stu-id="0153b-654">The approximations are based on actual measurements made on drivers using the techniques shown in the paper.</span></span> <span data-ttu-id="0153b-655">這些數位是使用 Direct3D 9 執行時間產生的，而且與驅動程式相依。</span><span class="sxs-lookup"><span data-stu-id="0153b-655">These numbers were generated using the Direct3D 9 runtime and are driver-dependent.</span></span>

<span data-ttu-id="0153b-656">這份檔中的技術是設計來測量執行時間和驅動程式的工作。</span><span class="sxs-lookup"><span data-stu-id="0153b-656">The techniques in this paper are designed to measure runtime and driver work.</span></span> <span data-ttu-id="0153b-657">一般情況下，在每個應用程式中提供符合 CPU 和 GPU 效能的結果是不切實際的，因為這需要一組完整的轉譯順序。</span><span class="sxs-lookup"><span data-stu-id="0153b-657">In general, it is impractical to provide results that match the performance of the CPU and the GPU in every application as this would require an exhaustive array of render sequences.</span></span> <span data-ttu-id="0153b-658">此外，您也很難對 GPU 的效能進行基準測試，因為它在轉譯順序之前，會高度依賴管線中的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="0153b-658">In addition, it is particularly difficult to benchmark performance of the GPU because it is highly dependent on the state setup in the pipeline before the render sequence.</span></span> <span data-ttu-id="0153b-659">例如，啟用 Alpha 混合幾乎不會影響所需的 CPU 工作量，但可能對 GPU 所完成的工作量有很大的影響。</span><span class="sxs-lookup"><span data-stu-id="0153b-659">For instance, enabling alpha blending does little to affect the amount of CPU work necessary, but can have a big impact on the amount of work done by the GPU.</span></span> <span data-ttu-id="0153b-660">因此，本文中的技術會限制需要轉譯的資料量，以將 GPU 工作限制為最小數量。</span><span class="sxs-lookup"><span data-stu-id="0153b-660">Therefore, the techniques in this paper constrain the GPU work to the minimum amount possible by limiting the amount of data that needs to be rendered.</span></span> <span data-ttu-id="0153b-661">這表示，資料表中的數位最符合 CPU 限制 (的應用程式所能達到的結果，而不是 GPU) 所限制的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0153b-661">This means that the numbers in the table will most closely match the results attained from applications that are CPU limited (as opposed to an application that is limited by the GPU).</span></span>

<span data-ttu-id="0153b-662">建議您使用所呈現的技巧，來涵蓋最重要的案例和設定。</span><span class="sxs-lookup"><span data-stu-id="0153b-662">You are encouraged to use the techniques presented to cover the scenarios and configurations most important to you.</span></span> <span data-ttu-id="0153b-663">資料表中的值可以用來與您產生的數位進行比較。</span><span class="sxs-lookup"><span data-stu-id="0153b-663">The values in the table can be used to compare with the numbers you generate.</span></span> <span data-ttu-id="0153b-664">由於每個驅動程式都有變化，因此產生實際數位的唯一方法就是使用您的案例來產生分析結果。</span><span class="sxs-lookup"><span data-stu-id="0153b-664">Since each driver varies, the only way to generate the actual numbers you will see is to generate profiling results using your scenarios.</span></span>



| <span data-ttu-id="0153b-665">API 呼叫</span><span class="sxs-lookup"><span data-stu-id="0153b-665">API Call</span></span>                             | <span data-ttu-id="0153b-666">平均週期數</span><span class="sxs-lookup"><span data-stu-id="0153b-666">Average number of Cycles</span></span> |
|--------------------------------------|--------------------------|
| <span data-ttu-id="0153b-667">SetVertexDeclaration</span><span class="sxs-lookup"><span data-stu-id="0153b-667">SetVertexDeclaration</span></span>                 | <span data-ttu-id="0153b-668">6500-11250</span><span class="sxs-lookup"><span data-stu-id="0153b-668">6500 - 11250</span></span>             |
| <span data-ttu-id="0153b-669">SetFVF</span><span class="sxs-lookup"><span data-stu-id="0153b-669">SetFVF</span></span>                               | <span data-ttu-id="0153b-670">6400-11200</span><span class="sxs-lookup"><span data-stu-id="0153b-670">6400 - 11200</span></span>             |
| <span data-ttu-id="0153b-671">SetVertexShader</span><span class="sxs-lookup"><span data-stu-id="0153b-671">SetVertexShader</span></span>                      | <span data-ttu-id="0153b-672">3000-12100</span><span class="sxs-lookup"><span data-stu-id="0153b-672">3000 - 12100</span></span>             |
| <span data-ttu-id="0153b-673">SetPixelShader</span><span class="sxs-lookup"><span data-stu-id="0153b-673">SetPixelShader</span></span>                       | <span data-ttu-id="0153b-674">6300-7000</span><span class="sxs-lookup"><span data-stu-id="0153b-674">6300 - 7000</span></span>              |
| <span data-ttu-id="0153b-675">SPECULARENABLE</span><span class="sxs-lookup"><span data-stu-id="0153b-675">SPECULARENABLE</span></span>                       | <span data-ttu-id="0153b-676">1900-11200</span><span class="sxs-lookup"><span data-stu-id="0153b-676">1900 - 11200</span></span>             |
| <span data-ttu-id="0153b-677">SetRenderTarget</span><span class="sxs-lookup"><span data-stu-id="0153b-677">SetRenderTarget</span></span>                      | <span data-ttu-id="0153b-678">6000-6250</span><span class="sxs-lookup"><span data-stu-id="0153b-678">6000 - 6250</span></span>              |
| <span data-ttu-id="0153b-679">SetPixelShaderConstant (1 常數) </span><span class="sxs-lookup"><span data-stu-id="0153b-679">SetPixelShaderConstant (1 Constant)</span></span>  | <span data-ttu-id="0153b-680">1500-9000</span><span class="sxs-lookup"><span data-stu-id="0153b-680">1500 - 9000</span></span>              |
| <span data-ttu-id="0153b-681">NORMALIZENORMALS</span><span class="sxs-lookup"><span data-stu-id="0153b-681">NORMALIZENORMALS</span></span>                     | <span data-ttu-id="0153b-682">2200-8100</span><span class="sxs-lookup"><span data-stu-id="0153b-682">2200 - 8100</span></span>              |
| <span data-ttu-id="0153b-683">LightEnable</span><span class="sxs-lookup"><span data-stu-id="0153b-683">LightEnable</span></span>                          | <span data-ttu-id="0153b-684">1300-9000</span><span class="sxs-lookup"><span data-stu-id="0153b-684">1300 - 9000</span></span>              |
| <span data-ttu-id="0153b-685">SetStreamSource</span><span class="sxs-lookup"><span data-stu-id="0153b-685">SetStreamSource</span></span>                      | <span data-ttu-id="0153b-686">3700-5800</span><span class="sxs-lookup"><span data-stu-id="0153b-686">3700 - 5800</span></span>              |
| <span data-ttu-id="0153b-687">照明</span><span class="sxs-lookup"><span data-stu-id="0153b-687">LIGHTING</span></span>                             | <span data-ttu-id="0153b-688">1700-7500</span><span class="sxs-lookup"><span data-stu-id="0153b-688">1700 - 7500</span></span>              |
| <span data-ttu-id="0153b-689">DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="0153b-689">DIFFUSEMATERIALSOURCE</span></span>                | <span data-ttu-id="0153b-690">900-8300</span><span class="sxs-lookup"><span data-stu-id="0153b-690">900 - 8300</span></span>               |
| <span data-ttu-id="0153b-691">AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="0153b-691">AMBIENTMATERIALSOURCE</span></span>                | <span data-ttu-id="0153b-692">900-8200</span><span class="sxs-lookup"><span data-stu-id="0153b-692">900 - 8200</span></span>               |
| <span data-ttu-id="0153b-693">COLORVERTEX</span><span class="sxs-lookup"><span data-stu-id="0153b-693">COLORVERTEX</span></span>                          | <span data-ttu-id="0153b-694">800-7800</span><span class="sxs-lookup"><span data-stu-id="0153b-694">800 - 7800</span></span>               |
| <span data-ttu-id="0153b-695">SetLight</span><span class="sxs-lookup"><span data-stu-id="0153b-695">SetLight</span></span>                             | <span data-ttu-id="0153b-696">2200-5100</span><span class="sxs-lookup"><span data-stu-id="0153b-696">2200 - 5100</span></span>              |
| <span data-ttu-id="0153b-697">SetTransform</span><span class="sxs-lookup"><span data-stu-id="0153b-697">SetTransform</span></span>                         | <span data-ttu-id="0153b-698">3200-3750</span><span class="sxs-lookup"><span data-stu-id="0153b-698">3200 - 3750</span></span>              |
| <span data-ttu-id="0153b-699">SetIndices</span><span class="sxs-lookup"><span data-stu-id="0153b-699">SetIndices</span></span>                           | <span data-ttu-id="0153b-700">900-5600</span><span class="sxs-lookup"><span data-stu-id="0153b-700">900 - 5600</span></span>               |
| <span data-ttu-id="0153b-701">環境</span><span class="sxs-lookup"><span data-stu-id="0153b-701">AMBIENT</span></span>                              | <span data-ttu-id="0153b-702">1150-4800</span><span class="sxs-lookup"><span data-stu-id="0153b-702">1150 - 4800</span></span>              |
| <span data-ttu-id="0153b-703">SetTexture</span><span class="sxs-lookup"><span data-stu-id="0153b-703">SetTexture</span></span>                           | <span data-ttu-id="0153b-704">2500-3100</span><span class="sxs-lookup"><span data-stu-id="0153b-704">2500 - 3100</span></span>              |
| <span data-ttu-id="0153b-705">SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="0153b-705">SPECULARMATERIALSOURCE</span></span>               | <span data-ttu-id="0153b-706">900-4600</span><span class="sxs-lookup"><span data-stu-id="0153b-706">900 - 4600</span></span>               |
| <span data-ttu-id="0153b-707">EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="0153b-707">EMISSIVEMATERIALSOURCE</span></span>               | <span data-ttu-id="0153b-708">900-4500</span><span class="sxs-lookup"><span data-stu-id="0153b-708">900 - 4500</span></span>               |
| <span data-ttu-id="0153b-709">SetMaterial</span><span class="sxs-lookup"><span data-stu-id="0153b-709">SetMaterial</span></span>                          | <span data-ttu-id="0153b-710">1000-3700</span><span class="sxs-lookup"><span data-stu-id="0153b-710">1000 - 3700</span></span>              |
| <span data-ttu-id="0153b-711">ZENABLE</span><span class="sxs-lookup"><span data-stu-id="0153b-711">ZENABLE</span></span>                              | <span data-ttu-id="0153b-712">700-3900</span><span class="sxs-lookup"><span data-stu-id="0153b-712">700 - 3900</span></span>               |
| <span data-ttu-id="0153b-713">WRAP0</span><span class="sxs-lookup"><span data-stu-id="0153b-713">WRAP0</span></span>                                | <span data-ttu-id="0153b-714">1600-2700</span><span class="sxs-lookup"><span data-stu-id="0153b-714">1600 - 2700</span></span>              |
| <span data-ttu-id="0153b-715">MINFILTER</span><span class="sxs-lookup"><span data-stu-id="0153b-715">MINFILTER</span></span>                            | <span data-ttu-id="0153b-716">1700-2500</span><span class="sxs-lookup"><span data-stu-id="0153b-716">1700 - 2500</span></span>              |
| <span data-ttu-id="0153b-717">MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="0153b-717">MAGFILTER</span></span>                            | <span data-ttu-id="0153b-718">1700-2400</span><span class="sxs-lookup"><span data-stu-id="0153b-718">1700 - 2400</span></span>              |
| <span data-ttu-id="0153b-719">SetVertexShaderConstant (1 常數) </span><span class="sxs-lookup"><span data-stu-id="0153b-719">SetVertexShaderConstant (1 Constant)</span></span> | <span data-ttu-id="0153b-720">1000-2700</span><span class="sxs-lookup"><span data-stu-id="0153b-720">1000 - 2700</span></span>              |
| <span data-ttu-id="0153b-721">COLOROP</span><span class="sxs-lookup"><span data-stu-id="0153b-721">COLOROP</span></span>                              | <span data-ttu-id="0153b-722">1500-2100</span><span class="sxs-lookup"><span data-stu-id="0153b-722">1500 - 2100</span></span>              |
| <span data-ttu-id="0153b-723">COLORARG2</span><span class="sxs-lookup"><span data-stu-id="0153b-723">COLORARG2</span></span>                            | <span data-ttu-id="0153b-724">1300-2000</span><span class="sxs-lookup"><span data-stu-id="0153b-724">1300 - 2000</span></span>              |
| <span data-ttu-id="0153b-725">COLORARG1</span><span class="sxs-lookup"><span data-stu-id="0153b-725">COLORARG1</span></span>                            | <span data-ttu-id="0153b-726">1300-1980</span><span class="sxs-lookup"><span data-stu-id="0153b-726">1300 - 1980</span></span>              |
| <span data-ttu-id="0153b-727">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="0153b-727">CULLMODE</span></span>                             | <span data-ttu-id="0153b-728">500-2570</span><span class="sxs-lookup"><span data-stu-id="0153b-728">500 - 2570</span></span>               |
| <span data-ttu-id="0153b-729">裁剪</span><span class="sxs-lookup"><span data-stu-id="0153b-729">CLIPPING</span></span>                             | <span data-ttu-id="0153b-730">500-2550</span><span class="sxs-lookup"><span data-stu-id="0153b-730">500 - 2550</span></span>               |
| <span data-ttu-id="0153b-731">DrawIndexedPrimitive</span><span class="sxs-lookup"><span data-stu-id="0153b-731">DrawIndexedPrimitive</span></span>                 | <span data-ttu-id="0153b-732">1200-1400</span><span class="sxs-lookup"><span data-stu-id="0153b-732">1200 - 1400</span></span>              |
| <span data-ttu-id="0153b-733">ADDRESSV</span><span class="sxs-lookup"><span data-stu-id="0153b-733">ADDRESSV</span></span>                             | <span data-ttu-id="0153b-734">1090-1500</span><span class="sxs-lookup"><span data-stu-id="0153b-734">1090 - 1500</span></span>              |
| <span data-ttu-id="0153b-735">ADDRESSU</span><span class="sxs-lookup"><span data-stu-id="0153b-735">ADDRESSU</span></span>                             | <span data-ttu-id="0153b-736">1070-1500</span><span class="sxs-lookup"><span data-stu-id="0153b-736">1070 - 1500</span></span>              |
| <span data-ttu-id="0153b-737">DrawPrimitive</span><span class="sxs-lookup"><span data-stu-id="0153b-737">DrawPrimitive</span></span>                        | <span data-ttu-id="0153b-738">1050-1150</span><span class="sxs-lookup"><span data-stu-id="0153b-738">1050 - 1150</span></span>              |
| <span data-ttu-id="0153b-739">SRGBTEXTURE</span><span class="sxs-lookup"><span data-stu-id="0153b-739">SRGBTEXTURE</span></span>                          | <span data-ttu-id="0153b-740">150-1500</span><span class="sxs-lookup"><span data-stu-id="0153b-740">150 - 1500</span></span>               |
| <span data-ttu-id="0153b-741">STENCILMASK</span><span class="sxs-lookup"><span data-stu-id="0153b-741">STENCILMASK</span></span>                          | <span data-ttu-id="0153b-742">570-700</span><span class="sxs-lookup"><span data-stu-id="0153b-742">570 - 700</span></span>                |
| <span data-ttu-id="0153b-743">STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="0153b-743">STENCILZFAIL</span></span>                         | <span data-ttu-id="0153b-744">500-800</span><span class="sxs-lookup"><span data-stu-id="0153b-744">500 - 800</span></span>                |
| <span data-ttu-id="0153b-745">STENCILREF</span><span class="sxs-lookup"><span data-stu-id="0153b-745">STENCILREF</span></span>                           | <span data-ttu-id="0153b-746">550-700</span><span class="sxs-lookup"><span data-stu-id="0153b-746">550 - 700</span></span>                |
| <span data-ttu-id="0153b-747">ALPHABLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="0153b-747">ALPHABLENDENABLE</span></span>                     | <span data-ttu-id="0153b-748">550-700</span><span class="sxs-lookup"><span data-stu-id="0153b-748">550 - 700</span></span>                |
| <span data-ttu-id="0153b-749">STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="0153b-749">STENCILFUNC</span></span>                          | <span data-ttu-id="0153b-750">560-680</span><span class="sxs-lookup"><span data-stu-id="0153b-750">560 - 680</span></span>                |
| <span data-ttu-id="0153b-751">STENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="0153b-751">STENCILWRITEMASK</span></span>                     | <span data-ttu-id="0153b-752">520-700</span><span class="sxs-lookup"><span data-stu-id="0153b-752">520 - 700</span></span>                |
| <span data-ttu-id="0153b-753">STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="0153b-753">STENCILFAIL</span></span>                          | <span data-ttu-id="0153b-754">500-750</span><span class="sxs-lookup"><span data-stu-id="0153b-754">500 - 750</span></span>                |
| <span data-ttu-id="0153b-755">ZFUNC</span><span class="sxs-lookup"><span data-stu-id="0153b-755">ZFUNC</span></span>                                | <span data-ttu-id="0153b-756">510-700</span><span class="sxs-lookup"><span data-stu-id="0153b-756">510 - 700</span></span>                |
| <span data-ttu-id="0153b-757">ZWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="0153b-757">ZWRITEENABLE</span></span>                         | <span data-ttu-id="0153b-758">520-680</span><span class="sxs-lookup"><span data-stu-id="0153b-758">520 - 680</span></span>                |
| <span data-ttu-id="0153b-759">STENCILENABLE</span><span class="sxs-lookup"><span data-stu-id="0153b-759">STENCILENABLE</span></span>                        | <span data-ttu-id="0153b-760">540-650</span><span class="sxs-lookup"><span data-stu-id="0153b-760">540 - 650</span></span>                |
| <span data-ttu-id="0153b-761">STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="0153b-761">STENCILPASS</span></span>                          | <span data-ttu-id="0153b-762">560-630</span><span class="sxs-lookup"><span data-stu-id="0153b-762">560 - 630</span></span>                |
| <span data-ttu-id="0153b-763">SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="0153b-763">SRCBLEND</span></span>                             | <span data-ttu-id="0153b-764">500-685</span><span class="sxs-lookup"><span data-stu-id="0153b-764">500 - 685</span></span>                |
| <span data-ttu-id="0153b-765">雙 \_ 側 \_ StencilMODE</span><span class="sxs-lookup"><span data-stu-id="0153b-765">Two\_Sided\_StencilMODE</span></span>              | <span data-ttu-id="0153b-766">450-590</span><span class="sxs-lookup"><span data-stu-id="0153b-766">450 - 590</span></span>                |
| <span data-ttu-id="0153b-767">ALPHATESTENABLE</span><span class="sxs-lookup"><span data-stu-id="0153b-767">ALPHATESTENABLE</span></span>                      | <span data-ttu-id="0153b-768">470-525</span><span class="sxs-lookup"><span data-stu-id="0153b-768">470 - 525</span></span>                |
| <span data-ttu-id="0153b-769">ALPHAREF</span><span class="sxs-lookup"><span data-stu-id="0153b-769">ALPHAREF</span></span>                             | <span data-ttu-id="0153b-770">460-530</span><span class="sxs-lookup"><span data-stu-id="0153b-770">460 - 530</span></span>                |
| <span data-ttu-id="0153b-771">ALPHAFUNC</span><span class="sxs-lookup"><span data-stu-id="0153b-771">ALPHAFUNC</span></span>                            | <span data-ttu-id="0153b-772">450-540</span><span class="sxs-lookup"><span data-stu-id="0153b-772">450 - 540</span></span>                |
| <span data-ttu-id="0153b-773">DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="0153b-773">DESTBLEND</span></span>                            | <span data-ttu-id="0153b-774">475-510</span><span class="sxs-lookup"><span data-stu-id="0153b-774">475 - 510</span></span>                |
| <span data-ttu-id="0153b-775">COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="0153b-775">COLORWRITEENABLE</span></span>                     | <span data-ttu-id="0153b-776">465-515</span><span class="sxs-lookup"><span data-stu-id="0153b-776">465 - 515</span></span>                |
| <span data-ttu-id="0153b-777">CCW \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="0153b-777">CCW\_STENCILFAIL</span></span>                     | <span data-ttu-id="0153b-778">340-560</span><span class="sxs-lookup"><span data-stu-id="0153b-778">340 - 560</span></span>                |
| <span data-ttu-id="0153b-779">CCW \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="0153b-779">CCW\_STENCILPASS</span></span>                     | <span data-ttu-id="0153b-780">340-545</span><span class="sxs-lookup"><span data-stu-id="0153b-780">340 - 545</span></span>                |
| <span data-ttu-id="0153b-781">CCW \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="0153b-781">CCW\_STENCILZFAIL</span></span>                    | <span data-ttu-id="0153b-782">330-495</span><span class="sxs-lookup"><span data-stu-id="0153b-782">330 - 495</span></span>                |
| <span data-ttu-id="0153b-783">SCISSORTESTENABLE</span><span class="sxs-lookup"><span data-stu-id="0153b-783">SCISSORTESTENABLE</span></span>                    | <span data-ttu-id="0153b-784">375-440</span><span class="sxs-lookup"><span data-stu-id="0153b-784">375 - 440</span></span>                |
| <span data-ttu-id="0153b-785">CCW \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="0153b-785">CCW\_STENCILFUNC</span></span>                     | <span data-ttu-id="0153b-786">250-480</span><span class="sxs-lookup"><span data-stu-id="0153b-786">250 - 480</span></span>                |
| <span data-ttu-id="0153b-787">SetScissorRect</span><span class="sxs-lookup"><span data-stu-id="0153b-787">SetScissorRect</span></span>                       | <span data-ttu-id="0153b-788">150-340</span><span class="sxs-lookup"><span data-stu-id="0153b-788">150 - 340</span></span>                |



 

## <a name="related-topics"></a><span data-ttu-id="0153b-789">相關主題</span><span class="sxs-lookup"><span data-stu-id="0153b-789">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0153b-790">Advanced 主題</span><span class="sxs-lookup"><span data-stu-id="0153b-790">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
