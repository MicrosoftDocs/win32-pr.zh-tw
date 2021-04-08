---
title: WinNT 使用者物件
description: WinNT User 物件代表 Windows NT 4.0 網域中的使用者帳戶。
ms.assetid: c57016e2-538b-4f37-a1bb-699fcf3c080d
ms.tgt_platform: multiple
keywords:
- WinNT 使用者物件 ADSI
- WinNT 提供者 ADSI、user 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2448fbc7cd77be9c76290777b16e23b2f7e97e61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931814"
---
# <a name="winnt-user-object"></a><span data-ttu-id="50628-105">WinNT 使用者物件</span><span class="sxs-lookup"><span data-stu-id="50628-105">WinNT User Object</span></span>

<span data-ttu-id="50628-106">WinNT User 物件代表 Windows NT 4.0 網域中的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="50628-106">The WinNT User object represents a user account in a Windows NT 4.0 domain.</span></span> <span data-ttu-id="50628-107">物件展示了特殊功能。</span><span class="sxs-lookup"><span data-stu-id="50628-107">The object exhibits special features.</span></span> <span data-ttu-id="50628-108">在一個實例中，它不支援 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 介面的所有屬性方法。</span><span class="sxs-lookup"><span data-stu-id="50628-108">In one instance, it does not support all the property methods of the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span> <span data-ttu-id="50628-109">在第二個實例中，它支援一些只能使用 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get) 或 [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) 方法存取的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="50628-109">In a second instance, it supports some custom properties that can be accessed only with the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span>

<span data-ttu-id="50628-110">如需 WinNT 使用者物件的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="50628-110">For more information about WinNT user objects, see:</span></span>

-   [<span data-ttu-id="50628-111">不支援的 IADsUser 屬性</span><span class="sxs-lookup"><span data-stu-id="50628-111">Unsupported IADsUser Properties</span></span>](unsupported-iadsuser-properties.md)
-   [<span data-ttu-id="50628-112">WinNT 自訂使用者屬性</span><span class="sxs-lookup"><span data-stu-id="50628-112">WinNT Custom User Properties</span></span>](winnt-custom-user-properties.md)
-   [<span data-ttu-id="50628-113">WinNT 使用者帳戶管理範例</span><span class="sxs-lookup"><span data-stu-id="50628-113">WinNT User Account Management Examples</span></span>](winnt-user-account-management-examples.md)

 

 




