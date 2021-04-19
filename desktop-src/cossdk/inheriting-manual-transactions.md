---
description: 繼承手動交易
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: 繼承手動交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970099"
---
# <a name="inheriting-manual-transactions"></a><span data-ttu-id="2de20-103">繼承手動交易</span><span class="sxs-lookup"><span data-stu-id="2de20-103">Inheriting Manual Transactions</span></span>

<span data-ttu-id="2de20-104">如果具有 BYOT 交易的物件在其內容中建立第二個物件，則下游物件可以繼承 BYOT 交易 (如果設定為繼承交易) 。</span><span class="sxs-lookup"><span data-stu-id="2de20-104">If an object with a BYOT transaction in its context creates a second object, the downstream object can inherit the BYOT transaction (if configured to inherit transactions).</span></span> <span data-ttu-id="2de20-105">使用 BYOT 閘道建立的第一個物件必須設定為「需要」或「支援」交易。</span><span class="sxs-lookup"><span data-stu-id="2de20-105">The first object created using the BYOT gateway needs to be configured to "require" or "support" transactions.</span></span> <span data-ttu-id="2de20-106">活動中的後續物件可以根據應用程式需求進行設定。</span><span class="sxs-lookup"><span data-stu-id="2de20-106">Subsequent objects in the activity could be configured based on application requirements.</span></span>

<span data-ttu-id="2de20-107">針對自動交易，COM + 執行時間不會嘗試認可交易，直到根物件指出它已準備就緒 (先呼叫 [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ，然後再從呼叫) 傳回。</span><span class="sxs-lookup"><span data-stu-id="2de20-107">For automatic transactions, the COM+ runtime does not attempt to commit the transaction until the root object indicates that it is ready (by calling [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) before returning from a call).</span></span> <span data-ttu-id="2de20-108">使用者應該注意到，BYOT 的交易可能會提早認可 (因為子物件的工作尚未) 完成，因為 "root" 並未在 COM + 執行時間環境下執行，而且 commit 語義未系結至物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="2de20-108">Users should be aware that a BYOT transaction could commit prematurely (in that the work of child objects has not been completed), because the "root" is not running under the COM+ runtime environment, and the commit semantics are not tied to the lifetime of the object.</span></span> <span data-ttu-id="2de20-109">一般情況下，使用者應該小心不會違反交易的同步處理界限。</span><span class="sxs-lookup"><span data-stu-id="2de20-109">In general, the user should take care to not violate the synchronization boundary of the transaction.</span></span>

<span data-ttu-id="2de20-110">否則，就會套用 COM + commit 語義。</span><span class="sxs-lookup"><span data-stu-id="2de20-110">Otherwise, COM+ commit semantics apply.</span></span> <span data-ttu-id="2de20-111">當同步處理界限內的物件正在呼叫時，COM + 將不會嘗試認可交易。</span><span class="sxs-lookup"><span data-stu-id="2de20-111">COM+ will not attempt to commit a transaction while an object within a synchronization boundary is in call.</span></span> <span data-ttu-id="2de20-112">此外，物件也可以使用 [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)來表示其一致性。</span><span class="sxs-lookup"><span data-stu-id="2de20-112">Also, objects can indicate their consistency using [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span></span> <span data-ttu-id="2de20-113">如果嘗試認可的交易包含已呼叫 **DisableCommit** 之物件的工作，交易將會中止。</span><span class="sxs-lookup"><span data-stu-id="2de20-113">If an attempt is made to commit a transaction which includes the work of an object that has called **DisableCommit**, the transaction will abort.</span></span>

 

 



