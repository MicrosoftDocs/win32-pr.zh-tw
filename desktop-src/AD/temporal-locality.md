---
title: 時態性位置
description: 時態性位置是減少部分更新視窗的規避策略。
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462004"
---
# <a name="temporal-locality"></a><span data-ttu-id="21f92-103">時態性位置</span><span class="sxs-lookup"><span data-stu-id="21f92-103">Temporal Locality</span></span>

<span data-ttu-id="21f92-104">*時態性位置* 是減少部分更新視窗的規避策略。</span><span class="sxs-lookup"><span data-stu-id="21f92-104">*Temporal locality* is an avoidance strategy that reduces the window for partial updates.</span></span> <span data-ttu-id="21f92-105">從指定來源複本進行的變更複寫會以遞增的 USN 順序進行。</span><span class="sxs-lookup"><span data-stu-id="21f92-105">Replication of changes from a given source replica proceeds in ascending USN order.</span></span> <span data-ttu-id="21f92-106">在一段時間內立即關閉的寫入將會有 Usn （彼此接近），並會在一段時間內緊密地傳播。</span><span class="sxs-lookup"><span data-stu-id="21f92-106">Writes that occur close together in time will have USNs that are "near" each other, and will be propagated close together in time.</span></span> <span data-ttu-id="21f92-107">建立或更新多個相關物件的應用程式，應該盡可能將物件盡可能保持在一起。</span><span class="sxs-lookup"><span data-stu-id="21f92-107">Applications that create or update multiple, related objects should write the objects as close together in time as possible.</span></span> <span data-ttu-id="21f92-108">例如，應用程式可以從使用者收集所有必要的輸入，並在使用者按一下 [套用] 按鈕時將它套用至目錄。</span><span class="sxs-lookup"><span data-stu-id="21f92-108">For example, the application could gather all necessary input from the user and apply it to the directory when the user clicks an "Apply" button.</span></span>

<span data-ttu-id="21f92-109">時態性位置也可減少因物件不一致而導致衝突解決問題的機率。</span><span class="sxs-lookup"><span data-stu-id="21f92-109">Temporal locality also reduces the odds of collision resolution introducing intra-object inconsistencies.</span></span>

 

 




