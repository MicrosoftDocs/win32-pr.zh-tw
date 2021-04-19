---
description: 在使用預設佇列回呼常式之前，您可以在認可檔案佇列時將它指定為回呼常式，或是從自訂回呼常式呼叫它，就必須將它初始化。
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: 初始化和終止回呼內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cb4c144cb9069d395ccd688e2a172680df8a12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994414"
---
# <a name="initializing-and-terminating-the-callback-context"></a><span data-ttu-id="82feb-103">初始化和終止回呼內容</span><span class="sxs-lookup"><span data-stu-id="82feb-103">Initializing and Terminating the Callback Context</span></span>

<span data-ttu-id="82feb-104">在使用預設佇列回呼常式之前，您可以在認可檔案佇列時將它指定為回呼常式，或是從自訂回呼常式呼叫它，就必須將它初始化。</span><span class="sxs-lookup"><span data-stu-id="82feb-104">Before the default queue callback routine can be used, either by specifying it as the callback routine when committing a file queue, or by calling it from a custom callback routine, it must be initialized.</span></span>

<span data-ttu-id="82feb-105">[**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)函式會建立預設佇列回呼常式所使用的內容結構。</span><span class="sxs-lookup"><span data-stu-id="82feb-105">The [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) function builds the context structure that is used by the default queue callback routine.</span></span> <span data-ttu-id="82feb-106">它會傳回該結構的 void 指標。</span><span class="sxs-lookup"><span data-stu-id="82feb-106">It returns a void pointer to that structure.</span></span> <span data-ttu-id="82feb-107">此結構對於預設回呼常式的作業而言是不可或缺的，必須傳遞至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="82feb-107">This structure is essential for the default callback routine's operation and must be passed to the callback routine.</span></span> <span data-ttu-id="82feb-108">您可以藉由指定 void 指標做為 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)呼叫中的內容，或在從自訂回呼常式呼叫 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) 時，指定 void 指標做為內容參數。</span><span class="sxs-lookup"><span data-stu-id="82feb-108">You do can this either by specifying the void pointer as the context in a call to [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), or by specifying the void pointer as the context parameter when calling [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) from a custom callback routine.</span></span> <span data-ttu-id="82feb-109">安裝應用程式不得變更或參考此內容結構。</span><span class="sxs-lookup"><span data-stu-id="82feb-109">This context structure must not be altered or referenced by the setup application.</span></span>

<span data-ttu-id="82feb-110">[**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)函式也會初始化預設佇列回呼常式的內容，但它會指定第二個視窗，以便每次佇列傳送通知時，接收呼叫端指定的進度訊息。</span><span class="sxs-lookup"><span data-stu-id="82feb-110">The [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) function also initializes a context for the default queue callback routine, but it specifies a second window to receive a caller-specified progress message each time the queue sends a notification.</span></span> <span data-ttu-id="82feb-111">這可讓您使用預設的 [提示] 和 [錯誤] 對話方塊，也可以在第二個視窗中內嵌進度列（例如，在安裝精靈的頁面中）。</span><span class="sxs-lookup"><span data-stu-id="82feb-111">This enables you to use the default disk prompting and error dialog boxes, and to also embed a progress bar in a second window, for example, in a page of an installation wizard.</span></span>

<span data-ttu-id="82feb-112">無論您是否使用 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)初始化預設佇列回呼常式所使用的內容，在佇列作業完成處理之後，請呼叫 [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) 來釋放在初始化內容結構時所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="82feb-112">Regardless of whether you initialized the context used by the default queue callback routine with [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex), after the queued operations have finished processing, call [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) to release the resources allocated in initializing the context structure.</span></span>

 

 



