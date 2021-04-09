---
title: MGM 程式設計考慮
description: 當您正在開發多播群組管理員用戶端時，請遵守下列指導方針
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- 多播，程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840388"
---
# <a name="mgm-programming-considerations"></a><span data-ttu-id="83365-104">MGM 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="83365-104">MGM Programming Considerations</span></span>

<span data-ttu-id="83365-105">當您正在開發多播群組管理員用戶端時，請遵守下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="83365-105">When you are developing multicast group manager clients, observe the following guidelines:</span></span>

-   <span data-ttu-id="83365-106">您必須在路由器進程內進行函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="83365-106">Function calls must be made from within the router process.</span></span> <span data-ttu-id="83365-107">如果從另一個進程呼叫函數，其結果將無效;用戶端不會與多播群組管理員互動。</span><span class="sxs-lookup"><span data-stu-id="83365-107">If functions are called from another process, their results will not be valid; the client will not interact with the multicast group manager.</span></span>
-   <span data-ttu-id="83365-108">使用 MGM API 的用戶端必須提供自己的錯誤檢查，以確保只有有效的資料會傳遞至多播群組管理員。</span><span class="sxs-lookup"><span data-stu-id="83365-108">Clients that use the MGM API must provide their own error checking, ensuring that only valid data is passed to the multicast group manager.</span></span> <span data-ttu-id="83365-109">MGM 函數不會傳回關於無效參數的詳細錯誤訊息;錯誤 \_ 不正確 \_ 參數值會傳回而不會有說明。</span><span class="sxs-lookup"><span data-stu-id="83365-109">MGM functions do not return detailed error messages about invalid parameters; the ERROR\_INVALID\_PARAMETER value is returned without explanation.</span></span>
-   <span data-ttu-id="83365-110">用戶端在呼叫 MGM 函式時，應謹慎使用鎖定。</span><span class="sxs-lookup"><span data-stu-id="83365-110">Clients should exercise caution in using locks while calling MGM functions.</span></span> <span data-ttu-id="83365-111">這樣做可以防止鎖死。</span><span class="sxs-lookup"><span data-stu-id="83365-111">Doing so can prevent deadlocks.</span></span> <span data-ttu-id="83365-112">呼叫 MGM 函式時，用戶端不應該保留任何可能同時在多播群組管理員回呼中保存的鎖定。</span><span class="sxs-lookup"><span data-stu-id="83365-112">When calling MGM functions, clients should not hold any locks that might simultaneously be held in a callback from the multicast group manager.</span></span>

 

 




