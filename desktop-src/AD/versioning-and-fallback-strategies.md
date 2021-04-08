---
title: 版本控制和回溯策略
description: 當應用程式使用上述其中一項技術來偵測部分更新，或讀取一組尚未到達其生效日期的物件時，應用程式必須正常地處理這種情況。
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- 版本控制和回溯策略廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839263"
---
# <a name="versioning-and-fallback-strategies"></a><span data-ttu-id="fe0e4-104">版本控制和回溯策略</span><span class="sxs-lookup"><span data-stu-id="fe0e4-104">Versioning and Fallback Strategies</span></span>

<span data-ttu-id="fe0e4-105">當應用程式使用上述其中一項技術來偵測部分更新，或讀取一組尚未到達其生效日期的物件時，應用程式必須正常地處理這種情況。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-105">When an application detects a partial update using one of the preceding techniques or reads a set of objects whose effective date has not yet been reached, the application must deal with the situation gracefully.</span></span> <span data-ttu-id="fe0e4-106">對於某些應用程式而言，適當的回應是「切換回」先前的物件版本。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-106">For some applications, the graceful response is to "fall back" to a previous version of the objects in question.</span></span> <span data-ttu-id="fe0e4-107">Active Directory Domain Services 不提供版本控制功能，則需要這項功能的應用程式必須自行提供。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-107">Active Directory Domain Services do not provide a versioning facility—applications that want this capability must provide it themselves.</span></span> <span data-ttu-id="fe0e4-108">版本控制的方法包括將「最後已知的良好」值保留在本機快取，並在目錄中儲存多組物件，例如在「舊」、「目前」和「新」容器中。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-108">Approaches to versioning include keeping the "last known good" values cached locally and storing multiple sets of objects in the directory, for example, in "old," "current," and "new" containers.</span></span> <span data-ttu-id="fe0e4-109">可能有許多其他架構。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-109">Many other schemes are possible.</span></span>

<span data-ttu-id="fe0e4-110">執行必須小心避免非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-110">Implementations must take care to avoid unintended consequences.</span></span> <span data-ttu-id="fe0e4-111">只有在偵測到部分更新或新物件尚未「生效」時，才應該使用舊版的物件。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-111">An earlier version of objects should be used only when a partial update is detected or the new objects are not yet "effective."</span></span> <span data-ttu-id="fe0e4-112">由於應用程式「無法運作」中的某些內容，可能會規避系統管理員的意圖。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-112">Falling back because something in the application "does not work" might circumvent an administrator's intent.</span></span> <span data-ttu-id="fe0e4-113">例如，兩部先前可以通訊的電腦可能會因為網際網路通訊協定安全性 (IPsec) 原則的變更，而發現自己無法這麼做。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-113">For example, two computers that formerly could communicate might find themselves unable to do so because of a change in Internet Protocol security (IPsec) policy.</span></span> <span data-ttu-id="fe0e4-114">如果這是系統管理員的一部分，受影響的系統不應該回復至允許它們進行通訊的原則，因為這會造成安全性缺口。</span><span class="sxs-lookup"><span data-stu-id="fe0e4-114">If this is intentional on the part of the administrator, the affected systems should not fall back to the policy that allowed them to communicate, as this would be a security breach.</span></span>

 

 




