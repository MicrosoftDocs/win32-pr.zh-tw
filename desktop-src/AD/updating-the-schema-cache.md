---
title: 更新架構快取
description: 寫入 Active Directory 伺服器的所有資訊都會針對架構進行驗證。
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- 更新架構快取 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671211"
---
# <a name="updating-the-schema-cache"></a><span data-ttu-id="dfc5b-104">更新架構快取</span><span class="sxs-lookup"><span data-stu-id="dfc5b-104">Updating the Schema Cache</span></span>

<span data-ttu-id="dfc5b-105">寫入 Active Directory 伺服器的所有資訊都會針對架構進行驗證。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-105">All information that is written to an Active Directory server is validated against the schema.</span></span> <span data-ttu-id="dfc5b-106">基於效能考慮，架構會保留在目錄伺服器 (域) 控制器的記憶體中。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-106">The schema is held in memory on directory servers (domain controllers) for performance reasons.</span></span> <span data-ttu-id="dfc5b-107">記憶體中的版本會在磁片上的版本更新後自動更新。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-107">The in-memory version is updated automatically after the on-disk version has been updated.</span></span> <span data-ttu-id="dfc5b-108">自動更新會在最後一次變更套用後五分鐘完成;在5分鐘的時間範圍內對架構套用另一項變更，會將計時器重設為另5分鐘。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-108">The automatic update occurs five minutes after the last change was applied; applying another change to the schema in the 5-minute window resets the timer for another 5 minutes.</span></span> <span data-ttu-id="dfc5b-109">此行為可讓快取保持一致，但可能會造成混淆，因為在快取更新之前，變更不會出現在架構中，即使已在磁片上套用也一樣。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-109">This behavior keeps the cache consistent, but can be confusing, because changes do not appear in the schema until the cache is updated, even though they were applied on disk.</span></span>

<span data-ttu-id="dfc5b-110">若要在架構更新後更新 Active Directory 的架構快取，或如果您想要立即使用非架構作業的架構更新，請新增 **schemaUpdateNow** 屬性， (它是) 至根 DSE (空白 DN) 值1的操作屬性。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-110">To update the Active Directory schema cache after a schema update, or if you want to use the schema update for non-schema operations immediately, add the **schemaUpdateNow** attribute (it is an operational attribute) to the root DSE (blank DN) with value 1.</span></span> <span data-ttu-id="dfc5b-111">架構快取更新會立即開始。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-111">A schema cache update will start immediately.</span></span> <span data-ttu-id="dfc5b-112">呼叫正在封鎖中。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-112">The call is blocking.</span></span> <span data-ttu-id="dfc5b-113">如果呼叫傳回時未發生錯誤，則會更新快取，而且所有架構更新都可以使用。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-113">If the call returns with no error, the cache is updated and all schema updates are ready to be used.</span></span> <span data-ttu-id="dfc5b-114">傳回錯誤表示快取更新失敗。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-114">An error return indicates the cache update was unsuccessful.</span></span> <span data-ttu-id="dfc5b-115">必須使用這項功能的應用程式應設計成可容納封鎖寫入，特別是當程式或腳本以互動方式執行時，提供使用者意見反應。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-115">Applications that must use this feature should be designed to accommodate the blocking write, particularly in giving the user feedback, if the program or script executes interactively.</span></span>

<span data-ttu-id="dfc5b-116">下列程式碼範例是範例 LDIFDE 腳本，示範如何觸發快取重載。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-116">The following code example is a sample LDIFDE script that shows how to trigger a cache reload.</span></span>

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

<span data-ttu-id="dfc5b-117">如需如何以程式設計方式更新架構快取的詳細資訊，請參閱更新架構快取的 [範例程式碼](example-code-for-updating-the-schema-cache.md)。</span><span class="sxs-lookup"><span data-stu-id="dfc5b-117">For more information about how to update the schema cache programmatically, see [Example Code for Updating the Schema Cache](example-code-for-updating-the-schema-cache.md).</span></span>

 

 




