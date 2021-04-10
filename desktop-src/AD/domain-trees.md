---
title: 網域樹狀結構
description: 網域樹狀目錄由數個網域所組成，這些網域共用通用的架構和設定，形成連續的命名空間。
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- 域樹 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183024"
---
# <a name="domain-trees"></a><span data-ttu-id="23d2c-104">網域樹狀結構</span><span class="sxs-lookup"><span data-stu-id="23d2c-104">Domain Trees</span></span>

<span data-ttu-id="23d2c-105">*網域樹狀目錄* 由數個網域所組成，這些網域共用通用的架構和設定，形成連續的命名空間。</span><span class="sxs-lookup"><span data-stu-id="23d2c-105">A *domain tree* is made up of several domains that share a common schema and configuration, forming a contiguous namespace.</span></span> <span data-ttu-id="23d2c-106">樹狀結構中的網域也會依信任關係連結在一起。</span><span class="sxs-lookup"><span data-stu-id="23d2c-106">Domains in a tree are also linked together by trust relationships.</span></span> <span data-ttu-id="23d2c-107">Active Directory 是一或多個樹狀結構的集合。</span><span class="sxs-lookup"><span data-stu-id="23d2c-107">Active Directory is a set of one or more trees.</span></span>

<span data-ttu-id="23d2c-108">您可以透過兩種方式來查看樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="23d2c-108">Trees can be viewed two ways.</span></span> <span data-ttu-id="23d2c-109">一個 view 是網域之間的信任關係。</span><span class="sxs-lookup"><span data-stu-id="23d2c-109">One view is the trust relationships between domains.</span></span> <span data-ttu-id="23d2c-110">另一個視圖是網域樹狀結構的命名空間。</span><span class="sxs-lookup"><span data-stu-id="23d2c-110">The other view is the namespace of the domain tree.</span></span>

## <a name="viewing-trust-relationships"></a><span data-ttu-id="23d2c-111">查看信任關係</span><span class="sxs-lookup"><span data-stu-id="23d2c-111">Viewing Trust Relationships</span></span>

<span data-ttu-id="23d2c-112">您可以根據個別網域和現有的信任關係，繪製網域樹狀結構的圖表。</span><span class="sxs-lookup"><span data-stu-id="23d2c-112">You can draw a diagram of a domain tree based on the individual domains and the existing trust relationship.</span></span>

<span data-ttu-id="23d2c-113">Windows 2000 會根據 Kerberos 安全性通訊協定，在網域之間建立信任關係。</span><span class="sxs-lookup"><span data-stu-id="23d2c-113">Windows 2000 establishes trust relationships between domains based on the Kerberos security protocol.</span></span> <span data-ttu-id="23d2c-114">Kerberos 信任是可轉移且階層式-如果網域 A 信任網域 B，而網域 B 信任網域 C，則網域 A 信任網域 C。</span><span class="sxs-lookup"><span data-stu-id="23d2c-114">Kerberos trust is transitive and hierarchical—if domain A trusts domain B, and domain B trusts domain C, then domain A trusts domain C.</span></span>

![網域樹系信任關係](images/domain-trust.png)

## <a name="viewing-the-namespace"></a><span data-ttu-id="23d2c-116">查看命名空間</span><span class="sxs-lookup"><span data-stu-id="23d2c-116">Viewing the Namespace</span></span>

<span data-ttu-id="23d2c-117">您也可以根據命名空間繪製網域樹狀結構的圖表。</span><span class="sxs-lookup"><span data-stu-id="23d2c-117">You can also draw a diagram of a domain tree based on the namespace.</span></span> <span data-ttu-id="23d2c-118">您可以遵循域樹命名空間階層的路徑，判斷物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="23d2c-118">You can determine an object's distinguished name by following the path up the hierarchy of the domain tree namespace.</span></span> <span data-ttu-id="23d2c-119">此視圖適用于將物件分組到邏輯階層中。</span><span class="sxs-lookup"><span data-stu-id="23d2c-119">This view is useful for grouping objects into a logical hierarchy.</span></span> <span data-ttu-id="23d2c-120">連續命名空間的主要優點是，來自命名空間根目錄的深層搜尋會搜尋整個階層。</span><span class="sxs-lookup"><span data-stu-id="23d2c-120">The chief advantage of a contiguous namespace is that a deep search from the root of the namespace searches the entire hierarchy.</span></span>

![命名空間網域樹](images/namespace.png)

 

 




