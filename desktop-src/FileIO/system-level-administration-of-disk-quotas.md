---
description: 系統管理員可以設定磁片區上特定使用者的配額。 系統管理員也可以設定磁片區的預設配額。
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: 磁片配額的系統層級管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191510"
---
# <a name="system-level-administration-of-disk-quotas"></a><span data-ttu-id="8c358-104">磁片配額的系統層級管理</span><span class="sxs-lookup"><span data-stu-id="8c358-104">System-level Administration of Disk Quotas</span></span>

<span data-ttu-id="8c358-105">系統管理員可以設定磁片區上特定使用者的配額。</span><span class="sxs-lookup"><span data-stu-id="8c358-105">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="8c358-106">系統管理員也可以設定磁片區的預設配額。</span><span class="sxs-lookup"><span data-stu-id="8c358-106">The administrator can also set default quotas for the volume.</span></span> <span data-ttu-id="8c358-107">除非系統管理員特別針對該使用者建立配額，否則磁片區上的新使用者會收到預設配額。</span><span class="sxs-lookup"><span data-stu-id="8c358-107">A new user on the volume receives the default quota unless the administrator established a quota specifically for that user.</span></span>

<span data-ttu-id="8c358-108">系統管理員可以查詢配額追蹤和強制執行 (或配額狀態的層級) 、預設配額限制，以及每個使用者的配額資訊。</span><span class="sxs-lookup"><span data-stu-id="8c358-108">The administrator can query the level of quota tracking and enforcement (or quota states), the default quota limits, and the per-user quota information.</span></span> <span data-ttu-id="8c358-109">每個使用者的配額資訊包含使用者的固定配額限制、警告閾值和配額使用量。</span><span class="sxs-lookup"><span data-stu-id="8c358-109">The per-user quota information contains the user's hard quota limit, warning threshold, and the quota usage.</span></span> <span data-ttu-id="8c358-110">系統管理員也可以啟用或停用配額強制。</span><span class="sxs-lookup"><span data-stu-id="8c358-110">The administrator can also enable or disable quota enforcement.</span></span>

<span data-ttu-id="8c358-111">有三個配額狀態，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="8c358-111">There are three quota states, as shown in the following table.</span></span>



| <span data-ttu-id="8c358-112">州</span><span class="sxs-lookup"><span data-stu-id="8c358-112">State</span></span>          | <span data-ttu-id="8c358-113">描述</span><span class="sxs-lookup"><span data-stu-id="8c358-113">Description</span></span>                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c358-114">停用配額</span><span class="sxs-lookup"><span data-stu-id="8c358-114">Quota disabled</span></span> | <span data-ttu-id="8c358-115">不會追蹤配額使用量變更，但不會移除配額限制。</span><span class="sxs-lookup"><span data-stu-id="8c358-115">Quota usage changes are not tracked, but the quota limits are not removed.</span></span> <span data-ttu-id="8c358-116">在此狀態下，效能不會受到磁片配額的影響。</span><span class="sxs-lookup"><span data-stu-id="8c358-116">In this state, performance is not affected by disk quotas.</span></span> <span data-ttu-id="8c358-117">這是預設狀態。</span><span class="sxs-lookup"><span data-stu-id="8c358-117">This is the default state.</span></span>                         |
| <span data-ttu-id="8c358-118">已追蹤配額</span><span class="sxs-lookup"><span data-stu-id="8c358-118">Quota tracked</span></span>  | <span data-ttu-id="8c358-119">系統會追蹤配額使用量變更，但不會強制執行配額限制。</span><span class="sxs-lookup"><span data-stu-id="8c358-119">Quota usage changes are tracked, but quota limits are not enforced.</span></span> <span data-ttu-id="8c358-120">處於此狀態時，不會產生任何配額違規事件，而且因為磁片配額違規，所以沒有任何檔案作業失敗。</span><span class="sxs-lookup"><span data-stu-id="8c358-120">In this state, no quota violation events are generated and no file operations fail because of disk quota violations.</span></span> |
| <span data-ttu-id="8c358-121">已強制執行配額</span><span class="sxs-lookup"><span data-stu-id="8c358-121">Quota enforced</span></span> | <span data-ttu-id="8c358-122">系統會追蹤配額使用量變更，並強制執行配額限制。</span><span class="sxs-lookup"><span data-stu-id="8c358-122">Quota usage changes are tracked and quota limits are enforced.</span></span>                                                                                                                           |



 

 

 



