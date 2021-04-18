---
description: 您必須先開啟檔案佇列，才能將檔案作業排在佇列中。 呼叫 SetupOpenFileQueue 函數會傳回佇列檔案的控制碼。 後續的佇列函式會使用此控制碼來參考開啟的佇列，並對其新增作業或掃描它。
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: 開啟和關閉佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978260"
---
# <a name="opening-and-closing-a-queue"></a><span data-ttu-id="dc1f9-105">開啟和關閉佇列</span><span class="sxs-lookup"><span data-stu-id="dc1f9-105">Opening and Closing a Queue</span></span>

<span data-ttu-id="dc1f9-106">您必須先開啟檔案佇列，才能將檔案作業排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="dc1f9-106">Before you can queue file operations, you must open a file queue.</span></span> <span data-ttu-id="dc1f9-107">呼叫 [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) 函數會傳回佇列檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dc1f9-107">Calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function returns a handle to a queue file.</span></span> <span data-ttu-id="dc1f9-108">後續的佇列函式會使用此控制碼來參考開啟的佇列，並對其新增作業或掃描它。</span><span class="sxs-lookup"><span data-stu-id="dc1f9-108">This handle is used by subsequent queue functions to reference the open queue and add operations to it or scan it.</span></span>

<span data-ttu-id="dc1f9-109">所有指定的檔案作業都已排入佇列並認可之後，您必須呼叫 [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) 函式來釋放在呼叫 [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)時所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="dc1f9-109">After all the specified file operations have been queued and committed, you must call the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function to release resources allocated during the call to [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span>

> [!Note]  
> <span data-ttu-id="dc1f9-110">[**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)函數不會認可檔案佇列。</span><span class="sxs-lookup"><span data-stu-id="dc1f9-110">The [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function does not commit the file queue.</span></span> <span data-ttu-id="dc1f9-111">呼叫 **SetupCloseFileQueue** 時未認可的任何作業都不會執行。</span><span class="sxs-lookup"><span data-stu-id="dc1f9-111">Any operations that are uncommitted when **SetupCloseFileQueue** is called will not be performed.</span></span>

 

 

 



