---
title: 同步作業
description: 當 RasDial 被叫用為同步作業時，除非已建立連接或發生錯誤，否則函數不會傳回。
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021932"
---
# <a name="synchronous-operations"></a><span data-ttu-id="913a6-103">同步作業</span><span class="sxs-lookup"><span data-stu-id="913a6-103">Synchronous Operations</span></span>

<span data-ttu-id="913a6-104">當 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 被叫用為同步作業時，除非已建立連接或發生錯誤，否則函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="913a6-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as a synchronous operation, the function does not return until the connection has been established or an error occurs.</span></span> <span data-ttu-id="913a6-105">同步模式提供了一種簡單的方法，讓 RAS 用戶端建立連接。</span><span class="sxs-lookup"><span data-stu-id="913a6-105">Synchronous mode provides a simple way for a RAS client to establish a connection.</span></span> <span data-ttu-id="913a6-106">用戶端可以直接呼叫 **RasDial**、等候函式傳回，然後呼叫 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函數來判斷連接作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="913a6-106">The client can simply call **RasDial**, wait for the function to return, and then call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to determine whether the connection operation was successful.</span></span> <span data-ttu-id="913a6-107">一旦建立連線之後，用戶端應用程式就可以在不中斷連接的情況下終止。</span><span class="sxs-lookup"><span data-stu-id="913a6-107">Once the connection has been established, the client application can terminate without breaking the connection.</span></span> <span data-ttu-id="913a6-108">如果發生錯誤，用戶端應用程式必須在終止之前 [關閉連接](disconnecting.md) 作業。</span><span class="sxs-lookup"><span data-stu-id="913a6-108">If an error occurs, the client application must [shut down the connection operation](disconnecting.md) before terminating.</span></span>

<span data-ttu-id="913a6-109">同步模式的缺點是，用戶端在連接作業繼續時，不會收到進度通知。</span><span class="sxs-lookup"><span data-stu-id="913a6-109">The disadvantage of synchronous mode is that the client does not receive progress notifications as the connection operation proceeds.</span></span> <span data-ttu-id="913a6-110">這項缺少進度通知的因應措施是，同步模式用戶端可以使用呼叫 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 的個別執行緒來輪詢和顯示目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="913a6-110">As a workaround for this lack of progress notifications, a synchronous mode client can use a separate thread that calls [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) to poll for and display the current state.</span></span> <span data-ttu-id="913a6-111">不過，對於想要接收進度資訊的 RAS 用戶端，慣用的技巧是以非同步方式叫用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 。</span><span class="sxs-lookup"><span data-stu-id="913a6-111">However, for RAS clients that want to receive progress information, the preferred technique is to invoke [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchronously.</span></span>

 

 




