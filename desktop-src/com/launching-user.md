---
title: 正在啟動使用者
description: 正在啟動使用者
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842767"
---
# <a name="launching-user"></a><span data-ttu-id="f871e-103">正在啟動使用者</span><span class="sxs-lookup"><span data-stu-id="f871e-103">Launching User</span></span>

<span data-ttu-id="f871e-104">這是應用程式識別碼的預設設定。</span><span class="sxs-lookup"><span data-stu-id="f871e-104">This is the default setting for the application identity.</span></span> <span data-ttu-id="f871e-105">當針對應用程式的身分識別選擇啟動使用者時，每個用戶端帳戶都會取得伺服器的新實例，且每部伺服器都會取得自己的 [視窗工作站](/windows/desktop/winstation/window-stations)。</span><span class="sxs-lookup"><span data-stu-id="f871e-105">When the launching user is chosen for the application's identity, each client account gets a new instance of the server and each server gets its own [window station](/windows/desktop/winstation/window-stations).</span></span> <span data-ttu-id="f871e-106">由於個別的伺服器實例，啟動使用者是最高層級的安全性保護身分識別設定。</span><span class="sxs-lookup"><span data-stu-id="f871e-106">Because of the separate server instances, launching user is the highest-level security protection identity setting.</span></span> <span data-ttu-id="f871e-107">不過，資源耗用量有有限的限制。</span><span class="sxs-lookup"><span data-stu-id="f871e-107">However, there are finite limits on resource consumption.</span></span> <span data-ttu-id="f871e-108">此外，用戶端將看不到伺服器所顯示的任何 GUI。</span><span class="sxs-lookup"><span data-stu-id="f871e-108">Also, any GUI the server displays will not be seen by the client.</span></span>

<span data-ttu-id="f871e-109">如果應用程式具有啟動使用者的身分識別，則會以模擬權杖執行。</span><span class="sxs-lookup"><span data-stu-id="f871e-109">If the application has the identity of the launching user, it runs with an impersonation token.</span></span> <span data-ttu-id="f871e-110">如需模擬和存取權杖的詳細資訊，請參閱模擬 [層級](impersonation-levels.md) 和 [掩蓋](cloaking.md)。</span><span class="sxs-lookup"><span data-stu-id="f871e-110">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f871e-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="f871e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f871e-112">應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="f871e-112">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="f871e-113">互動式使用者</span><span class="sxs-lookup"><span data-stu-id="f871e-113">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="f871e-114">服務身分識別</span><span class="sxs-lookup"><span data-stu-id="f871e-114">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="f871e-115">指定的使用者</span><span class="sxs-lookup"><span data-stu-id="f871e-115">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 