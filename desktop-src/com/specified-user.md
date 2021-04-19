---
title: 指定的使用者
description: 指定的使用者
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966790"
---
# <a name="specified-user"></a><span data-ttu-id="44796-103">指定的使用者</span><span class="sxs-lookup"><span data-stu-id="44796-103">Specified User</span></span>

<span data-ttu-id="44796-104">指定特定使用者 (以及使用者的密碼) 是 COM 伺服器慣用的身分識別。</span><span class="sxs-lookup"><span data-stu-id="44796-104">Specifying a particular user (and the user's password) is the preferred identity for COM servers.</span></span> <span data-ttu-id="44796-105">偏好使用此身分識別的原因是，不需要在執行伺服器的電腦上記錄任何人來執行伺服器，且如果伺服器將其 class factory 註冊為多用途，則每個用戶端都會與伺服器的相同實例進行交談。</span><span class="sxs-lookup"><span data-stu-id="44796-105">The reason this identity is preferred is that no one has to be logged on the machine where the server is running for the server to run, and every client talks to the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="44796-106">如果伺服器有 GUI，您就不應該選擇此身分識別;如果您這麼做，使用者將看不到使用者介面。</span><span class="sxs-lookup"><span data-stu-id="44796-106">If the server has a GUI, you should not choose this identity; if you do, the user will not be able to see the user interface.</span></span>

<span data-ttu-id="44796-107">這種類型的伺服器具有主要權杖，而且可以存取具有啟動使用者身分識別的伺服器可能無法存取的遠端資源。</span><span class="sxs-lookup"><span data-stu-id="44796-107">This type of server has a primary token and can access remote resources where a server that has the launching-user identity might not be able to.</span></span> <span data-ttu-id="44796-108">如需模擬和存取權杖的詳細資訊，請參閱模擬 [層級](impersonation-levels.md) 和 [掩蓋](cloaking.md)。</span><span class="sxs-lookup"><span data-stu-id="44796-108">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="44796-109">以固定用戶帳戶的身分執行比互動式使用者身分識別更安全，因為只有具有特定使用者密碼的人員才能將此身分識別指派給應用程式。</span><span class="sxs-lookup"><span data-stu-id="44796-109">Running as a fixed user account is more secure than the interactive user identity because this identity can be assigned to the application only by someone who has the specific user's password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44796-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="44796-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44796-111">應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="44796-111">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="44796-112">互動式使用者</span><span class="sxs-lookup"><span data-stu-id="44796-112">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="44796-113">正在啟動使用者</span><span class="sxs-lookup"><span data-stu-id="44796-113">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="44796-114">服務身分識別</span><span class="sxs-lookup"><span data-stu-id="44796-114">Service Identity</span></span>](service-identity.md)
</dt> </dl>

 

 




