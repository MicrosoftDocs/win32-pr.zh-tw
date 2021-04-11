---
description: 資料的本機快取是用來加速網路存取資料檔案的技巧。 它牽涉到在用戶端上快取資料，而不是在伺服器上快取資料。
ms.assetid: a7eb24b3-7e23-4798-8584-30a171fa4f04
title: 本機快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8132bc51831db752422de1e3071ee3ef0b33a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852119"
---
# <a name="local-caching"></a><span data-ttu-id="80bdb-104">本機快取</span><span class="sxs-lookup"><span data-stu-id="80bdb-104">Local Caching</span></span>

<span data-ttu-id="80bdb-105">資料的 *本機* 快取是用來加速網路存取資料檔案的技巧。</span><span class="sxs-lookup"><span data-stu-id="80bdb-105">*Local caching* of data is a technique used to speed network access to data files.</span></span> <span data-ttu-id="80bdb-106">它牽涉到在用戶端上快取資料，而不是在伺服器上快取資料。</span><span class="sxs-lookup"><span data-stu-id="80bdb-106">It involves caching data on clients rather than on servers when possible.</span></span>

<span data-ttu-id="80bdb-107">本機快取的作用是允許在檔案的相同區域上進行多個寫入作業，以合併到整個網路的一項寫入作業。</span><span class="sxs-lookup"><span data-stu-id="80bdb-107">The effect of local caching is that it allows multiple write operations on the same region of a file to be combined into one write operation across the network.</span></span> <span data-ttu-id="80bdb-108">本機快取會減少網路流量，因為資料會寫入一次。</span><span class="sxs-lookup"><span data-stu-id="80bdb-108">Local caching reduces network traffic because the data is written once.</span></span> <span data-ttu-id="80bdb-109">這類快取可改善應用程式的明顯回應時間，因為應用程式不會等待資料透過網路傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="80bdb-109">Such caching improves the apparent response time of applications because the applications do not wait for the data to be sent across the network to the server.</span></span>

<span data-ttu-id="80bdb-110">要讀取之資料的本機快取可能會出現，藉由向前讀取來加速作業。</span><span class="sxs-lookup"><span data-stu-id="80bdb-110">Local caching of data to be read can appear to speed things up by means of reading ahead.</span></span> <span data-ttu-id="80bdb-111">一個簡單的範例是依序存取資料的應用程式，例如編譯器的預處理器。</span><span class="sxs-lookup"><span data-stu-id="80bdb-111">A simple example is an application accessing data sequentially, such as a compiler's preprocessor.</span></span> <span data-ttu-id="80bdb-112">在這種情況下，作業系統的網路層會在應用程式要求資料之前，先在網路中讀取資料。</span><span class="sxs-lookup"><span data-stu-id="80bdb-112">In such cases, the network layer of the operating system reads data across the network before the application requests the data.</span></span> <span data-ttu-id="80bdb-113">在理想的情況下，網路會在應用程式從檔案系統要求資料之前提供資料，進而產生近乎即時的回應。</span><span class="sxs-lookup"><span data-stu-id="80bdb-113">Ideally, the network delivers the data before the application requests it from the file system, resulting in near-instantaneous response.</span></span> <span data-ttu-id="80bdb-114">在實務上，這種情況很少發生，但通常會藉由預期下一個要求來事先讀取應用程式。</span><span class="sxs-lookup"><span data-stu-id="80bdb-114">In practice, this rarely happens, but often reading ahead speeds applications by anticipating the next request.</span></span>

<span data-ttu-id="80bdb-115">本機快取也有助於減少網路流量，方法是在網路上讀取部分檔案，然後將它保留在本機快取中。</span><span class="sxs-lookup"><span data-stu-id="80bdb-115">Local caching can also help reduce network traffic by reading a portion of a file across the network once and then keeping it in the local cache.</span></span> <span data-ttu-id="80bdb-116">應用程式從本機快取讀取的後續讀取作業。</span><span class="sxs-lookup"><span data-stu-id="80bdb-116">Subsequent read operations on that portion by the application read from the local cache.</span></span>

<span data-ttu-id="80bdb-117">有一種可受益于本機快取的應用程式是批次檔。</span><span class="sxs-lookup"><span data-stu-id="80bdb-117">One type of application that can benefit from local caching is batch files.</span></span> <span data-ttu-id="80bdb-118">命令處理器一次讀取和執行批次檔一次。</span><span class="sxs-lookup"><span data-stu-id="80bdb-118">Command processors read and execute a batch file one line at a time.</span></span> <span data-ttu-id="80bdb-119">在每一行中，命令處理器都會開啟檔案、搜尋行的開頭、盡可能讀取檔案、關閉檔案，然後執行該行。</span><span class="sxs-lookup"><span data-stu-id="80bdb-119">For each line, the command processor opens the file, searches to the beginning of the line, reads as much as it needs, closes the file, then executes the line.</span></span> <span data-ttu-id="80bdb-120">每一行都會產生大量的網路流量。</span><span class="sxs-lookup"><span data-stu-id="80bdb-120">Each line results in a lot of network traffic.</span></span> <span data-ttu-id="80bdb-121">藉由快取用戶端上的整個批次檔，可以大幅減少網路流量。</span><span class="sxs-lookup"><span data-stu-id="80bdb-121">Network traffic can be reduced considerably by caching the entire batch file on a client.</span></span>

<span data-ttu-id="80bdb-122">本機快取也有助於解決與網路相關的其他問題，尤其是透過數據機和其他精簡管道執行工作的網路：回應時間變慢。</span><span class="sxs-lookup"><span data-stu-id="80bdb-122">Local caching also helps with another problem associated with networks, especially networks that perform work over modems and other thin pipes: slow response time.</span></span> <span data-ttu-id="80bdb-123">使用者不想等待資料透過網路抓取、修改後再回寫。</span><span class="sxs-lookup"><span data-stu-id="80bdb-123">Users do not want to wait while data is retrieved over the network, modified, and then written back.</span></span> <span data-ttu-id="80bdb-124">在預先讀取和寫入快取的情況下，這些函式的運作速度會比實際執行的速度快很多。</span><span class="sxs-lookup"><span data-stu-id="80bdb-124">With reading ahead and write caching, it often appears that these functions operate much faster than they actually do.</span></span>

<span data-ttu-id="80bdb-125">本機快取的風險是，只要用戶端上快取資料，寫入的資料就會與用戶端本身的完整性一樣多。</span><span class="sxs-lookup"><span data-stu-id="80bdb-125">A hazard of local caching is that written data only has as much integrity as the client itself for as long as the data is cached on the client.</span></span> <span data-ttu-id="80bdb-126">一般而言，本機快取的資料應該儘快排清到伺服器。</span><span class="sxs-lookup"><span data-stu-id="80bdb-126">In general, locally cached data should be flushed to the server as soon as possible.</span></span> <span data-ttu-id="80bdb-127">使用新式作業系統和硬體支援（例如不斷電供應系統供應器）時，將會降低遺失本機快取資料的風險。</span><span class="sxs-lookup"><span data-stu-id="80bdb-127">With modern operating systems and hardware support such as uninterruptible power supplies, the risk of losing locally cached data is reduced.</span></span> <span data-ttu-id="80bdb-128">但是風險仍然存在，而且您應該考慮資料完整性和明顯回應速度之間的取捨，以及資料完整性與減少網路流量之間的取捨。</span><span class="sxs-lookup"><span data-stu-id="80bdb-128">But the risk still exists, and you should consider both the trade-off between data integrity and apparent response speed and the trade-off between data integrity and reduced network traffic.</span></span>

 

 



