---
title: 複寫與資料完整性
description: Active Directory Domain Services 提供多宿主更新。
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory、使用、複寫和資料完整性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965769"
---
# <a name="replication-and-data-integrity"></a><span data-ttu-id="272af-104">複寫與資料完整性</span><span class="sxs-lookup"><span data-stu-id="272af-104">Replication and Data Integrity</span></span>

<span data-ttu-id="272af-105">Active Directory Domain Services 提供 *多宿主更新*。</span><span class="sxs-lookup"><span data-stu-id="272af-105">Active Directory Domain Services provide *multi-master update*.</span></span> <span data-ttu-id="272af-106">多宿主更新表示指定磁碟分割的所有完整複本都是可寫入的， (通用類別目錄伺服器上的部分複本無法寫入。 ) 多宿主更新表示即使某些複本無法運作，也不會封鎖更新。</span><span class="sxs-lookup"><span data-stu-id="272af-106">Multi-master update means that all full replicas of a given partition are writable (the partial replicas on global catalog servers are not writable.) Multi-master update means that updates are not blocked even when some replicas are inoperable.</span></span> <span data-ttu-id="272af-107">Active Directory 伺服器會將更新複本的變更傳播至所有其他複本。</span><span class="sxs-lookup"><span data-stu-id="272af-107">The Active Directory server propagates the changes from the updated replica to all other replicas.</span></span> <span data-ttu-id="272af-108">複寫是自動且透明的。</span><span class="sxs-lookup"><span data-stu-id="272af-108">Replication is automatic and transparent.</span></span>

<span data-ttu-id="272af-109">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="272af-109">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="272af-110">Active Directory Domain Services 中的複寫模型</span><span class="sxs-lookup"><span data-stu-id="272af-110">The Replication Model in Active Directory Domain Services</span></span>](replication-model-in-active-directory-domain-services.md)
-   [<span data-ttu-id="272af-111">Active Directory Domain Services 中的複寫行為</span><span class="sxs-lookup"><span data-stu-id="272af-111">Replication Behavior in Active Directory Domain Services</span></span>](replication-behavior-in-active-directory-domain-services.md)
-   [<span data-ttu-id="272af-112">偵測和避免複寫延遲</span><span class="sxs-lookup"><span data-stu-id="272af-112">Detecting and Avoiding Replication Latency</span></span>](detecting-and-avoiding-replication-latency.md)

 

 




