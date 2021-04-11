---
description: 藉由在開啟檔案的應用程式中，先開啟具有適當許可權和旗標的檔案，就會要求隨機鎖定。 系統將會要求您將需要的所有檔案，以重迭 (非同步) 作業。
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: 如何要求隨機鎖定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852123"
---
# <a name="how-to-request-an-opportunistic-lock"></a><span data-ttu-id="94ea2-104">如何要求隨機鎖定</span><span class="sxs-lookup"><span data-stu-id="94ea2-104">How to Request an Opportunistic Lock</span></span>

<span data-ttu-id="94ea2-105">用戶端應用程式只會在鎖定適用于本機伺服器上的檔案時，直接要求隨機鎖定。</span><span class="sxs-lookup"><span data-stu-id="94ea2-105">Client applications directly request opportunistic locks only when the lock is intended for a file on the local server.</span></span> <span data-ttu-id="94ea2-106">存取遠端伺服器上的檔案時，它是網路重新導向器，而不是用戶端應用程式，會要求來自遠端伺服器的隨機鎖定。</span><span class="sxs-lookup"><span data-stu-id="94ea2-106">When accessing files on remote servers, it is the network redirector, and not the client application, that requests the opportunistic lock from the remote server.</span></span>

<span data-ttu-id="94ea2-107">藉由在開啟檔案的應用程式中，先開啟具有適當許可權和旗標的檔案，就會要求隨機鎖定。</span><span class="sxs-lookup"><span data-stu-id="94ea2-107">Opportunistic locks are requested by first opening a file with permissions and flags appropriate to the application opening the file.</span></span> <span data-ttu-id="94ea2-108">系統將會要求您將需要的所有檔案，以重迭 (非同步) 作業。</span><span class="sxs-lookup"><span data-stu-id="94ea2-108">All files for which opportunistic locks will be requested must be opened for overlapped (asynchronous) operation.</span></span> <span data-ttu-id="94ea2-109">開啟檔案以進行重迭的作業之後，請使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式搭配適當的控制程式代碼來要求隨機鎖定。</span><span class="sxs-lookup"><span data-stu-id="94ea2-109">After the files are opened for overlapped operation, use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the appropriate control code to request an opportunistic lock.</span></span> <span data-ttu-id="94ea2-110">如需隨機鎖定作業的清單，請參閱隨機 [鎖定作業](opportunistic-lock-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="94ea2-110">For a list of the opportunistic lock operations, see [Opportunistic Lock Operations](opportunistic-lock-operations.md).</span></span>

<span data-ttu-id="94ea2-111">應用程式會使用與檔案相關聯之重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) **hEvent** 成員，來通知應用程式已中斷。</span><span class="sxs-lookup"><span data-stu-id="94ea2-111">Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the file.</span></span> <span data-ttu-id="94ea2-112">應用程式也可以使用 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 和 [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted)等函數。</span><span class="sxs-lookup"><span data-stu-id="94ea2-112">Applications may also use functions such as [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) and [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span></span> <span data-ttu-id="94ea2-113">應用程式會負責將正確的檔案與中斷的隨機鎖定產生關聯。</span><span class="sxs-lookup"><span data-stu-id="94ea2-113">The application is responsible for associating the correct file with the broken opportunistic lock.</span></span>

<span data-ttu-id="94ea2-114">如需通知的詳細資訊，請參閱 [同步](/windows/desktop/Sync/synchronization)處理。</span><span class="sxs-lookup"><span data-stu-id="94ea2-114">For more information on notification, see [Synchronization](/windows/desktop/Sync/synchronization).</span></span>

 

 
