---
description: 持續性記憶體 (PM) 技術可提供非暫時性媒體的位元組層級存取，同時也能大幅減少儲存或取得資料的延遲。
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Windows 中的持續性記憶體程式設計-NVML 整合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194855"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a><span data-ttu-id="9b5b7-103">Windows 中的持續性記憶體程式設計-NVML 整合</span><span class="sxs-lookup"><span data-stu-id="9b5b7-103">Persistent Memory Programming in Windows - NVML Integration</span></span>

<span data-ttu-id="9b5b7-104">持續性記憶體 (PM) 技術可提供非暫時性媒體的位元組層級存取，同時也能大幅減少儲存或取得資料的延遲。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-104">Persistent memory (PM) technology provides byte-level access to non-volatile media while also reducing the latency of storing or retrieving data significantly.</span></span> <span data-ttu-id="9b5b7-105">它會在系統的記憶體和傳統儲存體之間建立新的層。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-105">It creates a new tier between a system’s memory and traditional storage.</span></span> <span data-ttu-id="9b5b7-106">任何相依于或透過快速寫入持續媒體進行調整的程式，都可以從 PM 獲益。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-106">Any program that is dependent on or scales with quick writes to a persistent medium can benefit from PM.</span></span>

<span data-ttu-id="9b5b7-107">本文的目的是要說明如何將非動態記憶體程式庫 (NVML) 整合到 Visual Studio 專案中，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-107">The purpose of this article is to outline how the non-volatile memory library (NVML) can be integrated into a Visual Studio project for easy use.</span></span>

> [!Note]  
> <span data-ttu-id="9b5b7-108">持續性記憶體有時也稱為儲存類別記憶體 (SCM) 。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-108">Persistent Memory is sometimes also referred to as Storage Class Memory (SCM).</span></span>

 

## <a name="pm-and-nvml"></a><span data-ttu-id="9b5b7-109">PM 和 NVML</span><span class="sxs-lookup"><span data-stu-id="9b5b7-109">PM and NVML</span></span>

<span data-ttu-id="9b5b7-110">持續性記憶體的第一次支援是在 Windows Server 2016 和 Windows 10 年度更新版 (1607) 引進。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-110">First support for persistent memory was introduced in Windows Server 2016 and the Windows 10 Anniversary Update (1607).</span></span> <span data-ttu-id="9b5b7-111">若要快速流覽，請參閱這兩個 Channel9 影片：</span><span class="sxs-lookup"><span data-stu-id="9b5b7-111">For a quick overview, check out these two Channel9 videos:</span></span>

-   [<span data-ttu-id="9b5b7-112">在 Windows Server 2016 中使用非揮發性記憶體 (NVDIMM-N) 做為區塊存放裝置</span><span class="sxs-lookup"><span data-stu-id="9b5b7-112">Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P466)
-   [<span data-ttu-id="9b5b7-113">在 Windows Server 2016 中使用非揮發性記憶體 (NVDIMM-N) 做為位元組可定址存放裝置</span><span class="sxs-lookup"><span data-stu-id="9b5b7-113">Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P470)

<span data-ttu-id="9b5b7-114">為了協助開發人員充分利用持續性記憶體供應專案的優點，Microsoft 也提供了將非動態記憶體程式庫 (NVML) 至 Windows 的工作。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-114">To help developers take advantage of the benefits persistent memory offers, Microsoft has also contributed to the efforts of bringing the non-volatile memory library (NVML) to Windows.</span></span> <span data-ttu-id="9b5b7-115">此程式庫提供各種工具，可讓應用程式持續記憶體感知。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-115">This library provides various tools to make applications persistent-memory aware.</span></span> <span data-ttu-id="9b5b7-116">例如，它包含的程式碼可讓您輕鬆地建立 PM 感知的索引鍵/值存放區，以取得非常快速的查閱和商店。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-116">For example, it contains code that lets you easily create a PM-aware key-value store for extremely fast look-ups and stores.</span></span> <span data-ttu-id="9b5b7-117">您可以在 [NVM 程式庫](https://pmem.io/nvml/)中找到 NVML 的詳細資訊，包括範例。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-117">You can find more information on NVML, including samples, at [NVM Library](https://pmem.io/nvml/).</span></span>

## <a name="integrating-nvml-into-a-visual-studio-project"></a><span data-ttu-id="9b5b7-118">將 NVML 整合到 Visual Studio 專案中</span><span class="sxs-lookup"><span data-stu-id="9b5b7-118">Integrating NVML into a Visual Studio Project</span></span>

1. <span data-ttu-id="9b5b7-119">下載 NVML 程式庫檔案和標頭</span><span class="sxs-lookup"><span data-stu-id="9b5b7-119">Download NVML library files and headers</span></span>

-   <span data-ttu-id="9b5b7-120">NVML 會在 GitHub 上進行維護。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-120">NVML is maintained on GitHub.</span></span> <span data-ttu-id="9b5b7-121">您可以自行編譯來源，或直接從這裡下載已編譯的二進位檔： [NVML 1.2 版-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1)。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-121">You can either compile the source yourself, or just download compiled binaries directly from here: [NVML Version 1.2 - Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span></span>

2. <span data-ttu-id="9b5b7-122">將程式庫檔案和標頭放在您選擇的目錄中，例如： "C： \\ NVML \\ lib" 和 "c： \\ NVML \\ inc."。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-122">Place the library files and headers in a directory of your choosing, for example: “C:\\NVML\\lib” and “C:\\NVML\\inc” respectively.</span></span>

3. <span data-ttu-id="9b5b7-123">設定您的專案，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9b5b7-123">Configure your project as follows:</span></span>

-   <span data-ttu-id="9b5b7-124">開啟您的 visual studio 專案，然後在 [方案總管] 中，以滑鼠右鍵按一下您的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-124">Open your visual studio project and in the “Solution Explorer” right-click on your project’s name.</span></span>
-   <span data-ttu-id="9b5b7-125">在產生的快顯視窗底部開啟專案的 [設定] 窗格。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-125">Open the project’s setting pane at the bottom of the resulting pop-up.</span></span>
-   <span data-ttu-id="9b5b7-126">流覽至 [設定屬性-> C/c + +]，然後將儲存標頭的資料夾 (C： \\ NVML \\ inc.) 新增至 [其他 Include 目錄] 欄位。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-126">Navigate to “Configuration Properties -> C/C++” and add the folder in which you stored the header (C:\\NVML\\inc) to the “Additional Include Directories” field.</span></span>
-   <span data-ttu-id="9b5b7-127">接下來，流覽至 [設定內容-> 連結器]，然後將儲存程式庫的資料夾 (C： \\ NVML \\ lib) 新增至 [其他程式庫目錄] 欄位</span><span class="sxs-lookup"><span data-stu-id="9b5b7-127">Next, navigate to “Configuration Properties -> Linker” and add the folder in which you stored the library (C:\\NVML\\lib) to the “Additional Library Directories” field</span></span>

4. <span data-ttu-id="9b5b7-128">接下來，請確定您將目標設為 Windows Server 2016 或 Windows 10 年度更新版的專案：</span><span class="sxs-lookup"><span data-stu-id="9b5b7-128">Next, make sure you target the project for Windows Server 2016 or Windows 10 Anniversary Update:</span></span>

-   <span data-ttu-id="9b5b7-129">流覽至 [設定屬性-> 一般]，並將 [目標平臺版本] 欄位設定為 "10.0.14393.0" 和</span><span class="sxs-lookup"><span data-stu-id="9b5b7-129">Navigate to “Configuration Properties -> General” and set the “Target Platform Version” field to “10.0.14393.0” and</span></span>
-   <span data-ttu-id="9b5b7-130">流覽至 [設定屬性-> C/c + +]，然後將 [NTDDI \_ VERSION = NTDDI \_ WIN10 \_ RS1;] 新增至 [預處理器] 欄位。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-130">Navigate to “Configuration Properties -> C/C++” and add “NTDDI\_VERSION=NTDDI\_WIN10\_RS1;” to the “Preprocessor” field.</span></span>

5. <span data-ttu-id="9b5b7-131">在您的程式碼中包含標頭，並連結至所需的程式庫</span><span class="sxs-lookup"><span data-stu-id="9b5b7-131">Include the headers in your code and link to the required libraries</span></span>

-   <span data-ttu-id="9b5b7-132">至此，您可以直接在程式碼中包含您想要在程式碼中使用的標頭檔，就像任何其他標頭檔一樣。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-132">At this point, you can simply include the header files you are looking to use in your code like any other header files.</span></span> <span data-ttu-id="9b5b7-133">例如，若要使用 libpmem：</span><span class="sxs-lookup"><span data-stu-id="9b5b7-133">For example, to use libpmem:</span></span>
    -   <span data-ttu-id="9b5b7-134">新增 " \# include <libpmem .h>" 和</span><span class="sxs-lookup"><span data-stu-id="9b5b7-134">add "\#include <libpmem.h>" and</span></span>
    -   <span data-ttu-id="9b5b7-135">將 "libpmem" 新增至 [設定屬性-> 連結器-> 輸入-> 其他相依性]</span><span class="sxs-lookup"><span data-stu-id="9b5b7-135">add "libpmem.lib" to "Configuration Properties -> Linker -> Input -> Additional Dependencies"</span></span>

<span data-ttu-id="9b5b7-136">至此，您已準備好直接在程式碼中呼叫程式庫的函式，並利用這些函式。</span><span class="sxs-lookup"><span data-stu-id="9b5b7-136">At this point you are ready to call the library’s functions directly in your code and take advantage of them.</span></span>

 

 



