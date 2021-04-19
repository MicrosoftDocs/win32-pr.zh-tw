---
description: 資源管理員會在單一進程中以受信任服務的形式執行。 所有智慧卡存取的要求都是對資源管理員進行，它會將這些要求路由傳送至包含目標卡片的讀取器。
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Resource Manager 的執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982403"
---
# <a name="resource-manager-implementation"></a><span data-ttu-id="0c551-104">Resource Manager 的執行</span><span class="sxs-lookup"><span data-stu-id="0c551-104">Resource Manager Implementation</span></span>

<span data-ttu-id="0c551-105">[*資源管理員*](../secgloss/r-gly.md)會在單一進程中以受信任服務的形式執行。</span><span class="sxs-lookup"><span data-stu-id="0c551-105">The [*resource manager*](../secgloss/r-gly.md) runs as a trusted service in a single process.</span></span> <span data-ttu-id="0c551-106">所有 [*智慧卡*](../secgloss/s-gly.md) 存取的要求都是對資源管理員進行，它會將這些要求路由傳送至包含目標卡片的 [*讀取器*](../secgloss/r-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="0c551-106">All requests for [*smart card*](../secgloss/s-gly.md) access are made to the resource manager, which routes them to the [*reader*](../secgloss/r-gly.md) that contains the targeted card.</span></span>

<span data-ttu-id="0c551-107">智慧卡通常會與安全性和個人隱私一起使用。</span><span class="sxs-lookup"><span data-stu-id="0c551-107">Smart cards are often used in conjunction with security and personal privacy.</span></span> <span data-ttu-id="0c551-108">在可能的情況下，資源管理員會在存取讀取器或智慧卡時，使用基礎作業系統內現有的安全性機制。</span><span class="sxs-lookup"><span data-stu-id="0c551-108">Wherever possible, the resource manager uses the security mechanisms existing within the underlying operating system when accessing a reader or smart card.</span></span>

 

 
