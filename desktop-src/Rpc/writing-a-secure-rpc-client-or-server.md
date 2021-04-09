---
title: 撰寫安全的 RPC 用戶端或伺服器
description: 本節提供撰寫安全的 RPC 用戶端或伺服器的最佳作法建議。
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- 遠端程序呼叫 RPC、最佳作法、撰寫安全的用戶端或伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023839"
---
# <a name="writing-a-secure-rpc-client-or-server"></a><span data-ttu-id="e760e-104">撰寫安全的 RPC 用戶端或伺服器</span><span class="sxs-lookup"><span data-stu-id="e760e-104">Writing a Secure RPC Client or Server</span></span>

<span data-ttu-id="e760e-105">本節提供撰寫安全的 RPC 用戶端或伺服器的最佳作法建議。</span><span class="sxs-lookup"><span data-stu-id="e760e-105">This section provides best practice recommendations for writing a secure RPC client or server.</span></span>

<span data-ttu-id="e760e-106">本節中的資訊適用于 Windows 2000 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e760e-106">The information in this section applies to Windows 2000 and Windows XP.</span></span> <span data-ttu-id="e760e-107">本節適用于所有通訊協定序列，包括 [**ncalrpc**](/windows/desktop/Midl/ncalrpc)。</span><span class="sxs-lookup"><span data-stu-id="e760e-107">This section applies to all protocol sequences, including [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="e760e-108">開發人員傾向于將 **ncalrpc** 視為攻擊的可能目標，這在終端機伺服器上可能會有數百位使用者可存取服務，而危及或甚至關閉服務可能會導致取得額外的存取權。</span><span class="sxs-lookup"><span data-stu-id="e760e-108">Developers tend to think **ncalrpc** is not a probable target for an attack, which is not true on a terminal server where potentially hundreds of users have access to a service, and compromising or even bringing down a service can lead to acquiring extra access.</span></span>

<span data-ttu-id="e760e-109">本節分為下列主題：</span><span class="sxs-lookup"><span data-stu-id="e760e-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="e760e-110">要使用的安全性提供者</span><span class="sxs-lookup"><span data-stu-id="e760e-110">Which Security Provider To Use</span></span>](which-security-provider-to-use.md)
-   [<span data-ttu-id="e760e-111">控制用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="e760e-111">Controlling Client Authentication</span></span>](controlling-client-authentication.md)
-   [<span data-ttu-id="e760e-112">選擇驗證層級</span><span class="sxs-lookup"><span data-stu-id="e760e-112">Choosing an Authentication Level</span></span>](choosing-an-authentication-level.md)
-   [<span data-ttu-id="e760e-113">選擇安全性 QOS 選項</span><span class="sxs-lookup"><span data-stu-id="e760e-113">Choosing Security QOS Options</span></span>](choosing-security-qos-options.md)
-   [<span data-ttu-id="e760e-114">常見錯誤：假設 RpcServerRegisterAuthInfo 可防止未經授權的使用者呼叫您的伺服器</span><span class="sxs-lookup"><span data-stu-id="e760e-114">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [<span data-ttu-id="e760e-115">回撥</span><span class="sxs-lookup"><span data-stu-id="e760e-115">Callbacks</span></span>](callbacks.md)
-   [<span data-ttu-id="e760e-116">Null 會話</span><span class="sxs-lookup"><span data-stu-id="e760e-116">Null Sessions</span></span>](null-sessions.md)
-   [<span data-ttu-id="e760e-117">使用/robust 旗標</span><span class="sxs-lookup"><span data-stu-id="e760e-117">Use the /robust Flag</span></span>](use-the-robust-flag.md)
-   [<span data-ttu-id="e760e-118">適用于更佳介面和方法設計的 IDL 技術</span><span class="sxs-lookup"><span data-stu-id="e760e-118">IDL Techniques for Better Interface and Method Design</span></span>](idl-techniques-for-better-interface-and-method-design.md)
-   [<span data-ttu-id="e760e-119">Strict 和 Type Strict 內容控制碼</span><span class="sxs-lookup"><span data-stu-id="e760e-119">Strict and Type Strict Context Handles</span></span>](strict-and-type-strict-context-handles.md)
-   [<span data-ttu-id="e760e-120">不要信任您的對等</span><span class="sxs-lookup"><span data-stu-id="e760e-120">Do Not Trust Your Peer</span></span>](do-not-trust-your-peer.md)
-   [<span data-ttu-id="e760e-121">請勿使用端點安全性</span><span class="sxs-lookup"><span data-stu-id="e760e-121">Do Not Use Endpoint Security</span></span>](do-not-use-endpoint-security.md)
-   [<span data-ttu-id="e760e-122">請小心在相同進程中執行其他 RPC 端點</span><span class="sxs-lookup"><span data-stu-id="e760e-122">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [<span data-ttu-id="e760e-123">確認伺服器是否為其宣稱的身分</span><span class="sxs-lookup"><span data-stu-id="e760e-123">Verify The Server Is Who It Claims To Be</span></span>](verify-the-server-is-who-it-claims-to-be.md)
-   [<span data-ttu-id="e760e-124">使用主流通訊協定序列</span><span class="sxs-lookup"><span data-stu-id="e760e-124">Use Mainstream Protocol Sequences</span></span>](use-mainstream-protocol-sequences.md)
-   [<span data-ttu-id="e760e-125">我的 RPC 伺服器現在有多安全？</span><span class="sxs-lookup"><span data-stu-id="e760e-125">How Secure is my RPC Server Now?</span></span>](how-secure-is-my-rpc-server-now.md)

 

 