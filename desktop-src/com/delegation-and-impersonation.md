---
title: 委派和模擬
description: 在用戶端/伺服器案例中，一部伺服器通常會呼叫另一部伺服器來代表用戶端完成一些工作。 如果伺服器被授與代表用戶端的許可權，就稱為「委派」。
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104559344"
---
# <a name="delegation-and-impersonation"></a><span data-ttu-id="eba53-104">委派和模擬</span><span class="sxs-lookup"><span data-stu-id="eba53-104">Delegation and Impersonation</span></span>

<span data-ttu-id="eba53-105">在用戶端/伺服器案例中，一部伺服器通常會呼叫另一部伺服器來代表用戶端完成一些工作。</span><span class="sxs-lookup"><span data-stu-id="eba53-105">In client/server scenarios, it is common for one server to call another server to accomplish some task on a client's behalf.</span></span> <span data-ttu-id="eba53-106">如果伺服器被授與代表用戶端的許可權，就稱為「 *委派*」。</span><span class="sxs-lookup"><span data-stu-id="eba53-106">The situation where a server is given the authority to act on a client's behalf is called *delegation*.</span></span>

<span data-ttu-id="eba53-107">從安全性的觀點來看，有兩個關於委派的問題：</span><span class="sxs-lookup"><span data-stu-id="eba53-107">From a security standpoint, two issues arise regarding delegation:</span></span>

-   <span data-ttu-id="eba53-108">代表用戶端時，應該允許伺服器執行哪些動作？</span><span class="sxs-lookup"><span data-stu-id="eba53-108">What should the server be allowed to do when acting on the client's behalf?</span></span>
-   <span data-ttu-id="eba53-109">當伺服器代表用戶端呼叫其他伺服器時，會顯示哪個身分識別？</span><span class="sxs-lookup"><span data-stu-id="eba53-109">What identity is presented by the server when it calls other servers on behalf of a client?</span></span>

<span data-ttu-id="eba53-110">為了處理這些問題，COM 提供下列功能。</span><span class="sxs-lookup"><span data-stu-id="eba53-110">To deal with these issues, COM provides the following functionality.</span></span> <span data-ttu-id="eba53-111">用戶端可以設定模擬 *等級* ，判斷伺服器將能夠做為用戶端的程度。</span><span class="sxs-lookup"><span data-stu-id="eba53-111">The client can set an *impersonation level* that determines to what extent the server will be able to act as the client.</span></span> <span data-ttu-id="eba53-112">如果用戶端將足夠的許可權授與伺服器，伺服器就 *可以模擬* (假裝) 用戶端。</span><span class="sxs-lookup"><span data-stu-id="eba53-112">If the client grants enough authority to the server, the server can *impersonate* (pretend to be) the client.</span></span> <span data-ttu-id="eba53-113">模擬用戶端時，伺服器只會獲得用戶端有權使用之物件或資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="eba53-113">When impersonating the client, the server is given access to only those objects or resources that the client has permission to use.</span></span> <span data-ttu-id="eba53-114">作為用戶端的伺服器也可以啟用遮罩來遮罩自己的身分 *識別，並* 在呼叫其他 COM 元件時投射用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="eba53-114">The server, acting as a client, can also enable *cloaking* to mask its own identity and project the client's identity in calls to other COM components.</span></span>

![此圖顯示作為用戶端的伺服器如何啟用遮蓋。](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

<span data-ttu-id="eba53-116">請考慮上圖所示的案例，其中 A 和 B 是在不同電腦上的 C 處理常式。處理 A 呼叫 B，而 B 呼叫 C. 用戶端 A 設定模擬層級。</span><span class="sxs-lookup"><span data-stu-id="eba53-116">Consider the scenario illustrated by the preceding figure, where A and B are processes on a different machine from C. Process A calls B, and B calls C. Client A sets the impersonation level.</span></span> <span data-ttu-id="eba53-117">B 設定「掩蓋」功能。</span><span class="sxs-lookup"><span data-stu-id="eba53-117">B sets the cloaking capability.</span></span> <span data-ttu-id="eba53-118">如果設定了允許模擬的模擬層級，B 可以在代表的時候模擬。</span><span class="sxs-lookup"><span data-stu-id="eba53-118">If A sets an impersonation level that permits impersonation, B can impersonate A when calling C on A's behalf.</span></span> <span data-ttu-id="eba53-119">呈現給處理 C 的身分識別將會是身分識別或 B 的身分識別，這取決於是否由 B 啟用遮蓋。如果啟用了掩蓋，則呈現給處理 C 的身分識別將會是的。如果未啟用掩蓋功能，B 的身分識別將會顯示為 C。</span><span class="sxs-lookup"><span data-stu-id="eba53-119">The identity that is presented to process C will be either A's identity or B's identity, depending on whether cloaking was enabled by B. If cloaking is enabled, the identity presented to process C will be that of A. If cloaking is not enabled, B's identity will be presented to C.</span></span>

<span data-ttu-id="eba53-120">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="eba53-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="eba53-121">模擬</span><span class="sxs-lookup"><span data-stu-id="eba53-121">Impersonation</span></span>](impersonation.md)
-   [<span data-ttu-id="eba53-122">模擬層級</span><span class="sxs-lookup"><span data-stu-id="eba53-122">Impersonation Levels</span></span>](impersonation-levels.md)
-   [<span data-ttu-id="eba53-123">隱形</span><span class="sxs-lookup"><span data-stu-id="eba53-123">Cloaking</span></span>](cloaking.md)

 

 




