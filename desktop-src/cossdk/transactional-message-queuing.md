---
description: 交易是資料存放區的一系列修改 (例如資料庫或檔案系統，) 保證全部成功執行，或完全不執行。
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: 交易式訊息佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4730b20f4014cdf7c76462d3f2cae272695d907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025889"
---
# <a name="transactional-message-queuing"></a><span data-ttu-id="277fc-103">交易式訊息佇列</span><span class="sxs-lookup"><span data-stu-id="277fc-103">Transactional Message Queuing</span></span>

<span data-ttu-id="277fc-104">*交易* 是資料存放區的一系列修改 (例如資料庫或檔案系統，) 保證全部成功執行，或完全不執行。</span><span class="sxs-lookup"><span data-stu-id="277fc-104">A *transaction* is a series of modifications of a data store (such as a database or a file system) guaranteed either to be all successfully executed or not to be executed at all.</span></span> <span data-ttu-id="277fc-105">若要執行交易，記錄會在交易開始之前保留在資料存放區的狀態，而且如果其中一個修改失敗，交易就會傳回失敗，而初始狀態會還原 (或回復) 。</span><span class="sxs-lookup"><span data-stu-id="277fc-105">To implement a transaction, a record is kept of the state of the data store before the transaction begins and, if one of the modifications fails, the transaction returns failure and the initial state is restored (or rolled back).</span></span> <span data-ttu-id="277fc-106">交易是用來維護資料的完整性，因此在商務軟體程式設計中扮演重要的角色。</span><span class="sxs-lookup"><span data-stu-id="277fc-106">Transactions are used to maintain data integrity and consequently play an important role in business software programming.</span></span>

<span data-ttu-id="277fc-107">通常，應用程式可以使用分成數個較小交易或活動的商務交易或工作流程來開發。</span><span class="sxs-lookup"><span data-stu-id="277fc-107">Often, applications can be developed using a business transaction or workflow that is split into several smaller transactions or activities.</span></span> <span data-ttu-id="277fc-108">這些活動會以時間分隔，然後使用可靠的訊息佇列進行連接。</span><span class="sxs-lookup"><span data-stu-id="277fc-108">These activities are separated in time and then connected using reliable message queues.</span></span>

1.  <span data-ttu-id="277fc-109">第一個交易牽涉到訂單輸入資料庫。</span><span class="sxs-lookup"><span data-stu-id="277fc-109">The first transaction involves the order entry database.</span></span> <span data-ttu-id="277fc-110">[訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 會使用交易功能，將訊息從一個佇列移至另一個佇列，剛好一次移動一次。</span><span class="sxs-lookup"><span data-stu-id="277fc-110">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) moves the message from one queue to another queue, exactly one time, using transaction capabilities.</span></span> <span data-ttu-id="277fc-111">如果資料庫已更新，則佇列上會有一則訊息。</span><span class="sxs-lookup"><span data-stu-id="277fc-111">If the database is updated, there is a message on the queue.</span></span> <span data-ttu-id="277fc-112">如果訊息不會到達佇列，則會中止，而且資料庫會回復。</span><span class="sxs-lookup"><span data-stu-id="277fc-112">If the message doesn't reach the queue, it is aborted and the database is rolled back.</span></span>
2.  <span data-ttu-id="277fc-113">稍後，訊息佇列會發現伺服器可供使用。</span><span class="sxs-lookup"><span data-stu-id="277fc-113">Sometime later, Message Queuing discovers that the server is available.</span></span> <span data-ttu-id="277fc-114">沒有任何應用程式會輪詢伺服器是否存在。</span><span class="sxs-lookup"><span data-stu-id="277fc-114">There is no application polling for the existence of the server.</span></span> <span data-ttu-id="277fc-115">這是第二筆交易。</span><span class="sxs-lookup"><span data-stu-id="277fc-115">This is the second transaction.</span></span>
3.  <span data-ttu-id="277fc-116">第三筆交易牽涉到傳送資料庫查詢和傳送資料庫的更新。</span><span class="sxs-lookup"><span data-stu-id="277fc-116">The third transaction involves a shipping database query and the update of the shipping database.</span></span> <span data-ttu-id="277fc-117">如果伺服器在此交易中途失敗，則會復原修改，並將訊息傳回至輸入佇列。</span><span class="sxs-lookup"><span data-stu-id="277fc-117">If the server fails in the middle of this transaction, the modification is rolled back and the message is returned to the input queue.</span></span> <span data-ttu-id="277fc-118">這可確保在交易期間維護資料和資料庫的完整性。</span><span class="sxs-lookup"><span data-stu-id="277fc-118">This ensures that the integrity of the data and databases is maintained during the transactions.</span></span>

 

 



