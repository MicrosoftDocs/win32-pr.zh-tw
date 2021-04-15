---
title: RPC 安全性基本知識
description: 若要完成任何遠端程序呼叫，所有分散式應用程式都必須在用戶端與伺服器之間建立系結。
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840651"
---
# <a name="rpc-security-essentials"></a><span data-ttu-id="43c01-103">RPC 安全性基本知識</span><span class="sxs-lookup"><span data-stu-id="43c01-103">RPC Security Essentials</span></span>

<span data-ttu-id="43c01-104">若要完成任何遠端程序呼叫，所有分散式應用程式都必須在用戶端與伺服器之間建立系結。</span><span class="sxs-lookup"><span data-stu-id="43c01-104">To complete any remote procedure call, all distributed applications must create a binding between the client and the server.</span></span> <span data-ttu-id="43c01-105">如需系結的詳細資訊，請參閱系結 [和控制碼](binding-and-handles.md)。</span><span class="sxs-lookup"><span data-stu-id="43c01-105">For more information on bindings, see [Binding and Handles](binding-and-handles.md).</span></span> <span data-ttu-id="43c01-106">若要完成安全的遠端程序呼叫，需要額外的步驟。</span><span class="sxs-lookup"><span data-stu-id="43c01-106">To complete a secure remote procedure call, additional steps are necessary.</span></span> <span data-ttu-id="43c01-107">首先，伺服器必須在 DCE 術語) 中選擇安全性提供者 (authentication 服務。</span><span class="sxs-lookup"><span data-stu-id="43c01-107">First, the server must choose a security provider (authentication service in DCE terminology).</span></span> <span data-ttu-id="43c01-108">然後，它必須決定其驗證機制。</span><span class="sxs-lookup"><span data-stu-id="43c01-108">Then it must decide on its authentication mechanism.</span></span> <span data-ttu-id="43c01-109">之後，用戶端會取得伺服器的系結，並從 RPC 執行時間要求安全的遠端程序呼叫，並指定各種安全性選項，例如安全性提供者、安全性 QOS 選項等等。</span><span class="sxs-lookup"><span data-stu-id="43c01-109">After that, the client obtains a binding to the server, and requests a secure remote procedure call from the RPC run time, and specifies various security options, such as security provider, security QOS options, and so on.</span></span>

<span data-ttu-id="43c01-110">本節說明使用 RPC 函數為已驗證的分散式應用程式建立用戶端和伺服器時所需的基本概念和資訊。</span><span class="sxs-lookup"><span data-stu-id="43c01-110">This section explains the essential concepts and information required to use the RPC functions to create a client and server for an authenticated distributed application.</span></span> <span data-ttu-id="43c01-111">它會組織成下列主題：</span><span class="sxs-lookup"><span data-stu-id="43c01-111">It is organized into the following topics:</span></span>

-   [<span data-ttu-id="43c01-112">主體名稱</span><span class="sxs-lookup"><span data-stu-id="43c01-112">Principal Names</span></span>](principal-names.md)
-   [<span data-ttu-id="43c01-113">驗證層級</span><span class="sxs-lookup"><span data-stu-id="43c01-113">Authentication Levels</span></span>](authentication-levels.md)
-   [<span data-ttu-id="43c01-114">驗證服務</span><span class="sxs-lookup"><span data-stu-id="43c01-114">Authentication Services</span></span>](authentication-services.md)
-   [<span data-ttu-id="43c01-115">用戶端驗證認證</span><span class="sxs-lookup"><span data-stu-id="43c01-115">Client Authentication Credentials</span></span>](client-authentication-credentials.md)
-   [<span data-ttu-id="43c01-116">授權服務</span><span class="sxs-lookup"><span data-stu-id="43c01-116">Authorization Services</span></span>](authorization-services.md)
-   [<span data-ttu-id="43c01-117">服務品質</span><span class="sxs-lookup"><span data-stu-id="43c01-117">Quality of Service</span></span>](quality-of-service.md)
-   [<span data-ttu-id="43c01-118">授權函數</span><span class="sxs-lookup"><span data-stu-id="43c01-118">Authorization Functions</span></span>](authorization-functions.md)
-   [<span data-ttu-id="43c01-119">金鑰取得函式</span><span class="sxs-lookup"><span data-stu-id="43c01-119">Key Acquisition Functions</span></span>](key-acquisition-functions.md)
-   [<span data-ttu-id="43c01-120">用戶端模擬</span><span class="sxs-lookup"><span data-stu-id="43c01-120">Client Impersonation</span></span>](client-impersonation.md)

 

 




