---
description: 您可以指定預設佇列回呼常式來處理 SetupCommitFileQueue 所傳送的通知，也可以由根據預設佇列回呼常式功能建立的自訂回呼常式來呼叫它。
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: 使用預設佇列回呼常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975086"
---
# <a name="using-the-default-queue-callback-routine"></a><span data-ttu-id="ed83f-103">使用預設佇列回呼常式</span><span class="sxs-lookup"><span data-stu-id="ed83f-103">Using the Default Queue Callback Routine</span></span>

<span data-ttu-id="ed83f-104">您可以指定預設佇列回呼常式來處理 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)所傳送的通知，也可以由根據預設佇列回呼常式功能建立的自訂回呼常式來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="ed83f-104">The default queue callback routine can be specified to handle notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), or it can be called by a custom callback routine that builds on the functionality of the default queue callback routine.</span></span>

<span data-ttu-id="ed83f-105">下列各節說明如何初始化和終止預設佇列回呼常式所使用的內容。</span><span class="sxs-lookup"><span data-stu-id="ed83f-105">The following sections explain how to initialize and terminate the context used by a default queue callback routine.</span></span> <span data-ttu-id="ed83f-106">這些章節也會說明如何搭配使用預設佇列回呼常式與 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 或自訂回呼常式。</span><span class="sxs-lookup"><span data-stu-id="ed83f-106">The sections also describe how to use the default queue callback routine with [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) or a custom callback routine.</span></span>

-   [<span data-ttu-id="ed83f-107">初始化和終止回呼內容</span><span class="sxs-lookup"><span data-stu-id="ed83f-107">Initializing and Terminating the Callback Context</span></span>](initializing-and-terminating-the-callback-context.md)
-   [<span data-ttu-id="ed83f-108">呼叫預設佇列回呼常式</span><span class="sxs-lookup"><span data-stu-id="ed83f-108">Calling the Default Queue Callback Routine</span></span>](calling-the-default-queue-callback-routine.md)

 

 



