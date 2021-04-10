---
title: 模擬
description: 模擬是指執行緒在安全性內容中執行的能力，與擁有線程的進程內容不同。
ms.assetid: b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735fa12e175ecec5dc2a7ed741843d713532e19
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024169"
---
# <a name="impersonation"></a><span data-ttu-id="7ff84-103">模擬</span><span class="sxs-lookup"><span data-stu-id="7ff84-103">Impersonation</span></span>

<span data-ttu-id="7ff84-104">模擬是指執行緒在安全性內容中執行的能力，與擁有線程的進程內容不同。</span><span class="sxs-lookup"><span data-stu-id="7ff84-104">Impersonation is the ability of a thread to execute in a security context that is different from the context of the process that owns the thread.</span></span> <span data-ttu-id="7ff84-105">在用戶端的安全性內容中執行時，伺服器「是」用戶端的程度。</span><span class="sxs-lookup"><span data-stu-id="7ff84-105">When running in the client's security context, the server "is" the client, to some degree.</span></span> <span data-ttu-id="7ff84-106">伺服器執行緒會使用代表用戶端認證的存取權杖，來取得用戶端可存取之物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="7ff84-106">The server thread uses an access token representing the client's credentials to obtain access to the objects to which the client has access.</span></span>

<span data-ttu-id="7ff84-107">模擬的主要原因是要針對用戶端的身分識別來執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="7ff84-107">The primary reason for impersonation is to cause access checks to be performed against the client's identity.</span></span> <span data-ttu-id="7ff84-108">使用用戶端的身分識別來進行存取檢查，可能會因為用戶端有許可權的不同，而導致存取受限或展開。</span><span class="sxs-lookup"><span data-stu-id="7ff84-108">Using the client's identity for access checks can cause access to be either restricted or expanded, depending on what the client has permission to do.</span></span> <span data-ttu-id="7ff84-109">例如，假設檔案伺服器的檔案包含機密資訊，而且每個檔案都受到 ACL 的保護。</span><span class="sxs-lookup"><span data-stu-id="7ff84-109">For example, suppose a file server has files containing confidential information and that each of these files is protected by an ACL.</span></span> <span data-ttu-id="7ff84-110">為了協助防止用戶端取得這些檔案中資訊的未經授權存取，伺服器可以在存取檔案之前模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="7ff84-110">To help prevent a client from obtaining unauthorized access to information in these files, the server can impersonate the client before accessing the files.</span></span>

## <a name="access-tokens-for-impersonation"></a><span data-ttu-id="7ff84-111">存取模擬的權杖</span><span class="sxs-lookup"><span data-stu-id="7ff84-111">Access Tokens for Impersonation</span></span>

<span data-ttu-id="7ff84-112">存取權杖是描述進程或執行緒之安全性內容的物件。</span><span class="sxs-lookup"><span data-stu-id="7ff84-112">Access tokens are objects that describe the security context of a process or thread.</span></span> <span data-ttu-id="7ff84-113">它們提供的資訊包括使用者帳戶的身分識別，以及使用者帳戶可用的許可權子集。</span><span class="sxs-lookup"><span data-stu-id="7ff84-113">They provide information that includes the identity of a user account and a subset of the privileges available to the user account.</span></span> <span data-ttu-id="7ff84-114">每個進程都有 *主要存取權杖* ，可描述與進程相關聯之使用者帳戶的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="7ff84-114">Every process has a *primary access token* that describes the security context of the user account associated with the process.</span></span> <span data-ttu-id="7ff84-115">根據預設，當進程的執行緒與安全物件互動時，系統會使用主要權杖。</span><span class="sxs-lookup"><span data-stu-id="7ff84-115">By default, the system uses the primary token when a thread of the process interacts with a securable object.</span></span> <span data-ttu-id="7ff84-116">但是，當執行緒模擬用戶端時，模擬執行緒同時具有主要存取權杖和模擬 *權杖*。</span><span class="sxs-lookup"><span data-stu-id="7ff84-116">However, when a thread impersonates a client, the impersonating thread has both a primary access token and an *impersonation token*.</span></span> <span data-ttu-id="7ff84-117">模擬權杖代表用戶端的安全性內容，而此存取權杖是在模擬期間用於存取檢查的權杖。</span><span class="sxs-lookup"><span data-stu-id="7ff84-117">The impersonation token represents the client's security context, and this access token is the one that is used for access checks during impersonation.</span></span> <span data-ttu-id="7ff84-118">當模擬結束時，執行緒會還原為只使用主要存取權杖。</span><span class="sxs-lookup"><span data-stu-id="7ff84-118">When impersonation is over, the thread reverts to using only the primary access token.</span></span>

<span data-ttu-id="7ff84-119">您可以使用 [**OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) 函式來取得處理常式主要權杖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7ff84-119">You can use the [**OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) function to get a handle to the primary token of a process.</span></span> <span data-ttu-id="7ff84-120">您可以使用 [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函式來取得執行緒模擬權杖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7ff84-120">Use the [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function to get a handle to the impersonation token of a thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ff84-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="7ff84-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ff84-122">存取權杖</span><span class="sxs-lookup"><span data-stu-id="7ff84-122">Access Tokens</span></span>](/windows/desktop/SecAuthZ/access-tokens)
</dt> <dt>

[<span data-ttu-id="7ff84-123">委派和模擬</span><span class="sxs-lookup"><span data-stu-id="7ff84-123">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> </dl>

 

 