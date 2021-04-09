---
title: 上傳最佳作法
description: Highloads 可能會導致各種伺服器超時狀況，而這可能會在用戶端重試時增加負載。
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020895"
---
# <a name="upload-best-practices"></a><span data-ttu-id="c68f4-103">上傳最佳作法</span><span class="sxs-lookup"><span data-stu-id="c68f4-103">Upload Best Practices</span></span>

<span data-ttu-id="c68f4-104">Highloads 可能會導致各種伺服器超時狀況，而這可能會在用戶端重試時增加負載。</span><span class="sxs-lookup"><span data-stu-id="c68f4-104">Highloads may cause various server timeout conditions, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="c68f4-105">此外，大量未完成的連接將會耗用更多的伺服器資源，讓情況更糟。</span><span class="sxs-lookup"><span data-stu-id="c68f4-105">Also, a large number of outstanding connections will consume more server resources and make the situation worse.</span></span> <span data-ttu-id="c68f4-106">最重要的是，如果後端應用程式未撰寫來處理高負載狀況，可能會損毀或不正確的行為。</span><span class="sxs-lookup"><span data-stu-id="c68f4-106">On top of that, if backend app is not written to handle high load conditions, it may crash or mal-behave.</span></span> <span data-ttu-id="c68f4-107">應用程式應該執行下列步驟來限制後端的負載。</span><span class="sxs-lookup"><span data-stu-id="c68f4-107">The app shall perform the following steps to limit the load on the backend.</span></span>

<span data-ttu-id="c68f4-108">如果未撰寫伺服器應用程式來處理大量磁片區，則可能會發生 timeout 狀況，而這可能會在用戶端重試時增加負載。</span><span class="sxs-lookup"><span data-stu-id="c68f4-108">If the server application is not written to handle high volumes, timeout conditions may occur, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="c68f4-109">此外，大量未完成的連接將會耗用更多的伺服器資源。</span><span class="sxs-lookup"><span data-stu-id="c68f4-109">Also, a large number of outstanding connections will consume more server resources.</span></span>

<span data-ttu-id="c68f4-110">測試您的伺服器應用程式時，盡可能測試最高的負載。</span><span class="sxs-lookup"><span data-stu-id="c68f4-110">When testing your server application, test with highest load possible.</span></span> <span data-ttu-id="c68f4-111">您應使用多部用戶端電腦，每個都有數個並行的前景位作業，並測量後端的最大輸送量。</span><span class="sxs-lookup"><span data-stu-id="c68f4-111">You should use multiple client machines, each with several concurrent, foreground BITS jobs, and measure the maximum throughput at the backend.</span></span> <span data-ttu-id="c68f4-112">如果您無法測量輸送量，就必須估計輸送量。</span><span class="sxs-lookup"><span data-stu-id="c68f4-112">If you cannot measure the throughput, you will have to estimate the throughput.</span></span>

<span data-ttu-id="c68f4-113">伺服器應用程式應該位於與上傳 URL 不同的 URL (查看 BITS IIS 屬性 **BITSServerNotificationURL**) 。</span><span class="sxs-lookup"><span data-stu-id="c68f4-113">The server application should reside on a different URL from the upload URL (see the BITS IIS property, **BITSServerNotificationURL**).</span></span>

<span data-ttu-id="c68f4-114">最好的作法是根據經證實的輸送量值限制應用程式伺服器上的負載。</span><span class="sxs-lookup"><span data-stu-id="c68f4-114">It is good practice to limit the load on the application server based on proven throughput values.</span></span> <span data-ttu-id="c68f4-115">您應使用 IIS 屬性（ **MaxBandwidth** 和 **MaxConnections**）來限制應用程式伺服器上的負載。</span><span class="sxs-lookup"><span data-stu-id="c68f4-115">You should use the IIS properties, **MaxBandwidth** and **MaxConnections**, to limit the load on the application server.</span></span>

 

 




