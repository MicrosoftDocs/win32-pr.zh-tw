---
title: 在 Xbox 360 和 Windows 上針對多核心撰寫程式碼
description: 本主題提供一些有關如何開始使用多執行緒程式設計的建議。
ms.assetid: 661f13a6-c73d-8513-2bad-0ef9d1a361a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75899dacdfba829fc1a83e9393e6aa58574c9f30
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383242"
---
# <a name="coding-for-multicore-on-xbox-360-and-windows"></a><span data-ttu-id="ec98c-103">在 Xbox 360 和 Windows 上針對多核心撰寫程式碼</span><span class="sxs-lookup"><span data-stu-id="ec98c-103">Coding for multicore on Xbox 360 and Windows</span></span>

<span data-ttu-id="ec98c-104">多年來，處理器的效能不斷增加，而遊戲和其他程式已 reaped 這種增加的能力，而不需要執行任何特殊動作。</span><span class="sxs-lookup"><span data-stu-id="ec98c-104">For years the performance of processors has increased steadily, and games and other programs have reaped the benefits of this increasing power without having to do anything special.</span></span>

<span data-ttu-id="ec98c-105">規則已變更。</span><span class="sxs-lookup"><span data-stu-id="ec98c-105">The rules have changed.</span></span> <span data-ttu-id="ec98c-106">如果有的話，單處理器核心的效能現在會變得非常緩慢。</span><span class="sxs-lookup"><span data-stu-id="ec98c-106">The performance of single processor cores is now increasing very slowly, if at all.</span></span> <span data-ttu-id="ec98c-107">不過，一般電腦或主控台中提供的運算能力仍會持續成長。</span><span class="sxs-lookup"><span data-stu-id="ec98c-107">However, the computing power available in a typical computer or console continues to grow.</span></span> <span data-ttu-id="ec98c-108">差別在於，大部分的效能提升現在都是在單一機器中具有多個處理器核心，通常是在單一晶片中。</span><span class="sxs-lookup"><span data-stu-id="ec98c-108">The difference is that most of this performance gain now comes from having multiple processor cores in a single machine, often in a single chip.</span></span> <span data-ttu-id="ec98c-109">Xbox 360 CPU 在一個晶片上有三個處理器核心，而2006中所售出的電腦處理器大約70% 是多核心。</span><span class="sxs-lookup"><span data-stu-id="ec98c-109">The Xbox 360 CPU has three processor cores on one chip, and roughly 70 percent of PC processors sold in 2006 were multi-core.</span></span>

<span data-ttu-id="ec98c-110">可用處理能力的增加與過去一樣明顯，但現在開發人員必須撰寫多執行緒程式碼，才能使用此功能。</span><span class="sxs-lookup"><span data-stu-id="ec98c-110">The increases in available processing power are just as dramatic as in the past, but now developers have to write multithreaded code in order to use this power.</span></span> <span data-ttu-id="ec98c-111">多執行緒程式設計帶來了新的設計和程式設計挑戰。</span><span class="sxs-lookup"><span data-stu-id="ec98c-111">Multi-threaded programming brings with it new design and programming challenges.</span></span> <span data-ttu-id="ec98c-112">本主題提供一些有關如何開始使用多執行緒程式設計的建議。</span><span class="sxs-lookup"><span data-stu-id="ec98c-112">This topic gives some advice on how to get started with multithreaded programming.</span></span>

## <a name="the-importance-of-good-design"></a><span data-ttu-id="ec98c-113">良好設計的重要性</span><span class="sxs-lookup"><span data-stu-id="ec98c-113">The Importance of Good Design</span></span>

<span data-ttu-id="ec98c-114">良好的多執行緒程式設計很重要，但可能很困難。</span><span class="sxs-lookup"><span data-stu-id="ec98c-114">Good multithreaded program design is critical, but it can be very difficult.</span></span> <span data-ttu-id="ec98c-115">如果您 haphazardly 將主要遊戲系統移至不同的執行緒，您可能會發現每個執行緒的大部分時間都花費在等候其他執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-115">If you haphazardly move your major game systems onto different threads, you will likely find that each thread spends most of its time waiting on the other threads.</span></span> <span data-ttu-id="ec98c-116">這種類型的設計會導致複雜性和大量的調試工作變得更複雜，幾乎沒有效能提升。</span><span class="sxs-lookup"><span data-stu-id="ec98c-116">This type of design leads to increased complexity and significant debugging effort, with virtually no performance gain.</span></span>

<span data-ttu-id="ec98c-117">每次執行緒必須同步處理或共用資料時，就可能會發生資料損毀、同步處理額外負荷、鎖死和複雜度。</span><span class="sxs-lookup"><span data-stu-id="ec98c-117">Every time that threads have to synchronize or share data there is the potential for data corruption, synchronization overhead, deadlocks, and complexity.</span></span> <span data-ttu-id="ec98c-118">因此，您的多執行緒設計需要清楚地記錄每個同步處理和通訊點，而且應該盡可能將這些點最小化。</span><span class="sxs-lookup"><span data-stu-id="ec98c-118">Therefore, your multithreaded design needs to clearly document every synchronization and communication point, and it should minimize such points as much as possible.</span></span> <span data-ttu-id="ec98c-119">當執行緒需要進行通訊時，程式碼撰寫工作將會增加，如果影響到太多的原始程式碼，則會降低生產力。</span><span class="sxs-lookup"><span data-stu-id="ec98c-119">Where threads need to communicate, coding effort will increase, which can lower productivity if it affects too much source code.</span></span>

<span data-ttu-id="ec98c-120">多執行緒的最簡單設計目標是將程式碼分解成大型的獨立片段。</span><span class="sxs-lookup"><span data-stu-id="ec98c-120">The simplest design goal for multithreading is to break up the code into large independent pieces.</span></span> <span data-ttu-id="ec98c-121">如果您接著將這些部分限制在每個畫面上進行幾次通訊，您就會看到從多執行緒的速度大幅提升，而不會產生過度的複雜性。</span><span class="sxs-lookup"><span data-stu-id="ec98c-121">If you then restrict these pieces to communicating just a few times per frame, you will see significant speedup from multithreading, without undue complexity.</span></span>

## <a name="typical-threaded-tasks"></a><span data-ttu-id="ec98c-122">一般執行緒工作</span><span class="sxs-lookup"><span data-stu-id="ec98c-122">Typical Threaded Tasks</span></span>

<span data-ttu-id="ec98c-123">有幾種類型的工作已證明適合要放在不同的執行緒上。</span><span class="sxs-lookup"><span data-stu-id="ec98c-123">A few types of tasks have proven amenable to being put onto separate threads.</span></span> <span data-ttu-id="ec98c-124">下列清單並非詳盡的，但應該提供一些想法。</span><span class="sxs-lookup"><span data-stu-id="ec98c-124">The following list is not intended to be exhaustive, but should give some ideas.</span></span>

### <a name="rendering"></a><span data-ttu-id="ec98c-125">轉譯</span><span class="sxs-lookup"><span data-stu-id="ec98c-125">Rendering</span></span>

<span data-ttu-id="ec98c-126">轉譯（可能包括將場景圖形（可能是只呼叫 D3D 函式）的工作，通常會有50% 或更多 CPU 時間的帳戶。</span><span class="sxs-lookup"><span data-stu-id="ec98c-126">Rendering — which may include walking the scene graph or, possibly, only calling D3D functions — often accounts for 50 percent or more of CPU time.</span></span> <span data-ttu-id="ec98c-127">因此，將轉譯移至另一個執行緒可能會有很大的好處。</span><span class="sxs-lookup"><span data-stu-id="ec98c-127">Therefore, moving rendering to another thread can have significant benefits.</span></span> <span data-ttu-id="ec98c-128">Update 執行緒可以填入某種轉譯描述緩衝區，讓轉譯執行緒可以處理它。</span><span class="sxs-lookup"><span data-stu-id="ec98c-128">The update thread can fill in some sort of render description buffer, which the rendering thread can then process.</span></span>

<span data-ttu-id="ec98c-129">遊戲更新執行緒在轉譯執行緒之前一律為一個畫面格，這表示它會在畫面上顯示使用者動作之前，採用兩個畫面格。</span><span class="sxs-lookup"><span data-stu-id="ec98c-129">The game update thread is always one frame ahead of the render thread, which means that it takes two frames before user actions show up on the screen.</span></span> <span data-ttu-id="ec98c-130">雖然這樣的延遲可能會造成問題，但是分割工作負載的成長畫面播放速率通常會讓延遲總計保持可接受。</span><span class="sxs-lookup"><span data-stu-id="ec98c-130">Although this increased latency can be a problem, the increased frame rate from splitting up the workload generally keeps the total latency acceptable.</span></span>

<span data-ttu-id="ec98c-131">在大多數情況下，所有轉譯仍會在單一執行緒上進行，但它是與遊戲更新不同的執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-131">In most cases all rendering is still done on a single thread, but it is a different thread from the game update.</span></span>

<span data-ttu-id="ec98c-132">D3DCREATE \_ 多執行緒旗標有時會用來允許在其他執行緒上的單一線程和資源上進行轉譯; 在 Xbox 360 上會忽略此旗標，而您應避免在 Windows 上使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="ec98c-132">The D3DCREATE\_MULTITHREADED flag is sometimes used to allow rendering on one thread and resource creation on other threads; this flag is ignored on Xbox 360, and you should avoid using it on Windows.</span></span> <span data-ttu-id="ec98c-133">在 Windows 上，指定此旗標會強制 D3D 花很長的時間來同步處理，因此會減緩轉譯執行緒的速度。</span><span class="sxs-lookup"><span data-stu-id="ec98c-133">On Windows, specifying this flag forces D3D to spend a significant amount of time on synchronization, thus slowing down the render thread.</span></span>

### <a name="file-decompression"></a><span data-ttu-id="ec98c-134">檔案解壓縮</span><span class="sxs-lookup"><span data-stu-id="ec98c-134">File Decompression</span></span>

<span data-ttu-id="ec98c-135">載入時間一律太長，並將資料串流至記憶體，而不會影響畫面播放速率，可能是一項挑戰。</span><span class="sxs-lookup"><span data-stu-id="ec98c-135">Load times are always too long, and streaming data into memory without affecting the frame rate can be challenging.</span></span> <span data-ttu-id="ec98c-136">如果磁片上的所有資料都是主動壓縮的，則硬碟或光碟的資料傳送速率比較不可能是限制因素。</span><span class="sxs-lookup"><span data-stu-id="ec98c-136">If all data is aggressively compressed on disc, then data transfer speed from the hard drive or optical disc is less likely to be a limiting factor.</span></span> <span data-ttu-id="ec98c-137">在單一執行緒處理器上，通常沒有足夠的處理器時間可進行壓縮，以協助載入時間。</span><span class="sxs-lookup"><span data-stu-id="ec98c-137">On a single-threaded processor, there is usually not enough processor time available for compression to help load times.</span></span> <span data-ttu-id="ec98c-138">不過，在多處理器的系統上，檔案解壓縮會使用其他會浪費的 CPU 週期;它可改善載入時間和串流;它會節省光碟上的空間。</span><span class="sxs-lookup"><span data-stu-id="ec98c-138">On a multiprocessor system, however, file decompression uses CPU cycles that would otherwise be wasted; it improves load times and streaming; and it saves space on the disc.</span></span>

<span data-ttu-id="ec98c-139">請勿使用檔案解壓縮來取代在生產期間應完成的處理。</span><span class="sxs-lookup"><span data-stu-id="ec98c-139">Do not use file decompression as a replacement for processing that should be done during production.</span></span> <span data-ttu-id="ec98c-140">比方說，如果您在層級載入期間投入額外的執行緒來剖析 XML 資料，您就不會使用多執行緒來改善播放程式的體驗。</span><span class="sxs-lookup"><span data-stu-id="ec98c-140">For instance, if you devote an extra thread to parsing XML data during level loading, you are not using multithreading to improve the player's experience.</span></span>

<span data-ttu-id="ec98c-141">使用檔案解壓縮執行緒時，您仍然應該使用非同步檔案 i/o 和大型讀取，以便將資料讀取效率最大化。</span><span class="sxs-lookup"><span data-stu-id="ec98c-141">When using a file decompression thread, you should still use asynchronous file I/O and large reads in order to maximize data-reading efficiency.</span></span>

### <a name="graphics-fluff"></a><span data-ttu-id="ec98c-142">圖形寫錯字</span><span class="sxs-lookup"><span data-stu-id="ec98c-142">Graphics Fluff</span></span>

<span data-ttu-id="ec98c-143">有許多圖形 niceties 可改善遊戲的外觀，但不是絕對必要的。</span><span class="sxs-lookup"><span data-stu-id="ec98c-143">There are many graphical niceties that improve the look of the game but aren't strictly necessary.</span></span> <span data-ttu-id="ec98c-144">這些專案包括 cti 所產生的雲端動畫、軟線和線模擬、程式化、程式性植被指數、更多粒子或非遊戲物理。</span><span class="sxs-lookup"><span data-stu-id="ec98c-144">These include things like procedurally generated cloud animations, cloth and hair simulations, procedural waves, procedural vegetation, more particles, or non-gameplay physics.</span></span>

<span data-ttu-id="ec98c-145">因為這些效果不會影響遊戲，所以它們不會造成複雜的同步處理問題，它們可以在每個框架或較少的時候與其他執行緒進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ec98c-145">Because these effects don't affect gameplay, they don't cause tricky synchronization problems—they can synchronize with the other threads once per frame or less often.</span></span> <span data-ttu-id="ec98c-146">此外，在 Windows 遊戲中，這些效果可以為具有多核心 Cpu 的玩家帶來價值，同時在單一核心電腦上以無訊息方式省略，因此可讓您輕鬆地在各種功能之間進行調整。</span><span class="sxs-lookup"><span data-stu-id="ec98c-146">Additionally, on games for Windows these effects can add value for gamers with multicore CPUs, while silently being omitted on single-core computers, thus giving an easy way of scaling across a wide range of capabilities.</span></span>

### <a name="physics"></a><span data-ttu-id="ec98c-147">物理特性</span><span class="sxs-lookup"><span data-stu-id="ec98c-147">Physics</span></span>

<span data-ttu-id="ec98c-148">物理通常不能放在另一個執行緒上，以與遊戲更新平行執行，因為遊戲更新通常需要立即計算物理計算的結果。</span><span class="sxs-lookup"><span data-stu-id="ec98c-148">Physics often cannot be put onto a separate thread to run in parallel with the game update because the game update usually requires the results of the physics calculations immediately.</span></span> <span data-ttu-id="ec98c-149">多執行緒物理的替代方案是在多個處理器上執行。</span><span class="sxs-lookup"><span data-stu-id="ec98c-149">The alternative for multithreading physics is to run it on multiple processors.</span></span> <span data-ttu-id="ec98c-150">雖然可以完成這項作業，但這是一項複雜的工作，需要經常存取共用資料結構。</span><span class="sxs-lookup"><span data-stu-id="ec98c-150">Although this can be done, it is a complex task requiring frequent access to shared data structures.</span></span> <span data-ttu-id="ec98c-151">如果您可以讓物理工作負載夠低，使其符合主執行緒，您的作業將會比較簡單。</span><span class="sxs-lookup"><span data-stu-id="ec98c-151">If you can keep your physics workload low enough to fit on the main thread, your job will be simpler.</span></span>

<span data-ttu-id="ec98c-152">支援在多個執行緒上執行物理的程式庫可供使用。</span><span class="sxs-lookup"><span data-stu-id="ec98c-152">Libraries that support running physics on multiple threads are available.</span></span> <span data-ttu-id="ec98c-153">不過，這可能會導致問題：當您的遊戲在物理上執行時，它會使用許多執行緒，但其餘的時間則不會使用。</span><span class="sxs-lookup"><span data-stu-id="ec98c-153">However, this can lead to a problem: when your game is running physics, it uses many threads, but the rest of the time it uses few.</span></span> <span data-ttu-id="ec98c-154">在多個執行緒上執行物理將需要定址，如此一來，工作負載就會平均分散在整個框架中。</span><span class="sxs-lookup"><span data-stu-id="ec98c-154">Running physics on multiple threads will require addressing this so that the workload is distributed evenly over the frame.</span></span> <span data-ttu-id="ec98c-155">如果您撰寫多執行緒物理引擎，您必須特別注意所有的資料結構、同步處理點和負載平衡。</span><span class="sxs-lookup"><span data-stu-id="ec98c-155">If you write a multithreaded physics engine, you must pay careful attention to all of your data structures, synchronization points, and load balancing.</span></span>

## <a name="example-multithreaded-designs"></a><span data-ttu-id="ec98c-156">多執行緒設計範例</span><span class="sxs-lookup"><span data-stu-id="ec98c-156">Example Multithreaded Designs</span></span>

<span data-ttu-id="ec98c-157">Windows 遊戲需要在 CPU 核心數目不同的電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="ec98c-157">Games for Windows need to run on computers with different numbers of CPU cores.</span></span> <span data-ttu-id="ec98c-158">大部分的遊戲電腦仍舊只有一個核心，雖然兩核心機器的數目很快就會成長。</span><span class="sxs-lookup"><span data-stu-id="ec98c-158">Most game machines still have only one core, although the number of two-core machines is growing rapidly.</span></span> <span data-ttu-id="ec98c-159">Windows 的典型遊戲可能會將其工作負載分成一個執行緒進行更新和轉譯，以及選擇性的背景工作執行緒來新增額外的功能。</span><span class="sxs-lookup"><span data-stu-id="ec98c-159">A typical game for Windows might break its workload into one thread for update and rendering, with optional worker threads for adding extra functionality.</span></span> <span data-ttu-id="ec98c-160">此外，也可能會使用一些執行檔案 i/o 和網路的背景執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-160">In addition, some background threads for doing file I/O and networking would probably be used.</span></span> <span data-ttu-id="ec98c-161">[圖 1] 顯示執行緒，以及主要的資料傳輸點。</span><span class="sxs-lookup"><span data-stu-id="ec98c-161">Figure 1 shows the threads, together with the main data transfer points.</span></span>

<span data-ttu-id="ec98c-162">**圖1。Windows 遊戲中的執行緒設計**</span><span class="sxs-lookup"><span data-stu-id="ec98c-162">**Figure 1. Threading design in a game for Windows**</span></span>

![windows 遊戲中的執行緒設計](images/coding-for-multiple-cores-1.gif)

<span data-ttu-id="ec98c-164">一般的 Xbox 360 遊戲可以使用額外的 CPU 密集軟體執行緒，因此它可能會將其工作負載分解為更新執行緒、轉譯執行緒和三個背景工作執行緒，如圖2所示。</span><span class="sxs-lookup"><span data-stu-id="ec98c-164">A typical Xbox 360 game can use additional CPU-intensive software threads, so it might break up its workload into an update thread, rendering thread, and three worker threads, as shown in Figure 2.</span></span>

<span data-ttu-id="ec98c-165">**[圖 2]Xbox 360 遊戲中的執行緒設計**</span><span class="sxs-lookup"><span data-stu-id="ec98c-165">**Figure 2. Threading design in a game for Xbox 360**</span></span>

![xbox 360 遊戲中的執行緒設計](images/coding-for-multiple-cores-2.gif)

<span data-ttu-id="ec98c-167">除了檔案 i/o 和網路功能之外，這些工作都有可能耗用大量 CPU，足以受益于自己的硬體執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-167">With the exception of file I/O and networking, these tasks all have the potential to be CPU-intensive enough to benefit from being on their own hardware thread.</span></span> <span data-ttu-id="ec98c-168">這些工作也有可能會有足夠的獨立性，可在不進行通訊的情況下對整個框架執行。</span><span class="sxs-lookup"><span data-stu-id="ec98c-168">These tasks also have the potential to be independent enough that they can run for an entire frame without communicating.</span></span>

<span data-ttu-id="ec98c-169">遊戲更新執行緒管理控制器輸入、AI 和物理，並準備其他四個執行緒的指示。</span><span class="sxs-lookup"><span data-stu-id="ec98c-169">The game update thread manages controller input, AI, and physics, and prepares instructions for the other four threads.</span></span> <span data-ttu-id="ec98c-170">這些指示會放入遊戲更新執行緒所擁有的緩衝區中，因此在產生指示時不需要進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ec98c-170">These instructions are placed into buffers owned by the game update thread, so no synchronization is required as the instructions are generated.</span></span>

<span data-ttu-id="ec98c-171">在框架的結尾，遊戲更新執行緒將指令緩衝區交給其他四個執行緒，然後開始處理下一個畫面格，並填入另一組指令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ec98c-171">At the end of the frame, the game update thread hands off the instruction buffers to the four other threads, and then starts working on the next frame, filling in another set of instruction buffers.</span></span>

<span data-ttu-id="ec98c-172">因為更新和轉譯執行緒會彼此密集建置，所以它們的通訊緩衝區只會進行雙重緩衝處理：在任何指定的時間，更新執行緒會在轉譯執行緒從另一個緩衝區讀取時填滿一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ec98c-172">Because the update and rendering threads work in lockstep with each other, their communication buffers are simply double buffered: at any given time, the update thread is filling one buffer while the render thread is reading from the other.</span></span>

<span data-ttu-id="ec98c-173">其他背景工作執行緒不一定會與畫面播放速率相關聯。</span><span class="sxs-lookup"><span data-stu-id="ec98c-173">The other worker threads are not necessarily tied to the frame rate.</span></span> <span data-ttu-id="ec98c-174">將資料解壓縮可能會比框架少很多，或可能需要很多的畫面格。</span><span class="sxs-lookup"><span data-stu-id="ec98c-174">Decompressing a piece of data may take much less than a frame, or it may take many frames.</span></span> <span data-ttu-id="ec98c-175">即使是抹布和線的模擬，也可能不需要完全以畫面播放速率執行，因為較不頻繁的更新可能會很容易接受。</span><span class="sxs-lookup"><span data-stu-id="ec98c-175">Even the cloth and hair simulation may not need to run exactly at the frame rate because less frequent updates may be quite acceptable.</span></span> <span data-ttu-id="ec98c-176">因此，這三個執行緒需要不同的資料結構來與更新執行緒和轉譯執行緒通訊。</span><span class="sxs-lookup"><span data-stu-id="ec98c-176">Therefore, these three threads need different data structures to communicate with the update thread and the render thread.</span></span> <span data-ttu-id="ec98c-177">它們每個都需要可保存工作要求的輸入佇列，而轉譯執行緒需要可保存執行緒所產生之結果的資料佇列。</span><span class="sxs-lookup"><span data-stu-id="ec98c-177">They each need an input queue that can hold work requests, and the render thread needs a data queue that can hold the results produced by the threads.</span></span> <span data-ttu-id="ec98c-178">在每個框架的結尾，更新執行緒會將工作要求區塊新增至背景工作執行緒的佇列。</span><span class="sxs-lookup"><span data-stu-id="ec98c-178">At the end of each frame the update thread will add a block of work requests to worker threads' queues.</span></span> <span data-ttu-id="ec98c-179">只要針對每個畫面格加入清單一次，即可確保 update 執行緒能將同步處理額外負荷降到最低。</span><span class="sxs-lookup"><span data-stu-id="ec98c-179">Adding to the list just once per frame ensures that the update thread minimizes the synchronization overhead.</span></span> <span data-ttu-id="ec98c-180">每個背景工作執行緒都會使用如下所示的迴圈，盡可能快速地從工作佇列提取指派：</span><span class="sxs-lookup"><span data-stu-id="ec98c-180">Each of the worker threads pulls assignments from the work queue as quickly as it can, using a loop that looks something like this:</span></span>


```C++
for(;;)
{
    while( WorkQueueNotEmpty() )
    {
        RemoveWorkItemFromWorkQueue();
        ProcessWorkItem();
        PutResultInDataQueue();
    }
    WaitForSingleObject( hWorkSemaphore ); 
}
```



<span data-ttu-id="ec98c-181">因為資料會從更新執行緒移至背景工作執行緒，然後再到轉譯執行緒，所以在某些動作將它移至螢幕之前，可能會有三個或更多的框架延遲。</span><span class="sxs-lookup"><span data-stu-id="ec98c-181">Because the data goes from the update threads to the worker threads and then to the render thread, there can be a delay of three or more frames before some actions make it to the screen.</span></span> <span data-ttu-id="ec98c-182">但是，如果您將延遲容錯工作指派給背景工作執行緒，這應該不會造成問題。</span><span class="sxs-lookup"><span data-stu-id="ec98c-182">However, if you assign latency-tolerant tasks to the worker threads, then this should not be a problem.</span></span>

<span data-ttu-id="ec98c-183">另一種設計是讓多個背景工作執行緒都從相同的工作佇列中繪製。</span><span class="sxs-lookup"><span data-stu-id="ec98c-183">An alternate design would be to have several worker threads all drawing from the same work queue.</span></span> <span data-ttu-id="ec98c-184">這會提供自動負載平衡，讓所有工作者執行緒更有可能保持忙碌。</span><span class="sxs-lookup"><span data-stu-id="ec98c-184">This would give automatic load balancing and would make it more likely that all of the worker threads would stay busy.</span></span>

<span data-ttu-id="ec98c-185">遊戲更新執行緒必須小心，不要對工作者執行緒提供太多工作，否則工作佇列可能會持續成長。</span><span class="sxs-lookup"><span data-stu-id="ec98c-185">The game update thread must take care to not give too much work to the worker threads, or else the work queues may continuously grow.</span></span> <span data-ttu-id="ec98c-186">更新執行緒管理此作業的方式，取決於背景工作執行緒所執行的工作類型。</span><span class="sxs-lookup"><span data-stu-id="ec98c-186">How the update thread manages this depends on what sort of tasks the worker threads are doing.</span></span>

## <a name="simultaneous-multithreading-and-number-of-threads"></a><span data-ttu-id="ec98c-187">同步多執行緒和執行緒數目</span><span class="sxs-lookup"><span data-stu-id="ec98c-187">Simultaneous Multithreading and Number of Threads</span></span>

<span data-ttu-id="ec98c-188">所有線程都不會建立相等的。</span><span class="sxs-lookup"><span data-stu-id="ec98c-188">All threads are not created equal.</span></span> <span data-ttu-id="ec98c-189">兩個硬體執行緒可能位於不同晶片、相同晶片或甚至相同核心上。</span><span class="sxs-lookup"><span data-stu-id="ec98c-189">Two hardware threads might be on separate chips, on the same chip, or even on the same core.</span></span> <span data-ttu-id="ec98c-190">遊戲程式設計人員要注意的最重要設定是一個核心上的兩個硬體執行緒—同時多執行緒 (SMT) 或 Hyper-Threading 技術 (HT 技術) 。</span><span class="sxs-lookup"><span data-stu-id="ec98c-190">The most important configuration for game programmers to be aware of is two hardware threads on one core—Simultaneous Multi-Threading (SMT) or Hyper-Threading Technology (HT Technology).</span></span>

<span data-ttu-id="ec98c-191">SMT 或 HT 技術執行緒共用 CPU 核心的資源。</span><span class="sxs-lookup"><span data-stu-id="ec98c-191">SMT or HT Technology threads share the resources of the CPU core.</span></span> <span data-ttu-id="ec98c-192">因為它們共用執行單位，所以從執行兩個執行緒而不是一個執行緒的最大速度通常是10到20%，而不是兩個獨立硬體執行緒可能的100%。</span><span class="sxs-lookup"><span data-stu-id="ec98c-192">Because they share the execution units, the maximum speedup from running two threads instead of one is typically 10 to 20 percent, instead of the 100 percent that is possible from two independent hardware threads.</span></span>

<span data-ttu-id="ec98c-193">更明顯地來說，SMT 或 HT 技術執行緒共用 L1 指令和資料快取。</span><span class="sxs-lookup"><span data-stu-id="ec98c-193">More significantly, SMT or HT Technology threads share the L1 instruction and data caches.</span></span> <span data-ttu-id="ec98c-194">如果它們的記憶體存取模式不相容，它們可能會在快取上進行對抗，並導致許多快取遺漏。</span><span class="sxs-lookup"><span data-stu-id="ec98c-194">If their memory access patterns are incompatible, they can end up fighting over the cache and causing many cache misses.</span></span> <span data-ttu-id="ec98c-195">在最糟的情況下，CPU 核心的整體效能可能會在第二個執行緒執行時實際減少。</span><span class="sxs-lookup"><span data-stu-id="ec98c-195">In the worst case, the total performance for the CPU core can actually decrease when a second thread is run.</span></span> <span data-ttu-id="ec98c-196">在 Xbox 360 上，這是相當簡單的問題。</span><span class="sxs-lookup"><span data-stu-id="ec98c-196">On Xbox 360, this is a fairly simple problem.</span></span> <span data-ttu-id="ec98c-197">已知 Xbox 360 的設定：三個 CPU 核心各有兩個硬體執行緒，而開發人員將其軟體執行緒指派給特定的 CPU 執行緒，並可進行測量以查看其執行緒設計是否可提供額外的效能。</span><span class="sxs-lookup"><span data-stu-id="ec98c-197">The configuration of the Xbox 360 is known—three CPU cores each with two hardware threads—and developers assign their software threads to specific CPU threads and can measure to see whether their threading design gives them extra performance.</span></span>

<span data-ttu-id="ec98c-198">在 Windows 上，情況更為複雜。</span><span class="sxs-lookup"><span data-stu-id="ec98c-198">On Windows, the situation is more complicated.</span></span> <span data-ttu-id="ec98c-199">執行緒和其設定的數目會因電腦而異，且判斷設定會很複雜。</span><span class="sxs-lookup"><span data-stu-id="ec98c-199">The number of threads and their configuration will vary from computer to computer, and determining the configuration is complicated.</span></span> <span data-ttu-id="ec98c-200">函數 [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) 會提供不同硬體執行緒之間關聯性的相關資訊，而此函式可在 windows Vista、windows 7 和 WINDOWS XP SP3 上取得。</span><span class="sxs-lookup"><span data-stu-id="ec98c-200">The function [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) gives information about the relationship between different hardware threads, and this function is available on Windows Vista, Windows 7, and Windows XP SP3.</span></span> <span data-ttu-id="ec98c-201">因此，現在您必須使用 CPUID 指令和 Intel 和 AMD 提供的演算法，以決定您可以使用的「實際」執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="ec98c-201">Therefore, for now you have to use the CPUID instruction and the algorithms given by Intel and AMD in order to decide how many "real" threads you have available.</span></span> <span data-ttu-id="ec98c-202">如需詳細資訊，請參閱參考。</span><span class="sxs-lookup"><span data-stu-id="ec98c-202">See the references for more information.</span></span>

<span data-ttu-id="ec98c-203">DirectX SDK 中的 CoreDetection 範例包含範例程式碼，該程式碼會使用 [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) 函數或 CPUID 指令來傳回 CPU 核心拓撲。</span><span class="sxs-lookup"><span data-stu-id="ec98c-203">The CoreDetection sample in the DirectX SDK contains sample code that uses the [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) function or the CPUID instruction to return the CPU core topology.</span></span> <span data-ttu-id="ec98c-204">如果目前的平臺不支援 **GetLogicalProcessorInformation** ，則會使用 CPUID 指令。</span><span class="sxs-lookup"><span data-stu-id="ec98c-204">The CPUID instruction is used if **GetLogicalProcessorInformation** is not supported on the current platform.</span></span> <span data-ttu-id="ec98c-205">您可以在下列位置找到 CoreDetection：</span><span class="sxs-lookup"><span data-stu-id="ec98c-205">CoreDetection can be found in the following locations:</span></span>

<dl> <dt>

<span data-ttu-id="ec98c-206"><span id="Source_"></span><span id="source_"></span><span id="SOURCE_"></span>源：</span><span class="sxs-lookup"><span data-stu-id="ec98c-206"><span id="Source_"></span><span id="source_"></span><span id="SOURCE_"></span>Source:</span></span>
</dt> <dd>

<span data-ttu-id="ec98c-207">*DIRECTX SDK 根目錄* \\範例 \\ c + + \\ 其他 \\ CoreDetection</span><span class="sxs-lookup"><span data-stu-id="ec98c-207">*DirectX SDK root*\\Samples\\C++\\Misc\\CoreDetection</span></span>

</dd> <dt>

<span data-ttu-id="ec98c-208"><span id="Executable_"></span><span id="executable_"></span><span id="EXECUTABLE_"></span>可執行：</span><span class="sxs-lookup"><span data-stu-id="ec98c-208"><span id="Executable_"></span><span id="executable_"></span><span id="EXECUTABLE_"></span>Executable:</span></span>
</dt> <dd>

<span data-ttu-id="ec98c-209">*DIRECTX SDK 根目錄* \\範例 \\ c + + \\ 其他 \\ Bin \\CoreDetection.exe</span><span class="sxs-lookup"><span data-stu-id="ec98c-209">*DirectX SDK root*\\Samples\\C++\\Misc\\Bin\\CoreDetection.exe</span></span>

</dd> </dl>

<span data-ttu-id="ec98c-210">最安全的假設是每個 CPU 核心不需要超過一個 CPU 密集型執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-210">The safest assumption is to have no more than one CPU-intensive thread per CPU core.</span></span> <span data-ttu-id="ec98c-211">擁有比 CPU 核心更多的需要大量 CPU 的執行緒沒有任何好處，並帶來額外的額外負荷和其他執行緒的複雜度。</span><span class="sxs-lookup"><span data-stu-id="ec98c-211">Having more CPU-intensive threads than CPU cores gives little or no benefits, and brings the extra overhead and complexity of additional threads.</span></span>

## <a name="creating-threads"></a><span data-ttu-id="ec98c-212">建立執行緒</span><span class="sxs-lookup"><span data-stu-id="ec98c-212">Creating Threads</span></span>

<span data-ttu-id="ec98c-213">建立執行緒是相當簡單的作業，但是有許多可能的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec98c-213">Creating threads is a fairly simple operation, but there are many potential errors.</span></span> <span data-ttu-id="ec98c-214">下列程式碼顯示適當的方式來建立執行緒、等候它終止，然後清除。</span><span class="sxs-lookup"><span data-stu-id="ec98c-214">The code below shows the proper way of creating a thread, waiting for it to terminate, and then cleaning up.</span></span>


```C++
const int stackSize = 65536;
HANDLE hThread = (HANDLE)_beginthreadex( 0, stackSize,
            ThreadFunction, 0, 0, 0 );
// Do work on main thread here.
// Wait for child thread to complete
WaitForSingleObject( hThread, INFINITE );
CloseHandle( hThread );

...

unsigned __stdcall ThreadFunction( void* data )
{
#if _XBOX_VER >= 200
    // On Xbox 360 you must explicitly assign
    // software threads to hardware threads.
    XSetThreadProcessor( GetCurrentThread(), 2 );
#endif
    // Do child thread work here.
    return 0;
}
```



<span data-ttu-id="ec98c-215">當您建立執行緒時，您可以選擇指定子執行緒的堆疊大小，或指定零，在這種情況下，子執行緒將會繼承父執行緒的堆疊大小。</span><span class="sxs-lookup"><span data-stu-id="ec98c-215">When you create a thread, you have the option to specify the stack size for the child thread, or specify zero, in which case the child thread will inherit the parent thread's stack size.</span></span> <span data-ttu-id="ec98c-216">在 Xbox 360 上，當執行緒啟動時，堆疊會完全認可，而指定零可能會浪費大量的記憶體，因為許多子執行緒不需要像父系一樣多的堆疊。</span><span class="sxs-lookup"><span data-stu-id="ec98c-216">On Xbox 360, where stacks are fully committed when the thread starts, specifying zero can waste significant memory, because many child threads will not need as much stack as the parent.</span></span> <span data-ttu-id="ec98c-217">在 Xbox 360 也請務必將堆疊大小設為 64-KB 的倍數。</span><span class="sxs-lookup"><span data-stu-id="ec98c-217">On Xbox 360 it is also important that the stack size be a multiple of 64-KB.</span></span>

<span data-ttu-id="ec98c-218">如果您使用 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 函式來建立執行緒，則 C/c + + 執行時間 (CRT) 將無法在 Windows 上正確地初始化。</span><span class="sxs-lookup"><span data-stu-id="ec98c-218">If you use the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create threads, then the C/C++ runtime (CRT) will not get properly initialized on Windows.</span></span> <span data-ttu-id="ec98c-219">我們建議您改用 CRT [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx)函數。</span><span class="sxs-lookup"><span data-stu-id="ec98c-219">We recommend that you use the CRT [**\_beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) function instead.</span></span>

<span data-ttu-id="ec98c-220">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)或 [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx)的傳回值是執行緒控制碼。</span><span class="sxs-lookup"><span data-stu-id="ec98c-220">The return value from [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) or [**\_beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) is a thread handle.</span></span> <span data-ttu-id="ec98c-221">您可以使用這個執行緒來等候子執行緒終止，這比檢查執行緒狀態的迴圈中的旋轉更簡單且更有效率。</span><span class="sxs-lookup"><span data-stu-id="ec98c-221">This thread can be used to wait for the child thread to terminate, which is much simpler and much more efficient than spinning in a loop checking the thread status.</span></span> <span data-ttu-id="ec98c-222">若要等候執行緒終止，只要以執行緒控制碼呼叫 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 即可。</span><span class="sxs-lookup"><span data-stu-id="ec98c-222">To wait for the thread to terminate, simply call [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) with the thread handle.</span></span>

<span data-ttu-id="ec98c-223">線上程終止且執行緒控制碼已關閉之前，將不會釋放執行緒的資源。</span><span class="sxs-lookup"><span data-stu-id="ec98c-223">The resources for the thread will not be freed until the thread has terminated and the thread handle has been closed.</span></span> <span data-ttu-id="ec98c-224">因此，當您完成時，請務必使用 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 來關閉執行緒控制碼。</span><span class="sxs-lookup"><span data-stu-id="ec98c-224">Therefore, it is important to close the thread handle with [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) when you are finished with it.</span></span> <span data-ttu-id="ec98c-225">如果您將等待中的執行緒使用 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)來終止，請務必在等候完成之前關閉控制碼。</span><span class="sxs-lookup"><span data-stu-id="ec98c-225">If you will be waiting for the thread to terminate with [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), be sure to not close the handle until after the wait has completed.</span></span>

<span data-ttu-id="ec98c-226">在 Xbox 360 上，您必須使用 **XSetThreadProcessor** 明確地將軟體執行緒指派給特定的硬體執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-226">On Xbox 360, you must explicitly assign software threads to a particular hardware thread by using **XSetThreadProcessor**.</span></span> <span data-ttu-id="ec98c-227">否則，所有子執行緒都會保持在與父系相同的硬體執行緒上。</span><span class="sxs-lookup"><span data-stu-id="ec98c-227">Otherwise, all child threads will stay on the same hardware thread as the parent.</span></span> <span data-ttu-id="ec98c-228">在 Windows 上，您可以使用 [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask) ，強烈建議使用您的執行緒應該在哪個硬體執行緒上執行的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ec98c-228">On Windows, you can use [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask) to strongly suggest to the operating system which hardware threads your thread should run on.</span></span> <span data-ttu-id="ec98c-229">由於您不知道系統上可能執行了哪些其他進程，因此通常應該避免在 Windows 上執行這項技術。</span><span class="sxs-lookup"><span data-stu-id="ec98c-229">This technique should generally be avoided on Windows since you don't know what other processes might be running on the system.</span></span> <span data-ttu-id="ec98c-230">通常最好是讓 Windows 排程器將您的執行緒指派給閒置的硬體執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-230">It is typically better to let the Windows scheduler assign your threads to idle hardware threads.</span></span>

<span data-ttu-id="ec98c-231">建立執行緒是昂貴的作業。</span><span class="sxs-lookup"><span data-stu-id="ec98c-231">Creating threads is an expensive operation.</span></span> <span data-ttu-id="ec98c-232">執行緒應該建立和終結很少。</span><span class="sxs-lookup"><span data-stu-id="ec98c-232">Threads should be created and destroyed rarely.</span></span> <span data-ttu-id="ec98c-233">如果您發現自己想要經常建立和終結執行緒，請改用等候工作的執行緒集區。</span><span class="sxs-lookup"><span data-stu-id="ec98c-233">If you find yourself wanting to create and destroy threads frequently, use a pool of threads that wait around for work instead.</span></span>

## <a name="synchronizing-threads"></a><span data-ttu-id="ec98c-234">同步處理執行緒</span><span class="sxs-lookup"><span data-stu-id="ec98c-234">Synchronizing Threads</span></span>

<span data-ttu-id="ec98c-235">若要讓多個執行緒一起運作，您必須能夠同步處理執行緒、傳遞訊息，以及要求資源的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="ec98c-235">For multiple threads to work together, you must be able to synchronize threads, pass messages, and request exclusive access to resources.</span></span> <span data-ttu-id="ec98c-236">Windows 和 Xbox 360 隨附一組豐富的同步處理原始物件。</span><span class="sxs-lookup"><span data-stu-id="ec98c-236">Windows and Xbox 360 come with a rich set of synchronization primitives.</span></span> <span data-ttu-id="ec98c-237">如需這些同步處理原始物件的完整詳細資訊，請參閱平臺檔。</span><span class="sxs-lookup"><span data-stu-id="ec98c-237">For full details on these synchronization primitives, see the platform documentation.</span></span>

### <a name="exclusive-access"></a><span data-ttu-id="ec98c-238">獨佔存取權</span><span class="sxs-lookup"><span data-stu-id="ec98c-238">Exclusive Access</span></span>

<span data-ttu-id="ec98c-239">取得資源、資料結構或程式碼路徑的獨佔存取權，是常見的需求。</span><span class="sxs-lookup"><span data-stu-id="ec98c-239">Gaining exclusive access to a resource, data structure, or code path is a common need.</span></span> <span data-ttu-id="ec98c-240">取得獨佔存取權的其中一個選項是 mutex，其一般使用方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="ec98c-240">One option for gaining exclusive access is a mutex, whose typical usage is shown here.</span></span>


```C++
// Initialize
HANDLE mutex = CreateMutex( 0, FALSE, 0 );

// Use
void ManipulateSharedData()
{
    WaitForSingleObject( mutex, INFINITE );
    // Manipulate stuff...
    ReleaseMutex( mutex );
}

// Destroy
CloseHandle( mutex );
The kernel guarantees that, for a particular mutex, only one thread at a time can 
acquire it.
The main disadvantage to mutexes is that they are relatively expensive to acquire 
and release. A faster alternative is a critical section.
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection( &cs );

// Use
void ManipulateSharedData()
{
    EnterCriticalSection( &cs );
    // Manipulate stuff...
    LeaveCriticalSection( &cs );
}

// Destroy
DeleteCriticalSection( &cs );
```



<span data-ttu-id="ec98c-241">重要區段與 mutex 具有類似的語法，但是它們只能在進程內進行同步處理，而不是在進程之間進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ec98c-241">Critical sections have similar semantics to mutexes, but they can be used to synchronize only within a process, not between processes.</span></span> <span data-ttu-id="ec98c-242">其主要優點是它們執行的速度大約比 mutex 快20倍。</span><span class="sxs-lookup"><span data-stu-id="ec98c-242">Their main advantage is that they execute roughly twenty times faster than mutexes.</span></span>

### <a name="events"></a><span data-ttu-id="ec98c-243">事件</span><span class="sxs-lookup"><span data-stu-id="ec98c-243">Events</span></span>

<span data-ttu-id="ec98c-244">如果有兩個執行緒（可能是更新執行緒和轉譯執行緒）正在使用一對轉譯描述緩衝區，則它們需要一種方式來指出何時使用其特定緩衝區完成。</span><span class="sxs-lookup"><span data-stu-id="ec98c-244">If two threads—perhaps an update thread and a render thread—are taking turns using a pair of render description buffers, they need a way to indicate when they are done with their particular buffer.</span></span> <span data-ttu-id="ec98c-245">這可以藉由將使用 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)) 配置的事件 (與每個緩衝區產生關聯來完成。</span><span class="sxs-lookup"><span data-stu-id="ec98c-245">This can be done by associating an event (allocated with [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)) with each buffer.</span></span> <span data-ttu-id="ec98c-246">當執行緒以緩衝區完成時，它可以使用 [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent) 來表示這一點，然後在另一個緩衝區的事件上呼叫 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 。</span><span class="sxs-lookup"><span data-stu-id="ec98c-246">When a thread is done with a buffer, it can use [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent) to signal this, and can then call [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) on the other buffer's event.</span></span> <span data-ttu-id="ec98c-247">這項技術可輕鬆據此資源的三倍緩衝。</span><span class="sxs-lookup"><span data-stu-id="ec98c-247">This technique extrapolates easily to triple buffering of resources.</span></span>

### <a name="semaphores"></a><span data-ttu-id="ec98c-248">信號燈</span><span class="sxs-lookup"><span data-stu-id="ec98c-248">Semaphores</span></span>

<span data-ttu-id="ec98c-249">信號是用來控制可執行檔執行緒數目，通常用來執行工作佇列。</span><span class="sxs-lookup"><span data-stu-id="ec98c-249">A semaphore is used to control how many threads can be running and is commonly used to implement work queues.</span></span> <span data-ttu-id="ec98c-250">其中一個執行緒會將工作新增至佇列，並在每次將新的專案加入至佇列時使用 [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) 。</span><span class="sxs-lookup"><span data-stu-id="ec98c-250">One thread adds work to a queue and uses [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) whenever it adds a new item to the queue.</span></span> <span data-ttu-id="ec98c-251">這可讓一個背景工作執行緒從等候中的執行緒集區中釋放。</span><span class="sxs-lookup"><span data-stu-id="ec98c-251">This allows one worker thread to be released from the pool of waiting threads.</span></span> <span data-ttu-id="ec98c-252">工作者執行緒只會呼叫 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)，當它傳回時，他們知道佇列中有一個工作專案。</span><span class="sxs-lookup"><span data-stu-id="ec98c-252">The worker threads just call [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), and when it returns they know there is a work item in the queue for them.</span></span> <span data-ttu-id="ec98c-253">此外，必須使用重要區段或其他同步處理技術，才能保證共用工作佇列的安全存取。</span><span class="sxs-lookup"><span data-stu-id="ec98c-253">In addition, a critical section or other synchronization technique must be used in order to guarantee safe access to the shared work queue.</span></span>

### <a name="avoid-suspendthread"></a><span data-ttu-id="ec98c-254">避免 SuspendThread</span><span class="sxs-lookup"><span data-stu-id="ec98c-254">Avoid SuspendThread</span></span>

<span data-ttu-id="ec98c-255">有時候，當您想要讓執行緒停止正在執行的工作時，使用 [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) ，而不是正確的同步處理原始物件會很有吸引力。</span><span class="sxs-lookup"><span data-stu-id="ec98c-255">Sometimes when you want a thread to stop what it is doing, it is tempting to use [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) instead of the correct synchronization primitives.</span></span> <span data-ttu-id="ec98c-256">這一律是不良的概念，而且可能很容易導致鎖死和其他問題。</span><span class="sxs-lookup"><span data-stu-id="ec98c-256">This is always a bad idea and can easily lead to deadlocks and other problems.</span></span> <span data-ttu-id="ec98c-257">**SuspendThread** 也會與 Visual Studio 偵錯工具不正確互動。</span><span class="sxs-lookup"><span data-stu-id="ec98c-257">**SuspendThread** also interacts badly with the Visual Studio debugger.</span></span> <span data-ttu-id="ec98c-258">避免 **SuspendThread**。</span><span class="sxs-lookup"><span data-stu-id="ec98c-258">Avoid **SuspendThread**.</span></span> <span data-ttu-id="ec98c-259">請改用 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 。</span><span class="sxs-lookup"><span data-stu-id="ec98c-259">Use [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) instead.</span></span>

### <a name="waitforsingleobject-and-waitformultipleobjects"></a><span data-ttu-id="ec98c-260">WaitForSingleObject 和 WaitForMultipleObjects</span><span class="sxs-lookup"><span data-stu-id="ec98c-260">WaitForSingleObject and WaitForMultipleObjects</span></span>

<span data-ttu-id="ec98c-261">函數 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 是最常用的同步處理函數。</span><span class="sxs-lookup"><span data-stu-id="ec98c-261">The function [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) is the most commonly used synchronization function.</span></span> <span data-ttu-id="ec98c-262">不過，有時候您會想要讓執行緒等候數個條件，或符合一組條件的其中一個條件。</span><span class="sxs-lookup"><span data-stu-id="ec98c-262">However, sometimes you want a thread to wait until several conditions are simultaneously satisfied, or until one of a set of conditions are satisfied.</span></span> <span data-ttu-id="ec98c-263">在此情況下，您應該使用 [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects)。</span><span class="sxs-lookup"><span data-stu-id="ec98c-263">In this case, you should use [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).</span></span>

### <a name="interlocked-functions-and-lockless-programming"></a><span data-ttu-id="ec98c-264">連鎖函數和 Lockless 程式設計</span><span class="sxs-lookup"><span data-stu-id="ec98c-264">Interlocked Functions and Lockless Programming</span></span>

<span data-ttu-id="ec98c-265">有一系列函數可執行簡單的安全線程作業，而不需要使用鎖定。</span><span class="sxs-lookup"><span data-stu-id="ec98c-265">There is a family of functions for performing simple thread-safe operations without using locks.</span></span> <span data-ttu-id="ec98c-266">這些是連鎖的函式系列，例如 [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement)。</span><span class="sxs-lookup"><span data-stu-id="ec98c-266">These are the Interlocked family of functions, such as [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement).</span></span> <span data-ttu-id="ec98c-267">這些函式和其他使用旗標旗標的技巧，統稱為 lockless 程式設計。</span><span class="sxs-lookup"><span data-stu-id="ec98c-267">These functions, plus other techniques using careful setting of flags, are together known as lockless programming.</span></span> <span data-ttu-id="ec98c-268">Lockless 程式設計很難正確運作，而且在 Xbox 360 上比在 Windows 上更為困難。</span><span class="sxs-lookup"><span data-stu-id="ec98c-268">Lockless programming can be extremely tricky to do correctly, and is substantially more difficult on Xbox 360 than on Windows.</span></span>

<span data-ttu-id="ec98c-269">如需無鎖定程式設計的詳細資訊，請參閱 [Xbox 360 和 Microsoft Windows 的程式設計考慮 Lockless](./lockless-programming.md)。</span><span class="sxs-lookup"><span data-stu-id="ec98c-269">For more information about programming without locks, see [Lockless Programming Considerations for Xbox 360 and Microsoft Windows](./lockless-programming.md).</span></span>

### <a name="minimizing-synchronization"></a><span data-ttu-id="ec98c-270">最小化同步處理</span><span class="sxs-lookup"><span data-stu-id="ec98c-270">Minimizing Synchronization</span></span>

<span data-ttu-id="ec98c-271">某些同步處理方法會比其他方法更快。</span><span class="sxs-lookup"><span data-stu-id="ec98c-271">Some synchronization methods are faster than others.</span></span> <span data-ttu-id="ec98c-272">不過，您不需要藉由選擇最快的同步處理技術來優化您的程式碼，通常較不常進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ec98c-272">However, rather than optimizing your code by choosing the fastest synchronization techniques possible, it is usually better to synchronize less often.</span></span> <span data-ttu-id="ec98c-273">這比太頻繁地進行同步處理的速度更快，而且可讓更簡單的程式碼更容易進行 debug 錯。</span><span class="sxs-lookup"><span data-stu-id="ec98c-273">This is faster than synchronizing too frequently, and it makes for simpler code that is easier to debug.</span></span>

<span data-ttu-id="ec98c-274">某些作業（例如記憶體配置）可能必須使用同步處理原始物件才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="ec98c-274">Some operations, such as memory allocation, may have to use synchronization primitives in order to work correctly.</span></span> <span data-ttu-id="ec98c-275">因此，從預設共用堆積進行頻繁的配置將會導致頻繁的同步處理，這會浪費一些效能。</span><span class="sxs-lookup"><span data-stu-id="ec98c-275">Therefore, doing frequent allocations from the default shared heap will result in frequent synchronization, which will waste some performance.</span></span> <span data-ttu-id="ec98c-276">\_ \_ 如果您使用 HeapCreate) 可以避免發生此隱藏同步處理，則使用堆積不會序列化，以避免頻繁的配置或使用每個執行緒的堆積 (。</span><span class="sxs-lookup"><span data-stu-id="ec98c-276">Avoiding frequent allocations or using per-thread heaps (using HEAP\_NO\_SERIALIZE if you use HeapCreate) can avoid this hidden synchronization.</span></span>

<span data-ttu-id="ec98c-277">隱藏同步處理的另一個原因是 D3DCREATE \_ 多執行緒，這會導致 Windows 上的 D3D 在許多作業上使用同步處理。</span><span class="sxs-lookup"><span data-stu-id="ec98c-277">Another cause of hidden synchronization is D3DCREATE\_MULTITHREADED, which causes D3D on Windows to use synchronization on many operations.</span></span> <span data-ttu-id="ec98c-278"> (Xbox 360 上會忽略旗標。 ) </span><span class="sxs-lookup"><span data-stu-id="ec98c-278">(The flag is ignored on Xbox 360.)</span></span>

<span data-ttu-id="ec98c-279">每個執行緒的資料（也稱為執行緒區域儲存區）可能是避免同步處理的重要方式。</span><span class="sxs-lookup"><span data-stu-id="ec98c-279">Per-thread data, also known as thread local storage, can be an important way of avoiding synchronization.</span></span> <span data-ttu-id="ec98c-280">Visual C++ 可讓您使用 **\_ \_ declspec (執行緒)** 語法，將全域變數宣告為每個執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-280">Visual C++ allows you to declare global variables as being per-thread with the **\_\_declspec(thread)** syntax.</span></span>


```C++
__declspec( thread ) int tls_i = 1;
```



<span data-ttu-id="ec98c-281">這會讓進程中的每個執行緒都有自己的 tls \_ i 複本，而且可以安全且有效率地參考，而不需要進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ec98c-281">This gives each thread in the process its own copy of tls\_i, which can be referenced safely and efficiently without requiring synchronization.</span></span>

<span data-ttu-id="ec98c-282">**\_ \_ Declspec (thread)** 技術無法使用動態載入的 dll。</span><span class="sxs-lookup"><span data-stu-id="ec98c-282">The **\_\_declspec(thread)** technique does not work with dynamically loaded DLLs.</span></span> <span data-ttu-id="ec98c-283">如果您使用動態載入的 Dll，您將需要使用 TLSAlloc 系列的函式來執行執行緒區域儲存區。</span><span class="sxs-lookup"><span data-stu-id="ec98c-283">If you use dynamically loaded DLLs, you will need to use the TLSAlloc family of functions to implement thread local storage.</span></span>

## <a name="destroying-threads"></a><span data-ttu-id="ec98c-284">終結執行緒</span><span class="sxs-lookup"><span data-stu-id="ec98c-284">Destroying Threads</span></span>

<span data-ttu-id="ec98c-285">終結執行緒的唯一安全方法是讓執行緒本身結束，方法是從主執行緒函式傳回，或讓執行緒呼叫 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)或 [**\_ endthreadex**](https://msdn.microsoft.com/library/hw264s73(v=VS.71).aspx)。</span><span class="sxs-lookup"><span data-stu-id="ec98c-285">The only safe way to destroy a thread is to have the thread itself exit, either by returning from the main thread function or by having the thread call [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) or [**\_endthreadex**](https://msdn.microsoft.com/library/hw264s73(v=VS.71).aspx).</span></span> <span data-ttu-id="ec98c-286">如果使用 [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx)建立執行緒，則應該使用 **\_ endthreadex** 或從主執行緒函式傳回，因為使用 **ExitThread** 無法正確地釋放 CRT 資源。</span><span class="sxs-lookup"><span data-stu-id="ec98c-286">If a thread is created with [**\_beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx), then it should use **\_endthreadex** or return from the main thread function, since using **ExitThread** won't properly free CRT resources.</span></span> <span data-ttu-id="ec98c-287">請勿呼叫 [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) 函式，因為執行緒將不會正確地清除。</span><span class="sxs-lookup"><span data-stu-id="ec98c-287">Never call the [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) function, because the thread will not be properly cleaned up.</span></span> <span data-ttu-id="ec98c-288">執行緒應該一律認可自殺，永遠不會 murdered。</span><span class="sxs-lookup"><span data-stu-id="ec98c-288">Threads should always commit suicide—they should never be murdered.</span></span>

## <a name="openmp"></a><span data-ttu-id="ec98c-289">OpenMP</span><span class="sxs-lookup"><span data-stu-id="ec98c-289">OpenMP</span></span>

<span data-ttu-id="ec98c-290">OpenMP 是一種語言延伸模組，可讓您使用 pragma 來引導平行迴圈中的編譯器，以將多執行緒加入至您的程式。</span><span class="sxs-lookup"><span data-stu-id="ec98c-290">OpenMP is a language extension for adding multithreading to your program by using pragmas to guide the compiler in parallelizing loops.</span></span> <span data-ttu-id="ec98c-291">Windows 和 Xbox 360 上的 Visual C++ 2005 支援 OpenMP，並且可以與手動執行緒管理一起使用。</span><span class="sxs-lookup"><span data-stu-id="ec98c-291">OpenMP is supported by Visual C++ 2005 on Windows and Xbox 360 and can be used in conjunction with manual thread management.</span></span> <span data-ttu-id="ec98c-292">OpenMP 可能是您程式碼多執行緒元件的便利方法，但不太可能是理想的解決方案，特別是針對遊戲。</span><span class="sxs-lookup"><span data-stu-id="ec98c-292">OpenMP can be a convenient way to multithread parts of your code, but is unlikely to be the ideal solution, especially for games.</span></span> <span data-ttu-id="ec98c-293">OpenMP 可能更適用于長時間執行的生產工作，例如處理圖片和其他資源。</span><span class="sxs-lookup"><span data-stu-id="ec98c-293">OpenMP may be more applicable to longer-running production tasks such as processing art and other resources.</span></span> <span data-ttu-id="ec98c-294">如需詳細資訊，請參閱 Visual C++ 檔或移至 OpenMP [網站](https://www.openmp.org/)。</span><span class="sxs-lookup"><span data-stu-id="ec98c-294">For more information, see the Visual C++ documentation or go to the OpenMP [website](https://www.openmp.org/).</span></span>

## <a name="profiling"></a><span data-ttu-id="ec98c-295">程式碼剖析</span><span class="sxs-lookup"><span data-stu-id="ec98c-295">Profiling</span></span>

<span data-ttu-id="ec98c-296">多執行緒分析很重要。</span><span class="sxs-lookup"><span data-stu-id="ec98c-296">Multithreaded profiling is important.</span></span> <span data-ttu-id="ec98c-297">很容易就會很久，因為執行緒會彼此等候。</span><span class="sxs-lookup"><span data-stu-id="ec98c-297">It is easy to end up with long stalls where threads are waiting on each other.</span></span> <span data-ttu-id="ec98c-298">這些延遲可能難以尋找和診斷。</span><span class="sxs-lookup"><span data-stu-id="ec98c-298">These stalls can be difficult to find and diagnose.</span></span> <span data-ttu-id="ec98c-299">若要協助識別它們，請考慮將檢測新增至同步處理呼叫。</span><span class="sxs-lookup"><span data-stu-id="ec98c-299">To help identify them, consider adding instrumentation to your synchronization calls.</span></span> <span data-ttu-id="ec98c-300">取樣分析工具也可以協助識別這些問題，因為它可以記錄計時資訊，而不會大幅改變。</span><span class="sxs-lookup"><span data-stu-id="ec98c-300">A sampling profiler can also help identify these problems because it can record timing information without substantially altering it.</span></span>

## <a name="timing"></a><span data-ttu-id="ec98c-301">計時</span><span class="sxs-lookup"><span data-stu-id="ec98c-301">Timing</span></span>

<span data-ttu-id="ec98c-302">Rdtsc 指令是取得 Windows 精確計時資訊的一種方式。</span><span class="sxs-lookup"><span data-stu-id="ec98c-302">The rdtsc instruction is one way to get accurate timing information on Windows.</span></span> <span data-ttu-id="ec98c-303">可惜的是，rdtsc 有多個問題，使其成為出貨標題的不良選擇。</span><span class="sxs-lookup"><span data-stu-id="ec98c-303">Unfortunately, rdtsc has multiple problems that make it a poor choice for your shipping title.</span></span> <span data-ttu-id="ec98c-304">Cpu 之間不一定要同步處理 rdtsc 計數器，因此當您的執行緒在硬體執行緒之間移動時，可能會得到很大的正面或負面差異。</span><span class="sxs-lookup"><span data-stu-id="ec98c-304">The rdtsc counters are not necessarily synchronized between CPUs, so when your thread moves between hardware threads you may get large positive or negative differences.</span></span> <span data-ttu-id="ec98c-305">根據電源管理設定，rdtsc 計數器的遞增頻率也可能會隨著遊戲執行而變更。</span><span class="sxs-lookup"><span data-stu-id="ec98c-305">Depending on power management settings, the frequency at which the rdtsc counter increments may also change as your game runs.</span></span> <span data-ttu-id="ec98c-306">為了避免這些問題，您應該偏好 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 和 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) ，以在出貨遊戲中進行高精確度的時間。</span><span class="sxs-lookup"><span data-stu-id="ec98c-306">To avoid these difficulties, you should prefer [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) and [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) for high-precision timing in your shipping game.</span></span> <span data-ttu-id="ec98c-307">如需計時的詳細資訊，請參閱 [遊戲時間和多核心處理器](./game-timing-and-multicore-processors.md)。</span><span class="sxs-lookup"><span data-stu-id="ec98c-307">For more information about timing, see [Game Timing and Multicore Processors](./game-timing-and-multicore-processors.md).</span></span>

## <a name="debugging"></a><span data-ttu-id="ec98c-308">偵錯</span><span class="sxs-lookup"><span data-stu-id="ec98c-308">Debugging</span></span>

<span data-ttu-id="ec98c-309">Visual Studio 完全支援 Windows 和 Xbox 360 的多執行緒偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="ec98c-309">Visual Studio fully supports multithreaded debugging for Windows and Xbox 360.</span></span> <span data-ttu-id="ec98c-310">Visual Studio 執行緒] 視窗可讓您線上程之間切換，以便查看不同的呼叫堆疊和區域變數。</span><span class="sxs-lookup"><span data-stu-id="ec98c-310">The Visual Studio threads window lets you switch between threads in order to see the different call stacks and local variables.</span></span> <span data-ttu-id="ec98c-311">[執行緒] 視窗也可讓您凍結和解除凍結特定的執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-311">The threads window also lets you freeze and thaw particular threads.</span></span>

<span data-ttu-id="ec98c-312">在 Xbox 360 上，您可以使用 [監看式] 視窗中的 [ **\@ hwthread** ] 元變數，顯示目前選取的軟體執行緒執行所在的硬體執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec98c-312">On Xbox 360, you can use the **\@hwthread** meta-variable in the watch window to show the hardware thread on which the currently selected software thread is running.</span></span>

<span data-ttu-id="ec98c-313">如果您將執行緒命名為有意義的名稱，[執行緒] 視窗會更容易使用。</span><span class="sxs-lookup"><span data-stu-id="ec98c-313">The threads window is easier to use if you name your threads meaningfully.</span></span> <span data-ttu-id="ec98c-314">Visual Studio 和其他 Microsoft 偵錯工具都可讓您為執行緒命名。</span><span class="sxs-lookup"><span data-stu-id="ec98c-314">Visual Studio and other Microsoft debuggers allow you to name your threads.</span></span> <span data-ttu-id="ec98c-315">執行下列 **SetThreadName** 函式，並在每個執行緒啟動時呼叫它。</span><span class="sxs-lookup"><span data-stu-id="ec98c-315">Implement the following **SetThreadName** function and call it from each thread as it starts up.</span></span>


```C++
typedef struct tagTHREADNAME_INFO
{
    DWORD dwType;     // must be 0x1000
    LPCSTR szName;    // pointer to name (in user address space)
    DWORD dwThreadID; // thread ID (-1 = caller thread)
    DWORD dwFlags;    // reserved for future use, must be zero
} THREADNAME_INFO;

void SetThreadName( DWORD dwThreadID, LPCSTR szThreadName )
{
    THREADNAME_INFO info;
    info.dwType = 0x1000;
    info.szName = szThreadName;
    info.dwThreadID = dwThreadID;
    info.dwFlags = 0;

    __try
    {
        RaiseException( 0x406D1388, 0,
                    sizeof(info) / sizeof(DWORD),
            (DWORD*)&info );
    }
    __except( EXCEPTION_CONTINUE_EXECUTION ) {
    }
}

// Example usage:
SetThreadName(-1, "Main thread");
```



<span data-ttu-id="ec98c-316">內核偵錯工具 (KD) 和 WinDBG 也支援多執行緒的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="ec98c-316">The kernel debugger (KD) and WinDBG also support multithreaded debugging.</span></span>

## <a name="testing"></a><span data-ttu-id="ec98c-317">測試</span><span class="sxs-lookup"><span data-stu-id="ec98c-317">Testing</span></span>

<span data-ttu-id="ec98c-318">多執行緒程式設計很難處理，而某些多執行緒 bug 只會顯示很少，因此難以尋找和修正。</span><span class="sxs-lookup"><span data-stu-id="ec98c-318">Multithreaded programming can be tricky, and some multithreaded bugs show up only rarely, making them difficult to find and fix.</span></span> <span data-ttu-id="ec98c-319">清除這些電腦的其中一個最佳方式，就是在各式各樣的電腦上進行測試，特別是有四個以上處理器的電腦。</span><span class="sxs-lookup"><span data-stu-id="ec98c-319">One of the best ways to flush them out is to test on a wide range of computers, particularly those with four or more processors.</span></span> <span data-ttu-id="ec98c-320">在單一執行緒電腦上完美運作的多執行緒程式碼，可能會在四個處理器的電腦上立即失敗。</span><span class="sxs-lookup"><span data-stu-id="ec98c-320">Multithreaded code that works perfectly on a single-threaded computer may fail instantly on a four-processor computer.</span></span> <span data-ttu-id="ec98c-321">AMD 和 Intel Cpu 的效能與時間特性有很大的差異，因此請務必根據兩個廠商的 Cpu，在多處理器電腦上進行測試。</span><span class="sxs-lookup"><span data-stu-id="ec98c-321">The performance and timing characteristics of AMD and Intel CPUs can vary substantially, so be sure to test on multiprocessor computers based on CPUs from both vendors.</span></span>

## <a name="windows-vista-and-windows-7-improvements"></a><span data-ttu-id="ec98c-322">Windows Vista 和 Windows 7 的增強功能</span><span class="sxs-lookup"><span data-stu-id="ec98c-322">Windows Vista and Windows 7 Improvements</span></span>

<span data-ttu-id="ec98c-323">針對以較新版本的 Windows 為目標的遊戲，有許多 Api 可簡化可擴充多執行緒應用程式的建立。</span><span class="sxs-lookup"><span data-stu-id="ec98c-323">For games targeting the newer versions of Windows, there are a number of APIs that can simplify the creation of scalable multithreaded applications.</span></span> <span data-ttu-id="ec98c-324">這特別適用于新的 ThreadPool API 和一些額外的 syncrhonziation 基本專案 (條件變數、超薄讀取/寫入器鎖定，以及一次性的初始化) 。</span><span class="sxs-lookup"><span data-stu-id="ec98c-324">This is particularly true with the new ThreadPool API and some additional syncrhonziation primitives (condition variables, the slim read/writer lock, and one-time initialization).</span></span> <span data-ttu-id="ec98c-325">您可以在下列 MSDN 雜誌文章中找到這些技術的總覽：</span><span class="sxs-lookup"><span data-stu-id="ec98c-325">You can find an overview of these technologies in the following MSDN Magazine articles:</span></span>

-   [<span data-ttu-id="ec98c-326">使用新的執行緒集區 Api 改進擴充性</span><span class="sxs-lookup"><span data-stu-id="ec98c-326">Improve Scalability With New Thread Pool APIs</span></span>](/archive/msdn-magazine/2007/october/pooled-threads-improve-scalability-with-new-thread-pool-apis)
-   [<span data-ttu-id="ec98c-327">Windows Vista 新的同步處理基本專案</span><span class="sxs-lookup"><span data-stu-id="ec98c-327">Synchronization Primitives New To Windows Vista</span></span>](/archive/msdn-magazine/2007/june/concurrency-synchronization-primitives-new-to-windows-vista)

<span data-ttu-id="ec98c-328">在這些作業系統上使用 [Direct3D 11 功能](../direct3d11/direct3d-11-features.md) 的應用程式，也可以利用新的並行物件建立和延後內容命令清單的設計，為多執行緒轉譯提供更好的擴充性。</span><span class="sxs-lookup"><span data-stu-id="ec98c-328">Applications using [Direct3D 11 Features](../direct3d11/direct3d-11-features.md) on these operating systems can also take advantage of the new design for concurrent object creation and deferred context command lists for better scalability for multithreaded rendering.</span></span>

## <a name="summary"></a><span data-ttu-id="ec98c-329">總結</span><span class="sxs-lookup"><span data-stu-id="ec98c-329">Summary</span></span>

<span data-ttu-id="ec98c-330">藉由將執行緒之間的互動降至最低的仔細設計，您可以從多執行緒程式設計獲得大幅的效能提升，而不會增加程式碼的複雜度。</span><span class="sxs-lookup"><span data-stu-id="ec98c-330">With careful design that minimizes the interactions between threads, you can get substantial performance gains from multithreaded programming without adding excessive complexity to your code.</span></span> <span data-ttu-id="ec98c-331">這可讓您的遊戲程式碼提供下一波的處理器改良功能，並提供更吸引人的遊戲體驗。</span><span class="sxs-lookup"><span data-stu-id="ec98c-331">This will let your game code ride the next wave of processor improvements and deliver ever more compelling gaming experiences.</span></span>

## <a name="references"></a><span data-ttu-id="ec98c-332">參考資料</span><span class="sxs-lookup"><span data-stu-id="ec98c-332">References</span></span>

-   <span data-ttu-id="ec98c-333">Jim Beveridge & Robert Weiner， *Win32 中的多執行緒應用程式*，Addison-Wesley，1997</span><span class="sxs-lookup"><span data-stu-id="ec98c-333">Jim Beveridge & Robert Weiner, *Multithreading Applications in Win32*, Addison-Wesley, 1997</span></span>
-   <span data-ttu-id="ec98c-334">Chuck Walbourn、 [遊戲計時和多核心處理器](./game-timing-and-multicore-processors.md)、Microsoft Corporation、2005</span><span class="sxs-lookup"><span data-stu-id="ec98c-334">Chuck Walbourn, [Game Timing and Multicore Processors](./game-timing-and-multicore-processors.md), Microsoft Corporation, 2005</span></span>
-   <span data-ttu-id="ec98c-335">MSDN Library： [ **GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)</span><span class="sxs-lookup"><span data-stu-id="ec98c-335">MSDN Library: [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)</span></span>
-   [<span data-ttu-id="ec98c-336">OpenMP</span><span class="sxs-lookup"><span data-stu-id="ec98c-336">OpenMP</span></span>](https://www.openmp.org/)

 

 