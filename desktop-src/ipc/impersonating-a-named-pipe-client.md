---
description: 模擬是執行緒在安全性內容中執行的能力，與擁有線程的進程不同。
ms.assetid: 1bde4d4d-958e-45f4-8cdb-0572adcaa3ac
title: 模擬具名管道用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586de99ae24ba9bab8b65ba4cb1a3a91922aa9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971162"
---
# <a name="impersonating-a-named-pipe-client"></a><span data-ttu-id="2f8c6-103">模擬具名管道用戶端</span><span class="sxs-lookup"><span data-stu-id="2f8c6-103">Impersonating a Named Pipe Client</span></span>

<span data-ttu-id="2f8c6-104">模擬 *是執行緒* 在安全性內容中執行的能力，與擁有線程的進程不同。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-104">*Impersonation* is the ability of a thread to execute in a security context different from that of the process that owns the thread.</span></span> <span data-ttu-id="2f8c6-105">模擬可讓伺服器執行緒代表用戶端執行動作，但在用戶端的安全性內容限制內。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-105">Impersonation enables the server thread to perform actions on behalf of the client, but within the limits of the client's security context.</span></span> <span data-ttu-id="2f8c6-106">用戶端通常會有較低層級的存取權限。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-106">The client typically has some lesser level of access rights.</span></span> <span data-ttu-id="2f8c6-107">如需詳細資訊， [請參閱模擬](/windows/desktop/SecAuthZ/client-impersonation)。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-107">For more information, see [Impersonation](/windows/desktop/SecAuthZ/client-impersonation).</span></span>

<span data-ttu-id="2f8c6-108">具名管道伺服器執行緒可以呼叫 [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) 函式，以為連接到管道用戶端的使用者存取權杖。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-108">A named pipe server thread can call the [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) function to assume the access token of the user connected to the client end of the pipe.</span></span> <span data-ttu-id="2f8c6-109">例如，具名管道伺服器可以提供資料庫或檔案系統的存取權，讓管道伺服器具有特殊許可權的存取權。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-109">For example, a named pipe server can provide access to a database or file system to which the pipe server has privileged access.</span></span> <span data-ttu-id="2f8c6-110">當管道用戶端將要求傳送到伺服器時，伺服器會模擬用戶端，並嘗試存取受保護的資料庫。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-110">When a pipe client sends a request to the server, the server impersonates the client and attempts to access the protected database.</span></span> <span data-ttu-id="2f8c6-111">系統接著會根據用戶端的安全性層級，授與或拒絕伺服器的存取權。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-111">The system then grants or denies the server's access, based on the security level of the client.</span></span> <span data-ttu-id="2f8c6-112">當伺服器完成時，它會使用 [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) 函數來還原其原始安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-112">When the server is finished, it uses the [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) function to restore its original security token.</span></span>

<span data-ttu-id="2f8c6-113">模擬 [層級](/windows/desktop/SecAuthZ/impersonation-levels) 會決定伺服器在模擬用戶端時可執行檔作業。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-113">The [impersonation level](/windows/desktop/SecAuthZ/impersonation-levels) determines the operations the server can perform while impersonating the client.</span></span> <span data-ttu-id="2f8c6-114">根據預設，伺服器會在 SecurityImpersonation 模擬層級進行模擬。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-114">By default, a server impersonates at the SecurityImpersonation impersonation level.</span></span> <span data-ttu-id="2f8c6-115">但是，當用戶端呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟管道用戶端的控制碼時，用戶端可以使用安全性 \_ SQOS 目前的旗標 \_ 來控制伺服器的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="2f8c6-115">However, when the client calls the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to the client end of the pipe, the client can use the SECURITY\_SQOS\_PRESENT flag to control the server's impersonation level.</span></span>

 

 
