---
title: 有效的日期和時間
description: 有效的日期和時間是一種避免的策略，藉由將資訊的有效資料延後到未來的某個時間點（當變更的機率很高時），來防止版本扭曲和部分更新。
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020864"
---
# <a name="effective-date-and-time"></a><span data-ttu-id="5daa6-103">有效的日期和時間</span><span class="sxs-lookup"><span data-stu-id="5daa6-103">Effective Date and Time</span></span>

<span data-ttu-id="5daa6-104">*有效的日期和時間* 是一種避免的策略，藉由將資訊的有效資料延後到未來的某個時間點（當變更的機率很高時），來防止版本扭曲和部分更新。</span><span class="sxs-lookup"><span data-stu-id="5daa6-104">*Effective date and time* is an avoidance strategy that prevents version skew and partial updates by deferring the effective data of information to some point in the future when the change has a high probability of being fully replicated.</span></span> <span data-ttu-id="5daa6-105">若要執行有效的日期，應用程式物件必須包含有效的日期時間戳記，這個時間戳記會在建立或變更物件時填入。</span><span class="sxs-lookup"><span data-stu-id="5daa6-105">To implement effective dates, the application objects must include an effective date timestamp, which is filled in when the object is created or changed.</span></span> <span data-ttu-id="5daa6-106">物件的取用者會驗證時間戳記，並延遲使用物件，直到到達該日期和時間為止。</span><span class="sxs-lookup"><span data-stu-id="5daa6-106">Consumers of the objects verify the timestamp and defer use of the objects until that date and time are reached.</span></span>

<span data-ttu-id="5daa6-107">一些重要考量︰</span><span class="sxs-lookup"><span data-stu-id="5daa6-107">Some important considerations:</span></span>

-   <span data-ttu-id="5daa6-108">選擇此方法的應用程式必須確保有一組適用的資料可供使用，直到更新的物件變成有效為止。</span><span class="sxs-lookup"><span data-stu-id="5daa6-108">Applications that choose this approach must ensure that there is a set of applicable data to use until the updated objects become effective.</span></span>
-   <span data-ttu-id="5daa6-109">Windows NT 4.0 中的分散式時間服務會將已連線的 Windows 2000 的時鐘保持同步。</span><span class="sxs-lookup"><span data-stu-id="5daa6-109">Distributed time service in Windows NT 4.0 keeps the clocks of the connected Windows 2000 synchronized.</span></span> <span data-ttu-id="5daa6-110">不過，沒有時間服務是完美的，因此有一個小型的版本扭曲視窗。</span><span class="sxs-lookup"><span data-stu-id="5daa6-110">No time service is perfect, however, so there is a small window for version skew.</span></span>
-   <span data-ttu-id="5daa6-111">設定有效的日期，就能瞭解分散式系統的整體複寫延遲。</span><span class="sxs-lookup"><span data-stu-id="5daa6-111">Setting a good effective date presumes knowledge of the overall replication latency for the distributed system in question.</span></span> <span data-ttu-id="5daa6-112">在穩定的網路中，有效日期的最佳經驗法則是更新的 (時間) + (2 \* (平均整體延遲) ) 。</span><span class="sxs-lookup"><span data-stu-id="5daa6-112">In a stable network a good rule of thumb for effective dates is the (time of the update) + (2\*(average overall latency)).</span></span> <span data-ttu-id="5daa6-113">因此，對於整體延遲平均4小時的系統而言，延遲為8小時是合理的。</span><span class="sxs-lookup"><span data-stu-id="5daa6-113">So, for a system whose overall latency averages 4 hours, a delay of 8 hours is reasonable.</span></span>
-   <span data-ttu-id="5daa6-114">在不穩定的網路中，判斷有效日期的「良好」值會變得更困難，因為延遲可能會有極大的變化。</span><span class="sxs-lookup"><span data-stu-id="5daa6-114">In an unstable network, determining a "good" value for effective dates is much more difficult, since the latency may be highly variable.</span></span> <span data-ttu-id="5daa6-115">相較于其他規避或偵測策略（例如總和檢查碼或一致性 Guid），有效日期在不穩定的網路中是最有效的。</span><span class="sxs-lookup"><span data-stu-id="5daa6-115">Effective date is most "effective" in an unstable network when combined with other avoidance or detection strategies such as checksums or consistency GUIDs.</span></span> <span data-ttu-id="5daa6-116">如需詳細資訊，請參閱總和檢查碼 [和物件計數](checksums-and-object-counts.md)。</span><span class="sxs-lookup"><span data-stu-id="5daa6-116">For more information, see [Checksums and Object Counts](checksums-and-object-counts.md).</span></span>

 

 




