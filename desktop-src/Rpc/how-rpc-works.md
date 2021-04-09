---
title: RPC 的運作方式
description: RPC 工具會讓使用者看起來像用戶端直接呼叫位於遠端伺服器程式中的程式一樣。
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674088"
---
# <a name="how-rpc-works"></a><span data-ttu-id="bec68-103">RPC 的運作方式</span><span class="sxs-lookup"><span data-stu-id="bec68-103">How RPC Works</span></span>

<span data-ttu-id="bec68-104">RPC 工具會讓使用者看起來像用戶端直接呼叫位於遠端伺服器程式中的程式一樣。</span><span class="sxs-lookup"><span data-stu-id="bec68-104">The RPC tools make it appear to users as though a client directly calls a procedure located in a remote server program.</span></span> <span data-ttu-id="bec68-105">用戶端和伺服器都有自己的位址空間;也就是說，每個都有自己的記憶體資源，配置給程式所使用的資料。</span><span class="sxs-lookup"><span data-stu-id="bec68-105">The client and server each have their own address spaces; that is, each has its own memory resource allocated to data used by the procedure.</span></span> <span data-ttu-id="bec68-106">下圖說明 RPC 架構。</span><span class="sxs-lookup"><span data-stu-id="bec68-106">The following figure illustrates the RPC architecture.</span></span>

![rpc 架構](images/prog-a11.png)

<span data-ttu-id="bec68-108">如圖所示，用戶端應用程式會呼叫本機存根程式，而不是實際執行程式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="bec68-108">As the illustration shows, the client application calls a local stub procedure instead of the actual code implementing the procedure.</span></span> <span data-ttu-id="bec68-109">系統會使用用戶端應用程式來編譯和連結存根。</span><span class="sxs-lookup"><span data-stu-id="bec68-109">Stubs are compiled and linked with the client application.</span></span> <span data-ttu-id="bec68-110">用戶端 stub 程式碼，而不是包含實際執行遠端程式的程式碼：</span><span class="sxs-lookup"><span data-stu-id="bec68-110">Instead of containing the actual code that implements the remote procedure, the client stub code:</span></span>

-   <span data-ttu-id="bec68-111">從用戶端位址空間抓取必要的參數。</span><span class="sxs-lookup"><span data-stu-id="bec68-111">Retrieves the required parameters from the client address space.</span></span>
-   <span data-ttu-id="bec68-112">視需要將參數轉譯成標準的 NDR 格式，以便透過網路傳輸。</span><span class="sxs-lookup"><span data-stu-id="bec68-112">Translates the parameters as needed into a standard NDR format for transmission over the network.</span></span>
-   <span data-ttu-id="bec68-113">呼叫 RPC 用戶端執行時間程式庫中的函式，以將要求和其參數傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="bec68-113">Calls functions in the RPC client run-time library to send the request and its parameters to the server.</span></span>

<span data-ttu-id="bec68-114">伺服器會執行下列步驟來呼叫遠端程式。</span><span class="sxs-lookup"><span data-stu-id="bec68-114">The server performs the following steps to call the remote procedure.</span></span>

1.  <span data-ttu-id="bec68-115">Server RPC 執行時間程式庫函式會接受要求並呼叫伺服器 stub 程式。</span><span class="sxs-lookup"><span data-stu-id="bec68-115">The server RPC run-time library functions accept the request and call the server stub procedure.</span></span>
2.  <span data-ttu-id="bec68-116">伺服器 stub 會從網路緩衝區取出參數，並將它們從網路傳輸格式轉換成伺服器所需的格式。</span><span class="sxs-lookup"><span data-stu-id="bec68-116">The server stub retrieves the parameters from the network buffer and converts them from the network transmission format to the format the server needs.</span></span>
3.  <span data-ttu-id="bec68-117">伺服器 stub 會呼叫伺服器上的實際程式。</span><span class="sxs-lookup"><span data-stu-id="bec68-117">The server stub calls the actual procedure on the server.</span></span>

<span data-ttu-id="bec68-118">接著會執行遠端程式，可能產生輸出參數和傳回值。</span><span class="sxs-lookup"><span data-stu-id="bec68-118">The remote procedure then runs, possibly generating output parameters and a return value.</span></span> <span data-ttu-id="bec68-119">當遠端程式完成時，類似的步驟順序會將資料傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="bec68-119">When the remote procedure is complete, a similar sequence of steps returns the data to the client.</span></span>

1.  <span data-ttu-id="bec68-120">遠端過程會將其資料傳回到伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="bec68-120">The remote procedure returns its data to the server stub.</span></span>
2.  <span data-ttu-id="bec68-121">伺服器 stub 會將輸出參數轉換成透過網路傳輸所需的格式，並將它們傳回至 RPC 執行時間程式庫函式。</span><span class="sxs-lookup"><span data-stu-id="bec68-121">The server stub converts output parameters to the format required for transmission over the network and returns them to the RPC run-time library functions.</span></span>
3.  <span data-ttu-id="bec68-122">伺服器 RPC 執行時間程式庫函式會將網路上的資料傳輸至用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="bec68-122">The server RPC run-time library functions transmit the data on the network to the client computer.</span></span>

<span data-ttu-id="bec68-123">用戶端會透過網路接受資料，並將它傳回給呼叫的函式，來完成此程式。</span><span class="sxs-lookup"><span data-stu-id="bec68-123">The client completes the process by accepting the data over the network and returning it to the calling function.</span></span>

1.  <span data-ttu-id="bec68-124">用戶端 RPC 執行時間程式庫會接收遠端過程的傳回值，並將它們傳回至用戶端存根。</span><span class="sxs-lookup"><span data-stu-id="bec68-124">The client RPC run-time library receives the remote-procedure return values and returns them to the client stub.</span></span>
2.  <span data-ttu-id="bec68-125">用戶端 stub 會將資料從其 NDR 轉換成用戶端電腦所使用的格式。</span><span class="sxs-lookup"><span data-stu-id="bec68-125">The client stub converts the data from its NDR to the format used by the client computer.</span></span> <span data-ttu-id="bec68-126">存根會將資料寫入至用戶端記憶體，並將結果傳回用戶端上的呼叫程式。</span><span class="sxs-lookup"><span data-stu-id="bec68-126">The stub writes data into the client memory and returns the result to the calling program on the client.</span></span>
3.  <span data-ttu-id="bec68-127">呼叫程式會繼續執行，就像是在同一部電腦上呼叫程式一樣。</span><span class="sxs-lookup"><span data-stu-id="bec68-127">The calling procedure continues as if the procedure had been called on the same computer.</span></span>

<span data-ttu-id="bec68-128">執行時間程式庫提供兩個部分：與應用程式連結的匯入程式庫，以及會實作為動態連結程式庫 (DLL) 的 RPC 執行時間程式庫。</span><span class="sxs-lookup"><span data-stu-id="bec68-128">The run-time libraries are provided in two parts: an import library, which is linked with the application and the RPC run-time library, which is implemented as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="bec68-129">伺服器應用程式包含伺服器執行時間程式庫函式的呼叫，這些函數會註冊伺服器的介面，並允許伺服器接受遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="bec68-129">The server application contains calls to the server run-time library functions which register the server's interface and allow the server to accept remote procedure calls.</span></span> <span data-ttu-id="bec68-130">伺服器應用程式也包含用戶端應用程式所呼叫的應用程式特定的遠端程式。</span><span class="sxs-lookup"><span data-stu-id="bec68-130">The server application also contains the application-specific remote procedures that are called by the client applications.</span></span>

 

 




