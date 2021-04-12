---
description: Authz API 可讓應用程式使用較低層級的存取控制，以更佳的效能和更簡化的開發執行可自訂的存取檢查。
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: 使用 Authz API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320859"
---
# <a name="using-authz-api"></a><span data-ttu-id="2eee6-103">使用 Authz API</span><span class="sxs-lookup"><span data-stu-id="2eee6-103">Using Authz API</span></span>

<span data-ttu-id="2eee6-104">Authz API 可讓應用程式使用 [較低層級的存取控制](low-level-access-control.md)，以更佳的效能和更簡化的開發執行可自訂的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="2eee6-104">Authz API allows applications to perform customizable access checks with better performance and more simplified development than [Low-level Access Control](low-level-access-control.md).</span></span>

<span data-ttu-id="2eee6-105">Authz API 可讓應用程式快取存取檢查以改善效能、查詢和修改用戶端內容，以及定義可用來動態評估存取權限的商務規則。</span><span class="sxs-lookup"><span data-stu-id="2eee6-105">Authz API allows applications to cache access checks for improved performance, to query and modify client contexts, and to define business rules that can be used to evaluate access permission dynamically.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2eee6-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="2eee6-106">In This Section</span></span>



| <span data-ttu-id="2eee6-107">主題</span><span class="sxs-lookup"><span data-stu-id="2eee6-107">Topic</span></span>                                                                             | <span data-ttu-id="2eee6-108">描述</span><span class="sxs-lookup"><span data-stu-id="2eee6-108">Description</span></span>                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2eee6-109">初始化用戶端內容</span><span class="sxs-lookup"><span data-stu-id="2eee6-109">Initializing a Client Context</span></span>](initializing-a-client-context.md)<br/>     | <span data-ttu-id="2eee6-110">應用程式必須先建立用戶端內容，才能使用 Authz API 來執行存取檢查或審核。</span><span class="sxs-lookup"><span data-stu-id="2eee6-110">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="2eee6-111">查詢用戶端內容</span><span class="sxs-lookup"><span data-stu-id="2eee6-111">Querying a Client Context</span></span>](querying-a-client-context.md)<br/>             | <span data-ttu-id="2eee6-112">應用程式可以呼叫 [**AuthzGetInformationFromCoNtext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) 函數來查詢現有用戶端內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2eee6-112">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="2eee6-113">將 Sid 新增至用戶端內容</span><span class="sxs-lookup"><span data-stu-id="2eee6-113">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)<br/> | <span data-ttu-id="2eee6-114">應用程式可以藉由呼叫 [**AuthzAddSidsToCoNtext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)函式，將 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (sid) 新增至現有的用戶端內容。</span><span class="sxs-lookup"><span data-stu-id="2eee6-114">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span><br/> |
| [<span data-ttu-id="2eee6-115">使用 Authz API 檢查存取權</span><span class="sxs-lookup"><span data-stu-id="2eee6-115">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)<br/>   | <span data-ttu-id="2eee6-116">應用程式會藉由呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函式來判斷是否要授與安全物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="2eee6-116">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="2eee6-117">快取存取檢查</span><span class="sxs-lookup"><span data-stu-id="2eee6-117">Caching Access Checks</span></span>](caching-access-checks.md)<br/>                     | <span data-ttu-id="2eee6-118">當應用程式藉由呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函數來執行存取檢查時，可以快取該存取檢查的結果。</span><span class="sxs-lookup"><span data-stu-id="2eee6-118">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span><br/>                                                                                       |



 

 

