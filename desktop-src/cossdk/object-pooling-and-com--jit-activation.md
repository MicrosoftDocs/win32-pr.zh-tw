---
description: 為了達到最佳效能，COM + JIT 啟用基本上會在貪婪用戶端和貪婪伺服器之間遭遇折衷。 用戶端會取得物件參考，而伺服器可以更緊密地管理記憶體使用量。
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: 物件共用和 COM + JIT 啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386006"
---
# <a name="object-pooling-and-com-jit-activation"></a><span data-ttu-id="e3a84-104">物件共用和 COM + JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="e3a84-104">Object Pooling and COM+ JIT Activation</span></span>

<span data-ttu-id="e3a84-105">為了達到最佳效能，COM + JIT 啟用基本上會在貪婪用戶端和貪婪伺服器之間遭遇折衷。</span><span class="sxs-lookup"><span data-stu-id="e3a84-105">COM+ JIT activation essentially strikes a compromise between greedy clients and greedy servers for the sake of getting optimal performance.</span></span> <span data-ttu-id="e3a84-106">用戶端會取得物件參考，而伺服器可以更緊密地管理記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="e3a84-106">Clients get to keep object references, while servers can more closely manage memory utilization.</span></span>

<span data-ttu-id="e3a84-107">您可以使用 [Com + 物件](com--object-pooling.md)共用來進一步改善。</span><span class="sxs-lookup"><span data-stu-id="e3a84-107">You can refine this further by using [COM+ Object Pooling](com--object-pooling.md).</span></span> <span data-ttu-id="e3a84-108">藉由共用 JIT 啟動的物件，您可以專用特定數量的記憶體，以在記憶體中保留特定數量的物件，以準備立即重複使用。</span><span class="sxs-lookup"><span data-stu-id="e3a84-108">By pooling objects that are JIT activated, you can dedicate a certain amount of memory to hold a certain number of objects active in memory, ready for immediate reuse.</span></span> <span data-ttu-id="e3a84-109">當物件的建立成本很高時，這會是最有意義的，如同在保存多個資源的情況下。</span><span class="sxs-lookup"><span data-stu-id="e3a84-109">This makes the most sense when objects are expensive to create, as in the case where they hold multiple resources.</span></span>

<span data-ttu-id="e3a84-110">以這種方式共用 JIT 啟用的物件，您可以達到下列優點：</span><span class="sxs-lookup"><span data-stu-id="e3a84-110">Pooling JIT-activated objects in this manner, you can achieve the following benefits:</span></span>

-   <span data-ttu-id="e3a84-111">大幅加速的物件重新開機時間。</span><span class="sxs-lookup"><span data-stu-id="e3a84-111">Greatly accelerated object reactivation times.</span></span>
-   <span data-ttu-id="e3a84-112">重複使用物件所持有的任何昂貴資源。</span><span class="sxs-lookup"><span data-stu-id="e3a84-112">Reuse of any expensive resources the objects are holding.</span></span>
-   <span data-ttu-id="e3a84-113">更精確地控制集區物件的記憶體和資源使用。</span><span class="sxs-lookup"><span data-stu-id="e3a84-113">More precise governing of memory and resource use for the pooled objects.</span></span>
-   <span data-ttu-id="e3a84-114">保留系統管理彈性，讓您的應用程式可以調整以使用可用的資源，並適應變更的效能需求。</span><span class="sxs-lookup"><span data-stu-id="e3a84-114">Retention of administrative flexibility so that your application can scale to use available resources and adapt to changing performance requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3a84-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3a84-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3a84-116">COM + 即時啟用概念</span><span class="sxs-lookup"><span data-stu-id="e3a84-116">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="e3a84-117">COM + 物件共用</span><span class="sxs-lookup"><span data-stu-id="e3a84-117">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="e3a84-118">啟用元件的 JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="e3a84-118">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="e3a84-119">交易和 COM + JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="e3a84-119">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



