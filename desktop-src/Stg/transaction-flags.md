---
title: 交易旗標
description: 物件可以在直接或交易模式中開啟。
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183674"
---
# <a name="transaction-flags"></a><span data-ttu-id="6bfb2-103">交易旗標</span><span class="sxs-lookup"><span data-stu-id="6bfb2-103">Transaction Flags</span></span>

<span data-ttu-id="6bfb2-104">物件可以在直接或交易模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="6bfb2-104">An object can be opened in either direct or transacted mode.</span></span> <span data-ttu-id="6bfb2-105">在直接模式中開啟物件時，會立即和永久變更變更。</span><span class="sxs-lookup"><span data-stu-id="6bfb2-105">When an object is opened in direct mode, changes are made immediately and permanently.</span></span> <span data-ttu-id="6bfb2-106">當物件在交易模式中開啟時，會緩衝處理變更，以便在完成編輯之後，可以明確地認可或還原變更。</span><span class="sxs-lookup"><span data-stu-id="6bfb2-106">When an object is opened in transacted mode, changes are buffered so they can be explicitly committed or reverted once editing is complete.</span></span> <span data-ttu-id="6bfb2-107">已認可的變更會儲存到物件，而還原的變更會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="6bfb2-107">Committed changes are saved to the object while reverted changes are discarded.</span></span> <span data-ttu-id="6bfb2-108">Direct 模式是預設的存取模式。</span><span class="sxs-lookup"><span data-stu-id="6bfb2-108">Direct mode is the default access mode.</span></span>

<span data-ttu-id="6bfb2-109">在父代儲存物件上不需要交易模式，就能將它用於嵌套元素上。</span><span class="sxs-lookup"><span data-stu-id="6bfb2-109">Transacted mode is not required on a parent storage object in order to use it on a nested element.</span></span> <span data-ttu-id="6bfb2-110">不過，嵌套專案的交易會在其父儲存物件的交易內進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="6bfb2-110">A transaction for a nested element, however, is nested within the transaction for its parent storage object.</span></span> <span data-ttu-id="6bfb2-111">因此，在對父物件所做的變更認可之前，無法認可對子物件所做的變更，而且在最上層父)  (的根儲存物件實際寫入磁片之前，都會維持未認可狀態。</span><span class="sxs-lookup"><span data-stu-id="6bfb2-111">Therefore, changes made to a child object cannot be committed until those made to the parent are committed, and both remain uncommitted until the root storage object (the top-level parent) is actually written to disk.</span></span> <span data-ttu-id="6bfb2-112">換句話說，變更會往外移動：內建物件會將變更發佈至其直屬容器的交易。</span><span class="sxs-lookup"><span data-stu-id="6bfb2-112">In other words, the changes move outward: inner objects publish changes to the transactions of their immediate containers.</span></span>

 

 




