---
title: Active Directory Domain Services 的複寫模型功能
description: 在 Active Directory Domain Services 中使用的複寫模型稱為「聚合」的多重主要鬆散一致性。
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services，複寫模型
- 複寫模型功能 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923c49dd648063ebd6afd086be3729f28f1e4080
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965770"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a><span data-ttu-id="fcbd1-105">Active Directory Domain Services 的複寫模型功能</span><span class="sxs-lookup"><span data-stu-id="fcbd1-105">Features of the Replication Model for Active Directory Domain Services</span></span>

<span data-ttu-id="fcbd1-106">在 Active Directory Domain Services 中使用的複寫模型稱為「聚合」的 *多重主要鬆散一致性*。</span><span class="sxs-lookup"><span data-stu-id="fcbd1-106">The replication model used in Active Directory Domain Services is called *multi-master loose consistency with convergence*.</span></span> <span data-ttu-id="fcbd1-107">在此模型中，目錄可以有多個複本;複寫系統會將任何指定複本所做的變更傳播到所有其他複本。</span><span class="sxs-lookup"><span data-stu-id="fcbd1-107">In this model, the directory can have many replicas; a replication system propagates changes made at any given replica to all other replicas.</span></span> <span data-ttu-id="fcbd1-108">在任何特定時間，複本不保證會彼此一致 ( 「鬆散一致性」 ) ，因為變更可以隨時套用至任何複本 ( 「多宿主」 ) 。</span><span class="sxs-lookup"><span data-stu-id="fcbd1-108">The replicas are not guaranteed to be consistent with each other at any particular time ("loose consistency"), because changes can be applied to any replica at any time ("multi-master").</span></span> <span data-ttu-id="fcbd1-109">如果允許系統達到穩定狀態，但未發生任何新的更新，並且已完全複寫所有先前的更新，則所有複本都保證會在同一組值 ( 「會合」 ) 。</span><span class="sxs-lookup"><span data-stu-id="fcbd1-109">If the system is allowed to reach a steady state, in which no new updates are occurring and all previous updates have been completely replicated, all replicas are guaranteed to converge on the same set of values ("convergence").</span></span>

 

 




