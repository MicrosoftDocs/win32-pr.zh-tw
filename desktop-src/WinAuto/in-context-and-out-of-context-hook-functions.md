---
title: In-Context 和跨內容攔截函式
description: 使用 SetWinEventHook 註冊攔截函式時，用戶端會指定攔截函式是否在內容中或超出內容。 這些條款描述與伺服器位址空間相關之攔截函式的記憶體位置。
ms.assetid: 6876d74a-9c15-4f89-92ad-d072d9b528f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d96bff36f47b5e7fb0ad2e98d5a5347e2bc747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183877"
---
# <a name="in-context-and-out-of-context-hook-functions"></a><span data-ttu-id="80bcf-104">In-Context 和跨內容攔截函式</span><span class="sxs-lookup"><span data-stu-id="80bcf-104">In-Context and Out-of-Context Hook Functions</span></span>

<span data-ttu-id="80bcf-105">使用 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)註冊攔截函式時，用戶端會指定攔截函 *式是否在內容中* 或 *超出內容*。</span><span class="sxs-lookup"><span data-stu-id="80bcf-105">When registering a hook function with [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook), clients specify whether the hook function is *in-context* or *out-of-context*.</span></span> <span data-ttu-id="80bcf-106">這些條款描述與伺服器位址空間相關之攔截函式的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="80bcf-106">These terms describe the memory location of the hook function relative to the server's address space.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="80bcf-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="80bcf-107">In this section</span></span>

-   [<span data-ttu-id="80bcf-108">內容內部攔截函式</span><span class="sxs-lookup"><span data-stu-id="80bcf-108">In-Context Hook Functions</span></span>](in-context-hook-functions.md)
-   [<span data-ttu-id="80bcf-109">內容攔截函式預防措施</span><span class="sxs-lookup"><span data-stu-id="80bcf-109">In-Context Hook Function Precautions</span></span>](in-context-hook-function-precautions.md)
-   [<span data-ttu-id="80bcf-110">內容外攔截函式</span><span class="sxs-lookup"><span data-stu-id="80bcf-110">Out-of-Context Hook Functions</span></span>](out-of-context-hook-functions.md)

 

 




