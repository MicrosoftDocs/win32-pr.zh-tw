---
title: 將主機電腦上的 [以服務方式登入] 許可權授與許可權
description: 當安裝服務在網域使用者帳戶下執行時，帳戶必須擁有在本機電腦上以服務方式登入的許可權。
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671275"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a><span data-ttu-id="3c3fd-103">將主機電腦上的 [以服務方式登入] 許可權授與許可權</span><span class="sxs-lookup"><span data-stu-id="3c3fd-103">Granting Logon as Service Right on the Host Computer</span></span>

<span data-ttu-id="3c3fd-104">當安裝服務在網域使用者帳戶下執行時，帳戶必須擁有在本機電腦上以服務方式登入的許可權。</span><span class="sxs-lookup"><span data-stu-id="3c3fd-104">When installing a service to run under a domain user account, the account must have the right to logon as a service on the local computer.</span></span> <span data-ttu-id="3c3fd-105">請注意，此登入許可權僅適用于本機電腦，必須在每部主機電腦的本機 LSA 原則中授與。</span><span class="sxs-lookup"><span data-stu-id="3c3fd-105">Be aware that this logon right applies only to the local computer and must be granted in the local LSA policy of each host computer.</span></span> <span data-ttu-id="3c3fd-106">如果您的服務是以 LocalSystem 的身分執行（依預設會授與此許可權），則不需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="3c3fd-106">This step is not required if your service runs as LocalSystem, which, by default, is granted this right.</span></span>

<span data-ttu-id="3c3fd-107">如需如何以程式設計方式授與登入服務許可權的詳細資訊，請參閱 [LSAPrivs 範例程式碼](https://www.google.com/#q=LSAPrivs)。</span><span class="sxs-lookup"><span data-stu-id="3c3fd-107">For more information on how to programmatically grant logon as a service right, see the [LSAPrivs sample code](https://www.google.com/#q=LSAPrivs).</span></span>

 

 




