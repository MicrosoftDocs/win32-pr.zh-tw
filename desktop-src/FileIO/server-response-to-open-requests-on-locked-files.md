---
description: 您可以將應用程式對其他用戶端所造成的影響降至最低、盡可能授與最少的共用、要求所需的最低存取層級，以及使用適用于您應用程式的最小無侵入性隨機鎖定，來降低應用程式對其他用戶端的影響。
ms.assetid: c28b0ae0-0d35-4b59-9f54-87c55ca72716
title: 對鎖定檔案開啟要求的伺服器回應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d397613f6b54f2b42c26a5674a787b796f5f19e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511900"
---
# <a name="server-response-to-open-requests-on-locked-files"></a><span data-ttu-id="0f9fd-103">對鎖定檔案開啟要求的伺服器回應</span><span class="sxs-lookup"><span data-stu-id="0f9fd-103">Server Response to Open Requests on Locked Files</span></span>

<span data-ttu-id="0f9fd-104">隨機鎖定的存留期包含三個不同的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-104">The life of an opportunistic lock includes three distinct time spans.</span></span> <span data-ttu-id="0f9fd-105">在每一種情況下，伺服器會以不同的方式來判斷它對用戶端要求的回應，以開啟另一個用戶端鎖定的檔案。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-105">During each, the server determines by different means its reaction to a request from a client to open a file locked by another client.</span></span> <span data-ttu-id="0f9fd-106">一般而言，您可以將應用程式對其他用戶端所造成的影響降至最低，並藉由授與最少的共用、要求必要的最低存取層級，以及使用適合您應用程式的最少侵入式隨機鎖定，來將應用程式的影響降至最低。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-106">In general, you can minimize the impact your application has on other clients and the impact they have on your application by granting as much sharing as possible, requesting the minimum access level necessary, and using the least intrusive opportunistic lock suitable for your application.</span></span>

<span data-ttu-id="0f9fd-107">第一個是在伺服器開啟用戶端檔案之後，但在授與鎖定之前的期間。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-107">First is the period after the server opens a file for a client but before it grants a lock.</span></span> <span data-ttu-id="0f9fd-108">在這段期間內，檔案上不會有鎖定，且伺服器相依于共用、存取模式，以及您所要求的隨機鎖定類型，以判斷其對另一個開啟相同檔案之要求的回應。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-108">During this time, no lock exists on the file, and the server depends on sharing, access modes, and the type of opportunistic lock you request to determine its reaction to another request to open the same file.</span></span> <span data-ttu-id="0f9fd-109">例如，如果您開啟有問題的檔案進行寫入存取，您可能會禁止將可讀取快取存取權的隨機鎖定授與其他用戶端。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-109">For example, if you open the file in question for write access, you may inhibit granting opportunistic locks that allow read caching access to other clients.</span></span> <span data-ttu-id="0f9fd-110">伺服器授與鎖定之前的時間範圍通常是以毫秒為單位，但可能較長。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-110">The time span before the server grants a lock is typically in the millisecond range but may be longer.</span></span>

<span data-ttu-id="0f9fd-111">在授與隨機鎖定之後，伺服器會檢查鎖定，以判斷鎖定檔案上開啟要求的伺服器回應。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-111">After the opportunistic lock is granted, the server examines the lock to determine server reaction to an open request on a locked file.</span></span> <span data-ttu-id="0f9fd-112">同樣地，您的應用程式如何開啟檔案，以及它所保留的鎖定類型會影響伺服器的回應方式。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-112">Again, how your application opened the file and the type of lock it holds affects how the server responds.</span></span> <span data-ttu-id="0f9fd-113">如需有關如何在每個案例中回應伺服器的詳細資訊，請參閱隨機 [鎖定類型](types-of-opportunistic-locks.md)。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-113">For more information on how the server responds in each case, see [Types of Opportunistic Locks](types-of-opportunistic-locks.md).</span></span>

<span data-ttu-id="0f9fd-114">最後，在伺服器判斷出您的鎖定應該中斷 (結束) 但在您的應用程式完成其對中斷的回應之前，會有範圍。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-114">Finally, there is the span after the server determines that your lock should be broken (ended) but before your application completes its reaction to the break.</span></span> <span data-ttu-id="0f9fd-115">根據鎖定的類型而定，您的應用程式可以將鎖定降級為較低的層級，也可以降級為無。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-115">Depending on the type of lock, your application can downgrade the lock to a lower level or to none at all.</span></span> <span data-ttu-id="0f9fd-116">您的應用程式也可以關閉檔案和鎖定。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-116">Your application can also close the file and the lock.</span></span> <span data-ttu-id="0f9fd-117">在這段期間，伺服器會將來自其他用戶端的任何要求保存在 abeyance 中，以開啟先前鎖定的檔案。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-117">During this time, the server holds in abeyance any requests from other clients to open the formerly locked file.</span></span> <span data-ttu-id="0f9fd-118">此時間範圍的範圍可能從毫秒到數十秒。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-118">This time span may range from milliseconds to tens of seconds.</span></span> <span data-ttu-id="0f9fd-119">如需詳細資訊，請參閱 [中斷隨機鎖定](breaking-opportunistic-locks.md)。</span><span class="sxs-lookup"><span data-stu-id="0f9fd-119">For more information, see [Breaking Opportunistic Locks](breaking-opportunistic-locks.md).</span></span>

 

 



