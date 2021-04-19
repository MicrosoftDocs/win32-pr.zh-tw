---
description: 中斷隨機鎖定是指將某個用戶端對檔案的鎖定降級的程式，讓另一個用戶端可以開啟檔案，不論是否有無機會鎖定。
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: 中斷隨機鎖定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a29b6bd36d8c000b5288ea2408897415547c802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984712"
---
# <a name="breaking-opportunistic-locks"></a><span data-ttu-id="008e3-103">中斷隨機鎖定</span><span class="sxs-lookup"><span data-stu-id="008e3-103">Breaking Opportunistic Locks</span></span>

<span data-ttu-id="008e3-104">中斷隨機鎖定是指將某個用戶端對檔案的鎖定降級的程式，讓另一個用戶端可以開啟檔案，不論是否有無機會鎖定。</span><span class="sxs-lookup"><span data-stu-id="008e3-104">Breaking an opportunistic lock is the process of degrading the lock that one client has on a file so that another client can open the file, with or without an opportunistic lock.</span></span> <span data-ttu-id="008e3-105">當其他用戶端要求開啟的作業時，伺服器會延遲開啟的作業，並通知用戶端保存隨機鎖定。</span><span class="sxs-lookup"><span data-stu-id="008e3-105">When the other client requests the open operation, the server delays the open operation and notifies the client holding the opportunistic lock.</span></span>

<span data-ttu-id="008e3-106">持有鎖定的用戶端接著會採取適用于鎖定類型的動作，例如，放棄讀取緩衝區、關閉檔案等等。</span><span class="sxs-lookup"><span data-stu-id="008e3-106">The client holding the lock then takes actions appropriate to the type of lock, for example abandoning read buffers, closing the file, and so on.</span></span> <span data-ttu-id="008e3-107">只有當擁有隨機鎖定的用戶端通知伺服器完成時，伺服器才會開啟要求開啟作業的用戶端檔案。</span><span class="sxs-lookup"><span data-stu-id="008e3-107">Only when the client holding the opportunistic lock notifies the server that it is done does the server open the file for the client requesting the open operation.</span></span> <span data-ttu-id="008e3-108">不過，當層級2鎖定中斷時，伺服器會向用戶端回報已中斷，但是未等候任何通知，因為沒有快取的資料會排清至伺服器。</span><span class="sxs-lookup"><span data-stu-id="008e3-108">However, when a level 2 lock is broken, the server reports to the client that it has been broken but does not wait for any acknowledgment, as there is no cached data to be flushed to the server.</span></span>

<span data-ttu-id="008e3-109">在確認任何獨佔鎖定 (篩選、層級1或批次) 的中斷時，中斷鎖定的持有者無法要求另一個獨佔鎖定。</span><span class="sxs-lookup"><span data-stu-id="008e3-109">In acknowledging a break of any exclusive lock (filter, level 1, or batch), the holder of a broken lock cannot request another exclusive lock.</span></span> <span data-ttu-id="008e3-110">它可能會降低層級2鎖定或完全無鎖定的獨佔鎖定。</span><span class="sxs-lookup"><span data-stu-id="008e3-110">It can degrade an exclusive lock to a level 2 lock or no lock at all.</span></span> <span data-ttu-id="008e3-111">當它即將關閉檔案時，預留位置通常會釋放鎖定並關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="008e3-111">The holder typically releases the lock and closes the file when it is about to close the file anyway.</span></span>

<span data-ttu-id="008e3-112">應用程式會使用與鎖定中斷的檔案相關聯之重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) **hEvent** 成員，來通知應用程式發生中斷。</span><span class="sxs-lookup"><span data-stu-id="008e3-112">Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the file on which the lock is broken.</span></span> <span data-ttu-id="008e3-113">應用程式也可以使用 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 和 [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted)等函數。</span><span class="sxs-lookup"><span data-stu-id="008e3-113">Applications may also use functions such as [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) and [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span></span>

 

 
