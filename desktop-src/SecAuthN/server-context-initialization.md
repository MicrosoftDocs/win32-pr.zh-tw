---
description: 和用戶端一樣，伺服器也會取得認證控制碼，以準備回應來自用戶端的傳入驗證要求。
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: 伺服器內容初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1362c8fd71e079392f10a8e35f76ad511de3c49f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692919"
---
# <a name="server-context-initialization"></a><span data-ttu-id="6079b-103">伺服器內容初始化</span><span class="sxs-lookup"><span data-stu-id="6079b-103">Server Context Initialization</span></span>

<span data-ttu-id="6079b-104">和用戶端一樣，伺服器也會取得 [*認證*](../secgloss/c-gly.md) 控制碼，以準備回應來自用戶端的傳入驗證要求。</span><span class="sxs-lookup"><span data-stu-id="6079b-104">Like the client, the server also acquires a [*credentials*](../secgloss/c-gly.md) handle to be ready to respond to an incoming authentication request from the client.</span></span> <span data-ttu-id="6079b-105">伺服器認證是用來在支援伺服器驗證或相互驗證的 [*安全性通訊協定*](../secgloss/s-gly.md) 中，對用戶端驗證服務器。</span><span class="sxs-lookup"><span data-stu-id="6079b-105">Server credentials are used to authenticate the server to the client in [*security protocols*](../secgloss/s-gly.md) that support server authentication or mutual authentication.</span></span> <span data-ttu-id="6079b-106">伺服器會取得用來啟動伺服器之服務帳戶所定義的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="6079b-106">The server obtains a handle to its credentials defined by the service account used to start the server.</span></span> <span data-ttu-id="6079b-107">它會藉由呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="6079b-107">It does so by calling [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span></span>

<span data-ttu-id="6079b-108">伺服器可以取得其認證控制碼，然後進入「接聽」狀態，也可以在連線要求抵達之前等候接聽狀態，然後取得輸入認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="6079b-108">The server can acquire its credentials handle and then go into a listen state, or it can wait in a listen state until a connection request arrives and then acquire an inbound credentials handle.</span></span> <span data-ttu-id="6079b-109">如需認證功能的詳細資訊，請參閱 [認證管理](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="6079b-109">For more information on credentials functions, see [Credential Management](authentication-functions.md).</span></span>

<span data-ttu-id="6079b-110">當伺服器收到來自用戶端的連線要求訊息時，它會使用 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)來建立用戶端的本機 [*安全性內容*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6079b-110">When the server receives a connection request message from a client, it creates a local [*security context*](../secgloss/s-gly.md) for the client using [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span> <span data-ttu-id="6079b-111">伺服器會使用這個本機安全性內容來執行相同用戶端的未來要求。</span><span class="sxs-lookup"><span data-stu-id="6079b-111">The server uses this local security context to carry out future requests by the same client.</span></span> <span data-ttu-id="6079b-112">如需內容函數的詳細資訊，請參閱 [內容管理](authentication-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="6079b-112">For more information on context functions, see [Context Management](authentication-functions.md).</span></span>

<span data-ttu-id="6079b-113">伺服器會檢查傳回狀態和輸出緩衝區描述項，以確定目前沒有任何錯誤，而且如果發生錯誤，就會拒絕連接要求。</span><span class="sxs-lookup"><span data-stu-id="6079b-113">The server checks the return status and output buffer descriptor to ensure there are no errors so far, and can reject the connection request if there are errors.</span></span> <span data-ttu-id="6079b-114">如果 AcceptSecurityCoNtext 所傳回的輸出緩衝區中有資訊 [**(一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)，它會將該緩衝區組合至用戶端的回應訊息。</span><span class="sxs-lookup"><span data-stu-id="6079b-114">If there is information in the output buffer returned by [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), it bundles that buffer into a response message to the client.</span></span>

<span data-ttu-id="6079b-115">[**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)的任何輸出緩衝區都必須傳送回用戶端。</span><span class="sxs-lookup"><span data-stu-id="6079b-115">Any output buffer from [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) must be sent back to the client.</span></span> <span data-ttu-id="6079b-116">此外，如果傳回狀態需要通訊協定才能繼續 (需要繼續進行 \_ \_ \_ ，或每秒 \_ \_ 完成 \_ 並 \_ 繼續) ，則需要另一個與用戶端交換的訊息。</span><span class="sxs-lookup"><span data-stu-id="6079b-116">In addition, if the return status requires the protocol to continue (SEC\_I\_CONTINUE\_NEEDED or SEC\_I\_COMPLETE\_AND\_CONTINUE), another message exchange with the client is required.</span></span>

<span data-ttu-id="6079b-117">針對額外的腿，伺服器會等候用戶端以其他訊息回應。</span><span class="sxs-lookup"><span data-stu-id="6079b-117">For additional legs, the server waits for the client to respond with another message.</span></span> <span data-ttu-id="6079b-118">這項等候的時間可能會讓用戶端刻意沒有回應，而導致伺服器執行緒，以及不久的所有伺服器執行緒停止回應。</span><span class="sxs-lookup"><span data-stu-id="6079b-118">This wait can be timed out so as to avoid a denial of service attack where a client purposely never responds, causing a server thread and soon, all server threads, to stop responding.</span></span>

 

 
