---
title: 我的 RPC 伺服器有多安全？
description: 遵循本節所述的安全性（在 RPC SDK 的其他地方提供），而且通常會被視為適當的安全性作法，將會產生非常安全的伺服器。 這類伺服器會受到保護，以防止滲透攻擊或隱私權缺口。
ms.assetid: 528ff35c-f37c-43d8-8cc1-dbc36a9a826c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34279e4fb8899db6b7e980a0e868e91c6edb8166
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932265"
---
# <a name="how-secure-is-my-rpc-server-now"></a><span data-ttu-id="d98fc-104">我的 RPC 伺服器現在有多安全？</span><span class="sxs-lookup"><span data-stu-id="d98fc-104">How Secure is My RPC Server Now?</span></span>

<span data-ttu-id="d98fc-105">遵循本節所述的安全性（在 RPC SDK 的其他地方提供），而且通常會被視為適當的安全性作法，將會產生非常安全的伺服器。</span><span class="sxs-lookup"><span data-stu-id="d98fc-105">Following the security outlined in this section, provided elsewhere in the RPC SDK, and generally accepted as proper security practices, will result in a server that is very secure.</span></span> <span data-ttu-id="d98fc-106">這類伺服器會受到保護，以防止滲透攻擊或隱私權缺口。</span><span class="sxs-lookup"><span data-stu-id="d98fc-106">Such servers are protected from penetration attacks or privacy breaches.</span></span>

<span data-ttu-id="d98fc-107">如果狀態是在 RPC 呼叫之間保留，請確定單一用戶端不會導致配置過度的資源，而這可能會拒絕其他用戶端的服務。</span><span class="sxs-lookup"><span data-stu-id="d98fc-107">If state is kept between RPC calls, make sure a single client does not cause the allocation of excessive resources, which could potentially deny service to other clients.</span></span>

 

 




