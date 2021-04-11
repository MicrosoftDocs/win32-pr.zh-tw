---
title: 樹系
description: 樹系是一組未形成連續命名空間的一或多個域樹。
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- 樹系 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933068"
---
# <a name="forests"></a><span data-ttu-id="e8a1e-104">樹系</span><span class="sxs-lookup"><span data-stu-id="e8a1e-104">Forests</span></span>

<span data-ttu-id="e8a1e-105">[*樹*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85))系是一組未形成連續命名空間的一或多個域樹。</span><span class="sxs-lookup"><span data-stu-id="e8a1e-105">A [*forest*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) is a set of one or more domain trees that do not form a contiguous namespace.</span></span> <span data-ttu-id="e8a1e-106">樹系中的所有樹狀結構都會共用通用的架構、設定和通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="e8a1e-106">All trees in a forest share a common schema, configuration, and global catalog.</span></span> <span data-ttu-id="e8a1e-107">指定樹系中的所有樹狀結構會根據可轉移的階層式 Kerberos 信任關係進行信任。</span><span class="sxs-lookup"><span data-stu-id="e8a1e-107">All trees in a given forest exchange trust according to transitive hierarchical Kerberos trust relationships.</span></span> <span data-ttu-id="e8a1e-108">不同于樹狀結構，樹系不需要相異的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8a1e-108">Unlike trees, a forest does not require a distinct name.</span></span> <span data-ttu-id="e8a1e-109">樹系以一組交互參考物件和 Kerberos 信任關係的形式存在於成員樹狀結構中。</span><span class="sxs-lookup"><span data-stu-id="e8a1e-109">A forest exists as a set of cross-reference objects and Kerberos trust relationships recognized by the member trees.</span></span> <span data-ttu-id="e8a1e-110">樹系中的樹狀目錄會形成 Kerberos 信任用途的階層;信任樹狀結構根目錄中的樹狀結構名稱是指指定的樹系。</span><span class="sxs-lookup"><span data-stu-id="e8a1e-110">Trees in a forest form a hierarchy for the purposes of Kerberos trust; the tree name at the root of the trust tree refers to a given forest.</span></span>

<span data-ttu-id="e8a1e-111">下圖顯示非連續命名空間的樹系。</span><span class="sxs-lookup"><span data-stu-id="e8a1e-111">The following figure shows a forest of noncontiguous namespaces.</span></span>

![非連續命名空間的樹系](images/forests.png)

 

 