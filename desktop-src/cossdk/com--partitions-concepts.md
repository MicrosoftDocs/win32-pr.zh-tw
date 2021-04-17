---
description: COM + 磁碟分割概念
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: COM + 磁碟分割概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 483a34e6186cda8978c1882ed1fdfbe8732f7ec8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468125"
---
# <a name="com-partitions-concepts"></a><span data-ttu-id="07e92-103">COM + 磁碟分割概念</span><span class="sxs-lookup"><span data-stu-id="07e92-103">COM+ Partitions Concepts</span></span>

<span data-ttu-id="07e92-104">在需要在同一部電腦上使用不同版本或應用程式設定的運算環境中，當某個版本的應用程式需要不同的元件，或當某個版本需要電腦上與其他應用程式版本不相容的元件時，就會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="07e92-104">In computing environments where it's necessary to use different versions or configurations of an application on the same computer, conflicts can arise when one version of the application requires different components than the other or when one version requires a component on the computer that is incompatible with the other version of the application.</span></span> <span data-ttu-id="07e92-105">在過去，解決此問題的唯一方法是維護多部電腦，並在每部電腦上執行不同版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="07e92-105">In the past, the only way to solve this problem was to maintain multiple computers and run a different version of the application on each computer.</span></span> <span data-ttu-id="07e92-106">這種方法既昂貴又沒有效率，因為它會增加硬體成本和系統管理負擔。</span><span class="sxs-lookup"><span data-stu-id="07e92-106">Such an approach is costly and inefficient because it increases hardware costs and administrative overhead.</span></span>

<span data-ttu-id="07e92-107">COM + 藉由提供 COM + 分割功能來解決這個問題。</span><span class="sxs-lookup"><span data-stu-id="07e92-107">COM+ solves this problem by providing the COM+ partitions feature.</span></span> <span data-ttu-id="07e92-108">您可以使用 COM + 分割，在電腦上安裝不同版本的 COM + 應用程式，並同時執行它們。</span><span class="sxs-lookup"><span data-stu-id="07e92-108">You can use COM+ partitions to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="07e92-109">若要瞭解並使用這項功能，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="07e92-109">To understand and use this feature, see the following topics:</span></span>

-   [<span data-ttu-id="07e92-110">什麼是 COM + 磁碟分割？</span><span class="sxs-lookup"><span data-stu-id="07e92-110">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
-   [<span data-ttu-id="07e92-111">分割區執行</span><span class="sxs-lookup"><span data-stu-id="07e92-111">Partition Implementation</span></span>](partition-implementation.md)
-   [<span data-ttu-id="07e92-112">在分割區中註冊和啟用元件</span><span class="sxs-lookup"><span data-stu-id="07e92-112">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
-   [<span data-ttu-id="07e92-113">COM + 佇列元件和分割區</span><span class="sxs-lookup"><span data-stu-id="07e92-113">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
-   [<span data-ttu-id="07e92-114">應用程式設計限制</span><span class="sxs-lookup"><span data-stu-id="07e92-114">Application Design Restrictions</span></span>](application-design-restrictions.md)

## <a name="related-topics"></a><span data-ttu-id="07e92-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="07e92-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07e92-116">COM + 分割工作</span><span class="sxs-lookup"><span data-stu-id="07e92-116">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)
</dt> </dl>

 

 



