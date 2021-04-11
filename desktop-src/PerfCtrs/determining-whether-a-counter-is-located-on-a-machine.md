---
description: 若要判斷計數器是否已安裝在特定電腦上，請使用完整的計數器路徑來呼叫 PdhValidatePath。 \_如果計數器位於指定的電腦上，此函數會傳回錯誤成功。
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: 判斷計數器是否位於電腦上
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795878e2f9c97989fe924737ec7f8e7f14bdc67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944261"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a><span data-ttu-id="b0329-104">判斷計數器是否位於電腦上</span><span class="sxs-lookup"><span data-stu-id="b0329-104">Determining Whether a Counter Is Located on a Computer</span></span>

<span data-ttu-id="b0329-105">若要判斷計數器是否已安裝在特定電腦上，請使用完整的計數器路徑來呼叫 [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) 。</span><span class="sxs-lookup"><span data-stu-id="b0329-105">To determine if a counter is installed on a particular computer, call [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) with the fully qualified counter path.</span></span> <span data-ttu-id="b0329-106">\_如果計數器位於指定的電腦上，此函數會傳回錯誤成功。</span><span class="sxs-lookup"><span data-stu-id="b0329-106">The function returns ERROR\_SUCCESS if the counter is located on the specified computer.</span></span>

<span data-ttu-id="b0329-107">[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) 會驗證整個路徑;因此，如果路徑中有任何物件、實例或計數器不存在，則傳回值會指出。</span><span class="sxs-lookup"><span data-stu-id="b0329-107">[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) validates the entire path; therefore, if any object, instance, or counter in the path does not exist, the return value indicates so.</span></span> <span data-ttu-id="b0329-108">**PdhValidatePath** 會依下列順序驗證指定的計數器路徑：電腦、效能物件、實例和計數器。</span><span class="sxs-lookup"><span data-stu-id="b0329-108">**PdhValidatePath** verifies the specified counter path in this order: computer, performance object, instance, and counter.</span></span>

 

 



