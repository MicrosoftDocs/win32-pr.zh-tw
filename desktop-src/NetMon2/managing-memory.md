---
description: 如果專家在執行時間失敗，如果您使用網路監視器函式進行記憶體管理，網路監視器將會釋放配置的記憶體。
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: 管理記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943517"
---
# <a name="managing-memory"></a><span data-ttu-id="51b76-103">管理記憶體</span><span class="sxs-lookup"><span data-stu-id="51b76-103">Managing Memory</span></span>

<span data-ttu-id="51b76-104">如果專家在執行時間失敗，如果您使用網路監視器函式進行記憶體管理，網路監視器將會釋放配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="51b76-104">Should an expert fail during run time, if you use Network Monitor functions for memory management, Network Monitor will free allocated memory.</span></span> <span data-ttu-id="51b76-105">但是，當您撰寫專家時，可能需要取得系統資源和資料結構資訊。</span><span class="sxs-lookup"><span data-stu-id="51b76-105">However, when you write an expert, it might be necessary to acquire system resources and data structure information.</span></span> <span data-ttu-id="51b76-106">例如，網路監視器通訊協定聯合專家會取得檔案控制代碼來建立新的捕獲。</span><span class="sxs-lookup"><span data-stu-id="51b76-106">For example, the Network Monitor Protocol Coalesce Expert acquires a file handle to build a new capture.</span></span> <span data-ttu-id="51b76-107">每個專家都必須建立自己的 **try/catch** 處理，讓專家可以釋出所取得的資源。</span><span class="sxs-lookup"><span data-stu-id="51b76-107">Each expert must build its own **try/catch** handling so that the expert can free resources it acquired.</span></span>

<span data-ttu-id="51b76-108">配置記憶體時，請使用下列現有的記憶體函數：</span><span class="sxs-lookup"><span data-stu-id="51b76-108">When memory is allocated, use the following existing memory functions:</span></span>

-   [<span data-ttu-id="51b76-109">**ExpertAllocMemory**</span><span class="sxs-lookup"><span data-stu-id="51b76-109">**ExpertAllocMemory**</span></span>](expertallocmemory.md)
-   [<span data-ttu-id="51b76-110">**ExpertReallocMemory**</span><span class="sxs-lookup"><span data-stu-id="51b76-110">**ExpertReallocMemory**</span></span>](expertreallocmemory.md)

 

 



