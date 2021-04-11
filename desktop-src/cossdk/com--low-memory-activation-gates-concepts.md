---
description: COM + 嘗試防止這些錯誤路徑必須在伺服器上執行的情況。
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: COM + Low-Memory 啟用管制概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d844a0492301ef067f5b3cd0e0749ec3a21779
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "103945551"
---
# <a name="com-low-memory-activation-gates-concepts"></a><span data-ttu-id="2c8a0-103">COM + Low-Memory 啟用管制概念</span><span class="sxs-lookup"><span data-stu-id="2c8a0-103">COM+ Low-Memory Activation Gates Concepts</span></span>

<span data-ttu-id="2c8a0-104">一般而言，如果您有單一執行緒的單元 (STA) ，就不需要同步處理，因為該單元會為您提供同步處理。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-104">Generally, synchronization is not required when you have a single-threaded apartment (STA) because the apartment provides the synchronization for you.</span></span> <span data-ttu-id="2c8a0-105">當您有多執行緒單元 (MTA) 和無限制執行緒物件時，同步處理就會變得很重要。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-105">Synchronization becomes important when you have a multithreaded apartment (MTA) and a free-threaded object.</span></span> <span data-ttu-id="2c8a0-106">在過去，無限制執行緒物件必須處理鎖定。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-106">In the past, free-threaded objects have had to handle locking.</span></span> <span data-ttu-id="2c8a0-107">您可以藉由設定元件的同步處理屬性，來消除使用鎖定的需求。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-107">You can eliminate the need to use locking by setting the synchronization attribute for a component.</span></span>

<span data-ttu-id="2c8a0-108">當伺服器的資源無法有效率地回應尖峰負載時，通常就會發生可靠性問題。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-108">Reliability problems often occur when a server's resources cannot react efficiently to peak loads.</span></span> <span data-ttu-id="2c8a0-109">當伺服器沒有足夠的實體資源可以滿足尖峰需求時，它可能會耗盡虛擬記憶體。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-109">When a server doesn't have enough physical resources to meet peak demand, it can exhaust virtual memory.</span></span> <span data-ttu-id="2c8a0-110">如果使用者的程式碼或系統程式碼未正確處理記憶體配置失敗，就會發生問題。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-110">This becomes a problem if the user code or system code does not properly handle memory allocation failures.</span></span> <span data-ttu-id="2c8a0-111">伺服器開始變慢，而且當記憶體用盡時，記憶體配置會失敗。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-111">The server begins to slow down, and as memory is exhausted, memory allocations fail.</span></span> <span data-ttu-id="2c8a0-112">伺服器會執行錯誤路徑來處理配置失敗。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-112">The server executes error paths to handle the allocation failures.</span></span> <span data-ttu-id="2c8a0-113">如果錯誤路徑包含在伺服器上執行的系統或使用者程式碼中的錯誤，則很難安全地進行陷阱和處理。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-113">If an error path contains a bug in the system or user code running on the server, it's extremely difficult to trap and handle safely.</span></span>

<span data-ttu-id="2c8a0-114">COM + 嘗試防止這些錯誤路徑必須在伺服器上執行的情況。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-114">COM+ attempts to prevent situations in which these error paths have to be executed on a server.</span></span> <span data-ttu-id="2c8a0-115">透過低記憶體啟動閘道功能，COM + 會主動監視系統中的記憶體負載，並確保在執行使用者程式碼之前，有合理的可用記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-115">Through the low-memory activation gates feature, COM+ proactively monitors memory load in the system and ensures that a reasonable amount of memory is available before executing user code.</span></span> <span data-ttu-id="2c8a0-116">如果應用程式可用的虛擬記憶體百分比低於固定的臨界值，則在建立 COM + 伺服器應用程式或物件之前，啟用會失敗 (，如下圖所示) 。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-116">If the percentage of virtual memory available to the application falls below a fixed threshold, the activation fails before a COM+ server application or object is created (as shown in the illustration below).</span></span> <span data-ttu-id="2c8a0-117">藉由容錯移轉通常會執行的啟用，低記憶體啟用閘道功能可將使用者程式碼中與記憶體配置相關的問題降至最低，進而大幅提高系統可靠性。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-117">By failing these activations that would normally run, the low-memory activation gates feature minimizes the problems associated with memory allocations in user code, which significantly enhances system reliability.</span></span>

![顯示 COM + 應用程式與低記憶體啟用閘道之間關聯性的圖表。](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

<span data-ttu-id="2c8a0-119">低記憶體啟用閘道功能只適用于已安裝在 COM + 應用程式中的已設定 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-119">The low-memory activation gates feature applies only to configured COM components that are installed in a COM+ application.</span></span>

## <a name="how-the-low-memory-activation-gates-feature-works"></a><span data-ttu-id="2c8a0-120">Low-Memory 啟用閘道功能的運作方式</span><span class="sxs-lookup"><span data-stu-id="2c8a0-120">How the Low-Memory Activation Gates Feature Works</span></span>

<span data-ttu-id="2c8a0-121">根據啟用類型而定，低記憶體啟用閘道功能會使用不同的固定閾值層級。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-121">The low-memory activation gates feature uses a different fixed threshold level depending on the type of activation.</span></span> <span data-ttu-id="2c8a0-122">建立 COM + 伺服器應用程式時，如果有10% 以上的虛擬記憶體可用，COM + 允許啟用。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-122">When creating a COM+ server application, COM+ allows the activation if more than 10 percent of virtual memory is available.</span></span> <span data-ttu-id="2c8a0-123">如果有少於10% 的可用，COM + 會進行測試組態，以找出分頁檔是否可以擴充以容納新的記憶體負載。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-123">If less than 10 percent is available, COM+ makes a test allocation to find out if the paging file can expand to accommodate the new memory load.</span></span> <span data-ttu-id="2c8a0-124">如果分頁檔案展開，則會建立伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-124">If the paging file expands, the server application is created.</span></span> <span data-ttu-id="2c8a0-125">如果無法展開分頁檔案，啟用將會失敗，而且不會配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-125">If the paging file cannot be expanded, the activation fails and memory is not allocated.</span></span>

<span data-ttu-id="2c8a0-126">建立物件時，此程式很類似。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-126">The process is similar when creating an object.</span></span> <span data-ttu-id="2c8a0-127">在此情況下，如果有超過5% 的可用虛擬記憶體，COM + 允許啟用。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-127">In this case, COM+ allows the activation if more than 5 percent of virtual memory is available.</span></span> <span data-ttu-id="2c8a0-128">如果有少於5% 的可用，COM + 會繼續進行測試組態。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-128">If less than 5 percent is available, COM+ proceeds with a test allocation.</span></span> <span data-ttu-id="2c8a0-129">同樣地，如果測試組態會展開分頁檔案，就會建立物件。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-129">Again, if the test allocation expands the paging file, the object is created.</span></span> <span data-ttu-id="2c8a0-130">如果不是，啟用就會失敗。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-130">If not, the activation fails.</span></span>

<span data-ttu-id="2c8a0-131">低記憶體啟用閘道的固定閾值層級目前無法設定。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-131">The fixed threshold levels for low-memory activation gates are currently not configurable.</span></span> <span data-ttu-id="2c8a0-132">基於這個理由，沒有與這項功能相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="2c8a0-132">For this reason, there are no tasks associated with this feature.</span></span>

 

 



