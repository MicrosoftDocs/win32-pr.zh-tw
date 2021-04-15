---
description: COM + 佇列元件服務完全支援分割區的概念。 也就是說，在分割區中執行已排入佇列的元件時，會將訊息排入佇列，而元件最後會在元件分割區中執行。
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: COM + 佇列元件和分割區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510482"
---
# <a name="com-queued-components-and-partitions"></a><span data-ttu-id="27181-104">COM + 佇列元件和分割區</span><span class="sxs-lookup"><span data-stu-id="27181-104">COM+ Queued Components and Partitions</span></span>

<span data-ttu-id="27181-105">COM + 佇列元件服務完全支援分割區的概念。</span><span class="sxs-lookup"><span data-stu-id="27181-105">The COM+ queued components service fully supports the concept of partitions.</span></span> <span data-ttu-id="27181-106">也就是說，在分割區中執行已排入佇列的元件時，會將訊息排入佇列，而且最後會在元件的磁碟分割內執行該元件。</span><span class="sxs-lookup"><span data-stu-id="27181-106">That is, when a queued component within a partition is executed, the message is queued and the component is eventually executed within the component's partition.</span></span>

## <a name="queue-names-for-partitioned-components"></a><span data-ttu-id="27181-107">分割區元件的佇列名稱</span><span class="sxs-lookup"><span data-stu-id="27181-107">Queue Names for Partitioned Components</span></span>

<span data-ttu-id="27181-108">傳統上，已排入佇列的元件服務會使用應用程式名稱做為佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="27181-108">Traditionally, the queued components service uses the application name as the queue name.</span></span> <span data-ttu-id="27181-109">這表示在非資料分割的情況下，只有一個應用程式名稱實例存在於電腦上，每個應用程式名稱都有自己的訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="27181-109">This means that in a non-partitions scenario, where only one instance of an application name exists on a computer, each application name has its own message queue.</span></span>

<span data-ttu-id="27181-110">不過，在資料分割的情況下，相同應用程式名稱的多個實例可以存在於電腦上，佇列元件服務會針對任何共用相同應用程式名稱的已佇列元件使用相同的佇列。</span><span class="sxs-lookup"><span data-stu-id="27181-110">In the case of partitions, however, where multiple instances of the same application name can exist on a computer, the queued components service uses the same queue for any queued components that share the same application name.</span></span>

## <a name="activating-queued-components"></a><span data-ttu-id="27181-111">啟用已排入佇列的元件</span><span class="sxs-lookup"><span data-stu-id="27181-111">Activating Queued Components</span></span>

<span data-ttu-id="27181-112">分割區識別碼用來啟動非佇列元件的相同規則適用于已排入佇列的元件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="27181-112">The same rules for how the partition ID is used to activate a non-queued component applies to a queued component, as follows:</span></span>

-   <span data-ttu-id="27181-113">如果使用了「標記」來啟動已排入佇列的元件，並包含分割區識別碼，則會使用此資料分割識別碼來找出資料分割。</span><span class="sxs-lookup"><span data-stu-id="27181-113">If a moniker is used to activate the queued component and a partition ID is included, this partition ID is used to locate the partition.</span></span> <span data-ttu-id="27181-114">此分割識別碼的優先順序高於任何可能存在於正在啟動的元件之內容中的分割區識別碼。</span><span class="sxs-lookup"><span data-stu-id="27181-114">This partition ID takes precedence over any partition ID that might exist in the context for the component being activated.</span></span>
-   <span data-ttu-id="27181-115">如果未使用任何標記來啟用元件，則會使用物件內容中的分割區識別碼。</span><span class="sxs-lookup"><span data-stu-id="27181-115">If no moniker is being used to activate the component, the partition ID that is in the object's context is used.</span></span>
-   <span data-ttu-id="27181-116">如果物件的內容中沒有任何資料分割識別碼，則會使用 Active Directory 內的預設使用者對分割區對應。</span><span class="sxs-lookup"><span data-stu-id="27181-116">If no partition ID exists in the object's context, the default user-to-partition mapping within Active Directory is used.</span></span>

> [!Note]  
> <span data-ttu-id="27181-117">如果伺服器電腦與網路中斷連線，而且當伺服器中斷連線時，使用者對分割集的對應已變更，則磁碟分割快取可能會包含過期的使用者對資料分割集對應。</span><span class="sxs-lookup"><span data-stu-id="27181-117">If a server computer is disconnected from the network and if the user-to-partition set mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition set mapping.</span></span> <span data-ttu-id="27181-118">如果使用者對分割集對應是用來啟動元件的機制，這可能會導致啟用錯誤。</span><span class="sxs-lookup"><span data-stu-id="27181-118">This could result in an activation error if user-to-partition set mapping is the mechanism used to activate a component.</span></span>

 

<span data-ttu-id="27181-119">COM + 事件會完全整合到資料分割中。</span><span class="sxs-lookup"><span data-stu-id="27181-119">COM+ events are fully integrated into partitions.</span></span> <span data-ttu-id="27181-120">這表示訂閱者可以訂閱其應用程式位於資料分割內的發行者。</span><span class="sxs-lookup"><span data-stu-id="27181-120">This means that a subscriber can subscribe to a publisher whose application resides within a partition.</span></span> <span data-ttu-id="27181-121">若要允許此訂閱，訂閱者類別集合包含兩個與資料分割相關的屬性：事件類別資料分割識別碼和事件類別應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="27181-121">To allow this subscription, the subscriber class collection includes two partition-related properties—an event class partition ID and an event class application ID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27181-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="27181-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27181-123">應用程式設計限制</span><span class="sxs-lookup"><span data-stu-id="27181-123">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="27181-124">分割區執行</span><span class="sxs-lookup"><span data-stu-id="27181-124">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="27181-125">在分割區中註冊和啟用元件</span><span class="sxs-lookup"><span data-stu-id="27181-125">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="27181-126">什麼是 COM + 磁碟分割？</span><span class="sxs-lookup"><span data-stu-id="27181-126">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



