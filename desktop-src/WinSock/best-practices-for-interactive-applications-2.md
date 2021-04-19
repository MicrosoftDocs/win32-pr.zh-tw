---
description: 在變形生命資料格更新程式碼時，已發現數個撰寫高效能網路應用程式的指導方針。
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: 互動式應用程式的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972633"
---
# <a name="best-practices-for-interactive-applications"></a><span data-ttu-id="8946b-103">互動式應用程式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="8946b-103">Best Practices for Interactive Applications</span></span>

<span data-ttu-id="8946b-104">在變形生命資料格更新程式碼時，已發現數個撰寫高效能網路應用程式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="8946b-104">In morphing the Life cell update code, several guidelines for writing high performance network applications have been uncovered.</span></span> <span data-ttu-id="8946b-105">撰寫這些類型的應用程式時適用的一些一般策略如下：</span><span class="sxs-lookup"><span data-stu-id="8946b-105">Some general strategies to apply when writing these types of applications are:</span></span>

-   <span data-ttu-id="8946b-106">盡可能讓資料流程，而不是傳入區塊。</span><span class="sxs-lookup"><span data-stu-id="8946b-106">Make the data stream as much as possible, rather than going in chunks.</span></span>
-   <span data-ttu-id="8946b-107">使用一些大型交易，而不是許多小型交易。</span><span class="sxs-lookup"><span data-stu-id="8946b-107">Use a few large transactions rather than many small ones.</span></span> <span data-ttu-id="8946b-108">大型交易也可以有效率地進行資料流程處理。</span><span class="sxs-lookup"><span data-stu-id="8946b-108">Large transactions can also be efficiently streamed.</span></span>
-   <span data-ttu-id="8946b-109">辨識網路是很慢且不可靠的資源，並開發每個應用程式，以將其對網路的依賴降至最低。</span><span class="sxs-lookup"><span data-stu-id="8946b-109">Recognize that the network is a slow, unreliable resource and develop each application to minimize its reliance on the network.</span></span>
-   <span data-ttu-id="8946b-110">在網路上使用架構良好的資料標記法。</span><span class="sxs-lookup"><span data-stu-id="8946b-110">Use a well-architected representation of the data on the network.</span></span> <span data-ttu-id="8946b-111">資料標記法應該是電腦架構中立、不包含 fat，而且可能會壓縮。</span><span class="sxs-lookup"><span data-stu-id="8946b-111">The data representation should be computer-architecture agnostic, contain no fat, and possibly be compressed.</span></span>
-   <span data-ttu-id="8946b-112">在初始化和關閉期間，請不要讓使用者等待網路啟動或關閉。</span><span class="sxs-lookup"><span data-stu-id="8946b-112">During initialization and shutdown, do not make the user wait for the network to start up or shut down.</span></span> <span data-ttu-id="8946b-113">網路相關的初始化可能需要相當長的時間。</span><span class="sxs-lookup"><span data-stu-id="8946b-113">Network related initialization could take a relatively long time.</span></span> <span data-ttu-id="8946b-114">分隔非關鍵性的網路程式碼。</span><span class="sxs-lookup"><span data-stu-id="8946b-114">Separate the noncritical network code.</span></span>
-   <span data-ttu-id="8946b-115">適當地處理其影響的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8946b-115">Handle errors as appropriate to their impact.</span></span> <span data-ttu-id="8946b-116">並非所有的錯誤都很重要。</span><span class="sxs-lookup"><span data-stu-id="8946b-116">Not all errors are critical.</span></span> <span data-ttu-id="8946b-117">執行復原機制並提供不造成干擾的使用者意見反應。</span><span class="sxs-lookup"><span data-stu-id="8946b-117">Implement recovery mechanisms and provide nonintrusive user feedback.</span></span>
-   <span data-ttu-id="8946b-118">只有在適當時，才 (RPC) 使用遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="8946b-118">Use remote procedure calls (RPC) only when appropriate.</span></span> <span data-ttu-id="8946b-119">RPC 在 Windows Me/98 上是同步的，而且在用來傳送少量資料的情況下，一律會產生多對話、fat 的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8946b-119">RPC is synchronous on Windows Me/98 and always results in chatty, fat protocols when used to send small amounts of data.</span></span>
-   <span data-ttu-id="8946b-120">使用 Netstat 測量您的網路額外負荷;您可能會對度量所顯示的內容感到驚訝。</span><span class="sxs-lookup"><span data-stu-id="8946b-120">Measure your network overhead using Netstat; you may be surprised at what your measurements reveal.</span></span>
-   <span data-ttu-id="8946b-121">在各式各樣的網路上測試應用程式，尤其是緩慢或易失的網路。</span><span class="sxs-lookup"><span data-stu-id="8946b-121">Test the application on a variety of networks, especially slow or loss-prone networks.</span></span> <span data-ttu-id="8946b-122">無線區域網路網路、數據機和虛擬私人網路 (VPN) 在網際網路上，是很好的網路來進行測試。</span><span class="sxs-lookup"><span data-stu-id="8946b-122">Wireless LAN networks, modems, and virtual private networks (VPN) over the Internet are good networks for testing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8946b-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="8946b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8946b-124">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="8946b-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



