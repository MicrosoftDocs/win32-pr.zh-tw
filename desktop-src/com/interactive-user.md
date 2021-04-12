---
title: 互動式使用者
description: 互動式使用者是目前登入執行 COM 伺服器之電腦的使用者。
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316519"
---
# <a name="interactive-user"></a><span data-ttu-id="2d154-103">互動式使用者</span><span class="sxs-lookup"><span data-stu-id="2d154-103">Interactive User</span></span>

<span data-ttu-id="2d154-104">*互動式使用者* 是目前登入執行 COM 伺服器之電腦的使用者。</span><span class="sxs-lookup"><span data-stu-id="2d154-104">The *interactive user* is the user that is currently logged on to the computer where the COM server is running.</span></span> <span data-ttu-id="2d154-105">如果身分識別設定為互動式使用者，則如果伺服器將其 class factory 註冊為多用途，則所有用戶端都會使用相同的伺服器實例。</span><span class="sxs-lookup"><span data-stu-id="2d154-105">If the identity is set to be the interactive user, all clients use the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="2d154-106">如果沒有登入的使用者，伺服器將不會執行。</span><span class="sxs-lookup"><span data-stu-id="2d154-106">If no user is logged on, the server will not run.</span></span> <span data-ttu-id="2d154-107">如果伺服器有圖形化使用者介面 (GUI) 用戶端必須看到，您應該將互動式使用者用於伺服器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="2d154-107">If the server has a graphical user interface (GUI) that the client needs to see, you should use interactive user for the server's identity.</span></span> <span data-ttu-id="2d154-108">不過，選擇此身分識別會帶來一些安全性風險，因為伺服器會在登入使用者的身分識別下執行，而沒有登入使用者的知識或同意。</span><span class="sxs-lookup"><span data-stu-id="2d154-108">However, choosing this identity carries some security risks because the server runs under the identity of the logged on user without the logged on user's knowledge or consent.</span></span> <span data-ttu-id="2d154-109">此外，服務應用程式無法顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="2d154-109">In addition, a service application cannot display a user interface.</span></span> <span data-ttu-id="2d154-110">如需詳細資訊，請參閱 [互動式服務](/windows/desktop/Services/interactive-services)。</span><span class="sxs-lookup"><span data-stu-id="2d154-110">For more information, see [Interactive Services](/windows/desktop/Services/interactive-services).</span></span>

<span data-ttu-id="2d154-111">如果將 COM 伺服器設定為以互動式使用者的身分執行，則在終端機服務環境中，伺服器將會在符合用戶端使用者身分識別的互動式會話中啟動。</span><span class="sxs-lookup"><span data-stu-id="2d154-111">If a COM server is configured to run as the interactive user, in a terminal services environment, the server will be launched in the interactive session that matches the client's user identity.</span></span> <span data-ttu-id="2d154-112">不過，用戶端應用程式可以在不符合用戶端身分識別的會話中，使用會話的標記來參考伺服器所提供的物件。</span><span class="sxs-lookup"><span data-stu-id="2d154-112">However, the client application can use the session moniker to reference an object provided by the server in a session that does not match the client identity.</span></span> <span data-ttu-id="2d154-113">當使用此項時，用戶端應用程式可以指定任何會話，在這種情況下，伺服器將會以擁有會話的使用者身分執行，而不是啟動的使用者。</span><span class="sxs-lookup"><span data-stu-id="2d154-113">When this is used, the client application can specify any session, in which case the server will run as the user who owns the session, not the launching user.</span></span> <span data-ttu-id="2d154-114">此案例中的預設存取權限不允許啟動使用者呼叫伺服器上的方法。</span><span class="sxs-lookup"><span data-stu-id="2d154-114">The default access permissions in this scenario would not allow the launching user to call methods on the server.</span></span> <span data-ttu-id="2d154-115">不過，仍會有下列安全性風險：</span><span class="sxs-lookup"><span data-stu-id="2d154-115">However, the following security risks remain:</span></span>

-   <span data-ttu-id="2d154-116">如果 COM 伺服器公開不是由 COM 控制的介面，例如 TCP 埠、具名管道、LPC 埠、共用記憶體區段等等，則啟動使用者可以使用這些介面來影響伺服器。</span><span class="sxs-lookup"><span data-stu-id="2d154-116">If the COM server exposes interfaces that are not controlled by COM, such as TCP ports, named pipes, LPC ports, shared memory sections, and so on, these could be used by the launching user to influence the server.</span></span> <span data-ttu-id="2d154-117">設定為以互動式使用者的身份執行的 COM 物件應盡可能減少此受攻擊面。</span><span class="sxs-lookup"><span data-stu-id="2d154-117">COM objects configured to run as the interactive user should reduce this attack surface as much as possible.</span></span>
-   <span data-ttu-id="2d154-118">COM 物件可自由設定自己的存取權限。</span><span class="sxs-lookup"><span data-stu-id="2d154-118">COM objects are free to set their own access permissions.</span></span> <span data-ttu-id="2d154-119">如果物件在其 AppID 註冊中或藉由呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)來設定存取權限，以允許啟動使用者存取，則使用者可以啟動伺服器以另一位使用者的身份執行，然後存取該物件。</span><span class="sxs-lookup"><span data-stu-id="2d154-119">If the object sets access permissions, either in its AppID registration or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), to allow the launching user access, the user would be able to launch the server to run as another user, then access the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d154-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d154-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d154-121">應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="2d154-121">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="2d154-122">正在啟動使用者</span><span class="sxs-lookup"><span data-stu-id="2d154-122">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="2d154-123">服務身分識別</span><span class="sxs-lookup"><span data-stu-id="2d154-123">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="2d154-124">指定的使用者</span><span class="sxs-lookup"><span data-stu-id="2d154-124">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 