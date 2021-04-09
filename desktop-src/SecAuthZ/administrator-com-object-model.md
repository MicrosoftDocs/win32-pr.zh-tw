---
description: 以標準使用者身分執行的應用程式會藉由建立提高許可權的元件物件模型物件，執行需要系統管理員許可權的作業。
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: 系統管理員 COM 物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c7d73cf31ce86c4788675374f34d04f6acf106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851108"
---
# <a name="administrator-com-object-model"></a><span data-ttu-id="68d49-103">系統管理員 COM 物件模型</span><span class="sxs-lookup"><span data-stu-id="68d49-103">Administrator COM Object Model</span></span>

<span data-ttu-id="68d49-104">在系統管理員 COM 物件模型中，以標準使用者身分執行的應用程式會藉由建立提高許可權的 [元件物件模型](/windows/desktop/com/component-object-model--com--portal) 物件，執行需要系統管理員許可權的作業。</span><span class="sxs-lookup"><span data-stu-id="68d49-104">In the administrator COM object model, an application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> <span data-ttu-id="68d49-105">如需建立提高許可權的 COM 物件的詳細資訊，請參閱 [COM 提高許可權的標記](../com/the-com-elevation-moniker.md)。</span><span class="sxs-lookup"><span data-stu-id="68d49-105">For information about creating an elevated COM object, see [The COM Elevation Moniker](../com/the-com-elevation-moniker.md).</span></span>

<span data-ttu-id="68d49-106">使用系統管理員 COM 物件模型有一個缺點，就是每次執行特殊許可權作業時都會提示使用者。</span><span class="sxs-lookup"><span data-stu-id="68d49-106">One drawback to using the administrator COM object model is that the user is prompted each time a privileged operation is performed.</span></span>

<span data-ttu-id="68d49-107">任何可以控制 COM 物件的使用者介面都必須由 COM 物件本身呈現。</span><span class="sxs-lookup"><span data-stu-id="68d49-107">Any user interface that can control the COM object must be presented by the COM object itself.</span></span> <span data-ttu-id="68d49-108">否則，無特殊許可權的進程可能會造成提高許可權的 COM 物件執行具有特殊許可權的作業，而不會提示使用者。</span><span class="sxs-lookup"><span data-stu-id="68d49-108">Otherwise, an unprivileged process could cause the elevated COM object to perform privileged operations without the user being prompted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68d49-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="68d49-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68d49-110">開發需要系統管理員許可權的應用程式</span><span class="sxs-lookup"><span data-stu-id="68d49-110">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="68d49-111">系統管理員訊息代理程式模型</span><span class="sxs-lookup"><span data-stu-id="68d49-111">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="68d49-112">提高許可權的工作模型</span><span class="sxs-lookup"><span data-stu-id="68d49-112">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> <dt>

[<span data-ttu-id="68d49-113">作業系統服務模型</span><span class="sxs-lookup"><span data-stu-id="68d49-113">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
