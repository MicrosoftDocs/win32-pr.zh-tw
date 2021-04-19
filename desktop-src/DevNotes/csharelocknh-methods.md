---
description: 用來操作鎖定的方法群組。
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: CShareLockNH 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970101"
---
# <a name="csharelocknh-methods"></a><span data-ttu-id="ff30c-103">CShareLockNH 方法</span><span class="sxs-lookup"><span data-stu-id="ff30c-103">CShareLockNH Methods</span></span>

<span data-ttu-id="ff30c-104">用來操作鎖定的方法群組。</span><span class="sxs-lookup"><span data-stu-id="ff30c-104">A group of methods that is used to manipulate locks.</span></span>

## <a name="methods"></a><span data-ttu-id="ff30c-105">方法</span><span class="sxs-lookup"><span data-stu-id="ff30c-105">Methods</span></span>

<span data-ttu-id="ff30c-106">以下是 Rwnh.dll 匯出的方法。</span><span class="sxs-lookup"><span data-stu-id="ff30c-106">The following are methods exported by Rwnh.dll.</span></span>



| <span data-ttu-id="ff30c-107">方法</span><span class="sxs-lookup"><span data-stu-id="ff30c-107">Method</span></span>                                                                   | <span data-ttu-id="ff30c-108">描述</span><span class="sxs-lookup"><span data-stu-id="ff30c-108">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="ff30c-109">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="ff30c-109">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)                     | <span data-ttu-id="ff30c-110">取得讀取器/寫入器鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff30c-110">Acquires a reader/writer lock.</span></span>                                  |
| [<span data-ttu-id="ff30c-111">**ExclusiveToPartial**</span><span class="sxs-lookup"><span data-stu-id="ff30c-111">**ExclusiveToPartial**</span></span>](csharelocknh--exclusivetopartial.md)           | <span data-ttu-id="ff30c-112">變更狀態。</span><span class="sxs-lookup"><span data-stu-id="ff30c-112">Changes the state.</span></span>                                              |
| [<span data-ttu-id="ff30c-113">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="ff30c-113">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)                 | <span data-ttu-id="ff30c-114">釋放鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff30c-114">Releases a lock.</span></span>                                                |
| [<span data-ttu-id="ff30c-115">**FirstPartialToExclusive**</span><span class="sxs-lookup"><span data-stu-id="ff30c-115">**FirstPartialToExclusive**</span></span>](csharelocknh--firstpartialtoexclusive.md) | <span data-ttu-id="ff30c-116">用來將部分鎖定轉換為獨佔鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff30c-116">Used in converting a partial lock to an exclusive lock.</span></span>         |
| [<span data-ttu-id="ff30c-117">**PartialLock**</span><span class="sxs-lookup"><span data-stu-id="ff30c-117">**PartialLock**</span></span>](csharelocknh--partiallock.md)                         | <span data-ttu-id="ff30c-118">防止一個以上的執行緒完成取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff30c-118">Prevents more than one thread from completing acquiring a lock.</span></span> |
| [<span data-ttu-id="ff30c-119">**PartialUnlock**</span><span class="sxs-lookup"><span data-stu-id="ff30c-119">**PartialUnlock**</span></span>](csharelocknh--partialunlock.md)                     | <span data-ttu-id="ff30c-120">釋放部分鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff30c-120">Releases a partial lock.</span></span>                                        |
| [<span data-ttu-id="ff30c-121">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="ff30c-121">**ShareLock**</span></span>](csharelocknh--sharelock.md)                             | <span data-ttu-id="ff30c-122">取得共用模式的鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff30c-122">Obtains a lock for shared mode.</span></span>                                 |
| [<span data-ttu-id="ff30c-123">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="ff30c-123">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)                         | <span data-ttu-id="ff30c-124">從共用模式釋放鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff30c-124">Releases a lock from shared mode.</span></span>                               |
| [<span data-ttu-id="ff30c-125">**SharedToPartial**</span><span class="sxs-lookup"><span data-stu-id="ff30c-125">**SharedToPartial**</span></span>](csharelocknh--sharedtopartial.md)                 | <span data-ttu-id="ff30c-126">取得部分鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff30c-126">Obtains a partial lock.</span></span>                                         |
| [<span data-ttu-id="ff30c-127">**TryExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="ff30c-127">**TryExclusiveLock**</span></span>](csharelocknh--tryexclusivelock.md)               | <span data-ttu-id="ff30c-128">取得獨佔鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff30c-128">Obtains a lock exclusively.</span></span>                                     |



 

 

 



