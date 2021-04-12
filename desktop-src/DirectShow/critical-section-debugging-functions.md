---
description: 重要區段調試函數
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: 重要區段調試函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509909"
---
# <a name="critical-section-debugging-functions"></a><span data-ttu-id="e7353-103">重要區段調試函數</span><span class="sxs-lookup"><span data-stu-id="e7353-103">Critical Section Debugging Functions</span></span>

<span data-ttu-id="e7353-104">這些函式可協助您在程式碼中的重要區段中進行偵錯工具，以便更輕鬆地找出鎖死的原因。</span><span class="sxs-lookup"><span data-stu-id="e7353-104">These functions help to debug critical sections in your code, which can make it easier to find the cause of a deadlock.</span></span> <span data-ttu-id="e7353-105">這些函數會使用 [**CCritSec**](ccritsec.md) helper 類別。</span><span class="sxs-lookup"><span data-stu-id="e7353-105">These functions use the [**CCritSec**](ccritsec.md) helper class.</span></span>



| <span data-ttu-id="e7353-106">函式</span><span class="sxs-lookup"><span data-stu-id="e7353-106">Function</span></span>                             | <span data-ttu-id="e7353-107">描述</span><span class="sxs-lookup"><span data-stu-id="e7353-107">Description</span></span>                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="e7353-108">**CritCheckIn**</span><span class="sxs-lookup"><span data-stu-id="e7353-108">**CritCheckIn**</span></span>](critcheckin.md)   | <span data-ttu-id="e7353-109">如果目前的執行緒擁有指定的重要區段，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="e7353-109">Returns **TRUE** if the current thread owns the specified critical section.</span></span>  |
| [<span data-ttu-id="e7353-110">**CritCheckOut**</span><span class="sxs-lookup"><span data-stu-id="e7353-110">**CritCheckOut**</span></span>](critcheckout.md) | <span data-ttu-id="e7353-111">如果目前線程擁有指定的重要區段，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e7353-111">Returns **FALSE** if the current thread owns the specified critical section.</span></span> |
| [<span data-ttu-id="e7353-112">**DbgLockTrace**</span><span class="sxs-lookup"><span data-stu-id="e7353-112">**DbgLockTrace**</span></span>](dbglocktrace.md) | <span data-ttu-id="e7353-113">啟用或停用指定之重要區段的偵錯工具記錄。</span><span class="sxs-lookup"><span data-stu-id="e7353-113">Enables or disables debug logging for a given critical section.</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="e7353-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7353-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7353-115">偵錯工具</span><span class="sxs-lookup"><span data-stu-id="e7353-115">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



