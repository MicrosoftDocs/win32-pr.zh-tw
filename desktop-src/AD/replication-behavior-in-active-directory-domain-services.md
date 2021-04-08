---
title: Active Directory Domain Services 中的複寫行為
description: 複寫行為是一致且可預測的;給定複本的一組變更之後，就可以預測結果 \ 郵件; 變更將會傳播到所有其他複本。
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory，複寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839271"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a><span data-ttu-id="0fb76-104">Active Directory Domain Services 中的複寫行為</span><span class="sxs-lookup"><span data-stu-id="0fb76-104">Replication Behavior in Active Directory Domain Services</span></span>

<span data-ttu-id="0fb76-105">複寫行為是一致且可預測的;如果指定的複本有一組變更，可以預測結果，變更將會傳播到所有其他複本。</span><span class="sxs-lookup"><span data-stu-id="0fb76-105">Replication behavior is consistent and predictable; given a set of changes to a given replica, the outcome can be predicted—the changes will be propagated to all other replicas.</span></span> <span data-ttu-id="0fb76-106">設計可靠的一般模型來預測在所有其他複本或特定複本上套用變更的時間，因為無法得知分散式系統的未來狀態，所以不可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="0fb76-106">Devising a reliable general model for predicting when the changes will be applied at all other replicas, or at a particular replica, is impossible, because the future state of the distributed system as a whole cannot be known.</span></span> <span data-ttu-id="0fb76-107">這稱為「不具決定性的延遲」，而使用該目錄的應用程式必須瞭解並允許它。</span><span class="sxs-lookup"><span data-stu-id="0fb76-107">This is called "nondeterministic latency," and applications that use the directory must understand and allow for it.</span></span>

<span data-ttu-id="0fb76-108">這種情況並不複雜，可能會出現。</span><span class="sxs-lookup"><span data-stu-id="0fb76-108">The situation is not as complex at it might appear.</span></span> <span data-ttu-id="0fb76-109">應用程式只需要有三個狀態：</span><span class="sxs-lookup"><span data-stu-id="0fb76-109">There are only three states that an application must accommodate:</span></span>

-   <span data-ttu-id="0fb76-110">版本扭曲：任何套用至指定來源複本的變更都未傳播到指定的目的地複本。</span><span class="sxs-lookup"><span data-stu-id="0fb76-110">Version Skew: None of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="0fb76-111">讀取來源複本的應用程式會看到新版本的資訊，而讀取目的地的應用程式會看到舊版 (或沒有任何專案，如果新資訊是在第一次) 時新增的。</span><span class="sxs-lookup"><span data-stu-id="0fb76-111">An application reading the source replica sees the new version of the information, while an application reading the destination sees the old version (or nothing, if the new information was added for the first time).</span></span> <span data-ttu-id="0fb76-112">版本扭曲適用于所有目錄服務取用者。</span><span class="sxs-lookup"><span data-stu-id="0fb76-112">Version skew applies to all directory service consumers.</span></span>
-   <span data-ttu-id="0fb76-113">部分更新：套用至指定來源複本的部分變更已傳播到指定的目的地複本。</span><span class="sxs-lookup"><span data-stu-id="0fb76-113">Partial Update: Some of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="0fb76-114">讀取來源複本的應用程式會看到新的資訊，而讀取目的地的應用程式會將舊的和新的資訊混用 (或只有一些新的資訊，如果是第一次加入的新資訊) 。</span><span class="sxs-lookup"><span data-stu-id="0fb76-114">An application reading the source replica sees the new information, while an application reading the destination sees a mix of old and new information (or only some of the new information, if the new information was added for the first time).</span></span> <span data-ttu-id="0fb76-115">部分更新適用于使用兩個或多個相關物件來儲存其資訊的目錄服務取用者。</span><span class="sxs-lookup"><span data-stu-id="0fb76-115">Partial update applies to directory service consumers that use two or more related objects to store their information.</span></span>
-   <span data-ttu-id="0fb76-116">完整複寫狀態：套用至指定來源複本的所有變更都會傳播到指定的目的地複本。</span><span class="sxs-lookup"><span data-stu-id="0fb76-116">Fully Replicated State: All of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="0fb76-117">來源和目的地複本上的應用程式會看到相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="0fb76-117">Applications at the source and destination replicas see the same information.</span></span>

 

 




