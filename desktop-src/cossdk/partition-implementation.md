---
description: 在應用程式伺服器上安裝時，COM + 會自動建立一個磁碟分割，稱為「全域分割區」。
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: 分割區執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973398"
---
# <a name="partition-implementation"></a><span data-ttu-id="bae71-103">分割區執行</span><span class="sxs-lookup"><span data-stu-id="bae71-103">Partition Implementation</span></span>

<span data-ttu-id="bae71-104">在應用程式伺服器上安裝時，COM + 會自動建立一個磁碟分割，稱為「 *全域分割* 區」。</span><span class="sxs-lookup"><span data-stu-id="bae71-104">When installed on an application server, COM+ automatically creates a partition, known as the *global partition*.</span></span> <span data-ttu-id="bae71-105">全域分割區包含一組標準的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="bae71-105">The global partition includes a standard set of COM+ applications.</span></span> <span data-ttu-id="bae71-106">安裝在全域分割區中的 COM + 應用程式，會自動提供給伺服器上的所有使用者使用。</span><span class="sxs-lookup"><span data-stu-id="bae71-106">COM+ applications that are installed in the global partition are automatically available to all users on the server.</span></span> <span data-ttu-id="bae71-107">如果您有其他 COM + 應用程式可供伺服器上的所有使用者使用，您可以將這些應用程式新增至全域資料分割。</span><span class="sxs-lookup"><span data-stu-id="bae71-107">If you have other COM+ applications that you would like to make available to all users on the server, you can add them into the global partition.</span></span>

<span data-ttu-id="bae71-108">除了全域分割區之外，您還可以針對該伺服器上的使用者或整個網域中的使用者建立其他磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="bae71-108">In addition to the global partition, you can create other partitions for users on that server only, or for users throughout the domain.</span></span> <span data-ttu-id="bae71-109">建立額外的分割區，並在其中安裝多個 COM + 應用程式設定，可讓您的使用者在同一部電腦上同時執行這些應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="bae71-109">Creating additional partitions and installing multiple configurations of a COM+ application into them allows your users to execute those application configurations simultaneously on the same computer.</span></span> <span data-ttu-id="bae71-110">此外，將 COM + 應用程式安裝到全域資料分割以外的磁碟分割中，就可以控制使用者對這些應用程式的存取。</span><span class="sxs-lookup"><span data-stu-id="bae71-110">Also, by installing COM+ applications into a partition other than the global partition, you can control user access to those applications.</span></span>

<span data-ttu-id="bae71-111">**WINDOWS XP：** 無法使用建立、設定或委派 COM + 分割的能力。</span><span class="sxs-lookup"><span data-stu-id="bae71-111">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="bae71-112">全域分割區是唯一可用的 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="bae71-112">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="bae71-113">如需 Active Directory 中定義之本機分割區和分割區的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="bae71-113">For more information on local partitions and partitions defined within Active Directory, see the following topics:</span></span>

-   [<span data-ttu-id="bae71-114">本機分割區</span><span class="sxs-lookup"><span data-stu-id="bae71-114">Local Partitions</span></span>](local-partitions.md)
-   [<span data-ttu-id="bae71-115">磁碟分割和 Active Directory</span><span class="sxs-lookup"><span data-stu-id="bae71-115">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
-   [<span data-ttu-id="bae71-116">預設分割區</span><span class="sxs-lookup"><span data-stu-id="bae71-116">Default Partitions</span></span>](default-partitions.md)
-   [<span data-ttu-id="bae71-117">全域分割區</span><span class="sxs-lookup"><span data-stu-id="bae71-117">The Global Partition</span></span>](the-global-partition.md)
-   [<span data-ttu-id="bae71-118">分割區屬性</span><span class="sxs-lookup"><span data-stu-id="bae71-118">Partition Properties</span></span>](partition-properties.md)

## <a name="related-topics"></a><span data-ttu-id="bae71-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="bae71-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae71-120">應用程式設計限制</span><span class="sxs-lookup"><span data-stu-id="bae71-120">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="bae71-121">COM + 佇列元件和分割區</span><span class="sxs-lookup"><span data-stu-id="bae71-121">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="bae71-122">在分割區中註冊和啟用元件</span><span class="sxs-lookup"><span data-stu-id="bae71-122">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="bae71-123">什麼是 COM + 磁碟分割？</span><span class="sxs-lookup"><span data-stu-id="bae71-123">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



