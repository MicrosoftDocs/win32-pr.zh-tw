---
title: 選擇要使用的系結控制碼類型
description: 選擇要使用的系結控制碼類型
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021162"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a><span data-ttu-id="8ddb8-103">選擇要使用的系結控制碼類型</span><span class="sxs-lookup"><span data-stu-id="8ddb8-103">Choosing the Type of Binding Handles to Use</span></span>

<span data-ttu-id="8ddb8-104">**最佳做法：** 如果您知道應用程式將使用哪一台伺服器，請使用明確的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-104">**Best practice:** If you know which server the application will use, use explicit handles.</span></span> <span data-ttu-id="8ddb8-105">如果不是，請每次都使用明確控制碼結構，或搭配 **\_ 使用泛型控制碼與系** 結和 **\_ 解除** 系結常式。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-105">If you don't, use explicit handles construct every time, or use generic handles with **\_bind** and **\_unbind** routines.</span></span>

<span data-ttu-id="8ddb8-106">請勿使用隱含控制碼或自動控制碼。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-106">Do not use implicit handles or auto handles.</span></span> <span data-ttu-id="8ddb8-107">隱含控制碼不是安全線程，即使執行緒安全看似不必要，稍後可能會變成必要。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-107">Implicit handles are not thread safe, and even though thread safety may seem unnecessary, it could become necessary later.</span></span> <span data-ttu-id="8ddb8-108">自動控制碼的負荷很大，而且需要很多的設定才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-108">Auto handles have large overhead and require a lot of setup to work properly.</span></span> <span data-ttu-id="8ddb8-109">Active Directory 服務已取代其搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-109">Their search capabilities have been superseded by Active Directory services.</span></span>

<span data-ttu-id="8ddb8-110">明確控制碼非常有效率，而且許多吸引人的功能只適用于明確的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-110">Explicit handles are highly efficient, and many attractive capabilities are available only for explicit handles.</span></span> <span data-ttu-id="8ddb8-111">例如，如果有多個 RPC 呼叫將會進入相同的伺服器，您可以建立系結控制碼一次，並使用它來進行所有呼叫。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-111">For example, if several RPC calls will be going to the same server, you can construct the binding handle once and make all calls with it.</span></span> <span data-ttu-id="8ddb8-112">這種方法比其他方法更有效率。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-112">This approach is much more efficient than any other method.</span></span> <span data-ttu-id="8ddb8-113">如果呼叫將移至的伺服器不明，請為每個呼叫建立明確的系結控制碼，或使用泛型系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-113">If the server to which the call will go is unknown, construct an explicit binding handle for every call, or use generic binding handles.</span></span>

<span data-ttu-id="8ddb8-114">在 Microsoft™ Windows XP 中，RPC 執行時間在重複使用和快取呼叫上相當有效率，因此，如果 *n*+ 1 呼叫最後會在與第 *n* 次呼叫相同的伺服器上，則 rpc 會重新使用配置給第 *n* 次呼叫的資源，而不需要快取系結控制碼來改善效能。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-114">In Microsoft™ Windows XP, the RPC run time is quite efficient in re-using and caching calls, so if the *n*+1st call ends up on the same server as the *n* th call, RPC re-uses the resources allocated for the *n* th call, circumventing the need to cache binding handles to improve performance.</span></span>

 

 




