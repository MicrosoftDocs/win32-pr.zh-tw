---
description: Windows 上的本機 i/o 和網路 i/o 之間的差異。
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: 本機和網路 i/o 的差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987600"
---
# <a name="differences-in-local-and-network-io"></a><span data-ttu-id="73d5f-103">本機和網路 i/o 的差異</span><span class="sxs-lookup"><span data-stu-id="73d5f-103">Differences in Local and Network I/O</span></span>

<span data-ttu-id="73d5f-104">在 Windows 上的本機 i/o 和網路 i/o 之間有一些顯著的差異：</span><span class="sxs-lookup"><span data-stu-id="73d5f-104">There are some notable differences between local I/O and network I/O on Windows:</span></span>

-   <span data-ttu-id="73d5f-105">網路 i/o 支援取決於重新導向程式和網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="73d5f-105">Network I/O support depends on the redirector and the network protocol.</span></span>
-   <span data-ttu-id="73d5f-106">網路 i/o 效能取決於正在進行的網路 i/o 作業數目，以及網路連線的速度。</span><span class="sxs-lookup"><span data-stu-id="73d5f-106">Network I/O performance depends on how many network I/O operations are taking place and the speed of the network connection.</span></span> <span data-ttu-id="73d5f-107">您的應用程式必須能夠處理可能比本機電腦更快或更慢的伺服器的網路 i/o 作業，以及網路容量的暫時性變更。</span><span class="sxs-lookup"><span data-stu-id="73d5f-107">Your application must be able to handle network I/O operations with servers that may be much faster or slower than your local machine, as well as transient changes in network capacity.</span></span> <span data-ttu-id="73d5f-108">在這些情況下，您的應用程式可能需要等待更多時間才能完成作業。</span><span class="sxs-lookup"><span data-stu-id="73d5f-108">In these cases, your application may need to allow more time for the operation to complete.</span></span>
-   <span data-ttu-id="73d5f-109">您用來執行本機檔案 i/o 的函式在網路上可能會有不同的行為。</span><span class="sxs-lookup"><span data-stu-id="73d5f-109">The functions you use to perform local file I/O may behave differently over the network.</span></span> <span data-ttu-id="73d5f-110">例如，需要很長時間才能完成的網路 i/o 作業可能會超時。在某些情況下，檔案控制代碼可能會無限期地保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="73d5f-110">For example, a network I/O operation that takes a long time to complete may time out. In some situations, file handles may be left open indefinitely because of this.</span></span> <span data-ttu-id="73d5f-111">另一個範例是，函式可能會傳回錯誤碼，讓您的應用程式能夠處理網路 i/o 特定的程式碼。</span><span class="sxs-lookup"><span data-stu-id="73d5f-111">Another example is that functions may return error codes for your application to process that are specific to network I/O.</span></span>

 

 



