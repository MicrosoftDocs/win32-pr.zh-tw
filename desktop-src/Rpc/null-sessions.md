---
title: Null 會話
description: 有時抵達 null 會話的呼叫可能會顯示為已驗證的呼叫。
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462416"
---
# <a name="null-sessions"></a><span data-ttu-id="6ed01-103">Null 會話</span><span class="sxs-lookup"><span data-stu-id="6ed01-103">Null Sessions</span></span>

<span data-ttu-id="6ed01-104">有時抵達 null 會話的呼叫可能會顯示為已驗證的呼叫。</span><span class="sxs-lookup"><span data-stu-id="6ed01-104">Sometimes a call arriving on the null session can appear like an authenticated call.</span></span> <span data-ttu-id="6ed01-105">具體而言，呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 函數會傳回用於呼叫的驗證層級和安全性提供者。</span><span class="sxs-lookup"><span data-stu-id="6ed01-105">Specifically, calling the [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) function returns the authentication level and security provider used for the call.</span></span> <span data-ttu-id="6ed01-106">這種作業不表示呼叫不在 null 會話上。</span><span class="sxs-lookup"><span data-stu-id="6ed01-106">This operation does not mean the call was not on a null session.</span></span> <span data-ttu-id="6ed01-107">這兩個問題是直角的。</span><span class="sxs-lookup"><span data-stu-id="6ed01-107">The two issues are orthogonal.</span></span> <span data-ttu-id="6ed01-108">在 Microsoft Windows 2000 上，遠端程序呼叫可以嘗試模擬呼叫者，並在模擬之後檢查許可權。</span><span class="sxs-lookup"><span data-stu-id="6ed01-108">On Microsoft Windows 2000, a remote procedure call can attempt to impersonate a caller and check the permissions after impersonation.</span></span> <span data-ttu-id="6ed01-109">在 Microsoft Windows XP 上，呼叫 [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) 函式並檢查 **NullSession** 旗標會更快。</span><span class="sxs-lookup"><span data-stu-id="6ed01-109">On Microsoft Windows XP, it is faster to call the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function and check for the **NullSession** flag.</span></span>

<span data-ttu-id="6ed01-110">Windows 2000 和 Windows XP 之間存在另一個相關的差異。</span><span class="sxs-lookup"><span data-stu-id="6ed01-110">Another relevant difference exists between Windows 2000 and Windows XP.</span></span> <span data-ttu-id="6ed01-111">如果指定了 [ \_ \_ 僅允許 \_ 安全的] 旗標，則 \_ 會在 Windows 2000 中呼叫 null 會話。</span><span class="sxs-lookup"><span data-stu-id="6ed01-111">If only the RPC\_IF\_ALLOW\_SECURE\_ONLY flag is specified, calls on the null session go through in Windows 2000.</span></span> <span data-ttu-id="6ed01-112">在 Windows XP 中，在預設安全性設定的一般情況下，當指定此旗標時，會拒絕對 null 會話的呼叫，並拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="6ed01-112">In Windows XP, with the general tightening of default security settings, when this flag is specified, calls on the null session are rejected with access denied.</span></span> <span data-ttu-id="6ed01-113">但是，即使是使用 RPC \_ [ \_ \_ 僅允許安全] 旗標 \_ ，rpc 仍無法保證呼叫使用者的許可權等級。</span><span class="sxs-lookup"><span data-stu-id="6ed01-113">However, even with the RPC\_IF\_ALLOW\_SECURE\_ONLY flag, RPC does not guarantee the privilege level of the calling user.</span></span> <span data-ttu-id="6ed01-114">所有 RPC 檢查都是使用者有有效的認證。</span><span class="sxs-lookup"><span data-stu-id="6ed01-114">All RPC checks is that the user has valid credentials.</span></span> <span data-ttu-id="6ed01-115">呼叫使用者可能會使用 guest 帳戶或其他低許可權帳戶。</span><span class="sxs-lookup"><span data-stu-id="6ed01-115">It is possible that the calling user is using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="6ed01-116">\_如果 \_ \_ 使用 [僅允許安全] \_ ，請確定伺服器在 RPC 之後不會採用高許可權。</span><span class="sxs-lookup"><span data-stu-id="6ed01-116">Make sure the server does not assume high privilege once RPC\_IF\_ALLOW\_SECURE\_ONLY is used.</span></span>

 

 




