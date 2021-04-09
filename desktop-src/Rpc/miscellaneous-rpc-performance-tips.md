---
title: 其他 RPC 效能秘訣
description: 本節討論開發高效能 RPC 伺服器的其他效能秘訣。 本節提供許多參考 RPC 用戶端的秘訣。 正確開發 RPC 用戶端可讓 RPC 伺服器執行較少的工作。
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021081"
---
# <a name="miscellaneous-rpc-performance-tips"></a><span data-ttu-id="02896-105">其他 RPC 效能秘訣</span><span class="sxs-lookup"><span data-stu-id="02896-105">Miscellaneous RPC Performance Tips</span></span>

<span data-ttu-id="02896-106">本節討論開發高效能 RPC 伺服器的其他效能秘訣。</span><span class="sxs-lookup"><span data-stu-id="02896-106">This section discusses miscellaneous performance tips for developing high performance RPC servers.</span></span> <span data-ttu-id="02896-107">本節提供許多參考 RPC 用戶端的秘訣。</span><span class="sxs-lookup"><span data-stu-id="02896-107">This section provides many tips that refer to the RPC client.</span></span> <span data-ttu-id="02896-108">正確開發 RPC 用戶端可讓 RPC 伺服器執行較少的工作。</span><span class="sxs-lookup"><span data-stu-id="02896-108">Developing an RPC client properly enables the RPC server to perform less work.</span></span>

## <a name="use-kerberos"></a><span data-ttu-id="02896-109">使用 Kerberos</span><span class="sxs-lookup"><span data-stu-id="02896-109">Use Kerberos</span></span>

<span data-ttu-id="02896-110">如果使用安全性，請使用 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="02896-110">If security is used, use Kerberos.</span></span> <span data-ttu-id="02896-111">在伺服器端，Kerberos 不需要存取 KDC。</span><span class="sxs-lookup"><span data-stu-id="02896-111">On the server side, Kerberos does not require access to the KDC.</span></span> <span data-ttu-id="02896-112">這會將工作負載從伺服器移至用戶端，以提供更佳的執行伺服器。</span><span class="sxs-lookup"><span data-stu-id="02896-112">This moves the workload from the server to the client, which provides better performing servers.</span></span>

## <a name="use-static-identity-tracking"></a><span data-ttu-id="02896-113">使用靜態身分識別追蹤</span><span class="sxs-lookup"><span data-stu-id="02896-113">Use Static Identity Tracking</span></span>

<span data-ttu-id="02896-114">如果使用安全性，請嘗試使用靜態身分識別追蹤。</span><span class="sxs-lookup"><span data-stu-id="02896-114">If security is used, try to use static identity tracking.</span></span> <span data-ttu-id="02896-115">靜態身分識別追蹤在資源使用方面比動態身分識別追蹤更便宜。</span><span class="sxs-lookup"><span data-stu-id="02896-115">Static identity tracking is cheaper in terms of resource usage than dynamic identity tracking.</span></span> <span data-ttu-id="02896-116">如果用戶端身分識別變更，而且伺服器不應留意變更，請使用動態追蹤，而不是為每個身分識別建立不同的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="02896-116">If the client identity changes, and the server should not be aware of the change, use dynamic tracking instead of creating a different binding handle for each identity.</span></span> <span data-ttu-id="02896-117">但是，如果身分識別是一樣的，請確定 RPC 知道這一點，以避免 RPC 每次都會檢查變更的身分識別。</span><span class="sxs-lookup"><span data-stu-id="02896-117">But if the identity is the same, ensure RPC is aware of that fact to avoid having RPC make checks for changed identity every time.</span></span>

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a><span data-ttu-id="02896-118">使用 RpcGetAuthorizationCoNtextForClient 函式</span><span class="sxs-lookup"><span data-stu-id="02896-118">Use the RpcGetAuthorizationContextForClient Function</span></span>

<span data-ttu-id="02896-119">如果您需要在 Windows XP 中檢查存取權，請使用 [**RpcGetAuthorizationCoNtextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) 函數。</span><span class="sxs-lookup"><span data-stu-id="02896-119">If you need to check access in Windows XP, use the [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) function.</span></span> <span data-ttu-id="02896-120">產生的 Authz 內容可提供非常快速的存取檢查，可透過 RPC 執行時間有效率地快取。</span><span class="sxs-lookup"><span data-stu-id="02896-120">The resulting Authz contexts enables very fast access checks, which are efficiently cached by the RPC run time.</span></span>

## <a name="do-not-modify-the-token-unless-necessary"></a><span data-ttu-id="02896-121">除非必要，否則請勿修改權杖</span><span class="sxs-lookup"><span data-stu-id="02896-121">Do Not Modify the Token Unless Necessary</span></span>

<span data-ttu-id="02896-122">如果使用動態身分識別追蹤，除非絕對必要，否則請勿修改執行緒/進程 token。</span><span class="sxs-lookup"><span data-stu-id="02896-122">If dynamic identity tracking is used, do not modify the thread/process token unless absolutely necessary.</span></span> <span data-ttu-id="02896-123">即使已修改為先前擁有的設定，權杖通常與安全性系統有足夠的差異，以觸發新的安全性內容建立。</span><span class="sxs-lookup"><span data-stu-id="02896-123">Even if it is modified to settings it previously had, the token often is sufficiently different to the security system to trigger the establishment of a new security context.</span></span>

## <a name="consider-mixed-mode-serialization-for-context-handles"></a><span data-ttu-id="02896-124">針對內容控制碼考慮混合模式序列化</span><span class="sxs-lookup"><span data-stu-id="02896-124">Consider Mixed Mode Serialization for Context Handles</span></span>

<span data-ttu-id="02896-125">內容控制碼的預設序列化模式會序列化 (獨佔) 。</span><span class="sxs-lookup"><span data-stu-id="02896-125">The default serialization mode for context handle is serialized (exclusive).</span></span> <span data-ttu-id="02896-126">請考慮進行所有不修改共用序列化模式中內容控制碼狀態的呼叫。</span><span class="sxs-lookup"><span data-stu-id="02896-126">Consider making all calls that do not modify the state of the context handle in shared serialization mode.</span></span> <span data-ttu-id="02896-127">如需詳細資訊，請參閱 [**RpcSsCoNtextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) 。</span><span class="sxs-lookup"><span data-stu-id="02896-127">See [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) for more information.</span></span>

 

 




